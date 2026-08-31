# Bandit Level 31 → 32

## Objective

Interact with an authorized Git repository by creating and pushing the required file to the expected branch.

## Investigation Approach

The investigation focused on:

1. Inspecting the repository README.
2. Identifying the required filename.
3. Creating the required file with the challenge-provided content.
4. Reviewing Git status.
5. Committing the change.
6. Confirming the correct remote and branch.
7. Pushing the commit to the authorized repository.
8. Recording the server response without storing credentials.

## Security Concepts

- Git commits
- Remote repositories
- Branch management
- Git push
- Repository validation
- Secure credential handling

## SOC / Blue Team Relevance

Git monitoring can detect:

- Unexpected repository changes
- Unauthorized pushes
- Suspicious branch modifications
- Changes to sensitive files
- Supply-chain security issues

## Learning Outcome

This level strengthened practical Git workflow skills, remote repository interaction, branch management, and secure handling of challenge credentials.

## Ethical Use

All repository activity was performed against the authorized OverTheWire Bandit environment.
