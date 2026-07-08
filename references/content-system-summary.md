# Hillarys Content System — Conversation Summary

> Working document capturing everything decided, produced, or parked
> across this session. For Siva, Harshita, Koushin, Sujoy, Sai.
>
> Source documents: `content-framework.html` v1.1, `hillarys-content-os-prd-v1.1.docx`,
> Governance Runtime v4 (CLAUDE.md, COMPLIANCE.md, MANIFEST.md, MEMORY.md, etc.)
>
> Date: April 2026
> Version: 1.0

---

## 1. The Brief (from Siva's email)

The email Siva sent to Harshita, Koushin, and Sujoy (with Sai cc'd for IT access)
laid out two tracks of work:

**Track A — Content plan (Harshita + Sujoy, with Koushin advising)**
- Prepare a 90-day plan on inventory required × cost based on actual requirements
- Koushin to add value on transforming 10 pieces to 100 using AI tools
- Sujoy to retrieve the Hillarys UK content library from LWYD and consolidate
- Knowledge share of all existing content as the first step

**Track B — Tool build (Koushin, if interest exists)**
1. Vercel front end with live-adjustable Relevancy / Quality / Availability sliders
   giving directional guidance for the next 90 days
2. Supabase backend for content storage
3. Tagged storage after upload (image / video / source)
4. Auto-resize tool per channel/surface with download
5. Connect database to AI tool (e.g. Veo); store outputs
6. Rank outputs so they sit in usage containers
7. Figma MCP for real-time editing + copy
8. Copy library tied to brand voice + value prop + brand guidelines for on-the-fly generation
9. Use Sai's details for Claude Max subscription access

---

## 2. Inputs Gathered During the Session

A series of clarifying questions, with the answers recorded:

| # | Question | Answer |
|---|----------|--------|
| Q1 | What to produce? | Both — plan first, then tool scope |
| Q2 | Monthly volume per channel | Higher than PRD placeholders — pushing harder on Social + Perf |
| Q3 | Budget ceiling for 90 days | ₹3–5L (capex + opex combined) |
| Q4 | Who's executing | Harshita + Koushin co-producing |
| Q5 | HD library state | Deep across Global + India + LWYD-UK |
| Q6 | Copy Studio priority order | Social → Performance → Website → Physical+Email |
| Q7 | HILLARYS.md status | Skeleton exists; build a draft as Week 1 deliverable |
| Q8 | Reframe to "system not 90-day plan"? | Yes |
| Q9 | Deliverable format for the system | Live interactive dashboard |
| Q10 | Primary reader | Siva (needs to approve) |

---

## 3. Deliverables Produced

### 3.1 `hillarys-90-day-content-plan.docx` *(superseded)*

Word document, formal plan written for circulation. Contents:

- Cover + executive summary
- Starting inventory audit (RAG status per source)
- Target monthly volumes per channel
- Koushin's multiplication layer (10 → 100 workflows)
- Three-phase budget with line items
- Week-by-week rundown for 13 weeks
- Success metrics at Day 90
- Risks + dependencies
- Tool build scope (Part 2)
- Immediate next steps

**Status: superseded** by the system dashboard. Kept as the source for content
inside the dashboard but no longer the primary deliverable.

### 3.2 `hillarys-content-system.html` *(current primary deliverable)*

Interactive single-page dashboard. Nine views accessible from a sidebar:

1. **Stack overview** — the four-layer picture
2. **Decisions needed** — 6 approval checkboxes for Siva
3. **L1 Governance runtime** — how the tool gets built (CLAUDE.md, 24 commands, rule tiers)
4. **L2 Content framework** — 7 sources, 4 recipes, leverage ladder
5. **L3 Content OS tool** — 6 features, 9-table schema, 3-milestone build
6. **L4 Operating rhythm** — 90-day rotation + weekly/monthly cadence
7. **Budget simulator** — 10 live sliders against ₹5L ceiling
8. **90-day gantt** — workstreams W1–W13 with decision gates
9. **Team + handoffs** — RACI + 4 critical handoff points

---

## 4. The System Shape (Core Architectural Decision)

Hillarys runs on a **four-layer stack**, not a one-off 90-day project. Each layer
answers a different question; they only make sense together.

```
┌──────────────────────────────────────────────────┐
│  L1 · GOVERNANCE RUNTIME                          │  ← How the tool is built
│  CLAUDE.md, COMPLIANCE.md, 24 commands           │     (Koushin)
│  Sprints · TDD · cognitive modes · compliance    │
└──────────────────────────────────────────────────┘
                    ↓ governs how we build
┌──────────────────────────────────────────────────┐
│  L2 · CONTENT FRAMEWORK                           │  ← The fixed rules
│  7 sources · 4 channel recipes · leverage ladder │     (Siva owns values)
│  Non-negotiable; encoded in the tool as config   │
└──────────────────────────────────────────────────┘
                    ↓ encoded as config in
┌──────────────────────────────────────────────────┐
│  L3 · CONTENT OS TOOL                             │  ← The software
│  PRD v1.1 · Next.js + Supabase + Vercel          │     (Koushin builds)
│  6 features · 9 tables                           │
└──────────────────────────────────────────────────┘
                    ↓ runs the daily work of
┌──────────────────────────────────────────────────┐
│  L4 · OPERATING RHYTHM                            │  ← Weekly cadence
│  90-day plan (Q1 2026) · monthly reviews         │     (Harshita operates)
│  Quarterly resets                                │
└──────────────────────────────────────────────────┘
```

**Implication:** the 90-day plan stops being the deliverable. It becomes the
first quarterly rotation of the operating layer. The framework + tool + governance
runtime stay in place indefinitely; only the operating rhythm rotates.

---

## 5. The Six Decisions Needed from Siva

These are tracked in the dashboard's approval view. All six need to clear before
the system goes live.

| ID | Decision | Status |
|----|----------|--------|
| D1 | **System shape** — four-layer stack as the architectural commitment | Pending |
| D2 | **Tool build path** — adopt PRD v1.1; defer to Week 11 gate; ~₹4L build if approved | Pending |
| D3 | **First operating window** — 90-day plan as Q1 2026 rotation, ~₹4.35L | Pending |
| D4 | **Team RACI** — Harshita operates, Koushin builds + trains AI, Sujoy audits, Sai admin | Pending |
| D5 | **HD boundary** — Hunter Douglas India is a source, not a brand surface | Pending |
| D6 | **Cadence** — Monday gap dash, Friday voice review, monthly stakeholder, quarterly reset | Pending |

---

## 6. The 90-Day Plan (Layer 4, First Rotation)

### 6.1 Phase structure

| Phase | Weeks | Theme | Budget |
|-------|-------|-------|--------|
| 1 | 1–2 | Stop the bleed (gimbal + Drops folder + HILLARYS.md v0.1) | ~₹35.5K |
| 2 | 3–8 | Harvest WhatsApp corpus + paid UGC engine | ~₹1.52L |
| 3 | 8–13 | AI creative direction (Veo / Sora / Runway training) | ~₹2.13L |
| — | — | Contingency (~8%) | ~₹35K |
| | | **Total** | **₹4.35L** |

### 6.2 Target monthly volumes

Volumes pushed higher than PRD placeholders per owner direction:

| Channel | Volume / mo | HD library | Gimbal/UGC | AI std | AI advanced | Own shoots |
|---------|-------------|------------|------------|--------|-------------|------------|
| Social | 90 | 9 | 27 | 45 | 9 | — |
| Performance | 50 variants | 25 | 15 | 5 | 5 | — |
| Website | 10 refreshes | 7 | — | 1 | — | 2 |
| Physical | 4 | 4 | — | — | — | — |
| Email | 15 copy | — | — | — | — | — |
| **Total** | **154 + copy** | 45 | 42 | 51 | 14 | 2 |

### 6.3 Starting inventory verdict

| Source | State | Action |
|--------|-------|--------|
| HD library (Global + India + LWYD-UK) | GREEN — deep | Hold. Tag + catalogue. |
| Own pro shoots | AMBER — thin | Skip in 90 days |
| Mobile + gimbal | RED — empty | **Week 1 fix** |
| Mobile raw (WhatsApp) | AMBER — abundant, unused | **Week 2 harvest** (hidden asset) |
| AI standard | GREEN — adequate | Hold |
| AI advanced (Tier-★) | RED — no capability | Month 2–3 training |
| Install + BTS | RED — non-existent | Installer SOP week 1 |

### 6.4 The 10 → 100 multiplication engine (Koushin)

| 1 input | Tool | Transformation | Outputs |
|---------|------|----------------|---------|
| HD library hero | Runway / Kling | Image → 5-sec motion | 3 |
| Product shot | Midjourney / Flux | Style transfer, 5 rooms | 5 |
| Testimonial video | Descript / CapCut | Clip → 6 vertical cuts | 6 |
| Install B-roll | Premiere + AI color | Polish, before/after | 2–3 |
| Veo hero prompt | Veo 3 / Sora | Scene + 5 variants | 6 |
| Copy brief | Claude Sonnet 4.5 | Voice-locked variants | 6 |
| **10 inputs** | Mixed stack | Composite pipeline | **≈ 100** |

### 6.5 Things explicitly NOT in the 90 days

- No India professional shoot (HD library covers Physical + Website; AI-advanced will eat own-shoot category)
- No tool engineering build until Week 11 gate decision
- No new hires (run with 5-person team)
- No HD India brand surface activation
- No Figma MCP integration (v2 candidate)

---

## 7. The Tool Build (Layer 3) — Decision Architecture

### 7.1 Recommendation: defer to Week 11

Run the first 90 days on **Drive + spreadsheet + Claude Project** instead of
building the tool immediately. Revisit at Week 11 with real usage data.

### 7.2 What we run on for the 90 days

- **Drops folder** on Google Drive, channel-tagged subfolders
- **Inventory spreadsheet** tracking source × channel × weeks-of-cover (same logic as PRD gap engine, manual refresh)
- **Claude Project as Copy Studio** with HILLARYS.md + framework + recent approved posts as project knowledge (Sai activates Max subscription seats)
- **Cloudinary free tier** for resize-on-demand via URL transforms

### 7.3 When to green-light the tool (Week 11 decision gate)

Build if **any** of these are true:
- Harshita spends >4 hrs/week on inventory tracking or asset hunting
- Catalogue exceeds 500 tagged assets and Drive search stops scaling
- Copy Studio usage exceeds 40 generations/week
- Hillarys decides to hire a second associate (multi-user becomes real)
- Paid media spend grows and creative-variant velocity becomes the gating factor

### 7.4 If approved at Week 11 — staged build (8 weeks, ~₹4L)

| Milestone | Duration | Cost | Scope |
|-----------|----------|------|-------|
| A | 4 wks | ~₹2L | F1 Asset Library + F2 Channel views + F4 Resize — replaces the spreadsheet |
| B | 2 wks | ~₹1L | F3 Gap Engine + F5 Brand Voice ingestion |
| C | 2 wks | ~₹1L | F6 Copy Studio (built last, with 8+ weeks of prompt iteration learned from the Claude Project) |

Stack per PRD §8: Next.js 15 + Supabase + Vercel + Cloudinary + Anthropic API (Claude Sonnet 4.5 behind provider abstraction).

---

## 8. The Content Framework (Layer 2) — Reference

### 8.1 The 7 sources (fixed rubric values)

| Source | Quality | Relevance |
|--------|---------|-----------|
| AI — advanced (Tier-★) | 90% | 80% |
| HD library | 80% | 40% |
| Own pro shoots | 70% | 10% |
| AI — standard | 70% | 50% |
| Mobile + gimbal | 50% | 70% |
| Mobile — raw | 10% | 70% |

### 8.2 The 4 channel recipes (locked)

| Channel | Form | Recipe |
|---------|------|--------|
| **Social** | Dynamic-first | 60% AI / 30% mobile+gimbal / 10% HD library |
| **Performance** | Mixed | 50% HD library / 30% UGC+mobile / 20% AI |
| **Website** | Static-first | 70% HD library / 20% own shoots / 10% AI |
| **Physical** | Static | 100% HD library |
| Email | Copy-only | (no visual recipe — Copy Studio only) |

### 8.3 The leverage ladder

| Rung | What | Quality change |
|------|------|----------------|
| 1× Baseline | Phone, handheld, available light | — |
| 10× Stabilise | Gimbal/tripod, good light, clean frame | 10% → 50% |
| 100× Direct | Storyboard, model, colour grade, sound | 50% → 70% |
| 1000× AI compound | Veo/Sora/Runway with consistent character, variants at scale | → 90% at 10–50× lower cost |

---

## 9. The Governance Runtime (Layer 1) — Reference

### 9.1 The flow

`INTENT → PLAN → TEST → IMPLEMENT → PROOF → COMMIT → DONE`

Every piece of work in the tool build follows this. Skipping a step = work is invalid.

### 9.2 Three rule tiers

| Tier | Name | Override? | Examples |
|------|------|-----------|----------|
| T1 | **Iron** | Never | Intent before code, test-first, main branch protection, root cause before fix |
| T2 | **Steel** | With expiry | Four-tier test gates, architect review, design system enforcement, conventional commits |
| T3 | **Copper** | Tracked, not blocked | Office hours, weekly retro, completeness over shortcuts |

### 9.3 Why this matters for Hillarys

When Koushin builds the Content OS, he runs `/prd`, then `/conductor`, then `/dev`
per milestone. TDD is non-negotiable. The evidence chain means Harshita inherits
a documented, tested, reviewable system — not a black box only Koushin understands.

---

## 10. Team & RACI

| Person | Role | Owns |
|--------|------|------|
| **Siva Subramaniam** | Country Head · Approver | Framework values, budget, HILLARYS.md sign-off, quarterly resets |
| **Harshita Vishwas** | Marketing Associate · Operator | Daily ops, Drops harvest, UGC sourcing, gap dashboard |
| **Koushin Roy** (HD India) | Content Advisor · Builder | AI creative direction, multiplication engine, Content OS build if gated |
| **Sujoy Sinha** | Strategy · Advisor | HD library audit (Global + India + LWYD-UK), tagging schema, UGC release template |
| **Sai Datta** (Hillarys IT) | Platform Admin | Claude Max seats, Drops folder, Supabase/Vercel when tool ships |

### 10.1 Critical handoffs

1. **H1 — Library → Harshita (Week 2):** Sujoy delivers tagged catalogue v1. Harshita confirms search <10s.
2. **H2 — HILLARYS.md → Copy Studio (weekly):** Siva + Harshita maintain. Every rejected generation feeds next version.
3. **H3 — Koushin → Harshita skills (Week 10+):** AI workflows documented + taught. By Day 90 Harshita runs the multiplication engine.
4. **H4 — Week 11 gate → build:** Siva + Koushin decide commission vs another quarter on spreadsheet.

---

## 11. Cadence (runs forever, not just 90 days)

| When | What | Time |
|------|------|------|
| Monday | Harshita posts gap dashboard to Siva | 15 min |
| Wednesday | WhatsApp → Drops harvest | 30 min |
| Friday | Siva + Harshita HILLARYS.md review | 15 min |
| 1st Monday monthly | Full stakeholder review (all 4) | 30 min |
| Quarterly | 90-day retrospective + next rotation | half day |

---

## 12. Risks + Mitigations

| Risk | Mitigation |
|------|------------|
| Single-operator (Harshita is sole exec) | Drops folder + HILLARYS.md + Claude Project make ops paper-portable from Week 3 |
| Koushin availability (HD India day job) | ₹50K consultant budget as insurance for Weeks 8–9 intensive |
| AI tool churn (Veo/Sora pricing/access shifts) | Abstracted tooling budget; Runway + MJ + Kling as backstops |
| UGC rights + approvals | Sujoy drafts 1-page release form Week 3 |
| Brand voice drift | Weekly 15-min HILLARYS.md review with Siva |
| HD India boundary | Koushin + Siva align Week 2; HD brand activation is v2 |

---

## 13. Success Metrics at Day 90

**Inventory health (from gap engine logic, PRD §6):**
- Social runway ≥ 8 weeks (green)
- Performance runway ≥ 6 weeks, UGC bank ≥ 30 pieces
- Website ≥ 12 weeks (green) — HD-driven
- Physical ≥ 24 weeks (green) — HD-driven
- Source-mix drift <10% from recipe on all channels

**Operational health:**
- WhatsApp → Drops harvest runs weekly without reminder by Week 8
- HILLARYS.md at v1.1+ with iteration log
- Copy Studio: approved first-try ≥ 60% of generations
- Koushin: ≥ 10 Veo/Sora hero assets + 50 variants
- AI-advanced per-asset cost ≤ ₹1,000 by Week 10

---

## 14. Open Questions (to close before Week 11)

From PRD §10.1 and emerged during this session:

- [ ] Confirm monthly visual burn rates per channel (current numbers are scaled-up placeholders)
- [ ] Confirm monthly copy burn rates per channel + use case
- [ ] Confirm ai_advanced and ai_standard relevance percentages
- [ ] Confirm complete surface list per channel (PRD §5.1 is draft)
- [ ] Confirm copy format constraints per use case (§5.2 is draft, pending HILLARYS.md)
- [ ] Confirm asset retention policy (when to archive, expired-rights flow)
- [ ] Confirm monthly LLM budget cap (PRD default ₹2K — likely too low at real volume)
- [ ] Confirm: one brand voice file, or does HD India need its own even in v1?
- [ ] Does the tool become a multi-brand system later (Hillarys + HD India)?
- [ ] Who owns the tool post-launch — Harshita, Koushin, or a new hire?

---

## 15. v2 Candidates (parked, not in v1)

From PRD §10.2 — architecture must not preclude these:

- AI image / video generation inside the tool (Veo, MJ, Runway) with approval queue
- Image-aware copy generation ("generate caption for this image")
- Auto-tagging of visual assets via vision models on upload
- Multi-brand support (Hillarys + HD India as separate channel sets)
- Role-based access (agency, freelancer uploads)
- Auto-learning burn rates from consumption patterns
- Asset performance feedback loop (paid media winners → Copy Studio as few-shot examples)
- Campaign-level groupings + approval workflows
- Figma plugin: push approved copy + images directly to a Figma file
- A/B testing hooks (matched pairs + performance flowback)

---

## 16. Immediate Next Steps (within 48 hours of Siva's sign-off)

| Owner | Action |
|-------|--------|
| **Siva** | Circulate the dashboard to Harshita, Koushin, Sujoy. Schedule 30-min kickoff. |
| **Harshita** | Order 2× DJI Osmo Mobile gimbals (~₹30K). |
| **Sai** | Add Harshita + Koushin to Claude Max team. Create shared Claude Project shell. |
| **Sujoy** | Confirm HD library audit scope + tagging schema. Begin retrieval from LWYD. |
| **Koushin** | Confirm Weeks 8–9 training calendar block. Identify AI consultant shortlist. |
| **Siva + Harshita** | Draft HILLARYS.md v0.1 (brand voice, tone rules, 10 do's / 10 don'ts, 6 sample lines per channel). |

---

## 17. Files in the Workstream

| File | Purpose | Status |
|------|---------|--------|
| `content-framework.html` | Layer 2 source of truth | Stable (v1.1) |
| `hillarys-content-os-prd-v1.1.docx` | Layer 3 build brief | Stable (v1.1) |
| Governance Runtime v4 (CLAUDE.md, COMPLIANCE.md, etc.) | Layer 1 build method | Stable (v4) |
| `hillarys-90-day-content-plan.docx` | First-pass Word deliverable | Superseded |
| `hillarys-content-system.html` | Primary deliverable (interactive) | **Current** |
| `hillarys-content-system-summary.md` (this file) | Conversation summary | **Current** |
| `HILLARYS.md` (brand voice) | Layer 3 input — feeds Copy Studio | **Week 1 deliverable** |

---

## 18. Closing Note

> "The framework is the decision. You execute it. If an asset doesn't fit the
> recipe, it doesn't ship — no matter how good it looks in isolation."

The same logic applies to the system. The four layers are the decision.
Each layer has a clear owner and a clear question it answers.
Quarterly we revisit the operating rhythm; the rest stays in place.

The 90-day plan starts the moment Siva ticks all 6 boxes on the approval dashboard.

*— end of summary —*
