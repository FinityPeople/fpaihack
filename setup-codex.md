# Setting Up OpenAI Codex (Web App + CLI)

[Codex](https://openai.com/codex) is OpenAI's coding agent. It comes in two flavors:

- **Codex Web App** — a browser-based interface at [chatgpt.com/codex](https://chatgpt.com/codex)
- **Codex CLI** — a terminal-based coding agent (similar to Claude Code, but from OpenAI)

---

## Prerequisites

- A **ChatGPT Plus, Pro, Business, Edu, or Enterprise** plan (Codex is included with these plans)
- For the CLI: **Node.js 18+** is required (see below for install instructions)

---

## Part 1 — Codex Web App

The web app is the easiest way to get started. No installation needed.

1. Go to [chatgpt.com/codex](https://chatgpt.com/codex).
2. Sign in with your OpenAI / ChatGPT account.
3. Connect a GitHub repository when prompted.
4. Send a coding task — Codex will read your code, make changes, and create a PR.

### What it can do

- Read and understand your GitHub repos
- Write code and open pull requests
- Run tests in a sandboxed environment
- You can also tag `@codex` in GitHub PR comments to invoke it directly

> **Tip:** Create a git checkpoint before each task so you can easily revert if needed.

---

## Part 2 — Codex CLI

The CLI runs locally in your terminal, similar to Claude Code.

### Step 1 — Make sure you have Node.js

Codex CLI requires **Node.js 18 or later**.

Check if you already have it:

```bash
node --version
```

If you see `v18.x.x` or higher, you're good — skip to Step 2.

If not, install Node.js:

**Mac (Homebrew):**

```bash
brew install node
```

**Mac (without Homebrew):**

Download the installer from [nodejs.org](https://nodejs.org/) — pick the LTS version.

**Windows:**

```powershell
winget install OpenJS.NodeJS.LTS
```

Or download the installer from [nodejs.org](https://nodejs.org/) — pick the LTS version. **Make sure "Add to PATH" is checked during installation.**

After installing, close and reopen your terminal, then verify:

```bash
node --version
```

### Step 2 — Install Codex CLI

**Using npm (Mac, Windows, Linux):**

```bash
npm install -g @openai/codex
```

**Using Homebrew (Mac only):**

```bash
brew install codex
```

Verify it worked:

```bash
codex --version
```

### Step 3 — Sign in

Run:

```bash
codex
```

You'll be prompted to sign in. Choose **"Sign in with ChatGPT"** if you have a ChatGPT plan (recommended). You can also use an OpenAI API key if you prefer.

### Step 4 — Use it

Navigate to a project folder and start Codex:

```bash
cd my-project
codex
```

Then type natural language requests, just like you would with Claude Code.

---

## Windows notes

- Codex CLI works natively on Windows, but macOS and Linux are the most tested platforms.
- If you run into issues on Windows, consider using **WSL** (Windows Subsystem for Linux). Install WSL, then follow the Mac/Linux instructions inside your WSL terminal.
- Your Windows files are accessible inside WSL at `/mnt/c/`.

---

## Codex Desktop App

OpenAI also offers a Codex desktop app:

1. Go to [openai.com/codex](https://openai.com/codex) or the [OpenAI downloads page](https://developers.openai.com/codex/app).
2. Download the app for your platform (macOS Apple Silicon or Windows).
3. Install and sign in with your ChatGPT / OpenAI account.

---

## Troubleshooting

| Problem | Solution |
|---|---|
| `codex: command not found` | Close and reopen your terminal. Make sure npm's global bin folder is in your PATH. Run `npm config get prefix` to find it. |
| `npm: command not found` | You need Node.js installed first. See Step 1 above. |
| Node version too old | Run `node --version`. If below 18, update Node.js using the instructions in Step 1. |
| Sign-in fails | Make sure you have an active ChatGPT Plus, Pro, Business, Edu, or Enterprise plan. |
| Permission error with npm install | Don't use `sudo`. Instead, fix npm permissions: [npm docs](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally). |

---

## Docs and resources

- [Codex quickstart](https://developers.openai.com/codex/quickstart)
- [Codex CLI docs](https://developers.openai.com/codex/cli)
- [Codex CLI on GitHub](https://github.com/openai/codex)
- [Codex web app](https://chatgpt.com/codex)
- [Codex desktop app](https://developers.openai.com/codex/app)
