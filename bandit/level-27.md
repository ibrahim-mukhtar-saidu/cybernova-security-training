# Bandit Level 27 → 28

## Objective

Analyze a Git repository and retrieve information from the repository history within the authorized training environment.

## Investigation Approach

The investigation focused on:

1. Cloning the authorized Git repository.
2. Inspecting repository metadata.
3. Reviewing tracked files.
4. Examining commit history.
5. Identifying information exposed through repository content.
6. Keeping discovered credentials outside the public repository.

## Security Concepts

- Git repositories
- Repository history
- Version control
- Credential exposure
- Secure source-code management

## SOC / Blue Team Relevance

Defenders should monitor repositories for:

- Hard-coded credentials
- Secrets committed to source control
- Sensitive information in commit history
- Accidental secret exposure
- Unauthorized repository modifications

## MITRE ATT&CK Relevance

This exercise provides defensive learning related to:

- **T1552 — Unsecured Credentials**

## Learning Outcome

This level strengthened understanding of Git, repository inspection, commit history, source-control security, and secret management.

## Ethical Use

All investigation activity was performed against the authorized OverTheWire training repository.
