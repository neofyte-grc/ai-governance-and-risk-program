# AI Risk Register

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Register owner:** GRC Analyst  
**Approval authority:** AI Governance Committee  
**Assessment stage:** Predeployment  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** Monthly during assessment and pilot; quarterly after stabilization; immediately upon material trigger

---

## 1. Document Purpose

This register identifies, assesses, assigns, treats, and tracks material risks associated with PLG RouteAssist. It applies the scoring rules defined in [`05-ai-risk-assessment-methodology.md`](05-ai-risk-assessment-methodology.md).

The register links risks to affected parties, system capabilities, data, components, flows, owners, planned controls, evidence, evaluations, metrics, and future remediation records.

---

## 2. Rating and Evidence Notice

RouteAssist is in a fictional predeployment stage. Most controls in this register are planned and have not been implemented or tested.

Therefore:

- **Inherent risk** reflects exposure before relying on planned controls.
- **Current risk** remains equal to inherent risk unless an existing condition has verified evidence.
- **Target residual risk** represents the intended rating after controls are implemented and validated.
- A target rating is not a current residual-risk conclusion.
- Production and pilot approvals have not been granted.

### 2.1 Rating bands

| Score | Rating |
| ---: | --- |
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

```text
Risk score = Likelihood × Impact
```

---

## 3. Portfolio Risk Summary

| Risk ID | Risk title | Inherent L×I | Inherent rating | Treatment | Target L×I | Target rating | Owner | Status |
| --- | --- | ---: | --- | --- | ---: | --- | --- | --- |
| `AIR-001` | Inappropriate medical-delivery priority or route | 4×5 = 20 | Critical | Avoid / Reduce | 2×5 = 10 | High | Dispatch Director | Escalated |
| `AIR-002` | Unsafe or impractical route recommendation | 4×5 = 20 | Critical | Reduce | 2×5 = 10 | High | Dispatch Director | Open |
| `AIR-003` | Inaccurate, incomplete, or stale input data | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Data / AI Lead | Open |
| `AIR-004` | Unequal driver or courier assignment outcomes | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Dispatch Director | Open |
| `AIR-005` | Automation bias and ineffective human review | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Dispatch Director | Open |
| `AIR-006` | Unauthorized employment or performance use | 3×4 = 12 | High | Avoid / Reduce | 1×4 = 4 | Low | Human Resources Manager | Open |
| `AIR-007` | Excessive or unauthorized personal-data processing | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Dispatch Director | Open |
| `AIR-008` | Unauthorized access or privileged misuse | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Information Security Lead | Open |
| `AIR-009` | Manipulated inputs, integrations, or outputs | 3×5 = 15 | High | Reduce | 2×5 = 10 | High | Information Security Lead | Open |
| `AIR-010` | Vendor opacity or unannounced material change | 4×4 = 16 | High | Reduce / Transfer | 2×4 = 8 | Moderate | Procurement / Vendor Manager | Open |
| `AIR-011` | Model or data drift degrades recommendations | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Data / AI Lead | Open |
| `AIR-012` | Misleading rationale or uncertainty presentation | 4×3 = 12 | High | Reduce | 2×3 = 6 | Moderate | Data / AI Lead | Open |
| `AIR-013` | Unapproved use-case expansion | 3×4 = 12 | High | Avoid / Reduce | 1×4 = 4 | Low | AI Governance Committee | Open |
| `AIR-014` | Incomplete logging and weak traceability | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | CIO / IT Director | Open |
| `AIR-015` | Monitoring fails to detect harmful patterns | 4×4 = 16 | High | Reduce | 2×4 = 8 | Moderate | Data / AI Lead | Open |
| `AIR-016` | RouteAssist outage or failed manual fallback | 3×4 = 12 | High | Reduce | 2×3 = 6 | Moderate | CIO / IT Director | Open |
| `AIR-017` | Delayed or ineffective AI incident response | 3×5 = 15 | High | Reduce | 2×4 = 8 | Moderate | Incident Manager | Open |
| `AIR-018` | Complaint or dispute mechanisms fail affected parties | 3×4 = 12 | High | Reduce | 2×3 = 6 | Moderate | Customer Service Manager | Open |
| `AIR-019` | Feedback loops reinforce earlier errors or disparities | 3×4 = 12 | High | Reduce | 2×4 = 8 | Moderate | Data / AI Lead | Open |
| `AIR-020` | Governance ownership or approval failure | 3×4 = 12 | High | Reduce | 1×4 = 4 | Low | AI Governance Committee | Open |

---

## 4. Risk Distribution

| Rating | Inherent risks | Target residual risks |
| --- | ---: | ---: |
| Critical | 2 | 0 |
| High | 18 | 3 |
| Moderate | 0 | 14 |
| Low | 0 | 3 |
| **Total** | **20** | **20** |

The target state still includes three High risks because severe impact cannot be eliminated solely through preventive controls. These risks require executive awareness, strong evidence, and continuing monitoring.

---

## 5. Detailed Risk Records

### `AIR-001` — Inappropriate medical-delivery priority or route

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-10` — Safety and operational continuity |
| Secondary domains | Performance, human oversight, legal/contractual, reputation |
| Risk statement | Because RouteAssist may rely on incomplete historical patterns or fail to understand time-sensitive medical-delivery context, it may recommend an inappropriate priority, route, or schedule, resulting in severe delay, service failure, contractual exposure, or harm to a recipient. |
| Sources | `CAP-001`, `CAP-003`, `CAP-005`, `DATA-002`, `OBS-003`, `DF-007` through `DF-012` |
| Affected parties | Healthcare clients, shipment recipients, drivers, dispatchers, PLG |
| Inherent rating | Likelihood 4 × Impact 5 = **20 Critical** |
| Current rating | **20 Critical**; required controls are not yet validated |
| Treatment | Avoid in initial pilot; reduce before any later authorization |
| Planned controls | Exclude medical use from pilot; verified priority indicator; mandatory supervisor review; explicit stop conditions; medical scenario testing; manual fallback; enhanced monitoring; incident escalation |
| Required evidence | Approved pilot boundary, configuration restriction, review logs, test results, training records, fallback exercise, monitoring report, governance approval |
| Target residual | Likelihood 2 × Impact 5 = **10 High** |
| Owner | `ROLE-004` — Dispatch Director |
| Approval | Chief Operating Officer after AI Governance Committee review |
| Uncertainty | High until medical scenarios, vendor behavior, data, interface, and human-review performance are validated |
| Target milestone | Before any medical-delivery use |
| Review trigger | Medical scope change, incident, near miss, threshold breach, material system change |
| Status | Escalated |

### `AIR-002` — Unsafe or impractical route recommendation

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-10` — Safety and operational continuity |
| Secondary domains | Performance, data quality, human oversight, third party |
| Risk statement | Because mapping data may be stale, incomplete, or unable to capture current road, vehicle, weather, or safety conditions, RouteAssist may recommend an unsafe or impractical route, resulting in injury, vehicle damage, shipment loss, delay, or service disruption. |
| Sources | `CAP-003`, `DATA-004`, `DATA-005`, `DF-005`, `OBS-009` |
| Affected parties | Drivers, couriers, recipients, public, customers, PLG |
| Inherent rating | 4 × 5 = **20 Critical** |
| Current rating | **20 Critical** |
| Treatment | Reduce |
| Planned controls | Freshness checks; approved route sources; visible limitations; driver rejection authority; safety rule layer; edge-case testing; alternate-route and manual fallback; safety incident reporting |
| Required evidence | Data freshness logs, provider SLA, interface screenshots, safety test results, driver training, rejection logs, fallback exercise |
| Target residual | 2 × 5 = **10 High** |
| Owner | `ROLE-004` — Dispatch Director |
| Supporting owners | CIO / IT Director, Data / AI Lead, Operations Manager |
| Uncertainty | Moderate to high because real-world conditions change rapidly |
| Target milestone | Before limited pilot |
| Review trigger | Safety event, provider change, new geography, repeated route override, severe weather failure |
| Status | Open |

### `AIR-003` — Inaccurate, incomplete, or stale input data

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-03` — Data quality and governance |
| Secondary domains | Performance, operations, monitoring |
| Risk statement | Because operational data originates from multiple systems with different owners and update frequencies, RouteAssist may process inaccurate, incomplete, conflicting, duplicated, or stale inputs, resulting in unreliable recommendations and downstream operational errors. |
| Sources | `DATA-001` through `DATA-007`, `DF-002` through `DF-006`, `OBS-001` |
| Affected parties | Dispatchers, drivers, couriers, customers, recipients, warehouse personnel |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Data-owner assignments; field allowlist; schema, range, completeness, conflict, and freshness validation; lineage; missing-data block; source-quality monitoring; correction workflow |
| Required evidence | Data dictionary, lineage record, validation configuration, rejected-input logs, data-quality dashboard, owner review |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-006` — Data / AI Lead |
| Uncertainty | Moderate until source data is profiled |
| Target milestone | Before evaluation dataset approval |
| Review trigger | New source, repeated validation failure, data incident, performance degradation |
| Status | Open |

### `AIR-004` — Unequal driver or courier assignment outcomes

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-05` — Fairness and harmful impact |
| Secondary domains | Workforce, data quality, reputation, legal/contractual |
| Risk statement | Because historical assignments and operational proxies may reflect earlier imbalances or incomplete worker context, RouteAssist may repeatedly recommend favorable or unfavorable assignments to particular workers or groups, resulting in unequal workload, opportunity, earnings, travel burden, or trust. |
| Sources | `CAP-002`, `DATA-003`, `DATA-006`, `OBS-002`, `FM-002` |
| Affected parties | PLG-employed drivers and independent couriers |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Approved eligibility factors; prohibited proxy review; workload and opportunity slice analysis; outcome thresholds; supervisor review; dispute process; periodic HR and GRC review |
| Required evidence | Feature inventory, slice definitions, evaluation results, assignment-distribution dashboard, complaint records, corrective-action evidence |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-004` — Dispatch Director |
| Supporting roles | Human Resources Manager, Data / AI Lead, Legal / Privacy Advisor |
| Uncertainty | High until relevant groups and outcome measures are validated |
| Target milestone | Before assignment capability pilot |
| Review trigger | Disparity threshold, complaint pattern, new factor, new worker population |
| Status | Open |

### `AIR-005` — Automation bias and ineffective human review

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-07` — Human factors and oversight |
| Secondary domains | Governance, safety, performance, workforce |
| Risk statement | Because dispatchers work under time pressure and may perceive AI output as authoritative, they may accept recommendations without adequate review, resulting in uncorrected errors, unsafe decisions, harmful outcomes, or unclear accountability. |
| Sources | `FM-001`, `FM-010`, `OBS-005`, human-review workflow |
| Affected parties | Dispatchers, drivers, couriers, customers, recipients, PLG |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Role-based training; relevant context and limitation display; required review fields; override authority; non-retaliation; time-pressure simulation; override and approval-pattern monitoring; supervisor sampling |
| Required evidence | Training completion, interface evaluation, simulation results, review logs, override metrics, supervisor review evidence, worker feedback |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-004` — Dispatch Director |
| Uncertainty | High until human-review simulation and pilot behavior are assessed |
| Target milestone | Before pilot |
| Review trigger | Very low override rate, repeated identical decisions, user complaint, error missed by reviewer |
| Status | Open |

### `AIR-006` — Unauthorized employment or performance use

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-02` — Intended use and misuse |
| Secondary domains | Workforce, privacy, legal/contractual, governance |
| Risk statement | Because RouteAssist generates assignment, workload, location, and decision records, managers may use those records for unauthorized employee ranking, discipline, or performance decisions, resulting in unfair employment effects, privacy harm, policy violations, or loss of trust. |
| Sources | Prohibited-use boundary, `FM-002`, `DATA-003`, `DATA-008` |
| Affected parties | Employees, drivers, couriers, supervisors |
| Inherent rating | 3 × 4 = **12 High** |
| Current rating | **12 High** |
| Treatment | Avoid and reduce |
| Planned controls | Explicit policy prohibition; role-based reporting; field and dashboard restriction; HR approval for secondary use; access monitoring; sanctions; worker dispute channel |
| Required evidence | Policy, access matrix, report inventory, access logs, HR review records, awareness records, investigation records |
| Target residual | 1 × 4 = **4 Low** |
| Owner | `ROLE-013` — Human Resources Manager |
| Uncertainty | Moderate |
| Target milestone | Before pilot access is granted |
| Review trigger | Report request, suspected secondary use, HR complaint, role change |
| Status | Open |

### `AIR-007` — Excessive or unauthorized personal-data processing

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-08` — Privacy and data protection |
| Secondary domains | Security, governance, vendor, legal/contractual |
| Risk statement | Because RouteAssist may process workforce identity, location, workload, customer, recipient, and medical-delivery information, PLG or its vendor may collect, retain, disclose, or reuse more data than necessary, resulting in privacy harm, unauthorized secondary use, contractual exposure, or loss of trust. |
| Sources | `DATA-002` through `DATA-008`, `DF-004`, `DF-007`, `OBS-008` |
| Affected parties | Employees, couriers, customers, recipients, healthcare clients |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Data minimization; approved field allowlist; purpose limitation; restricted free text; retention and deletion rules; vendor data-use prohibition; access control; privacy review |
| Required evidence | Data inventory, field mapping, privacy review, vendor terms, retention schedule, deletion evidence, access logs |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-004` — Dispatch Director as business/data owner |
| Supporting roles | Legal / Privacy Advisor, CIO / IT Director, Procurement / Vendor Manager |
| Uncertainty | High until vendor data practices and final fields are confirmed |
| Target milestone | Before vendor connection or pilot |
| Review trigger | New field, new purpose, new vendor/subprocessor, privacy complaint, data incident |
| Status | Open |

### `AIR-008` — Unauthorized access or privileged misuse

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-09` — Security and integrity |
| Secondary domains | Privacy, governance, operations |
| Risk statement | Because RouteAssist connects sensitive operational data, privileged functions, and multiple user roles, compromised credentials or excessive privileges may allow unauthorized access, configuration changes, data exposure, or fraudulent decisions. |
| Sources | `CMP-008`, `TZ-02`, `TZ-07`, access model |
| Affected parties | PLG, workers, customers, recipients, healthcare clients |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Named accounts; MFA; role-based access; least privilege; privileged access approval; separation of duties; periodic access review; session and administrative logging; timely removal |
| Required evidence | Access matrix, approval records, MFA configuration, privileged-user list, access-review results, termination tests, log samples |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-007` — Information Security Lead |
| Uncertainty | Moderate until vendor administration model is known |
| Target milestone | Before pilot |
| Review trigger | Access anomaly, role change, vendor support request, security incident |
| Status | Open |

### `AIR-009` — Manipulated inputs, integrations, or outputs

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-09` — Security and integrity |
| Secondary domains | Safety, data quality, operations, incident response |
| Risk statement | Because RouteAssist depends on APIs, source systems, external data, and downstream integrations, a malicious or accidental alteration may manipulate input or output, resulting in unsafe routes, improper assignments, delayed deliveries, data exposure, or loss of system trust. |
| Sources | `DF-002` through `DF-016`, `FM-007`, trust boundaries |
| Affected parties | Drivers, couriers, customers, recipients, healthcare clients, PLG |
| Inherent rating | 3 × 5 = **15 High** |
| Current rating | **15 High** |
| Treatment | Reduce |
| Planned controls | Service authentication; encryption; schema and integrity validation; replay protection; secrets management; change control; anomaly alerts; human approval; incident response |
| Required evidence | Architecture, configuration, interface tests, secrets review, alert tests, security logs, incident exercise |
| Target residual | 2 × 5 = **10 High** |
| Owner | `ROLE-007` — Information Security Lead |
| Uncertainty | High until threat modeling and vendor security review are complete |
| Target milestone | Before pilot |
| Review trigger | Vulnerability, anomalous request, vendor incident, unauthorized change, integrity failure |
| Status | Open |

### `AIR-010` — Vendor opacity or unannounced material change

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-12` — Third-party and supply-chain risk |
| Secondary domains | Change management, performance, security, privacy |
| Risk statement | Because PLG may rely on a vendor-hosted AI service with limited visibility, the vendor may change the model, data practices, subprocessors, security, or performance without sufficient notice, invalidating PLG's assessment and controls. |
| Sources | `EE-006`, `TZ-04`, `ARCH-001`, `ARCH-003`, `ARCH-009` |
| Affected parties | All RouteAssist users and affected parties |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce and transfer/share contractually |
| Planned controls | Due diligence; documentation requirements; version identification; advance change notice; incident notice; subprocessor disclosure; audit/evidence rights; service levels; termination and data-return provisions |
| Required evidence | Completed questionnaire, contract, vendor reports, change notices, service reviews, exit test |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-009` — Procurement / Vendor Manager |
| Uncertainty | High until a vendor is selected and reviewed |
| Target milestone | Before contract execution |
| Review trigger | Vendor change, renewal, incident, missed SLA, new subprocessor, evidence gap |
| Status | Open |

### `AIR-011` — Model or data drift degrades recommendations

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-04` — Performance and reliability |
| Secondary domains | Monitoring, change management, data quality |
| Risk statement | Because delivery patterns, traffic, geography, customers, workforce, and source data change over time, RouteAssist performance may drift outside approved thresholds, resulting in increasingly inaccurate or harmful recommendations. |
| Sources | Operating context, `DATA-005`, `DATA-006`, monitoring requirements |
| Affected parties | Dispatchers, drivers, couriers, customers, recipients, PLG |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Baseline metrics; drift indicators; slice monitoring; outcome feedback; alert thresholds; periodic revalidation; version tracking; restriction and rollback procedure |
| Required evidence | Baseline report, monitoring configuration, drift report, alert test, revalidation records, rollback exercise |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-006` — Data / AI Lead |
| Uncertainty | High before baseline and production-like data exist |
| Target milestone | Before pilot and continuously thereafter |
| Review trigger | Threshold breach, new geography, seasonal shift, source change, complaint pattern |
| Status | Open |

### `AIR-012` — Misleading rationale or uncertainty presentation

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-06` — Transparency and explainability |
| Secondary domains | Human factors, performance, reputation |
| Risk statement | Because RouteAssist explanations or confidence information may be incomplete, overly precise, or difficult to interpret, reviewers may misunderstand the basis or uncertainty of a recommendation, resulting in inappropriate reliance or weak challenge. |
| Sources | `OUT-008`, `ARCH-004`, human-review workflow |
| Affected parties | Dispatchers, supervisors, drivers, couriers, customers, recipients |
| Inherent rating | 4 × 3 = **12 High** |
| Current rating | **12 High** |
| Treatment | Reduce |
| Planned controls | Explanation requirements; limitation display; uncertainty labels; usability testing; reviewer training; prohibition on unsupported certainty; feedback channel |
| Required evidence | Interface standard, screenshots, usability study, training records, reviewer feedback, decision-quality results |
| Target residual | 2 × 3 = **6 Moderate** |
| Owner | `ROLE-006` — Data / AI Lead |
| Uncertainty | High until interface and user testing are complete |
| Target milestone | Before human-review simulation |
| Review trigger | Reviewer misunderstanding, misleading vendor output, unexplained error, interface change |
| Status | Open |

### `AIR-013` — Unapproved use-case expansion

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-02` — Intended use and misuse |
| Secondary domains | Governance, change management, legal/contractual |
| Risk statement | Because RouteAssist may appear useful beyond its approved purpose, PLG personnel may expand it to new services, geographies, data, worker decisions, or automated actions without reassessment, resulting in unrecognized risk and invalid controls. |
| Sources | `FM-008`, prohibited uses, rescreening triggers |
| Affected parties | New and existing users and affected parties |
| Inherent rating | 3 × 4 = **12 High** |
| Current rating | **12 High** |
| Treatment | Avoid and reduce |
| Planned controls | AI inventory; approved-use configuration; change intake; policy prohibition; access restriction; periodic use review; reapproval trigger; sanctions |
| Required evidence | Inventory, approved-use record, change tickets, configuration, access logs, periodic review, exception records |
| Target residual | 1 × 4 = **4 Low** |
| Owner | `ROLE-002` — AI Governance Committee |
| Uncertainty | Moderate |
| Target milestone | Before pilot |
| Review trigger | New proposal, new data, new downstream action, new user group, audit finding |
| Status | Open |

### `AIR-014` — Incomplete logging and weak traceability

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-14` — Monitoring and detection |
| Secondary domains | Governance, security, incident response, evidence |
| Risk statement | Because recommendation, version, input, human-review, override, downstream-action, and administrative records may be incomplete or alterable, PLG may be unable to reconstruct decisions, detect problems, investigate incidents, or prove control operation. |
| Sources | `DS-004`, `DS-005`, `DS-007`, `DF-015` through `DF-019`, `ARCH-007` |
| Affected parties | PLG and all parties affected by untraceable decisions |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Required event schema; unique IDs; version capture; time synchronization; centralized logs; tamper protection; retention; access control; completeness monitoring; control testing |
| Required evidence | Log specification, samples, completeness report, retention configuration, access list, tamper test, incident reconstruction exercise |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-005` — CIO / IT Director |
| Uncertainty | High until logging is implemented and tested |
| Target milestone | Before pilot |
| Review trigger | Missing record, failed log transfer, investigation gap, unauthorized log access |
| Status | Open |

### `AIR-015` — Monitoring fails to detect harmful patterns

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-14` — Monitoring and detection |
| Secondary domains | Performance, fairness, human oversight, operations |
| Risk statement | Because aggregate performance metrics may hide subgroup, route, service, human-review, or rare-event failures, PLG may not detect drift, disparity, repeated overrides, or emerging harm before it becomes widespread. |
| Sources | Impact screening, evaluation themes, `OBS-007`, `DF-017` |
| Affected parties | Workers, customers, recipients, healthcare clients, PLG |
| Inherent rating | 4 × 4 = **16 High** |
| Current rating | **16 High** |
| Treatment | Reduce |
| Planned controls | Metric catalog; slice monitoring; override and complaint indicators; thresholds; alert ownership; governance dashboard; periodic deep review; independent sampling |
| Required evidence | Metric definitions, dashboards, threshold approvals, alerts, meeting records, trend reviews, sampling results |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-006` — Data / AI Lead |
| Supporting roles | GRC Analyst, Dispatch Director, Customer Service Manager, HR Manager |
| Uncertainty | High until metrics and baselines are validated |
| Target milestone | Before pilot |
| Review trigger | Missed incident, unexplained complaint, metric blind spot, new affected group |
| Status | Open |

### `AIR-016` — RouteAssist outage or failed manual fallback

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-10` — Safety and operational continuity |
| Secondary domains | Third party, operations, human factors |
| Risk statement | Because PLG may become operationally dependent on RouteAssist or its external services, an outage or degraded service may disrupt dispatch, while an untested manual fallback may fail under real workload and time pressure. |
| Sources | `CMP-012`, failure and fallback paths, `ARCH-006` |
| Affected parties | Dispatchers, drivers, couriers, customers, recipients, warehouse personnel |
| Inherent rating | 3 × 4 = **12 High** |
| Current rating | **12 High** |
| Treatment | Reduce |
| Planned controls | Availability monitoring; dependency status; timeout and safe-failure behavior; documented manual process; staffing and access readiness; continuity exercise; recovery objectives |
| Required evidence | Continuity plan, exercise results, outage logs, staffing plan, recovery test, post-exercise remediation |
| Target residual | 2 × 3 = **6 Moderate** |
| Owner | `ROLE-005` — CIO / IT Director |
| Supporting owner | Operations Manager |
| Uncertainty | Moderate until fallback is exercised at realistic volume |
| Target milestone | Before pilot |
| Review trigger | Outage, failed exercise, staffing change, dependency change, capacity increase |
| Status | Open |

### `AIR-017` — Delayed or ineffective AI incident response

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-15` — Incident response and recovery |
| Secondary domains | Security, safety, privacy, governance, third party |
| Risk statement | Because AI-related incidents may appear as operational errors, data issues, harmful patterns, misuse, or vendor events, PLG may fail to identify, contain, investigate, communicate, or recover promptly, increasing harm and allowing recurrence. |
| Sources | Incident requirements, `DF-018` through `DF-020`, escalation paths |
| Affected parties | All users and affected parties |
| Inherent rating | 3 × 5 = **15 High** |
| Current rating | **15 High** |
| Treatment | Reduce |
| Planned controls | AI incident definition; reporting channel; severity matrix; cross-functional playbooks; vendor notification; evidence preservation; suspension authority; recovery validation; tabletop exercise |
| Required evidence | Incident plan, contact list, vendor terms, tabletop results, sample incident record, recovery approval template |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-016` — Business Continuity / Incident Manager |
| Uncertainty | Moderate to high until exercises test coordination |
| Target milestone | Before pilot |
| Review trigger | Incident, near miss, delayed report, exercise failure, vendor notification gap |
| Status | Open |

### `AIR-018` — Complaint or dispute mechanisms fail affected parties

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-17` — Reputation and stakeholder trust |
| Secondary domains | Fairness, governance, workforce, legal/contractual |
| Risk statement | Because people affected by RouteAssist may not know how a recommendation influenced an outcome or how to challenge it, complaints and disputes may be missed, delayed, or resolved without relevant evidence, allowing harm to continue and reducing trust. |
| Sources | Affected-party register, `ARCH-010`, transparency requirements |
| Affected parties | Drivers, couriers, customers, recipients, healthcare clients |
| Inherent rating | 3 × 4 = **12 High** |
| Current rating | **12 High** |
| Treatment | Reduce |
| Planned controls | Accessible intake; case routing; linkage to recommendation and review record; response timelines; non-retaliation; correction process; trend reporting; escalation criteria |
| Required evidence | Procedure, channel test, sample cases, response-time report, correction records, trend review |
| Target residual | 2 × 3 = **6 Moderate** |
| Owner | `ROLE-014` — Customer Service Manager |
| Supporting roles | HR Manager, Dispatch Director, Legal / Privacy Advisor, GRC Analyst |
| Uncertainty | Moderate until affected-party mechanisms are tested |
| Target milestone | Before pilot |
| Review trigger | Missed complaint, repeated issue, retaliation concern, unresolved dispute, response breach |
| Status | Open |

### `AIR-019` — Feedback loops reinforce earlier errors or disparities

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-03` — Data quality and governance |
| Secondary domains | Fairness, performance, change management |
| Risk statement | Because RouteAssist-influenced assignments and decisions may later enter operational history, future evaluation or model updates may treat those outcomes as independent ground truth, reinforcing earlier errors, preferences, or disparities. |
| Sources | `DATA-006`, `OBS-007`, outcome-monitoring flow |
| Affected parties | Drivers, couriers, customers, recipients |
| Inherent rating | 3 × 4 = **12 High** |
| Current rating | **12 High** |
| Treatment | Reduce |
| Planned controls | Data lineage; decision-source flag; separation of AI-influenced outcomes; curated training and evaluation data; feedback-loop analysis; approval before reuse |
| Required evidence | Data schema, provenance records, dataset review, reuse approval, feedback-loop test, model update record |
| Target residual | 2 × 4 = **8 Moderate** |
| Owner | `ROLE-006` — Data / AI Lead |
| Uncertainty | High until vendor learning behavior and dataset use are known |
| Target milestone | Before outcome data is reused |
| Review trigger | Model update, dataset refresh, vendor learning claim, unexplained pattern persistence |
| Status | Open |

### `AIR-020` — Governance ownership or approval failure

| Field | Assessment |
| --- | --- |
| Primary domain | `TAX-01` — Governance and accountability |
| Secondary domains | Change management, risk acceptance, incident response |
| Risk statement | Because RouteAssist spans business, technical, data, security, privacy, vendor, and operational functions, unclear ownership or conflicting authority may allow decisions, risks, exceptions, changes, or incidents to proceed without accountable approval. |
| Sources | RACI analysis, decision-rights matrix, accountability gaps |
| Affected parties | PLG and all RouteAssist users and affected parties |
| Inherent rating | 3 × 4 = **12 High** |
| Current rating | **12 High** |
| Treatment | Reduce |
| Planned controls | Governance charter; stable role IDs; one accountable owner per activity; approval gates; authority matrix; documented delegation; meeting cadence; dissent and decision records |
| Required evidence | Charter, committee roster, approvals, meeting minutes, risk acceptance, delegation records, periodic RACI review |
| Target residual | 1 × 4 = **4 Low** |
| Owner | `ROLE-002` — AI Governance Committee |
| Uncertainty | Low to moderate |
| Target milestone | Before pilot decision |
| Review trigger | Owner change, missed approval, conflicting instruction, audit finding, severe incident |
| Status | Open |

---

## 6. Risk Interdependencies

| Risk cluster | Related risks | Combined concern |
| --- | --- | --- |
| Critical-delivery cluster | `AIR-001`, `AIR-002`, `AIR-003`, `AIR-005`, `AIR-017` | Poor data, unsafe output, nominal review, and delayed response may combine into severe medical-delivery harm |
| Workforce-impact cluster | `AIR-004`, `AIR-005`, `AIR-006`, `AIR-007`, `AIR-018`, `AIR-019` | Assignment patterns, weak challenge, unauthorized secondary use, and poor dispute handling may create cumulative worker harm |
| Vendor and change cluster | `AIR-009`, `AIR-010`, `AIR-011`, `AIR-013`, `AIR-019` | Vendor opacity or unapproved change may introduce integrity, drift, scope, or feedback-loop risk simultaneously |
| Detection and response cluster | `AIR-014`, `AIR-015`, `AIR-017`, `AIR-018` | Missing logs, weak metrics, and incomplete complaints may prevent timely detection and response |
| Governance cluster | `AIR-006`, `AIR-010`, `AIR-013`, `AIR-020` | Unclear authority may allow prohibited use, weak vendor governance, or unauthorized expansion |
| Continuity cluster | `AIR-002`, `AIR-003`, `AIR-009`, `AIR-016`, `AIR-017` | Data, integration, vendor, or response failures may disrupt operations and overload manual fallback |

Risk owners must consider these clusters when prioritizing controls. A control shared by several risks may become a concentration point and single source of failure.

---

## 7. Treatment Priorities

### Priority 1 — Block critical and prohibited exposure

- Keep medical-delivery prioritization and other Tier 4 uses outside the initial pilot.
- Enforce advisory-only behavior and human approval.
- Prevent unauthorized employment and secondary uses.
- Establish emergency restriction and suspension authority.

### Priority 2 — Establish trustworthy inputs and traceability

- Complete data lineage, quality, freshness, validation, and minimization controls.
- Capture system version, recommendation, rationale, human decision, override, and downstream outcome.
- Protect logs and evidence.

### Priority 3 — Validate system and human performance

- Approve evaluation questions and thresholds before testing.
- Test normal, edge, high-impact, security, failure, and misuse scenarios.
- Test human review under realistic time pressure.
- Analyze workload, opportunity, service, and geographic slices.

### Priority 4 — Govern vendors, changes, and monitoring

- Complete vendor due diligence and contractual protections.
- Define material-change and revalidation rules.
- Establish performance, drift, human-behavior, complaint, incident, and control metrics.

### Priority 5 — Demonstrate response and recovery

- Exercise manual fallback.
- Conduct an AI incident tabletop.
- Validate suspension, investigation, notification, remediation, and return-to-service procedures.

---

## 8. Risk Acceptance Status

No High or Critical risk in this initial register is accepted.

Risk acceptance may occur only after:

- Planned controls are implemented.
- Required evaluations and control tests are complete.
- Evidence supports the residual rating.
- Uncertainty is understood and documented.
- Conditions, monitoring, and expiration or review dates are defined.
- The proper authority approves the risk.

Target residual ratings are planning objectives, not acceptance decisions.

---

## 9. Register Maintenance

The GRC Analyst will coordinate updates when:

- A risk is added, retired, split, combined, rescored, or reassigned.
- A control is implemented or fails.
- Evidence or evaluation results become available.
- A metric threshold is breached.
- A complaint, override pattern, incident, or near miss occurs.
- The use case, capability, data, model, vendor, interface, geography, or affected party changes.
- A governance decision, exception, or risk acceptance is made.
- A POA&M action changes status.

Changes must preserve identifier history and document rating rationale.

---

## 10. NIST AI RMF Alignment

| NIST AI RMF function | Register application |
| --- | --- |
| GOVERN | Assigns risk owners, acceptance authority, escalation, review cadence, and governance responsibilities |
| MAP | Connects risks to use context, affected parties, capabilities, data, components, flows, and impacts |
| MEASURE | Defines evaluation, evidence, monitoring, uncertainty, and residual-risk requirements |
| MANAGE | Prioritizes treatment, restricts critical exposure, tracks target risk, and defines reassessment triggers |

Detailed subcategory mappings will be maintained in [`07-framework-crosswalk.md`](07-framework-crosswalk.md).

---

## 11. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Risk Register |
| Repository path | `docs/06-ai-risk-register.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Monthly during assessment and pilot; quarterly after stabilization; immediately upon material trigger |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-19 | Tommy Marshall | Created the initial RouteAssist risk register with 20 risk records, inherent and target ratings, treatments, owners, evidence requirements, and interdependencies. |

---

## 12. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 13. Portfolio Notice

This register is part of an educational portfolio project based on a fictional organization and fictional AI system. The risks, ratings, controls, evidence, owners, and target residual scores are illustrative.

The register does not provide legal advice, regulatory advice, certification, independent assurance, or a guarantee that a real AI system is safe, fair, secure, compliant, reliable, or suitable for deployment.
