# Bandit Level 21 → 22

## Objective

Investigate a scheduled task that periodically executes a script and determine how the task is used to obtain the credential for the Bandit Level 22 account.

## Investigation Approach

The challenge focused on Linux scheduled tasks and the security implications of scripts executed automatically by the system.

The investigation involved:

1. Accessing the Bandit Level 21 environment.
2. Inspecting the system cron configuration.
3. Identifying the scheduled task associated with the Bandit account.
4. Examining the script executed by the scheduled task.
5. Understanding which account and files were involved in the scheduled execution.
6. Following the authorized execution path to obtain the next-level credential.
7. Keeping the credential out of the public repository.

## Techniques and Commands

The investigation involved:

- Linux cron
- Scheduled task analysis
- File inspection
- Shell-script analysis
- File permissions
- Secure credential handling

Representative investigation commands include:

    ls -la /etc/cron.d/

    cat /etc/cron.d/<relevant-job>

    ls -la /usr/bin/<relevant-script>

    cat /usr/bin/<relevant-script>

The exact filenames and sensitive credential output should not be included in public documentation unless they are intentionally sanitized.

## Security Concepts

### Cron

Cron is a Linux scheduling mechanism used to execute commands or scripts automatically at specified times.

Scheduled tasks are important security-monitoring artifacts because they can provide persistence or execute administrative operations without direct user interaction.

### Scheduled Scripts

A cron job may execute a shell script or another program.

Security analysts should examine:

- Script ownership
- File permissions
- Executed commands
- Referenced files
- User context
- Output destinations

Unexpected modifications to scheduled scripts can create security risks.

### File Permissions

The security of a scheduled task depends partly on who can modify the files and scripts involved.

Scripts executed automatically should have appropriate ownership and permissions so unauthorized users cannot alter their behavior.

### Credential Security

Credentials obtained during a controlled security exercise should be treated as sensitive information.

Challenge passwords were not included in this repository.

## SOC / Blue Team Relevance

Cron analysis is relevant to defensive security because scheduled tasks can be abused for persistence and automated execution.

A SOC analyst investigating a Linux host may review:

- `/etc/cron.d/`
- `/etc/crontab`
- User crontabs
- Scheduled scripts
- File ownership and permissions
- Recent changes to scheduled-task configuration

Useful investigation questions include:

- What scheduled tasks exist?
- Which user executes them?
- What scripts do they launch?
- Can an unprivileged user modify those scripts?
- What files or commands do the scripts access?

## MITRE ATT&CK Relevance

This exercise provides defensive learning related to:

- **T1053 — Scheduled Task/Job**
- **T1053.003 — Scheduled Task/Job: Cron**

These mappings are provided for security-learning purposes and do not imply that the Bandit challenge itself represents a real-world intrusion.

## Evidence / Screenshot Reference

Recommended sanitized evidence:

- `evidence/screenshots/bandit-21-cron-configuration.png`
- `evidence/screenshots/bandit-21-script-analysis.png`
- `evidence/screenshots/bandit-21-permissions.png`
- `evidence/screenshots/bandit-21-result-redacted.png`

Screenshots must not contain passwords, tokens, private keys, or other sensitive credentials.

## Credential Handling

No Bandit password is intentionally stored in this repository.

Challenge credentials should remain outside the public project directory or be redacted before screenshots and documentation are committed.

## Learning Outcome

This level strengthened practical understanding of Linux cron, scheduled-task analysis, shell scripts, file permissions, automated execution, credential handling, and defensive monitoring of persistence-related mechanisms.

## Ethical Use

This documentation is based on authorized activity within the OverTheWire Bandit training environment.

The techniques described should only be used against systems for which explicit authorization has been provided.
