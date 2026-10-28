# Telnet vs SSH Traffic Analysis with Wireshark

A beginner-friendly network security lab comparing Telnet and SSH traffic in a controlled local environment. The goal is to observe how Telnet can expose application data as readable plaintext, while SSH encrypts session contents.

> **Safety:** Run this lab only on systems and accounts you are authorized to use. Use a dedicated test account and harmless test data. Never commit passwords, tokens, private keys, or packet captures containing credentials to a public repository.

## Repository contents

- `captures/` — location for approved, sanitized capture files; raw captures are ignored by Git by default.
- `docs/` — lab reference material and supporting documentation.
- `evidence/` — evidence inventory and submission notes.
- `notes/` — observations and reflection answers.
- `screenshots/` — screenshots showing filters and stream inspection.
- `scripts/` — optional helper scripts (no automated scanning or remote targeting).
- `COMMANDS.md` — commands and Wireshark filters used in the lab.
- `EVIDENCE_CHECKLIST.md` — checklist for collecting and reviewing evidence.
- `GITHUB_WORKFLOW.md` — Git Bash workflow for creating and pushing the repository.
- `LAB_REPORT.md` — report template for recording your own results.

## Lab objectives

1. Start a Wireshark capture on the loopback interface.
2. Generate a local Telnet session and identify its packets.
3. Follow the Telnet TCP stream and observe readable application data where present.
4. Generate a local SSH session and identify SSH traffic.
5. Follow the SSH TCP stream and compare it with the Telnet stream.
6. Explain why SSH is preferred for secure remote administration.

## Environment

Complete this section with the environment you actually used.

- Operating system / VM: `TODO`
- Wireshark version: `TODO`
- Telnet service and port: `TODO`
- SSH service and port: `TODO`
- Capture interface: `lo` / `TODO`
- Date performed: `TODO`

## Quick start

1. Review `docs/` and `COMMANDS.md`.
2. Perform the exercise in your own authorized lab.
3. Save screenshots in `screenshots/` using the filenames in `EVIDENCE_CHECKLIST.md`.
4. Record actual observations in `notes/observations.md` and complete `LAB_REPORT.md`.
5. Review every file for secrets and personal information.
6. Follow `GITHUB_WORKFLOW.md` to initialize Git and push to GitHub.

## Expected comparison

| Observation | Telnet | SSH |
|---|---|---|
| Wireshark display filter | `telnet` | `ssh` |
| Application content in Follow TCP Stream | May be readable as plaintext | Session content should be encrypted and not readable as application plaintext |
| Credential exposure risk | High on untrusted networks | Designed to protect credentials and session data |
| Suitable for secure administration | No | Yes |

Actual packet visibility depends on the service, client, capture point, and session configuration. Record what your own capture shows rather than assuming a result.

## Evidence and privacy

Use only synthetic test data. Before publishing, inspect screenshots and any proposed capture files for credentials, tokens, usernames, hostnames, private addresses, or other sensitive information. The `.gitignore` excludes common packet-capture files by default; do not override it unless you have confirmed a capture is sanitized and safe to publish.

## Repository suggestion

- **Repository name:** `telnet-vs-ssh-wireshark-lab`
- **Description:** `Beginner network security lab comparing Telnet plaintext traffic and SSH encryption using Wireshark, with documented commands, observations, screenshots, and a Git Bash GitHub workflow.`

## Status

This repository is a documentation and evidence template. Replace every `TODO` and add your own genuine screenshots and observations after completing the lab. Do not claim a step was completed unless you performed it.
