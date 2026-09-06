---
name: public-sector-bids
group: Bidding
description: >-
  Handle government digital presales: policy interpretation, solution design and bid
  documentation. Use when responding to government RFPs, tenders, compliance matrices, or FAR
  rules.
---

# public-sector-bids

## Core Philosophy
Public sector, government, and municipal technology procurement is governed by rigid statutory frameworks (e.g. FAR in the US, Public Contracts Regulations in the UK). In government bidding, technical excellence alone never wins: compliance is the binary gate. If a proposal fails a single mandatory compliance clause or format guideline, it is disqualified without evaluation. Winning public sector bids requires strict compliance matrix mapping, verifiable past performance, and clear alignment with public policy mandates.

---

## 4-Step Public Sector Bid Response Framework

### Step 1: RFP Decomposition & The Compliance Matrix
1. **The Shredding Process**:
   - Deconstruct the Request for Proposal (RFP) or Tender into an exhaustive **Compliance Matrix**:
     - Extract every sentence containing "shall", "must", "will", or "is required to".
   - Assign each requirement a unique ID, RFP section reference, response author, and compliance status (Full / Partial / Non-Compliant).
2. **The Bid / No-Bid Decision Gate**:
   - Evaluate against strict criteria before committing 100+ hours:
     - Do we have active clearance / certifications (FedRAMP, SOC 2, ISO 27001)?
     - Can we satisfy 100% of mandatory "shall" statements?
     - Do we have 3 verifiable past performance citations of similar size, scope, and complexity within the last 3 years?

### Step 2: Solution Architecture & Policy Alignment
1. **Mapping to Government Standards**:
   - Cloud First Policy: Federal Cloud Smart / Cloud First directives.
   - Cybersecurity Framework: NIST SP 800-53 controls, CMMC Level 2, FIPS 140-2 encryption standards.
   - Accessibility: Section 508 / WCAG 2.1 AA compliance with a completed Voluntary Product Accessibility Template (VPAT).
   - Data Sovereignty: In-country data residency and personnel clearance requirements.

### Step 3: Proposal Authoring & "Scoring-Engine" Formatting
1. **Mirroring Evaluator Scoring Rubrics**:
   - Government evaluators score using strict point-based rubrics. Structure headings to mirror the RFP's Statement of Work (SOW) verbatim.
   - Make scoring effortless for evaluators: Start every technical section with an explicit compliance assertion:
     - *"Compliant. [Company Name] fully meets the requirements of Section 3.2.1. Our platform executes..."*
2. **Quantified Past Performance Citations**:
   - Present 3 past performance references: Contract Number, Contracting Agency, Period of Performance, Total Contract Value, Point of Contact (COR/COTR), and Specific Metrics of Success.

### Step 4: Red Team Review & Submission Gate
1. **The 3-Tier Review Cycle**:
   - *Pink Team (60% draft)*: Review architecture, compliance coverage, and win themes.
   - *Red Team (90% draft)*: Mock evaluator scoring—grade proposal strictly against the RFP rubric without mercy.
   - *Gold Team (Final)*: Verify signatures, pricing sheets, certificates of insurance, and submission portal upload requirements.

---

## Deliverable Format: Government RFP Compliance Matrix (`COMPLIANCE-MATRIX.md`)

```markdown
# Public Sector RFP Compliance Matrix & Bid Plan: [Tender Name]

## 1. Tender Metadata
- **Solicitation / RFP Number**: [Solicitation #]
- **Issuing Agency**: [Agency / Ministry Name]
- **Submission Deadline**: [YYYY-MM-DD HH:MM Timezone]
- **Contract Type**: [Firm Fixed Price (FFP) / Time & Materials (T&M)]

## 2. Master Compliance Tracking Matrix
| Req ID | RFP Section | Requirement Summary | Compliance (C / PC / NC) | Proposal Section | Evidence / Proof |
|---|---|---|---|---|---|
| R-01 | Sec 3.1.1 | Data must be stored in FedRAMP Moderate cloud | Fully Compliant | Vol 1, Sec 1.2 | AWS GovCloud hosting architecture |
| R-02 | Sec 3.2.4 | Support MFA via PIV/CAC cards | Fully Compliant | Vol 1, Sec 2.1 | SAML 2.0 PKI integration spec |
| R-03 | Sec 4.1.0 | 24/7 US-based citizen support | Fully Compliant | Vol 2, Sec 1.4 | Operations center staffing roster |

## 3. Past Performance Citations
- **Citation 1**: [Agency Name] — Contract [Contract #] ($X.XM)
  - Scope: Automated infrastructure compliance for 5,000 cloud servers.
  - COR Contact: [Name, Title, Official Government Email]

## 4. Submission Checklist (Gold Team Gate)
- [ ] VPAT / Section 508 accessibility statement attached.
- [ ] Pricing model submitted on prescribed agency Excel template.
- [ ] Signed SF-1449 / solicitation cover sheet included.
- [ ] SAM.gov Unique Entity Identifier (UEI) verified active.
```

---

## Worked Example: Municipal Cloud Infrastructure Tender

- **Opportunity**: City government tender for automated cloud backup and disaster recovery.
- **Strategy**: Built a complete compliance matrix mapping all 42 mandatory requirements to NIST 800-53 controls. Included an active VPAT 2.4 document.
- **Outcome**: Achieved highest technical score (98/100) among 7 competing vendors; awarded $1.2M 3-year contract.

---

## Verification Checklist

- [ ] Every mandatory "shall" and "must" statement in the RFP is mapped in the compliance matrix.
- [ ] Bid/No-Bid review confirms required security certifications (FedRAMP, SOC 2, ISO) are active.
- [ ] Section 508 / VPAT accessibility documentation is prepared and verified.
- [ ] Past performance citations include active agency references and verifiable contract numbers.
- [ ] Proposal structure mirrors RFP section numbers to enable rapid evaluator scoring.

---

## Anti-Patterns

- **Commercial Fluff in Government Bids**: Submitting marketing brochures instead of directly answering compliance clauses.
- **Missing Mandatory Forms**: Getting disqualified on page 1 for forgetting a signed standard government certification form.
- **Ghosting Requirements**: Ignoring difficult RFP requirements hoping the evaluator won't notice.
