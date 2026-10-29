# Project 22 — Web Application VAPT

## Overview
A hands-on Vulnerability Assessment and Penetration Testing (VAPT)
portfolio project using OWASP Juice Shop in a controlled local lab.

The project focuses on a structured testing methodology, evidence
collection, vulnerability validation, risk assessment, and remediation
reporting.

## Objectives
- Establish a reproducible local testing environment.
- Document the assessment scope and rules of engagement.
- Perform structured web application reconnaissance.
- Validate findings with clear, reproducible evidence.
- Produce a professional report with remediation recommendations.

## Lab Environment
- Operating system: Kali Linux
- Virtualization: Oracle VirtualBox
- Practice application: OWASP Juice Shop
- Deployment: Docker
- Target URL: http://127.0.0.1:3000

## Scope and Safety
Testing is restricted to the locally hosted OWASP Juice Shop instance.
Public websites, third-party systems, unrelated containers, and other
network devices are outside the project scope.

No denial-of-service testing is planned.

## Project Structure
- `scope/` — Assessment scope and testing boundaries
- `notes/` — Session logs and project documentation
- `evidence/` — Supporting evidence collected during the assessment
- `screenshots/` — Visual evidence
- `scans/` — Authorized scan outputs
- `reports/` — Assessment reports
- `scripts/` — Project scripts

## Progress
- [x] Pre-Phase 1: Environment preparation and documentation
- [x] Local application HTTP response verified
- [x] Application loaded successfully in Kali Firefox
- [x] Assessment scope documented
- [x] Phase 1: Initial application reconnaissance
- [x] HTTP headers and Nmap output collected
- [x] API documentation reviewed and inventoried
- [x] Unauthenticated API request and OPTIONS response recorded
- [x] Potential `/ftp` directory-listing finding documented
- [x] Phase 1 notes, scan evidence, and screenshots committed to GitHub
- [ ] Final Phase 1 scope and evidence review
- [ ] Further vulnerability validation
- [ ] Remediation recommendations
- [ ] Final VAPT report

## Current Status
Phase 1 reconnaissance and initial API review have been documented.
The `/ftp` directory listing remains a preliminary finding; its impact
has not yet been validated. No authentication bypass has been confirmed.
Further review is required before Phase 1 can be formally closed.


## Disclaimer
This project is for educational and portfolio purposes. Testing must
remain within the documented scope and applicable authorization.
