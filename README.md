<div align="center">

# 🧠 Pattern Recognition

**Structured, falsifiable analysis — for any coding assistant.**

A Skill that structures analysis around the observation and reasoning methods historically associated with rigorous scientific discovery: first-principles decomposition, invariance analysis, cross-domain analogy, and falsifiable reporting.

[![Skill](https://img.shields.io/badge/format-Agent%20Skill-D97757?style=flat)](https://github.com/anthropics/skills)
[![40+ agents](https://img.shields.io/badge/works%20with-40%2B_agents-blue?style=flat)](https://github.com/vercel-labs/skills)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat)]()

[Overview](#overview) · [Install](#installation) · [Methodology](#core-methodology) · [Usage](#usage) · [Structure](#package-structure) · [Versioning](#versioning)

</div>

---

## Overview

`pattern-recognition` is an [Agent Skill](https://github.com/anthropics/skills) — a self-contained package of instructions and reference material that a coding assistant loads dynamically when relevant to a task — that structures how the assistant analyzes recurring structures in data, systems, and behavior.

Rather than defaulting to the first explanation that fits the available evidence, the skill directs the assistant to treat anomalies as primary signal, search for invariants across scale and context, test hypotheses through thought experiments, and report findings in a format that states what would falsify them. It draws on documented reasoning approaches of Einstein, Feynman, Tesla, Newton, Darwin, Curie, Turing, and Ramanujan as reference models, not as narrative flourish.

The intended use case is analytical work where surface-level pattern matching is insufficient — root-cause analysis, historical or systemic comparisons, and open-ended research questions.

Because it follows the [Agent Skills](https://github.com/anthropics/skills) standard, it is not tied to one product. It works the same way across Claude Code, Claude.ai, Cursor, Codex, Gemini CLI, Windsurf, Cline, Copilot, and 40+ other agents supported by the [`npx skills`](https://github.com/vercel-labs/skills) CLI.

---

## Installation

**Universal — via the skills registry**

```bash
npx skills add rudraksha132/pattern-recognition
```

This resolves the package and installs it for every supported agent detected on your machine.

**Target a specific agent**
```bash
npx skills add rudraksha132/pattern-recognition -a claude-code
npx skills add rudraksha132/pattern-recognition -a cursor
npx skills add rudraksha132/pattern-recognition -a codex
npx skills add rudraksha132/pattern-recognition -a windsurf
```

**Install globally, available in every project**
```bash
npx skills add rudraksha132/pattern-recognition -g
```

**Preview what would be installed**
```bash
npx skills add rudraksha132/pattern-recognition --list
```

**Claude Code — plugin marketplace**
```bash
/plugin marketplace add rudraksha132/pattern-recognition
/plugin install pattern-recognition
```

**Claude.ai / Claude apps (Pro, Max, Team, Enterprise)**
1. Download this repository, or clone it locally.
2. Navigate to **Settings → Capabilities → Skills → Upload skill**.
3. Upload the repository folder.

**Claude API**
Upload the package via the [Skills API](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) and reference it in the `skills` parameter of your request configuration.

**Manual**
```bash
git clone https://github.com/rudraksha132/pattern-recognition.git ~/.claude/skills/pattern-recognition
```

### Verify

```bash
npx skills list
```
`pattern-recognition` should appear with its install location and target agent(s).

---

## Core methodology

The skill discourages several default reasoning shortcuts and replaces them with an explicit protocol:

| Principle | Description |
|---|---|
| Anomaly-first analysis | Outliers and exceptions are treated as the primary object of study, not excluded as noise. |
| Cross-domain analogy | When analysis stalls in one domain, the skill directs a search for structurally similar patterns in unrelated fields (epidemiology, fluid dynamics, market cycles). |
| Invariance analysis | Following Einstein's approach to relativity, the method looks for what remains constant as context, scale, or observer changes, and treats that invariant as the underlying rule. |
| Thought experiments | Hypotheses are extended to their limiting cases before being accepted. |
| Compression as a validity check | An explanation that cannot be stated concisely is treated as incomplete. |
| Structured reporting | Every finding is reported in a standard format that includes the conditions under which it would be falsified, and the questions it leaves open. |

---

## Usage

The skill is triggered automatically by prompts such as:

```
"What's the underlying pattern here?"
"Why does this keep happening?"
"Analyze the failure modes in [system / event / market]"
"What would explain both of these observations?"
"Approach this from first principles"
```

It can also be invoked explicitly:

```
Use the pattern-recognition skill to analyze why our last three product
launches stalled at the same stage.
```

The assistant moves through an observation → anomaly identification → invariance analysis → hypothesis testing pipeline, concluding with a structured Pattern Report: name, invariant core, generator rule, prediction, falsification conditions, and open questions.

---

## How it works

1. Install drops `SKILL.md` and its `references/` folder into the target agent's skills directory.
2. The agent matches incoming prompts against the skill's description and loads it when relevant.
3. The core protocol in `SKILL.md` runs the request through a fixed analytical pipeline.
4. Deep-dive reference files — genius-specific reasoning maps, a pattern taxonomy, and historical case studies — are pulled in on demand rather than loaded up front, keeping the base skill lightweight.

---

## Package structure

```
pattern-recognition/
├── SKILL.md                              Core protocol, loaded first
├── README.md
└── references/
    ├── genius-thinking-maps.md           Reference methods: Einstein, Feynman, Tesla,
    │                                      Newton, Ramanujan, Darwin, Curie, Turing
    ├── pattern-taxonomy.md               Catalog of recurring patterns, with examples
    └── failure-and-success-stories.md    Case studies of historical pattern recognition
                                           successes and near-misses
```

`SKILL.md` sits at the repository root so the package installs directly via `npx skills add rudraksha132/pattern-recognition`, with no subpath needed.

| Phase | Focus |
|---|---|
| 0 — Setup | Establishes the analytical posture: hypothesis-neutral, anomaly-attentive |
| 1 — Observation | Layered observation (surface / structural / universal), anomaly scanning, cross-domain input |
| 2 — Analysis | First-principles decomposition, invariance analysis, thought experiments, compression checks |
| 3–4 — Iteration | Treats unresolved confusion and failed hypotheses as informative, not as stopping points |
| 5 — Human/historical patterns | Recurring social and historical templates (paradigm shifts, systemic overreach) |
| 6 — Structural patterns | Common generative mechanisms in natural and complex systems (power laws, feedback loops, phase transitions) |
| 7 — Reporting | Standardized, falsifiable output format |

---

## Versioning

Releases follow semantic versioning via the `version` field in `SKILL.md` frontmatter.

```bash
npx skills add rudraksha132/pattern-recognition@v1.0.0   # pin a release
npx skills update pattern-recognition                     # update to latest
npx skills remove pattern-recognition                     # uninstall
```

Installing from `main` tracks the latest changes.

---

## Publishing

This repository is ready to publish as-is: push it to a public GitHub repository named `pattern-recognition`, and it becomes installable immediately via `npx skills add rudraksha132/pattern-recognition`. There is no separate submission step — the [skills.sh](https://skills.sh) directory indexes public packages automatically once they're installed.

---

## Privacy

The skill makes no network calls of its own. It is a prompt and a set of Markdown reference files with no telemetry, accounts, or backend. Install-time fetches are limited to GitHub and the skills registry used by your agent.

---

## Attribution

Built as an [Agent Skill](https://github.com/anthropics/skills) (YAML frontmatter, Markdown instructions, bundled reference files), installable via [`npx skills`](https://github.com/vercel-labs/skills). Reference material draws on documented reasoning practices of Einstein, Feynman, Tesla, Newton, Darwin, Curie, Turing, and Ramanujan.

## License

MIT
