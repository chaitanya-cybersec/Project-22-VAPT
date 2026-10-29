# Project 22 — VAPT Assessment Scope

## 1. Project Information

- Project: Project 22 (P22)
- Assessment type: Web Application Vulnerability Assessment and
  Penetration Testing (VAPT)
- Practice application: OWASP Juice Shop
- Date documented: 27 October 2026
- Stage: Phase 1 — Reconnaissance and Initial API Review

## 2. Objective

Assess the security of a deliberately vulnerable web application
in a controlled local lab, document observations, collect evidence,
and prepare a professional VAPT report.

## 3. In-Scope Target

- Application: OWASP Juice Shop
- URL: http://127.0.0.1:3000
- Hosting method: Local Docker container
- Container name: juice-shop
- Host binding: 127.0.0.1:3000

Testing is restricted to this local practice application.

## 4. Out-of-Scope Targets

The following are excluded:

- Public websites and third-party systems
- Other devices on the local network
- The Kali host operating system and unrelated services
- Other Docker containers or applications
- Any target not explicitly added to this scope

## 5. Planned Testing Activities

Subject to the project phase and its documented procedures:

- Manual application navigation and reconnaissance
- Review of HTTP responses and security-related headers
- Identification and validation of potential web vulnerabilities
- Evidence collection and risk assessment
- Remediation recommendations and report preparation

## 6. Safety Restrictions

- Keep testing confined to the local Juice Shop instance.
- Do not perform denial-of-service or load testing.
- Do not attack unrelated systems or attempt to access real users'
  accounts or data.
- Avoid destructive actions and unnecessary data modification.
- Record findings accurately; do not claim a vulnerability without
  sufficient evidence.
- Stop if the target differs from the documented scope.

## 7. Evidence Management

- Notes: ~/Project_22/notes/
- Evidence: ~/Project_22/evidence/
- Screenshots: ~/Project_22/screenshots/
- Scan outputs: ~/Project_22/scans/
- Reports: ~/Project_22/reports/

Use descriptive filenames with the date and activity. Preserve
original outputs and redact secrets or sensitive information
before sharing evidence publicly.

## 8. Verification Status

- Docker container observed running: Yes
- HTTP response verified: Yes (HTTP 200 OK)
- Kali Firefox access verified: Yes
- Scope documented: Yes
- Initial reconnaissance started: Yes
- Initial API review performed: Yes
- Vulnerability validation: In progress
- Formal assessment closure: Pending review

## 9. Phase Gate

Pre-Phase 1 setup must be reviewed and documented before testing
begins. This scope defines the intended lab boundary; it does not
authorize testing against any other target.

---
End of Assessment Scope
