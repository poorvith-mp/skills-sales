---
name: cold-outreach
last_reviewed: 2026-09-06
group: Pipeline
description: >-
  Write cold email and DM sequences that get replies, including domain warmup and deliverability.
  Use when drafting personalized cold emails, LinkedIn DMs, or follow-up cadences.
---

# Cold Outreach

Cold outreach succeeds on technical deliverability and acute relevance, not brute volume. Spray-and-pray sequences destroy domain reputation and land in spam folders. Modern outbound requires isolated secondary domain infrastructure, strict SPF/DKIM/DMARC authentication, automated warmup ramps, and tight multi-channel cadences across Email and LinkedIn.

## 1. Domain Infrastructure & Deliverability Protocol

Protect your primary company domain by building dedicated outbound infrastructure:

### A. Secondary Domain Architecture
- **Never send cold outreach from your primary apex domain** (e.g. `company.com`). If an outreach campaign gets flagged, primary corporate email deliverability is compromised.
- Purchase 2–3 lookalike secondary domains (e.g. `trycompany.com`, `usecompany.com`, `companyhq.com`) configured with Google Workspace or Microsoft 365 mailboxes.
- Set up 301 redirects from secondary domain roots to your primary website homepage.

### B. DNS Authentication Records (Mandatory)
Before sending a single email, configure four DNS records on every sending domain:
1. **SPF (Sender Policy Framework)**:
   ```txt
   v=spf1 include:_spf.google.com ~all
   ```
2. **DKIM (DomainKeys Identified Mail)**: Generate a 2048-bit cryptographic key in Google Workspace / M365 admin and publish the TXT record at `google._domainkey.domain.com`.
3. **DMARC (Domain-based Message Authentication)**:
   ```txt
   v=DMARC1; p=quarantine; rua=mailto:dmarc-reports@trycompany.com; pct=100; sp=quarantine
   ```
4. **Custom Tracking Domain (CNAME)**: When using tracking pixels or click tracking, use a dedicated subdomain (`track.trycompany.com`) with an SSL cert. *Best practice*: Disable open/click tracking entirely for cold emails to improve inbox placement.

### C. Automated Domain Warmup Schedule
Warm up mailboxes for 14–21 days using automated peer networks (Smartlead, Instantly) before sending cold campaigns:
- **Week 1 (Days 1–7)**: 5–10 automated warmup emails/day. Zero cold prospect emails.
- **Week 2 (Days 8–14)**: 15–20 warmup emails/day. Start cold outbound at 5 emails/day/mailbox.
- **Week 3+ (Production)**: 25–35 cold emails/day + 15 warmup emails/day per mailbox.
- **Hard Ceiling**: Maximum 40 cold emails per mailbox per day. To send 200 emails/day, use 5 mailboxes distributed across 2 domains.

## 2. Multi-Channel Cadence Architecture (Email + LinkedIn)

Structure outreach across 4–5 touches over a 16-day window:

```
Day 1:  [Email 1] Personal observation + problem statement + low-friction ask
Day 2:  [LinkedIn] Profile view + connection request (blank note or 1-line observation)
Day 5:  [Email 2] Quick bump with 1-sentence customer proof or metric
Day 8:  [LinkedIn DM] Short value drop if connection accepted (no calendar link)
Day 12: [Email 3] Frictionless resource or perspective shift
Day 16: [Email 4] Polite breakup closing the loop
```

### High-Converting Email Frameworks
- **Subject Lines**: 2–4 words, lowercase, non-promotional: `quick question`, `[Company] <> [Prospect Company]`, `re: [Specific Trigger]`.
- **Word Count**: Strictly between 50 and 90 words. Long emails trigger cognitive fatigue on mobile screens.
- **The Low-Friction Call to Action (CTA)**:
  - *Weak*: "Can we schedule a 30-minute demo on Tuesday at 2pm? Here's my Calendly link."
  - *Strong*: "Open to checking out the 2-minute breakdown?" or "Worth exploring, or is this not on your radar for Q3?"

### LinkedIn DM Rules
- Keep messages under 250 characters.
- Anchor to a public signal: comment on their recent post, hiring announcement, or podcast appearance.
- Never pitch or drop a scheduling link in the connection request note.

## 3. List Hygiene & Bounce Prevention
- Run every prospect email through real-time verification tools (NeverBounce, ZeroBounce) before loading into cadences.
- Maintain a bounce rate strictly `< 2.0%`. Bounces above 3% trigger spam filtering across Google and Microsoft networks.

## Critical Rules
1. Never send cold outreach from the primary domain used for corporate operations.
2. Every prospect email list must be validated immediately prior to sending; never send to stale or unverified lists.
3. Keep cold emails under 90 words with a single, clear question rather than multiple demands.

## Verification Checklist
- [ ] Secondary domains configured with valid SPF, DKIM, and DMARC records.
- [ ] Mailboxes warmed up for a minimum of 14 days with >50% warmup engagement.
- [ ] Prospect list verified with <2% predicted bounce rate.
- [ ] Email copy contains zero spam trigger phrases ("free", "guarantee", "act now", "urgent").
- [ ] CTA is conversational and asks for interest rather than booking calendar time directly.

## Anti-Patterns
- NEVER exceed 40 cold emails per mailbox per day; distribute volume across multiple inboxes.
- NEVER include calendar links (Calendly/HubSpot) in initial outreach emails; links degrade deliverability.
- NEVER send generic template blasts that lack custom, role-specific personalization triggers.
