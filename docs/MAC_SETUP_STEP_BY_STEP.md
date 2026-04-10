# SD4ALL — Mac Setup: Step-by-Step

Follow these steps **in order**. Open **Terminal** on your Mac (press `Cmd + Space`, type `Terminal`, hit Enter).

Copy-paste each block one at a time. Wait for each to finish before moving to the next.

---

## Step 1: Check what you already have

```bash
echo "=== Git ===" && git --version 2>/dev/null || echo "NOT INSTALLED"
echo "=== Python ===" && python3 --version 2>/dev/null || echo "NOT INSTALLED"
echo "=== Node ===" && node --version 2>/dev/null || echo "NOT INSTALLED"
echo "=== Homebrew ===" && brew --version 2>/dev/null || echo "NOT INSTALLED"
echo "=== VS Code ===" && code --version 2>/dev/null || echo "NOT INSTALLED"
```

**Write down which ones say "NOT INSTALLED"** — you only need to install those.

---

## Step 2: Install Homebrew (Mac's package manager)

Skip if Step 1 showed Homebrew is already installed.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

It will ask for your Mac password (you won't see characters as you type — that's normal). It may take 5-10 minutes.

**If you have an Apple Silicon Mac (M1/M2/M3/M4)**, run this after Homebrew installs:
```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

**Verify it worked:**
```bash
brew --version
```

---

## Step 3: Install Git, Python, Node

```bash
brew install git python@3.12 node
```

**Verify:**
```bash
git --version && python3 --version && node --version
```

---

## Step 4: Configure Git with your identity

```bash
git config --global user.name "esteves-pixel"
git config --global user.email "YOUR_EMAIL@example.com"
```

Replace `YOUR_EMAIL@example.com` with the email you use on GitHub.

---

## Step 5: Install VS Code

```bash
brew install --cask visual-studio-code
```

**Verify:** press `Cmd + Space`, type `Visual Studio Code`, it should appear.

---

## Step 6: Create your Projects folder and clone the repo

```bash
mkdir -p ~/Projects
cd ~/Projects
git clone https://github.com/esteves-pixel/SD4ALL-AI-Lab.git
cd SD4ALL-AI-Lab
```

**Verify — you should see your project files:**
```bash
ls -la
```

Expected output includes: `CLAUDE.md`, `README.md`, `bpm/`, `data/`, `agents/`, `docs/`, `notebooks/`

---

## Step 7: Open the project in VS Code

```bash
code ~/Projects/SD4ALL-AI-Lab
```

This opens VS Code with your entire project. You can now browse and edit any file.

---

## Step 8: Install Claude Code CLI (optional but recommended)

This lets you run Claude directly from your Mac Terminal, connected to your repo.

```bash
npm install -g @anthropic-ai/claude-code
```

**To use it:**
```bash
cd ~/Projects/SD4ALL-AI-Lab
claude
```

---

## Step 9: Install recommended VS Code extensions

Open VS Code, then press `Cmd + Shift + X` (Extensions panel) and install:

1. **Markdown All in One** — better markdown editing
2. **GitLens** — see Git history inline
3. **Python** — Python support
4. **Jupyter** — notebook support

Or install from Terminal:
```bash
code --install-extension yzhang.markdown-all-in-one
code --install-extension eamodio.gitlens
code --install-extension ms-python.python
code --install-extension ms-toolsai.jupyter
```

---

## You're Done! Verify Everything

Run this final check:

```bash
echo "=== SETUP VERIFICATION ==="
echo "Git:      $(git --version)"
echo "Python:   $(python3 --version)"
echo "Node:     $(node --version)"
echo "Homebrew: $(brew --version | head -1)"
echo "VS Code:  $(code --version | head -1)"
echo "Repo:     $(cd ~/Projects/SD4ALL-AI-Lab && git remote -v | head -1)"
echo "=== ALL DONE ==="
```

---

## What to Do Next

1. Open VS Code: `code ~/Projects/SD4ALL-AI-Lab`
2. Open the file `bpm/layer0-strategic/strategic-goals.md`
3. Fill in your Mission, Vision, and Goals
4. Save, then in Terminal:
   ```bash
   cd ~/Projects/SD4ALL-AI-Lab
   git add . && git commit -m "Add strategic goals" && git push
   ```
5. Come back to Claude Code (web) and I'll see your changes after a `git pull`

---

## Troubleshooting

| Problem | Fix |
|---|---|
| `git clone` asks for password | Use a Personal Access Token (GitHub → Settings → Developer Settings → Tokens) or set up SSH keys |
| `brew: command not found` | Restart Terminal, or run the Apple Silicon path fix from Step 2 |
| `code: command not found` | Open VS Code manually, press `Cmd+Shift+P`, type "Shell Command: Install 'code' command" |
| `permission denied` | Prefix command with `sudo` (e.g., `sudo npm install -g @anthropic-ai/claude-code`) |
