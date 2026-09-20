# Gap Assessment and Plan of Action and Milestones

## PLG RouteAssist

**System:** `AI-SYS-001` — PLG RouteAssist  
**Owner:** GRC Analyst  
**Approver:** AI Governance Committee  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Date:** 2026-09-20

---

## 1. Purpose

This document compares the RouteAssist current state with its required target state and records prioritized remediation in a Plan of Action and Milestones (POA&M).

RouteAssist is predeployment. A documented control design is not treated as an implemented or effective control.

---

## 2. Status Definitions

| Status | Meaning |
| --- | --- |
| Open | Work has not started |
| In progress | Remediation has started but is incomplete |
| Pending validation | Implementation is complete but testing is not |
| Closed | Evidence demonstrates completion and authorized closure |
| Accepted | Authorized, time-limited risk acceptance exists |
| Deferred | Work is postponed by documented authority and rationale |

---

## 3. Gap Summary

| Priority | Count | Governance meaning |
| --- | ---: | --- |
| Critical | 2 | Blocks pilot or affected use |
| High | 9 | Requires remediation before pilot unless formally excluded from scope |
| Moderate | 5 | Requires assigned treatment and governance tracking |
| Low | 0 | None identified in the initial predeployment review |
| **Total** | **16** | — |

---

## 4. POA&M Register

| POA&M ID | Priority | Gap and risk | Corrective action | Owner | Target milestone | Status |
| --- | --- | --- | --- | --- | --- | --- |
| `POAM-001` | Critical | Medical-delivery capability is not safely authorized; `AIR-001` | Enforce pilot exclusion, test blocking and escalation, and require separate executive approval for future use | Dispatch Director | Before pilot | Open |
| `POAM-002` | Critical | Route safety performance and edge-case behavior are unvalidated; `AIR-002` | Complete route-safety scenarios, define mandatory thresholds, correct defects, and retest | Dispatch Director | Before pilot | Open |
| `POAM-003` | High | Governance charter and approval gates are unapproved; `AIR-020` | Approve charter, committee membership, quorum, decision rights, and lifecycle gates | Committee Chair | Before pilot decision | Open |
| `POAM-004` | High | Data lineage, quality profile, and owner approval are incomplete; `AIR-003`, `AIR-007` | Complete data inventory, lineage, allowlist, profiling, validation, and privacy review | Data / AI Lead | Before formal evaluation | Open |
| `POAM-005` | High | Vendor evidence and contractual protections are unavailable; `AIR-010` | Complete due diligence, contract review, change-notice, incident, audit, data-use, and exit terms | Procurement / Vendor Manager | Before contract or connection | Open |
| `POAM-006` | High | Access and privileged-administration design are untested; `AIR-008` | Implement MFA, RBAC, least privilege, privileged approval, logging, and access-review tests | Information Security Lead | Before pilot access | Open |
| `POAM-007` | High | Integration integrity and adversarial resistance are untested; `AIR-009` | Test authentication, encryption, schema, replay, manipulation, secrets, rate limiting, and safe failure | Information Security Lead | Before pilot | Open |
| `POAM-008` | High | Fairness measures, slices, and thresholds are not approved; `AIR-004`, `AIR-019` | Define relevant slices and legitimate factors; evaluate workload, opportunity, burden, overrides, and complaints | Human Resources Manager | Before assignment pilot | Open |
| `POAM-009` | High | Human-review effectiveness is unproven; `AIR-005`, `AIR-012` | Complete training, usability, automation-bias, time-pressure, override, and escalation simulations | Dispatch Director | Before pilot | Open |
| `POAM-010` | High | Required logs and reconstruction capability are not implemented; `AIR-014` | Implement event schema, version capture, human-decision logs, protection, completeness alerts, and reconstruction testing | CIO / IT Director | Before pilot | Open |
| `POAM-011` | High | Monitoring baselines, thresholds, and alert routing are not operational; `AIR-011`, `AIR-015` | Approve metric catalog, implement dashboard and alerts, validate calculations, and test routing | Data / AI Lead | Before pilot | Open |
| `POAM-012` | High | Incident and fallback procedures are unexercised; `AIR-016`, `AIR-017` | Conduct manual-fallback and AI-incident tabletop exercises; remediate and retest gaps | Business Continuity / Incident Manager | Before pilot | Open |
| `POAM-013` | Moderate | Complaint, dispute, and correction process is not tested; `AIR-018` | Implement accessible intake, evidence linkage, service targets, correction, non-retaliation, and trend review | Customer Service Manager | Before pilot | Open |
| `POAM-014` | Moderate | Retention, deletion, vendor exit, and decommissioning are incomplete; `AIR-007`, `AIR-010` | Approve schedules and exit checklist; validate deletion, export, access removal, and record preservation | CIO / IT Director | Before production | Open |
| `POAM-015` | Moderate | Independent assurance scope is undefined; `AIR-015`, `AIR-020` | Approve risk-based assurance plan and closure-testing requirements | Internal Audit / Assurance | Before production | Open |
| `POAM-016` | Moderate | Legal, privacy, employment, and contractual obligations register is incomplete | Document applicable obligations, owners, evidence, review triggers, and unresolved questions | Legal / Privacy Advisor | Before vendor connection | Open |

---

## 5. Milestone Dependencies

| Milestone | Required completed items |
| --- | --- |
| Evaluation readiness | `POAM-003`, `POAM-004`, approved test plan, and approved thresholds |
| Vendor connection | `POAM-005`, `POAM-006`, `POAM-007`, and `POAM-016` |
| Limited non-medical pilot | `POAM-001` through `POAM-013`, with no unresolved blocking failure |
| Production authorization | Pilot evidence plus `POAM-014`, `POAM-015`, accepted residual risk, and committee approval |
| Medical-delivery consideration | Separate assessment, all related control evidence, successful high-impact testing, and executive approval |

---

## 6. POA&M Management Requirements

Each POA&M item must include:

- A unique identifier.
- The related gap, risk, control, finding, or incident.
- Priority and rationale.
- Corrective action.
- Accountable owner.
- Supporting roles.
- Dependencies.
- Required evidence.
- Target milestone and due date.
- Current status.
- Blockers or resource constraints.
- Risk-acceptance or exception information.
- Validation and closure approval.

POA&M identifiers must not be reused. Closed or canceled records must remain available for historical traceability.

---

## 7. Closure Requirements

A POA&M item may close only when:

- The corrective action is implemented.
- Required evidence is complete and retained.
- Design and operating effectiveness are tested as applicable.
- Related risks and control statuses are updated.
- Remaining risk is within tolerance or formally accepted.
- An authorized reviewer approves closure.

The action owner may not be the sole validator for a High or Critical item.

---

## 8. Evidence Requirements

Acceptable closure evidence may include:

- Approved governance records.
- Configuration exports.
- Access-control records.
- Test scripts and results.
- Evaluation reports.
- Log samples and completeness reports.
- Training and competency records.
- Vendor contracts and assurance evidence.
- Exercise or tabletop reports.
- Monitoring dashboards and alert tests.
- Privacy, legal, HR, or security review.
- Retest results.
- Risk-acceptance or exception records.

Screenshots alone should not be used when stronger system-generated or independently verifiable evidence is available.

---

## 9. Due-Date and Escalation Rules

- Overdue Critical items are escalated immediately to the Chief Operating Officer.
- Overdue High items are reported to the AI Governance Committee.
- Scope, due-date, owner, or priority changes require documented approval.
- Repeated extensions require root-cause review.
- A closed item reopens when evidence fails, conditions change, or remediation proves ineffective.
- A target date does not authorize operation past a failed lifecycle gate.
- Resource constraints must be documented but do not automatically justify risk acceptance.

---

## 10. Risk-Acceptance Rules

Risk acceptance is not the same as POA&M closure.

An accepted POA&M item must document:

- The unresolved condition.
- Related risks and controls.
- Business rationale.
- Compensating controls.
- Approved operating boundaries.
- Monitoring requirements.
- Accountable owner.
- Approval authority.
- Acceptance and expiration dates.
- Conditions requiring immediate reconsideration.

Critical residual risk is outside PLG’s normal appetite and is not routinely accepted.

---

## 11. Reporting

The monthly POA&M report will show:

- Items by priority and status.
- Due and overdue actions.
- Blocked lifecycle gates.
- Dependencies and resource constraints.
- Evidence awaiting validation.
- Risk changes.
- Expiring exceptions and risk acceptances.
- Recently closed and reopened items.
- Decisions needed from leadership.

Severe blockers and missed Critical milestones are reported immediately.

---

## 12. Governance Review Questions

The AI Governance Committee should ask:

1. Which gaps currently prevent safe pilot or production use?
2. Are owners and due dates realistic?
3. Which actions depend on vendor evidence or technical resources?
4. Are planned controls being credited before implementation?
5. Does evidence demonstrate effectiveness or only completion?
6. Have similar findings been grouped into a systemic issue?
7. Has any remediation introduced a new risk?
8. Are exceptions accumulating or repeatedly extended?
9. Do closed items require continued monitoring?
10. Does the remaining risk stay within approved boundaries?

---

## 13. NIST AI RMF Alignment

| Function | Contribution |
| --- | --- |
| GOVERN | Assigns accountable owners, approval authority, evidence expectations, and escalation |
| MAP | Links gaps to context, impacts, affected parties, and lifecycle stage |
| MEASURE | Requires validation and sufficient evidence before closure |
| MANAGE | Prioritizes remediation and tracks risk treatment to completion |

---

## 14. Document Control

| Field | Value |
| --- | --- |
| Document title | Gap Assessment and Plan of Action and Milestones |
| Repository path | `docs/15-gap-assessment-and-poam.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Monthly and upon material change |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist gap assessment and 16-item POA&M. |

---

## 15. Related Documents

- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [AI Governance Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Third-Party and Vendor AI Risk Review](14-third-party-and-vendor-ai-risk-review.md)
- [Executive Summary and Recommendations](16-executive-summary-and-recommendations.md)

---

## 16. Portfolio Notice

This fictional POA&M represents planned remediation rather than completed implementation or verified closure.

It does not establish compliance, certification, legal sufficiency, control effectiveness, or authorization for a real AI system.
