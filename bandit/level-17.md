# Bandit Level 17 → 18

## Objective

Identify the changed credential between two password files and use the resulting credential to authenticate to the Bandit Level 18 account.

## Investigation Approach

The challenge provided two files containing password data. The investigation focused on comparing the files and identifying the entry that differed.

The workflow was:

1. Access the Bandit Level 17 environment using the SSH private key obtained from the previous level.
2. Inspect the available password files.
3. Compare the files to identify the changed entry.
4. Treat the differing value as the credential for the next level.
5. Use SSH to authenticate to the Bandit Level 18 account.

## Techniques and Commands

The investigation involved:

- SSH private-key authentication
- File inspection
- Text-file comparison
- diff for identifying differences
- Secure credential handling

A representative comparison command is:

    diff passwords.old passwords.new

The differing entry identifies the credential required for the next authentication step.

## Security Concepts

### File Comparison

Comparing two versions of a file can reveal unauthorized modifications, configuration changes, or changed credentials.

The diff utility provides a concise way to identify differences between text files.

### Credential Security

Credentials discovered during a controlled security exercise should not be copied into public documentation.

Only the investigative method and sanitized results are documented in this repository.

### SSH Authentication

SSH can authenticate users using either passwords or cryptographic key pairs, depending on the server configuration.

## SOC / Blue Team Relevance

File comparison is useful during security investigations when analysts need to determine whether a configuration, account database, script, or other important file has changed.

Potential defensive applications include:

- Detecting unauthorized file modifications
- Investigating configuration drift
- Comparing known-good and suspicious files
- Supporting incident-response investigations
- Validating changes during security reviews

## MITRE ATT&CK Relevance

This exercise primarily develops defensive investigation skills rather than demonstrating a specific adversary technique.

Relevant concepts include:

- File and directory discovery
- Credential access awareness
- Valid account authentication
- Investigation of changes to security-relevant files

MITRE ATT&CK mappings should be treated as contextual rather than claiming that the Bandit challenge itself represents real-world adversary activity.

## Evidence / Screenshot Reference

Recommended evidence:

- Comparison of the two password files with sensitive output redacted
- Successful authentication to the next authorized Bandit level
- Terminal evidence showing the comparison workflow

Sensitive credentials must not appear in screenshots committed to the repository.

## Credential Handling

No Bandit password or private credential is intentionally stored in this repository.

Challenge credentials should remain outside the public project directory or be redacted before documentation is committed.

## Learning Outcome

This level strengthened practical understanding of file comparison, credential handling, SSH authentication, and investigation of changes between two versions of a file.

## Ethical Use

This documentation is based on authorized activity within the OverTheWire Bandit training environment.

The techniques described should only be used against systems for which explicit authorization has been provided.
