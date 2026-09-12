---
name: account-management
last_reviewed: 2026-09-06
group: Post-sale
description: >-
  Own the customer after onboarding: adoption tracking, health reviews, expansion plays and QBRs.
  Use when managing enterprise accounts, quarterly reviews, or expansion.
---

# account-management

## Core Philosophy
Account Management in modern B2B SaaS is not "checking in" every quarter to ask if everything is fine. Real account management is continuous value realization, defensive risk mitigation, and systematic account expansion. If an account manager only speaks to a customer 60 days before contract renewal, the renewal is already lost. Account managers must operate as trusted technical advisors who map customer organizational objectives to demonstrable software outcomes.

---

## 4-Step Account Management & Expansion Framework

### Step 1: Account Telemetry & Health Scoring (0–100)
1. **The 4 Pillars of Account Health**:
   - *Product Adoption (30% weight)*: % of purchased licenses active, depth of feature usage, frequency of admin logins.
   - *Value Realization (30% weight)*: Customer-quantified ROI metrics (e.g. build minutes saved, tickets resolved).
   - *Executive Engagement (20% weight)*: Multi-threaded relationships (connected with VP, Director, and lead architect).
   - *Support & Sentiment (20% weight)*: Open P1/P2 support ticket count, CSAT survey trends.
2. **Health Bands & Playbooks**:
   - *Green (80–100)*: Ripe for expansion, reference calls, and co-marketing case studies.
   - *Yellow (60–79)*: Proactive intervention: schedule technical working session to unblock feature adoption.
   - *Red (< 60)*: Immediate Executive Sponsor intervention; convene internal triage team.

### Step 2: The High-Impact Quarterly Business Review (QBR)
1. **The Modern QBR Agenda (45 Minutes)**:
   - *Minutes 0–10 (The Value Delivered)*: Review past 90 days against their stated success criteria (with exact telemetry data).
   - *Minutes 10–20 (Benchmark & Gap Analysis)*: How their team compares to top-quartile industry peers.
   - *Minutes 20–35 (Forward Roadmap & Strategic Alignment)*: Unveiling new capabilities matching their upcoming initiatives.
   - *Minutes 35–45 (Joint Action Plan)*: Formalize commitments and owners for the next 90 days.
2. **Banned QBR Behavior**:
   - Never spend 30 minutes reciting basic product changelogs or reading slide text verbatim.

### Step 3: Multi-Threading & Stakeholder Mapping
1. **De-Risking Single Points of Failure**:
   - If your sole champion leaves the organization, the account enters the danger zone.
   - Maintain active touchpoints with at least 3 distinct personas:
     - *The Economic Buyer* (CFO / VP): Cares about TCO, ROI, and security compliance.
     - *The Champion / Decision Maker* (Engineering Director / Tech Lead): Cares about developer velocity and team efficiency.
     - *The Daily User* (Senior Dev / DevOps): Cares about DX, ergonomics, and reliability.

### Step 4: Land-and-Expand Commercial Plays
1. **Expansion Triggers**:
   - Seat utilization reaches $\ge 85\%$ of purchased capacity.
   - Cross-departmental interest (e.g., Security team notices DevOps team using the audit pipeline).
   - New product tier launch (e.g., Enterprise Governance, SSO, or Advanced Compliance).
2. **The Expansion Pitch**:
   - Build a bottom-up business case demonstrating that moving to an enterprise site-license reduces per-seat costs while unlocking organization-wide compliance.

---

## Deliverable Format: Account Strategy & Expansion Plan (`ACCOUNT-PLAN.md`)

```markdown
# Enterprise Account Strategy Plan: [Customer Name]

## 1. Account Snapshot
- **Current ARR**: [$XXX,XXX] | **Contract Term**: [Dates]
- **Seats Purchased / Active**: [Seats] / [Seats] ([% Utilization])
- **Account Health Score**: [Score / 100] ([Green / Yellow / Red])
- **Primary Economic Buyer**: [Name, Title]
- **Internal Champion**: [Name, Title]

## 2. Multi-Threading Matrix
| Name | Title | Persona | Relationship Strength | Last Touch |
|---|---|---|---|---|
| [Contact 1] | VP of Infrastructure | Economic Buyer | Neutral (Met at QBR) | 45 days ago |
| [Contact 2] | Staff Platform Dev | Champion | Strong (Slack connect) | 3 days ago |
| [Contact 3] | Head of Security | Evaluator | Weak (Need intro) | Not met |

## 3. 90-Day Value Delivery Metrics
- **Metric 1**: [e.g. Reduced mean CI build duration from 22m to 6m]
- **Metric 2**: [e.g. Saved $38,000 in redundant cloud compute]

## 4. Expansion Roadmap & Target Deals
- **Expansion Opportunity**: [Upgrade to Enterprise Site License + Dedicated VPC]
- **Target Expansion ARR**: [+$XX,XXX]
- **Key Catalyst / Milestone**: [Team expansion planned in Q3]
- **Next Executive Action**: [Executive Sponsor dinner with VP on MM/DD]
```

---

## Worked Example: Infrastructure SaaS Account Expansion

- **Baseline**: Series B fintech account paying $45k ARR for 50 developer seats.
- **Intervention**: Account manager noticed 48 of 50 seats active and detected queries originating from the compliance security team. Arranged a tailored demo for the CISO showcasing audit-log automation.
- **Outcome**: Upgraded contract to $110k ARR Enterprise Tier with SOC 2 compliance add-on, 6 months before annual renewal date.

---

## Verification Checklist

- [ ] Account health score combines quantitative product usage and multi-threaded relationships.
- [ ] QBR agenda leads with customer value realized, not vendor feature lists.
- [ ] Account maintains documented relationships across at least 3 distinct organizational levels.
- [ ] Stagnant or yellow accounts have an active technical remediation plan.
- [ ] Expansion plays are tied directly to customer team growth milestones.

---

## Anti-Patterns

- **Single Champion Trap**: Building a relationship with only one tech lead and losing the entire $100k account when they change jobs.
- **The Renewal Surprise**: Finding out the customer is unhappy for the first time during the renewal contract negotiation.
- **Feature Begging**: Relying on uncommitted future product roadmap promises to prevent churn.
