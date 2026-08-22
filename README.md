# Canada Health Infoway (canada-health-infoway)

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

Canada Health Infoway is an independent, federally funded not-for-profit organization that leads the adoption of digital health and pan-Canadian interoperability across Canada's province- and territory-fragmented healthcare system. Infoway stewards the pan-Canadian FHIR interoperability specifications (CA Core+ and the CA Baseline profiles, developed with the Canadian Institute for Health Information) and operates the Canadian FHIR Registry, the Canadian URI Registry, and a national Terminology Gateway. Its developer-facing API surface, published through the Accelero developer portal, is a HAPI-FHIR R4 (4.0.1) Terminology Service plus a companion RESTful Terminology API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/canada-health-infoway/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/canada-health-infoway/refs/heads/main/apis.yml)

**Home market:** Canada

## Tags

- Healthcare
- Canada
- FHIR
- HL7
- Interoperability
- Terminology
- National Health System
- Digital Health
- Standards
- CA Core

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Infoway FHIR Terminology Service API

HL7 FHIR R4 (4.0.1) terminology service from Canada Health Infoway's Terminology Gateway (HAPI FHIR), exposing CodeSystem, ValueSet, ConceptMap, and OperationDefinition resources with read/vread/history/search plus the `$lookup`, `$expand`, `$translate`, and `$validate-code` terminology operations. A live FHIR CapabilityStatement is served at `/fhir/v1/metadata` (anonymous).

- **Human URL:** [https://termapi.infoway-inforoute.ca/fhir/fhir-apidocs/v1/swagger-ui](https://termapi.infoway-inforoute.ca/fhir/fhir-apidocs/v1/swagger-ui)
- **Base URL:** `https://termapi.infoway-inforoute.ca/fhir/v1`

#### Properties

- [OpenAPI](openapi/infoway-fhir-terminology-service-api-openapi.json) (Swagger 2.0)
- [CapabilityStatement](fhir/infoway-terminology-gateway-capabilitystatement.json) (FHIR R4)
- [API Reference](https://termapi.infoway-inforoute.ca/fhir/fhir-apidocs/v1/swagger-ui)
- [Documentation](https://accelero.infoway-inforoute.ca/en/tools/developer-tools/terminology-service-api)

### Infoway Terminology Service API

RESTful (non-FHIR) terminology API for browsing and downloading Canadian terminology content — code systems, subsets (value sets), maps, resource locations, and packages — with delta/versioning, session login (basic credentials, SSO token, or JWT), and webhook-style notification subscriptions.

- **Human URL:** [https://termapi.infoway-inforoute.ca/schema/v1/swaggerui/index.html](https://termapi.infoway-inforoute.ca/schema/v1/swaggerui/index.html)
- **Base URL:** `https://termapi.infoway-inforoute.ca/rest/v1`

#### Properties

- [OpenAPI](openapi/infoway-terminology-service-api-openapi.json) (Swagger 2.0)
- [API Reference](https://termapi.infoway-inforoute.ca/schema/v1/swaggerui/index.html)
- [Documentation](https://accelero.infoway-inforoute.ca/en/tools/developer-tools/terminology-service-api)

## Standards Stewardship

Beyond the terminology APIs, Infoway stewards Canada's pan-Canadian FHIR baseline:

- **CA Core+** — pan-Canadian core FHIR specification (with CIHI): [initiative](https://accelero.infoway-inforoute.ca/en/initiatives/pan-canadian-core-specifications)
- **Canadian FHIR Registry** — national FHIR profile repository: [tool](https://accelero.infoway-inforoute.ca/en/tools/developer-tools/canadian-fhir-registry)
- **Canadian URI Registry** — identifier/code-system namespaces: [tool](https://accelero.infoway-inforoute.ca/en/tools/developer-tools/canadian-uri-registry)
- **pan-Canadian Interoperability Specifications** — [InfoScribe](https://infoscribe.infoway-inforoute.ca/display/PCI)

## Common Properties

- [Website](https://www.infoway-inforoute.ca/en/)
- [Developer Portal](https://accelero.infoway-inforoute.ca/en/tools/developer-tools)
- [Documentation](https://www.infoway-inforoute.ca/en/what-we-do/connected-care/digital-health-standards)
- [Sign Up](https://accelero.infoway-inforoute.ca/en/register)
- [Blog](https://www.infoway-inforoute.ca/en/blog)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
