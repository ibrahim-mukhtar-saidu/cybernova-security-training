# CYBERNOVA CTF Training — OverTheWire Bandit

![Platform](https://img.shields.io/badge/Platform-OverTheWire-blue)
![Focus](https://img.shields.io/badge/Focus-Linux%20%7C%20Networking%20%7C%20Security-red)
![Levels](https://img.shields.io/badge/Bandit-00--20-green)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

## Overview

This repository documents my hands-on cybersecurity training through the
OverTheWire Bandit wargame.

The purpose of this project is not simply to complete CTF levels. It is to
develop practical skills in Linux administration, command-line investigation,
file permissions, encoding, compression, networking, authentication, SSH,
TLS/SSL, service enumeration, restricted environments, and privilege
escalation.

The exercises are documented as a structured cybersecurity learning record
with technical explanations, observed results, lessons learned, security
implications, and selected evidence.

---

## Objectives

The primary objectives of this training are to:

- Develop strong Linux command-line skills.
- Understand Linux filesystem permissions and ownership.
- Investigate files and directories using native Linux tools.
- Work with hidden files and unusual filenames.
- Identify and process encoded data.
- Analyze compressed and archived files.
- Use pattern matching and text-processing utilities.
- Develop basic network enumeration skills.
- Understand TCP-based services.
- Work with SSH authentication.
- Understand TLS/SSL connections.
- Analyze service behavior.
- Understand restricted shell environments.
- Identify and understand SUID executables.
- Understand real UID versus effective UID.
- Practice basic privilege-escalation concepts.
- Develop structured cybersecurity investigation habits.
- Connect technical findings to defensive and SOC use cases.

---

## Training Environment

| Component | Details |
|---|---|
| Training Platform | OverTheWire Bandit |
| Operating System | Parrot OS |
| Shell | Bash |
| Primary Language | Linux shell commands |
| Networking Tools | Nmap, OpenSSL, SSH |
| Target Environment | OverTheWire Bandit Linux server |
| Training Type | Authorized cybersecurity lab |
| Documented Range | Bandit 00 → 20 |

---

## Skills Demonstrated

### Linux

- Filesystem navigation
- File discovery
- Hidden-file identification
- File permissions
- File ownership
- Symbolic links
- Special filenames
- Text processing
- File type identification
- Compression and archive handling

### Networking

- Local TCP communication
- Port enumeration
- Service discovery
- Service/version detection
- Client/server communication

### Authentication & Cryptography

- SSH authentication
- SSH private keys
- TLS/SSL connections
- Certificate inspection
- Secure credential transmission

### Security

- SUID analysis
- Effective UID identification
- Privilege escalation concepts
- Restricted shell analysis
- Authentication service analysis
- Attack-surface enumeration

---

## Bandit Progress

| Level | Primary Security / Technical Focus | Status |
|---|---|---|
| 00 → 01 | Basic Linux file access | Completed |
| 01 → 02 | Special filename handling | Completed |
| 02 → 03 | Filenames containing spaces | Completed |
| 03 → 04 | Hidden files | Completed |
| 04 → 05 | File identification | Completed |
| 05 → 06 | File properties and permissions | Completed |
| 06 → 07 | System-wide file discovery | Completed |
| 07 → 08 | Searching structured text | Completed |
| 08 → 09 | Duplicate/unique data analysis | Completed |
| 09 → 10 | Human-readable strings | Completed |
| 10 → 11 | Base64 encoding | Completed |
| 11 → 12 | Character transformation | Completed |
| 12 → 13 | Multi-layer compression | Completed |
| 13 → 14 | SSH private-key authentication | Completed |
| 14 → 15 | TCP/TLS authentication | Completed |
| 15 → 16 | TLS service interaction | Completed |
| 16 → 17 | Network enumeration and SSH key extraction | Completed |
| 17 → 18 | File comparison | Completed |
| 18 → 19 | Restricted shell / non-interactive SSH | Completed |
| 19 → 20 | SUID privilege escalation | Completed |
| 20 → 21 | TCP client/server authentication | In Progress |

---

## Documentation Structure

Each level has a dedicated technical report:

```text
bandit/
├── level-00.md
├── level-01.md
├── level-02.md
├── ...
├── level-19.md
└── level-20.md

Each report documents:

Objective
Environment
Scenario / challenge
Initial reconnaissance
Commands used
Command-by-command explanation
Observed result
Technical analysis
Security concept
Skills demonstrated
Defensive / SOC relevance
Lessons learned
Evidence / screenshot reference
Credential-handling note
Ethical / lab scope note
Knowledge Notes

Cross-level security concepts are consolidated in:

notes/
├── linux.md
├── networking.md
├── ssh.md
├── tls.md
└── privilege-escalation.md

These notes summarize the broader concepts learned during the practical
exercises.

Evidence

Selected screenshots and supporting evidence are stored under:

evidence/screenshots/

Evidence is intended to demonstrate important technical activities such as:

Linux investigation
File and permission analysis
Network enumeration
TLS connections
SSH authentication
Service identification
Restricted shell behavior
SUID analysis

The repository intentionally avoids storing sensitive authentication material.

Credential Handling

Credentials obtained during the training exercises are not published in
this repository.

Passwords are represented as:

[REDACTED]

Private SSH keys and other authentication material are intentionally excluded
from public documentation.

The purpose of the repository is to demonstrate technical methodology,
security reasoning, and practical skills rather than expose credentials.

Defensive / SOC Relevance

Although Bandit is a Linux-based CTF environment, many of the skills practiced
here have direct relevance to security operations.

Examples include:

Enumeration

Understanding how services and files can be discovered helps security analysts
recognize attack-surface enumeration and investigate suspicious activity.

Authentication

Working with SSH, TLS, and credentials provides practical exposure to
authentication mechanisms that frequently appear in security monitoring.

Privilege Escalation

Analyzing SUID binaries demonstrates how excessive or unsafe privileges can
be abused to execute actions with elevated permissions.

File Investigation

Searching, identifying, comparing, and processing files develops foundational
skills useful during host-based investigations.

Command-Line Analysis

Linux command-line proficiency is valuable when investigating servers,
security appliances, cloud workloads, and incident-response environments.

Ethical Use

All activities documented in this repository were performed in an authorized
training environment provided for cybersecurity education.

The techniques should only be used against systems for which explicit
authorization has been provided.

Disclaimer

This repository is a cybersecurity education and portfolio project.

The documented techniques are intended for:

Authorized laboratories
CTF competitions
Cybersecurity education
Defensive security research
Systems owned or explicitly authorized by the tester

Unauthorized use of security techniques against third-party systems may be
illegal or harmful.

Learning Approach

For each challenge, I aim to follow a repeatable investigation process:

Observe
   ↓
Enumerate
   ↓
Form a hypothesis
   ↓
Test with appropriate tools
   ↓
Analyze the result
   ↓
Identify the security concept
   ↓
Document evidence
   ↓
Connect the technique to defensive security

This approach is intended to develop transferable cybersecurity investigation
skills rather than memorization of individual commands.

Project Status

Current training: Bandit 20 → 21

Documented range: Bandit 00 → 20

Next objective: Complete the remaining Bandit challenges and continue
expanding the technical notes and evidence collection.

Author

Ibrahim Mukhtar Saidu

Aspiring Cybersecurity Analyst | SOC & Blue Team

CYBERNOVA AI

Related Portfolio

This CTF training is part of the broader CYBERNOVA AI cybersecurity portfolio,
which includes practical projects involving:

Security monitoring
Threat detection
Incident response
Threat intelligence
Linux security
Windows security monitoring
Cloud security monitoring
Identity and access security
SIEM concepts
Python security automation
