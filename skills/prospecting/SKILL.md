---
name: prospecting
last_reviewed: 2026-09-06
group: Pipeline
description: >-
  Build and qualify a target list from an ICP, with enrichment and disqualification rules. Use
  when finding high-intent B2B target accounts, leads, or list building.
---

# prospecting

## Core Philosophy
Modern B2B outbound prospecting is not buying a list of 10,000 unverified email addresses and blasting them with generic AI sales sequences. That approach destroys domain reputation and yields $< 0.1\%$ response rates. Precision prospecting is an investigative discipline: building high-conviction account lists filtered by verified technographic stack signals, firmographic trigger events, and disqualifying bad fits before reaching out.

---

## 4-Step Precision Prospecting Framework

### Step 1: Technographic & Firmographic ICP Definition
1. **The 4 ICP Filters**:
   - *Firmographics*: Company headcount (e.g. 50–250 employees), ARR stage ($5M–$30M), geography, industry.
   - *Technographics*: Exact software tools installed (e.g. uses Next.js, AWS EKS, Snowflake, Stripe).
   - *Regulatory / Compliance*: Subject to SOC 2, HIPAA, GDPR, or PCI-DSS requirements.
   - *Org Structure*: Has at least 1 dedicated DevOps/Platform engineer or Head of Security.
2. **Explicit Disqualification Criteria**:
   - Immediately exclude: Freelancers, agencies, bootstrapped teams with $< 5$ engineers, companies using non-supported legacy tech stacks (e.g. on-premise mainframe).

### Step 2: Trigger Event & Buying Intent Sourcing
1. **The 5 High-Conversion Buying Triggers**:
   - *Leadership Change*: New VP of Engineering, CTO, or CISO hired within the last 90 days (new leaders have budget and mandates to fix systems).
   - *Funding Event*: Company raised Series A or B in past 60 days (mandate to scale infrastructure quickly).
   - *Job Postings*: Hiring for specific roles (e.g. hiring 4 Kubernetes engineers implies impending infrastructure complexity).
   - *Public Incidents*: Recent outage, post-mortem, or security vulnerability discussed publicly.
   - *Tech Migration*: Public announcement or repository signals indicating migration to cloud/microservices.

### Step 3: Precision Contact Identification & Multi-Threading
1. **The 3-Persona Account Infiltration Map**:
   - *Target Persona 1: The Operator / User* (Staff Engineer / Dev Lead): Feels the daily friction; tests the product.
   - *Target Persona 2: The Functional Leader* (Director of Infrastructure / VP Engineering): Owns team velocity and hiring budget.
   - *Target Persona 3: The Executive / Economic Buyer* (CTO / CFO): Approves contracts $> $25text{k}$.
2. **Contact Verification**:
   - Verify email deliverability using zero-bounce verification tools (NeverBounce, MillionVerifier). Enforce bounce rate $< 2\%$.

### Step 4: Account Tiering & Outreach Channel Allocation
1. **Tiered Outreach Allocation**:
   - *Tier 1 (Top 20 Accounts)*: 100% custom, multi-channel approach (Email + LinkedIn + mutual intro request).
   - *Tier 2 (Next 80 Accounts)*: Highly personalized modular templates tailored to their specific tech stack.
   - *Tier 3 (Broader 200 Accounts)*: Programmatic outbound segmented by trigger event.

---

## Deliverable Format: Target Account Prospecting List (`PROSPECTING-LIST.md`)

```markdown
# Target Account Prospecting Matrix: [Campaign Name]

## 1. ICP Filters & Campaign Trigger
- **Target Persona**: VP of Infrastructure / Platform Engineering Leads
- **Target Company Size**: 50–250 employees, Series A–B funded
- **Primary Technographic Filter**: Running Kubernetes on AWS
- **Primary Buying Trigger**: Hired new VP of Engineering in last 60 days

## 2. High-Priority Target Account Matrix
| Company Name | Headcount | Tech Stack Signals | Trigger Event | Primary Contact | Title | Verified Email |
|---|---|---|---|---|---|---|
| [TargetCo A] | 120 | AWS, EKS, Terraform | Raised $18M Series A; hiring 3 SREs | [Name] | VP Engineering | `name@targetco.com` |
| [TargetCo B] | 85 | GCP, GKE, Go | New CTO hired from Stripe 45d ago | [Name] | Head of Platform | `name@targetco.com` |

## 3. Disqualification Log
- `Company X`: Disqualified — uses on-prem VMware; no cloud presence.
- `Company Y`: Disqualified — 8 total employees; below minimum scale threshold.

## 4. Multi-Channel Outreach Plan
- **Day 1**: Personalized email referencing their specific tech stack and trigger event.
- **Day 3**: LinkedIn profile view + relevant comment on their technical post.
- **Day 7**: Email 2 sharing relevant technical architecture benchmark.
```

---

## Worked Example: Cloud Observability Prospecting

- **ICP Filter**: B2B SaaS companies running ClickHouse or high-throughput Kafka clusters.
- **Trigger**: Companies posting job descriptions mentioning "Kafka scaling bottlenecks".
- **Outreach**: Identified 35 target accounts. Sent personalized messages referencing their specific job posting requirements and attaching an architectural optimization cheat sheet.
- **Outcome**: 31% positive response rate; 9 qualified discovery calls booked from 35 accounts.

---

## Verification Checklist

- [ ] Every target account meets all 4 ICP criteria (firmographic, technographic, scale, roles).
- [ ] Every account has a documented trigger event justifying outreach timing.
- [ ] Email addresses are 100% validated with verified deliverability status.
- [ ] At least 2 personas are identified per target account for multi-threading.
- [ ] Accounts failing criteria are explicitly documented in a disqualification log.

---

## Anti-Patterns

- **Scraping Without Verification**: Exporting 5,000 unverified contacts and damaging domain deliverability.
- **Ignoring Technographics**: Pitching an AWS-specific solution to a company operating entirely on Google Cloud.
- **Single-Threaded Outreach**: Contacting only one junior engineer and abandoning the account when they don't reply.
