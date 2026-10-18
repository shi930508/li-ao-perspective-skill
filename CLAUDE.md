# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A content-only Codex/Claude "persona skill" for 李敖 (Li Ao), generated with [女娲·Skill造人术](https://github.com/alchaincyf/nuwa-skill). There is no build system, test suite, linter, or package manifest. "Development" means editing Markdown and keeping it internally consistent. The only installable unit is the `li-ao-perspective/` directory (the README installs it via Codex's `install-skill-from-github.py --path li-ao-perspective`). README and docs are written in Chinese; keep new content in Chinese.

## Architecture

- `li-ao-perspective/SKILL.md` is the skill itself and the only file the runtime loads up front. The YAML frontmatter `description` is the trigger: it fires on explicit "李敖视角/模式/口吻/文风" requests and deliberately does **not** fire for plain factual queries about Li Ao. Preserve that split when editing it.
- `SKILL.md` is organized as: roleplay rules → answer workflow (question classification, minimal research routing, research steps A–E, answer shape, drift check, acceptance gate) → five invocation modes → identity card → mental models → decision heuristics → expression DNA → values/anti-patterns → tensions → intellectual lineage → honesty boundaries.
- `references/research/01–12-*.md` are the evidence base, loaded lazily. The "最小研究路由" section of `SKILL.md` maps question type to the 1–3 files to read (e.g. style → `03` + `10`, decisions → `05` + `06`). When adding or renaming a research file, update that routing list.
- `12-synthesis.md` is the Phase 2 distillation. Its candidate table and triple-validation (跨域复现 / 生成力 / 排他性) produced the 7 mental models (M1–M7) and 9 heuristics that `SKILL.md` restates. These counts are repeated in `SKILL.md`'s self-check section, in the description frontmatter, and in `README.md` ("7 个核心心智模型", "9 条决策启发式", "12 份研究稿", "70余项" sources); change them together.
- `references/sources/{articles,books,transcripts}/` and `scripts/` contain only `.gitkeep`; they are placeholders for user-supplied source material and helper scripts.

## Conventions that matter when editing

- Source layering is part of the content: claims are tagged as 本人原话 / 可核事实 / 他人评价 / 框架推断. Do not blur these tiers or add quotes without a verifiable source; the skill itself forbids fabricating Li Ao's experiences or sayings.
- The guardrails in `SKILL.md` (no gender/body/vulnerability shaming, no privacy exposure, no encouraging litigation-as-harassment or dangerous stunts, say "框架推断，不是本人立场" for topics Li Ao never addressed) are load-bearing; any new mode, example, or style sample must stay inside them.
- Style capture targets sentence structure and method, not profanity or catchphrases.
