# AWS Project 2 — IAM Security Baseline (Admin / Dev / Audit)

## Overview
This project demonstrates setting up a secure IAM baseline in AWS by creating role-based IAM groups and users, applying least-privilege permissions, and enabling MFA for privileged access.

## What I Built
- Created IAM groups:
  - **Admins** (AdministratorAccess)
  - **Developers** (PowerUserAccess or controlled dev access depending on requirement)
  - **Auditors** (SecurityAudit - read-only security visibility)
- Created IAM users:
  - **admin-user** → added to Admins group + MFA enabled
  - **dev-user** → added to Developers group (MFA optional)
  - **audit-user** → added to Auditors group (read-only)
- Verified sign-in using IAM user sign-in URL and account ID / alias

## Security Controls Implemented
- **MFA enabled** for privileged IAM user (admin-user)
- Root account kept for emergency use only (no daily usage)
- Role separation: Admin vs Dev vs Audit
- Auditors restricted to read-only security visibility

## Evidence (Screenshots)
Screenshots are available in the `/screenshots` folder:
- IAM groups created
- IAM users created
- MFA enabled for admin-user
- Permission policies attached

## Skills Demonstrated
- AWS IAM
- Least privilege access control
- MFA / identity security
- Account access management

## Next Improvements
- Enable MFA for dev-user and audit-user
- Add password policy + access analyzer checks
- Replace broad policies with custom least-privilege policies (production style)