# Customer Support Escalation Guide

Routing rules, severity definitions, and handoff protocols.

## Severity Matrix & SLA
| Severity | Definition | Response SLA | Target Resolution |
|---|---|---|---|
| P0 (Critical) | System outage, data loss, security vulnerability | < 15 min | < 2 hours |
| P1 (High) | Core functionality broken, no workaround available | < 1 hour | < 8 hours |
| P2 (Normal) | Non-blocking bug, standard billing question | < 4 hours | < 24 hours |
| P3 (Low) | Feature inquiry, cosmetic issue | < 1 business day | Scheduled |

## Internal Routing
- **Security / Auth**: Escalate immediately to Security on-call; do not request credentials from user.
- **Data Integrity**: Route to Database / Infrastructure lead with incident ID and account ID.
- **Refunds > $500**: Route to Finance / Operations queue with transaction trace.
