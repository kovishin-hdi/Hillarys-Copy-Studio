# Changelog

All notable changes to the Hillarys Copy Studio. Each version covers `SKILL.md`, `references/`, and the adapters.

The format is loosely based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [1.3.0] — 2026-07-13

Adds the **Order Journey Charter** — the customer-facing source of truth — and wires it through the skill as a fact-check layer. Until now the skill governed *how* we say things (voice, matrix, choreography, template anatomy) but had no canonical record of *what is true*. This release grounds every draft in the **"Your Order Journey" leaflet** the customer is actually handed, closing the gap between what we tell the customer on paper and what our messages say.

### Added
- `references/order-journey-charter.md` **(new)** — the **customer-facing source of truth**, drawn from the "Your Order Journey" leaflet:
  - The **eight journey stages** with the leaflet's named owner for each (Home Consultation → Quotation → Price & Discount Freeze → 50% Advance/Order Processed → Manufacturing → Ready for Dispatch → Installation → After-Care & Warranty).
  - The **three-stage payment schedule** — a **5% / ₹5,000 token "price & discount freeze"** *before* the 50% advance (previously absent from the skill), then the 50% balance — with the rule that the token does **not** process the order and procurement is **split** (curtains/Roman fabric same-day; other blinds & components after check-measurement).
  - The **canonical facts** copy must not contradict — indicative quote (~90–95%, valid 15 days), **15 working days from check-measurement** (longer for motorised/imported), no changes/cancel/refund after the 50%, one install visit (re-visit chargeable), 48-hour defect window, warranty = manufacturing defects only.
  - The **owner roster + escalation matrix** (Level 1 DC / CSR-MMT / CSR-CRM / Installation Manager, Level 2 ASM/SM, Level 3 Customer Service — orders@hillarys.co.in / 090082 81888).
  - The **Commitment**, verbatim — *"you shouldn't have to chase us for status updates"* and *"every person who visits your home will be introduced to you in advance, by name"* — cited as the primary source for the anti-silence and ownership-visibility doctrines.
  - A **leaflet → CRM-trigger mapping table** and a **How the Copy Studio uses this file** section (the fact-check discipline).
- `references/order-journey-leaflet.pdf` **(new)** — the leaflet itself, the primary-source document the Charter is drawn from.

### Changed
- `SKILL.md`:
  - §3 operating stack now lists `order-journey-charter.md` as the **fact source**, explicitly distinct from the voice sources, with a note that any draft stating a number/timeline/owner/rule must match it.
  - §6 reframed so both journey halves narrate **one map the customer holds**, citing the leaflet's two Commitment lines as the written origin of the anti-silence and ownership rules.
  - §7 rejection list gains a failure condition: a draft that **contradicts the Charter**.
  - §8: the refusal to promise "15-day delivery" now cites the true figure (15 *working* days from *check-measurement*).
  - §12 reference index updated with the charter and the leaflet PDF.
- `README.md`: new "map underneath both journeys" subsection, a v1.3.0 "What's new," an enforcement-table row for leaflet consistency, and the repository structure updated.

### Notes — open decisions surfaced (for Operations & Marketing)
- **CRM Trigger 1's procurement line is broader than the leaflet.** T1 says all fabrics are procured today; the leaflet orders only curtains/Roman fabric same-day and everything else after check-measurement, and the real hard rule is *no changes at all* after the 50%. Recommend revising T1.
- **The 5% / ₹5,000 token freeze is not narrated in WhatsApp** — it is the customer's first payment and currently a silent step. Recommend a `price_frozen` trigger in the standard anatomy.
- **Two support numbers coexist** — leaflet 090082 81888 vs CRM Toll-Free +91-7795830298. Confirm which is canonical for which purpose.
- **Public timeline wording** needs one approved phrasing across sales, lifecycle, and marketing (e.g. "made to measure in about three weeks").

---

## [1.2.0] — 2026-07-07

Brings the repository up to date with the full customer-journey lifecycle. The post-order library (previously local-only) is now published, upgraded to v1.1 with marketing's review applied, and joined by a new pre-order lead-journey library — so the skill now covers enquiry → qualification → appointment → consultation → order → production → dispatch → installation, end to end.

### Added
- `references/lead-lifecycle-triggers.md` **(new)** — the **pre-order lead journey**: the prospect half of the WhatsApp journey, from first enquiry to a booked home consultation.
  - Lead sources: website form (L1) and WhatsApp-button fresh lead (L2, with a Bangalore serviceability/pincode gate).
  - Qualification sequence (L3): property → windows → style → site readiness, one question per message.
  - Site-not-ready hold (L4) with Experience-Centre offer and the ≤15-day consultation-visit case.
  - Lead-status triggers L5–L13: RNR / Unable to Contact, Call Back / Follow-up-Later, Appointment Booked, same-day reminder, Site Note Ready–Future Requirement (with early delay-nudge logic), Store Visit, Not Interested, Less than ₹20K, and existing-customer inbound menus by status.
  - The CRM mechanics the copy depends on: the **30-minute follow-up rule**, the **running Notes summary**, and the **smart-skip rule**.
  - Three pre-order doctrine rules: **guide-not-gate, honesty-over-capture, no-silence**.
- `references/` is now committed as loose files at the repository root (previously shipped only inside the packaged zip), so the operating stack is browsable and diffable on GitHub and `git clone` yields a working skill.

### Changed
- `references/crm-lifecycle-triggers.md` → **v1.1**, applying the marketing team's review of the 12 post-order triggers:
  - T1: roadmap step 1 now names the **50% advance**; `*One important note:*` bolded.
  - Two-step lookahead standardised across T2–T11 from `Next:` / `Then:` to a bolded, numbered **`*Here are the NEXT STEPS:*`** header (content unchanged — still exactly two steps).
  - T2 access instruction added ("kindly" softened to "please" per the rejection list); T6 craft-line rewrite (**resolves the old craft-number open decision**); T7 "fabric stitching is complete"; T8 "Crafted, measured, and checked" + "one final step — the balance payment."
  - T12: new craft line; added Toll-Free **+91-7795830298**; added the **{Link} referral**, reconciled with the referral rule (Voice of Brand §16) — "share the Hillarys experience" + "token of appreciation," never "refer and earn."
  - New merge variable `{Link}`; new Open Decision on the referral-token definition.
- `SKILL.md`: §3 operating stack now lists the pre-order and post-order WhatsApp libraries as distinct sources of truth; §6 reframed around the two halves of the journey and the consultation seam; §12 reference index updated.
- `README.md`: repository structure lists `lead-lifecycle-triggers.md`.
- `hillarys-copy-studio.zip` refreshed to match the current skill.

### Notes
- The two lifecycle libraries now cover the full customer journey end to end.
- Open decisions are recorded in each file for marketing to close (canonical site-completion timeline set and the referral-token definition are the load-bearing ones).

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
