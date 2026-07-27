---
generated: '2026-07-27'
method: generated
name: Find and query an SP Energy Networks dataset
description: Discover a dataset in the SP Energy Networks open data catalogue, read its field schema, then query its records with ODSQL.
api: openapi/scottishpower-spen-open-data-explore-api-openapi.json
operations: [getDatasets, getDatasetsFacets, getDataset, getRecords]
source: >-
  Every operationId verified verbatim in
  openapi/scottishpower-spen-open-data-explore-api-openapi.json. Behaviour notes
  verified live against
  https://spenergynetworks.opendatasoft.com/api/explore/v2.1 on 2026-07-27.
---

# Find and query an SP Energy Networks dataset

The core read loop for SP Energy Networks (ScottishPower's electricity distribution and transmission licensee) open network data: 150 datasets covering the embedded capacity register, substation demand, LV monitoring, smart-meter penetration and flexibility.

Base URL: `https://spenergynetworks.opendatasoft.com/api/explore/v2.1`

## Auth
- None required. The catalogue is fully anonymous.
- Optional API key raises quotas and unlocks account-visible datasets: `Authorization: Apikey <API_KEY>` header, or `apikey=<API_KEY>` query parameter. See `authentication/scottishpower-authentication.yml`.

## Idempotency
- The API supports HTTP `GET` only. Every step below is safe and idempotent — retry freely. See `conventions/scottishpower-conventions.yml`.

## Steps
1. **Narrow the catalogue** — `getDatasetsFacets` (`GET /catalog/facets`) with `facet=publisher` (or `theme`, `keyword`) to see what dimensions exist and how many datasets sit under each. Publishers at harvest: SP Energy Networks SC389555 (145) and SP Distribution SC189125 (1).
2. **Find the dataset** — `getDatasets` (`GET /catalog/datasets`) with an ODSQL `where` (e.g. `where=search(dataset_id, "substation")`) and `select=dataset_id` to keep the payload small. Read `total_count` and `results[]`. Identifiers are human-readable slugs such as `spen-weekly-substation-carbon-estimate`.
3. **Read the schema** — `getDataset` (`GET /catalog/datasets/{dataset_id}`) and take `fields[]`: each entry has `name`, `label`, `type` and `annotations` (`facet`, `sortable`). Only use these names in a `select`, `where` or `group_by`, or you get a 400 `ODSQLError` naming the unknown field.
4. **Query the records** — `getRecords` (`GET /catalog/datasets/{dataset_id}/records`) with `select`, `where`, `order_by`, `limit` and `offset`. Response envelope is `{total_count, results, links}`.

## Limits
- `limit` max 100 without a `group_by` (max 20000 with one), and `offset + limit` must stay below 10000. `limit=99999` returns 400 `InvalidRESTParameterError`.
- For anything larger, switch to the export skill — `/exports` has no row cap.
- Anonymous quota is 5,000 requests/day; read `X-RateLimit-Remaining` on every response. See `rate-limits/scottishpower-rate-limits.yml`.

## Errors
- **403 `ForbiddenAccess` on `/records` is normal, not exceptional.** Metadata for all 150 datasets is public, but most datasets refuse records anonymously — 87 of 100 probed on 2026-07-27. On 403, fall back to the dataset metadata from step 3, try the export endpoints, or supply an API key.
- 404 `NotFoundResource` means the `dataset_id` does not exist on this domain — go back to step 2.
- Errors are not RFC 9457; see `errors/scottishpower-problem-types.yml` for the three envelope shapes.

## Notes
- Live example payloads for steps 1, 2 and 4 are in `examples/`.
- Data is published under the SP Energy Networks Open Data Licence (based on CC BY 4.0) — attribute SP Energy Networks when you republish.
