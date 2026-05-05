# SSH Access Control

## Status

Planned.

This document will define the planned SSH access control approach for the EC2 workload.

---

## Purpose

The purpose of this document is to document secure administrative access to the EC2 Linux instance.

SSH is a common administrative protocol and should be restricted carefully.

---

## SSH Security Goals

The SSH access design should support:

- Key-based authentication
- Restricted source IP access
- No committed private keys
- No password-based login
- Documented administrative access
- Optional review of Session Manager as an alternative

---

## Planned SSH Controls

| Control | Planned Review |
|---|---|
| Key pair created securely | Planned |
| Private key stored safely | Planned |
| Private key excluded from GitHub | Required |
| SSH source restricted | Planned |
| Password authentication disabled | Planned |
| Root SSH login reviewed | Planned |
| Session Manager reviewed | Optional / future |

---

## Security Group SSH Rule

Planned rule:

| Direction | Protocol | Port | Source | Purpose |
|---|---|---|---|---|
| Inbound | TCP | 22 | Trusted public IP only | Administrative SSH access |

Avoid:

| Direction | Protocol | Port | Source | Why Avoid |
|---|---|---|---|---|
| Inbound | TCP | 22 | 0.0.0.0/0 | Exposes SSH to the internet |

---

## Private Key Handling

Private SSH keys must never be committed to GitHub.

Do not commit:

- `.pem` files
- private key files
- screenshots showing private key content
- terminal output exposing secrets
- credential notes

---

## SSH Configuration Items to Review

Potential Linux SSH settings:

| Setting | Purpose |
|---|---|
| PasswordAuthentication | Disable password-based SSH login |
| PermitRootLogin | Restrict root login |
| PubkeyAuthentication | Use key-based authentication |
| AllowUsers | Optional user restriction |
| MaxAuthTries | Limit repeated attempts |

---

## Alternative Access Method

AWS Systems Manager Session Manager may be reviewed as an alternative to direct SSH.

Potential benefits:

- No inbound SSH required
- IAM-based access control
- Session logging options
- Reduced public exposure

This may be reviewed conceptually or implemented later depending on scope.

---

## Planned Evidence

Later implementation may include:

- Redacted security group screenshot
- SSH access test notes
- SSH configuration notes
- Private key handling notes
- Session Manager review notes
