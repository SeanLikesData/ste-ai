# Structured Technical English for AI (STE-AI)

STE-AI is a writing specification for clear, consistent, low-cognitive-load AI communication.

It standardizes how AI explains ideas, answers questions, and writes durable instruction files.

## Why STE-AI exists

AI produces conversational replies and documents that people and other agents must understand.

Without shared writing rules, that output can become inconsistent, indirect, repetitive, or difficult to maintain.

STE-AI provides one reusable style for:

- Conversations between people and AI agents.
- Summaries, reports, plans, and explanations.
- Agent instructions such as `SKILL.md` and `AGENTS.md` files.
- Documentation that multiple people or agents maintain over time.
- Prose that must support quick and accurate action.

## Inspiration from ASD-STE100

ASD-STE100 Simplified Technical English is a controlled natural language and international standard for technical documentation.

The European aerospace industry began developing it in the late 1970s. Its original goal was clearer English-language maintenance documentation.

Its use began in commercial aviation and later expanded into defense projects. The standard combines writing rules with a controlled dictionary.

These controls reduce ambiguity and make technical instructions easier to understand across languages and organizations.

STE-AI applies the same general idea to AI communication: shared constraints can produce clearer and more consistent writing.

STE-AI is an independent specification. It is not ASD-STE100, an implementation of ASD-STE100, or a conformance checker.

STE-AI does not reproduce the ASD-STE100 controlled dictionary. It is not affiliated with ASD or its STE Maintenance Group.

## What STE-AI changes

- Leads with the answer, result, recommendation, or next action.
- Uses short sentences, active voice, and common words.
- Limits justification while preserving decision-changing risks.
- Separates verified facts from inference.
- Removes filler, decorative language, and unnecessary recaps.

## Why structured AI writing matters

AI-authored instruction files can remain active for months or years. Their wording affects every agent that reads them.

Stable terms make those instructions easier to review, compare, revise, and transfer between agents.

Explicit scope and sentence rules also reduce interpretation differences. This consistency supports long-term maintenance of files such as `SKILL.md`.

## Install in Pi

After the npm release, install the package globally:

```bash
pi install npm:ste-ai
```

Install the current GitHub version before the npm release:

```bash
pi install https://github.com/SeanLikesData/ste-ai
```

Start a new Pi session after installation.

Pi can load the skill when a writing task matches its description. Invoke it directly when you need certainty:

```text
/skill:ste-ai
```

## Use with other agents

The skill follows the Agent Skills directory format. Compatible agents can load `skills/ste-ai/SKILL.md` directly.

Copy the `skills/ste-ai` directory into a skill location supported by your agent.

## Scope

The specification applies to replies, documents, summaries, reports, plans, explanations, and AI instruction files.

It does not override requested styles. It also exempts code, commit messages, transcripts, and verbatim quotes.

## Design

The specification uses four layers:

1. Turn structure controls answer order and list size.
2. Calibration controls detail, uncertainty, and recommendations.
3. Sentence rules control length, voice, tense, and ambiguity.
4. Vocabulary rules prefer common, stable, and direct terms.

## Package contents

```text
skills/
└── ste-ai/
    └── SKILL.md
```

The package contains no executable extension and no runtime dependency.

## Develop

Inspect the npm archive without publishing:

```bash
npm run check
```

Load the local package in a temporary Pi session:

```bash
pi -e .
```

## Sources and attribution

- [ASD-STE100 official overview](https://www.asd-ste100.org/about_STE.html)
- [ASD overview of Simplified Technical English](https://www.asd-europe.org/standards-specifications/simplified-technical-english/)
- [ASD explanation of STE fundamentals](https://www.asd-europe.org/standards-specifications/simplified-technical-english/what-are-the-basics-of-simplified-technical-english/)

Simplified Technical English and ASD-STE100 are trademarks of ASD, Brussels, Belgium.

## License

MIT
