---
generated: '2026-07-27'
method: generated
name: Harvest the SP Energy Networks catalogue as DCAT
description: Pull the whole 150-dataset SP Energy Networks catalogue as DCAT-AP RDF/XML (or CSV) to index it in another data portal or catalogue.
api: openapi/scottishpower-spen-open-data-explore-api-openapi.json
operations: [getDatasets, listExportFormats, exportCatalogDCAT, exportCatalogCSV, exportDatasets]
source: >-
  Every operationId verified verbatim in
  openapi/scottishpower-spen-open-data-explore-api-openapi.json. The DCAT export
  was verified live (HTTP 200, application/rdf+xml) on 2026-07-27.
---

# Harvest the SP Energy Networks catalogue as DCAT

For catalogue-to-catalogue federation: take SP Energy Networks' entire published inventory in one machine-readable document rather than crawling it dataset by dataset. This is the path a national or regional data portal uses to index a UK distribution network operator's holdings.

Base URL: `https://spenergynetworks.opendatasoft.com/api/explore/v2.1`

## Auth
- None. The catalogue and its exports are fully anonymous — verified 2026-07-27 with no key and no account.

## Idempotency
- GET only — safe to retry. See `conventions/scottishpower-conventions.yml`.

## Steps
1. **Size the catalogue** — `getDatasets` (`GET /catalog/datasets?limit=1`) and read `total_count`. It was 150 at harvest, split 145 / 1 between SP Energy Networks SC389555 and SP Distribution SC189125.
2. **Check the catalogue export formats** — `listExportFormats` (`GET /catalog/exports`).
3. **Harvest the DCAT document** — `exportCatalogDCAT` (`GET /catalog/exports/dcat{dcat_ap_format}`). The plain `dcat` form returns DCAT-AP RDF/XML; national profiles `dcat_ap_ch`, `dcat_ap_de`, `dcat_ap_se`, `dcat_ap_sp`, `dcat_ap_it`, `dcat_ap_vl` and `dcat_ap_benap` are also available. The full document was ~4.2 MB of `application/rdf+xml` at harvest.
4. **Or take a flat inventory** — `exportCatalogCSV` (`GET /catalog/exports/csv`), or `exportDatasets` (`GET /catalog/exports/{format}`) for `json`, `xlsx`, `ttl`, `dublin_core`, `rss` or `sitemap`.

## Errors
- 400 `InvalidExportFormat` — the message enumerates every valid format; pick from it.
- See `errors/scottishpower-problem-types.yml`.

## Notes
- The catalogue records metadata for all 150 datasets, including ones whose records are not anonymously readable — so a harvest gives a complete picture of what SP Energy Networks publishes, even where the data itself is gated. See `data-model/scottishpower-data-model.yml`.
- Re-harvest cadence: there is no status page and no dated changelog for this portal, so poll the catalogue (or the per-dataset `/explore/dataset/{id}/rss/` feeds) rather than waiting for a notification. See `lifecycle/scottishpower-lifecycle.yml`.
- Licence: SP Energy Networks Open Data Licence, based on CC BY 4.0. Carry the attribution into your catalogue records.
