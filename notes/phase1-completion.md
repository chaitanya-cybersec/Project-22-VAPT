# Project 22 — Phase 1 Completion Note

## Project
P22 — Vulnerability Assessment and Penetration Testing (VAPT)

## Target
OWASP Juice Shop running locally at `http://127.0.0.1:3000`

## Phase
Phase 1 — Reconnaissance and Initial API Review

## Completed Activities
- Verified that the local Juice Shop application was responding.
- Captured Nmap service-detection output for port 3000.
- Saved HTTP response headers and the homepage.
- Retrieved and reviewed the API documentation.
- Documented the B2B API endpoint `POST /b2b/v2/orders`.
- Recorded the API's declared bearer-token authentication requirement.
- Tested an unauthenticated GET request to `/b2b/v2/orders`; it returned HTTP 401.
- Sent an OPTIONS request to `/b2b/v2/orders`; it returned HTTP 204 and advertised HTTP methods.
- Captured the `/ftp` directory listing and documented it as a preliminary finding.
- Verified that `/ftp/legal.md` returned HTTP 200 without supplying authentication.
- Reviewed `legal.md`; its visible content consisted primarily of placeholder text.
- Verified that `/ftp/robots.txt` returned HTTP 403; the reason is unknown.
- Recorded the reproducible 12-byte response-length discrepancy for `/ftp`.
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
- `scans/phase1-ftp-legal-md-check.txt`
- `scans/phase1-ftp-robots-txt-check.txt`
- `screenshots/phase1-ftp-directory-listing.png`
- `notes/phase1-api-inventory.md`
- `notes/phase1-finding-001.md`

## Preliminary Finding
The `/ftp` route returned HTTP 200 and displayed filenames, sizes, and timestamps. The listed `legal.md` file was accessible without supplied authentication, but its reviewed content consisted primarily of placeholder text. Meaningful sensitive-data exposure and security impact have not been demonstrated; severity remains unassigned.

## Limitations and Unresolved Questions
- No authentication bypass has been confirmed.
- The security impact of wildcard CORS has not been established.
- The OPTIONS response does not prove that all advertised methods can perform protected actions.
- The `/ftp` listing's security impact remains undetermined.
- A 12-byte discrepancy was observed between the declared response length and the downloaded `/ftp` listing body; its cause remains unresolved.
- The reason `/ftp/robots.txt` returned HTTP 403 is unknown.

## Safety and Scope
Testing is restricted to the authorized local OWASP Juice Shop lab. No order was submitted during the documented API reconnaissance. No destructive actions or denial-of-service testing were performed.

## Git Status
The latest documentation changes are tracked in Git and pushed to the private GitHub repository. Confirm the final commit and clean working tree before declaring the documentation review complete.

## Completion Status
Reconnaissance and initial API review activities are documented. The documentation review can be completed after consistency checks. Vulnerability validation, impact assessment, severity assignment, and final VAPT reporting remain outstanding.
