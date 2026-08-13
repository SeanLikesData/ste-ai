<div align="center">

# Structured Technical English for AI

**Clear, consistent, low-cognitive-load writing for AI conversations and documents.**

[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-compatible-111827)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![No executable code](https://img.shields.io/badge/executable%20code-none-16a34a)](skills/ste-ai/SKILL.md)

</div>

STE-AI gives AI agents one reusable writing standard. It keeps answers direct, preserves decision-critical detail, and makes long-lived instruction files easier to maintain.

## Install

[Installation instructions for Pi, Claude Code, Codex, Cursor, Gemini CLI, GitHub Copilot, and other Agent Skills clients](INSTALL.md)

## See the difference

<table>
<tr>
<th width="50%">Typical AI writing</th>
<th width="50%">With STE-AI</th>
</tr>
<tr>
<td valign="top">

> Great question. There are several factors that could potentially influence this decision. It is worth noting that the current migration plan appears to have some gaps. You may want to consider creating a rollback procedure before moving forward. This would help ensure a more robust and seamless migration process.

</td>
<td valign="top">

> Delay the migration until the rollback procedure is tested.
>
> The current plan has no verified recovery path. A failed migration could extend the outage.
>
> Next: test the rollback procedure in staging.

</td>
</tr>
</table>

STE-AI applies the same rules to reports, plans, summaries, and agent instructions such as `SKILL.md` and `AGENTS.md`.

## Use

Agents can load STE-AI automatically when a writing task matches its description. Most clients also support direct selection.

| Agent | Direct use |
| --- | --- |
| Claude Code | `/ste-ai` |
| Codex | `$ste-ai` |
| Cursor | `/ste-ai` |
| Pi | `/skill:ste-ai` |

You can also ask for it by name:

```text
Use STE-AI to rewrite this report without removing evidence or caveats.
```

## What it changes

- Leads with the answer, result, recommendation, or next action.
- Uses short sentences, active voice, and common words.
- Preserves risks, caveats, evidence, and decision-critical alternatives.
- Separates verified facts from inference.
- Removes filler, decorative language, and unnecessary recaps.

The complete specification is in [`SKILL.md`](skills/ste-ai/SKILL.md).

## Why structured AI writing matters

AI-authored instructions can remain active for months or years. Their wording affects every person and agent that reads them.

Stable terms make those instructions easier to review, compare, revise, and transfer between agents. Explicit scope and sentence rules reduce interpretation differences during maintenance.

STE-AI contains one Markdown skill file. It has no scripts, hooks, network access, or runtime dependencies.

## Inspiration from ASD-STE100

ASD-STE100 Simplified Technical English is a controlled natural language and international standard for technical documentation.

The European aerospace industry began developing it in the late 1970s. The original goal was clearer English-language maintenance documentation. Its use expanded from commercial aviation into defense projects and other technical fields.

ASD-STE100 combines writing rules with a controlled dictionary. These controls reduce ambiguity across languages and organizations.

STE-AI applies the general principle of shared writing constraints to AI communication. It does not reproduce the ASD-STE100 controlled dictionary.

STE-AI is independent. It is not ASD-STE100, an ASD-STE100 implementation, or a conformance checker. It is not affiliated with ASD or its STE Maintenance Group.

Official references:

- [ASD-STE100 overview](https://www.asd-ste100.org/about_STE.html)
- [ASD Simplified Technical English](https://www.asd-europe.org/standards-specifications/simplified-technical-english/)
- [STE fundamentals](https://www.asd-europe.org/standards-specifications/simplified-technical-english/what-are-the-basics-of-simplified-technical-english/)

Simplified Technical English and ASD-STE100 are trademarks of ASD, Brussels, Belgium.

## Package contents

```text
skills/
└── ste-ai/
    └── SKILL.md
```

## Development

Validate the skill with the Agent Skills reference tool:

```bash
uvx --from 'git+https://github.com/agentskills/agentskills#subdirectory=skills-ref' \
  skills-ref validate ./skills/ste-ai
```

Inspect the npm archive without publishing:

```bash
npm run check
```

## Inspiration

STE-AI draws from two sources:

- [ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/) showed how shared writing constraints improve technical communication.
- The [I Have ADHD](https://github.com/ayghri/i-have-adhd) skill demonstrated effective low-cognitive-load rules and cross-agent skill distribution.

## License

[MIT](LICENSE)
