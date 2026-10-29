# P22 — Preliminary Finding 001

## Title
Potentially Exposed Directory Listing and File Access

## Target
http://127.0.0.1:3000/ftp

## Phase
Phase 1 — Reconnaissance and Initial API Review

## Observation
An unauthenticated GET request to /ftp returned HTTP 200
and rendered a directory listing containing filenames, sizes,
and timestamps.

The listing included document files, backup files, and other
file types. A separate unauthenticated GET request to
/ftp/legal.md returned HTTP 200, confirming that at least one
listed file was accessible without supplying authentication.

A GET request to /ftp/robots.txt returned HTTP 403.
The reason for this response has not been established.

## Evidence
- scans/phase1-ftp-listing.html
- scans/phase1-ftp-headers.txt
- screenshots/phase1-ftp-directory-listing.png
- scans/phase1-ftp-legal-md-check.txt
- scans/phase1-ftp-robots-txt-check.txt
- HTTP status for /ftp: 200 OK
- HTTP status for /ftp/legal.md: 200 OK
- HTTP status for /ftp/robots.txt: 403 Forbidden
- The /ftp listing exposes filenames, sizes, and timestamps.
- curl repeatedly reported a 12-byte Content-Length discrepancy:
  the response declared 11,330 bytes, while 11,318 bytes were received.
- The downloaded HTML contained closing body and HTML tags.
  The cause of the response-length discrepancy remains unknown.

## Assessment Status
Preliminary — directory listing and access to one listed file
have been observed. The sensitivity of the file contents,
security impact, and severity have not been established.

## Limitations
- HTTP 200 confirms a successful response, not that the content
  is sensitive or exploitable.
- HTTP 403 for /ftp/robots.txt does not establish why access
  was denied.
- The response-length discrepancy has not been explained.
- No authentication bypass has been confirmed.

## Safety
Testing is restricted to the local OWASP Juice Shop lab.
No destructive actions or denial-of-service testing were performed.

## Next Steps
- Review the accessible documentation file's content only as needed
  to assess whether it contains security-relevant information.
- Assess the exposure risk without downloading potentially sensitive
  files unnecessarily.
- Investigate the response-length discrepancy separately.
- Determine severity only after sufficient impact evidence exists.
