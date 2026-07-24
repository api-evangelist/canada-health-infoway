# Canada Health Infoway (canada-health-infoway)

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
