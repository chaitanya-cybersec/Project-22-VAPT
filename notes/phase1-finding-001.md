# P22 — Preliminary Finding 001

## Title
Potentially Exposed Directory Listing

## Target
http://127.0.0.1:3000/ftp

## Phase
Phase 1 — Reconnaissance

## Observation
The /ftp route returned HTTP 200 and rendered a directory
listing containing filenames, sizes, and timestamps.

## Evidence
- scans/phase1-ftp-listing.html
- scans/phase1-ftp-headers.txt
- screenshots/phase1-ftp-directory-listing.png
- HTTP status: 200 OK
- Directory listing exposes filenames, sizes, and timestamps.
- curl reported a 12-byte Content-Length discrepancy.

## Assessment Status
Preliminary — impact and sensitivity not yet validated.

## Safety
Testing is restricted to the local OWASP Juice Shop lab.

## Next Steps
- Investigate the HTTP response-length discrepancy.
- Assess the impact of the exposed directory listing.
- Validate findings before assigning severity.
