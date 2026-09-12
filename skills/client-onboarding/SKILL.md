---
name: client-onboarding
last_reviewed: 2026-09-06
group: Post-sale
description: >-
  Set up a new engagement: intake, access, environments and communication cadence. Use when
  managing post-sale client kickoff, implementation, or training.
---

# client-onboarding

## Core Philosophy
Client onboarding sets the tone for the entire customer lifecycle. The first 30 days post-sale are the most critical period in determining long-term retention and expansion: customer excitement is at its peak, but buyer's remorse is lurking. Effective client onboarding is not a loose series of "touch base" calls; it is a rigorous, structured project management discipline that drives rapid time-to-first-value (TTFV) through a Mutual Action Plan (MAP).

---

## 4-Stage Client Onboarding Framework

### Step 1: Internal Sales-to-Success Handoff (Day 0)
1. **The Pre-Kickoff Dossier**:
   - Sales rep must transfer documented context before client kickoff:
     - The "Why": Core commercial pain and promised business outcomes.
     - The "Who": Key stakeholders, champions, skeptics, and procurement contacts.
     - Technical Scope: Contracted deliverables, architecture constraints, timeline commitments.
     - Sensitive Landmines: Previous vendor failures, internal political tensions, budget sensitivities.

### Step 2: Kickoff Meeting & Mutual Action Plan (MAP) (Days 1–7)
1. **The High-Impact Kickoff Meeting (45 Minutes)**:
   - *Agenda*: Introductions & roles, review stated business objectives, walk through the Mutual Action Plan (MAP), confirm technical prerequisites, and establish communication channels.
2. **Mutual Action Plan Construction**:
   - Define exact milestones, dependencies, due dates, and accountable owners on *both* vendor and client teams:
     - Milestone 1: Environment provisioning & credentials exchange.
     - Milestone 2: Technical architecture review & security sign-off.
     - Milestone 3: Initial pilot integration & smoke test.
     - Milestone 4: Team training & production rollout.
     - Milestone 5: First Value Realization & formal onboarding sign-off.

### Step 3: Technical Implementation & Access Provisioning (Days 8–21)
1. **Friction-Free Provisioning Checklist**:
   - Provide explicit, copy-pasteable access request templates (e.g. AWS IAM least-privilege policies, SAML SSO parameters, IP allowlisting).
2. **Dedicated Shared Channels**:
   - Establish a shared Slack/Teams channel for real-time unblocking of engineering roadblocks.
3. **Weekly Status Pulse (Red/Amber/Green)**:
   - Send weekly 1-page progress email to executive sponsors highlighting completed tasks, upcoming blockers, and owner assignments.

### Step 4: Value Realization & Formal Hand-Off (Days 22–30)
1. **The First Value Milestone (TTFV)**:
   - Ensure the customer executes their primary core transaction in production within 30 days.
2. **Formal Graduation Sign-Off**:
   - Review initial baseline metrics against the pre-sale success criteria.
   - Transition account from Onboarding Specialist to assigned ongoing Account Manager.

---

## Deliverable Format: Mutual Action Plan (`MUTUAL-ACTION-PLAN.md`)

```markdown
# Client Onboarding & Mutual Action Plan: [Client Name]

## 1. Executive Overview & Target Outcomes
- **Target Go-Live Date**: [YYYY-MM-DD]
- **Target Time-to-First-Value (TTFV)**: [<= 21 days]
- **Primary Business Metric**: [e.g. 100% automated backup coverage across 40 nodes]

## 2. Stakeholder RACI Matrix
- **Executive Sponsor (Client)**: [Name, Title]
- **Technical Lead (Client)**: [Name, Title]
- **Onboarding Manager (Vendor)**: [Name, Title]
- **Solutions Architect (Vendor)**: [Name, Title]

## 3. Implementation Milestone Schedule
| Phase | Milestone / Task | Owner | Due Date | Status |
|---|---|---|---|---|
| Phase 1 | SSO & API Access Provisioned | Client Tech Lead | Day 5 | Completed |
| Phase 2 | Test Environment Deployment | Vendor SA | Day 10 | In Progress |
| Phase 3 | End-to-End Pilot Workflow | Both Teams | Day 18 | Pending |
| Phase 4 | Team Workshop (45 mins) | Vendor OM | Day 24 | Scheduled |
| Phase 5 | Production Go-Live Sign-Off | Client Exec Sponsor | Day 30 | Pending |

## 4. Risks & Dependencies
- **Dependency A**: Client IT security approval for webhook egress (ETA: Day 8).
```

---

## Worked Example: Enterprise Cloud Migration Kickoff

- **Client**: 200-engineer healthtech company adopting an automated cloud compliance tool.
- **Execution**: Onboarding lead shared a pre-formatted Terraform module for read-only AWS IAM role creation during the kickoff call. Credentials delivered in 24 hours.
- **Result**: First continuous compliance scan executed on Day 4 (target was Day 14). Onboarding completed in 18 days with 100% stakeholder attendance.

---

## Verification Checklist

- [ ] Internal sales-to-success handoff document completed prior to client kickoff.
- [ ] Mutual Action Plan (MAP) contains explicit deliverables, deadlines, and owners for both sides.
- [ ] Shared communication channel (Slack Connect / Teams) launched within 48 hours.
- [ ] Technical prerequisites and least-privilege access specs provided in copy-paste templates.
- [ ] Executive sponsor receives weekly RAG status updates.

---

## Anti-Patterns

- **The Cold Hand-Off**: Forcing the client to re-explain their business requirements and architecture to the onboarding team from scratch.
- **Vague Deadlines**: Operating without a written Mutual Action Plan, leading to onboarding dragging past 90 days.
- **Unstructured Training**: Hosting a 2-hour generic webinar where 80% of client attendees tune out.
