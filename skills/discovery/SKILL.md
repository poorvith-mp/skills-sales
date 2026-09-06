---
name: discovery
group: Pipeline
description: >-
  Structure discovery calls: question design, current-state mapping, and gap quantification. Use
  when running sales discovery calls or BANT qualification.
---

# discovery

## Core Philosophy
Sales discovery is not an interrogation where an SDR fires off a 20-question checklist from a CRM script. Discovery is a collaborative diagnostic interview. Top sales professionals uncover the root cause of organizational dysfunction, quantify the latent cost of inaction, and help buyers understand the true scope of their problem better than they understand it themselves. If discovery is done right, the solution and pricing become obvious.

---

## 4-Step Diagnostic Discovery Framework

### Step 1: Pre-Call Intelligence & Hypothesis Formulation
1. **15-Minute Pre-Call OSINT**:
   - Review LinkedIn: Buyer's background, tenure, recent promotions, engineering pedigree.
   - Inspect Company Tech Stack: BuiltWith, Wappalyzer, public GitHub repositories, Job Postings (which indicate what tools and languages they are currently hiring for).
2. **Formulate a Plausible Hypothesis**:
   - Before dialing, write down: *"Based on their tech stack and recent hiring surge, they are likely experiencing [Specific Bottleneck] causing [Business Consequence]."*

### Step 2: The Diagnostic Question Flow (SPIN + Gap Selling)
1. **Situation (Context without Prying)**:
   - Ask questions you couldn't learn online: *"How is your platform team currently structured between cloud infrastructure and product feature squads?"*
2. **Problem (Pain Exploration)**:
   - Probe the friction: *"Where does the deployment process slow down between a pull request getting approved and landing in production?"*
3. **Implication (Cost of Inaction)**:
   - Quantify the organizational bleeding: *"When that deployment pipeline fails at 6:00 PM, what happens to the engineering on-call rotation? How many developer hours are burned remediating it?"*
4. **Need-Payoff (Future State Vision)**:
   - Let the buyer articulate the value: *"If your engineers could deploy schema migrations with zero risk of locking tables, what would that unlock for your quarterly release roadmap?"*

### Step 3: Gap Quantification & The Cost of Inaction (COI)
1. **Quantifying the Financial Bleed**:
   $$text{Annual COI} = (text{Frequency of Incident / Year})  imes (text{Hours to Fix})  imes (text{Blended Hourly Dev Cost}) + text{Downtime Revenue Loss}$$
2. **Securing Agreement on the Math**:
   - Rephrase the calculation back to the buyer: *"So between developer time and customer SLA credits, this issue is costing your organization roughly $180,000 annually. Does that align with how your leadership views this?"*

### Step 4: Qualification & Mutual Next Steps
1. **MEDDPICC Quick Calibration**:
   - *Metrics*: Verified quantifiable COI.
   - *Economic Buyer*: Identified who has budget approval authority.
   - *Decision Criteria*: Technical, commercial, and security requirements.
   - *Decision Process*: Steps to contract sign-off (legal, procurement, security).
2. **Closing the Call with a Mutual Action**:
   - Never end with "I'll send some slides."
   - Schedule the exact date and time for the technical demo / architecture review with specific key stakeholders invited.

---

## Deliverable Format: Discovery Call Brief (`DISCOVERY-BRIEF.md`)

```markdown
# Sales Discovery Brief: [Company Name]

## 1. Call Snapshot & Participants
- **Account**: [Company Name] | **Domain**: [URL]
- **Attendees**: [Buyer Name, Title] | [Vendor Rep, Title]
- **Current Tech Stack**: [AWS, Kubernetes, Go, PostgreSQL]

## 2. Diagnostic Findings (The Current State vs Desired State)
- **Current State**: [Describe manual / broken status quo]
- **Primary Technical Pain**: [Specific bottleneck identified]
- **Root Cause**: [Why existing tools fail]
- **Desired Future State**: [Buyer's ideal workflow]

## 3. Cost of Inaction (COI) Quantification
- **Incident Frequency**: [e.g. 4 outages / quarter]
- **Engineering Hours Lost**: [~40 hours per incident @ $100/hr = $16,000]
- **Direct Revenue Impact**: [~$25,000 in SLA refunds]
- **Total Annual Bleed**: **~$85,000 / year**

## 4. MEDDPICC Calibration
- **Economic Buyer**: [VP of Engineering - sign-off required >$30k]
- **Decision Criteria**: [SOC 2 compliance, CLI ergonomics, <5ms latency]
- **Timeline / Catalyst**: [Must solve before Q4 peak traffic on Nov 15]

## 5. Agreed Next Step
- **Next Meeting**: Technical Architecture Demo on [Date/Time]
- **Attendees Required**: Buyer to invite Lead Platform Architect
```

---

## Worked Example: Platform Tool Discovery Call

- **Hypothesis**: Engineering team growing rapidly, causing database migration collisions.
- **Dialogue Discovery**: Uncovered that a recent bad schema migration caused a 3-hour outage on Black Friday, resulting in $120,000 in lost transactions and executive scrutiny.
- **Quantification**: Quantified total business impact at $210,000 including lost dev productivity.
- **Outcome**: Scheduled technical POC review directly with the VP of Engineering; deal closed in 21 days at $48k ARR.

---

## Verification Checklist

- [ ] Pre-call research verified tech stack and buyer role prior to meeting.
- [ ] Open-ended diagnostic questions uncovered root cause, not just symptoms.
- [ ] Cost of Inaction (COI) is quantified with concrete numerical estimates.
- [ ] Economic buyer and decision timeline are identified.
- [ ] Call concludes with a firm calendar date and time for the next milestone.

---

## Anti-Patterns

- **Feature Spraying**: Showing product UI or slide decks in the first 20 minutes before diagnosing the problem.
- **Interrogation Mode**: Reading through a rigid checklist of 15 BANT questions like a bureaucrat.
- **Accepting Surface Pain**: Stopping at "deployments are slow" without asking *why* they are slow and *what* it costs.
