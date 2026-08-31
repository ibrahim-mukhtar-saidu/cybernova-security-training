# Bandit Level 26 → 27

## Objective

Analyze a restricted shell environment and understand how an executable's behavior and terminal interaction affect command execution.

## Investigation Approach

The investigation focused on:

1. Connecting using the authorized SSH key.
2. Examining the restricted environment.
3. Understanding the behavior of the provided executable.
4. Investigating terminal and shell interaction.
5. Obtaining access to the next authorized training account.
6. Keeping the private SSH key outside the repository.

## Security Concepts

- SSH private keys
- File permissions
- Restricted shells
- Terminal behavior
- Setuid execution
- Privilege boundaries

## SOC / Blue Team Relevance

Security analysts should monitor:

- SSH private-key authentication
- Unauthorized key usage
- Setuid binaries
- Unexpected shell spawning
- Privilege-boundary violations

## Credential Handling

The SSH private key used during this challenge is intentionally excluded from Git through `.gitignore`.

## Learning Outcome

This level strengthened practical understanding of SSH key authentication, restricted shells, terminal behavior, setuid programs, and credential protection.

## Ethical Use

All activity was performed against the authorized OverTheWire Bandit environment.
