---
generated: '2026-07-27'
method: generated
name: Bulk export an SP Energy Networks dataset
description: Take a whole SP Energy Networks dataset without paging — pick a supported export format and pull it in one request.
api: openapi/scottishpower-spen-open-data-explore-api-openapi.json
operations: [getDataset, listDatasetExportFormats, exportRecords, exportRecordsCSV, exportRecordsParquet, exportRecordsGPX, getDatasetAttachments]
source: >-
  Every operationId verified verbatim in
  openapi/scottishpower-spen-open-data-explore-api-openapi.json. Format list and
  error behaviour verified live on 2026-07-27.
---

# Bulk export an SP Energy Networks dataset

The records endpoint is capped (100 rows without a `group_by`, `offset+limit` under 10000). The exports endpoints are not — this is how you take a whole dataset, and it costs one request against the daily quota instead of hundreds.

Base URL: `https://spenergynetworks.opendatasoft.com/api/explore/v2.1`

## Auth
- None required for anonymously-readable datasets; optional API key otherwise. See `authentication/scottishpower-authentication.yml`.

## Idempotency
- GET only — safe to retry. See `conventions/scottishpower-conventions.yml`.

## Steps
1. **Confirm the dataset and its size** — `getDataset` (`GET /catalog/datasets/{dataset_id}`) for the field schema and record count. A dataset like `spen-weekly-substation-carbon-estimate` carries 310,125 rows, which is 3,102 paged calls versus one export.
2. **Check what formats it offers** — `listDatasetExportFormats` (`GET /catalog/datasets/{dataset_id}/exports`). Platform formats include `csv`, `json`, `xlsx`, `parquet`, `geojson`, `gpx`, `rdf`, `ttl`, `dublin_core` and the `dcat_ap_*` profiles. An unsupported value returns 400 `InvalidExportFormat` and the error message lists every valid format.
3. **Export** — one of:
   - `exportRecords` (`GET /catalog/datasets/{dataset_id}/exports/{format}`) for any format,
   - `exportRecordsCSV` (`.../exports/csv`) — note CSV output carries a byte-order mark by default,
   - `exportRecordsParquet` (`.../exports/parquet`) for analytics loads,
   - `exportRecordsGPX` (`.../exports/gpx`) for the geographic datasets (substation and licence-area polygons).
   You can still narrow the export with ODSQL `select`, `where` and `group_by` — `group_by` works on export endpoints in v2.1.
4. **Pick up the supporting files** — `getDatasetAttachments` (`GET /catalog/datasets/{dataset_id}/attachments`) for methodology notes and documents published alongside the data.

## Errors
- 403 `ForbiddenAccess` — the dataset's data is not readable by the calling identity. Most SPEN datasets refuse anonymous record/export access even though their metadata is public.
- 400 `InvalidExportFormat` — use a format returned by step 2.
- See `errors/scottishpower-problem-types.yml`.

## Notes
- Quota is per request, not per row, so an export is the cheapest way to consume a large dataset. See `rate-limits/scottishpower-rate-limits.yml`.
- Attribute SP Energy Networks under the SP Energy Networks Open Data Licence (CC BY 4.0 basis) when republishing.
