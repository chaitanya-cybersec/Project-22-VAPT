# Project 22 — Pre-Phase 1 Report
## Environment Setup and Lab Preparation

**Date:** 27 October 2026
**Operating System:** Kali GNU/Linux Rolling 2026.3
**Project:** VAPT — Vulnerability Assessment and Penetration Testing
**Stage:** Pre-Phase 1
**Status:** Environment prepared; application verification pending

---

## 1. Objective

Prepare a local security-testing environment, verify essential
tools and connectivity, establish a project directory structure,
and identify the authorized practice application.

No vulnerability scanning or exploitation is documented as
completed in this stage.

## 2. System Environment

### Operating System
- Distribution: Kali GNU/Linux Rolling
- Version: 2026.3

### Memory
- Total RAM: Approximately 4.3 GiB
- Available RAM at verification: Approximately 3.1 GiB
- Swap: Approximately 953 MiB
- Swap usage at verification: 0 B

### Disk
- Root filesystem: 79 GB
- Used: 17 GB
- Available: 58 GB
- Usage: 23%

### Network
- Interface: eth0
- IPv4 address: 10.0.2.15/24
- Network interface state: UP
- External IP connectivity: Verified using ping to 1.1.1.1
- DNS resolution: Verified for github.com
- VirtualBox NAT is consistent with the observed address.

## 3. Tools Verified

### Git
- Version: 2.53.0
- Status: Installed

### Docker
- Version: 28.5.2+dfsg4
- Status: CLI installed
- Initial non-sudo access: Permission denied on Docker socket
- Privileged container listing: Successful using sudo docker ps

### Practice Application
- Application: OWASP Juice Shop
- Docker image: bkimminich/juice-shop
- Container name: juice-shop
- Container ID: 44e329f223d3
- Observed state: Up 20 minutes at verification
- Port mapping: 127.0.0.1:3000 -> container port 3000
- Exposure: Bound to the local loopback interface

Note: Container status was observed during setup. HTTP response
and browser access have not yet been verified.

## 4. Project Directory Structure

Created under ~/Project_22/:

Project_22/
├── scope/
├── notes/
├── evidence/
├── screenshots/
├── scans/
├── reports/
└── scripts/

Purpose:
- scope/: Authorization and testing boundaries
- notes/: Session logs and methodology
- evidence/: Supporting assessment evidence
- screenshots/: Visual evidence
- scans/: Authorized scan outputs
- reports/: Final assessment reports
- scripts/: Project testing utilities

## 5. Documentation Created

- notes/session-2026-10-27.md
  Initial session log covering setup activities and pending tasks.

- notes/pre-phase-1-environment-setup.md
  This report, documenting environment preparation and verification.

## 6. Outstanding Tasks

1. Verify the Juice Shop page in Kali Firefox.
2. Check the local HTTP response using curl.
3. Define and record assessment scope and rules.
4. Establish an evidence naming convention.
5. Begin Phase 1 only after the application and scope are verified.

## 7. Authorization and Safety

Testing is restricted to the locally hosted OWASP Juice Shop
instance unless additional targets are explicitly authorized.

No testing against public or third-party targets is authorized
by this document.

## 8. Completion Criteria

Pre-Phase 1 setup is documented. Application availability,
formal scope confirmation, and assessment readiness remain
pending until the outstanding tasks are completed.

## 9. Evidence Sources

The initial observations in this report are based on terminal
outputs collected during the setup session on 27 October 2026.

Raw command outputs and screenshots should be retained separately
where appropriate. This report records observed results; it is
not a substitute for the original evidence.

---
End of Pre-Phase 1 Report
