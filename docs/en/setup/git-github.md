# Git & GitHub

This guide covers the basics of setting up Git and GitHub for version control.

## 1. Install Git

- **Windows (WSL / Ubuntu)**: `sudo apt install -y git`
- **macOS**: `brew install git` (see [macOS setup](mac.md))
- **Linux**: `sudo apt install -y git`

Verify:

```bash
git --version
```

## 2. Configure Git

Set your name and email (these will appear in your commit history):

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

## 3. Create a GitHub Account

If you do not have one, create a free account at:  
[https://github.com/](https://github.com/)

Use your institutional or personal email address.

## 4. Authenticate with GitHub

The recommended way to authenticate is via **SSH keys** or the **GitHub CLI**.

### Option A: SSH Key

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
cat ~/.ssh/id_ed25519.pub
```

Copy the output and add it to GitHub: **Settings → SSH and GPG keys → New SSH key**.

### Option B: GitHub CLI

```bash
# Install gh (macOS)
brew install gh

# Install gh (Ubuntu/WSL)
sudo apt install gh

# Authenticate
gh auth login
```

## 5. Clone a Repository

```bash
git clone git@github.com:<username>/<repository>.git
```

## 6. Basic Git Workflow

```bash
git status           # check what has changed
git add .            # stage all changes
git commit -m "msg"  # commit with a message
git push             # push to GitHub
git pull             # pull latest changes
```

---

[← Back to Setup Overview](index.md)
