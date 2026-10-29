# Project 22 — Phase 1 Completion Note

## Project
P22 — Vulnerability Assessment and Penetration Testing (VAPT)

## Target
OWASP Juice Shop running locally at `http://127.0.0.1:3000`

## Phase
Phase 1 — Reconnaissance and Initial API Review

## Completed Activities
- Verified the local Juice Shop application was responding.
- Captured Nmap service-detection output for port 3000.
- Saved HTTP response headers and the homepage.
- Retrieved and reviewed the API documentation.
- Documented the B2B API endpoint `POST /b2b/v2/orders`.
- Recorded the API's declared bearer-token authentication requirement.
- Tested an unauthenticated GET request to `/b2b/v2/orders`; it returned HTTP 401.
- Sent an OPTIONS request to `/b2b/v2/orders`; it returned HTTP 204 and advertised HTTP methods.
- Captured the `/ftp` directory listing and documented it as a preliminary finding.
- Saved scan outputs, notes, and screenshots in the project repository.

## Evidence Locations
- `scans/phase1-localhost-nmap.txt`
- `scans/phase1-http-headers.txt`
- `scans/phase1-homepage.html`
- `scans/phase1-api-docs.html`
- `scans/phase1-swagger-init.js`
- `scans/phase1-b2b-orders-unauthenticated.txt`
- `scans/phase1-b2b-orders-options.txt`
- `scans/phase1-ftp-listing.html`
- `scans/phase1-ftp-headers.txt`
- `screenshots/phase1-ftp-directory-listing.png`
- `notes/phase1-api-inventory.md`
- `notes/phase1-finding-001.md`

## Preliminary Finding
The `/ftp` route returned HTTP 200 and displayed filenames, sizes, and timestamps. The impact and sensitivity of the listed files have not yet been validated, so severity has not been assigned.

## Limitations and Unresolved Questions
- No authentication bypass has been confirmed.
- The security impact of wildcard CORS has not been established.
- The OPTIONS response does not prove that all advertised methods can perform protected actions.
- The `/ftp` listing's security impact remains unvalidated.
- A 12-byte discrepancy was observed between the reported response length and the downloaded `/ftp` listing body; its cause remains unresolved.

## Safety and Scope
Testing is restricted to the authorized local OWASP Juice Shop lab. No order was submitted during the documented API reconnaissance.

## Git Status
Phase 1 evidence was committed and pushed to the private GitHub repository in commit `a71ce4e`.

## Completion Status
Reconnaissance evidence and initial API documentation are recorded. Phase 1 should be considered ready for closure after the scope, README, and evidence are reviewed for consistency.
