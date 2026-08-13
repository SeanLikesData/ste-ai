<div align="center">

<img src="ste-ai-logo.png" alt="STE-AI owl logo" width="180">

# Structured Technical English for AI

**Clear, consistent, low-cognitive-load writing for AI conversations and documents.**

[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-compatible-111827)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

</div>

STE-AI stops AI from burying the answer. It gives agents specific rules for direct replies and maintainable documents.

## Install

🔗 [Installation Instructions](INSTALL.md)

## See the difference

<table>
<tr>
<th width="50%">Typical AI writing</th>
<th width="50%">With STE-AI</th>
</tr>
<tr>
<td valign="top">

> Great question. At its core, this is not just a deployment decision. The payment-retry path is load-bearing, so a failure there could increase the blast radius. The good news is that 214 tests passed and staging checkout works, which suggests the update is in relatively strong shape.
>
> That said, the failed test may be the smoking gun. An untested rollback is also a potential footgun. A belt-and-suspenders approach would add an Initial Verification gate, or IV, before deployment. Ultimately, this will create a robust and seamless release process without unnecessary yak shaving.

</td>
<td valign="top">

> Do not deploy today.
>
> The payment-retry test failed.
>
> The team has not tested rollback.
>
> However, 214 tests passed, and checkout works in staging.
>
> Next:
>
> 1. Fix the payment-retry test.
> 2. Test rollback in staging.

</td>
</tr>
</table>

### Agent instructions

<table>
<tr>
<th width="50%">Typical AI-authored <code>AGENTS.md</code></th>
<th width="50%">With STE-AI</th>
</tr>
<tr>
<td valign="top">

> ## Testing
>
> Testing is the load-bearing gate in the delivery spine. When making changes, run the relevant tests to reduce the blast radius and avoid hidden footguns at integration seams. Where appropriate, add belt-and-suspenders coverage for behavior that crosses the validation substrate. Record Initial Verification as IV so agents can track it consistently. Avoid unnecessary yak shaving, but do not mark work complete until you are reasonably confident that everything functions correctly.

</td>
<td valign="top">

> ## Testing
>
> 1. Run the tests that cover each changed behavior.
> 2. Add a test when no current test covers the new behavior.
> 3. Do not mark the task complete while a related test fails.
> 4. Report each failing test and its cause.

</td>
</tr>
</table>

The second version gives each agent the same completion criteria. It removes judgment calls such as “where appropriate” and “reasonably confident.”

## The rules

### Response rules

1. Lead with the answer, result, recommendation, or next action.
2. Keep lists to five items. Rank or split longer lists.
3. Give no more than two reasons for a recommendation unless the user asks for more.
4. Preserve every risk, caveat, and alternative that can change the decision.
5. Name the specific evidence state, such as `failed`, `untested`, `unknown`, or `assumed`.

### Language rules

1. Keep sentences to 20 words or fewer. Put one idea in each sentence.
2. Use active voice and the present tense. Use imperative verbs for instructions.
3. Use one stable term for each concept. Define technical terms when they first appear.
4. Use known numbers instead of vague quantities such as “some” or “several.”
5. Remove filler, decorative claims, repeated recaps, and closing invitations.

The complete specification is in [`SKILL.md`](skills/ste-ai/SKILL.md).

## Why this matters

AI instructions work more consistently across models when they use stable terms and explicit rules. This also makes `SKILL.md`, `AGENTS.md`, and related files easier to maintain.

## Inspiration

### ASD-STE100

[ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/) is an international standard for controlled technical writing. Aerospace teams developed it to make maintenance documents easier to understand across languages and organizations.

STE-AI adapts the principle of shared writing constraints for AI communication. It does not reproduce the ASD-STE100 dictionary or claim ASD-STE100 compliance.

STE-AI is independent and is not affiliated with ASD or its STE Maintenance Group. Simplified Technical English and ASD-STE100 are trademarks of ASD, Brussels, Belgium.

### I Have ADHD

The [I Have ADHD](https://github.com/ayghri/i-have-adhd) skill influenced STE-AI’s low-cognitive-load rules and cross-agent distribution format.

## License

[MIT](LICENSE)
