# Setting Up Claude (Desktop App + Claude Code CLI)

This guide covers two tools from Anthropic:

- **Claude Desktop** — a desktop app for chatting with Claude (like ChatGPT but from Anthropic)
- **Claude Code** — a command-line coding agent that lives in your terminal and can read, write, and run code

You can use either or both depending on your workflow.

---

## Prerequisites

- An **Anthropic account** with a Claude Pro, Max, Teams, or Enterprise plan. The free plan does not include Claude Code access.
- For Claude Code on Windows: [Git for Windows](https://git-scm.com/downloads/win) must be installed first (not needed on Mac or if using WSL).

---

## Part 1 — Claude Desktop App

The desktop app gives you a chat interface for talking with Claude. It also supports desktop extensions that can access your local files and tools.

### Install

1. Go to [claude.com/download](https://claude.com/download).
2. Download the installer for your platform (Mac or Windows).
3. Run the installer.
   - **Mac:** Open the `.dmg` file and drag Claude to your Applications folder.
   - **Windows:** Run the `.msix` installer and follow the prompts.
4. Launch Claude from your Applications folder (Mac) or Start menu (Windows).
5. Sign in with your Anthropic account.

That's it — you're ready to chat.

### Docs

- [Claude Desktop help center](https://support.claude.com/en/collections/16163169-claude-desktop)

---

## Part 2 — Claude Code (terminal agent)

Claude Code is a coding agent that runs in your terminal. It can understand your codebase, edit files, run commands, and work with git — all through natural language.

### Install on Mac / Linux

Open **Terminal** and run:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Or with Homebrew:

```bash
brew install --cask claude-code
```

### Install on Windows

**Option A: PowerShell (recommended)**

Open **PowerShell** and run:

```powershell
irm https://claude.ai/install.ps1 | iex
```

**Option B: CMD**

Open **Command Prompt** and run:

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

**Option C: winget**

```powershell
winget install Anthropic.ClaudeCode
```

> Remember: Windows native setups require [Git for Windows](https://git-scm.com/downloads/win). Install it first if you don't have it. If you're using WSL, you don't need Git for Windows — just use the Mac/Linux install command inside WSL.

### Verify installation

```bash
claude --version
```

You should see a version number. If you get an error, try closing and reopening your terminal.

### First run

1. Open your terminal and navigate to a project folder:
   ```bash
   cd my-project
   ```
2. Start Claude Code:
   ```bash
   claude
   ```
3. A browser window will open asking you to sign in. Complete the sign-in.
4. You're ready. Type natural language requests like:
   - "Explain what this project does"
   - "Find all files that handle authentication"
   - "Write a function that parses CSV files"
   - "Run the tests and fix any failures"

### Update

Native installations auto-update in the background. You can also force an update:

```bash
claude update
```

For Homebrew: `brew upgrade claude-code`
For winget: `winget upgrade Anthropic.ClaudeCode`

---

## Tips for beginners

- **Claude Desktop** is great for brainstorming, asking questions, and getting explanations.
- **Claude Code** is great for hands-on coding — it can read your files, make changes, and run commands directly.
- You can use both at the same time. They use the same Anthropic account.
- Claude Code works best when you start it from inside a project folder so it has context about your code.

---

## Troubleshooting

| Problem | Solution |
|---|---|
| `claude: command not found` | Close and reopen your terminal. If still not working, check that `~/.local/bin` is in your PATH. |
| Browser sign-in doesn't open | Copy the URL from the terminal output and paste it into your browser manually. |
| "You don't have access" | Make sure your Anthropic account has a Pro, Max, Teams, or Enterprise plan. The free plan doesn't include Claude Code. |
| Windows: `'irm' is not recognized` | You're in CMD, not PowerShell. Use the CMD install command instead. |
| Windows: `The token '&&' is not a valid statement separator` | You're in PowerShell, not CMD. Use the PowerShell install command instead. |

---

## Docs and resources

- [Claude Code documentation](https://code.claude.com/docs/en/setup)
- [Claude Code on GitHub](https://github.com/anthropics/claude-code)
- [Claude Desktop help center](https://support.claude.com/en/collections/16163169-claude-desktop)
- [Claude Desktop download](https://claude.com/download)
