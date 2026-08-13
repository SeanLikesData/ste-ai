# How to install

Review [`SKILL.md`](skills/ste-ai/SKILL.md) before installation. STE-AI contains no executable code, hooks, or network access.

<details>
<summary><strong>Claude Code</strong></summary>

### Install

```bash
claude plugin marketplace add SeanLikesData/ste-ai
claude plugin install ste-ai@ste-ai
```

### Verify

```bash
claude plugin list
```

### Use

Restart Claude Code. Claude can load STE-AI when a writing task matches its description.

Invoke the plugin skill directly:

```text
/ste-ai:ste-ai
```

### Update

```bash
claude plugin marketplace update ste-ai
claude plugin update ste-ai@ste-ai
```

### Uninstall

```bash
claude plugin uninstall ste-ai@ste-ai
claude plugin marketplace remove ste-ai
```

Install the plain Agent Skill instead of the plugin:

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent claude-code --scope user
```

</details>

<details>
<summary><strong>Codex</strong></summary>

### Install

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent codex --scope user
```

### Verify

```bash
gh skill list --agent codex --scope user
```

### Use

Restart Codex if the skill does not appear automatically.

Select it directly:

```text
$ste-ai
```

### Update

```bash
gh skill update ste-ai
```

</details>

<details>
<summary><strong>Cursor</strong></summary>

### Install

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent cursor --scope user
```

Cursor also supports installation through **Customize → Rules → Add Rule → Remote Rule (GitHub)**.

### Verify

Restart Cursor. Open **Customize**, then **Skills**, and confirm that STE-AI appears.

### Use

```text
/ste-ai
```

### Update

```bash
gh skill update ste-ai
```

</details>

<details>
<summary><strong>Gemini CLI</strong></summary>

### Install

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent gemini-cli --scope user
```

Gemini CLI also supports direct Git installation:

```bash
gemini skills install https://github.com/SeanLikesData/ste-ai.git --path skills/ste-ai --consent
```

### Verify

```bash
gemini skills list --all
```

### Update

For a GitHub CLI installation:

```bash
gh skill update ste-ai
```

</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

### Install

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent github-copilot --scope user
```

### Verify

Restart the agent session. Use `/skills` and confirm that STE-AI appears.

### Update

```bash
gh skill update ste-ai
```

</details>

<details>
<summary><strong>Pi</strong></summary>

Pi discovers this repository as a native package.

### Install

```bash
pi install https://github.com/SeanLikesData/ste-ai
```

### Verify

```bash
pi list
```

Start a new Pi session. Invoke STE-AI directly:

```text
/skill:ste-ai
```

### Update

```bash
pi update https://github.com/SeanLikesData/ste-ai
```

### Uninstall

```bash
pi remove https://github.com/SeanLikesData/ste-ai
```

The npm command will become available after the first npm release:

```bash
pi install npm:ste-ai
```

</details>

<details>
<summary><strong>Other Agent Skills clients</strong></summary>

The open [`skills` CLI](https://github.com/vercel-labs/skills) supports many additional agents.

### Install

```bash
npx skills@latest add SeanLikesData/ste-ai --skill ste-ai
```

The installer detects available agents and asks where to install STE-AI. The current installer requires Node.js 22.20 or newer.

Install STE-AI globally for one agent:

```bash
npx skills@latest add SeanLikesData/ste-ai --skill ste-ai --agent claude-code --global
```

Replace `claude-code` with the applicable agent value.

### Verify

```bash
npx skills@latest list --global
```

### Update

```bash
npx skills@latest update ste-ai
```

### Uninstall

```bash
npx skills@latest remove --global ste-ai
```

</details>

<details>
<summary><strong>Manual installation</strong></summary>

Copy [`skills/ste-ai`](skills/ste-ai) into the user skill directory for your agent.

| Agent | Directory |
| --- | --- |
| Claude Code | `~/.claude/skills/ste-ai/` |
| Codex | `~/.codex/skills/ste-ai/` |
| Cursor | `~/.cursor/skills/ste-ai/` |
| Gemini CLI | `~/.gemini/skills/ste-ai/` |
| GitHub Copilot | `~/.copilot/skills/ste-ai/` |
| Pi | `~/.pi/agent/skills/ste-ai/` |

Restart the agent after installation.

</details>

## Preview before installation

Use the GitHub CLI to inspect the skill:

```bash
gh skill preview SeanLikesData/ste-ai ste-ai
```

Use `--scope project` instead of `--scope user` in GitHub CLI commands for the current project only.
