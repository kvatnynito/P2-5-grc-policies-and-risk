# Cost-Control Notes

## Status

Planned.

This document will track cost-control considerations for the AWS EC2 Hardening & Vulnerability Management lab.

---

## Purpose

The purpose of this document is to prevent unnecessary AWS costs while deploying, hardening, patching, and assessing an EC2 workload.

---

## Services and Features to Watch

| Service / Feature | Cost Risk |
|---|---|
| EC2 instance runtime | Charges if instance is running outside Free Tier or too long |
| EBS volumes | Volumes can remain after instance termination |
| EBS snapshots | Snapshots can accumulate charges |
| Elastic IP | May create charges if unused |
| NAT Gateway | Can create hourly and data-processing charges |
| CloudWatch logs | Log ingestion and storage can create cost |
| Amazon Inspector | May create charges depending on usage |
| Systems Manager | Some features are free, others may create cost depending on configuration |

---

## Cost-Control Rules

Planned rules:

1. Use Free Tier eligible EC2 where possible.
2. Use one AWS region.
3. Stop or terminate EC2 after testing.
4. Delete unused EBS volumes.
5. Avoid unnecessary snapshots.
6. Avoid NAT Gateway unless required.
7. Avoid load balancers for this lab.
8. Confirm Amazon Inspector pricing before enabling.
9. Review CloudWatch log retention.
10. Check billing dashboard after lab sessions.

---

## EC2 Cleanup Checklist

Before ending each AWS lab session:

- [ ] Stop or terminate unused EC2 instances
- [ ] Delete unused EBS volumes
- [ ] Delete unused snapshots
- [ ] Release unused Elastic IP addresses
- [ ] Review security groups
- [ ] Review CloudWatch log groups
- [ ] Review Amazon Inspector status if enabled
- [ ] Review Systems Manager resources if used
- [ ] Check billing dashboard
- [ ] Document remaining resources

---

## Evidence to Collect Later

Later implementation may include:

- Redacted billing screenshot
- EC2 runtime notes
- Cleanup notes
- Cost lessons learned
