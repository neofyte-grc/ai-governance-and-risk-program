# AI Risk Assessment Methodology

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Methodology owner:** GRC Analyst  
**Approval authority:** AI Governance Committee  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** Annually and upon material methodology, system, use-case, or risk-tolerance change

---

## 1. Document Purpose

This document establishes the method Peachtree Logistics Group (PLG) uses to identify, analyze, evaluate, treat, accept, monitor, and communicate risks associated with RouteAssist.

It provides the scoring and decision rules for [`06-ai-risk-register.md`](06-ai-risk-register.md). The methodology is designed to support consistent prioritization while preserving professional judgment, affected-party analysis, and escalation of severe risks that may not be adequately represented by a numeric score.

---

## 2. Methodology Objectives

The methodology is intended to:

1. Create repeatable and understandable AI risk assessments.
2. Connect the use case, stakeholders, data, system components, impacts, controls, tests, evidence, metrics, and remediation actions.
3. Evaluate both organizational harm and harm to affected people or groups.
4. Distinguish inherent risk from residual risk.
5. Make uncertainty and missing information visible.
6. Assign accountable risk owners.
7. Support proportionate treatment and approval decisions.
8. Prevent a favorable average score from hiding a severe impact.
9. Define when risks must be escalated, restricted, avoided, or independently challenged.
10. Support NIST AI RMF GOVERN, MAP, MEASURE, and MANAGE activities.

---

## 3. Scope

The methodology applies to risks arising from:

- Intended use
- Foreseeable misuse
- Prohibited use
- Users and affected parties
- Data collection, quality, lineage, representativeness, retention, and use
- Model or AI-service behavior
- Performance, reliability, robustness, and uncertainty
- Human review, automation bias, override, and escalation
- Privacy and sensitive information
- Cybersecurity and system integrity
- Safety and time-sensitive operations
- Workforce and economic effects
- Fairness and harmful differential effects
- Customer, recipient, and healthcare-client outcomes
- Third-party vendors and external dependencies
- Change management and revalidation
- Monitoring, complaints, incidents, and recovery
- Legal, contractual, governance, and reputational exposure

The methodology does not replace specialist legal, privacy, safety, security, data-science, or audit methods.

---

## 4. Core Risk Concepts

### 4.1 Risk

Risk is the effect of uncertainty on PLG's objectives, affected parties, operations, assets, obligations, or trust.

### 4.2 Inherent risk

Inherent risk is the level of risk before considering the effectiveness of controls intended to reduce that risk.

Existing conditions may be described for context, but the inherent rating should not assume that proposed or untested controls operate effectively.

### 4.3 Residual risk

Residual risk is the risk remaining after relevant controls are implemented and supported by sufficient evidence.

A planned control does not reduce residual risk until its design is approved and its operation is supported by evidence appropriate to the decision.

### 4.4 Risk owner

The risk owner is the role with authority, accountability, and resources to manage the risk. The GRC Analyst coordinates assessment but does not automatically own every risk.

### 4.5 Control owner

The control owner is accountable for the design, implementation, maintenance, evidence, and remediation of a specific control.

### 4.6 Affected party

An affected party is a person, group, organization, or community that may experience benefit or harm from RouteAssist, even without directly using the system.

---

## 5. Risk Identification Sources

Risk identification will draw from:

- Project overview and scope
- Organization and AI use-case profile
- Stakeholder and affected-party analysis
- AI inventory and impact screening
- Data-flow and system-context analysis
- Business-process walkthroughs
- Interviews and workshops
- Vendor documentation and due diligence
- Data-quality and lineage analysis
- Evaluation and test results
- Human-review simulations
- Threat modeling and security review
- Privacy and legal review
- Complaints, disputes, overrides, and user feedback
- Monitoring trends and threshold breaches
- Incidents and near misses
- Internal audit or independent assurance findings
- Material changes and new use cases
- Relevant NIST AI RMF considerations

Absence of reported harm is not proof that risk is absent, especially before deployment or when complaint and detection mechanisms are weak.

---

## 6. Risk Taxonomy

| Taxonomy ID | Risk domain | Examples |
| --- | --- | --- |
| `TAX-01` | Governance and accountability | Missing owner, unclear authority, weak approvals, unrecorded risk acceptance, or ineffective challenge |
| `TAX-02` | Intended use and misuse | Scope expansion, prohibited use, unauthorized secondary use, or misleading representation |
| `TAX-03` | Data quality and governance | Incomplete, inaccurate, stale, unrepresentative, improperly sourced, or poorly governed data |
| `TAX-04` | Performance and reliability | Incorrect recommendation, inconsistent performance, poor calibration, drift, or degraded availability |
| `TAX-05` | Fairness and harmful impact | Unjustified differences in workload, opportunity, delay, access, service, or burden |
| `TAX-06` | Transparency and explainability | Misleading rationale, missing limitations, unclear uncertainty, or inadequate disclosure |
| `TAX-07` | Human factors and oversight | Automation bias, alert fatigue, rubber-stamping, inadequate training, weak override, or retaliation |
| `TAX-08` | Privacy and data protection | Excessive collection, unauthorized use, location exposure, retention, reidentification, or data leakage |
| `TAX-09` | Security and integrity | Unauthorized access, manipulated input, compromised integration, output tampering, or weak administration |
| `TAX-10` | Safety and operational continuity | Unsafe routing, critical delay, service disruption, failed fallback, or cascading operational effect |
| `TAX-11` | Workforce and organizational impact | Displacement, deskilling, workload imbalance, surveillance, role confusion, or inappropriate performance use |
| `TAX-12` | Third-party and supply-chain risk | Vendor opacity, unannounced change, weak notification, subcontractor exposure, outage, or lock-in |
| `TAX-13` | Change and revalidation | Unapproved model, data, threshold, interface, or use-case change that invalidates prior assessment |
| `TAX-14` | Monitoring and detection | Missing metrics, unobserved drift, incomplete logs, weak alerting, or delayed escalation |
| `TAX-15` | Incident response and recovery | Delayed reporting, ineffective containment, lost evidence, premature restoration, or repeated failure |
| `TAX-16` | Legal, contractual, and compliance | Unmet obligation, inadequate notice, unauthorized processing, contract breach, or recordkeeping failure |
| `TAX-17` | Reputation and stakeholder trust | Loss of confidence caused by harm, secrecy, misleading claims, repeated errors, or weak response |

A risk may be assigned one primary domain and multiple secondary domains.

---

## 7. Risk-Statement Standard

Each material risk should use a cause-event-impact structure:

> Because **[condition, threat, vulnerability, dependency, or uncertainty]**, there is a possibility that **[risk event]**, resulting in **[impact to people, operations, safety, privacy, security, obligations, finances, or trust]**.

### 7.1 Example

> Because historical delivery data may underrepresent unusual medical-delivery conditions, RouteAssist may recommend an inappropriate priority or route during an uncommon event, resulting in delayed delivery, service disruption, contractual exposure, or harm to a recipient.

### 7.2 Risk-statement quality criteria

A risk statement should:

- Describe uncertainty rather than a known issue alone.
- Separate the cause, event, and consequence.
- Identify affected parties or assets where relevant.
- Avoid combining unrelated risks into one record.
- Avoid naming a control failure as the only impact.
- Avoid vague language such as “AI risk may occur.”
- Be understandable to both business and technical readers.
- Support an accountable treatment decision.

---

## 8. Required Risk-Register Fields

Each risk record should include:

| Field | Requirement |
| --- | --- |
| Risk ID | Stable identifier using `AIR-###` |
| Title | Short, distinct description |
| Primary domain | Primary taxonomy category |
| Secondary domains | Additional relevant categories |
| Risk statement | Cause-event-impact statement |
| Source or trigger | Origin of the concern |
| Affected parties | People or groups that may experience harm |
| Affected assets or processes | Related system, data, capability, component, or business process |
| Existing conditions | Relevant controls or limitations already present |
| Inherent likelihood | Score from 1 to 5 |
| Inherent impact | Score from 1 to 5 |
| Inherent score and rating | Likelihood multiplied by impact and mapped to rating band |
| Treatment decision | Avoid, reduce, transfer/share, accept, or investigate |
| Planned controls | Control IDs or required control themes |
| Control evidence | Evidence needed to rely on controls |
| Residual likelihood | Post-control score from 1 to 5 |
| Residual impact | Post-control score from 1 to 5 |
| Residual score and rating | Post-control score and rating band |
| Risk owner | Accountable role |
| Target date | Date for treatment or decision |
| Status | Open, in progress, accepted, monitored, closed, or escalated |
| Related records | Control, evaluation, metric, evidence, incident, gap, or POA&M IDs |
| Assumptions and uncertainty | Known limitations in the rating |
| Review trigger and cadence | When the risk must be reassessed |

---

## 9. Likelihood Scale

Likelihood is the probability or frequency of the risk event within the defined use context and assessment period.

| Score | Rating | General definition | Illustrative indicators |
| ---: | --- | --- | --- |
| 1 | Rare | Event is highly unusual under expected conditions and has little supporting evidence | Strong preventive controls; no comparable events; narrow exposure; exceptional conditions required |
| 2 | Unlikely | Event could occur but is not expected during normal operation | Limited exposure; few relevant precedents; multiple conditions must align |
| 3 | Possible | Event is plausible and may occur occasionally | Credible scenario; known data or process weakness; comparable events exist; controls may be inconsistent |
| 4 | Likely | Event is expected to occur repeatedly or under common operating conditions | Frequent exposure; known failures or overrides; weak control design; significant environmental variability |
| 5 | Almost certain | Event is expected frequently, is already occurring, or is unavoidable without treatment | Active pattern, repeated incidents, systemic weakness, or control absence |

### 9.1 Likelihood factors

Assessors should consider:

- Exposure frequency and transaction volume
- Number and variety of users
- Number and variety of affected parties
- Data quality and environmental variability
- Novelty and system complexity
- Human time pressure and workload
- Threat capability and opportunity
- Vendor and integration dependency
- Historical incidents, near misses, complaints, or overrides
- Strength and maturity of existing conditions
- Detectability before harm occurs
- Rate of model, data, or operating-context change

### 9.2 Likelihood uncertainty

When evidence is weak, the assessor should:

- Document the uncertainty.
- Avoid assigning a low score solely because no incidents have been recorded.
- Use a conservative score when missing information could reasonably conceal frequent exposure.
- Create a validation or monitoring action.

---

## 10. Impact Scale

Impact represents the most credible consequence if the risk event occurs. The assessor considers the highest relevant impact across affected parties and organizational dimensions rather than averaging severe harm with lower impacts.

| Score | Rating | General definition |
| ---: | --- | --- |
| 1 | Minimal | Negligible effect; easily corrected; no meaningful harm, sensitive-data exposure, or service disruption |
| 2 | Minor | Limited and recoverable effect; short disruption; low financial or trust impact; no serious harm |
| 3 | Moderate | Material operational, workforce, privacy, security, customer, contractual, or reputational effect requiring formal response |
| 4 | Major | Severe effect on people or operations; significant sensitive-data exposure, service failure, financial loss, contractual breach, or sustained trust damage |
| 5 | Severe / Critical | Potential death or serious injury, severe essential-service failure, widespread or difficult-to-reverse harm, major rights impact, or existential organizational consequence |

### 10.1 Impact dimensions

The impact score should consider:

| Dimension | Questions |
| --- | --- |
| Safety | Could the event cause physical harm, unsafe routing, or dangerous operating conditions? |
| Medical or essential service | Could it delay or disrupt a time-sensitive medical or similarly critical delivery? |
| Workforce | Could it affect workload, opportunity, income, discipline, performance perception, or psychological safety? |
| Fairness | Could effects be materially different across people, groups, locations, services, or delivery types? |
| Privacy | Could personal, location, customer, or medical-delivery information be misused, exposed, or retained improperly? |
| Security | Could systems, data, identities, configurations, or outputs be compromised? |
| Operations | Could delivery, warehouse, dispatch, billing, or continuity processes be materially disrupted? |
| Customer and recipient | Could service be delayed, denied, misrouted, or inaccurately explained? |
| Legal and contractual | Could PLG breach a duty, contract, notification requirement, or approved policy? |
| Financial | Could PLG experience loss, penalties, remediation cost, or lost business? |
| Reputation and trust | Could the event materially damage confidence among workers, clients, recipients, partners, or leadership? |
| Reversibility | Can the effect be corrected fully and promptly, or is it lasting or difficult to detect? |
| Scale | How many people, transactions, locations, or systems could be affected? |

### 10.2 Impact override rules

The impact score must be at least 5 when a credible event could cause death, serious injury, or comparable critical harm.

The impact score should generally be at least 4 when a credible event could:

- Materially delay a time-sensitive medical delivery.
- Cause severe safety exposure.
- Create significant or repeated workforce disadvantage.
- Expose sensitive data at material scale.
- Cause major service disruption or contractual failure.
- Produce harm that is difficult to reverse before detection.

Human review may reduce likelihood, but it does not erase the inherent impact of a severe outcome.

---

## 11. Risk Calculation

### 11.1 Inherent risk

```text
Inherent risk score = Inherent likelihood × Inherent impact
```

### 11.2 Residual risk

```text
Residual risk score = Residual likelihood × Residual impact
```

### 11.3 Risk bands

| Score | Rating | Required response |
| ---: | --- | --- |
| 1–4 | Low | Manage through routine controls and periodic review |
| 5–9 | Moderate | Assign owner, document treatment or acceptance, and monitor |
| 10–16 | High | Formal treatment plan, governance review, defined evidence, and approval required |
| 17–25 | Critical | Immediate escalation; avoid, restrict, suspend, or remediate before use unless extraordinary authority explicitly approves |

### 11.4 Risk matrix

| Impact ↓ / Likelihood → | 1 Rare | 2 Unlikely | 3 Possible | 4 Likely | 5 Almost certain |
| --- | ---: | ---: | ---: | ---: | ---: |
| **5 Severe / Critical** | 5 Moderate | 10 High | 15 High | 20 Critical | 25 Critical |
| **4 Major** | 4 Low | 8 Moderate | 12 High | 16 High | 20 Critical |
| **3 Moderate** | 3 Low | 6 Moderate | 9 Moderate | 12 High | 15 High |
| **2 Minor** | 2 Low | 4 Low | 6 Moderate | 8 Moderate | 10 High |
| **1 Minimal** | 1 Low | 2 Low | 3 Low | 4 Low | 5 Moderate |

The numeric score is a prioritization aid. It does not override mandatory requirements, prohibited uses, severe affected-party concerns, or professional judgment.

---

## 12. Severity and Score Overrides

PLG may raise a rating above the calculated band when:

- A single credible outcome could create severe harm.
- Multiple moderate effects combine into a major consequence.
- Harm may affect people with limited ability to identify, challenge, or remedy the decision.
- Missing information materially weakens confidence.
- The system operates in a new or poorly understood context.
- Vendor opacity prevents validation.
- Detection is unlikely before harm occurs.
- A risk affects a prohibited use or mandatory requirement.
- Similar risks are correlated and may occur together.
- The score understates scale, reversibility, or affected-party impact.

A downward override requires stronger justification and documented evidence than an upward override.

---

## 13. Control Assessment

### 13.1 Control-design rating

| Rating | Definition |
| --- | --- |
| Effective design | Control activity is specific, assigned, feasible, risk-responsive, and capable of achieving the objective if performed |
| Partially effective design | Control addresses part of the risk but has material gaps, ambiguity, weak ownership, or insufficient coverage |
| Ineffective design | Control cannot reasonably achieve the objective or is missing |
| Not assessed | Insufficient evidence to determine design adequacy |

### 13.2 Operating-effectiveness rating

| Rating | Definition |
| --- | --- |
| Effective | Sufficient evidence indicates the control operated as designed for the assessed period and population |
| Partially effective | Control operated inconsistently or exceptions reduce assurance |
| Ineffective | Control did not operate as designed or material failures occurred |
| Not implemented | Planned control is not operational |
| Not tested | Control may operate, but sufficient evidence has not been evaluated |

### 13.3 Evidence rule

Residual risk may be reduced only when:

- The control is implemented.
- The control directly addresses the relevant cause, event, or consequence.
- Evidence is relevant, reliable, complete, timely, and traceable.
- Exceptions and limitations are considered.
- The assessor documents how the control changes likelihood, impact, or both.

Policies, plans, or vendor claims alone do not prove operating effectiveness.

---

## 14. Residual-Risk Rating

Residual likelihood and impact are rescored after evaluating control evidence.

### 14.1 Residual-rating rules

- Do not subtract arbitrary points merely because a control exists.
- Explain which control changes which rating factor.
- A preventive control may reduce likelihood.
- A containment, fallback, or recovery control may reduce impact.
- A detective control may reduce impact when timely detection enables effective intervention.
- A weak or untested control does not justify a material reduction.
- Severe inherent impact may remain severe even when likelihood is reduced.
- Interdependent controls should be assessed for common failure.
- Human oversight should be evaluated for actual authority, information, competence, time, and behavior.

### 14.2 Target residual risk

The target residual risk is the intended level after planned treatments. It is not the current residual risk unless controls are implemented and validated.

---

## 15. Risk-Treatment Options

| Treatment | Description | Example |
| --- | --- | --- |
| Avoid | Do not begin or continue the activity creating the risk | Exclude medical-delivery prioritization from the pilot |
| Reduce | Implement controls to lower likelihood or impact | Require validated data, supervisor review, testing, and monitoring |
| Transfer or share | Allocate defined obligations through insurance, contract, or service arrangement while retaining PLG accountability | Require vendor notification, indemnity, or service commitments |
| Accept | Formally acknowledge and approve residual risk within authorized tolerance | Accept a documented low residual risk with monitoring |
| Investigate | Obtain information before selecting final treatment | Conduct additional slice analysis or vendor due diligence |

Transfer does not eliminate PLG's responsibility for how it uses RouteAssist.

---

## 16. Risk-Acceptance Authority

| Residual rating | Minimum authority | Conditions |
| --- | --- | --- |
| Low | Assigned risk owner within delegated authority | Document rationale and monitoring where relevant |
| Moderate | Assigned senior risk owner | GRC review, treatment rationale, and defined review date |
| High | Chief Operating Officer following AI Governance Committee review | Written justification, control evidence, conditions, monitoring, and expiration or review date |
| Critical | Not accepted through normal delegation | Avoid, restrict, suspend, or remediate; extraordinary governing-body action and specialized review would be required |

The person accepting a risk must have authority over the affected objective and must understand the affected-party consequences and uncertainty.

No person may accept risk solely because remediation is inconvenient, expensive, or delayed.

---

## 17. Mandatory Escalation Conditions

Escalation is required when:

- Inherent or residual risk is Critical.
- Residual risk is High and exceeds delegated tolerance.
- A credible scenario involves death, serious injury, or severe medical-delivery harm.
- A proposed use conflicts with a prohibited-use boundary.
- A risk owner is missing or lacks authority and resources.
- Required evidence is unavailable or unreliable.
- A severe incident, near miss, or repeated complaint occurs.
- Monitoring reveals material drift, disparity, override patterns, or control failure.
- A vendor makes an unapproved material change.
- Human reviewers cannot meaningfully challenge the system.
- A risk affects multiple business units or may create cascading failure.
- Legal, contractual, privacy, or notification uncertainty may materially change the decision.
- Stakeholders disagree materially about risk severity or treatment.

---

## 18. Uncertainty Assessment

Each risk should receive an uncertainty rating.

| Rating | Definition | Required action |
| --- | --- | --- |
| Low uncertainty | Strong, relevant, and representative evidence supports the rating | Proceed using normal review cadence |
| Moderate uncertainty | Some important assumptions or evidence limitations remain | Document assumptions and create targeted validation or monitoring |
| High uncertainty | Major information gaps, novel context, limited transparency, or weak evidence materially affect confidence | Use conservative rating, escalate, restrict use, and obtain evidence before approval |

### 18.1 Sources of uncertainty

- No production history
- Small or unrepresentative evaluation dataset
- Unclear vendor documentation
- Unknown training or development data
- Unmeasured affected-party impact
- Novel geography or delivery type
- Changing environmental conditions
- Incomplete complaint or incident data
- Weak data lineage
- Unvalidated human-review behavior
- Missing control evidence
- Correlated or cascading risk

Uncertainty should influence the decision, not be hidden in narrative notes.

---

## 19. Affected-Party Analysis

For each material risk, assessors should consider:

- Who may benefit?
- Who may be harmed?
- Who bears the risk while someone else receives the benefit?
- Does the affected party know RouteAssist influences the process?
- Can the affected party challenge, appeal, complain, or obtain correction?
- Is the harm distributed differently across locations, services, workers, customers, or delivery types?
- Is the impact reversible?
- Does the affected party have limited bargaining power or visibility?
- Could proxies produce unintended differential outcomes?
- Are complaints or overrides likely to reveal the harm?

Low organizational cost does not mean low affected-party impact.

---

## 20. Scenario Analysis

Risk assessments should include normal, edge, failure, misuse, and change scenarios.

| Scenario type | Purpose | Example |
| --- | --- | --- |
| Normal operation | Assess expected workflow | Routine delivery with complete and current data |
| Edge case | Assess unusual but plausible conditions | Remote route, atypical delivery window, or rare service type |
| Data failure | Assess incomplete or conflicting data | Stale driver availability or conflicting priority indicators |
| Human-factor failure | Assess ineffective oversight | Dispatcher accepts output under severe time pressure |
| Technical failure | Assess outage or system degradation | Vendor API timeout or logging failure |
| Security misuse | Assess malicious or unauthorized behavior | Manipulated route input or unauthorized threshold change |
| Prohibited use | Assess boundary enforcement | Manager uses assignments for disciplinary ranking |
| High-impact use | Assess severe consequence | Incorrect medical-delivery priority recommendation |
| Material change | Assess invalidated assumptions | Vendor updates model without adequate notice |
| Cascading failure | Assess connected effects | Incorrect schedule adjustment delays multiple dependent deliveries |

---

## 21. Assessment Workflow

### Step 1 — Establish context

- Confirm use case, system boundary, capability, lifecycle stage, and assessment period.
- Identify users, affected parties, owners, data, dependencies, and approved purposes.
- Confirm the applicable impact tier.

### Step 2 — Identify risks

- Review documents, workflows, data flows, stakeholder input, vendor information, and scenarios.
- Create distinct cause-event-impact statements.
- Assign taxonomy domains and related identifiers.

### Step 3 — Rate inherent risk

- Score likelihood and impact without relying on proposed or untested controls.
- Apply severity and uncertainty overrides.
- Document rationale and affected parties.

### Step 4 — Assign ownership

- Assign a risk owner with authority and resources.
- Identify supporting control owners and specialists.
- Escalate unowned risks.

### Step 5 — Select treatment

- Choose avoid, reduce, transfer/share, accept, or investigate.
- Define target residual risk and required completion date.
- Map planned controls, evaluations, and evidence.

### Step 6 — Assess controls

- Evaluate design and operating effectiveness.
- Review exceptions, control dependencies, and evidence quality.
- Do not credit unimplemented or untested controls as effective.

### Step 7 — Rate residual risk

- Rescore likelihood and impact.
- Explain how evidence supports each change.
- Assign uncertainty and compare against tolerance.

### Step 8 — Approve or escalate

- Obtain risk acceptance from the required authority.
- Record conditions, expiration, monitoring, and dissent.
- Restrict or suspend use when required.

### Step 9 — Monitor and reassess

- Link risk to metrics, incidents, complaints, overrides, changes, tests, and POA&M actions.
- Reassess on schedule or when a trigger occurs.

---

## 22. Risk Status Definitions

| Status | Definition |
| --- | --- |
| Draft | Risk is being documented and has not completed review |
| Open | Risk is validated and requires a decision or treatment |
| In progress | Approved treatment activities are underway |
| Pending validation | Controls are implemented but evidence or testing is incomplete |
| Accepted | Authorized role has accepted residual risk with documented conditions |
| Monitored | Risk is within approved tolerance and tracked through defined indicators |
| Escalated | Risk exceeds authority, tolerance, or response capability |
| Closed | Risk is removed, avoided, no longer applicable, or reduced with verified evidence and approved closure |

Closing a remediation action does not automatically close the risk.

---

## 23. Review Cadence

| Risk rating or condition | Minimum review cadence |
| --- | --- |
| Critical | Continuous or event-driven oversight with formal review at least monthly until reduced or avoided |
| High | At least monthly during pilot or remediation and quarterly after stabilization |
| Moderate | At least quarterly or semiannually depending on exposure |
| Low | At least annually |
| High uncertainty | At each material evidence update and governance gate |
| Material change | Before approval or deployment of the change |
| Severe incident or threshold breach | Immediately or according to incident-response timeline |

The AI Governance Committee may require more frequent review.

---

## 24. Reassessment Triggers

Risks must be reassessed when:

- The intended, restricted, or prohibited use changes.
- A new capability, user, affected party, geography, customer, or delivery type is introduced.
- Medical-delivery or safety-related scope changes.
- A new sensitive data source or downstream action is introduced.
- The model, vendor, data, threshold, interface, integration, or hosting environment materially changes.
- Evaluation or monitoring reveals degraded performance, drift, or differential impact.
- Override, complaint, dispute, error, or incident patterns exceed thresholds.
- A severe incident or near miss occurs.
- A control fails or evidence becomes unreliable.
- A risk assumption is invalidated.
- A relevant legal, contractual, policy, or organizational requirement changes.
- RouteAssist is restored after suspension or prolonged inactivity.

---

## 25. Risk Aggregation and Interdependency

Individual risk scores should not be reviewed in isolation.

PLG should evaluate:

- Risks that share the same control or data source
- Risks that may occur together
- Cascading effects across dispatch, warehouse, delivery, billing, and customer service
- Concentration in one vendor or integration
- Repeated low or moderate events that create cumulative harm
- Multiple risks affecting the same person or group
- Common-cause failure in identity, logging, data quality, or human review
- Feedback loops that reinforce earlier outcomes
- Control dependencies that can fail simultaneously

Aggregated exposure may require a higher priority than the individual scores suggest.

---

## 26. Risk Communication

Risk communication should state:

- What may happen and why
- Who or what may be affected
- Inherent risk
- Relevant uncertainty
- Existing and planned controls
- Evidence quality
- Residual and target risk
- Treatment decision
- Risk owner and target date
- Required approval
- Monitoring and escalation conditions
- Limitations and dissenting views

Executive communication should translate technical detail into business and affected-party consequences without hiding material uncertainty.

---

## 27. Quality Assurance

Before approval, the GRC Analyst should confirm that:

- [ ] The risk statement includes cause, event, and impact.
- [ ] Users and affected parties are identified.
- [ ] Related processes, data, components, flows, and capabilities are linked.
- [ ] Inherent scoring does not rely on planned controls.
- [ ] Likelihood and impact rationales are documented.
- [ ] Severity override rules were considered.
- [ ] Uncertainty is rated and explained.
- [ ] The risk owner has authority and resources.
- [ ] Treatment is specific and time-bound.
- [ ] Controls directly address the risk.
- [ ] Residual scoring is supported by evidence.
- [ ] Acceptance authority matches the residual rating.
- [ ] Metrics, tests, evidence, incidents, gaps, and POA&M actions are linked.
- [ ] Review cadence and triggers are defined.
- [ ] Material disagreement is recorded.

---

## 28. Traceability Requirements

Each High or Critical risk should trace through:

```text
Use case, capability, process, data, component, or flow
    → affected party or asset
    → AIR risk identifier
    → AIC control identifier
    → EVAL evaluation or control test
    → EVD evidence identifier
    → MET monitoring indicator
    → GAP or POAM remediation identifier when needed
    → AI-INC incident identifier when applicable
```

A missing link should be treated as a governance gap.

---

## 29. NIST AI RMF Alignment

| NIST AI RMF function | Methodology application |
| --- | --- |
| GOVERN | Establishes ownership, risk tolerance, escalation, acceptance, documentation, and review requirements |
| MAP | Identifies context, affected parties, impacts, dependencies, misuse, and risk statements |
| MEASURE | Defines likelihood, impact, uncertainty, control evidence, evaluation, and residual-risk analysis |
| MANAGE | Defines treatment, prioritization, acceptance, monitoring, escalation, and reassessment |

Detailed subcategory mappings will be maintained in [`07-framework-crosswalk.md`](07-framework-crosswalk.md).

---

## 30. Methodology Limitations

- Numeric scores simplify complex and sometimes uncertain conditions.
- Likelihood may be difficult to estimate before deployment.
- Historical data may not represent future use or rare events.
- Some harms are qualitative, cumulative, delayed, or difficult to observe.
- Affected parties may experience impacts not visible in organizational metrics.
- Vendor opacity may limit confidence.
- Risk ratings reflect the defined fictional context and professional judgment.
- A score does not establish legal compliance, safety, fairness, or fitness for use.

Professional judgment and documented challenge remain necessary.

---

## 31. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Risk Assessment Methodology |
| Repository path | `docs/05-ai-risk-assessment-methodology.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Annually and upon material methodology, system, use-case, or risk-tolerance change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-19 | Tommy Marshall | Established the AI risk taxonomy, scoring scales, matrix, treatment rules, acceptance authority, uncertainty method, and assessment workflow. |

---

## 32. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Register](06-ai-risk-register.md)
- [Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 33. Portfolio Notice

This document is part of an educational portfolio project based on a fictional organization and fictional AI system. The methodology, scales, thresholds, and decision authorities are illustrative and tailored to the PLG RouteAssist case study.

It does not provide legal advice, regulatory advice, certification, independent assurance, or a guarantee that the method is sufficient for a real organization, AI system, or jurisdiction.
