# Sample Human Review Decision Record

> **Fictional evidence sample — not evidence of actual control operation.**

## Decision Identification

| Field | Entry |
| --- | --- |
| Decision ID | `DEC-SAMPLE-001` |
| Transaction ID | `TX-SAMPLE-1042` |
| System | `AI-SYS-001` |
| Model version | `SIM-0.9` |
| Reviewer | Sample Dispatcher |
| Date and time | 2026-09-20 09:15 ET |
| Recommendation type | Route recommendation |
| Impact level | Enhanced review |

## Recommendation

RouteAssist recommended Route A based on estimated travel time and delivery-window compliance.

## Reviewer Observations

| Item | Observation |
| --- | --- |
| Data freshness | Traffic source updated 42 minutes earlier |
| Conflicting information | Dispatcher received a current road-closure notice |
| Safety concern | Route A included the closed segment |
| Alternative | Route B added 11 minutes but avoided the closure |
| Explanation limitation | System rationale did not reflect the current closure |

## Human Decision

- [ ] Approve
- [x] Modify
- [ ] Reject
- [x] Escalate
- [ ] Invoke fallback

**Final action:** Assign Route B and report stale external route data.

**Reason code:** `DATA-FRESHNESS / ROUTE-SAFETY`

**Rationale:** Current operational information contradicted the AI recommendation. The safer feasible route was selected.

## Escalation

| Field | Entry |
| --- | --- |
| Escalated to | Dispatch Supervisor and Data / AI Lead |
| Severity | Moderate |
| Immediate action | Route corrected; similar recommendations flagged for review |
| Linked issue | `DEF-SAMPLE-001` |

## Outcome

Delivery completed without a reported safety event. Data / AI review determined that the external traffic feed exceeded its proposed freshness threshold.

## Control Demonstration

| Control | Demonstrated Activity |
| --- | --- |
| `AIC-009` | Data freshness concern identified |
| `AIC-020` | Human modified the recommendation |
| `AIC-023` | Decision and rationale recorded |
| `AIC-024` | Defect routed for monitoring review |

**Repository path:** `evidence/02-sample-human-review-decision-record.md`
