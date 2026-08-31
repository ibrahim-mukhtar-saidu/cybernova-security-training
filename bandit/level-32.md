# Bandit Level 32 → 33

## Objective

Analyze an uppercase-restricted shell and understand how shell parsing and environment behavior can affect command execution.

## Investigation Approach

The investigation focused on:

1. Connecting to the authorized Bandit account.
2. Observing that entered commands were converted to uppercase.
3. Testing shell behavior.
4. Understanding the difference between the restricted command interface and the underlying shell.
5. Reaching the underlying shell environment.
6. Verifying the resulting execution context.
7. Retrieving the final challenge credential while keeping it out of the repository.

## Security Concepts

- Shell parsing
- Environment variables
- Restricted shells
- Command interpretation
- Process execution
- Privilege boundaries

## SOC / Blue Team Relevance

Analysts should investigate:

- Unexpected shell transitions
- Restricted-shell bypass indicators
- Unexpected interpreter execution
- Child processes spawned by privileged programs
- Changes in execution context

## MITRE ATT&CK Relevance

- **T1059.004 — Command and Scripting Interpreter: Unix Shell**

## Learning Outcome

This level strengthened understanding of shell parsing, restricted execution environments, process context, and defensive monitoring of shell activity.

## Ethical Use

All activity was performed within the authorized OverTheWire Bandit environment.
