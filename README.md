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
- [ ] Phase 1: Initial application reconnaissance
- [ ] Vulnerability assessment and validation
- [ ] Remediation recommendations
- [ ] Final VAPT report

## Current Status
Pre-Phase 1 is complete. Formal vulnerability testing has not yet
started.

## Disclaimer
This project is for educational and portfolio purposes. Testing must
remain within the documented scope and applicable authorization.
