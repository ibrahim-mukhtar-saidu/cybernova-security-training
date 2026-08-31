# Bandit Level 25 → 26

## Objective

Analyze an SSH environment and understand how terminal behavior can affect the execution of a restricted shell.

## Investigation Approach

The investigation focused on:

1. Connecting to the authorized SSH environment.
2. Inspecting the available files and permissions.
3. Understanding the restricted shell behavior.
4. Examining terminal dimensions and program behavior.
5. Using the available environment to reach the next training stage.
6. Treating all retrieved credentials as sensitive.

## Security Concepts

- SSH
- Restricted shells
- Terminal control
- Process execution
- Setuid programs
- Linux permissions

## SOC / Blue Team Relevance

Analysts should investigate:

- Unexpected restricted-shell behavior
- Unusual SSH sessions
- Privileged executable execution
- Terminal manipulation
- Unexpected child processes

## MITRE ATT&CK Relevance

Relevant defensive concepts include:

- **T1021.004 — Remote Services: SSH**
- **T1548.001 — Abuse Elevation Control Mechanism: Setuid and Setgid**

## Learning Outcome

This level strengthened understanding of SSH sessions, restricted execution environments, terminal behavior, Linux permissions, and privileged processes.

## Ethical Use

All activity was performed within the authorized OverTheWire environment.
