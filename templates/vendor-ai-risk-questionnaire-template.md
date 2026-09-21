# Vendor AI Risk Questionnaire Template

## 1. Vendor and Service Information

| Field | Response |
| --- | --- |
| Review ID | `[VDR-###]` |
| Vendor | `[Legal name]` |
| Service | `[Name]` |
| Version | `[Version]` |
| Primary contact | `[Name / contact]` |
| PLG owner | `[Role]` |
| Review date | `[YYYY-MM-DD]` |
| Proposed use | `[Use case]` |

---

## 2. AI Governance

1. Who is accountable for AI governance and risk management?
2. What policies govern intended use, prohibited use, fairness, safety, privacy, security, and incidents?
3. How are risks identified, assessed, treated, accepted, and monitored?
4. How may customers report harmful output or request correction?
5. What independent assurance covers the service?

**Vendor response:** `[Response and evidence references]`

---

## 3. Model and System

1. What model or decision technology is used?
2. How are model and service versions identified?
3. What are the intended uses, prohibited uses, and known limitations?
4. What customer controls or configurations are required?
5. What explanations or uncertainty information are available?
6. What system dependencies are required?
7. Can the service operate safely when a dependency fails?

**Vendor response:** `[Response and evidence references]`

---

## 4. Data Governance

1. What customer data is collected, generated, stored, or transferred?
2. Is customer data used for training, tuning, evaluation, or product improvement?
3. What are the data sources, rights, provenance, quality, and representation practices?
4. Where is data processed and stored?
5. What are the retention, deletion, export, and backup practices?
6. How is customer data separated?
7. How are AI-influenced outcomes identified?

**Vendor response:** `[Response and evidence references]`

---

## 5. Performance, Safety, and Fairness

1. What metrics, test datasets, and thresholds are used?
2. How does performance vary across operating conditions and relevant groups?
3. How are edge, rare, high-impact, and misuse scenarios tested?
4. How are unsafe or unsupported outputs blocked or escalated?
5. How are drift, degradation, and harmful disparities detected?
6. What known failure modes exist?
7. What corrective or rollback mechanisms are available?

**Vendor response:** `[Response and evidence references]`

---

## 6. Human Oversight and Transparency

1. What information is presented to human reviewers?
2. How are rationale, confidence, uncertainty, and limitations communicated?
3. Can users modify, reject, override, or escalate output?
4. Can required review be bypassed?
5. How is user activity logged?
6. What human-factor or usability testing has been conducted?

**Vendor response:** `[Response and evidence references]`

---

## 7. Security and Privacy

1. How are authentication, authorization, privileged access, encryption, secrets, logs, and vulnerabilities managed?
2. What security and privacy assurance reports are available?
3. How are incidents detected, contained, investigated, and reported?
4. How are privacy requests and legal holds supported?
5. Has the service experienced a material security, privacy, safety, or AI incident?
6. How are administrative and support activities logged?
7. What penetration, application-security, or integration testing is performed?

**Vendor response:** `[Response and evidence references]`

---

## 8. Subprocessors and Supply Chain

| Subprocessor | Function | Location | Data access | Critical dependency | Change notice |
| --- | --- | --- | --- | --- | --- |
| `[Name]` | `[Function]` | `[Location]` | `[Access]` | `[Yes / No]` | `[Terms]` |

---

## 9. Change Management

1. How much advance notice is provided for material changes?
2. Are release notes, impact information, and updated limitations provided?
3. Can PLG delay, test, reject, or roll back a change?
4. How are emergency changes communicated?
5. How long are prior versions supported?
6. How are model and configuration changes identified?
7. What regression testing occurs before release?

**Vendor response:** `[Response and evidence references]`

---

## 10. Incident Response

1. What events trigger customer notification?
2. What notification timeframe applies?
3. What evidence will be provided?
4. How will the vendor support investigation and correction?
5. How are affected versions and customers identified?
6. How are lessons learned communicated?
7. What authority does PLG have to suspend or disconnect the service?

**Vendor response:** `[Response and evidence references]`

---

## 11. Resilience and Exit

1. What availability and recovery commitments apply?
2. When was disaster recovery last tested?
3. What happens when the AI service or dependency fails?
4. How can PLG export data and configurations?
5. How is deletion verified after termination?
6. What transition assistance is available?
7. What risks may prevent or delay vendor exit?

**Vendor response:** `[Response and evidence references]`

---

## 12. Evidence Register

| Evidence ID | Document | Period or version | Reviewer | Result | Expiration |
| --- | --- | --- | --- | --- | --- |
| `[EVD-###]` | `[Document]` | `[Period]` | `[Reviewer]` | `[Result]` | `[Date]` |

---

## 13. Findings

| Finding ID | Finding | Severity | Required action | Owner | Due date | Status |
| --- | --- | --- | --- | --- | --- | --- |
| `[VFN-###]` | `[Finding]` | `[Critical / High / Moderate / Low]` | `[Action]` | `[Owner]` | `[Date]` | `[Status]` |

---

## 14. Decision

| Decision field | Response |
| --- | --- |
| Overall vendor risk | `[Critical / High / Moderate / Low]` |
| Decision | `[Approve / Conditional / Defer / Reject]` |
| Approved scope | `[Scope]` |
| Conditions | `[Conditions]` |
| Required contract terms | `[Terms]` |
| Open POA&M items | `[POAM-###]` |
| Approver | `[Role]` |
| Decision date | `[YYYY-MM-DD]` |
| Next review | `[YYYY-MM-DD]` |

---

## 15. Document Control

**Repository path:** `templates/vendor-ai-risk-questionnaire-template.md`  
**Template version:** 1.0
