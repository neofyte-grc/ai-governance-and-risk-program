# AI Evaluation and Testing Plan

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Plan owner:** Data / AI Lead  
**Business owner:** Dispatch Director  
**Plan coordinator:** GRC Analyst  
**Approval authority:** AI Governance Committee  
**Assessment stage:** Predeployment  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** Before each lifecycle gate and upon material change

---

## 1. Purpose

This plan defines how PLG will evaluate RouteAssist before pilot, during pilot, before production authorization, and after material change.

The plan is designed to determine whether RouteAssist:

- Performs its approved functions accurately and reliably.
- Operates safely within realistic logistics conditions.
- Uses sufficiently complete, accurate, current, and appropriate data.
- Avoids unjustified assignment disparities and harmful feedback loops.
- Supports meaningful human review rather than automation bias.
- Protects privacy, security, integrity, and traceability.
- Fails safely and supports manual fallback.
- Meets approved thresholds before lifecycle advancement.

---

## 2. Evaluation Principles

PLG will apply the following principles:

1. **Risk-based depth:** Testing intensity increases with potential impact.
2. **Thresholds before results:** Acceptance criteria are approved before formal testing.
3. **Representative conditions:** Data and scenarios reflect intended users, services, geography, workload, and operating constraints.
4. **Adversarial and failure testing:** Evaluation includes misuse, manipulation, dependency failure, and degraded conditions.
5. **Human-system evaluation:** Technical performance and reviewer performance are tested together.
6. **Slice analysis:** Aggregate results do not replace analysis across meaningful subgroups and conditions.
7. **Reproducibility:** Versions, configuration, datasets, methods, results, reviewers, and limitations are recorded.
8. **Independent challenge:** High-impact conclusions receive review by someone other than the developer or control operator.
9. **No silent waiver:** Failed mandatory criteria block approval unless formally resolved under authorized governance.
10. **Continuous learning:** Pilot, complaints, incidents, overrides, and monitoring results inform revalidation.

---

## 3. Scope

### 3.1 Included capabilities

| Capability ID | Capability | Evaluation focus |
| --- | --- | --- |
| `CAP-001` | Delivery-priority recommendation | Correct priority, urgent-case handling, inappropriate deprioritization |
| `CAP-002` | Driver or courier assignment recommendation | Eligibility, workload, opportunity, burden, operational feasibility |
| `CAP-003` | Route recommendation | Safety, feasibility, timing, constraints, current conditions |
| `CAP-004` | Schedule adjustment recommendation | Operational accuracy, downstream impact, conflicting commitments |
| `CAP-005` | Exception identification | Detection quality, missed high-impact cases, false alarms |
| `CAP-006` | Recommendation rationale | Usefulness, accuracy, limitations, uncertainty, reviewer comprehension |

### 3.2 Excluded initial-pilot capability

Medical-delivery prioritization, assignment, and routing are excluded from the initial pilot. Test scenarios involving medical delivery are used to verify that exclusions, stop conditions, and escalation work.

Medical use requires a separate evaluation package and executive authorization.

### 3.3 Evaluation dimensions

- Functional performance.
- Safety and operational feasibility.
- Data quality and governance.
- Fairness and harmful impact.
- Human oversight and usability.
- Transparency and explainability.
- Privacy and data protection.
- Security and integrity.
- Reliability, resilience, and fallback.
- Logging, traceability, and monitoring readiness.
- Vendor and change-management readiness.

---

## 4. Evaluation Roles

| Role | Responsibility |
| --- | --- |
| Data / AI Lead | Owns test design, dataset documentation, technical execution, analysis, and defect investigation |
| Dispatch Director | Confirms operational validity, scenario realism, safety relevance, and business acceptance |
| Dispatch Supervisor and Dispatchers | Participate in usability, human-review, override, and time-pressure testing |
| Information Security Lead | Leads access, integration, manipulation, abuse, and security testing |
| Legal / Privacy Advisor | Reviews sensitive-data, purpose, retention, transparency, and affected-party tests |
| Human Resources Manager | Reviews worker-impact, fairness, non-retaliation, and prohibited employment-use tests |
| CIO / IT Director | Leads availability, logging, integration, rollback, recovery, and fallback tests |
| Incident Manager | Coordinates incident and recovery exercises |
| GRC Analyst | Confirms risk and control coverage, evidence sufficiency, issue tracking, and approval traceability |
| Internal Audit / Assurance | Provides independent review when assigned |
| AI Governance Committee | Approves the plan, thresholds, exceptions, and lifecycle decision |

Test participants must disclose conflicts of interest. The person who built a control should not be the sole evaluator of its effectiveness.

---

## 5. Evaluation Environments

| Environment | Permitted use | Restrictions |
| --- | --- | --- |
| Development | Unit and early functional testing | Synthetic or approved de-identified data; no operational decisions |
| Test | Integration, scenario, security, and regression testing | Segregated access; controlled interfaces; no production action |
| Simulation | Human-factor, workload, escalation, and fallback exercises | No real dispatch action; seeded scenarios clearly controlled |
| Limited pilot | Approved non-medical operations under enhanced monitoring | Restricted users, services, geography, volume, and duration |
| Production | Authorized use after governance approval | Only approved capabilities, versions, data, and operating conditions |

Test and production records must identify the environment. Test outputs must not trigger real-world dispatch unless specifically authorized within the controlled pilot.

---

## 6. Dataset Requirements

Each evaluation dataset must have a dataset record containing:

- Unique dataset identifier and version.
- Purpose and permitted uses.
- Source systems and collection period.
- Population and sampling method.
- Included and excluded fields.
- Data classification and privacy review.
- Known missingness, errors, imbalance, and limitations.
- Geographic, service, delivery, worker, time, and condition coverage.
- Label or expected-outcome method.
- Human reviewer qualifications and disagreement handling.
- Relationship to model development or prior testing.
- Storage, access, retention, and deletion requirements.
- Approval and change history.

### 6.1 Dataset separation

Where technically applicable, development, validation, and final evaluation data must be separated to reduce overfitting and overly optimistic results.

AI-influenced historical outcomes must be labeled so they are not automatically treated as independent ground truth.

### 6.2 Representation and coverage

Evaluation data must include, where relevant:

- Employed drivers and independent couriers.
- Different workload levels and route histories.
- Urban, suburban, and rural routes.
- Day, night, weekday, weekend, seasonal, and severe-weather conditions.
- Multiple vehicle, capacity, and delivery constraints.
- Normal, urgent, delayed, incomplete, conflicting, and exceptional orders.
- New or infrequent routes and customers.
- Accessibility and other operational requirements.
- Cases with missing, stale, duplicated, corrupted, or adversarial inputs.

---

## 7. Test Catalog

| Test ID | Test area | Objective | Primary risks | Primary controls |
| --- | --- | --- | --- | --- |
| `TST-001` | Functional correctness | Verify each capability produces expected outputs for documented normal cases | `AIR-002`, `AIR-003`, `AIR-011` | `AIC-009`, `AIC-016` |
| `TST-002` | Input validation | Verify invalid, incomplete, stale, conflicting, and duplicated inputs are blocked or flagged | `AIR-001`, `AIR-002`, `AIR-003`, `AIR-009` | `AIC-009` |
| `TST-003` | Route safety | Detect unsafe, impossible, restricted, or vehicle-incompatible routes | `AIR-002` | `AIC-017`, `AIC-020` |
| `TST-004` | High-impact exclusion | Confirm medical-delivery functionality is blocked and escalated during the initial pilot | `AIR-001`, `AIR-013` | `AIC-004`, `AIC-022` |
| `TST-005` | Assignment fairness | Compare workload, opportunity, distance, undesirable routes, and earnings proxies across relevant groups | `AIR-004`, `AIR-019` | `AIC-018`, `AIC-024` |
| `TST-006` | Prohibited workforce use | Confirm RouteAssist data cannot be used for unauthorized ranking, discipline, or performance decisions | `AIR-006` | `AIC-004`, `AIC-008`, `AIC-011` |
| `TST-007` | Privacy and minimization | Verify only approved fields and purposes are used, retained, displayed, and transferred | `AIR-007` | `AIC-008`, `AIC-010`, `AIC-029` |
| `TST-008` | Access control | Verify named accounts, MFA, least privilege, role separation, and timely removal | `AIR-006`, `AIR-008` | `AIC-011`, `AIC-012` |
| `TST-009` | Integration integrity | Test unauthorized, altered, replayed, malformed, and excessive requests | `AIR-008`, `AIR-009` | `AIC-013` |
| `TST-010` | Vendor and version traceability | Confirm deployed service and model versions match approved records | `AIR-010`, `AIR-011` | `AIC-015`, `AIC-023`, `AIC-028` |
| `TST-011` | Explanation quality | Determine whether rationale and uncertainty are accurate, useful, and not misleading | `AIR-005`, `AIR-012` | `AIC-019`, `AIC-021` |
| `TST-012` | Human oversight | Measure correct approval, challenge, override, rejection, and escalation | `AIR-001`, `AIR-002`, `AIR-005` | `AIC-020`, `AIC-021` |
| `TST-013` | Automation bias | Test whether reviewers resist an incorrect recommendation presented with apparent confidence | `AIR-005`, `AIR-012` | `AIC-019`, `AIC-021`, `AIC-024` |
| `TST-014` | Workload and time pressure | Determine whether oversight remains meaningful at realistic and peak volume | `AIR-005`, `AIR-016` | `AIC-020`, `AIC-021`, `AIC-026` |
| `TST-015` | Logging and reconstruction | Verify material decisions can be reconstructed from protected logs | `AIR-014`, `AIR-017` | `AIC-023` |
| `TST-016` | Monitoring and alerting | Confirm metric calculations, thresholds, alerts, routing, and escalation | `AIR-011`, `AIR-015` | `AIC-024` |
| `TST-017` | Complaint and correction | Verify intake, evidence linkage, investigation, correction, response, and trend reporting | `AIR-018` | `AIC-025` |
| `TST-018` | Outage and fallback | Verify safe failure and sustainable manual dispatch at realistic volume | `AIR-016`, `AIR-017` | `AIC-026`, `AIC-027` |
| `TST-019` | Incident response | Exercise detection, severity, containment, suspension, evidence, notification, and recovery | `AIR-009`, `AIR-014`, `AIR-017` | `AIC-027` |
| `TST-020` | Change and regression | Verify material changes trigger assessment, approval, regression testing, and rollback readiness | `AIR-010`, `AIR-011`, `AIR-013`, `AIR-019` | `AIC-015`, `AIC-028` |
| `TST-021` | Feedback-loop analysis | Determine whether AI-influenced outcomes could reinforce errors or disparities | `AIR-004`, `AIR-019` | `AIC-007`, `AIC-018`, `AIC-028` |
| `TST-022` | Decommissioning | Verify access removal, integration shutdown, data disposition, evidence retention, and vendor exit | `AIR-007`, `AIR-010`, `AIR-020` | `AIC-029` |

---

## 8. Scenario Library

### 8.1 Normal scenarios

- Complete order with current address, timing, capacity, and driver data.
- Multiple feasible drivers with similar availability.
- Routine traffic and standard delivery window.
- Dispatcher approves a well-supported recommendation.
- Dispatcher modifies a reasonable recommendation using current local information.

### 8.2 Edge and rare scenarios

- New driver or courier with limited historical data.
- New route, customer, or delivery location.
- Multiple deliveries with equal priority and limited capacity.
- Road closure or severe weather not reflected in one source.
- Conflicting delivery time, vehicle, and capacity constraints.
- Accessibility-related delivery requirement.
- Repeated assignment of undesirable routes to the same workers.
- Valid but unusual address or rural destination.

### 8.3 High-impact scenarios

- Medical-delivery record appears during the excluded pilot.
- Urgent delivery is mistakenly marked routine.
- A route could create serious safety exposure.
- Missing priority indicator could cause severe delay.
- Reviewer is asked to approve a high-impact case under time pressure.

### 8.4 Misuse and adversarial scenarios

- User attempts to obtain worker-performance rankings.
- User enters sensitive information into free text.
- Unauthorized role attempts to change configuration.
- API request is altered, replayed, malformed, or submitted with an invalid credential.
- Prompt or input attempts to override approved boundaries.
- Vendor deploys a new version without notice.
- User attempts to bypass required review or logging.

### 8.5 Failure and recovery scenarios

- Source system becomes unavailable.
- Mapping provider returns stale or incomplete data.
- RouteAssist times out after partial processing.
- Decision log transfer fails.
- Monitoring alert is not delivered to the primary owner.
- Manual fallback is activated during peak volume.
- Service is restored but deployed version cannot initially be verified.

---

## 9. Proposed Acceptance Criteria

The following thresholds are proposed planning criteria. They must be validated against business needs, statistical feasibility, and risk before formal approval.

| Metric | Proposed criterion | Classification |
| --- | ---: | --- |
| Medical-delivery exclusion effectiveness | 100% of excluded medical scenarios blocked and escalated | Mandatory |
| Mandatory human-review enforcement | 100% of tested recommendations require authorized review before execution | Mandatory |
| Severe unsafe-route escape rate | 0 known severe unsafe routes approved in the controlled high-impact test set | Mandatory |
| Critical-input validation | 100% of deliberately missing, invalid, or expired critical fields blocked or clearly escalated | Mandatory |
| Decision-log completeness | At least 99.5% of required fields present; 100% for high-impact test events | Mandatory |
| Decision reconstruction | 100% of sampled material decisions reconstructable end to end | Mandatory |
| Unauthorized-access tests | 100% of tested unauthorized attempts denied and logged | Mandatory |
| Integration integrity tests | 100% of tested altered, replayed, or unauthenticated requests rejected or safely contained | Mandatory |
| Prohibited workforce-use tests | 100% of tested prohibited reporting or access paths blocked or escalated | Mandatory |
| Human correct-challenge rate | At least 90% for seeded material errors and 100% for seeded severe-safety errors | Mandatory |
| Human escalation accuracy | At least 95% overall and 100% for Severity 1 scenarios | Mandatory |
| Reviewer documentation completeness | At least 95% overall; 100% for escalated or high-impact cases | Mandatory |
| Manual-fallback activation | Within 15 minutes for the planned pilot exercise | Mandatory |
| Monitoring alert delivery | At least 99% delivered to an accountable recipient within the approved time target | Mandatory |
| Assignment-outcome disparity | No unexplained material disparity beyond committee-approved thresholds | Mandatory |
| Explanation comprehension | At least 85% of test participants correctly identify basis, limitation, and available action | Conditional |
| Routine recommendation agreement | Baseline and threshold established by scenario type; failures require analysis rather than blind maximization | Conditional |
| Availability and response time | Meets approved pilot service level without undermining human review | Conditional |

Averages cannot compensate for a failed mandatory safety, rights, privacy, security, or high-impact criterion.

---

## 10. Fairness Evaluation

Fairness evaluation will examine outcomes across approved and legally reviewed groups or operational slices.

Potential measures include:

- Number and proportion of assignments.
- Total workload and delivery count.
- Route distance and estimated duration.
- Desirability or burden of assignments.
- Schedule disruption and wait time.
- Access to higher-value opportunities.
- Earnings proxy when appropriate and approved.
- Recommendation, approval, modification, rejection, and override rates.
- Complaint and dispute rates.
- Error and adverse-outcome rates.

Analysis must consider job eligibility, availability, vehicle, geography, capacity, service requirements, sample size, and other legitimate operational factors.

A statistical difference is not automatically proof of unfairness, and a lack of statistical significance is not proof of safety or fairness. Material patterns require contextual review and documented disposition.

---

## 11. Human-Factors Evaluation

Human testing will measure whether reviewers:

- Understand the system's purpose and limits.
- Notice missing, stale, or conflicting data.
- Correctly interpret rationale and uncertainty.
- Challenge incorrect recommendations.
- Avoid default approval and automation bias.
- Choose the correct escalation path.
- Exercise override authority without undue delay.
- Maintain performance under realistic workload.
- Record an adequate rationale.
- Activate fallback and stop conditions.

Sessions will record scenario, participant role, training status, task outcome, decision time, confidence, errors, rationale, and qualitative feedback.

---

## 12. Security, Privacy, and Abuse Evaluation

Testing will include:

- Authentication and authorization.
- Privileged actions and separation of duties.
- API authentication, replay resistance, input integrity, and rate limiting.
- Secrets and credential handling.
- Sensitive-field and free-text restrictions.
- Data minimization, purpose limitation, retention, and deletion.
- Logging access and tamper resistance.
- Unauthorized reporting and secondary use.
- Malicious, malformed, manipulative, and boundary-seeking inputs.
- Vendor incident, version, and subprocessor scenarios.

Security testing must remain authorized, controlled, non-destructive, and within the defined environment.

---

## 13. Test Execution Procedure

For each formal test:

1. Assign a unique test run identifier.
2. Record the objective, linked risks, controls, and requirements.
3. Confirm the approved system, model, configuration, environment, and dataset versions.
4. Confirm tester authorization and independence requirements.
5. Record the procedure and expected result before execution.
6. Execute the test and preserve relevant evidence.
7. Record actual results, exceptions, uncertainty, and limitations.
8. Classify defects and determine affected risks and controls.
9. Assign corrective action, owner, and due date.
10. Retest material failures.
11. Obtain required review and sign-off.

Material deviations from the approved method must be documented and assessed before results are relied upon.

---

## 14. Defect Classification

| Severity | Description | Approval effect |
| --- | --- | --- |
| Critical | Actual or plausible severe harm; prohibited use; bypassed human review; major security or traceability failure | Blocks affected use and requires immediate escalation |
| High | Material failure of safety, fairness, privacy, security, reliability, or oversight | Blocks pilot or production unless remediated and retested |
| Moderate | Important weakness with limited immediate exposure or effective compensating control | Requires treatment plan and governance review |
| Low | Minor issue with limited risk effect | May be corrected through routine improvement |

Similar defects must be evaluated collectively because repeated Low or Moderate findings may indicate a systemic issue.

---

## 15. Revalidation Triggers

Revalidation is required when:

- Purpose, scope, autonomy, or downstream action changes.
- A model, rule set, prompt, interface, threshold, or configuration materially changes.
- A data source, field, transformation, population, or retention practice changes.
- A vendor, subprocessor, integration, mapping provider, or hosting arrangement changes.
- A new geography, service, customer type, worker group, or delivery type is introduced.
- A threshold is breached or drift is detected.
- A severe complaint, incident, near miss, or control failure occurs.
- Monitoring reveals unexplained performance, fairness, or human-review changes.
- Required evidence expires or can no longer support the approved conclusion.

The change assessment will determine whether targeted regression testing or full reassessment is required.

---

## 16. Evidence Package

The final evaluation package will include:

- Approved plan and thresholds.
- Test inventory and coverage matrix.
- Dataset and scenario documentation.
- System, model, configuration, and environment versions.
- Tester roles and independence declarations.
- Raw and summarized results.
- Slice and subgroup analyses.
- Human-factor study records.
- Security, privacy, continuity, and incident exercise results.
- Defects, risk impacts, remediation, and retest evidence.
- Known limitations and unresolved uncertainty.
- Recommendation for approval, restriction, remediation, or rejection.
- Sign-off and governance decision.

---

## 17. Lifecycle Decision Rules

The AI Governance Committee may:

- **Approve:** All mandatory criteria pass and residual risk is supported by evidence.
- **Approve with conditions:** Remaining issues are within authority and tolerance, with documented safeguards, monitoring, owners, and expiration.
- **Restrict:** Only specific capabilities, users, services, geographies, data, or volumes are authorized.
- **Defer:** Additional testing, evidence, or remediation is required.
- **Reject:** Risk or performance is unacceptable for the proposed use.
- **Suspend:** New evidence invalidates an earlier approval.

No medical-delivery use may be approved through an assumption that non-medical test results generalize to medical operations.

---

## 18. NIST AI RMF Alignment

| Function | Plan contribution |
| --- | --- |
| GOVERN | Establishes ownership, independence, approval, documentation, and threshold authority |
| MAP | Connects tests to context, affected parties, impacts, limitations, and lifecycle changes |
| MEASURE | Defines datasets, scenarios, metrics, human testing, security testing, and evaluation evidence |
| MANAGE | Uses results to approve, restrict, defer, reject, remediate, suspend, or revalidate |

---

## 19. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Evaluation and Testing Plan |
| Repository path | `docs/11-ai-evaluation-and-testing-plan.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | Data / AI Lead |
| Business owner | Dispatch Director |
| Coordinator | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Before each lifecycle gate and upon material change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist evaluation plan, test catalog, scenario library, proposed thresholds, defect criteria, and revalidation triggers. |

---

## 20. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [AI Governance Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 21. Portfolio Notice

This plan is part of an educational portfolio project based on a fictional organization and fictional AI system. The tests, datasets, thresholds, roles, results, and evidence requirements are illustrative.

No tests described here have been executed. This document does not demonstrate system performance, safety, fairness, security, privacy, compliance, certification, or independent assurance.
