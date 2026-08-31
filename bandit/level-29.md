# Bandit Level 29 → 30

## Objective

Investigate Git branches and repository history to identify information available outside the default branch.

## Investigation Approach

The investigation focused on:

1. Inspecting available branches.
2. Comparing branch contents.
3. Reviewing commits.
4. Identifying development-related repository data.
5. Treating discovered credentials as sensitive.

## Security Concepts

- Git branches
- Remote branches
- Development environments
- Source-control exposure
- Credential security

## SOC / Blue Team Relevance

Development branches can unintentionally expose:

- Credentials
- Debug information
- Internal configuration
- Security-sensitive code
- Testing artifacts

Security teams should apply secret scanning and access controls across all branches.

## MITRE ATT&CK Relevance

- **T1552 — Unsecured Credentials**

## Learning Outcome

This level strengthened understanding of Git branch enumeration, development artifacts, repository security, and credential exposure.
