# CRM Lifecycle Triggers — The 12-Message WhatsApp Journey (Post-Order)
Version: 1.1
Status: Operational template library (customer-facing, automated)
Owner: Hillarys India — CRM / Marketing
Source: The realisation of Service Brand Playbook, Moment 4, Marketing Action #3 — *"Create a simple Hillarys-branded WhatsApp message template library — twelve standard messages, each thoroughly word-tested, that coordinators can copy-paste."*
Companion file: `lead-lifecycle-triggers.md` — the **pre-order** half of the journey (enquiry → qualification → appointment → consultation). This library begins where that one ends: the moment an order is confirmed and advance is received.

---

## What this is

These are the **twelve automated WhatsApp messages** a customer receives across a single order — from confirmation to installation. They are the operational answer to the most damaging moment in the Hillarys journey: **the Silence After Advance** (see `service-brand-playbook.md`, Moment 4).

The playbook diagnosed the disease — customers pay 50%, then hear nothing, and trust decays. This library is the cure: a message at every meaningful state change, so the customer *never has to chase us for an update*. That is the whole point. Every trigger is one more proof of the brand promise: **"we handle this so you don't have to."**

**The customer journey has two halves, and Hillarys owns both:**
- **Pre-order** (`lead-lifecycle-triggers.md`): first enquiry → qualification → appointment booked → home consultation → quotation → advance. The job is to guide and reassure a *prospect* without pressure.
- **Post-order** (this file): advance received → check-measure → production → QC → balance → dispatch → installation. The job is to keep a *paying customer* informed and calm through the wait.

The seam between them is the home consultation: the pre-order library hands the customer to a Design Consultant; that visit produces the order and advance; Trigger 1 below picks the customer up the moment the advance clears.

**Governance:**
- **One CRM owns each order** and is the single point of contact until handover.
- **The CRM approves every message before it sends.** These are automated *triggers*, not autopilot — a human named person stands behind each one.
- The messages are word-tested. Coordinators copy the approved wording; they do not improvise per-order except in the merge fields.

---

## v1.1 — what changed in the marketing review

This version applies the marketing team's markup of the v1.0 library, and takes each note one step further into a house standard. Every change below is faithful to the marketing intent; where a note collided with a standing brand rule (the rejection list in `SKILL.md` §7), the intent is kept and the wording is refined to be on-brand — those cases are called out.

| Trigger | Marketing note | Applied as |
|---|---|---|
| T1 | Confirm the advance is 50%; bold "One important note" | Roadmap step 1 now reads "50% advance received"; `*One important note:*` is bolded (WhatsApp `*asterisks*`) |
| T2 | Add "be available and keep window access open"; convert Next/Then to a bolded, numbered "NEXT STEPS" | Availability + access line added; lookahead is now `*Here are the NEXT STEPS:*` + numbered list. "Kindly be available" softened to "Please be home" (§7 bans "kindly") |
| T3–T5, T9–T11 | Convert Next/Then to bolded, numbered NEXT STEPS | Applied as the new house standard for the two-step lookahead |
| T6 | Comma after "your fabric is in"; remove "and"; new craft line "…skilled craftsmen who have perfected this process over time — giving it the care and attention it deserves" | Applied verbatim (em-dash for house style). This **resolves Open Decision #1** — marketing chose experiential wording over a number |
| T7 | "fabric stitching is complete"; NEXT STEPS numbered | Applied; "quality check" kept in sentence case for house consistency |
| T8 | "Crafted, Measured and Checked"; "Before we dispatch your order, there's one final step — the balance payment"; NEXT STEPS numbered | Applied (sentence case). Note the word **order changed** to Crafted → Measured → Checked |
| T12 | New craft line "Carefully measured, expertly crafted, and perfectly fitted — made for your home exactly how you imagined"; add Toll-Free +91-7795830298; add referral link {Link} with a "token of appreciation" | Applied. The referral is reconciled with the brand's referral rule — see T12 rationale and Open Decision #5 |
| Library-wide | Bold the NEXT STEPS header; number the steps | New standard: the two-step lookahead now renders as a bold `*Here are the NEXT STEPS:*` header over a numbered list, replacing the `Next:` / `Then:` labels. The *content* is unchanged — it is still exactly two steps — only the formatting is standardised |

---

## The doctrine — why every message is built the way it is

A Hillarys lifecycle message is never *just* a status update. A bare "your order is in production" is operationally true and emotionally empty — it reads like a ticket system, which the Voice of Brand forbids (`voice-of-brand.md` §4 Humanise, §14 CRM & WhatsApp tone). Every message in this library carries **three payloads**, always in this order:

1. **The status** — what just happened, in plain, calm language. The fact the trigger exists to report.
2. **The craft / care line** — one sentence of emotional reassurance that reframes the status as *handling and care*, not logistics. This is what turns "stitching is done" into "every seam, fold, and finish is being checked… nothing reaches your home until it's right." It is the line that makes an operational update *feel premium*.
3. **The two-step lookahead** — a bold `*Here are the NEXT STEPS:*` header over a **numbered list of exactly the next two steps**. This is the anti-silence mechanism: the customer always knows where they are and what is coming, so uncertainty never has room to grow. It is the Wednesday-update doctrine, compressed into every message. (v1.0 wrote this as `Next:` / `Then:`; v1.1 renders it as a bolded, numbered header. Same two steps — clearer format.)

Plus two constants that sit across all three:
- **Ownership visibility** — the message comes from a named CRM (`{crm}`), set up in Trigger 1 and standing behind every later trigger. Never "our team" as the sole owner of a message.
- **Calm, not hype** — no urgency, no scarcity, no discount language, no exclamation-stacking. Celebration is allowed (a genuine milestone); pressure is not.

> **The test for any lifecycle message:** does it report the fact, reassure the feeling, and remove the uncertainty about what's next? If a message does only the first, it is incomplete — it has become the ticket system we exist to replace.

---

## Anatomy of a lifecycle message

```
[Status line]              ← what just happened, calm and plain
[Craft / care line]        ← one sentence: reframe logistics as handling & care
                             (blank line)
*Here are the NEXT STEPS:*  ← the two-step lookahead (bold header)
1. [the immediate next step]
2. [the step after that]
```

With two deliberate exceptions:
- **Trigger 1 (the welcome)** carries the full **seven-step roadmap** instead of a two-step lookahead, because its job is to set the whole map at the start.
- **Trigger 12 (installation complete)** is terminal — there is no "next step," so it closes with support, a toll-free line, and a gentle referral invitation instead of a lookahead.

**Format rules that render correctly on WhatsApp:**
- **Bold is written with single asterisks** — `*like this*` — which WhatsApp renders as bold on the customer's phone. The bolded spans in this library are the T1 roadmap intro, `*One important note:*` (T1), and every `*Here are the NEXT STEPS:*` header.
- Emoji render as-is.
- `*Here are the NEXT STEPS:*` and its numbered list are customer-facing. **`Fires when:` is internal context only — it is NEVER sent to the customer.**
- Target length: ~6–7 lines with the craft line + numbered lookahead. This is a phone screen, not an email. Trim before you pad.
- Emoji discipline: **1–2 per message** by default. The welcome (T1) and the balance-due (T8) use more, by design, because they are the two highest-emotion moments (arrival and payment).

---

## Merge variables — the `{curly braces}`

Auto-filled per order. **Never reword or remove a variable** — the sentences *around* them are open to editing, the tokens are not.

| Variable | Fills with | Notes |
|---|---|---|
| `{name}` | Customer's name | Warm, first-name basis |
| `{crm}` | The owning CRM's name | The single point of contact; set in T1 |
| `{type}` | `curtain` / `blind` / `both` | ⚠️ See Open Decision #2 — "your both is almost home" reads awkwardly |
| `{cmdate}` | Check-measure date | T2 |
| `{slot}` | Check-measure time slot | T2 |
| `{installer}` | Installer's name | T2, T10, T11 — a second named person |
| `{instdate}` | Installation date | T11 |
| `{islot}` | Installation time slot | T11 |
| `{balance}` | Balance amount due (₹) | T8 |
| `{pay}` | Secure payment link | T8 |
| `{Link}` | Personal referral link | T12 |

**Fixed brand assets (constants, not merge fields):**
- **Toll-Free:** +91-7795830298 (T12; also the lead-lifecycle support number)

---

## The 12 triggers — at a glance

| # | Code | Journey stage | Customer emotional state | Trust risk this message defends against |
|---|---|---|---|---|
| 1 | `order_confirmed` | Decision → Waiting | Excited, slightly anxious (just paid 50% advance) | The Silence After Advance beginning; not knowing what happens next; fabric-lock anxiety |
| 2 | `cm_scheduled` | Waiting | Anticipating, wanting certainty | A vague "someone will come"; access/logistics confusion |
| 3 | `cm_completed` | Waiting | Reassured, watching for progress | Wondering if the measurement was done right |
| 4 | `quotation_sent` | Decision (approval) | Evaluating, mildly cautious | "Additional charges after advance" fear; feeling rushed to approve |
| 5 | `order_approved` | Waiting | Committed, wanting momentum | Post-approval silence; "did anything actually happen?" |
| 6 | `crafting_started` | Waiting | Excited, invested | The long production wait; feeling forgotten mid-order |
| 7 | `stitching_qc` | Waiting | Anticipating quality | Worrying the product might arrive flawed |
| 8 | `ready_balance_due` | Waiting → Action | Anticipation + payment friction | Balance ask feeling transactional; trust wobble at the money moment |
| 9 | `payment_received` | Waiting | Relieved, eager | Payment made, then silence; "did it go through, what now?" |
| 10 | `dispatched` | Waiting → Installation | Excited, nearly there | Delivery-handling anxiety (the "Porter" fear); loss of visibility in transit |
| 11 | `install_scheduled` | Installation | Anticipating the finish | Not knowing who's coming, when, or how prepared they are |
| 12 | `install_completed` | Post-installation | Grateful, proud | The abandonment-after-sale fear; feeling dropped once we have the money |

Emotional-state stages map to `experience-state-map.md` and `voice-of-brand.md` §9. Voice modulates across them: warm at the start, transparent and proactive through the wait, celebratory at handover, grateful after.

---

## The 12 triggers — full template library

> `Fires when:` lines are internal only. Do not send them to the customer.

### TRIGGER 1 — Order confirmed · `order_confirmed`
**Fires when:** Order created / 50% advance received; procurement cleared.
**Stage:** Decision → Waiting. **State:** excited, slightly anxious. **Voice:** warm, welcoming, reassuring.
**Job:** set the whole map, introduce the named owner, open the single channel, and gently lock fabric selection.

```
Hello {name} 🎉 Welcome to Hillarys, and congratulations on your new {type}.

I'm {crm}, your Customer Relationship Manager and your single point of contact until handover. I've set up this group so every update reaches you in one place — you'll never have to chase us for one. 💬

Here's the journey ahead, so you always know where we are:
1. Order confirmed — 50% advance received ✅
2. Check-measure at your home 📏
3. Quotation shared for your approval 📋
4. Production — your fabric stitched, blinds made 🪡
5. Quality check approved 🔍
6. Balance payment & dispatch 🚚
7. Installation day 🏡

From today, your windows are in good hands — and we'll treat them like our own. 🤝

*One important note:* all fabrics for your order are being procured today, so fabric selections can't be changed after this point.

I'll guide you through each step as it happens. Anything you need in between, just message me here.
```
*Why this works:* it is the Single Named Handover from Moment 4 — one named person, one channel, one promise ("you'll never have to chase us"). The seven-step roadmap replaces the two-step lookahead because T1's job is to hand the customer the whole map. The fabric-lock note is bolded and framed as care ("being procured today"), not restriction. *v1.1:* step 1 now names the 50% advance; the fabric-lock note is bolded per marketing.

---

### TRIGGER 2 — Check-measure planned · `cm_scheduled`
**Fires when:** Check-measure assigned to installer with a date.
**Stage:** Waiting. **State:** anticipating. **Voice:** transparent, proactive.

```
Hi {name}, your check-measure is planned for {cmdate} ({slot}) with {installer} 📏 Our check-measure team will call to confirm. Please be home on the day and keep all your windows accessible.

Every measurement we take is the foundation of a perfect fit, so we take our time to get it exactly right. 🎯

*Here are the NEXT STEPS:*
1. Our team completes the check-measure at your home.
2. We prepare your quotation and scope of work for your approval.
```
*Craft line reframes:* a logistics appointment becomes "the foundation of a perfect fit." Introduces `{installer}` — the second named person. *v1.1:* added the availability + window-access instruction marketing asked for. "Kindly be available" softened to "Please be home" — "kindly" is on the rejection list (`SKILL.md` §7); the *instruction* is preserved, the corporate word is not.

---

### TRIGGER 3 — Check-measure done · `cm_completed`
**Fires when:** Installer marks CM complete (Site Capture / Ops OS).
**Stage:** Waiting. **State:** reassured. **Voice:** calm, confident.

```
Hi {name}, your check-measure is successfully completed ✅

We've carefully re-checked every measurement to make sure your {type} fits your windows just right. 📐

*Here are the NEXT STEPS:*
1. We share your final quotation and scope of work for your approval.
2. Once you approve, we place components and move into production.
```

---

### TRIGGER 4 — Quotation / SOW sent · `quotation_sent`
**Fires when:** SOW generated in Ops OS; awaiting approval.
**Stage:** Decision (approval). **State:** evaluating. **Voice:** clear, no-pressure, trustworthy.
**Job:** deliver the price without the "additional ₹25k after advance" fear. Defends The Quote moment (Playbook Moment 3).

```
Hi {name}, please find your scope of work and final quotation attached 📋 Review and approve whenever you're ready — I'm here to talk through anything you need. 😊

Every detail here has been mapped specifically to your windows and your home.

*Here are the NEXT STEPS:*
1. On your approval, we place all remaining components.
2. Your fabric arrives and goes to our tailoring team to begin crafting.
```
*Note:* "final quotation" and "mapped specifically to your windows" quietly reinforce the no-surprises promise. Approval is invited, never pressured — "whenever you're ready" replaces "kindly."

---

### TRIGGER 5 — Approved → components placed · `order_approved`
**Fires when:** Approval ack uploaded; stage-2 cleared in Ops OS.
**Stage:** Waiting. **State:** committed, wanting momentum. **Voice:** appreciative, proactive.

```
Thank you for approving, {name}! ✅ All remaining components in your order are placed today. 📦

Each piece has been chosen specifically for your order — nothing off the shelf, everything made to your scope.

*Here are the NEXT STEPS:*
1. Your fabric arrives with us and goes to our master tailors for crafting.
2. Once stitching is done, your order moves into quality check.
```
*Defends against post-approval silence:* proves within the same day that approval triggered real action ("placed today").

---

### TRIGGER 6 — Crafting in progress · `crafting_started`
**Fires when:** Fabric received; handed to tailoring team.
**Stage:** Waiting. **State:** excited, invested. **Voice:** warm, premium.

```
Exciting update {name} — your fabric is in, your {type} is now with our master tailors ✂️ Crafting is officially underway 🪡

Your fabric is now in the hands of skilled craftsmen who have perfected this process over time — giving it the care and attention it deserves. ✨

*Here are the NEXT STEPS:*
1. Once stitching is complete, your order goes into quality check.
2. On clearing QC, we share your balance and payment link to schedule dispatch.
```
*v1.1:* applies marketing's markup exactly — comma after "your fabric is in," "and" removed, and the new craft line about skilled craftsmen. This **resolves Open Decision #1**: marketing chose experiential wording ("perfected this process over time") over a hard number. A real, defensible number (years / pieces made) can still upgrade the line later if one is confirmed.

---

### TRIGGER 7 — Stitching done / QC · `stitching_qc`
**Fires when:** Stitching complete; QC in progress.
**Stage:** Waiting. **State:** anticipating quality. **Voice:** reassuring, exacting.

```
Quick update {name} — fabric stitching is complete and your order is now in quality check. 🔍

Every seam, fold, and finish is being checked against our standards before it leaves us — nothing reaches your home until it's right. ✔️

*Here are the NEXT STEPS:*
1. Once it clears QC, we share your balance and payment link.
2. On payment, we dispatch your order and arrange installation.
```
*Craft line does emotional pre-work:* the customer is told we catch flaws *before* dispatch, so the arrival carries less anxiety. *v1.1:* "fabric stitching is complete" per marketing.

---

### TRIGGER 8 — Ready, balance due · `ready_balance_due`
**Fires when:** QC done; awaiting 50% dispatch payment.
**Stage:** Waiting → Action. **State:** anticipation + payment friction. **Voice:** celebratory then calm-transactional. **Emoji:** heavier by design (a milestone + a money moment).
**Job:** ask for the balance without turning the relationship transactional. The care line does the trust work *before* the money line.

```
Great news {name}! ✅ Your order has cleared quality check and is ready to dispatch. 🎉

Crafted, measured, and checked — your {type} is now ready for the journey home.

Before we dispatch your order, there's just one final step to complete — the balance payment:
💰 Balance due: ₹{balance}
🔗 Pay securely: {pay}

*Here are the NEXT STEPS:*
1. Once your balance is in, we dispatch your order.
2. We schedule your installation on a day that suits you.
```
*Structure matters:* the emotional payoff ("ready for the journey home") lands *before* the payment ask, so the balance feels like the last small step of a well-handled journey — not a toll gate. "Pay securely" reassures at the exact point trust could wobble. *v1.1:* the recap line now reads "Crafted, measured, and checked" (marketing's new word order) and the balance step uses marketing's "one final step to complete" framing.

---

### TRIGGER 9 — Payment received · `payment_received`
**Fires when:** Dispatch payment received.
**Stage:** Waiting. **State:** relieved, eager. **Voice:** grateful, warm.

```
Thank you {name}! 🙏 Your balance is received and your order is ready for dispatch.

Your {type} is packed with care and ready to make its way to you. 📦

*Here are the NEXT STEPS:*
1. Share a convenient day and we dispatch your order.
2. We line up your installation right after.
```
*Closes the payment loop immediately:* confirms receipt so the customer never wonders "did it go through?" — a small silence this trigger deliberately fills.

---

### TRIGGER 10 — Dispatched · `dispatched`
**Fires when:** Order dispatched.
**Stage:** Waiting → Installation. **State:** excited, nearly there. **Voice:** reassuring about handling.

```
Your order is on its way, {name}! 🚚 It's been dispatched and will reach you shortly.

Handled with care every step of the journey — your {type} is almost home. 🏡

*Here are the NEXT STEPS:*
1. We schedule your installation and confirm the date and slot.
2. {installer} arrives to fit everything just right.
```
*"Handled with care every step of the journey"* directly answers the Porter / third-party-delivery anxiety documented in the reviews — the brand stays visibly in charge of the last mile.

---

### TRIGGER 11 — Installation scheduled · `install_scheduled`
**Fires when:** Installation date set.
**Stage:** Installation. **State:** anticipating the finish. **Voice:** thoughtful, premium.
**Job:** defend The Installer Arriving moment (Playbook Moment 5) — the customer meets us for the second time.

```
Hi {name}, your installation is scheduled for {instdate} ({islot}) with {installer} 🛠️

{installer} will treat your home with the same care that went into crafting your order. 🤝

*Here are the NEXT STEPS:*
1. We confirm the final slot a day before, and {installer} messages you 15 minutes before arriving.
2. Installation day — your {type} comes to life in your home. 🏡
```
*The "15 minutes before arriving" line* is the Moment-1 / Moment-5 choreography made into a customer-facing promise — it pre-sells the installer as prepared and branded, not a stranger at the door.

---

### TRIGGER 12 — Installation completed · `install_completed`
**Fires when:** Installation marked complete.
**Stage:** Post-installation. **State:** grateful, proud. **Voice:** celebratory, relationship-led.
**Job:** The Last Ten Feet (Playbook Moment 6) — defend against the biggest post-sale fear (being dropped once we have the money), keep the support channel open, and invite advocacy gently.

```
All done, {name}! 🎉 Your installation is complete — we hope you love your new {type}. 🏡

Carefully measured, expertly crafted, and perfectly fitted — made for your home exactly how you imagined. ✨

For any assistance going forward, our Toll-Free line is +91-7795830298 — we'll be happy to help with anything you need.

Know someone looking for curtains or blinds? You can share the Hillarys experience with your personal Referral Link {Link} — whenever you share it and the person you refer chooses us, we'll send across a small token of appreciation. Thank you for your support!

Thank you for choosing Hillarys 🙏
```
*Rationale:* the new craft line is marketing's ("carefully measured, expertly crafted, and perfectly fitted"). The toll-free line makes the promise of continued support concrete. On the **referral** — v1.0 deliberately carried *no* referral ask here, on the Voice of Brand rule against transactional referrals (`voice-of-brand.md` §16; `SKILL.md` §8). Marketing has now added one, and it is compatible *because of how it is framed*: it uses the approved "**share the Hillarys experience**" language and a "**token of appreciation**" (gratitude), not a cash "refer and earn ₹X" mechanic. That is the exact line §16 draws. The Copy Studio keeps this framing and would refuse any future rewrite that turns it into a rewards/earnings pitch. See Open Decision #5.

---

## The craft-line pattern — a reusable device

The single most portable idea in this library is the **craft / care line**: one sentence that reframes an operational fact as handling and care. Reach for it any time you must report logistics to a customer.

| Operational fact | Off-brand (ticket system) | On-brand (craft line) |
|---|---|---|
| Measurement booked | "Appointment scheduled." | "Every measurement is the foundation of a perfect fit." |
| In production | "Order in production." | "In the hands of skilled craftsmen who have perfected this process over time — giving it the care and attention it deserves." |
| In QC | "Undergoing quality check." | "Every seam, fold, and finish checked… nothing reaches your home until it's right." |
| Dispatched | "Out for delivery." | "Handled with care every step of the journey — almost home." |
| Installed | "Installation closed." | "Carefully measured, expertly crafted, and perfectly fitted — made for your home exactly how you imagined." |

When a scenario arises that these 12 triggers don't cover (a delay, a reschedule, a partial dispatch), **compose in the same anatomy**: status → craft line → two-step lookahead (`*Here are the NEXT STEPS:*` + numbered) → named owner. Never fall back to a bare status.

---

## Open decisions (for marketing review)

1. **Craft-number credibility (T6) — RESOLVED in v1.1.** Marketing replaced the v1.0 placeholder with "skilled craftsmen who have perfected this process over time." A real, defensible number (years of craftsmanship, pieces made) would make the line stronger still — *keep this open as an upgrade the moment a true figure is confirmed; a specific number always beats a vague flourish.*
2. **`{type}` awkwardness (T8, T9, T10, T12) — STILL OPEN.** When `{type}` = `both`, the craft lines read awkwardly ("your both is almost home"). *Decision needed:* keep `{type}` or switch those specific lines to "your order." *Recommendation: use "your order" wherever the sentence inflects `{type}` as a noun — it is graceful for all three values and never breaks.*
3. **Emoji count on T1 and T8.** These two use more emoji than the 1–2 default, by design (arrival + payment, the two highest-emotion moments). *Confirm the team is comfortable with the heavier load on exactly these two.*
4. **Message length.** With the craft line + numbered NEXT STEPS, messages now run ~6–7 lines — slightly longer than v1.0's `Next:`/`Then:` form. *Confirm this still reads well on a phone, or flag which triggers to trim.* The lookahead is load-bearing (it is the anti-silence mechanism) — trim the status or craft line before cutting a NEXT STEP.
5. **Referral mechanic (T12) — NEW.** The "token of appreciation" is deliberately vague. *Decision needed:* is the token a fixed gift, a voucher, a credit? Keep the customer-facing wording soft ("token of appreciation" / "share the Hillarys experience") regardless of what the token is operationally — the moment the copy names a cash amount or says "earn," it crosses the §16 line and stops being on-brand.

---

## How the Copy Studio uses this file

- **Editing a lifecycle message?** Start from the canonical template above. Preserve the three-payload anatomy and every `{variable}`. You may refine the prose around the tokens; you may not drop a payload.
- **Drafting a message for a state these 12 don't cover** (delay, reschedule, escalation, partial order)? Compose in the same anatomy — status, craft line, numbered NEXT STEPS, named owner — and keep it calm.
- **Something has gone wrong** (missed date, damaged item, complaint in the group)? This library stops; **service recovery takes over** (`service-recovery-system.md`). Recovery is trust restoration, not a status update — acknowledge, name the person who will handle it, give a real timeline, and only then return to the lifecycle cadence.
- **The customer is still a prospect** (no order yet)? This is the wrong file — use `lead-lifecycle-triggers.md` for enquiry, qualification, and appointment-booking.
- **Reviewing a proposed message?** Run it through the rejection list in `SKILL.md` §7. A lifecycle message additionally fails if it: drops the named owner, drops the two-step lookahead, reverts to bare status with no craft line, adds urgency/discount language to the balance ask (T8), turns the T12 referral into an "earn rewards" pitch, or reworks a `{variable}`.

---

## Cross-references

- `lead-lifecycle-triggers.md` — the pre-order half: enquiry → qualification → appointment → consultation. This library begins at order confirmation, where that one ends.
- `service-brand-playbook.md` — Moment 4 (Silence After Advance, the origin of this library), Moment 3 (The Quote → T4), Moment 5 (Installer Arriving → T11), Moment 6 (Last Ten Feet → T12), and the Three Spaces (Space 3, the WhatsApp group).
- `voice-of-brand.md` — §9 stage-by-stage customer language, §14 CRM & WhatsApp tone, §16 referral restraint.
- `experience-state-map.md` — the emotional state each trigger meets.
- `service-recovery-system.md` — what to do when a trigger's premise fails.
- `communication-surface-map.md` — WhatsApp as the live reassurance layer.

---

*End of file. Living document — revise as triggers are added, wording is word-tested in production, and the open decisions are resolved.*
