---
name: Browse and download Canadian terminology content (RESTful API)
description: Log in to the RESTful Terminology API, browse code systems / subsets / maps / packages, and download versioned content.
api: openapi/infoway-terminology-service-api-openapi.json
operations: [login, getCodeSystems, findSubsets, getConcepts, downloadSubset, logout]
---

# Browse and download terminology content

Use this skill to discover and download Canadian terminology content via the non-FHIR RESTful Terminology API.

Base URL: `https://termapi.infoway-inforoute.ca/rest/v1`

## Auth
1. `login` — POST `/session` with `auth` (Base64 `username:password`), `ssotoken`, or `btoken`. It returns `authToken` (SSO), `btoken` (JWT), and profile attributes. Reuse the returned token on subsequent calls via the `auth`/`btoken` query parameter.

## Steps
2. `getCodeSystems` — GET `/codesystems` to list Canadian code systems (paged: `currentPage`, `totalPages`, `pageSize`, `totalRecords`).
3. `findSubsets` — GET `/subsets` to list terminology subsets (value sets); note the `subsetid`.
4. `getConcepts` — GET `/subset/{subsetid}/concepts` to read the concepts in a subset.
5. `downloadSubset` — GET `/subset/{subsetid}/download` to download the subset content; use `/subset/{subsetid}/delta` for incremental change since a prior version.
6. `logout` — DELETE `/session` when finished.

## Rules
- Unauthenticated content reads return `403`. Register free at https://accelero.infoway-inforoute.ca/en/register.
- Pagination is page-number based (see conventions/canada-health-infoway-conventions.yml).
- To be notified of content changes, subscribe via POST `/notification` (see asyncapi/canada-health-infoway-notifications-webhooks.yml).
