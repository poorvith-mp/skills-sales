---
name: solution-engineering
group: Pipeline
description: >-
  Do the pre-sales technical work: demo engineering, POC scoping and competitive battlecards. Use
  when delivering technical product demos, scoping POCs, or handling RFIs.
---

# solution-engineering

## Core Philosophy
Solution Engineering (SE) is the bridge between commercial persuasion and technical reality. A great Solution Engineer does not give standard 60-minute feature-by-feature product tours. SEs engineer undeniable technical conviction. They uncover the prospect's real architecture constraints, build tailored interactive demonstrations with realistic customer data, rigorously scope Proof of Concepts (POCs) with binary success criteria, and dismantle technical deal-killers before security reviews begin.

---

## 4-Step Technical Solution Engineering Framework

### Step 1: Technical Discovery & Architecture Mapping
1. **The Infrastructure Deconstruction**:
   - Before building a demo, map the prospect’s current technical reality:
     - Cloud Providers (AWS, GCP, Azure, on-prem).
     - Core Runtime & Frameworks (Node.js, Go, Python, Kubernetes).
     - Databases & Storage Engines (Postgres, DynamoDB, Snowflake).
     - Identity & Auth Providers (Okta, Azure AD, Auth0).
     - Network Topology & Security Boundaries (VPC peering, proxies, air-gapped constraints).
2. **Identify the Technical Showstoppers**:
   - Pinpoint the exact technical hurdle that could kill the deal: *"Can your engine process 50k events/sec without exceeding a 100ms memory footprint?"*

### Step 2: Tailored Demo Engineering (The "Demo of One")
1. **The 3 Rules of High-Impact Technical Demos**:
   - *Rule 1: Use Their Data / Vocabulary*: Seed demo databases with realistic domain entities matching their industry (e.g. healthcare claims for healthtech, ticker symbols for fintech; never `foo` or `bar`).
   - *Rule 2: Inverted Pyramid Flow*: Show the ultimate payoff in the first 5 minutes; walk backward into the configuration mechanics.
   - *Rule 3: Show the Failure Mode & Recovery*: Demonstrate how the system handles simulated failures, network disconnects, or bad data gracefully.

### Step 3: Scoping & Running High-Velocity POCs (Mutual Test Plans)
1. **The 14-Day Bounded POC Model**:
   - Never agree to an open-ended, undefined trial.
   - Establish a **Proof of Concept Charter** with strictly 3–5 binary, measurable success criteria:
     - Example: *"Criteria 1: Ingest 100,000 mock events via API with zero dropped packets and p99 latency < 50ms."*
   - Pre-condition: Commercial agreement on pricing and contract terms *before* the POC starts ("If all success criteria are met, customer agrees to execute contract by [Date]").
2. **Daily POC Standup Cadence**:
   - 15-minute daily async Slack check-in to clear roadblocks and track criteria completion.

### Step 4: Technical Objection Handling & Security Architecture
1. **Dismantling Architecture Objections**:
   - Address data sovereignty, tenant isolation, and cryptographic hashing with ready-to-deploy architecture diagrams.
2. **Security & Compliance Pacification**:
   - Provide pre-compiled security packages: SOC 2 Type II report, penetration test summaries, CAIQ / SIG Lite questionnaires, and detailed data flow diagrams.

---

## Deliverable Format: POC Charter & Technical Evaluation Spec (`POC-CHARTER.md`)

```markdown
# Proof of Concept Charter: [Prospect Name]

## 1. POC Objectives & Timeline
- **POC Start Date**: [YYYY-MM-DD] | **POC End Date**: [YYYY-MM-DD] (Duration: 14 Days)
- **Target Commercial Outcome**: Conversion to Annual Enterprise Tier ($[XX,XXX] ARR)
- **Technical Sponsors**: [Prospect Lead Architect] & [Vendor Solution Engineer]

## 2. Defined Technical Success Criteria
| Criteria ID | Technical Requirement | Verification Method | Pass / Fail Metric | Status |
|---|---|---|---|---|
| SC-01 | Webhook ingestion throughput | Run simulated load test | >= 10,000 req/sec at < 40ms latency | Pending |
| SC-02 | RBAC Integration | Connect Okta SAML | Team permissions enforce least privilege | Passed |
| SC-03 | Custom reporting export | Generate Parquet dump | Export 1M rows in < 15 seconds | Pending |

## 3. Architecture & Integration Topology
- **Deployment Mode**: [Cloud Hosted / Dedicated VPC / Self-Hosted Agent]
- **Prerequisites Required**: [AWS IAM Role credentials, Okta test tenant]

## 4. Mutual Commercial Commitment
If all defined success criteria (SC-01 through SC-03) are verified as passed by [POC End Date], [Prospect Company] agrees to proceed with MSA execution for the Enterprise Tier.
```

---

## Worked Example: High-Throughput API Solution Engineering

- **Prospect Challenge**: Evaluating an enterprise API gateway. Prospect claimed competitor failed at 20k RPS concurrency.
- **SE Action**: Configured an isolated benchmark environment using `k6` load-testing scripts simulating 30k RPS with realistic payload shapes during the technical demo.
- **Outcome**: Demonstrated sub-20ms p99 response times live on screen. Closed POC in 5 days; customer signed a $90k annual contract.

---

## Verification Checklist

- [ ] Technical architecture and constraints mapped prior to demo delivery.
- [ ] Demo uses realistic customer domain data and terminology.
- [ ] POC is strictly time-bounded (<= 14–21 days) with 3–5 binary success criteria.
- [ ] Commercial commitment is linked directly to passing POC criteria.
- [ ] Security documentation (SOC 2, data flow diagram) is ready for infosec review.

---

## Anti-Patterns

- **The Unbounded Sandbox**: Granting a 60-day open-ended trial without success criteria, where the prospect forgets to log in.
- **Generic Click-Through Demos**: Clicking through every menu item in the settings tab for 45 minutes.
- **Surprise Security Reviews**: Handing the deal to procurement only to discover an unaddressed 6-month infosec audit requirement.
