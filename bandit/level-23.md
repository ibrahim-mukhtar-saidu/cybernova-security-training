# Bandit Level 23 → 24

## Objective

Analyze a cron-executed script and understand how automated execution can be used to process files within a controlled Linux environment.

## Environment

| Item | Details |
|---|---|
| Platform | OverTheWire Bandit |
| Source System | Parrot OS |
| Shell | Bash |
| Protocol | SSH |
| SSH Port | 2220 |
| Starting Account | bandit23 |
| Target Account | bandit24 |
| Authorization | Authorized cybersecurity training lab |
| Investigation Type | Scheduled-task and script analysis |

## Investigation Approach

The investigation focused on:

1. Inspecting the cron configuration.
2. Identifying the script executed automatically.
3. Reviewing the script's execution logic.
4. Understanding file ownership and permissions.
5. Determining how the scheduled process handles user-controlled files.
6. Observing the resulting credential retrieval mechanism.
7. Keeping challenge credentials outside the repository.

## Security Concepts

- Linux cron
- Shell scripting
- File permissions
- Automated execution
- Temporary files
- User and process context
- Credential handling

## SOC / Blue Team Relevance

Scheduled scripts should be monitored for:

- Unexpected command execution
- Suspicious file processing
- Writable directories used by privileged processes
- Unusual cron activity
- Unexpected child processes
- Changes to scheduled scripts

## MITRE ATT&CK Relevance

- **T1053.003 — Scheduled Task/Job: Cron**
- **T1059.004 — Command and Scripting Interpreter: Unix Shell**

## Evidence / Screenshot Reference

Recommended sanitized evidence:

- `evidence/screenshots/bandit-23-cron-analysis.png`
- `evidence/screenshots/bandit-23-script-analysis.png`
- `evidence/screenshots/bandit-23-result-redacted.png`

Screenshots must not contain passwords, tokens, private keys, or other sensitive challenge credentials.

## Credential Handling

Bandit credentials are intentionally excluded from the public repository.

Challenge credentials should remain outside the repository or be redacted before documentation is committed.

## Learning Outcome

This level strengthened practical understanding of Linux cron, shell scripting, file permissions, automated execution, temporary-file handling, process context, and defensive monitoring of scheduled activity.

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
