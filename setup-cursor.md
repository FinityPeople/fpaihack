# Setting Up Cursor (Editor + AI in One)

[Cursor](https://cursor.com) is a code editor (a fork of VS Code) with AI built directly into the editor. Unlike Claude Code or Codex, Cursor **bundles the editor and the AI subscription together** — you don't install a separate editor and you don't need a Claude or ChatGPT plan.

If you already use VS Code, Cursor will feel familiar: it supports the same keybindings and most of the same extensions.

---

## Prerequisites

- A **Cursor Pro** subscription ($20/mo) or higher. Sign up at [cursor.com/pricing](https://cursor.com/pricing).
- The free "Hobby" tier is for evaluation only — it won't have enough model quota for hackathon work.
- No separate Anthropic or OpenAI subscription is needed. Cursor's Pro plan includes access to frontier models (Claude, GPT, Gemini) out of the box.

---

## Part 1 — Install Cursor

Cursor ships as a GUI installer for Mac and Windows. **No terminal restart or PATH tweaking needed** — unlike the CLI-based tools (Claude Code, Codex).

### Mac

1. Go to [cursor.com/download](https://cursor.com/download).
2. Download the `.dmg` for your chip (Apple Silicon or Intel — the site auto-detects).
3. Open the `.dmg` and drag **Cursor** to your Applications folder.
4. Launch Cursor from Applications.

### Windows

1. Go to [cursor.com/download](https://cursor.com/download).
2. Download the `.exe` installer.
3. Run the installer and follow the prompts.
4. Launch Cursor from the Start menu.

---

## Part 2 — First run and sign-in

1. Launch Cursor.
2. Click the account icon (bottom-left corner) and choose one of:
   - **Email**
   - **Google**
   - **GitHub**
3. Your browser will open for OAuth. Complete the sign-in and you'll be redirected back to Cursor automatically.
4. Your plan tier shows next to the account icon once signed in.

> If sign-in fails, double-check your account has an active Pro (or higher) subscription at [cursor.com/pricing](https://cursor.com/pricing).

---

## Part 3 — Using Cursor

Cursor has four main AI features. Open a project folder (`File → Open Folder…` or drag it onto the Cursor icon) and try them:

| Feature | How to open | What it does |
|---|---|---|
| **Tab completion** | Just start typing | Inline AI autocomplete, multi-line and multi-edit |
| **Chat** | `Cmd+L` (Mac) / `Ctrl+L` (Win) | Ask questions about your code, get explanations |
| **Composer** | `Cmd+I` (Mac) / `Ctrl+I` (Win) | Multi-file edits — describe a change, review a diff |
| **Agent** | `Cmd+I` then toggle "Agent" | Autonomous multi-step tasks: reads files, runs commands, edits code |

More details and walkthroughs: [cursor.com/docs/agent/overview](https://cursor.com/docs/agent/overview).

---

## Part 4 — Optional: Cursor CLI commands

Cursor ships with two optional terminal commands. Most users don't need them, but they're handy.

### The `cursor` command — open a folder from the terminal

Like `code .` for VS Code. To install it:

1. In Cursor, press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Win).
2. Type "**Install 'cursor' command**" and run it.
3. Open a new terminal and try it:
   ```bash
   cursor ./my-project
   ```

### The `cursor-agent` CLI — agent in the terminal

A terminal-based AI agent, similar in spirit to `claude` or `codex`. Install:

**Mac / Linux:**

```bash
curl https://cursor.com/install -fsS | bash
```

**Windows (PowerShell):**

```powershell
irm 'https://cursor.com/install?win32=true' | iex
```

Close and reopen your terminal, then:

```bash
cursor-agent
```

Docs: [cursor.com/docs/cli/overview](https://cursor.com/docs/cli/overview).

---

## Part 5 — VS Code extensions work in Cursor

Because Cursor is a VS Code fork, most VS Code extensions work directly. Install them from the Extensions panel (`Cmd+Shift+X` / `Ctrl+Shift+X`).

Notably for this hackathon: the **Databricks** extension installs and runs in Cursor, giving you the same Databricks Connect / Asset Bundles integration you'd get in VS Code.

---

## Troubleshooting

| Problem | Solution |
|---|---|
| Sign-in fails or "no plan" error | Confirm your Cursor account has an active Pro subscription at [cursor.com/pricing](https://cursor.com/pricing). |
| `cursor: command not found` in terminal | In Cursor, run Command Palette → "Install 'cursor' command". |
| `cursor-agent: command not found` | Close and reopen your terminal after running the install script. |
| Databricks extension doesn't appear | Open the Extensions panel (`Cmd+Shift+X` / `Ctrl+Shift+X`) and search for "Databricks". Install the official one by Databricks. |
| Model quota exhausted mid-hackathon | Pro includes extended limits, but if you hit them you can upgrade to Pro+ ($60/mo, 3x quota) from your Cursor account settings. |

---

## Docs and resources

- [Cursor pricing](https://cursor.com/pricing)
- [Cursor download](https://cursor.com/download)
- [Installation guide](https://cursor.com/help/getting-started/install)
- [Agent overview](https://cursor.com/docs/agent/overview)
- [CLI overview](https://cursor.com/docs/cli/overview)
- [MCP setup](https://cursor.com/docs/mcp) — see also [`mcp-databricks-cursor.md`](mcp-databricks-cursor.md) in this repo

---

## Questions or problems?

Ping one of the mentors on Teams with:

- What you tried
- The exact error message (a screenshot helps)
