# Lufthansa Cargo

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

Lufthansa Cargo AG is the air freight arm of the Lufthansa Group, headquartered in Frankfurt, Germany. It sells and operates belly capacity across the Lufthansa passenger fleet plus its own Boeing 777F freighters, and runs the Frankfurt Cargo Center hub, so it sits in the chain as the airline carrier between the freight forwarder and the destination handling agent. Its API posture is real but two-speed: a live Apigee developer portal at developer.lufthansa-cargo.com publishes four OpenAPI 3.0 contracts anonymously downloadable without a login (Routing Offer, Shipment Tracking, Shipment Tracking Subscribe, Station Information), while six further API products in the same portfolio - smartBooking, Truck PreAdvice, ULD Status, AirMail, CargoXML and CargoIMP - are published only as info-block stubs carrying the sentence that access is granted upon prior approval and agreement. Registration is reviewed by Lufthansa Cargo API managers before keys are issued and production access requires successful test-environment validation, so this is application-approval, not self-serve. The published REST surface is a proprietary Lufthansa Cargo shape, but it carries open air-cargo vocabulary inside it - IATA AWB prefix 020 plus 8-digit AWB numbers, 3-letter IATA station codes and the IATA cargo status code set (RCS, MAN, DEP, ARR, RCF, NFD, DLV) - while the legacy Cargo-IMP and Cargo-XML EDI message sets remain in the portfolio as gated products and IATA ONE Record went live in July 2026 through the IBS Software ONE Record server rather than as anything Lufthansa Cargo publishes itself.

**Areas:** Logistics · Supply Chain · Germany · Air Cargo · Freight · Track and Trace · Standards · Aviation

## Lufthansa Cargo on APIs.io

Everything profiled for Lufthansa Cargo is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/lufthansa-cargo/](https://apis.io/providers/lufthansa-cargo/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Lufthansa Cargo Shipment Tracking API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-shipment-tracking-api/) — Retrieves the current status of an air freight shipment by IATA Air Waybill, keyed on a 3-digit AWB prefix (020 = Lufthansa Cargo) plus an 8-digit AWB…
- [Lufthansa Cargo Shipment Tracking Subscribe API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-shipment-tracking-subscribe-api/) — Subscription API that pushes shipment milestone updates to a caller-supplied HTTPS callback URL. Create, read, update, delete and list subscriptions for a…
- [Lufthansa Cargo Smart Booking API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-smartbooking-api/) — Prior-agreement API. Lufthansa Cargo's digital booking connect for forwarders wiring an in-house system to the carrier and for ePlatforms integrating LH…
- [Lufthansa Cargo TruckPreAdvice API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-truck-preadvice-api/) — Prior-agreement API. Manages advance notification of truck deliveries as an alternative to the Quick Drop-Off/Pick-Up page in the Lufthansa ePortal.…
- [Lufthansa Cargo ULDStatus API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-uld-status-api/) — Prior-agreement API behind the smartULD add-on service. Exposes sensory data from smart Unit Load Devices - ambient temperature, battery level, geodata -…
- [Lufthansa Cargo CargoXML API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-cargoxml-api/) — Prior-agreement API product named CargoXML in the Lufthansa Cargo portfolio, referencing the IATA Cargo-XML message standard. The portal publishes an…
- [Lufthansa Cargo CargoIMP API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-cargoimp-api/) — Prior-agreement API product listed as CargoIMP in the portfolio, referencing the legacy IATA Cargo Interchange Message Procedures EDI message set. The…
- [Lufthansa Cargo AirMail API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-airmail-api/) — Prior-agreement API product covering airmail carriage for postal operators. The portal publishes an OpenAPI 3.0.3 info block titled "AirMail APIs" whose…
- [Lufthansa Cargo Routes API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-routes-api/) — The routes API from Lufthansa Cargo — 1 operation(s) for routes.
- [Lufthansa Cargo Stations API](https://apis.io/apis/lufthansa-cargo/lufthansa-cargo-stations-api/) — The stations API from Lufthansa Cargo — 3 operation(s) for stations.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Collections (4)

Postman and Open Collection request collections.

- [Routing Offer API](https://apis.io/collections/lufthansa-cargo/open-lufthansa-cargo-routing-offer-api/)
- [Shipment Tracking API](https://apis.io/collections/lufthansa-cargo/open-lufthansa-cargo-shipment-tracking-api/)
- [Shipment Tracking Subscribe API](https://apis.io/collections/lufthansa-cargo/open-lufthansa-cargo-shipment-tracking-subscribe-api/)
- [Station Information API](https://apis.io/collections/lufthansa-cargo/open-lufthansa-cargo-station-information-api/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.lufthansa-cargo.com/)
- [Documentation](https://developer.lufthansa-cargo.com/how-to-connect)
- [Sign up](https://developer.lufthansa-cargo.com/login)
- [Support](https://developer.lufthansa-cargo.com/contact)
- [Changelog](https://developer.lufthansa-cargo.com/news)
- [Blog](https://www.lufthansa-cargo.com/en/ci/newsroom)
- [Terms of service](https://developer.lufthansa-cargo.com/terms)
- [GitHub](https://github.com/LufthansaCargo)

## API Evangelist rating

**Kin Score 17.0** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 57.1 |
| Contract quality | 50.1 |
| Contract governance | 0.0 |
| Operational transparency | 2.6 |
| Developer ergonomics | 2.4 |
| Access clarity | 0.0 |

**Agent readiness 18.0** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 5.9** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/lufthansa-cargo/](https://apis.io/providers/lufthansa-cargo/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Lufthansa Cargo: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/lufthansa-cargo/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
