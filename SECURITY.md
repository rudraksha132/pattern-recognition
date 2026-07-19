# Security Policy

## About this project

`pattern-recognition` is an [Agent Skill](https://github.com/anthropics/skills) — a package of Markdown instructions and reference files that a coding assistant loads dynamically. It contains **no executable code, no scripts, and no network calls of its own**. The attack surface is therefore narrow, but the model in which it runs is shared with whatever the user pastes in, which is worth being explicit about.

---

## Supported versions

| Version | Supported |
|---|---|
| The latest tagged release (currently `1.0.0`) | ✅ Yes |
| `main` branch, at the most recent commit | ✅ Yes |
| Any older release | ❌ No — please upgrade |

The skill is small enough that backporting is rarely useful. If you find a security-relevant issue in an older release, the fix will land on `main` and ship in the next release.

---

## Reporting a vulnerability

**Please do not file a public issue for security problems.** Use one of the private channels below instead.

### Preferred: GitHub private vulnerability reporting

Use [GitHub's private vulnerability reporting](https://github.com/rudraksha132/pattern-recognition/security/advisories/new) on this repository. This is the fastest way to reach the maintainer team and keeps the report out of the public issue tracker.

### Alternative: email

If you can't or don't want to use GitHub's reporting flow, email **rudraksha132@gmail.com** with the subject line starting with `[security]`.

### What to include

To help us triage quickly, please include:

1. **A clear description of the issue** — what the concern is and how it could be triggered.
2. **Steps to reproduce** — ideally a specific prompt and agent configuration that would surface the problem.
3. **The version affected** — the `version` field in `SKILL.md` frontmatter, or the commit SHA.
4. **Your assessment of impact** — what an attacker could achieve, and under what conditions. If you're not sure, say so.
5. **Whether you want public credit** when the issue is disclosed.

You do not need to include a fix. A clean repro and a clear description are enough.

---

## What to expect

| Stage | Target time |
|---|---|
| Acknowledgement of the report | Within **3 business days** |
| Initial assessment (confirmed, declined, or needs more info) | Within **7 days** |
| Fix in a release or a public advisory | As soon as a fix is verified |

We will keep you informed if the timeline changes. If you haven't heard back within a week, please follow up on the same channel — the email may have been filtered, and we'd rather hear from you twice than miss a real report.

---

## Scope

Because the project is pure Markdown with YAML frontmatter, the realistic security concerns are limited to:

- **Prompt-injection content in the reference material.** A reference file that includes instructions to override the assistant's behavior, exfiltrate data, or change the protocol would be in scope. Report it.
- **Malicious examples in documentation.** Worked examples that ask the model to generate harmful content, or that demonstrate a "Pattern Report" whose only point is to launder a bad claim as a structured output, are in scope.
- **Frontmatter manipulation.** The `description` field is consumed by the agent's skill-matching logic. Content there that changes the activation behavior beyond what the README documents is in scope.
- **Build / install pipeline issues.** The repo is plain text, but `npx skills` and any other tooling that fetches and installs the package are part of the trust boundary. Concerns about *that* path should go to the upstream tooling, but tell us too if it affects this package.

Out of scope:

- Behavior of the underlying model or agent. If the model produces a poor Pattern Report for a sensitive topic, that's a model issue, not a skill issue — file it with the model provider.
- Output quality concerns that are not security-relevant. Use the issue tracker for those.

---

## Disclosure policy

We follow a **coordinated disclosure** process:

1. We will work with you to confirm the issue and agree on a fix.
2. We will prepare a fix and, where appropriate, a public advisory describing the issue at a high level.
3. We will release the fix and the advisory together.
4. We will credit you in the advisory if you asked for credit and it's safe to do so.

Please give us a reasonable window to address the issue before publishing details. In most cases this will be **30 days**; complex cases may take longer and we will negotiate the timeline with you.

---

## Past advisories

None at this time. When an advisory is published, it will appear in [GitHub Security Advisories](https://github.com/rudraksha132/pattern-recognition/security/advisories) and be noted in the `CHANGELOG.md`.

---

## Acknowledgements

Thanks to the people who report issues responsibly. The skill is small, but the trust placed in shared prompt files is real, and the people who flag problems before they ship are doing the community a genuine service.
