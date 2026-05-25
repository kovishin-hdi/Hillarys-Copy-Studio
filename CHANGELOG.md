# Changelog

All notable changes to the Hillarys Copy Studio. Each version covers `SKILL.md`, `references/`, and the adapters.

The format is loosely based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [1.1.0] — 2026-05-25

### Added
- `adapters/chatgpt/` — ChatGPT Custom GPT adapter:
  - `INSTALL.md` — 15-minute Custom GPT setup
  - `gpt-instructions.md` — paste into the Custom GPT's Instructions field
- `scripts/sync-claude-to-adapters.py` — regenerates all three adapter instruction files from `SKILL.md` + `references/voice-of-brand.md`
- `scripts/sync-claude-to-adapters.sh` — Bash wrapper around the Python sync script
- `scripts/README.md` — sync workflow + suggested git pre-commit hook
- `--check` mode in the sync script for CI / pre-commit usage

### Changed
- The three adapter instruction files (`copilot-instructions.md`, `agent-instructions.md`, `gpt-instructions.md`) are now **auto-generated** from a single shared body. Each carries an `AUTO-GENERATED FILE` banner and a source hash. Do not edit them by hand — edit `SKILL.md` and re-run the sync.
- Updated `README.md` to include the ChatGPT adapter and document the sync flow.

### Fixed
- Eliminated drift risk between adapter instruction files. Previously, updating Voice of Brand meant manually editing two (now three) files; now it's one script run.

---

## [1.0.0] — 2026-05-25

### Added
- Initial Copy Studio skill package
- `SKILL.md` — operating brain (Claude-native)
- `references/` — full operating stack:
  - `voice-of-brand.md`
  - `the-real-content-matrix.md` (text)
  - `the-real-content-matrix.png` (visual)
  - `service-brand-playbook.md`
  - `content-system-summary.md`
  - `copy-system.md`
  - `copy-studio-agent.md`
  - `communication-surface-map.md`
  - `experience-state-map.md`
  - `service-recovery-system.md`
- Adapters:
  - `adapters/claude/` — Claude.ai / Claude Code / API install
  - `adapters/github-copilot/` — GitHub Copilot custom instructions
  - `adapters/m365-copilot-agent/` — Microsoft 365 Copilot Studio agent

### Decisions encoded
- The customer is buying handling, not curtains
- The Wednesday Update is the heartbeat of the post-advance silence
- 15-day delivery promise is retired in favour of 21 days (or silence)
- "Premium London-based brand" is retired in favour of *"50 years of European craftsmanship, now made in India"*
- The Real Content Matrix becomes the lookup for all visual content briefs
- Channel recipes (Social / Performance / Website / Physical) are locked

---

## How to version going forward

- **Major (X.0.0):** breaking changes — voice rewrite, new mandatory moment in the choreography, retirement of a core principle.
- **Minor (0.X.0):** new reference files, new adapters, new rejection-list entries.
- **Patch (0.0.X):** typo fixes, clarifications, formatting.

When updating:
1. Bump the version in this file with a new dated entry.
2. List what changed under **Added**, **Changed**, **Removed**, **Fixed**.
3. If an adapter needs re-publishing (M365 Copilot especially), note that in the entry.
4. Commit and push.
