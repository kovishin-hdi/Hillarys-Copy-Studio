# Hillarys Copy Studio — Claude Skill

The full Hillarys India Copy Studio, packaged as a Claude skill. Anyone with this repo can install it and have Claude operate as the Copy Studio — same intelligence, same voice, same governance.

> "We do not sell products. We deliver confidence, comfort, transformation, and convenience."
> — Hillarys Voice of Brand

---

## What this is

A **skill** is a reusable instruction set that teaches Claude how to behave for a specific job. This one teaches Claude to operate as the Hillarys India Copy Studio:

- A **service-brand communication intelligence system**, not a generic AI copywriter.
- Trained on the full Hillarys operating stack: Voice of Brand, the Real Content Matrix (AIDA × Source), the Service Brand Playbook, the Content System, and supporting docs.
- Triggers automatically when you ask Claude for any Hillarys-related communication — WhatsApp messages, social posts, ads, website copy, scripts, briefs, content plans, service-recovery responses.
- Will push back on copy that breaks the brand — discount language, loud luxury, broken promises, post-advance silence, missing ownership.

---

## What you get when the skill is loaded

Ask Claude any of these — once the skill is installed, it will respond as the Copy Studio:

- *"Draft a Wednesday update for a customer in production week 2."*
- *"Write a Reel script for cold-traffic Instagram targeting Bangalore homeowners."*
- *"Review this caption — is it on-brand?"* (paste caption)
- *"We need a 90-day social content plan."*
- *"A customer is angry about a Porter delivery. Help me draft the service-recovery message."*
- *"Write the consultant's opening script for the doorbell moment."*
- *"Which AIDA cell does this fit?"* (paste content)

Claude will diagnose emotional state → identify trust risk → pick the matrix cell → draft in voice → self-check against the rejection list.

---

## Installation

### Option 1 — Claude.ai (web / desktop / mobile)

1. Download this repo as a `.zip` from GitHub, or clone it.
2. Open Claude.ai → **Settings** → **Capabilities** → **Skills**.
3. Click **Upload skill** and select the `hillarys-copy-studio` folder (or the `.skill` packaged file if provided).
4. Start a new conversation. The skill will activate whenever you ask for Hillarys-related communication.

### Option 2 — Claude Code (terminal / developers)

```bash
git clone <(https://github.com/kovishin-hdi/Hillarys-Copy-Studio)> ~/.claude/skills/hillarys-copy-studio
```

The skill will be available in any Claude Code session.

### Option 3 — API / Claude Platform

Pass the contents of `SKILL.md` as a system prompt or include the `references/` files as documents. The skill is plain Markdown — it works anywhere Claude reads instructions.

---

## How to use it well

**1. Just ask naturally.** You don't have to mention "Copy Studio" — the skill auto-triggers on Hillarys, curtains, blinds, consultations, installations, service recovery, etc.

**2. Give it the situation, not just the task.** The Copy Studio is built around emotional state. "Write a WhatsApp message" is okay; "Write a WhatsApp message for a customer who paid advance 4 days ago and hasn't heard from us" is much better.

**3. Trust the pushback.** If the Copy Studio refuses to write "15-day delivery" or "premium London brand" — that's the skill working. The reasons are in `references/service-brand-playbook.md`.

**4. Use diagnosis mode for audits.** Paste an existing post / message / caption and ask "is this on-brand?" — you'll get a structured diagnosis (stage, cell, trust risk, recommendation).

**5. Use draft mode for production.** Ask it to write, and you'll get diagnosis + draft + self-check. The diagnosis at the top makes the reasoning auditable; the self-check at the bottom proves it ran through the rejection list.

---

## Repository structure

```
hillarys-copy-studio/
├── SKILL.md                              ← The operating brain. Read this to understand the system.
├── README.md                             ← This file.
└── references/
    ├── voice-of-brand.md                 ← Full Voice of Brand framework
    ├── the-real-content-matrix.md        ← 28-cell AIDA × Source lookup table
    ├── the-real-content-matrix.png       ← Visual poster of the matrix
    ├── service-brand-playbook.md         ← Six moments, three spaces, choreography
    ├── content-system-summary.md         ← Four-layer content stack + 90-day rotation
    ├── copy-system.md                    ← Core definition of the brand
    ├── copy-studio-agent.md              ← Agent identity statement
    ├── communication-surface-map.md      ← Function of each comms surface
    ├── experience-state-map.md           ← Customer emotional state by stage
    └── service-recovery-system.md        ← Service recovery as trust restoration
```

---

## What the skill enforces

The Copy Studio holds these as non-negotiable:

| Principle | Enforcement |
|---|---|
| The customer is buying handling, not curtains. | Every draft tested against the "we handle this so you don't have to" promise. |
| Calm > hype. | Aggressive urgency, scarcity, and discount language rejected. |
| Refined > loud luxury. | "Premium London-based brand," "most prestigious," etc. rewritten. |
| Promises we can keep. | "15-day delivery" replaced with realistic timelines. |
| Ownership visibility. | Every customer-facing message names a person and a next step. |
| Wednesday Update doctrine. | Post-advance silence is the biggest brand risk — copy actively defends against it. |
| AIDA × Source discipline. | Every visual brief mapped to one of 28 matrix cells before drafting. |
| Voice modulation by stage. | Attention voice ≠ Action voice ≠ Post-install voice. The skill knows which is which. |

---

## Sharing access

To give a teammate or partner access:

1. Add them as a collaborator to this GitHub repo (or share the `.zip`).
2. They follow the installation steps above.
3. Their Claude now operates as the Copy Studio — same as yours.

No API keys, no licences, no setup. The skill is plain Markdown. It travels.

---

## Updating the skill

The Copy Studio is a living system. When the brand voice evolves, when a new service moment is added, when a campaign reveals a missing principle:

1. Edit the relevant file in `references/` (or `SKILL.md` for orchestration changes).
2. Commit and push. Anyone who pulls the repo gets the update.

Versioning convention: bump the version line at the top of any changed file and note the change in a `CHANGELOG.md` (create if it doesn't exist).

---

## Who built this

The Copy Studio is the operationalised brain of the Hillarys India brand — distilled from the 192-review audit, the Voice of Brand framework, the Real Content Matrix, and the Service Brand Playbook. The skill packaging makes it portable.

---

## Closing principle

> The brand is not the logo. It is the lowest-quality moment in the customer's journey.
> The Copy Studio exists so that no message you send is that moment.

— *Service Brand Playbook*
