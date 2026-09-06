---
name: win-loss-analysis
group: Pipeline
description: >-
  Interview won and lost deals, find the pattern, and feed it back to product, pricing and
  marketing. Use when conducting post-mortem interviews on lost deals or won customers.
---

# win-loss-analysis

## Core Philosophy
Most sales teams attribute won deals to brilliant salesmanship and lost deals to "too expensive" or "missing feature X". Both explanations are usually self-serving myths. Win-Loss Analysis is a rigorous qualitative and quantitative post-mortem discipline. Conducted objectively, it uncovers the true decision drivers of enterprise buyers, exposes competitive vulnerabilities, tests market positioning, and feeds actionable intelligence back into product, pricing, and marketing roadmaps.

---

## 4-Step Win-Loss Analysis Framework

### Step 1: Sample Selection & Interview Architecture
1. **The Balanced Cohort**:
   - Analyze deals across 3 distinct cohorts every quarter:
     - *Won Deals (5–8 interviews)*: Why did they actually sign? What almost stopped them?
     - *Lost to Competitor (5–8 interviews)*: Why did the competitor win? What did they do better?
     - *Lost to "No Decision" / Status Quo (5–8 interviews)*: Why did the initiative die? Why was inaction acceptable?
2. **Neutral Third-Party Interviewer Rule**:
   - The account executive who managed the deal must *never* conduct the interview. Buyers will not be honest with the salesperson. Interviews should be conducted by Product Marketing, RevOps, or an independent consultant.

### Step 2: The 20-Minute Buyer Interview Protocol
1. **The Diagnostic Question Flow**:
   - *The Catalyst*: "What happened inside your organization that initiated this project in the first place?"
   - *The Evaluation*: "Who else was on the shortlist, and how did you narrow it down to the final two?"
   - *The Decision Pivot*: "Take me back to the exact meeting where the final decision was made. What was the deciding factor?"
   - *Pricing & Packaging*: "How did our pricing structure compare to your budget and the competitor's model?"
   - *Sales Experience*: "Where did our team help you, and where did our sales process create friction?"

### Step 3: Pattern Extraction & Quantitative Tagging
1. **Systematic Factor Tagging**:
   - Tag interview transcripts across 5 standard dimensions:
     - *Product Capabilities* (Feature gaps, UX ergonomics, performance).
     - *Pricing & Commercials* (TCO, packaging structure, transparency).
     - *Security & Compliance* (SOC 2, deployment model, vendor risk).
     - *Sales Experience* (Technical responsiveness, POC quality, pushiness).
     - *Brand & Market Perception* (Reputation, stability, customer references).
2. **The "Feature vs Perception" Filter**:
   - Check whether lost deals cite features you *already have*. If 40% of lost deals say you lack a feature that is in production, you have a marketing/demo communication failure, not a product gap.

### Step 4: Executive Synthesis & Action Loops
1. **Quarterly Win-Loss Briefing**:
   - Present findings directly to the Executive Leadership Team (CEO, Head of Product, Head of Sales, CMO):
     - Top 3 reasons we win (double down on these in marketing).
     - Top 3 reasons we lose (prioritize in product and sales enablement).
     - Direct verbatim quotes from enterprise buyers.

---

## Deliverable Format: Win-Loss Analysis Synthesis (`WIN-LOSS-REPORT.md`)

```markdown
# Quarterly Win-Loss Analysis Report: [Quarter / Year]

## 1. Executive Summary & Win-Rate Trends
- **Total Closed Deals Evaluated**: [Count] (Won: [Count] | Lost: [Count])
- **Overall Blended Win Rate**: [XX%] (vs [XX%] previous quarter)
- **Total Interviews Completed**: [Count] ([X] Won, [Y] Lost to Competitor, [Z] No Decision)

## 2. Key Decision Drivers (Why We Win vs Why We Lose)
| Dimension | Top Win Driver | Top Loss Driver | Recommended Action |
|---|---|---|---|
| Product | Fast local CLI execution & developer ergonomics | Missing automated Terraform provider | Accelerate Terraform provider launch |
| Pricing | Transparent usage-based model | Opaque enterprise seat minimums | Lower enterprise minimum seat tier |
| Sales Process | Technical SE demos with live custom code | Delayed responses to infosec questionnaire | Build automated SOC 2 trust center |

## 3. Direct Verbatim Buyer Quotes
- **From Won Deal (VP Eng @ Fintech)**:
  > *"Your competitor felt like a legacy enterprise vendor trying to lock us in. Your team gave us a working Docker container on day 1."*
- **From Lost Deal (Director Infra @ HealthTech)**:
  > *"We loved your product, but Competitor X had an out-of-the-box HIPAA BAA agreement ready, whereas your team took 3 weeks to review legal terms."*

## 4. Prioritized Action Items
1. **Product**: Ship Terraform provider v1.0 by end of Q3 (Blocks 35% of lost deals).
2. **Sales**: Standardize pre-approved infosec answers in automated knowledge bank.
3. **Marketing**: Update homepage messaging to emphasize native HIPAA compliance.
```

---

## Worked Example: Database Tool Win-Loss Overhaul

- **Findings**: 60% of lost deals cited "lack of enterprise replication capabilities".
- **Discovery**: In interviews, buyers revealed they did not actually need complex multi-region active-active replication; they simply needed automated asynchronous read-replicas, which the product already supported but the sales team failed to showcase in demos.
- **Action**: Retrained sales engineers on demoing read-replica setup in under 60 seconds.
- **Result**: Win rate against primary competitor jumped from 22% to 41% the following quarter.

---

## Verification Checklist

- [ ] Interviews are conducted by neutral third parties (not the deal's account executive).
- [ ] Sample covers won deals, competitor losses, and "no decision" stalls.
- [ ] Root causes are separated into true product gaps vs demo/positioning gaps.
- [ ] Report includes verbatim quotes from economic buyers and evaluators.
- [ ] Concrete action items are assigned to product, marketing, and sales leadership.

---

## Anti-Patterns

- **Relying on CRM Dropdown Fields**: Trusting the sales rep's subjective single-click "Lost to Price" note in Salesforce.
- **Only Interviewing Happy Customers**: Celebrating wins while ignoring why 70% of evaluations walk away.
- **Weaponizing Feedback**: Using win-loss reports to attack individual sales reps or product managers rather than fixing systemic processes.
