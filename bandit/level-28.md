# Bandit Level 28 → 29

## Objective

Investigate Git commit history to identify information that was present in previous revisions but removed from the current version.

## Investigation Approach

The investigation focused on:

1. Cloning the authorized repository.
2. Inspecting the current repository state.
3. Reviewing commit history.
4. Comparing revisions.
5. Identifying historical content.
6. Treating discovered credentials as sensitive.

## Security Concepts

- Git history
- Commit comparison
- Deleted information
- Source-control security
- Credential exposure

## SOC / Blue Team Relevance

Security teams should understand that deleting a secret from the latest version does not necessarily remove it from repository history.

Controls should include:

- Secret scanning
- Repository history review
- Credential rotation
- Access control
- Secure secret storage

## MITRE ATT&CK Relevance

- **T1552 — Unsecured Credentials**

## Learning Outcome

This level demonstrated why historical source-control data must be considered when investigating potential credential exposure.
