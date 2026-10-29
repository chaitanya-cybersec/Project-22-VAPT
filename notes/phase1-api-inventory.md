# P22 — Phase 1 API Inventory

## Source
scans/phase1-swagger-init.js

## API Information
- Title: NextGen B2B API
- Version: 2.0.0
- OpenAPI: 3.0.0
- Base path: /b2b/v2

## Documented Operation
- Method: POST
- Path: /orders
- Operation ID: createCustomerOrder
- Purpose: Create a customer order
- Request format: application/json
- Documented response: HTTP 200

## Authentication
- Security scheme: bearerAuth
- Type: HTTP bearer
- Token format: JWT
- Root-level security declaration references bearerAuth.
- Runtime enforcement has not been tested.

## Request Schema
- Order requires cid.
- Order may contain orderLines or orderLinesData.
- OrderLine requires productId and quantity.
- quantity has a documented minimum of 1.
- customerReference is optional.

## Assessment Status
API contract documented during reconnaissance.
No order was submitted.
No authentication bypass has been confirmed.

## Evidence
- scans/phase1-swagger-init.js

## Runtime Reconnaissance

### Unauthenticated GET Request
- Request: GET /b2b/v2/orders
- Response: HTTP 401 Unauthorized
- Message: No Authorization header was found.
- Evidence: scans/phase1-b2b-orders-unauthenticated.txt

### OPTIONS Request
- Request: OPTIONS /b2b/v2/orders
- Response: HTTP 204 No Content
- Access-Control-Allow-Origin: *
- Advertised methods: GET, HEAD, PUT, PATCH, POST, DELETE
- Evidence: scans/phase1-b2b-orders-options.txt

### Preliminary Interpretation
- The unauthenticated GET request was rejected.
- The OPTIONS response advertises HTTP methods but does not establish
  whether protected operations can be performed without authentication.
- The security impact of wildcard CORS has not been established.
- No authentication bypass has been confirmed.
- No order was submitted.

### Additional Schema Details
- OrderLines is an array of OrderLine objects.
- OrderLinesData is a string for customer-specific order data.
- Its documented example includes productId, quantity,
  customerReference, and couponCode.
- The specification declares bearerAuth as a root-level security
  requirement.
- These are documented contract details; runtime validation and
  security have not been fully tested.

