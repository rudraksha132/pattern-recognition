# Contributing to Pattern Recognition

Thanks for your interest in improving the `pattern-recognition` skill. This project is a single, prompt-shaped artifact plus a set of reference files — small in surface area, but the bar for analytical rigor is high. This guide explains how to propose changes, what we look for in reviews, and how to set up a local development workflow.

---

## Table of contents

- [Code of conduct](#code-of-conduct)
- [What this project is](#what-this-project-is)
- [What we welcome](#what-we-welcome)
- [What we are unlikely to accept](#what-we-are-unlikely-to-accept)
- [Reporting bugs](#reporting-bugs)
- [Suggesting a feature or new pattern](#suggesting-a-feature-or-new-pattern)
- [Improving documentation](#improving-documentation)
- [Submitting a pull request](#submitting-a-pull-request)
- [Local development](#local-development)
- [Style and content conventions](#style-and-content-conventions)
- [Review process](#review-process)
- [Becoming a maintainer](#becoming-a-maintainer)

---

## Code of conduct

By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing. Maintainers are expected to enforce it consistently.

---

## What this project is

`pattern-recognition` is an [Agent Skill](https://github.com/anthropics/skills) — a self-contained package of instructions and reference files that a coding assistant loads dynamically when its description matches the user's prompt. The artifact consists of:

- `SKILL.md` — the core protocol, loaded first.
- `references/` — deeper material pulled in on demand (genius thinking maps, pattern taxonomy, case studies).
- `README.md` — installation and usage documentation.

There is no compiled code, no test suite, and no runtime. "Correctness" here means the skill produces a *rigorously shaped* Pattern Report, not just a plausible one.

---

## What we welcome

- **Reference material improvements** — new entries in `pattern-taxonomy.md`, additional case studies in `failure-and-success-stories.md`, or new genius thinking maps.
- **Tightening the protocol** — clearer stage boundaries in `SKILL.md`, sharper definitions of *invariant* and *falsification condition*, better handling of edge cases (e.g., insufficient evidence, contradictory observations).
- **Documentation fixes** — installation steps that no longer match a current tool, broken anchors, typos, examples that mislead.
- **Examples and worked-through Pattern Reports** that illustrate the protocol on real or synthetic problems.
- **Compatibility notes** for new agents supported by the [`npx skills`](https://github.com/vercel-labs/skills) CLI.

## What we are unlikely to accept

- **Personality changes** to the output. The skill's value comes from its restraint. Requests like "make the report friendlier" or "add emojis to the final output" are out of scope.
- **Domain-specific forks** (e.g., a financial-only or medical-only variant). The skill is intentionally cross-domain; forks should live as separate skills.
- **Telemetry, network calls, or accounts.** The skill makes no network calls of its own. PRs that add them will be declined regardless of the rationale.
- **Unverified claims presented as established fact** in the reference material. If a Pattern Report entry doesn't have a falsification condition, it isn't a Pattern Report — it's a claim, and that distinction matters here.

If you're unsure whether a change fits, open an issue first. A 5-minute discussion saves a 5-day PR.

---

## Reporting bugs

Before opening a bug report, search [existing issues](https://github.com/rudraksha132/pattern-recognition/issues) to make sure it hasn't already been reported.

When you open a bug report, include:

1. **The skill version** — from the `version` field in `SKILL.md` frontmatter, or the commit SHA if you're on `main`.
2. **The agent you ran it in** — Claude Code, Cursor, Codex, Claude.ai, etc., with version where applicable.
3. **The prompt you used** — the exact text. A pattern-shaped question that triggered the skill incorrectly is more useful than a paraphrase.
4. **What you expected to see** — including which stage of the protocol you expected the response to follow.
5. **What you actually saw** — a full or partial response is fine. Quote the section you think is wrong and explain why.
6. **Why you think the skill is at fault**, not the underlying model. If you're not sure, say so — that framing changes what we investigate.

> [!TIP]
> **Reproducibility matters more than eloquence.** A bug report with one specific prompt, the exact model, and the exact wrong response is worth ten vague ones.

## Suggesting a feature or new pattern

For new pattern entries, additional reference material, or changes to the core protocol, open an issue first using the **Feature request** template. The issue should include:

- **The use case** — what kind of question should the skill be able to answer better?
- **A worked example** — a concrete prompt plus a sketch of the desired Pattern Report shape.
- **Where it lives** — does this belong in `SKILL.md` (a protocol change), in `references/pattern-taxonomy.md` (a new entry), or as a brand-new reference file?

We use the issue thread to align on scope before any code is written.

---

## Improving documentation

Small documentation fixes (typos, broken links, clearer sentences) are the easiest way to contribute and don't need an issue first. Open a PR directly against the relevant file. For larger restructuring — a new section in the README, a rewrite of an installation path — open an issue first so the change can be discussed before it's written.

---

## Submitting a pull request

### Before you open a PR

1. **Search for related issues and PRs.** If your change is non-trivial, link the issue it addresses.
2. **For new content**, make sure it follows the same shape as the surrounding material. A Pattern Report entry without a *falsification condition* is incomplete. A reference file without inline examples is harder to use than the existing ones.
3. **Read your own diff once for tone.** This skill is intentionally restrained. PRs that introduce marketing language, hype, or overconfident framing tend to get pushed back on.

### PR checklist

- [ ] The PR has a clear, specific title ("Add phase-transition case study to failure-and-success-stories.md", not "Updates").
- [ ] The PR description explains *why* the change is needed, not just *what* it does.
- [ ] All new content includes falsification conditions or an explicit note that the content is reference material, not a Pattern Report.
- [ ] The diff is minimal — no incidental reformatting of unchanged lines.
- [ ] Linked issues are referenced with `Fixes #123` or `Refs #123` in the PR body.
- [ ] Markdown renders correctly on GitHub — check headings, tables, and admonitions (the `> [!NOTE]` syntax this repo uses).

### Commit messages

- Use the imperative mood ("Add pattern taxonomy entry", not "Added" or "Adds").
- Keep the subject line under 72 characters.
- Reference the issue number in the body when applicable.

We do not enforce a specific commit-message convention (Conventional Commits, etc.) — but we may squash your commits on merge, so individual commit messages can be terse.

---

## Local development

Because the project is plain Markdown with YAML frontmatter, there is no build step. The "development loop" is:

1. **Edit the file** in your preferred editor.
2. **Read it back** to make sure the rendering is what you expect (GitHub's preview, or your editor's Markdown preview).
3. **Test it in your target agent.** For Claude Code, point the skill at your local clone:

   ```bash
   git clone https://github.com/rudraksha132/pattern-recognition.git ~/.claude/skills/pattern-recognition
   ```

   Edit in place, restart the agent, and run a pattern-shaped prompt. The agent should pick up the changes immediately.

4. **For protocol changes**, run a small set of test prompts and compare the resulting Pattern Reports against the expected shape:

   - Does the output include an *invariant core* and a *generator rule*?
   - Does it state a falsification condition?
   - Does it list open questions when the evidence is incomplete?

### Optional tooling

- A Markdown linter (e.g., `markdownlint-cli`) is welcome but not required.
- A spell-checker on changed files. CI does not run one; please self-check.
- For the `npx skills` test path, you can run `npx skills add <your-fork> -a claude-code` to install from a branch before opening a PR.

---

## Style and content conventions

These conventions are enforced through review rather than tooling, but please read them before opening a PR.

### Voice

- **Direct, not promotional.** The skill is described in the README, not in `SKILL.md`. The protocol itself should be operational.
- **Hedged where the evidence is hedged.** If a reference entry is a hypothesis, say so. If it's an established result, that's also worth saying.
- **No first-person plural ("we", "us")** in `SKILL.md`. The protocol is what the assistant does, not what a team does.

### Pattern Reports

Every Pattern Report example in the documentation, and every new entry in `pattern-taxonomy.md`, should have:

| Section | Required? | Notes |
|---|---|---|
| Name | Yes | A short label that captures the generator rule. |
| Observed in | Yes | The domains or systems where the pattern has been seen. |
| Invariant core | Yes | What stays constant as context changes. |
| Generator rule | Yes | The mechanism that produces the pattern. |
| Prediction | Yes | What we'd expect to see if the rule is right. |
| Falsification conditions | Yes | What evidence would disprove it. |
| Open questions | Encouraged | What's still unresolved. |

If any of these are missing in a new entry, call it out in the PR description and explain why.

### Markdown style

- ATX headings (`##`, `###`).
- One sentence per line in long paragraphs — makes diffs cleaner.
- Code blocks fenced with triple backticks and an explicit language where possible.
- Admonitions use the GitHub syntax: `> [!NOTE]`, `> [!TIP]`, `> [!IMPORTANT]`, `> [!WARNING]`, `> [!CAUTION]`.
- Tables for any structured comparison of three or more items.

### File layout

- New reference material lives in `references/`.
- New skill variants (for example, a domain-specific version) should be a separate skill, not a subfolder here.
- If you're adding a new top-level file, justify it in the PR description. The repo intentionally stays small.

---

## Review process

1. **A maintainer will respond within 7 days** of opening a PR. If we can't review in that window, we'll tell you when we can.
2. **Reviews are specific.** If we ask for changes, we'll point at the section, not the file. Push back if a comment doesn't make sense to you.
3. **Two approvals are required** for changes to `SKILL.md`. One is enough for documentation and reference changes.
4. **Squash-merge is the default.** Your PR is what gets recorded; the individual commits are not.
5. **Stale PRs** (no activity for 30 days) may be closed. Reopen when you're ready to continue.

---

## Becoming a maintainer

Maintainers are added by existing maintainers, on the basis of sustained, high-quality contributions. There is no formal application process. If you find yourself regularly proposing, reviewing, and merging improvements, ask — we'd like to make it official.

---

## Recognition

Contributors are listed in the release notes when their PR is merged. Significant contributions (a new reference file, a sustained pattern of improvements) are noted in the README's Attribution section.

Thanks for taking the time to make this project more rigorous.
