---
name: Translate a code between code systems (FHIR $translate)
description: Find the relevant ConceptMap and translate a source code to its target code(s) on the Infoway Terminology Gateway.
api: openapi/infoway-fhir-terminology-service-api-openapi.json
operations: [findConceptMaps, getConceptMap, translateConcept]
---

# Translate a concept through a ConceptMap

Use this skill to map a code from one code system to another using a published Canadian ConceptMap.

Base URL: `https://termapi.infoway-inforoute.ca/fhir/v1`

## Auth
Requires an authenticated session (see authentication/canada-health-infoway-authentication.yml).

## Steps
1. `findConceptMaps` — GET `/ConceptMap?name={name}` (or by source/target) to locate the ConceptMap id.
2. `getConceptMap` — GET `/ConceptMap/{id}` to inspect its source/target systems and metadata.
3. `translateConcept` — GET `/ConceptMap/{id}/$translate?system={sourceSystem}&code={code}` (or POST `/ConceptMap/{id}/$translate` with a Parameters body) to return the mapped target Coding(s) and equivalence.

## Rules
- The response is a FHIR `Parameters` resource; check `result` and each `match` element.
- Errors are FHIR `OperationOutcome`; `404` means the ConceptMap id does not exist.
