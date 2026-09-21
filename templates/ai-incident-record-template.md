# AI Incident Record Template

## 1. Incident Identification

| Field | Entry |
| --- | --- |
| Incident ID | `[AI-INC-###]` |
| Incident title | `[Short title]` |
| Date and time detected | `[Timestamp]` |
| Reporter | `[Name / role / contact]` |
| System and use-case IDs | `[AI-SYS-### / UC-###]` |
| Preliminary severity | `[Severity 1–4]` |
| Status | `[Open / Contained / Recovering / Closed]` |
| Incident commander | `[Name / role]` |

---

## 2. Event Description

- **What happened:** `[Description]`
- **How was it detected?** `[Alert / complaint / observation / vendor / audit]`
- **Affected capabilities:** `[Capabilities]`
- **Affected parties:** `[Parties]`
- **Actual harm:** `[Known impact]`
- **Potential harm:** `[Potential impact]`
- **Is the event ongoing?** `[Yes / No / Unknown]`

---

## 3. System Context

| Item | Detail |
| --- | --- |
| Model or service version | `[Version]` |
| Configuration version | `[Version]` |
| Vendor | `[Vendor]` |
| Data sources | `[Sources]` |
| Users and roles | `[Users]` |
| Transaction or decision IDs | `[Identifiers]` |
| Related changes | `[Change IDs]` |

---

## 4. Response Timeline

| Time | Event or action | Owner | Evidence |
| --- | --- | --- | --- |
| `[Timestamp]` | `[Event]` | `[Owner]` | `[Evidence ID]` |

---

## 5. Containment Actions

Select all that apply:

- [ ] Recommendation corrected or rejected
- [ ] Capability restricted
- [ ] User access suspended
- [ ] Credential revoked
- [ ] Integration isolated
- [ ] Data source blocked
- [ ] Version rolled back
- [ ] Manual fallback activated
- [ ] RouteAssist suspended
- [ ] Vendor notified
- [ ] Evidence preserved
- [ ] Affected party protected or assisted

**Containment details:** `[Details]`

---

## 6. Investigation

| Area | Finding |
| --- | --- |
| Root cause | `[Finding]` |
| Contributing factors | `[Factors]` |
| Data behavior | `[Finding]` |
| Model or system behavior | `[Finding]` |
| Human-review behavior | `[Finding]` |
| Control performance | `[Succeeded / Failed / Absent]` |
| Similar prior events | `[Events]` |
| Affected scope and duration | `[Scope]` |

---

## 7. Evidence Register

| Evidence ID | Description | Source | Collected by | Collection time | Storage location |
| --- | --- | --- | --- | --- | --- |
| `[EVD-###]` | `[Description]` | `[Source]` | `[Name]` | `[Timestamp]` | `[Location]` |

---

## 8. Notifications

| Audience | Required? | Date and time | Owner | Status |
| --- | --- | --- | --- | --- |
| `[Audience]` | `[Yes / No]` | `[Timestamp]` | `[Owner]` | `[Status]` |

---

## 9. Corrective Actions

| Action ID | Corrective action | Owner | Due date | POA&M ID | Status |
| --- | --- | --- | --- | --- | --- |
| `[ACT-###]` | `[Action]` | `[Owner]` | `[Date]` | `[POAM-###]` | `[Status]` |

---

## 10. Recovery and Closure

- **Recovery validation:** `[Tests and evidence]`
- **Residual risk:** `[Rating and rationale]`
- **Return-to-service approver:** `[Role / date]`
- **Lessons learned:** `[Lessons]`
- **Final severity:** `[Severity]`
- **Closure approver:** `[Role / date]`
- **Closure date:** `[YYYY-MM-DD]`

---

## 11. Document Control

**Repository path:** `templates/ai-incident-record-template.md`  
**Template version:** 1.0
