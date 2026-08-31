# Bandit Level 18 → 19

## Objective

Access the Bandit Level 19 environment when the normal interactive SSH session is restricted, and retrieve the required challenge credential without exposing sensitive information in the repository.

## Investigation Approach

The challenge demonstrated how an SSH account can restrict normal interactive access while still allowing specific remote commands to be executed.

The investigation focused on:

1. Attempting normal SSH authentication.
2. Observing the restricted-session behavior.
3. Determining whether a specific remote command could be executed.
4. Using non-interactive SSH command execution to access the challenge file.
5. Treating the resulting credential as sensitive information.
6. Keeping the credential outside the public repository.

## Techniques and Commands

The investigation involved:

- SSH authentication
- Non-interactive SSH command execution
- Remote file access
- Restricted shell analysis
- Secure credential handling

A representative command pattern is:

    ssh -p 2220 bandit18@bandit.labs.overthewire.org cat readme

This demonstrates that SSH can be used to request a specific remote command rather than relying exclusively on an interactive shell.

## Security Concepts

### Restricted Shells

A restricted account can limit interactive shell functionality after authentication. This can be used as an access-control mechanism to reduce the actions available to a user.

### Non-Interactive SSH

SSH supports execution of a specified command on the remote system.

From a defensive perspective, administrators and SOC analysts should understand how remote command execution behaves and how restricted accounts are configured.

### Access Control

Restricting interactive access can reduce the attack surface of service accounts and specialized accounts.

However, administrators should verify that permitted commands cannot unintentionally provide access to sensitive resources.

### Credential Security

Credentials discovered during a controlled security exercise should be treated as sensitive information.

No challenge password is included in this documentation.

## SOC / Blue Team Relevance

This level provides practical exposure to:

- SSH authentication behavior
- Restricted accounts
- Remote command execution
- Access-control analysis
- Credential protection
- Investigation of unusual authentication behavior

These concepts are relevant when investigating potentially suspicious SSH activity in a SOC environment.

## MITRE ATT&CK Relevance

The exercise provides useful defensive context for:

- **T1021.004 — Remote Services: SSH**
- **T1059 — Command and Scripting Interpreter**

The mapping is included for defensive learning and should not be interpreted as evidence that the Bandit challenge itself represents a real-world intrusion.

## Evidence / Screenshot Reference

Recommended evidence:

- SSH authentication attempt
- Restricted-session behavior
- Authorized non-interactive command execution
- Successful challenge completion, with sensitive credentials redacted

Example evidence paths:

    evidence/screenshots/bandit-18-ssh-restricted.png
    evidence/screenshots/bandit-18-command-execution.png
    evidence/screenshots/bandit-18-result-redacted.png

Sensitive passwords must not appear in committed screenshots.

## Credential Handling

Challenge credentials are intentionally excluded from this repository.

The local credential file is protected and ignored by Git:

- `bandit-credentials.txt`
- `*.sshkey`

Private credentials and SSH keys should remain outside the public repository.

## Learning Outcome

This level strengthened practical understanding of SSH authentication, restricted environments, non-interactive remote command execution, access control, and secure credential handling.

## Ethical Use

This documentation is based on authorized activity within the OverTheWire Bandit training environment.

The techniques described should only be used against systems for which explicit authorization has been provided.
