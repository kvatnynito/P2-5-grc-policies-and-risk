# Security Group Exposure Review

## Status

Planned.

This document will track security group exposure review for the EC2 workload.

---

## Purpose

The purpose of this document is to review whether the EC2 workload is exposed only as much as needed.

Security groups act as instance-level virtual firewalls in AWS.

---

## Review Goals

The security group review should answer:

- Which inbound ports are open?
- Which sources can connect?
- Are any rules overly broad?
- Are rules documented?
- Are temporary rules removed?
- Does the instance need a public IP?
- Is outbound access appropriate?

---

## Planned Security Group Rule Table

| Rule Purpose | Direction | Protocol | Port | Source/Destination | Status | Notes |
|---|---|---|---|---|---|---|
| SSH admin access | Inbound | TCP | 22 | Trusted IP only | Planned | Avoid broad internet exposure |
| HTTP test access | Inbound | TCP | 80 | Only if needed | Planned | Not required by default |
| HTTPS test access | Inbound | TCP | 443 | Only if needed | Planned | Not required by default |
| Outbound updates | Outbound | TCP | 443 | 0.0.0.0/0 | Planned | May be needed for package updates |

---

## Risky Rules to Avoid

| Rule | Risk |
|---|---|
| SSH from 0.0.0.0/0 | Exposes admin access to the internet |
| RDP from 0.0.0.0/0 | Exposes Windows admin access to the internet |
| All traffic from 0.0.0.0/0 | Extremely broad exposure |
| Unused open ports | Expands attack surface |
| Unlabeled rules | Makes review harder |

---

## Exposure Review Questions

During implementation, answer:

1. Which security group is attached to the EC2 instance?
2. Which inbound rules exist?
3. Which outbound rules exist?
4. Why does each rule exist?
5. Can any rule be removed?
6. Is the instance reachable from the internet?
7. Is that exposure intentional?
8. What would be different in production?

---

## Remediation Approach

If risky exposure is found:

1. Identify the rule.
2. Determine whether it is needed.
3. Restrict the source or destination.
4. Remove unused ports.
5. Test required connectivity.
6. Document the change.

---

## Planned Evidence

Later implementation may include:

- Redacted security group screenshot
- Rule review table
- Exposure finding notes
- Remediation notes
- Lessons learned
