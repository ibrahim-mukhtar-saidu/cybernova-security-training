# Bandit Level 24 → 25

## Objective

Analyze a network authentication service and understand how multiple candidate credentials can be tested against an authorized service.

## Investigation Approach

The investigation focused on:

1. Identifying the network service.
2. Determining the relevant connection parameters.
3. Understanding the service's authentication protocol.
4. Preparing candidate inputs from the provided training material.
5. Automating repetitive authentication attempts within the authorized challenge environment.
6. Identifying the successful response.
7. Keeping the discovered credential outside the repository.

## Security Concepts

- TCP services
- Network authentication
- Input automation
- Credential validation
- Rate considerations
- Secure credential handling

## SOC / Blue Team Relevance

Defenders should monitor for:

- Repeated authentication failures
- Rapid authentication attempts
- Connection bursts
- Suspicious source addresses
- Automated login behavior
- Account lockout events

## MITRE ATT&CK Relevance

- **T1110 — Brute Force**

The technique is documented here for defensive detection and authorized training purposes.

## Learning Outcome

This level strengthened understanding of network services, authentication workflows, automation, repeated authentication attempts, and detection opportunities.

## Ethical Use

All activity was performed against the authorized OverTheWire Bandit training environment.
