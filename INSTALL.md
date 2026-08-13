# Install STE-AI

Review [`SKILL.md`](skills/ste-ai/SKILL.md) before installation. STE-AI contains no executable code, hooks, or network access.

## GitHub CLI

The GitHub CLI installs Agent Skills for many coding agents.

Preview STE-AI:

```bash
gh skill preview SeanLikesData/ste-ai ste-ai
```

Use the command for your agent:

| Agent | Install for all projects |
| --- | --- |
| Claude Code | `gh skill install SeanLikesData/ste-ai ste-ai --agent claude-code --scope user` |
| Codex | `gh skill install SeanLikesData/ste-ai ste-ai --agent codex --scope user` |
| Cursor | `gh skill install SeanLikesData/ste-ai ste-ai --agent cursor --scope user` |
| Gemini CLI | `gh skill install SeanLikesData/ste-ai ste-ai --agent gemini-cli --scope user` |
| GitHub Copilot | `gh skill install SeanLikesData/ste-ai ste-ai --agent github-copilot --scope user` |
| Pi | `gh skill install SeanLikesData/ste-ai ste-ai --agent pi --scope user` |

Replace `--scope user` with `--scope project` for the current project only.

List installed skills:

```bash
gh skill list
```

Update STE-AI:

```bash
gh skill update ste-ai
```

## Cross-agent installer

The open [`skills` CLI](https://github.com/vercel-labs/skills) supports many additional agents.

```bash
npx skills@latest add SeanLikesData/ste-ai --skill ste-ai
```

The installer detects available agents and asks where to install STE-AI. The current installer requires Node.js 22.20 or newer.

Install STE-AI globally for one agent:

```bash
npx skills@latest add SeanLikesData/ste-ai --skill ste-ai --agent claude-code --global
```

Replace `claude-code` with the applicable agent value. Examples include `codex`, `cursor`, `gemini-cli`, `github-copilot`, and `pi`.

Update or remove STE-AI:

```bash
npx skills@latest update ste-ai
npx skills@latest remove ste-ai
```

## Pi

Install the GitHub repository as a native Pi package:

```bash
pi install https://github.com/SeanLikesData/ste-ai
```

Start a new Pi session. Invoke STE-AI directly when needed:

```text
/skill:ste-ai
```

Update or remove the package:

```bash
pi update https://github.com/SeanLikesData/ste-ai
pi remove https://github.com/SeanLikesData/ste-ai
```

The npm command will become available after the first npm release:

```bash
pi install npm:ste-ai
```

## Claude Code

Install with the GitHub CLI:

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent claude-code --scope user
```

Restart Claude Code. Claude can load STE-AI when a writing task matches its description.

Invoke it directly:

```text
/ste-ai
```

## Codex

Install with the GitHub CLI:

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent codex --scope user
```

Restart Codex if the skill does not appear automatically.

Select it directly:

```text
$ste-ai
```

## Cursor

Install with the GitHub CLI:

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent cursor --scope user
```

Restart Cursor. Open **Customize**, then **Skills**, to confirm that STE-AI appears.

Invoke it directly:

```text
/ste-ai
```

Cursor also supports installation from GitHub through **Customize → Rules → Add Rule → Remote Rule (GitHub)**.

## Gemini CLI

Install with the GitHub CLI:

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent gemini-cli --scope user
```

Gemini CLI also supports direct Git installation:

```bash
gemini skills install https://github.com/SeanLikesData/ste-ai.git --path skills/ste-ai --consent
```

List installed skills:

```bash
gemini skills list --all
```

## GitHub Copilot

Install with the GitHub CLI:

```bash
gh skill install SeanLikesData/ste-ai ste-ai --agent github-copilot --scope user
```

Restart the agent session. Use `/skills` to confirm that STE-AI appears.

## Manual installation

Copy [`skills/ste-ai`](skills/ste-ai) into the user skill directory for your agent.

| Agent | Directory |
| --- | --- |
| Claude Code | `~/.claude/skills/ste-ai/` |
| Codex | `~/.codex/skills/ste-ai/` |
| Cursor | `~/.cursor/skills/ste-ai/` |
| Gemini CLI | `~/.gemini/skills/ste-ai/` |
| GitHub Copilot | `~/.copilot/skills/ste-ai/` |
| Pi | `~/.pi/agent/skills/ste-ai/` |

Restart the agent after a manual installation.
