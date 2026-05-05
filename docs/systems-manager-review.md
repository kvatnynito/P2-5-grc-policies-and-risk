# AWS Systems Manager Review

## Status

Planned.

This document will review AWS Systems Manager concepts relevant to EC2 management and security operations.

---

## Purpose

The purpose of this document is to understand how AWS Systems Manager can support EC2 management, patching, inventory, and secure administrative access.

---

## Systems Manager Areas to Review

| Feature | Purpose |
|---|---|
| Session Manager | Browser or CLI-based shell access without direct SSH exposure |
| Patch Manager | Helps automate patching workflows |
| Inventory | Collects instance metadata |
| Run Command | Runs commands on managed instances |
| State Manager | Maintains desired configuration |
| Parameter Store | Stores configuration values and secrets-like parameters |

---

## Requirements to Review

Systems Manager may require:

- SSM Agent installed on the instance
- IAM instance profile/role
- Network access to SSM endpoints
- Correct region configuration
- Logging configuration if sessions are logged

---

## Session Manager Security Value

Session Manager may reduce risk by:

- Removing need for inbound SSH
- Using IAM-based access control
- Supporting session logging
- Improving administrative access tracking
- Reducing exposed management ports

---

## Planned Review Questions

1. Is the SSM Agent installed by default on the selected AMI?
2. What IAM role is required?
3. Does the instance need internet access or VPC endpoints?
4. Can Session Manager replace SSH in this lab?
5. How does Patch Manager relate to vulnerability remediation?
6. What logs or evidence can Systems Manager provide?

---

## Implementation Decision

To be completed later.

Possible outcomes:

- Review Systems Manager conceptually only
- Implement Session Manager
- Implement Patch Manager review
- Defer deeper Systems Manager work to a future project

---

## Planned Evidence

Later implementation may include:

- Systems Manager managed instance screenshot
- IAM role notes
- Session Manager notes
- Patch Manager notes
- Lessons learned
