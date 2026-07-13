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

## The customer journey, end to end

The skill now models the **whole customer relationship** — from a stranger's first enquiry to the day their curtains are fitted — as two automated WhatsApp journeys that meet at the home consultation. The **lead journey** guides a *prospect* to a booked consultation; the **order journey** carries a *paying customer* calmly through the wait. Same promise throughout: *"we handle this so you don't have to."*

```
  ┌─ PRE-ORDER · Lead journey (prospect) ──────────────────────┐
  │  Enquiry → Serviceability check → Qualification →           │
  │  Appointment booked → (re-engagement · holds)               │  references/lead-lifecycle-triggers.md
  └──────────────────────────────┬──────────────────────────────┘
                                 │
                      ╔══════════▼═══════════╗
                      ║  THE SEAM            ║
                      ║  Home consultation   ║   visit → order → 50% advance
                      ╚══════════╤═══════════╝
                                 │
  ┌──────────────────────────────▼──────────────────────────────┐
  │  Order confirmed → Check-measure → Quotation → Production →  │
  │  Quality check → Balance → Dispatch → Installation           │  references/crm-lifecycle-triggers.md
  └─ POST-ORDER · Order journey (customer) ─────────────────────┘
```

### Pre-order — the lead journey (`lead-lifecycle-triggers.md`)

Keyed to lead source and CRM lead status. Guide-not-gate, honesty-over-capture, no-silence — backed by the **30-minute follow-up**, **running Notes**, and **smart-skip** mechanics.

| Trigger | Fires on | What it does |
|---|---|---|
| **L1** | Website form complete | Welcome + qualification (skips the pincode gate) |
| **L2** | Fresh WhatsApp-button lead | Welcome → **Bangalore serviceability / pincode gate** → qualify |
| **L3** | After YES / slot confirmed | Qualification: property → windows → style → site readiness |
| **L4** | Site not ready | Capture timeline, offer an Experience-Centre visit, hold warmly |
| **L5** | RNR / Unable to Contact | Re-engage — "pick one call-back window", no blame |
| **L6** | Call Back / Follow-up-Later | Thank-you-for-your-time, then a reminder on the follow-up date |
| **L7** | Appointment Booked | Confirm the free in-home consultation |
| **L8** | Appointment today (1 hr before) | Reminder + decision-maker + experience video |
| **L9** | Site Note Ready — Future | Hold, then an **early** readiness nudge (15d → Day 10 …) |
| **L10** | Store Visit | Schedule an Experience-Centre visit |
| **L11** | Not Interested | A gracious close, door left open |
| **L12** | Less than ₹20K | Redirect to the Shivaji Nagar Experience Centre (threshold never named) |
| **L13** | Existing-customer inbound | Menu re-entry by status — reschedule · book · talk to an expert · locate |

### Post-order — the order lifecycle (`crm-lifecycle-triggers.md`, v1.1)

Twelve word-tested messages that cure the *Silence After Advance*. Every message carries three payloads in order — **status → craft/care line → a bold, numbered `*Here are the NEXT STEPS:*` lookahead** — plus a named owner.

| Trigger | Code | Milestone |
|---|---|---|
| **T1** | `order_confirmed` | Welcome + 7-step roadmap + 50% advance + fabric lock |
| **T2** | `cm_scheduled` | Check-measure planned (installer named) |
| **T3** | `cm_completed` | Measurements done & re-checked |
| **T4** | `quotation_sent` | Scope of work + final quotation |
| **T5** | `order_approved` | Components placed the same day |
| **T6** | `crafting_started` | With the master tailors |
| **T7** | `stitching_qc` | Stitched, now in quality check |
| **T8** | `ready_balance_due` | Cleared QC — balance due |
| **T9** | `payment_received` | Balance received |
| **T10** | `dispatched` | On its way — handled with care |
| **T11** | `install_scheduled` | Installation scheduled (installer messages 15 min before) |
| **T12** | `install_completed` | Done + toll-free support + gentle referral |

> A visual companion — both journeys as an annotated flow map for marketing review — can be regenerated on request.

### The map underneath both journeys — the Order Journey Charter (`order-journey-charter.md`)

The messages above are *how we say things*. Underneath them sits the **customer-facing document that says what is true** — the **"Your Order Journey" leaflet** every customer is handed, captured for the skill as [`references/order-journey-charter.md`](references/order-journey-charter.md) (the leaflet itself ships alongside it as [`order-journey-leaflet.pdf`](references/order-journey-leaflet.pdf)).

It is the **fact-check layer**: every WhatsApp trigger, quote note, consultation script, and service-recovery line must stay consistent with what the customer was already told on paper. A message that is beautifully on-voice but contradicts the leaflet is a broken promise wearing good copy. The Charter pins down:

- **The three-stage payment schedule** — a **5% / ₹5,000 token "price & discount freeze"** *before* the 50% advance (the CRM library previously jumped straight to the 50%), then the 50% balance. The token freezes the price; it does **not** process the order.
- **The real timeline** — 15 *working* days from *check-measurement* (longer for motorised/imported) — the true number behind the skill's refusal to promise "15-day delivery."
- **The hard rules** — no changes/cancel/refund after the 50%; quote valid 15 days; one install visit (re-visit chargeable); 48-hour defect window; warranty = manufacturing defects only.
- **The named-owner roster + escalation matrix** — Design Consultant → CSR/MMT → CSR/CRM → Installation Manager (Level 1), ASM/SM (Level 2), Customer Service (Level 3) — the roster the "name a person" rule draws from.
- **The Commitment, verbatim** — *"you shouldn't have to chase us for status updates"* and *"every person who visits your home will be introduced to you in advance, by name."* The anti-silence mandate and the ownership rule, promised to the customer in writing.

This is how the flywheel tightens: the skill no longer just writes in the right *voice* — it writes in a way that is provably consistent with the promise document in the customer's hand.

---

## What's new — v1.3.0

This release adds the **Order Journey Charter** — the customer-facing source of truth — and wires it through the skill as a fact-check layer. See [`CHANGELOG.md`](CHANGELOG.md) for the detailed entry.

- **Added** [`references/order-journey-charter.md`](references/order-journey-charter.md) and the source leaflet [`references/order-journey-leaflet.pdf`](references/order-journey-leaflet.pdf): the 8-stage journey, the 3-stage payment schedule, real timelines, hard rules, owner roster + escalation matrix, and the written Commitment.
- **Wired** the Charter into `SKILL.md` — §3 operating stack (as the fact source, distinct from the voice sources), §6 (both journeys narrate one map the customer holds), §7 rejection list (a draft fails if it contradicts the Charter), §8 (the "15-day" refusal now cites the true number), and §12 reference index.
- **Surfaced** four drifts between the leaflet and the current libraries as open decisions — the 5%/₹5,000 token step isn't narrated in WhatsApp; CRM Trigger 1's procurement line is broader than the leaflet's split-procurement rule; two support numbers coexist; and public timeline wording needs one approved phrasing.

---

## Previously — v1.2.0

This release brings the repo up to date with the **full journey** above. See [`CHANGELOG.md`](CHANGELOG.md) for the detailed entry.

- **Added** the pre-order lead journey (`lead-lifecycle-triggers.md`) — the prospect half of the journey was previously undocumented.
- **Upgraded** the post-order library to **v1.1** with marketing's review applied: 50% advance named in T1; the two-step lookahead standardised to a bold, numbered `*Here are the NEXT STEPS:*` block across T2–T11; refreshed craft lines in T6–T8; and T12 now carries the Toll-Free line (+91-7795830298) and a referral, reconciled with the Voice of Brand's "share the experience, never refer-and-earn" rule.
- **Restructured** the repo so `references/` ships as loose files at the root — browsable and diffable on GitHub, and `git clone` yields a working skill.
- **`SKILL.md`** now treats the journey as two halves meeting at the consultation seam.

**Open for marketing to close** (flagged in-file): lock one canonical site-completion timeline set; define what the referral "token of appreciation" is; resolve the `{type}` = "both" phrasing in T8–T12.

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
git clone <this-repo-url> ~/.claude/skills/hillarys-copy-studio
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
    ├── lead-lifecycle-triggers.md        ← Pre-order lead journey (enquiry → qualification → appointment)
    ├── crm-lifecycle-triggers.md         ← 12 automated post-order WhatsApp triggers (order → install)
    ├── order-journey-charter.md          ← Source of truth: 8 stages, payment schedule, timelines, rules, owners, Commitment
    ├── order-journey-leaflet.pdf         ← The customer-facing "Your Order Journey" leaflet (primary source for the charter)
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
| Ownership visibility. | Every customer-facing message names a person and a next step — from the Charter's owner roster, never "our team." |
| Consistency with the leaflet. | Every fact — payment %, timeline, rule, owner — is checked against the Order Journey Charter so no message contradicts what the customer holds on paper. |
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
