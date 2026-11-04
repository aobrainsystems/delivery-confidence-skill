# Trust score rules (summary)

Score = 100 minus capped deductions. Each deduction lists the issue keys behind it and an owner role.

| Check | Rule | Max deduction | Owner |
|---|---|---|---|
| Unsized children | share of children without an estimate | 15 | PO |
| Stale | not Done and not updated for 14+ days | 15 | PO |
| Missing target | no fixVersion and no due date | 10 | RELEASE |
| Blocked without owner | blocked or flagged, no assignee | 15 | RELEASE |
| Scope growth | more than 25% growth since baseline | 15 | PO |
| Status contradictions | children mostly Done but epic To Do, past due not Done, Done with open children | 15 | PO |
| Missing assignee | in-progress child unassigned | 10 | PO |
| Orphans | in-scope issues with no parent | 5 | PO |
| Insufficient history | fewer than 9 weekly throughput samples | 15 | RELEASE |
