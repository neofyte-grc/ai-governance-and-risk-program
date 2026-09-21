# AI Impact Assessment Template

## 1. Assessment Record

| Field | Response |
| --- | --- |
| Assessment ID | `[AIA-###]` |
| System ID | `[AI-SYS-###]` |
| Use-case ID | `[UC-###]` |
| System name | `[Name]` |
| Business owner | `[Role]` |
| Assessor | `[Name / role]` |
| Assessment date | `[YYYY-MM-DD]` |
| Lifecycle stage | `[Design / Pilot / Production / Change / Retirement]` |

---

## 2. Purpose and Boundaries

- **Intended purpose:** `[Purpose]`
- **In-scope capabilities:** `[Capabilities]`
- **Prohibited uses:** `[Uses]`
- **Users:** `[Users]`
- **Affected parties:** `[Parties]`
- **Geography and jurisdictions:** `[Locations]`
- **Human role:** `[Review, decision, override, and escalation]`

---

## 3. Impact Analysis

| Domain | Potential benefit | Potential harm | Severity | Affected parties | Safeguards |
| --- | --- | --- | --- | --- | --- |
| Safety | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |
| Fairness | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |
| Privacy | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |
| Security | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |
| Workforce | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |
| Operations | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |
| Legal / contractual | `[Benefit]` | `[Harm]` | `[1–5]` | `[Parties]` | `[Controls]` |

---

## 4. Data Assessment

| Question | Response |
| --- | --- |
| What data is used? | `[Categories]` |
| Is sensitive data involved? | `[Yes / No — explain]` |
| Is each field necessary? | `[Assessment]` |
| Are source, quality, lineage, and freshness documented? | `[Status]` |
| Could historical data reflect bias? | `[Assessment]` |
| Will AI-influenced outcomes be reused? | `[Yes / No — safeguards]` |

---

## 5. Human Oversight

- **Reviewer:** `[Role]`
- **Information available:** `[Inputs, rationale, uncertainty, and limitations]`
- **Actions available:** `[Approve / modify / reject / escalate / stop]`
- **Time and workload constraints:** `[Assessment]`
- **Training required:** `[Training]`
- **Fallback:** `[Manual process]`

---

## 6. Risk-Tier Determination

| Factor | Rating | Rationale |
| --- | --- | --- |
| Scale | `[Low / Medium / High]` | `[Rationale]` |
| Data sensitivity | `[Low / Medium / High]` | `[Rationale]` |
| Potential consequence | `[Low / Medium / High / Severe]` | `[Rationale]` |
| Reversibility | `[Easy / Moderate / Difficult]` | `[Rationale]` |
| Human control | `[Strong / Moderate / Weak]` | `[Rationale]` |
| Final impact tier | `[Tier 1–4]` | `[Rationale]` |

---

## 7. Required Controls

| Control area | Requirement | Owner | Status |
| --- | --- | --- | --- |
| Governance | `[Requirement]` | `[Owner]` | `[Status]` |
| Data | `[Requirement]` | `[Owner]` | `[Status]` |
| Human oversight | `[Requirement]` | `[Owner]` | `[Status]` |
| Security | `[Requirement]` | `[Owner]` | `[Status]` |
| Privacy | `[Requirement]` | `[Owner]` | `[Status]` |
| Monitoring | `[Requirement]` | `[Owner]` | `[Status]` |
| Incident response | `[Requirement]` | `[Owner]` | `[Status]` |

---

## 8. Assessment Decision

| Field | Response |
| --- | --- |
| Decision | `[Approve / Conditional / Restrict / Defer / Reject]` |
| Required actions | `[Actions]` |
| Monitoring conditions | `[Conditions]` |
| Reassessment triggers | `[Triggers]` |
| Approver | `[Name / role]` |
| Date | `[YYYY-MM-DD]` |

---

## 9. Document Control

**Repository path:** `templates/ai-impact-assessment-template.md`  
**Template version:** 1.0
