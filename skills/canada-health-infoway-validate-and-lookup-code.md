---
name: Validate and look up a clinical code (FHIR terminology)
description: Authenticate to the Infoway Terminology Gateway, then use FHIR terminology operations to look up a code's properties and validate it against a value set.
api: openapi/infoway-fhir-terminology-service-api-openapi.json
operations: [getCapabilityStatement, lookupConcept, findValueSets, getValueSetCodeValidation]
---

# Validate and look up a clinical code

Use this skill to resolve and validate a code against a Canadian code system / value set on Canada Health Infoway's FHIR R4 Terminology Gateway.

Base URL: `https://termapi.infoway-inforoute.ca/fhir/v1`

## Auth
Terminology content is gated. Register free at https://accelero.infoway-inforoute.ca/en/register, then authenticate. Pass credentials as the `auth` query parameter (Base64 `username:password`) or `Authorization: Basic`, or a JWT via `btoken`. The `/metadata` CapabilityStatement is the only anonymous endpoint.

## Steps
1. (Optional, anonymous) `getCapabilityStatement` — GET `/metadata` to confirm the server, FHIR version (4.0.1), and supported operations.
2. `lookupConcept` — GET `/CodeSystem/$lookup?system={system}&code={code}` to return the display name and properties for a code. Use `lookupConceptByCoding` (POST `/CodeSystem/$lookup`) when supplying a full Coding.
3. `findValueSets` — GET `/ValueSet?name={name}` to locate the target value set id.
4. `getValueSetCodeValidation` — GET `/ValueSet/{id}/$validate-code?system={system}&code={code}` to confirm the code is a valid member of that value set.

## Rules
- Errors are FHIR `OperationOutcome`. A `403` means missing/invalid credentials — establish a session first (see authentication/canada-health-infoway-authentication.yml).
- Read-only; no idempotency key needed (see conventions/canada-health-infoway-conventions.yml).
