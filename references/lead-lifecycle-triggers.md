# Lead Lifecycle Triggers — The Pre-Order WhatsApp Journey (Enquiry → Appointment)
Version: 1.0
Status: Operational template library (customer-facing, automated + assisted)
Owner: Hillarys India — CRM / Marketing / Design Consultant desk
Companion file: `crm-lifecycle-triggers.md` — the **post-order** half (order confirmed → installation). This library ends where that one begins.

---

## What this is

This is the **pre-order half of the Hillarys journey**: every automated WhatsApp message a *prospect* receives from their first enquiry to the moment a home consultation is booked (and, when a lead isn't ready yet, everything that keeps the relationship warm until they are).

If `crm-lifecycle-triggers.md` protects the **paying customer** through the wait, this file protects the **prospect** through the decision. Same brand promise — *"we handle this so you don't have to"* — carried from the very first message, before any money has changed hands.

**Where this sits in the whole journey:**

```
   ENQUIRY ──▶ QUALIFY ──▶ APPOINTMENT BOOKED ──▶ HOME CONSULTATION ──▶ order + advance
   └──────────── lead-lifecycle-triggers.md (this file) ────────────┘         │
                                                                              ▼
                                          crm-lifecycle-triggers.md (order_confirmed → install_completed)
```

The seam is the **home consultation**: this library's job is to get a qualified, serviceable prospect to a booked appointment (or to hold a not-yet-ready lead warmly until they are). The Design Consultant runs the visit; the visit produces the order and advance; Trigger 1 of the post-order library picks the customer up from there.

**Governance:**
- **Serviceability first.** Hillarys currently services **Bangalore only**. Every WhatsApp-button lead is pincode-checked before qualification; out-of-area leads get an honest, warm close, never a false promise.
- **One assigned team member owns each lead** and follows up. Automated messages set the appointment intent; a named person confirms availability and calls back — within 30 minutes of the customer's response (see *Cross-cutting mechanics*).
- **The system never re-asks what it already knows.** Before any qualification message sends, it checks which details are already on file and asks only for what's missing (see *The smart-skip rule*).
- These are word-tested templates. The team copies the approved wording; per-lead variation lives in the merge fields and in the option the customer picks.

---

## The doctrine — how a pre-order message earns trust before we've earned money

A prospect has given us nothing yet but their attention. That makes the pre-order voice different from the post-order voice in one specific way: **there is no order to reassure about, so the reassurance is about *us* — that we are easy, honest, and worth their time.** Three rules govern every message here:

1. **Guide, never gate.** We are collecting qualification details (property type, windows, style, site readiness) — but the customer must feel *guided*, not *processed*. Each question is framed as helping us prepare for *their* consultation, not as a form we require them to complete. (`voice-of-brand.md` §7.2 Guide, §2 Simplify.)
2. **Honesty over capture.** If we can't serve them (outside Bangalore) or they're not ready (site incomplete) or the fit is wrong (budget below range), we say so warmly and leave the door open — we do not drag an unqualified lead through the funnel. An honest "not yet" protects the brand more than a booked appointment we can't honour.
3. **Never let a prospect wait in silence.** Every response gets an immediate acknowledgement, and a named person calls back within 30 minutes. The anti-silence doctrine that governs the post-order library starts *here* — a lead who messages and hears nothing is the pre-order version of the Silence After Advance.

Plus the two constants shared with the whole system:
- **Ownership visibility** — a real person confirms and calls back; automated messages say "our team will connect with you shortly," and then someone actually does.
- **Calm, not hype** — no "Book now!", no scarcity, no discount bait. We invite; we do not pressure. A prospect who feels chased is a prospect who remembers being chased.

> **The test for any pre-order message:** does it move the lead forward *and* leave them feeling helped rather than harvested? If it collects a detail but makes the customer feel like a record being filled in, rewrite it.

---

## Anatomy of a lead message

Pre-order messages are shorter and more functional than post-order ones (they're mid-conversation, often awaiting a menu reply), but they still carry a consistent shape:

```
[Warm opener / acknowledgement]     ← name the person, thank or welcome them
[The ask or the answer]             ← one clear question, or one clear confirmation
[The options, when choosing]        ← a short, scannable list (property type, slot, timeline)
[Sign-off]                          ← "Regards, Hillarys Curtains & Blinds" on standalone sends
```

**Format rules (WhatsApp):**
- One question per message. Never stack two decisions in a single bubble — the customer answers the last one and drops the first.
- Options render as a short bulleted or dashed list, ≤ 6 items. If there are more, split the flow.
- Bold with single asterisks `*like this*` for the one thing that matters (a confirmed slot, a key instruction).
- Emoji: **light** — 0–1 per message in the qualification flow. This is a working conversation, not a milestone celebration; save emoji for genuine warmth points (welcome, "almost done", appointment booked).
- The sign-off block appears on standalone automated sends, not on every back-and-forth bubble.

---

## Shared assets & merge variables

**Merge variables:**

| Variable | Fills with | Notes |
|---|---|---|
| `{Name}` / `{{1}}` | Prospect's name | `{{1}}` is the WhatsApp template placeholder form; `{Name}` the readable form — same value |
| `{slot}` | The time window the customer picked | Home-consultation slot or call-back window |
| `{timeline}` | Site-completion estimate the customer picked | 15 / 20 / 25 / 30 / 45 / 60 / 90 days |

**Fixed brand assets (constants):**

| Asset | Value |
|---|---|
| Service area | **Bangalore only** (pincode-gated) |
| Toll-Free | **7795830298** ( +91-7795830298 ) |
| Experience Centre | Shivaji Nagar, Bangalore |
| Experience Centre location link | https://maps.app.goo.gl/GptR7ZPZCRguLbYX7 |
| Customer-experience video (same-day reminder) | https://youtu.be/AE5gGeKcYEA |

**The three slot schemes (keep them distinct):**

| Scheme | Options | Used for |
|---|---|---|
| **Home-consultation slots** | Mon–Fri 11 AM / 2 PM / 5 PM · Sat 11 AM / 2 PM / 5 PM | Booking a Design Consultant home visit when the site is ready |
| **Call-back windows** | 10 AM–1 PM · 1 PM–4 PM · 4 PM–7 PM | "Reply with ONE window and we'll call you" — used across re-engagement and Experience-Centre flows |
| **Consultation-visit slots** | 10 AM–1 PM · 1 PM–4 PM · 4 PM–7 PM | When a site is ≤15 days from ready and a consultant plans a visit |

**The qualification data set (what we're collecting):**
Pincode (serviceability) → Property type (2BHK / 3BHK / 4BHK / Villa / Others) → Windows needing cover (1–3 / 4–6 / 7–10 / 10+) → Style (Basic / Modern / Luxury) → Site & interiors ready? (Yes / No) → Appointment slot **or** site-completion timeline → Full address / WhatsApp location.

---

## The lead-status trigger map

Every automated pre-order message is keyed to a **lead source** or a **lead status** in the CRM. This is the index; the templates follow.

| Trigger | Fires on | Job |
|---|---|---|
| **L1 · Website form complete** | Prospect submits the full website form | Welcome, confirm intent, run qualification (no pincode gate — form already scoped) |
| **L2 · Fresh WhatsApp lead** | Prospect taps the WhatsApp button on the website | Welcome → **pincode/serviceability gate** → qualification |
| **L3 · Qualification sequence** | After YES / after slot confirmed | Collect property, windows, style, site-readiness; branch on site-ready |
| **L4 · Site not ready** | Customer answers "site not ready" | Capture timeline, offer Experience-Centre visit, hold warmly |
| **L5 · RNR / Unable to Contact** | Lead status set to RNR or Unable to Contact | Re-engage: "we tried reaching you — pick one call-back window" |
| **L6 · Call Back / Follow-up – Later** | Lead status: Fresh–Call Back, or Qualified–Call Back & Follow-up | Thank-you-for-your-time, then reminder on the follow-up date |
| **L7 · Appointment booked** | Lead status: Appointment Booked | Confirm the free in-home consultation |
| **L8 · Same-day reminder** | Appointment is today (1 hr before) | Remind, ask for the decision-maker, share the experience video |
| **L9 · Site Note Ready – Future Requirement** | Lead status: Site Note Ready | Acknowledge, then delay-trigger a "is your site ready now?" nudge |
| **L10 · Store Visit** | Lead status: Store Visit | Schedule an Experience-Centre visit |
| **L11 · Not Interested** | Lead status: Not Interested | Warm close, leave the door open, give the toll-free |
| **L12 · Less than ₹20K** | Lead status: Less than ₹20K | Redirect to the Experience Centre self-serve, gracefully |
| **L13 · Existing-customer inbound** | Any existing lead messages us, keyed by their status | Menu-driven re-entry (reschedule / talk to an expert / book / locate) |

---

## The templates

> `Fires on:` lines are internal. The sign-off "Regards, Hillarys Curtains & Blinds" is customer-facing on standalone sends.

### L1 — Website form complete → welcome + qualification
**Fires on:** Prospect submits the full website form (name, contact, requirement).
**Stage:** Discovery → Consultation. **Voice:** warm, welcoming, guiding.

```
Hi {Name}, thank you for choosing Hillarys.

Our team will help you plan your curtains & blinds home consultation — fabric selection, measurements, and a quotation built around what you need.

A few quick details help us prepare for your visit. Shall we begin?
Reply YES to continue.

Regards,
Hillarys Curtains & Blinds
```
*Then run the qualification sequence (L3).* Because the website form already captured contact and requirement, this path **skips the pincode gate** and goes straight to property → windows → style → site-readiness.
*Voice note:* the raw operational line "we require a few additional details" is reframed as "a few quick details help us prepare for your visit" — same ask, but it serves the customer's consultation instead of our records (`voice-of-brand.md` §7.2 Guide). "Reply YES" is kept as the WhatsApp opt-in mechanic.

---

### L2 — Fresh WhatsApp lead → serviceability gate
**Fires on:** Prospect taps the WhatsApp button on the website (Day 0).
**Stage:** Discovery. **Voice:** warm, honest.

**L2a — Welcome + pincode:**
```
Hi {Name}, thank you for choosing Hillarys.

We'll help you plan your curtains & blinds home consultation — fabric selection, measurements, and a quotation built around your space.

To confirm we can reach you, could you share your 6-digit pincode?

Regards,
Hillarys Curtains & Blinds
```

**L2b — Within Bangalore → proceed** to the qualification sequence (L3), starting with property type.

**L2c — Outside Bangalore → honest close:**
```
Thank you for reaching out to Hillarys. Right now our service is available only within Bangalore — but we're growing, and we'll be sure to let you know the moment we reach your city.

Regards,
Hillarys Curtains & Blinds
```
*Why the gate matters:* qualifying an out-of-area lead only to disappoint them later is the opposite of "we handle this." The honest close (rule 2) protects the brand and keeps the door open without a false promise.

---

### L3 — The qualification sequence
**Fires on:** After the customer replies YES (L1) / passes the pincode gate (L2) / confirms a slot in a re-engagement flow.
**Stage:** Consultation. **Voice:** guided, one question at a time.

Send these **one per message**, in order, skipping any detail already on file (see *The smart-skip rule*):

**Q1 — Property type:**
```
To tailor your consultation, what's your property type?
- 2BHK
- 3BHK
- 4BHK
- Villa
- Other
```

**Q2 — Windows:**
```
How many windows would you like covered with curtains or blinds?
- 1–3
- 4–6
- 7–10
- More than 10
```

**Q3 — Style:**
```
And the style you're leaning towards?
- Basic
- Modern
- Luxury
```

**Q4 — Site readiness (the branch point):**
```
Is your site ready and the interior work completed?
- Yes
- No
```

**Q4 → Yes → book the consultation:**
```
Wonderful. Please choose an appointment slot that suits you:
- Mon–Fri · 11 AM
- Mon–Fri · 2 PM
- Mon–Fri · 5 PM
- Sat · 11 AM
- Sat · 2 PM
- Sat · 5 PM
```
then:
```
Almost done — could you share your full address or WhatsApp location so our consultant can reach you?
```
then the **close** (L3-close):
```
Thank you for sharing your details. Our expert Design Consultants will be in touch shortly to confirm your appointment and assist you further.
```

**Q4 → No →** go to **L4 (site not ready)**.

*Voice note:* every "Kindly" in the raw flow is dropped or replaced with "Please" — "kindly" is on the rejection list (`SKILL.md` §7). Each question carries a one-line reason ("to tailor your consultation") so it reads as guidance, not interrogation.

---

### L4 — Site not ready → capture timeline + offer the Experience Centre
**Fires on:** Customer answers "No" to site readiness (or later says the site still isn't ready).
**Stage:** Consultation (deferred). **Voice:** patient, no-pressure, keep-warm.

**L4a — Acknowledge + ask for timeline:**
```
Thank you for letting us know. Once your site and interiors are ready, we'll gladly send our Design Consultant across.

If you can share a rough completion timeline, we'll plan your consultation around it:
- 15 days
- 20 days
- 30 days
- 45 days
- 60 days
- 90 days
```

**L4b — Offer an Experience-Centre visit while they wait:**
```
While your site is coming together, you're welcome to visit our Experience Centre to explore fabrics in person. Reply with ONE window that suits you and we'll make sure a Design Consultant is free to guide you:
- 10 AM–1 PM
- 1 PM–4 PM
- 4 PM–7 PM

Our Experience Centre: https://maps.app.goo.gl/GptR7ZPZCRguLbYX7

Regards,
Hillarys Curtains & Blinds
```
then, once they pick a window:
```
Thank you for sharing your preferred time to visit our Experience Centre. Our team will confirm availability and get back to you shortly.

Regards,
Hillarys Curtains & Blinds
```

**L4c — Special case: site ≤15 days from ready → plan a consultation visit.**
When the timeline chosen is **15 days**, the consultant can plan a visit rather than only an Experience-Centre trip:
```
Great — since your site is expected to be ready within about 15 days, our Design Consultant can plan a visit for measurements, fabric selection, and quotation support.

So the visit goes smoothly, a clean space to lay out the fabric options helps a lot. Please pick a slot that suits you:
- 10 AM–1 PM
- 1 PM–4 PM
- 4 PM–7 PM

Regards,
Hillarys Curtains & Blinds
```
then the L3-close.

*After any L4 close, set the follow-up and update Notes (see Cross-cutting mechanics). A ≤15-day lead is close to ready — keep the follow-up tight.*

---

### L5 — RNR / Unable to Contact → re-engage
**Fires on:** Lead status = *RNR* or *Unable to Contact* (we called, couldn't reach them).
**Stage:** Consultation (stalled). **Voice:** warm, undefensive — never scolding.

```
Hi {{1}}, we tried reaching you earlier about your consultation.

Whenever it's convenient, reply with ONE window for your home consultation and our Design Consultant will call you then:
- 10 AM–1 PM
- 1 PM–4 PM
- 4 PM–7 PM

Regards,
Hillarys Curtains & Blinds
```
**Once a window is selected:**
```
Thank you for confirming. Our team will connect with you shortly to confirm the slot is available.

A few quick details help us prepare — shall we continue?
Reply YES to continue.

Regards,
Hillarys Curtains & Blinds
```
then run the qualification sequence (L3), skipping anything already collected. Set follow-up + update Notes.
*Voice note:* "we tried reaching you" is stated once, plainly, with no guilt attached ("we couldn't get through", not "you didn't answer"). The customer is never made to feel they did something wrong.

---

### L6 — Call Back / Follow-up – Later → hold and remind
**Fires on:** Lead status = *Fresh – Call Back* or *Qualified – Call Back & Follow-up – Later* (a specific follow-up time is agreed).
**Stage:** Consultation (scheduled). **Voice:** warm, appreciative.

**L6a — After the call, confirm the follow-up:**
```
Hi {Name}, thank you for your time today — it was good speaking with you.

As agreed, we'll reconnect at the scheduled time to arrange your in-home consultation. If anything comes up before then, we're a message away, or call us on 7795830298.

Warm regards,
Team Hillarys
```

**L6b — On the follow-up date, the reminder:**
```
Hi {Name}, a gentle reminder about your enquiry with Hillarys — your home consultation is still open.

Reply with ONE window and our Design Consultant will call you then:
- 10 AM–1 PM
- 1 PM–4 PM
- 4 PM–7 PM

Regards,
Hillarys Curtains & Blinds
```
**Once a window is selected:** confirm ("Thank you for confirming your appointment slot. Our team will connect with you shortly to confirm availability."), then — for a *Fresh – Call Back* lead not yet qualified — run the qualification sequence (L3). Set follow-up + update Notes.
*Note:* a *Qualified* lead is already scoped, so L6 goes straight to slot confirmation and the close. A *Fresh* lead still needs qualification after the slot. The smart-skip rule decides which.

---

### L7 — Appointment booked → confirm
**Fires on:** Lead status = *Appointment Booked*.
**Stage:** Consultation (confirmed). **Voice:** warm, reassuring.

```
✅ Appointment booked

Thank you, {Name}. Your free in-home design consultation is scheduled. Our Design Consultant will visit, understand what you're looking for, take measurements, show you suitable fabrics, and share a quotation — all in one visit.

If anything changes, just let us know.

Regards,
Hillarys Curtains & Blinds
```
*Why "free" and "one visit":* the two quiet reassurances a first-time prospect needs — no cost to meet us, and no fragmented back-and-forth. This is the "we handle this" promise, pre-order.

---

### L8 — Same-day reminder (1 hour before)
**Fires on:** Appointment is today; 1 hour before the slot.
**Stage:** Consultation (imminent). **Voice:** warm, lightly practical.

```
Hi {Name}, a quick reminder — your Hillarys consultation is today ✅

Our Design Consultant will help with fabric selection, take measurements, and share an on-the-spot quotation. It helps if the key decision-maker can be there, so nothing waits on a second conversation.

A glimpse of what to expect, from other homes: https://youtu.be/AE5gGeKcYEA

Regards,
Hillarys Curtains & Blinds
```
*The decision-maker line* is operationally important (it prevents a wasted visit) but framed as convenience for *them* ("so nothing waits"), never as our requirement. The video is social proof at the moment of highest intent.

---

### L9 — Site Note Ready – Future Requirement → hold + delay-nudge
**Fires on:** Lead status = *Site Note Ready – Future Requirement* (qualified, but the site won't be ready for a while).
**Stage:** Consultation (parked). **Voice:** patient, low-touch.

**L9a — Acknowledge and park:**
```
Hi {Name}, thank you for choosing Hillarys. As discussed, we'll reconnect at the right time to arrange your consultation.
```

**L9b — Delay-trigger the readiness nudge.** Based on the timeline the customer gave, fire the nudge *before* the stated date, so we reach them just as the site lands:

| Customer said | Nudge fires on day |
|---|---|
| 15 days | Day 10 |
| 20 days | Day 14 |
| 25 days | Day 15 |
| 30 days | Day 20 |
| 45 days | Day 25 |

**The nudge:**
```
Hi {Name}, just checking in — is your site ready for the consultation now? As soon as it is, we'll be glad to send our Design Consultant across to help with your requirements. Let us know a convenient time and we'll take it from there.

Regards,
Hillarys Curtains & Blinds
```
- **Yes, site is ready →** offer the home-consultation slots (Mon–Fri / Sat scheme), confirm, close, set follow-up.
- **No, not ready →** back to L4 (capture a fresh timeline, offer the Experience Centre).

*Why nudge early:* reaching out *before* the deadline (Day 10 for a 15-day site) catches the lead at the moment of readiness instead of after they've moved on — the pre-order version of proactive, not reactive.

---

### L10 — Store Visit → schedule the Experience-Centre visit
**Fires on:** Lead status = *Store Visit* (prospect wants to come to us).
**Stage:** Consultation. **Voice:** welcoming.

```
Hi {Name}, thank you for your interest in visiting our Experience Centre. Reply with ONE window and we'll schedule your visit accordingly:
- 10 AM–1 PM
- 1 PM–4 PM
- 4 PM–7 PM

Our Experience Centre: https://maps.app.goo.gl/GptR7ZPZCRguLbYX7

Regards,
Hillarys Curtains & Blinds
```
**Once a window is selected:**
```
Thank you for sharing your preferred time to visit our Experience Centre. Our team will confirm availability and get back to you shortly.

Regards,
Hillarys Curtains & Blinds
```
Set follow-up + update Notes.

---

### L11 — Not Interested → warm close
**Fires on:** Lead status = *Not Interested*.
**Stage:** Exit (kept open). **Voice:** gracious, no pressure.

```
Hello {{1}}, thank you for your time and for speaking with us. We completely understand — and if curtains or blinds are ever on your mind again, we'd be glad to help on 7795830298. Wishing you a lovely day ahead.

Regards,
Hillarys Curtains & Blinds
```
*The brand's posture on a "no":* accept it gracefully, leave one warm door open, and stop. No "are you sure?", no discount to change their mind. A respected "no" is remembered as respect.

---

### L12 — Less than ₹20K → redirect to self-serve
**Fires on:** Lead status = *Less than ₹20K* (requirement below the home-consultation threshold).
**Stage:** Redirect. **Voice:** helpful, un-condescending.

```
Hello {{1}}, you're very welcome to visit the Hillarys Experience Centre in Shivaji Nagar to explore our range of curtains and blinds. Bring your window measurements and our team will help you choose the right pieces for your space.

Our Experience Centre: https://maps.app.goo.gl/GptR7ZPZCRguLbYX7

Regards,
Hillarys Curtains & Blinds
```
*Handle with care:* a smaller requirement is still a real customer. The message offers a genuine, useful path (walk-in + measurements) rather than a brush-off — no mention of the threshold, no "your order is too small." (`voice-of-brand.md` §13 — no "budget," no "cheap.")

---

### L13 — Existing-customer inbound → menu re-entry
**Fires on:** A lead already in the system messages us again. The response is keyed to their current lead status. **First apply the smart-skip rule** — if their details are on file and only the slot is pending, go straight to the slot ask; don't re-run qualification.

**L13a — Status RNR / Call Back / Unable to Contact →** send the L5 re-engagement flow (pick a call-back window → confirm → qualify if needed).

**L13b — Status Appointment Booked:**
```
Hi {Name}, we can see your consultation with Hillarys is already scheduled.

If you'd like to make any changes or have a question before then, we're here to help. Please choose:
📅 Reschedule my appointment
👨‍💼 Talk to an expert
```
- **Reschedule →** "Thank you — we've noted your reschedule request. A team member will contact you shortly to find a new date and time that suits you." *(set follow-up + Notes)*
- **Talk to an expert →** "Thank you for reaching out. A member of our team will contact you shortly to help." *(set follow-up + Notes)*

**L13c — Status Site Not Ready – Future Requirement:**
```
Hi {Name}, thank you for reaching out — your enquiry is still open with us. Whenever you'd like to move forward, we're here. Please choose:
📅 Schedule a consultation
👨‍💼 Talk to an expert
```
- **Schedule a consultation →** the L6b reminder (pick a call-back window → confirm → close).
- **Talk to an expert →** the expert-callback confirmation above.

**L13d — Status Store Visit:**
```
Hi {Name}, thank you for reaching out. How can we help with your enquiry? Please choose:
🏠 Book a free home consultation
🏢 Reschedule my Experience Centre visit
📍 Experience Centre location
👨‍💼 Talk to an expert
```
- **Book a home consultation →** L6b reminder flow (call-back window → confirm → close).
- **Reschedule EC visit →** "We've noted your request to reschedule your Experience Centre visit. A team member will contact you shortly to arrange a new time."
- **EC location →** "Here's our Experience Centre: https://maps.app.goo.gl/GptR7ZPZCRguLbYX7 — we look forward to welcoming you. Anything else you need, just say the word."
- **Talk to an expert →** expert-callback confirmation.

**L13e — Status Not Interested / Less than ₹20K:**
```
Hi {Name}, thank you for reaching out. Would you like to speak with one of our experts about your enquiry?
👨‍💼 Talk to an expert
```
→ expert-callback confirmation.

**L13f — Any other inbound (no clear status):**
```
Hi {Name}, thank you for reaching out to Hillarys. Would you like to speak with one of our experts about your enquiry?
👨‍💼 Talk to an expert
```
→ expert-callback confirmation.

*Every L13 branch ends by setting the follow-up date and updating Notes (below).*

---

## Cross-cutting mechanics — the CRM rules behind the copy

These aren't messages; they're the operating rules that make the copy trustworthy. The Copy Studio references them so no draft contradicts them.

### The 30-minute follow-up rule
The moment a customer receives a "thank you / our team will connect shortly" message, the CRM **auto-sets the Follow-up Date & Time to the customer's response time + 30 minutes.** The assigned team member calls within that window. This is the promise behind "shortly" — if a message says the team will connect and no one calls for a day, the copy has lied. The 30-minute rule is what keeps every "shortly" honest.

### The running Notes summary
On every customer response, the CRM **updates the Notes with the option the customer selected** and maintains a **running summary of the whole interaction** — property type, window count, style, site readiness, timeline, chosen slots, and every reply. The next team member who opens the lead has full context and never asks the customer to repeat themselves. (This is the operational backbone of "we handle this so you don't have to" — the customer's information follows them; they don't carry it.)

### The smart-skip rule
Before sending any qualification message, the system **checks which required details are already collected:**
- Some details missing → ask **only** for the missing ones.
- All details collected, only the slot pending → send **only** the slot request, nothing else.
- Never ask for anything already provided.

This is a copy rule as much as a system rule: re-asking a question the customer already answered is the fastest way to make a premium brand feel like a call centre. When in doubt, the Copy Studio assumes the smart-skip is active and drafts the *shortest* honest next message.

---

## Development notes — where the Copy Studio takes the raw flow further

The operational flows above work. These are the elevations that make them *on-brand*, applied in the templates and recorded here so the reasoning is auditable. This is the "step further" — the difference between a functional bot script and the Hillarys voice.

| Raw operational phrasing | Why it needs work | Copy Studio elevation |
|---|---|---|
| "we require a few additional details" | Transactional — the details serve *our* records | "a few quick details help us prepare for your visit" — the ask serves *their* consultation (§7.2 Guide) |
| "Kindly …" (throughout) | On the rejection list (§7 — corporate) | "Please …" or drop entirely |
| "We tried reaching you earlier" (bare) | Can read as mild blame | "we couldn't get through — whenever it's convenient" — no guilt, all warmth |
| "Currently our services are available only within Bangalore" | Flat, closes the door | keep the fact, add the open door: "we're growing, and we'll let you know the moment we reach your city" |
| "you can visit … less than ₹20K" logic | Risk of making a small customer feel small | never name the threshold; offer a genuine, useful path (walk-in + measurements) |
| One message asking two things | Customer answers one, drops the other | strict **one question per message** in qualification |
| "Reply YES to continue" | Slightly botty, but functional | kept — it's a clear WhatsApp opt-in; softened the surrounding line so it doesn't feel like a gate |

**The through-line:** every pre-order elevation serves rule 1 of the doctrine — *guide, never gate.* The customer should finish the qualification flow feeling helped, not processed.

---

## Open decisions (for marketing review)

1. **Timeline option inconsistency.** Different flows offer different timeline sets (15/20/30/45/60/90 in some; 15/20/25/30/45/60 in others; the delay-trigger table covers 15–45). *Decision needed:* lock one canonical timeline set and one delay-trigger mapping across all branches, so the CRM logic and the copy never disagree.
2. **The 25-day gap.** The delay-trigger table jumps 20 → 25 → 30, but some timeline menus omit 25 days. *Confirm* whether 25 days is a live option; align the menu and the trigger table.
3. **"Reply YES" vs. no-friction start.** The YES opt-in adds a step. *Decide* whether it's worth the WhatsApp opt-in compliance value, or whether qualification should begin immediately after the pincode gate.
4. **Emoji in menus (L13).** The existing-customer menus use 📅 👨‍💼 🏠 🏢 📍 as option markers. *Confirm* the team is comfortable with icon-led menus here — they aid scannability, and this is the one place in the pre-order flow where menu clarity outranks emoji restraint.
5. **Toll-free consistency.** The number appears as `7795830298` (pre-order) and `+91-7795830298` (post-order T12). *Recommendation:* standardise the display format across both libraries.

---

## How the Copy Studio uses this file

- **A prospect, no order yet?** This is the file. (An existing paying customer's order-status question belongs to `crm-lifecycle-triggers.md`; a complaint belongs to `service-recovery-system.md`.)
- **Drafting a message for a lead state these triggers don't cover?** Compose in the anatomy — warm opener → one clear ask/answer → scannable options → sign-off — obey the three doctrine rules (guide-not-gate, honesty-over-capture, no-silence), and respect the smart-skip and 30-minute-follow-up rules.
- **Serviceability, budget-fit, or readiness is in question?** Default to the honest branch (L2c out-of-area, L11 not-interested, L12 below-threshold, L4 not-ready). An honest "not yet / not us" is on-brand; a captured-but-can't-honour lead is not.
- **Reviewing a proposed pre-order message?** Run `SKILL.md` §7. A lead message additionally fails if it: stacks two questions, re-asks a collected detail, uses "kindly," names a budget threshold to the customer, blames the customer for a missed call, promises a callback with no owner behind the 30-minute rule, or pressures a "no."

---

## Cross-references

- `crm-lifecycle-triggers.md` — the post-order half; picks the customer up at order confirmation, where this file's consultation-to-order seam ends.
- `voice-of-brand.md` — §7.2 Guide, §7.1 Simplify, §9 Discovery & Consultation language, §13 words we avoid (budget/cheap), §14 CRM & WhatsApp tone, §16 referral restraint.
- `experience-state-map.md` — the prospect's emotional state through Discovery and Consultation.
- `service-brand-playbook.md` — Moment 1 (The Bell Ring) and Moment 2 (The Swatch Unrolling) are the consultation this file books; the pre-order voice sets up those moments.
- `service-recovery-system.md` — when a booked consultation is missed, cancelled, or goes wrong, recovery takes over.
- `communication-surface-map.md` — WhatsApp as the pre-sale guidance layer.

---

*End of file. Living document — revise as lead sources, statuses, and the CRM's follow-up logic evolve, and as the open decisions are resolved.*
