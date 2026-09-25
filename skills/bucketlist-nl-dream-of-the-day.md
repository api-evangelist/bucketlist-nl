---
name: dream-of-the-day
description: Retrieve the current Dream of the Day from Bucketlist.nl
api: https://bucketlist.nl/brand/droom-van-de-dag.openapi.json
operations:
  - getDreamOfTheDay
---

## Steps
1. **Call the endpoint** `GET https://bucketlist.nl/api/droom-van-de-dag`.
2. Optionally include query parameters:
   - `scope` (`nederland` or `wereld`) to limit the region.
   - `lang` (`nl`, `en`, `de`, `fr`, `es`) to set language.
3. No authentication is required.
4. The response is JSON with fields `title`, `description`, `image`, `url`, and `referralUrl`.
5. Cache according to `Cache‑Control` header.

## Idempotency & Errors
- The operation is **idempotent** – repeated calls return the same day's data.
- Possible error responses:
  - `4xx` for malformed query parameters.
  - `5xx` for server errors.

## Conformance
- Conforms to OpenAPI spec `droom-van-de-dag.openapi.json` operationId `getDreamOfTheDay`.
