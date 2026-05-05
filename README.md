# P2-5: AWS EC2 Hardening & Vulnerability Management

## Overview

This repository is part of **Cybersecurity Portfolio 2: AWS Cloud Security & Engineering**.

The purpose of this project is to design and document hardening and vulnerability management practices for an AWS EC2 workload. This lab will focus on secure EC2 deployment, SSH access control, patching, security group exposure review, basic vulnerability assessment, and AWS Systems Manager concepts.

This project is planned as the fifth AWS-focused lab in Portfolio 2 because workload hardening should build on the AWS account, network, logging, and storage security foundations from the earlier projects.

---

## Status

**Planned**

This project has not been implemented yet.

Work on this repository will begin after the required Portfolio 1 homelab foundation is completed and after the initial AWS account, VPC, logging, and S3 security foundations are prepared.

Current status:

- [ ] EC2 hardening plan created
- [ ] SSH access control plan documented
- [ ] Patch management plan created
- [ ] Security group exposure review planned
- [ ] Vulnerability assessment plan created
- [ ] Systems Manager review planned
- [ ] Cost-control notes created
- [ ] Screenshots and evidence collected
- [ ] Final documentation completed

---

## Portfolio Context

### Portfolio 1 Foundation

Portfolio 1 focuses on building a local cybersecurity homelab using Proxmox, pfSense, network segmentation, Active Directory, Splunk, and vulnerable systems.

Portfolio 1 builds the local infrastructure, endpoint, and vulnerability management foundation.

### Portfolio 2 Direction

Portfolio 2 expands local infrastructure and security concepts into AWS cloud security and cloud engineering.

This repository focuses on securing and assessing an AWS EC2 workload.

---

## Project Goal

The goal of this project is to understand how EC2 workloads can be deployed, hardened, monitored, patched, and reviewed for exposure risk.

By the end of this project, the planned AWS environment should include documentation for:

- EC2 workload security baseline
- SSH access control
- Security group exposure review
- Patch management approach
- Basic vulnerability assessment
- AWS Systems Manager review
- Cost-control considerations
- Redacted evidence and screenshots

---

## Planned Skills

This project is intended to develop hands-on familiarity with:

- EC2 workload security
- Linux server hardening basics
- SSH hardening
- Security group review
- Cloud workload exposure management
- Patch management
- Vulnerability management workflow
- AWS Systems Manager concepts
- Amazon Inspector concepts
- Security documentation
- Cost-conscious cloud operations

---

## Planned AWS Services

The following AWS services and features may be used in this project:

| AWS Service / Feature | Planned Use |
|---|---|
| Amazon EC2 | Deploy and harden a test Linux instance |
| Amazon VPC | Place EC2 into a controlled network |
| Security Groups | Restrict inbound and outbound access |
| IAM Roles | Attach controlled permissions to EC2 if needed |
| AWS Systems Manager | Review patching and management concepts |
| Amazon Inspector | Optional vulnerability assessment review if cost-controlled |
| CloudTrail | Review EC2-related management events |
| CloudWatch | Optional monitoring review |
| AWS CLI | Optional validation and testing |

---

## Planned Lab Sections

### 1. EC2 Hardening Baseline

Planned tasks:

- Deploy or document a Free Tier eligible EC2 Linux instance
- Review AMI selection
- Review instance type
- Review storage settings
- Confirm no unnecessary public exposure
- Document initial hardening checklist

Expected outcome:

> EC2 workload security is reviewed before the instance is used for testing.

---

### 2. SSH Access Control

Planned tasks:

- Restrict SSH access to a trusted source IP where possible
- Avoid broad SSH exposure to `0.0.0.0/0`
- Review key pair handling
- Document secure administrative access
- Review alternatives such as Systems Manager Session Manager

Expected outcome:

> Administrative access is controlled and documented with risk reasoning.

---

### 3. Patch Management

Planned tasks:

- Review operating system update process
- Document package update commands
- Review AWS Systems Manager patching concepts
- Document before/after patch status
- Connect patching to vulnerability management

Expected outcome:

> The EC2 workload has a documented patch management plan.

---

### 4. Security Group Exposure Review

Planned tasks:

- Review inbound security group rules
- Review outbound security group rules
- Identify risky rules
- Document rule purpose
- Remove or avoid unnecessary exposure

Expected outcome:

> Network exposure is documented and limited to required access.

---

### 5. Vulnerability Assessment

Planned tasks:

- Review vulnerability assessment options
- Review Amazon Inspector conceptually or use only if cost-controlled
- Optionally compare with local vulnerability management concepts from Portfolio 1
- Document findings and remediation approach
- Avoid unnecessary scanning against public targets

Expected outcome:

> Vulnerability management workflow is documented for an AWS-hosted workload.

---

### 6. Systems Manager Review

Planned tasks:

- Review AWS Systems Manager capabilities
- Document Session Manager concept
- Review patch management features
- Review required IAM role concepts
- Decide whether Systems Manager will be implemented in this lab or reviewed conceptually

Expected outcome:

> AWS Systems Manager is understood as a management and operational security tool for EC2 workloads.

---

## Planned Deliverables

This repository is expected to include:

- EC2 hardening plan
- SSH access control documentation
- Patch management plan
- Security group exposure review
- Vulnerability assessment plan
- Systems Manager review
- Cost-control notes
- Redacted screenshots
- Lessons learned
- Final project summary

---

## Proposed Repository Structure

    P2-5-aws-ec2-hardening-vulnerability-management/
    ├── README.md
    ├── docs/
    │   ├── ec2-hardening-plan.md
    │   ├── ssh-access-control.md
    │   ├── patch-management-plan.md
    │   ├── security-group-exposure-review.md
    │   ├── vulnerability-assessment-plan.md
    │   ├── systems-manager-review.md
    │   ├── cost-control-notes.md
    │   └── lessons-learned.md
    ├── diagrams/
    │   └── README.md
    └── screenshots/
        └── README.md

---

## Security Notes

Sensitive information will not be committed to this repository.

This includes:

- AWS account ID
- Access keys
- Secret access keys
- Private SSH keys
- Public IP addresses unless intentionally documented and safe
- Private IP addresses if considered sensitive
- Unredacted ARNs
- Unredacted screenshots
- Any credential material

Private keys must never be committed to this repository.

---

## Cost-Control Notes

This project is designed to stay within the AWS Free Tier or near-free usage.

Special care will be taken with:

- EC2 instance runtime
- EBS volumes
- EBS snapshots
- Elastic IP addresses
- Amazon Inspector
- CloudWatch logs and metrics
- NAT Gateway if private subnet outbound access is used

The goal is to learn EC2 hardening and vulnerability management without creating unnecessary cost.

---

## Relationship to AWS Solutions Architect Associate

This project supports foundational knowledge for the **AWS Certified Solutions Architect – Associate** certification by focusing on:

- EC2 deployment
- Compute workload placement
- Security groups
- IAM roles for services
- Monitoring basics
- Operational security
- Cost-aware workload design
- Secure access patterns

This repository is not a certification study guide. It is a hands-on portfolio project designed to support practical AWS learning.

---

## Resume Skill Alignment

This project is intended to support resume experience related to:

- AWS EC2 hardening
- Linux server security
- SSH access control
- Security group review
- Vulnerability management
- Patch management
- AWS Systems Manager concepts
- Cloud workload security documentation

Example resume bullet after completion:

> Hardened and assessed an AWS EC2 Linux workload by restricting SSH access, reviewing security group exposure, applying patch management practices, and documenting vulnerability remediation steps.

---

## Current Status Summary

This repository is currently in the planning stage.

Implementation will begin after the required Portfolio 1 foundation is completed and after the AWS account, VPC, logging, and S3 security foundations are prepared.
