# Human Review Decision Log Template

## 1. Decision Record

| Field | Entry |
| --- | --- |
| Decision ID | `[DEC-###]` |
| Transaction ID | `[Transaction ID]` |
| System and model version | `[Version]` |
| Date and time | `[Timestamp]` |
| Reviewer | `[Name / role]` |
| Recommendation type | `[Priority / Assignment / Route / Schedule / Exception]` |
| Delivery or case ID | `[Identifier]` |
| Impact level | `[Standard / Enhanced / High impact / Stop]` |

---

## 2. Review Information

| Review item | Observation |
| --- | --- |
| Recommendation | `[Original output]` |
| Material inputs | `[Inputs reviewed]` |
| Data freshness | `[Current / Stale / Unknown]` |
| Missing or conflicting data | `[None / Describe]` |
| Recommendation rationale | `[System rationale]` |
| Uncertainty or limitations | `[Displayed limitations]` |
| Operational conditions | `[Traffic, weather, vehicle, capacity, timing, and safety]` |
| Affected-party considerations | `[Worker, customer, recipient, or public]` |

---

## 3. Review Checklist

- [ ] Reviewer identity and authority confirmed
- [ ] Use is within approved scope
- [ ] Data quality and freshness reviewed
- [ ] Operational feasibility considered
- [ ] Safety concerns considered
- [ ] Affected-party impact considered
- [ ] Rationale and uncertainty reviewed
- [ ] Alternatives considered when appropriate
- [ ] Escalation and fallback requirements considered

---

## 4. Human Decision

Select one:

- [ ] Approve
- [ ] Modify
- [ ] Reject
- [ ] Escalate
- [ ] Invoke manual fallback
- [ ] Stop or suspend

**Final human-approved action:** `[Action]`

**Reason code:** `[Code]`

**Decision rationale:** `[Explain the decision.]`

---

## 5. Override Information

| Field | Entry |
| --- | --- |
| Was the recommendation overridden? | `[Yes / No]` |
| Override category | `[Safety / Data / Fairness / Operations / Customer / Other]` |
| Original recommendation | `[Original output]` |
| Final action | `[Human-approved action]` |
| Expected effect | `[Describe]` |

---

## 6. Escalation

| Field | Entry |
| --- | --- |
| Escalation required? | `[Yes / No]` |
| Escalation trigger | `[Trigger]` |
| Severity | `[1–4]` |
| Escalated to | `[Role]` |
| Time escalated | `[Timestamp]` |
| Temporary action | `[Action]` |
| Incident or complaint ID | `[ID, if applicable]` |

---

## 7. Outcome

| Field | Entry |
| --- | --- |
| Downstream action completed | `[Yes / No]` |
| Completion time | `[Timestamp]` |
| Outcome known? | `[Yes / No]` |
| Outcome | `[Describe]` |
| Complaint or incident received | `[Yes / No — ID]` |
| Follow-up required | `[Action / owner / date]` |

---

## 8. Supervisor Review

| Field | Entry |
| --- | --- |
| Supervisor review required? | `[Yes / No]` |
| Supervisor | `[Name / role]` |
| Review result | `[Accepted / Returned / Escalated]` |
| Comments | `[Comments]` |
| Review date | `[YYYY-MM-DD]` |

---

## 9. Document Control

**Repository path:** `templates/human-review-decision-log-template.md`  
**Template version:** 1.0
