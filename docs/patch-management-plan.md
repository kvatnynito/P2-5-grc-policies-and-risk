# Patch Management Plan

## Status

Planned.

This document will define the planned patch management approach for the EC2 workload.

---

## Purpose

The purpose of this document is to document how operating system updates and patching will be reviewed for an AWS EC2 Linux instance.

Patch management reduces exposure to known vulnerabilities.

---

## Planned Patch Management Goals

The patch management process should support:

- Reviewing current package status
- Applying operating system updates
- Documenting update commands
- Recording before/after status
- Connecting patching to vulnerability remediation
- Reviewing AWS Systems Manager patching concepts

---

## Linux Update Commands to Review

For Ubuntu-based systems:

    sudo apt update
    sudo apt upgrade -y

For Amazon Linux-based systems:

    sudo dnf update -y

or, depending on version:

    sudo yum update -y

---

## Planned Patch Workflow

1. Identify operating system and version.
2. Review available package updates.
3. Apply updates.
4. Reboot if required.
5. Validate service availability.
6. Document before/after status.
7. Review remaining vulnerabilities if using a scanner.

---

## Patch Documentation Table

| Item | Notes |
|---|---|
| Operating system | To be completed |
| Kernel version before patching | To be completed |
| Kernel version after patching | To be completed |
| Update command used | To be completed |
| Reboot required | To be completed |
| Issues encountered | To be completed |
| Remediation notes | To be completed |

---

## AWS Systems Manager Patch Review

Systems Manager may provide patching capabilities for managed EC2 instances.

Planned review:

- Required IAM role
- SSM Agent requirement
- Patch Manager concept
- Maintenance windows concept
- Compliance reporting concept

---

## Risks to Consider

| Risk | Mitigation |
|---|---|
| Running outdated packages | Apply updates |
| No patch documentation | Record before/after status |
| Broken service after patching | Validate after updates |
| Forgotten EC2 instance | Stop or terminate after testing |
| Unclear remediation | Link vulnerabilities to patches |

---

## Planned Evidence

Later implementation may include:

- OS version output
- Update command output
- Patch status notes
- Reboot notes
- Lessons learned
