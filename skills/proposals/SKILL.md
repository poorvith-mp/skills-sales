---
name: proposals
last_reviewed: 2026-09-06
group: Pipeline
description: >-
  Turn an RFP or opportunity into a win narrative with scope, pricing, timeline, win themes and
  proof. Use when writing formal sales proposals, Statements of Work, or executive pitches.
---

# Proposals

A winning proposal is not a capabilities brochure; it is an executive business case. High-conversion proposals lead with the client's quantifiable problem, establish 2–3 distinct win themes, define rigid Statement of Work (SOW) boundaries, and back every capability claim with verified proof.

## 1. The Win Narrative Architecture

Structure formal proposals and RFP responses into four distinct decision layers:

### A. Executive Pitch & Problem Statement
- **Quantified Current State**: Document the financial or operational cost of the client's current bottleneck (e.g. "manual reconciliation consumes 35 hours/week, introducing a 4.2% error rate across $12M in transactions").
- **Target State & Business Outcomes**: State the measurable impact delivered upon completion (e.g. "automated ledger synchronization reducing error rate to <0.1% and saving $180,000 annually").
- **Win Themes**: 2–3 strategic pillars that distinguish your bid (e.g. Speed-to-value within 30 days; Proven SOC 2 Type II compliance; Zero operational downtime).

### B. Statement of Work (SOW) & Milestone Deliverables
Break implementation into discrete, inspectable milestone phases:
- **Phase 1: Discovery & Technical Scoping** (Weeks 1–2): Architecture blueprint, API audit, migration matrix.
- **Phase 2: Core Engineering & Integration** (Weeks 3–6): Bi-directional synchronization pipelines, webhook handlers, role-based access.
- **Phase 3: Validation, Staging & User Acceptance Testing (UAT)** (Weeks 7–8): End-to-end integration tests, load tests, compliance audit sign-off.
- **Phase 4: Production Rollout & Knowledge Transfer** (Weeks 9–10): Blue/green deployment, runbook documentation, admin training sessions.

### C. Scope Boundaries (In-Scope vs. Out-of-Scope)
Explicitly document what is **NOT** included to prevent scope creep:
- *Out-of-scope*: Data migration of unformatted records prior to FY2024; customization of third-party legacy ERP endpoints without published REST APIs.

### D. Investment & Milestone Schedule

| Milestone / Deliverable | Timeline | Investment | Acceptance Criteria |
|---|---|---|---|
| Milestone 1: Blueprint & Architecture | Weeks 1–2 | $15,000 | Signed architectural decision record and schema design |
| Milestone 2: Core Pipeline & Integration | Weeks 3–6 | $35,000 | Staging pipeline processing 10,000 test transactions |
| Milestone 3: UAT & Production Release | Weeks 7–9 | $20,000 | Zero critical defects in UAT and successful cutover |
| **Total Engagement** | **9 Weeks** | **$70,000** | **Final project sign-off and SLA activation** |

## 2. Risk Reversal & Proof Points
- **Relevant Case Studies**: Include 1–2 vignettes of comparable engagements with before/after metrics.
- **Service Level Agreements & Warranties**: 30-day bug-fix warranty on all delivered code post-cutover.
- **Decision Timeline**: Include explicit offer validity date (e.g. "Pricing and milestone schedule guaranteed through October 31, 2026").

## Critical Rules
1. Never submit pricing before explicitly defining acceptance criteria for every deliverable.
2. Every proposal must state what happens when change requests occur (e.g. "additional requirements billed at $X/hour or scoped as a Phase 2 addendum").
3. Avoid generic fluff ("we are passionate about customer success"); cite verified uptime, certifications, or delivery stats instead.

## Verification Checklist
- [ ] Client problem quantified with specific baseline and target metrics.
- [ ] 2–3 explicit win themes woven throughout the narrative.
- [ ] Statement of Work contains clear in-scope and out-of-scope boundaries.
- [ ] Investment table ties fee payments directly to verifiable milestones, not arbitrary dates.
- [ ] Acceptance criteria, warranty period, and change-order procedures documented.

## Anti-Patterns
- NEVER provide an open-ended "Time & Materials" estimate without an agreed maximum cap and approval trigger.
- NEVER bury pricing at the end without having established measurable ROI in the Executive Summary.
- NEVER leave third-party dependencies (client API access, infrastructure provisioning) unassigned.
