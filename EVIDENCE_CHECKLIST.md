# Evidence Checklist

Use your own screenshots from the lab. These filenames are suggested; adapt them to match the evidence you actually collected.

## Screenshots

- [ ] `screenshots/01-wireshark-loopback-capture.png` — Wireshark capture running on loopback.
- [ ] `screenshots/02-telnet-filter.png` — packets identified with the `telnet` display filter.
- [ ] `screenshots/03-telnet-stream.png` — Follow TCP Stream view showing only harmless test data; redact anything sensitive.
- [ ] `screenshots/04-ssh-filter.png` — packets identified with the `ssh` display filter.
- [ ] `screenshots/05-ssh-stream.png` — Follow TCP Stream view demonstrating that session application contents are not readable as plaintext.
- [ ] `screenshots/06-comparison-notes.png` — optional screenshot of your completed comparison or report.

## Supporting evidence

- [ ] Record OS/VM and Wireshark version in `LAB_REPORT.md`.
- [ ] Record the exact filters and commands in `COMMANDS.md` if they differ from the template.
- [ ] Complete `notes/observations.md` with your own findings.
- [ ] Answer the reflection questions in `LAB_REPORT.md`.
- [ ] Confirm screenshots are legible and do not expose passwords, tokens, private keys, real usernames, or unnecessary private network details.
- [ ] Check `git status --ignored` and confirm raw captures are not being staged.
- [ ] Review the final repository page after pushing.

## Before publishing

- [ ] No real credentials or secrets.
- [ ] No unreviewed `.pcap` / `.pcapng` files.
- [ ] No misleading claim that unperformed work is complete.
- [ ] README and report reflect the actual environment and observations.
