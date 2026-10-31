# ScottishPower

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

ScottishPower (Scottish Power Limited, Glasgow) is one of the "Big Six" British energy companies and has been wholly owned by Spain's Iberdrola since 2007. It is unusual in the post-liberalisation UK market for still spanning three regulated roles at once: ScottishPower Energy Retail supplies electricity and gas to millions of British homes and businesses; SP Energy Networks is the licensed distribution network operator for central and southern Scotland (SP Distribution), Merseyside, Cheshire and North Wales (SP Manweb), plus the transmission owner for southern Scotland (SP Transmission); and ScottishPower Renewables develops and operates onshore and offshore wind. That structure produces the sharpest possible version of this sector's split, and the split is the finding. On the consumer side there is nothing — Britain has no Consumer Data Right, no Green Button mandate and no consumer energy data-portability obligation of any kind, and ScottishPower publishes no developer portal, no self-serve API programme and no documented way for a third party to obtain an individual customer's usage or billing data. developer.scottishpower.co.uk, developers.scottishpower.co.uk, data.scottishpower.co.uk and docs.scottishpower.co.uk do not resolve at all, api.scottishpower.co.uk exists in DNS but returns HTTP 403, and www.scottishpower.co.uk returns HTTP 403 to every anonymous client on every path including /robots.txt. The only public account of ScottishPower's API programme is a WSO2 customer story describing an API Manager deployment used to expose services to commercial partners — an internal, partner-gated estate, not a developer programme. On the network side the picture inverts completely. Ofgem's Data Best Practice Guidance, made a licence condition under the RIIO-ED2 price control (Special Licence Condition 9.5), obliges electricity network licensees to treat their data as "presumed open", and SP Energy Networks has actually built that: the SP Energy Networks Open Data Portal at spenergynetworks.opendatasoft.com serves 150 datasets — embedded capacity register, network flow, historic substation demand, LV monitoring, smart-meter penetration, generation heat maps, flexibility and connections data — through a live, fully anonymous Opendatasoft Explore API v2.1 with a real OpenAPI 3.0.3 contract, CORS wide open, a 5,000 request/day anonymous quota, a DCAT-AP catalogue export, and an SP Energy Networks Open Data Licence based on Creative Commons Attribution 4.0. Britain mandated the infrastructure and the network data, not the data right — ScottishPower is the proof. Its smart-meter obligation runs through the Smart DCC and the Smart Energy Code, which is an infrastructure monopoly for licensed parties rather than a consumer data right, and no public register entry or endpoint for that obligation could be verified from outside.

**Areas:** Energy · United Kingdom · Utilities · Electricity · Gas · Energy Retailer · Smart Metering · Grid · Open Data · Distribution Network Operator · Renewables · Energy Markets

## ScottishPower on APIs.io

Everything profiled for ScottishPower is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/scottishpower/](https://apis.io/providers/scottishpower/)** — or go straight to one of the APIs or properties below.

### APIs (3)

- [SP Energy Networks Open Data Search API (v1.0)](https://apis.io/apis/scottishpower/spen-open-data-search-api-v1/) — The legacy Opendatasoft Search API v1.0 still served alongside Explore v2.1 on the SP Energy Networks Open Data Portal. Verified anonymously on 2026-07-27:…
- [ScottishPower Catalog API](https://apis.io/apis/scottishpower/scottishpower-catalog-api/) — API to enumerate datasets
- [ScottishPower Dataset API](https://apis.io/apis/scottishpower/scottishpower-dataset-api/) — API to work on records

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [scottishpower-spen-open-data](https://apis.io/servers/scottishpower/scottishpower-spen-open-data/)

#### Examples (3)

Example requests and responses.

- [Scottishpower Catalog Facets Example](https://apis.io/examples/scottishpower/scottishpower-catalog-facets-example/)
- [Scottishpower List Datasets Example](https://apis.io/examples/scottishpower/scottishpower-list-datasets-example/)
- [Scottishpower Query Records Example](https://apis.io/examples/scottishpower/scottishpower-query-records-example/)

#### Collections (1)

Postman and Open Collection request collections.

- [Explore API](https://apis.io/collections/scottishpower/open-scottishpower-spen-open-data-explore-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Scottishpower Spen Open Data Explore Api Overlay](https://apis.io/overlays/scottishpower/scottishpower-spen-open-data-explore-api-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Scottishpower Authentication](https://apis.io/security/scottishpower/scottishpower-authentication/)
- [Scottishpower Domain Security](https://apis.io/security/scottishpower/scottishpower-domain-security/)
- [Scottishpower Vulnerability Disclosure](https://apis.io/security/scottishpower/scottishpower-vulnerability-disclosure/)

#### Rate limits (1)

Published request limits.

- [Scottishpower Rate Limits](https://apis.io/rate-limits/scottishpower/scottishpower-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.scottishpower.co.uk/)
- [Documentation](https://www.spenergynetworks.co.uk/pages/energy_data_hub.aspx)
- [Getting started](https://spenergynetworks.opendatasoft.com/explore/)
- [API reference](https://spenergynetworks.opendatasoft.com/api/explore/v2.1/console)
- [Sign up](https://spenergynetworks.opendatasoft.com/signup/)
- [Support](https://spenergynetworks.opendatasoft.com/pages/support-help-main/)
- [Security](https://spenergynetworks.opendatasoft.com/.well-known/security.txt)
- [Terms of service](https://spenergynetworks.opendatasoft.com/terms/terms-and-conditions/)
- [Privacy policy](https://spenergynetworks.opendatasoft.com/terms/privacy-policy/)

## API Evangelist rating

**Kin Score 40.3** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 17.0 |
| Contract governance | 4.5 |
| Operational transparency | 55.3 |
| Developer ergonomics | 56.5 |
| Access clarity | 34.2 |

**Agent readiness 35.4** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 32.0** — Energy & Utilities

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/scottishpower/](https://apis.io/providers/scottishpower/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ScottishPower: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/scottishpower/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
