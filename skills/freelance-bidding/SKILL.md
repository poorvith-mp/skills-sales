---
name: freelance-bidding
group: Bidding
description: >-
  Build marketplace positioning and write job-specific proposals that mirror the client's stated
  pain with targeted proof. Use when writing winning Upwork proposals, freelance pitches, or bids.
---

# freelance-bidding

## Core Philosophy
Winning freelance, agency, and consulting bids on competitive marketplaces (Upwork, Catalant, Contra) is not a volume game of copying and pasting generic cover letters. Clients on marketplaces are terrified of two things: hiring a fraud who wastes their budget, and managing an amateur who requires constant hand-holding. A winning bid is a diagnostic proposal that mirrors the client's exact words, demonstrates immediate domain mastery, and outlines a derisked 3-phase execution plan before anyone else.

---

## 4-Step Freelance Proposal Architecture

### Step 1: Client Post Deconstruction & Reverse-Engineering
1. **Decode the Real Need**:
   - Extract the core technical blocker from the client's post.
   - Look for unstated anxieties: Have they been burned by previous freelancers? Is the deadline imminent? Are they non-technical founders needing guidance?
2. **Identify Magic Trigger Phrases**:
   - Extract their exact vocabulary (e.g. "Stripe Connect webhook failures", "Next.js 14 server actions bug"). You must reflect these exact terms in your opening lines.

### Step 2: The First 2 Lines (The Win-or-Die Opening)
1. **The Mobile Preview Rule**:
   - On Upwork and freelance platforms, clients only see the first **140–160 characters** before clicking "Expand".
   - Banned Openers: "Dear Hiring Manager", "I have 8 years of experience in...", "I am a full stack developer passionate about...".
   - High-Conversion Formula:
     - *"Fixed this exact Next.js 14 webhook hydration error last week on an enterprise billing app. Here is why it happens and how to resolve it in under 4 hours:"*

### Step 3: The 3-Phase Structured Execution Roadmap
1. **Phase 1: Diagnostic & Audit (Immediate - Day 1)**:
   - Review codebase, replicate issue in local isolated environment, deliver root-cause memo.
2. **Phase 2: Implementation & Automated Testing (Days 2–3)**:
   - Implement clean fix, add unit/integration tests to prevent regression, verify edge cases.
3. **Phase 3: Deployment & Documentation (Day 4)**:
   - Deploy to staging, guide client walkthrough, provide 1-page maintenance SOP and video loom.

### Step 4: Targeted Proof-of-Work & Friction-Free CTA
1. **Hyper-Relevant Proof**:
   - Provide 1 or 2 links to *identical* past work (live URL, GitHub PR, or screenshot of benchmark). Never dump a generic 20-item portfolio.
2. **The Low-Friction Closing Call to Action**:
   - *"If you can grant read-only GitHub repo access, I can run a quick diagnostic today and tell you the exact line of code causing the lock. Are you free for a 10-minute sync this afternoon?"*

---

## Deliverable Format: Winning Proposal Template (`PROPOSAL.md`)

```markdown
# Freelance Marketplace Proposal: [Project Title]

## 1. The Opening Hook (Visible in Preview)
Fixed this exact [Specific Technical Problem] last month for a [Client Type]. The issue is almost certainly caused by [Technical Root Cause Hypothesis].

## 2. Diagnostic & Technical Approach
Here is the exact approach I'll take to resolve this cleanly:
- **Root Cause**: [Explain why their current error occurs without jargon].
- **Proposed Solution**: [Specific architecture or library fix].
- **Regression Prevention**: [Automated test or safety check added].

## 3. 3-Step Execution Plan
- **Step 1 (Day 1)**: Repo intake, environment setup, and local bug reproduction.
- **Step 2 (Day 2)**: Core implementation and unit test suite verification.
- **Step 3 (Day 3)**: Staging deployment, client verification walkthrough, and documentation.

## 4. Relevant Proof-of-Work
- Similar Project Case Study: [Clean URL or GitHub commit link]
- Client Review: *"Resolved our database locking issue in 24 hours with zero downtime."*

## 5. Next Steps
Happy to hop on a 10-minute screen share to review your logs and confirm the fix. What time zone are you based in?
```

---

## Worked Example: High-Value Upwork Bid for Database Performance

- **Client Post**: *"Postgres database running on AWS RDS CPU hits 100% every day at 2 PM. Need someone to optimize queries fast."*
- **Opening Sentence**: *"Your 2 PM CPU spike is almost certainly a rogue analytical query running a sequential table scan during peak OLTP traffic without a composite index."*
- **Bid Price**: $2,500 fixed-price (top 5% of bids).
- **Result**: Client messaged within 12 minutes; hired without interviewing other applicants.

---

## Verification Checklist

- [ ] First 2 sentences directly address the client's problem without any biographical throat-clearing.
- [ ] Proposal quotes the client's specific technologies and error symptoms.
- [ ] Includes a clear 3-step timeline and execution milestones.
- [ ] Includes at most 2 hyper-relevant case studies or proof links.
- [ ] Concludes with a specific, low-friction closing call to action.

---

## Anti-Patterns

- **Generic Boilerplate**: Sending a 5-paragraph template reciting your degree and list of 25 programming languages.
- **Price Racing to the Bottom**: Slashing prices to $10/hr, which signals incompetence and desperation to serious clients.
- **Asking "What is your budget?"**: Failing to provide clear scope and pricing guidance upfront.
