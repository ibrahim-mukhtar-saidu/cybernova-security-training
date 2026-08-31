# Bandit Level 30 → 31

## Objective

Investigate Git metadata and identify information stored in a repository tag.

## Investigation Approach

The investigation focused on:

1. Inspecting repository history.
2. Enumerating Git tags.
3. Inspecting the discovered tag.
4. Determining the object type referenced by the tag.
5. Reading the object content.
6. Treating the resulting credential as sensitive.

## Techniques

Representative commands included:

    git tag -l
    git show <tag>
    git cat-file -t <tag>
    git cat-file -p <tag>

## Security Concepts

- Git tags
- Git objects
- Repository metadata
- Credential exposure
- Source-control security

## SOC / Blue Team Relevance

Security analysts should consider Git metadata and historical objects during investigations because sensitive information can exist outside normal tracked files.

## MITRE ATT&CK Relevance

- **T1552 — Unsecured Credentials**

## Learning Outcome

This level strengthened understanding of Git objects, tags, repository metadata, and source-control secret exposure.

## Ethical Use

The repository was investigated only within the authorized OverTheWire training environment.
