# ScottishPower (scottishpower)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
