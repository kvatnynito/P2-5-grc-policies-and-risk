# EC2 Hardening Plan

## Status

Planned.

This document will define the planned EC2 hardening baseline for this lab.

---

## Purpose

The purpose of this document is to plan security controls for an AWS EC2 Linux workload before testing patching, vulnerability assessment, or monitoring.

---

## Planned EC2 Overview

| Item | Planned Value |
|---|---|
| Instance name | To be selected |
| AMI | Amazon Linux or Ubuntu Server |
| Instance type | Free Tier eligible if possible |
| Subnet placement | Public or private, based on lab design |
| Public IP | Only if required |
| SSH access | Restricted |
| IAM role | Least privilege if required |
| Storage | Minimal test storage |
| Monitoring | Basic review |

---

## Hardening Goals

The EC2 hardening plan should support:

- Controlled administrative access
- Minimal network exposure
- Updated operating system packages
- Secure key handling
- Least-privilege IAM role usage
- Basic monitoring and logging
- Clear documentation of configuration decisions
- Cost-conscious resource usage

---

## Initial Hardening Checklist

| Control | Status | Notes |
|---|---|---|
| Use trusted AMI | Planned | Avoid unknown images |
| Use Free Tier eligible instance | Planned | Reduce cost risk |
| Restrict SSH access | Planned | Avoid broad internet exposure |
| Review security group rules | Planned | Inbound rules should be justified |
| Update packages | Planned | Apply OS updates |
| Disable password SSH login | Planned | Use key-based access |
| Protect private key | Planned | Never commit keys |
| Review IAM role permissions | Planned | Attach only if needed |
| Review EBS volume settings | Planned | Avoid unused volumes |
| Document cleanup steps | Planned | Reduce cost risk |

---

## Secure Configuration Questions

During implementation, answer:

1. Which AMI was selected and why?
2. Is the instance publicly reachable?
3. Which inbound ports are open?
4. Who can SSH into the instance?
5. Are packages updated?
6. Is password authentication disabled?
7. Is an IAM role attached?
8. Are permissions scoped appropriately?
9. What evidence proves the workload was hardened?

---

## Risks to Consider

| Risk | Mitigation |
|---|---|
| SSH exposed to the internet | Restrict source IP or use Session Manager |
| Unpatched operating system | Apply updates and document patch status |
| Overly permissive IAM role | Use least privilege |
| Private key exposure | Never commit keys |
| Unused EBS volumes | Delete after testing |
| Unnecessary public IP | Use only when required |
| No documentation | Maintain checklist and evidence |

---

## Planned Evidence

Later implementation may include:

- Redacted EC2 instance configuration screenshot
- Security group screenshot
- OS update command output
- SSH configuration notes
- IAM role review
- Lessons learned
