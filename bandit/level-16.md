# Bandit Level 16 → 17

## Objective

Authenticate to the Bandit Level 17 account using the private SSH key obtained during the Level 16 challenge.

## Environment

| Item | Details |
|---|---|
| Platform | OverTheWire Bandit |
| Source System | Parrot OS |
| Shell | Bash |
| Protocol | SSH |
| SSH Port | 2220 |
| Starting Account | bandit16 |
| Target Account | bandit17 |
| Authorization | Authorized cybersecurity training lab |
| Investigation Type | Network service enumeration and TLS service interaction |

## Investigation Approach

The challenge involved identifying the appropriate network service, interacting with the service securely, retrieving the SSH private key, protecting it with restrictive permissions, validating the key, and using it for SSH authentication.

## Techniques and Commands

The investigation used:

- Nmap for service enumeration
- OpenSSL for TLS service interaction
- SSH for remote authentication
- ssh-keygen for SSH key validation
- chmod for protecting private-key permissions

The recovered key was stored outside the Git repository and protected with restrictive permissions.

## Security Concepts

### Service Enumeration

Network service enumeration helps identify exposed services and determine which protocols are available on a host.

### TLS

TLS provides encrypted communication between a client and service. OpenSSL can be used to interact with and investigate TLS-enabled services.

### SSH Key Authentication

SSH public-key authentication uses a private key on the client and a corresponding public key on the server.

Private keys must be protected because unauthorized possession may allow authenticated access.

### File Permissions

The private key was restricted with:

`chmod 600`

This limits access to the file owner.

## SOC / Blue Team Relevance

This challenge demonstrates practical skills relevant to security operations:

- Network service enumeration
- Protocol identification
- TLS investigation
- SSH authentication
- Secure credential handling
- Private-key protection
- Authentication troubleshooting

## MITRE ATT&CK Relevance

Potentially relevant defensive ATT&CK techniques include:

- **T1078 — Valid Accounts**
- **T1021.004 — Remote Services: SSH**

These mappings are provided for defensive learning.

## Evidence / Screenshot Reference

Recommended evidence:

- `evidence/screenshots/bandit-16-service-enumeration.png`
- `evidence/screenshots/bandit-16-key-validation.png`
- `evidence/screenshots/bandit-16-ssh-authentication.png`

Screenshots must be sanitized and must not contain passwords, private SSH keys, tokens, or other credentials.

## Credential Handling

Sensitive challenge credentials are intentionally excluded from this repository.

The repository uses `.gitignore` entries for:

- `bandit-credentials.txt`
- `*.sshkey`

Private keys should remain outside the public repository.

## Learning Outcome

This level strengthened practical understanding of service enumeration, TLS interaction, SSH key authentication, file permissions, and secure credential handling.

## Limitations

This exercise was performed in the controlled OverTheWire Bandit training
environment and therefore does not reproduce the complexity of a production
enterprise environment.

Limitations include:

- Synthetic or intentionally constructed challenge conditions.
- Limited system and network scope.
- No production authentication infrastructure.
- No enterprise SIEM, EDR, identity platform, or centralized logging.
- No real organizational incident-response process.
- Challenge objectives may simplify real-world investigative scenarios.
- Results should not be interpreted as evidence of production security
  capability by themselves.

The primary value of the exercise is the development of transferable Linux,
command-line investigation, analytical reasoning, evidence-handling, and
security-documentation skills.

## Ethical Use

This documentation is based on authorized activity within the OverTheWire Bandit training environment.

The techniques described should only be used against systems for which explicit authorization has been provided.
