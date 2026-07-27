# ScottishPower (scottishpower)

ScottishPower (Scottish Power Limited, Glasgow) is one of the "Big Six" British energy companies and has been wholly owned by Spain's Iberdrola since 2007. It spans three regulated roles at once: ScottishPower Energy Retail supplies electricity and gas to British homes and businesses; SP Energy Networks is the licensed distribution network operator for central and southern Scotland (SP Distribution), Merseyside, Cheshire and North Wales (SP Manweb), plus transmission owner for southern Scotland (SP Transmission); and ScottishPower Renewables develops onshore and offshore wind. That structure produces the sharpest version of this sector's split. On the consumer side there is nothing — Britain has no Consumer Data Right, no Green Button mandate and no consumer energy data-portability obligation, and ScottishPower publishes no developer portal and no documented route to an individual customer's usage or billing data. On the network side, Ofgem's Data Best Practice Guidance — a licence condition under RIIO-ED2 — obliges network operators to treat their data as "presumed open", and SP Energy Networks actually built it: 150 datasets served through a live, fully anonymous Opendatasoft Explore API v2.1 with a real OpenAPI 3.0.3 contract. Britain mandated the infrastructure and the network data, not the data right.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/scottishpower/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/scottishpower/refs/heads/main/apis.yml)

## Tags

- Energy
- United Kingdom
- Utilities
- Electricity
- Gas
- Energy Retailer
- Smart Metering
- Grid
- Open Data
- Distribution Network Operator
- Renewables
- Energy Markets

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

### SP Energy Networks Open Data Explore API

The live, anonymous REST API behind the SP Energy Networks Open Data Portal — ScottishPower's regulated distribution and transmission arm publishing its network data under Ofgem's Data Best Practice "presumed open" licence condition. Implements the Opendatasoft Explore API v2.1 contract (OpenAPI 3.0.3, 16 paths) over a catalogue of 150 datasets covering the embedded capacity register, network flow, historic substation demand curves, LV monitoring, smart-meter penetration by transformer, secondary substations, generation heat maps, connections insight and per-dataset data-quality scores. Verified on 2026-07-27 with no API key and no account.

- **Human URL:** [https://spenergynetworks.opendatasoft.com/api/explore/v2.1/console](https://spenergynetworks.opendatasoft.com/api/explore/v2.1/console)
- **Base URL:** `https://spenergynetworks.opendatasoft.com/api/explore/v2.1`

#### Tags

- Open Data
- Energy
- Electricity
- Grid
- Distribution Network Operator
- Embedded Capacity Register
- Smart Metering
- Flexibility
- United Kingdom

#### Properties

- [OpenAPI](openapi/scottishpower-spen-open-data-explore-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [API Reference](https://spenergynetworks.opendatasoft.com/api/explore/v2.1/console)
- [Documentation](https://help.opendatasoft.com/apis/ods-explore-v2/)
- [Documentation](https://spenergynetworks.opendatasoft.com/pages/support-help-main/)
- [Getting Started](https://spenergynetworks.opendatasoft.com/explore/)
- [Licensing](https://spenergynetworks.opendatasoft.com/p/sp-energy-networks-open-data-licence/)
- [Terms of Service](https://spenergynetworks.opendatasoft.com/terms/)
- [Glossary](https://spenergynetworks.opendatasoft.com/glossary/)

### SP Energy Networks Open Data Search API (v1.0)

The legacy Opendatasoft Search API v1.0 still served alongside Explore v2.1 on the SP Energy Networks Open Data Portal. Verified anonymously on 2026-07-27: `GET /api/datasets/1.0/search/?rows=1` returned HTTP 200 with `nhits` 150, matching the v2.1 catalogue exactly. Recorded because it is live and callable without credentials, but it is superseded.

- **Human URL:** [https://help.opendatasoft.com/apis/ods-search-v1/](https://help.opendatasoft.com/apis/ods-search-v1/)
- **Base URL:** `https://spenergynetworks.opendatasoft.com/api/datasets/1.0`

#### Tags

- Open Data
- Search
- Energy
- Legacy
- United Kingdom

#### Properties

- [Documentation](https://help.opendatasoft.com/apis/ods-search-v1/)
- [API Reference](https://spenergynetworks.opendatasoft.com/api/datasets/1.0/search/)
- [Licensing](https://spenergynetworks.opendatasoft.com/p/sp-energy-networks-open-data-licence/)

## Common Properties

- [Website](https://www.scottishpower.co.uk/)
- [Website](https://www.spenergynetworks.co.uk/)
- [Portal Home](https://spenergynetworks.opendatasoft.com/)
- [Documentation](https://www.spenergynetworks.co.uk/pages/energy_data_hub.aspx)
- [Licensing](https://spenergynetworks.opendatasoft.com/p/sp-energy-networks-open-data-licence/)
- [Licensing](https://spenergynetworks.opendatasoft.com/p/sp-energy-networks-shared-data-licence/)
- [Terms of Service](https://spenergynetworks.opendatasoft.com/terms/terms-and-conditions/)
- [Privacy Policy](https://spenergynetworks.opendatasoft.com/terms/privacy-policy/)
- [Support](https://spenergynetworks.opendatasoft.com/pages/support-help-main/)
- [Forum](https://community.scottishpower.co.uk/)
- [FAQ](https://spenergynetworks.opendatasoft.com/p/faq/)

## Mandate Posture

| Field | Value |
| --- | --- |
| Home market | United Kingdom |
| Mandate regime | `smart-meter-infrastructure` — Smart DCC / Smart Energy Code |
| Mandate status | `live-claimed-unverified` — no public register entry or endpoint could be called |
| Second mandate | Ofgem Data Best Practice, RIIO-ED2 SLC 9.5 — `live-implemented`, verified by anonymous HTTP 200 |
| Consumer data right | None. The UK has no CDR or Green Button equivalent. |
| Data standard | No consumer-data standard reference found. Open data via Opendatasoft Explore v2.1 + DCAT-AP catalogue export. |
| Consumer data API | No |
| Market/network data open | Yes — 150 datasets, anonymous, CC BY 4.0-derived licence |
| Access gate | `self-serve` (open data); nothing published for consumer data |
| Auth model | Anonymous HTTPS GET; optional `apikey` query parameter for higher quotas |

## Maintainers

- **Kin Lane** — kin@apievangelist.com
