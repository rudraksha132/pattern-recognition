# Changelog

All notable changes to the `pattern-recognition` skill are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html). Dates are in `YYYY-MM-DD` and reflect the date the release was tagged on `main`.

---

## [Unreleased]

### Added

- `CONTRIBUTING.md` — guide for proposing changes to the skill and its reference material.
- `CODE_OF_CONDUCT.md` — community standards and enforcement process.
- `SUPPORT.md` — where to ask questions and what to expect.
- `SECURITY.md` — coordinated disclosure process for security-relevant reports.

### Changed

- None.

### Removed

- None.

### Fixed

- None.

---

## [1.0.0] — 2026-07-19

The first public release of the `pattern-recognition` skill.

### Added

- **`SKILL.md`** — the core seven-stage protocol (Setup → Observation → Analysis → Iteration → Human/historical patterns → Structural patterns → Reporting) with a `version: 1.0.0` frontmatter field.
- **`references/genius-thinking-maps.md`** — reference methods drawing on documented reasoning practices of Einstein, Feynman, Tesla, Newton, Darwin, Curie, Turing, and Ramanujan.
- **`references/pattern-taxonomy.md`** — a catalog of recurring patterns, each with an invariant core, generator rule, prediction, and falsification conditions.
- **`references/failure-and-success-stories.md`** — historical case studies of pattern recognition in science and engineering.
- **`README.md`** — installation instructions for the `npx skills` registry, the Claude Code plugin marketplace, Claude.ai, and the Claude API, plus a worked example Pattern Report.
- **`.claude-plugin/marketplace.json` and `.claude-plugin/plugin.json`** — manifests for Claude Code's plugin marketplace distribution.
- **`LICENSE`** — MIT License, Copyright (c) 2026 rudraksha.
- **`assets/banner.svg`** — the project banner shown in the README.

### Notes

- This is the first tagged release. Installing from `main` before this tag worked for early users; the `1.0.0` tag marks the protocol as stable enough to pin against.
- The skill is intentionally cross-domain. Domain-specific variants should be released as separate skills, not as sub-paths of this one.
- A "honest scope note" appears in the README to make clear that Pattern Reports are structured hypotheses, not verified results.

---

## Release types

For convenience, the change categories below are used throughout this file. They follow the [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) conventions.

- **Added** — new features, reference entries, or files.
- **Changed** — changes in existing functionality, structure, or behavior.
- **Deprecated** — soon-to-be removed features. The skill has none of these yet.
- **Removed** — features that have been removed. The skill has none of these yet.
- **Fixed** — bug fixes, broken links, typos, and rendering issues.
- **Security** — fixes for security-relevant issues. The skill has none of these yet; when one occurs, it will be cross-referenced with the GitHub Security Advisory.

---

## Versioning rules

Because the skill is a prompt-shaped artifact rather than a software library, the version bumps are interpreted as:

- **Patch (`x.y.Z`)** — typo fixes, broken links, single-line corrections to existing reference material. No protocol changes.
- **Minor (`x.Y.0`)** — additions to reference material, new examples, clarifications to existing stages. The protocol's *meaning* does not change.
- **Major (`X.0.0`)** — changes to the protocol's stage definitions, the order of stages, the output shape of a Pattern Report, or the meaning of "falsification condition." These are deliberately rare.

The current protocol is at `1.0.0` because the maintainer considers the output shape stable. Future minor versions will add reference material; future major versions will not be entered into lightly.

---

[Unreleased]: https://github.com/rudraksha132/pattern-recognition/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/rudraksha132/pattern-recognition/releases/tag/v1.0.0
