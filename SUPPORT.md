# Support

This page is for people using `pattern-recognition` and looking for help. If you're contributing instead, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Quick links

- [Report a bug](https://github.com/rudraksha132/pattern-recognition/issues/new?template=bug_report.md)
- [Request a feature or new pattern entry](https://github.com/rudraksha132/pattern-recognition/issues/new?template=feature_request.md)
- [Ask a question (Discussions)](https://github.com/rudraksha132/pattern-recognition/discussions)
- [Read the README](README.md)
- [Read the security policy](SECURITY.md)
- [Read the code of conduct](CODE_OF_CONDUCT.md)

---

## Before you ask

The fastest path to a useful answer is to check the obvious places first:

1. **The README's [Install](README.md#installation) and [Usage](README.md#usage) sections.** Most "it doesn't work" questions are actually "I installed it but the agent didn't activate it" — see the tip near the end of the README.
2. **Existing issues and discussions.** Search before posting; your question may already be answered.
3. **The skill description in `SKILL.md` frontmatter.** If your prompt doesn't match the description, the agent won't load the skill, and that looks like a bug but isn't.

---

## Where to ask

| Kind of question | Where |
|---|---|
| "How do I install this on agent X?" | [Discussions → Q&A](https://github.com/rudraksha132/pattern-recognition/discussions) |
| "The skill produced a Pattern Report I disagree with" | [Discussions → Q&A](https://github.com/rudraksha132/pattern-recognition/discussions) |
| "The skill is not activating for my prompt" | [Discussions → Q&A](https://github.com/rudraksha132/pattern-recognition/discussions) |
| "Here's a bug with a clear repro" | [Issues → bug report](https://github.com/rudraksha132/pattern-recognition/issues/new?template=bug_report.md) |
| "I'd like a new pattern entry / reference file" | [Issues → feature request](https://github.com/rudraksha132/pattern-recognition/issues/new?template=feature_request.md) |
| "I found a security issue" | [SECURITY.md](SECURITY.md) — **do not** file a public issue |

If you accidentally post a security concern in a public issue, we'll convert it to a private report and let you know, but the public path is much slower.

---

## Response times

This is a small project maintained in spare time. Realistic expectations:

| Channel | Target first response |
|---|---|
| Security reports | 3 business days (see [SECURITY.md](SECURITY.md)) |
| Bug reports with a clear repro | 7 days |
| Feature requests | 14 days |
| Q&A discussions | Best effort, often faster |

If a maintainer is away for an extended period, a pinned discussion will say so.

---

## What *not* to expect

To set expectations honestly:

- **The maintainer is not on call.** This is an open-source project, not a service.
- **The skill will not produce perfect Pattern Reports.** The output is a structured hypothesis, not a verified result. The README is explicit about this; please read the "Honest scope note" near the methodology section before assuming a particular report is wrong *because* it disagrees with your own view.
- **The skill does not have access to your data.** It can't see your private repos, your logs, or your past conversations unless you paste them in. "I ran it and it doesn't know about my codebase" is not a bug.
- **Custom agent setups may need custom fixes.** If you've heavily modified how your agent discovers skills, generic installation instructions may not apply. A discussion with your specific setup is the right venue.

---

## Asking well

A good question includes:

- The agent you used (Claude Code, Cursor, Codex, Claude.ai, …) and its version.
- The skill version (from `SKILL.md` frontmatter) or commit SHA.
- The exact prompt you used, copied verbatim.
- What you expected and what you got.
- A link to an existing issue or discussion if it relates to one.

The "Reproducibility matters more than eloquence" tip in [CONTRIBUTING.md](CONTRIBUTING.md) applies to support questions too.

---

## Community

This project is small enough that the GitHub repo *is* the community space. There is no Discord, no Slack, and no mailing list. If you want a real-time answer, that won't change.

For anything else, an issue or a discussion works fine.
