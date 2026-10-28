# GitHub Workflow Using Git Bash

This guide assumes Git for Windows and a GitHub account are available. Replace the repository URL placeholder with your own URL.

## Suggested repository details

- **Name:** `telnet-vs-ssh-wireshark-lab`
- **Description:** `Beginner network security lab comparing Telnet plaintext traffic and SSH encryption using Wireshark, with documented commands, observations, screenshots, and a Git Bash GitHub workflow.`
- **Visibility:** Public only after reviewing all files and confirming no sensitive data is present; otherwise keep it private.

## Option A — Create an empty repository on GitHub first

1. Sign in to GitHub and create a new repository named `telnet-vs-ssh-wireshark-lab`.
2. Add the description above.
3. Since this local folder already has a README, `.gitignore`, and license, do not initialize the GitHub repository with additional files.
4. Open Git Bash and navigate to the extracted project folder.

Example (change the path to where you extracted the ZIP):

```bash
cd /c/Users/YOUR_USERNAME/Downloads/telnet-vs-ssh-wireshark-lab
```

Initialize and review:

```bash
git init
git branch -M main
git status
git add README.md .gitignore LICENSE COMMANDS.md EVIDENCE_CHECKLIST.md GITHUB_WORKFLOW.md LAB_REPORT.md
git add docs evidence notes screenshots scripts captures
git status
git diff --cached
```

Check the staged file list carefully. Git ignores raw `.pcap` and `.pcapng` files by default.

Commit:

```bash
git commit -m "Add Telnet vs SSH Wireshark lab documentation"
```

Connect and push (replace the URL with your own repository URL):

```bash
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/telnet-vs-ssh-wireshark-lab.git
git remote -v
git push -u origin main
```

GitHub may ask you to authenticate in a browser or with a configured credential manager. Do not put a password or token directly in a script or commit it to the repository.

## Option B — If the repository already exists locally

Check the current repository before changing anything:

```bash
git status
git remote -v
git branch
```

If this is already a Git repository, do not run `git init` again unnecessarily. Add the remote only if one is not already configured. Confirm the correct remote before pushing.

## Updating the project later

After adding your genuine screenshots and updating your report:

```bash
git status
git diff
git add README.md COMMANDS.md EVIDENCE_CHECKLIST.md LAB_REPORT.md notes screenshots docs
git status
git diff --cached
git commit -m "Add lab observations and evidence"
git push
```

## Troubleshooting

- **`git: command not found`:** Install Git for Windows, then reopen Git Bash.
- **`remote origin already exists`:** Run `git remote -v`; use `git remote set-url origin YOUR_REPOSITORY_URL` only after verifying the intended URL.
- **Authentication failure:** Follow GitHub's current sign-in/credential-manager prompts. Do not paste credentials into source files.
- **Nothing to commit:** Run `git status`; empty placeholder files may be present, but Git does not track empty directories.
- **Evidence folder not appearing:** Keep the included `.gitkeep` files or add actual evidence files.
- **A capture appears staged:** Unstage it with `git restore --staged path/to/file.pcap`, then verify `.gitignore`. Do not publish captures unless you have inspected and sanitized them.

## Final verification

After pushing, open the repository page and confirm the README renders correctly, folders and Markdown files are visible, and the evidence is genuine and safe to share.
