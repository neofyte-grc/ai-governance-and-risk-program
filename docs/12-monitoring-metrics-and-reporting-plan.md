# Monitoring, Metrics, and Reporting Plan

## PLG RouteAssist

**System:** `AI-SYS-001` — PLG RouteAssist  
**Owner:** Data / AI Lead  
**Coordinator:** GRC Analyst  
**Approver:** AI Governance Committee  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Date:** 2026-09-20

---

## 1. Purpose

This plan defines how PLG will monitor RouteAssist performance, safety, fairness, human oversight, security, privacy, resilience, complaints, incidents, and control health after deployment.

Monitoring does not replace predeployment testing. It detects changes, emerging harm, control failures, and invalid assumptions during actual use.

---

## 2. Monitoring Principles

- Measure technical and human-system performance together.
- Review aggregate results and meaningful operational slices.
- Assign every alert to an accountable owner and response target.
- Preserve the data, version, and decision context needed for investigation.
- Use thresholds to trigger investigation, restriction, revalidation, or suspension.
- Treat missing or unreliable monitoring data as a risk condition.
- Do not interpret a single metric without operational context.

---

## 3. Metric Catalog

| Metric ID | Metric | Type | Proposed threshold or trigger | Owner | Cadence |
| --- | --- | --- | --- | --- | --- |
| `MET-001` | Valid recommendation rate | KPI | Baseline established during testing; investigate material decline | Data / AI Lead | Daily; monthly trend |
| `MET-002` | Severe unsafe-route escape count | KRI | Greater than 0 | Dispatch Director | Immediate |
| `MET-003` | Critical-input validation failure rate | KRI | Any unblocked critical-field failure | Data / AI Lead | Continuous |
| `MET-004` | Data freshness compliance | KPI | Below 99% or source-specific approved target | Data / AI Lead | Daily |
| `MET-005` | Medical-use exclusion failures | KRI | Greater than 0 during excluded pilot | Dispatch Director | Immediate |
| `MET-006` | Human-review enforcement | KCI | Below 100% | CIO / IT Director | Continuous |
| `MET-007` | Approval, modification, rejection, and escalation rates | KPI/KRI | Unexpected shift from approved baseline | Dispatch Director | Weekly during pilot |
| `MET-008` | Override rate by user and slice | KRI | Outlier or unexplained material change | Dispatch Director | Weekly during pilot |
| `MET-009` | Correct-challenge rate | KCI | Below 90% overall or below 100% for severe seeded errors | Dispatch Director | Each simulation |
| `MET-010` | Review completion time | KPI | Exceeds approved limit or undermines meaningful review | Dispatch Director | Weekly |
| `MET-011` | Reviewer workload | KRI | Exceeds approved safe-review capacity | Operations Manager | Daily |
| `MET-012` | Assignment-outcome disparity | KRI | Exceeds committee-approved threshold without justified cause | HR Manager | Monthly |
| `MET-013` | Complaint and dispute rate | KRI | Material increase, repeat theme, or severe allegation | Customer Service Manager | Weekly; monthly trend |
| `MET-014` | Decision-log completeness | KCI | Below 99.5%; below 100% for high-impact events | CIO / IT Director | Daily |
| `MET-015` | Decision reconstruction success | KCI | Below 100% for sampled material decisions | GRC Analyst | Monthly sample |
| `MET-016` | Model or data drift | KRI | Approved statistical or operational threshold breached | Data / AI Lead | Continuous; monthly review |
| `MET-017` | Availability | KPI | Below approved pilot or production SLA | CIO / IT Director | Continuous |
| `MET-018` | Manual-fallback activation time | KCI | More than 15 minutes in planned pilot exercise | Operations Manager | Each event or exercise |
| `MET-019` | Security alert count and severity | KRI | Any High or Critical AI-related alert | Information Security Lead | Immediate |
| `MET-020` | Unauthorized access attempts | KRI | Any successful attempt or repeated failed pattern | Information Security Lead | Continuous |
| `MET-021` | Vendor material-change notice compliance | KCI | Any material change without required notice | Procurement / Vendor Manager | Each change |
| `MET-022` | Open overdue High-risk actions | KRI | Greater than 0 without approved exception | GRC Analyst | Weekly |
| `MET-023` | AI incident count and time to contain | KRI/KPI | Any Severity 1 incident or missed response target | Incident Manager | Immediate; monthly trend |
| `MET-024` | Control-test pass rate | KCI | Mandatory control failure or declining trend | GRC Analyst | Monthly or per test cycle |

Thresholds are proposed until formally approved. Baselines must be established before unexplained deviations can be evaluated reliably.

---

## 4. Required Monitoring Slices

Where sample size and lawful use permit, metrics will be analyzed by:

- Employed driver and independent courier.
- User, team, supervisor, and location.
- Service and delivery type.
- Urban, suburban, and rural geography.
- Route length, shift, time, weather, and workload.
- New and established workers.
- Recommendation type and system version.
- Approved high-impact category.

Small samples, confounders, and data limitations must be documented. Aggregate performance must not conceal localized harm.

---

## 5. Alert Response

| Level | Condition | Required response |
| --- | --- | --- |
| Critical | Severe harm, medical-exclusion failure, bypassed review, or major compromise | Stop affected use and initiate incident response immediately |
| High | Mandatory threshold failure, material disparity, unapproved change, or major control failure | Restrict affected capability and investigate within 30 minutes |
| Moderate | Repeated degradation, localized failure, or warning threshold | Assign investigation within one business day |
| Low | Minor deviation or isolated non-material error | Track through routine improvement |

Alerts must record:

- Metric and threshold.
- Affected capability, users, delivery type, and period.
- System and model version.
- Detection and acknowledgment time.
- Accountable owner.
- Immediate action.
- Investigation and disposition.
- Linked incident, risk, control, or POA&M item.

---

## 6. Monitoring Workflow

1. Collect approved source data.
2. Validate source completeness and freshness.
3. Calculate metrics using controlled logic.
4. Compare results with thresholds and baselines.
5. Generate and route alerts.
6. Acknowledge and triage the alert.
7. Investigate the affected scope.
8. Apply corrective, restrictive, or incident-response action.
9. Record the disposition and supporting evidence.
10. Review trends through the governance process.
11. Update risks, controls, tests, or thresholds where warranted.

---

## 7. Reporting Cadence

| Audience | Content | Cadence |
| --- | --- | --- |
| Dispatch Supervisor | Review behavior, overrides, workload, and safety exceptions | Daily during pilot |
| Control owners | Assigned alerts, control failures, and overdue actions | Weekly |
| AI Governance Committee | Risk posture, thresholds, trends, complaints, incidents, vendor changes, and decisions | Monthly during pilot; quarterly thereafter |
| Chief Operating Officer | Critical and High risks, severe incidents, acceptance decisions, and roadmap | Quarterly and upon severe trigger |
| Internal Audit / Assurance | Control evidence, trends, exceptions, and remediation | Risk-based; at least annually |

Severe events are reported immediately and do not wait for a scheduled report.

---

## 8. Dashboard Requirements

The governance dashboard should display:

- Current system and model version.
- Approved lifecycle stage and use boundaries.
- Open risks by rating.
- Open and overdue POA&M actions.
- Performance and data-quality trends.
- Safety events and near misses.
- Assignment-outcome measures by approved slice.
- Human-review and override behavior.
- Complaint and dispute trends.
- Security and privacy alerts.
- Availability, fallback, and recovery activity.
- Vendor changes and SLA performance.
- Control-testing results.
- Expiring exceptions and risk acceptances.

Dashboard access must be role-based, and sensitive workforce or personal information must be minimized.

---

## 9. Data Quality and Metric Validation

Metric owners must document:

- Calculation logic.
- Data sources.
- Population and exclusions.
- Refresh frequency.
- Accountable owner.
- Threshold and rationale.
- Known limitations.
- Change history.

PLG will periodically test:

- Source completeness and timeliness.
- Calculation accuracy and reproducibility.
- Alert generation and delivery.
- Dashboard access and version control.
- Links between metrics, risks, controls, incidents, and actions.
- Whether monitoring creates unnecessary privacy or workforce risk.

---

## 10. Governance Actions

Monitoring may result in:

- Continued operation.
- Increased observation or sampling.
- Corrective training.
- Data or configuration correction.
- Targeted testing or full revalidation.
- Capability, user, geography, service, or volume restriction.
- Manual fallback, rollback, or suspension.
- Updated risk ratings or risk acceptance.
- Vendor remediation or contract escalation.
- New or revised POA&M actions.

Averages cannot compensate for a failed mandatory safety, rights, privacy, security, or high-impact threshold.

---

## 11. Related Risks and Controls

| Area | Risks | Controls |
| --- | --- | --- |
| Data quality and drift | `AIR-003`, `AIR-011`, `AIR-019` | `AIC-007`, `AIC-009`, `AIC-024`, `AIC-028` |
| Fairness and workforce impact | `AIR-004`, `AIR-006`, `AIR-018` | `AIC-018`, `AIC-024`, `AIC-025` |
| Human oversight | `AIR-005`, `AIR-012` | `AIC-019`, `AIC-020`, `AIC-021`, `AIC-024` |
| Logging and detection | `AIR-014`, `AIR-015` | `AIC-023`, `AIC-024`, `AIC-030` |
| Continuity and incidents | `AIR-016`, `AIR-017` | `AIC-026`, `AIC-027` |
| Vendor and change | `AIR-010`, `AIR-013` | `AIC-014`, `AIC-015`, `AIC-028` |

---

## 12. NIST AI RMF Alignment

| Function | Contribution |
| --- | --- |
| GOVERN | Assigns metric owners, reporting, escalation, and evidence accountability |
| MAP | Maintains operational context through affected-party and operating-condition slices |
| MEASURE | Defines indicators, thresholds, validation, feedback, and trend analysis |
| MANAGE | Converts threshold breaches into investigation, treatment, restriction, or suspension |

---

## 13. Document Control

| Field | Value |
| --- | --- |
| Document title | Monitoring, Metrics, and Reporting Plan |
| Repository path | `docs/12-monitoring-metrics-and-reporting-plan.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | Data / AI Lead |
| Coordinator | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Monthly during pilot; quarterly after stabilization; upon material change |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist monitoring, metric, alert, dashboard, and reporting requirements. |

---

## 14. Related Documents

- [AI Risk Register](06-ai-risk-register.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 15. Portfolio Notice

This fictional portfolio plan contains illustrative metrics and proposed thresholds. It does not demonstrate actual monitoring, compliance, safety, or system performance.
