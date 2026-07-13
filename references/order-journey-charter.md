# The Order Journey Charter — The Customer-Facing Source of Truth
Version: 1.0
Status: Canonical fact base (primary source, customer-facing)
Owner: Hillarys India — Operations / Customer Service
Source: **"Your Order Journey — From consultation to installation"**, the Hillarys-branded leaflet handed to every customer. The document itself ships with this skill at `references/order-journey-leaflet.pdf`.
Companion files: `crm-lifecycle-triggers.md` (the post-order WhatsApp messages this journey is narrated by), `lead-lifecycle-triggers.md` (the pre-order half), `service-brand-playbook.md` (the six moments the journey passes through).

---

## What this is, and why it exists

Every other file in this skill governs **how we say things** — voice, matrix, choreography, template anatomy. This file governs **what is true**.

"Your Order Journey" is the leaflet the customer holds in their hand. It is the company, in its own words, telling the customer the map, the money, the owners, the rules, and the promise. It is the one artifact in the whole relationship that the customer can point back to and say *"but you told me…"*.

That makes it the **source of truth**. Every WhatsApp trigger, every consultation script, every quotation note, every service-recovery message must stay consistent with what this leaflet already told the customer. A message that is beautifully on-voice but **contradicts the leaflet** is not on-brand — it is a broken promise wearing good copy.

**This is the second half of the trust equation.** The Silence After Advance (Playbook Moment 4) is the risk that we say *nothing*. The risk this file defends against is that we say something *different* — the leaflet promises "15 working days from check-measurement," a message implies 15 calendar days from order, and the gap becomes a complaint. Consistency between the leaflet and every downstream word **is** trust continuity. That is how this file makes the flywheel come together: it is the fact-check layer the rest of the studio drafts against.

> **The test this file adds to every draft:** does this contradict anything the customer was already told in the leaflet — a percentage, a timeline, an owner, a rule? If yes, the draft is wrong, however good it reads. Match the Charter first, then make it sing.

---

## The eight stages of the order journey

The leaflet lays the whole journey out for the customer as eight numbered stages, each with a named **Owner**. This is the map the customer is working from — the CRM lifecycle messages narrate it.

| # | Stage | What it means (customer-facing) | Owner (per leaflet) |
|---|---|---|---|
| 1 | **Home Consultation** | The Design Consultant visited with fabric and style samples, took measurements, and helped select fabric, design and colour. | Design Consultant |
| 2 | **Quotation Shared** | An **indicative** quotation (approx. **90–95% accurate**, based on preliminary dimensions), valid **15 days** from issue. | Design Consultant |
| 3 | **Price & Discount Freeze** | A **token advance of 5% of order value or ₹5,000, whichever is higher**, freezes the price version and the discount agreed at quotation. **Does not yet process the order or begin procurement.** | Design Consultant / ASM |
| 4 | **50% Advance — Order Processed** | Payment of **50% of order value** processes the order and schedules the check-measurement visit. **Fabric (curtains, Roman blinds) is ordered the same day. Other blinds and hardware/components are ordered only after check-measurement confirms final specs.** No changes are accepted once this payment is made. | DC / ASM / CSR / Measurement Technician (MMT) |
| 5 | **Manufacturing** | Products are custom made-to-measure. **Standard timeline: 15 working days from check-measurement**, subject to fabric availability (**longer for motorised / imported fabric** — the customer is informed). | CSR / CRM |
| 6 | **Ready for Dispatch** | Once products are ready, the **balance 50%** is collected and installation is scheduled at the customer's convenience. | CSR / CRM |
| 7 | **Installation** | The installation team fits the products at site. The site (civil, electrical, access) must be ready to avoid a **chargeable re-visit**. | CSR / Installation Manager |
| 8 | **After-Care & Warranty** | Report any manufacturing defect or shipping damage **within 48 hours, with photos**. The product is backed by warranty **against manufacturing defects**. | Customer Service |

**Note the seam.** The leaflet is written from the point at which the customer is already at stage 3 ("YOU ARE HERE" in the reference copy) — i.e. the *order side*. Stages 1–2 are the consultation the pre-order lead journey books (`lead-lifecycle-triggers.md`); stages 3–8 are what the post-order CRM library narrates (`crm-lifecycle-triggers.md`).

---

## The payment schedule — the biggest fact to get right

The leaflet is explicit that payment happens in **three stages**, not two. This is the single most important reconciliation this Charter makes, because the CRM lifecycle library currently opens at the 50% advance and does not narrate the token freeze.

| Stage | Amount | What it does | Does **not** do |
|---|---|---|---|
| **Token — Price Freeze** | **5% or ₹5,000, whichever is higher** | Freezes the price version and the discount % agreed at quotation. | Does **not** process the order; does **not** begin procurement. |
| **Total Advance** | **50% of order value** | Processes the order, schedules the check-measurement, and starts procurement (fabric for curtains / Roman blinds same day; other blinds & components after check-measurement). | — |
| **Balance** | **50%** | Payable when the products are ready for dispatch. | — |

**Rules the copy must carry at the right moment:**
- The **token freeze does not process the order** — never imply it does. It buys the customer time at a locked price and discount; procurement waits for the 50%.
- **Procurement is split, not blanket.** Only curtains and Roman-blind *fabric* is ordered the same day as the 50%. Other blinds, hardware and components are ordered **after** check-measurement confirms final specs. Any "everything is being ordered today" line is factually too broad (see Open Decision #1 on CRM Trigger 1).
- **Once 50% is paid, the order cannot be cancelled, refunded or changed.** Change requests must be shared with the DC / ASM / CSR **at the time of payment**. This is a hard rule — copy must not soften it into "changes may be possible."

---

## The facts the copy must never contradict

Pulled verbatim in substance from the leaflet's "Good to Know" and payment sections. Treat these as fixed unless Operations revises the leaflet.

**Quotation & price**
- The consultation quotation is **indicative, ~90–95% accurate**, based on preliminary dimensions.
- It is **valid 15 days** from issue; pricing may be revised beyond that.
- **Final price is confirmed only after the check-measurement visit.**

**Timeline**
- Manufacturing standard is **15 working days from check-measurement** — *working* days, anchored to check-measure, **not** calendar days from order.
- **Longer for motorised / imported fabric**; the customer is told when this applies.
- → This is the true number behind the skill's rule against promising "15-day delivery" in marketing (`SKILL.md` §8). Marketing copy still avoids a bare "15 days," because a prospect reads it as 15 calendar days from *order*; the honest internal fact is "15 working days from check-measurement (~3 weeks calendar)."

**Site readiness & installation**
- **One installation visit is included** in the order value.
- If the site isn't ready or access isn't available, a **re-visit is chargeable**.
- Civil, electrical and access work must be complete **before** the installation date.
- The customer **inspects at installation and signs the acknowledgement**.

**After-care & warranty**
- Report any **defect or damage within 48 hours, with photographs**, to **orders@hillarys.co.in**.
- Warranty **covers manufacturing defects only** — see full Terms & Conditions on the quote.

---

## Who to reach — the owner roster and escalation matrix

The skill's standing rule is *"every customer-facing message names a person and a next step"* (`SKILL.md` §2, §6). This leaflet is where those names come from. Use it as the roster when a draft needs to name an owner or route an escalation.

| Level | Stage / concern | Contact | When to use |
|---|---|---|---|
| **Level 1** | Consultation, quote, fabric/design changes | **Design Consultant** | First point of contact for anything pre-installation |
| **Level 1** | Check-measurement scheduling | **CSR / Measurement Technician (MMT)** | Confirming or rescheduling the measurement visit |
| **Level 1** | Production & dispatch status | **CSR / CRM** | Order tracking after production begins |
| **Level 1** | Installation scheduling & fitting | **CSR / Installation Manager** | Scheduling, site readiness, fitting day |
| **Level 2** | Unresolved query, pricing / discount approval | **Assistant Sales Manager / Sales Manager (ASM)** | If Level 1 hasn't resolved it within a reasonable time |
| **Level 3** | Escalations, warranty claims, complaints | **Customer Service** — orders@hillarys.co.in / **090082 81888** | Formal escalation or written complaint |

**Escalation etiquette for the Copy Studio:** when a service-recovery draft routes a customer upward, it names the *next* level, never dead-ends. "I'm escalating this to our Sales Manager, [name], who will call you by [time]" — a person and a time, per `service-recovery-system.md`.

**Two support numbers exist — do not use them interchangeably** (see Open Decision #3):
- **090082 81888** — the leaflet's Customer Service / escalation line (orders@hillarys.co.in).
- **+91-7795830298** — the Toll-Free line used in CRM Trigger 12 and the lead-lifecycle support number.

---

## The Commitment — the brand promise, in the company's own words

The leaflet closes with three commitments. These are not the Copy Studio's interpretation of the promise — they are the **primary source** the "we handle this so you don't have to" doctrine is built on. Quote them; hold copy to them.

> **We'll keep you informed at every stage — you shouldn't have to chase us for status updates.**
> **Every person who visits your home will be introduced to you in advance, by name.**
> Full Terms & Conditions are available on your Quote, Sign-Off and Tax Invoice documents.

The first line is the charter for the entire CRM lifecycle library — the anti-silence mandate, in writing, given to the customer. The second is the source of the skill's ownership-visibility rule and of the CRM triggers' "installer messages 15 minutes before arriving" promise. When you need to *prove* to a colleague why a message must name a person, cite this line — the customer was promised it on paper.

---

## How the Charter maps to the WhatsApp lifecycle

The leaflet is the map; the CRM triggers are the voice walking the customer through it. This is the alignment — read it before editing any lifecycle message so a wording change never drifts from what the leaflet states.

| Leaflet stage | Post-order trigger(s) (`crm-lifecycle-triggers.md`) | Consistency to hold |
|---|---|---|
| 1 Home Consultation | *(pre-order)* — booked by `lead-lifecycle-triggers.md` | The consultation is where fabric/design/colour is chosen. |
| 2 Quotation Shared | — indicative quote at consultation | Indicative, ~90–95%, valid 15 days. Distinct from the **final** quote below. |
| 3 Price & Discount Freeze | *(not yet narrated — see Open Decision #2)* | 5%/₹5,000 token; freezes price + discount; does **not** process the order. |
| 4 50% Advance — Order Processed | **T1** `order_confirmed` | 50% processes the order + schedules check-measure. Procurement is **split** (see Open Decision #1). No changes after 50%. |
| — Check-measurement | **T2** `cm_scheduled`, **T3** `cm_completed` | Scheduled by the 50% payment; the foundation of the final price. |
| — Final quotation / SOW | **T4** `quotation_sent`, **T5** `order_approved` | **Final** price confirmed only after check-measure. |
| 5 Manufacturing | **T6** `crafting_started`, **T7** `stitching_qc` | 15 **working** days from **check-measure**; longer for motorised/imported. |
| 6 Ready for Dispatch | **T8** `ready_balance_due`, **T9** `payment_received`, **T10** `dispatched` | Balance 50% collected when ready; then dispatch. |
| 7 Installation | **T11** `install_scheduled` | One visit included; re-visit chargeable if site not ready; installer named + messages 15 min before. |
| 8 After-Care & Warranty | **T12** `install_completed` | Toll-free support; 48-hour defect window; warranty = manufacturing defects only. |

---

## How the Copy Studio uses this file

- **Before stating a fact, check it here.** Any percentage, amount, timeline, owner, or rule in a draft must match this Charter. When it doesn't, the Charter wins and the draft is corrected — not the other way around.
- **When a draft needs to name an owner or route an escalation,** pull the name from the roster above rather than inventing "our team."
- **When you must write a status the 12 triggers don't cover** (delay, reschedule, partial dispatch, cancellation request), the Charter tells you what's *true* about that situation — e.g. that changes aren't accepted after 50%, that a re-visit is chargeable, that motorised fabric runs longer — so the message is honest as well as on-voice. Then compose in the CRM anatomy (status → craft line → numbered NEXT STEPS → named owner).
- **When editing a lifecycle message,** run it against the mapping table above so a wording change never contradicts the leaflet the customer already has.
- **This file states facts, not voice.** It never overrides `voice-of-brand.md` on *how* to say something — only on *what* is true. A fact from here still gets said in the Hillarys voice.

---

## Open decisions (for Operations & Marketing to close)

These are the drifts this Charter surfaces between the customer-facing leaflet and the current skill. Each is flagged, not silently resolved — closing them is a business call.

1. **CRM Trigger 1's procurement line is too broad.** T1 says *"all fabrics for your order are being procured today, so fabric selections can't be changed after this point."* The leaflet is narrower: only curtains / Roman-blind **fabric** is ordered same-day; other blinds, hardware and components are ordered **after check-measurement**. And the real hard rule is broader than fabric: *no changes at all* once 50% is paid. *Recommendation:* revise T1 to reflect both — lock fabric selection **and** state that the order can't be changed after the 50%, without claiming everything is ordered today. Keep the framing as care, not restriction.

2. **The 5% / ₹5,000 token freeze is not narrated in WhatsApp.** The CRM library opens at the 50% advance (T1); the token freeze (leaflet stage 3) has no message. *Decision needed:* does the token step warrant its own trigger (e.g. `price_frozen` — confirm the freeze, name what it does and doesn't do, set expectations for the 50%)? It is the customer's first payment and currently a silent step. *Recommendation:* add one, in the standard anatomy — it is exactly the kind of silence this skill exists to fill.

3. **Two support numbers.** The leaflet's Customer Service line is **090082 81888**; the CRM Toll-Free (T12) and lead-lifecycle support number is **+91-7795830298**. *Decision needed:* confirm which is canonical for which purpose (general support vs. escalation), or consolidate. Until then, use each in its documented context and do not swap them.

4. **Timeline wording across surfaces.** Internally the true figure is "15 working days from check-measurement." Marketing copy avoids a bare "15 days" (a prospect misreads it as calendar-days-from-order, the exact over-promise `SKILL.md` §8 refuses). *Confirm* the approved public phrasing — e.g. "made to measure in about three weeks" — so lifecycle, sales, and marketing all say the same true thing in the same safe way.

---

## Cross-references

- `crm-lifecycle-triggers.md` — the 12 post-order WhatsApp messages that narrate stages 4–8 of this journey.
- `lead-lifecycle-triggers.md` — the pre-order half that books stage 1 (the consultation).
- `service-brand-playbook.md` — the six moments the journey passes through (The Quote, The Silence After Advance, The Installer Arriving, The Last Ten Feet).
- `service-recovery-system.md` — invoked when a fact in this Charter is breached (missed timeline, chargeable re-visit dispute, defect claim).
- `voice-of-brand.md` — governs *how* every fact in this Charter is said.
- `experience-state-map.md` — the emotional state the customer is in at each stage.

---

*End of file. Living document — revise whenever the customer-facing leaflet is updated, and re-check the mapping table and open decisions against the lifecycle libraries when it is.*
