# SD4ALL Mac Development Setup Guide

## 1. What is a Repository (Repo)?

A **repository** is a folder tracked by Git that stores your code, documents, and history of every change. Think of it like a project folder with a built-in time machine.

### How to Select / Work with Repositories

**You already have one!** This repo (`SD4ALL-AI-Lab`) lives on GitHub at:
`https://github.com/esteves-pixel/SD4ALL-AI-Lab`

**On your Mac, to clone (download) it:**
```bash
# 1. Open Terminal (Cmd + Space, type "Terminal")
# 2. Navigate to where you want your projects
cd ~/Projects

# 3. Clone your repo
git clone https://github.com/esteves-pixel/SD4ALL-AI-Lab.git

# 4. Enter the repo
cd SD4ALL-AI-Lab
```

**To switch between repos**, just `cd` into different folders. Each folder with a `.git` directory is a repo.

### Key Git Commands You'll Use Daily
```bash
git status              # See what changed
git add .               # Stage all changes
git commit -m "message" # Save a snapshot
git push                # Upload to GitHub
git pull                # Download latest from GitHub
```

---

## 2. Cloud Environments — What Are They?

A **cloud environment** is a computer running somewhere else (AWS, Google Cloud, etc.) that you connect to from your Mac. You're using one right now — this Claude Code session runs in the cloud.

### Types You'll Encounter

| Environment | What It Is | When to Use |
|---|---|---|
| **GitHub Codespaces** | VS Code in your browser, connected to your repo | Quick edits, no local setup needed |
| **Claude Code (Web)** | This! Claude AI with access to your repo | AI-assisted development, automation |
| **Google Colab** | Free Jupyter notebooks with GPU | ML experiments, data analysis |
| **AWS / GCP / Azure** | Full cloud servers | Production deployments, heavy compute |

### What You Need on Your Mac (Local Setup)

```bash
# 1. Install Homebrew (Mac package manager)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 2. Install essential tools
brew install git python@3.12 node

# 3. Install Claude Code CLI (so you can use me from Terminal)
npm install -g @anthropic-ai/claude-code

# 4. Install VS Code
brew install --cask visual-studio-code

# 5. Install Conda (Python environment manager)
brew install --cask miniconda
conda init zsh  # restart Terminal after this
```

### How Local + Cloud Work Together

```
Your Mac (local)                    Cloud
┌─────────────────┐     git push    ┌──────────────┐
│ VS Code / Claude │ ──────────────→│   GitHub     │
│ Code CLI         │                │  (your repo) │
│                  │ ←──────────────│              │
│ Edit, test,      │    git pull    └──────┬───────┘
│ run locally      │                       │
└─────────────────┘                        │ triggers
                                    ┌──────┴───────┐
                                    │ Claude Code  │
                                    │ (cloud AI)   │
                                    │ GitHub Actions│
                                    │ (automation) │
                                    └──────────────┘
```

**You edit locally on your Mac → push to GitHub → cloud services react.**

---

## 3. Recommended Mac Folder Structure

```
~/Projects/
├── SD4ALL-AI-Lab/          ← This repo (BPM system, AI, data)
├── sd4all-website/         ← Future: your business website
└── sd4all-operations/      ← Future: ops documentation
```

---

## 4. Daily Workflow

1. **Open Terminal** on your Mac
2. `cd ~/Projects/SD4ALL-AI-Lab`
3. `git pull` to get latest changes
4. Work on your files (VS Code, Jupyter, etc.)
5. `git add . && git commit -m "what I did" && git push`
6. Or open Claude Code: `claude` in Terminal to get AI help

---

## 5. Quick Reference: Where Things Live

| What | Where | How to Access |
|---|---|---|
| Your code & docs | GitHub repo | `git clone` / VS Code |
| AI assistant | Claude Code | Terminal: `claude` or web |
| Python notebooks | `notebooks/` folder | Jupyter / VS Code / Colab |
| Business processes | `bpm/` folder | Markdown files in repo |
| Data & KPIs | `data/` folder | Python scripts, dashboards |
