---
name: support-replies
last_reviewed: 2026-09-06
group: Post-sale
description: >-
  Write support responses and handle escalations across email, chat and social, including service
  recovery. Use when drafting empathetic, accurate customer support replies or macros.
---

# support-replies

## Core Philosophy
Customer support is not a low-cost triage center designed to deflect users with canned macro responses. In modern software companies, every support interaction is a brand-defining moment and a critical retention lever. Exceptional support combines technical accuracy, deep empathy, rapid resolution, and radical transparency during outages. A great support reply resolves the immediate bug, explains *why* it occurred, and prevents future recurrence.

---

## 4-Step Customer Support & Escalation Framework

### Step 1: Issue Classification & Priority SLAs
1. **Severity Tiers & Response Standards**:
   - *P1 - Critical Outage (SLA: < 15 mins)*: Core production system down, data corruption risk, major financial/operational impact for multiple accounts.
   - *P2 - Major Degradation (SLA: < 1 hour)*: Core feature broken with no feasible workaround; single high-value account blocked.
   - *P3 - Minor Issue (SLA: < 4 hours)*: Non-critical feature bug with acceptable workaround; UI glitch.
   - *P4 - General Inquiry / Feature Request (SLA: < 24 hours)*: How-to questions, billing inquiries, feedback.

### Step 2: Anatomy of a World-Class Technical Support Reply
1. **The 4-Part Reply Architecture**:
   - *1. Empathetic Acknowledgment & Validation*: Validate the user's frustration without defensive corporate language.
   - *2. Direct Answer / Root Cause*: State the solution or the exact technical explanation in sentence 1 or 2.
   - *3. Concrete Actionable Steps*: Numbered, reproducible instructions or code snippets to resolve the issue immediately.
   - *4. Proactive Recurrence Prevention*: Note what engineering is doing to ensure this bug never happens again.
2. **Banned Support Clichés**:
   - Never say: "We apologize for any inconvenience this may have caused", "As stated in our documentation", or "Please be patient while we look into this."

### Step 3: Crisis Management & Outage Communication
1. **Public Incident Cadence (Status Page & In-App)**:
   - *Investigating (T + 5m)*: Acknowledge the issue publicly. Even if the root cause is unknown, state that engineering is actively investigating.
   - *Identified (T + 20m)*: Share the specific technical component impacted and the remediation being applied.
   - *Monitoring (T + 45m)*: Fix deployed; telemetry returning to baseline.
   - *Resolved (T + 60m)*: Incident closed; announce post-mortem schedule.
2. **Post-Incident Service Recovery**:
   - For impacted P1 enterprise accounts, deliver an unprompted Root Cause Analysis (RCA) within 48 hours detailing timeline, root cause, and engineering safeguards.

### Step 4: Closed-Loop Product Feedback
1. **Tagging & Engineering Feedback Loops**:
   - Tag every ticket with: Component (e.g. Auth, Billing, Webhooks), Root Cause (UX confusion, true bug, docs gap), and Resolution Type.
   - Weekly Support-to-Product review: If $> 10$ tickets report the same UX friction, file a P1 usability ticket in Linear/Jira to fix the root cause in code.

---

## Deliverable Format: Support Macro & Escalation Guide (`SUPPORT-PLAYBOOK.md`)

```markdown
# Customer Support Operations & Response Playbook

## 1. SLA & Severity Matrix
| Severity | Definition | Initial Response SLA | Update Cadence | Escalation Target |
|---|---|---|---|---|
| P1 - Critical | Production Down / Data Loss | < 15 Minutes | Every 30 mins | On-Call Lead & CTO |
| P2 - Major | Core Feature Broken / No Workaround | < 1 Hour | Every 2 hours | Engineering Squad Lead |
| P3 - Minor | Non-critical Bug / Has Workaround | < 4 Hours | Daily | Support Engineer |
| P4 - Inquiry | General Guidance / Billing | < 24 Hours | As resolved | Tier 1 Support |

## 2. Response Templates

### P2 Technical Bug Reply Template
Hi [Customer Name],

Thanks for reaching out and sharing that stack trace. You've encountered an issue where our webhook parser fails when payload timestamps include microsecond precision—I know how frustrating it is to have your ingestion pipeline stall.

Here is how to resolve this immediately:
1. In your webhook configuration, truncate timestamps to standard ISO-8601 (`YYYY-MM-DDTHH:MM:SSZ`).
2. Alternatively, apply this payload transform: `[Code Snippet]`.

Our engineering team has already committed a fix to support microsecond precision (PR #412), which is scheduled for deployment tomorrow at 10:00 AM UTC. Once live, you can revert this workaround.

Let me know if this gets your ingestion running, and I'll keep this ticket open until the permanent fix deploys.

Best,
[Your Name]

## 3. Service Recovery Protocol (Post-Outage)
- Issue credit voucher or SLA refund automatically without waiting for client demand.
- Send written 1-page RCA memo within 48 hours for enterprise accounts.
```

---

## Worked Example: High-Stakes Escalation Handling

- **Scenario**: Fintech customer experienced failed API authentication during morning market open due to a cached token expiration bug.
- **Action**: Support lead acknowledged within 4 minutes with direct engineering workaround. CTO hopped on a temporary Zoom bridge with the client's lead architect to verify live traffic restoration.
- **Follow-up**: Customer was credited $1,500 automatically; received full post-mortem in 24 hours. Customer praised transparency publicly on LinkedIn.

---

## Verification Checklist

- [ ] Ticket severity and SLA response targets are clearly categorized.
- [ ] Responses lead with the direct technical solution, not generic apologies.
- [ ] Concrete code snippets or step-by-step reproduction instructions are provided.
- [ ] Incident communication cadences are maintained during active outages.
- [ ] Recurring ticket topics are fed back into product engineering backlogs.

---

## Anti-Patterns

- **Robot Deflection**: Sending an automated link to docs that doesn't answer the user's specific technical question.
- **Defensive Blaming**: Telling the user "it works on our machines" or blaming their network without investigation.
- **Radio Silence During Outages**: Going dark for 3 hours during a major system incident while users vent on Twitter.
