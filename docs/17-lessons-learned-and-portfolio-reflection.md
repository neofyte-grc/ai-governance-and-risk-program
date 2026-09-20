# Lessons Learned and Portfolio Reflection

## PLG RouteAssist AI Governance and Risk Assessment

**Author:** Tommy Marshall  
**Role demonstrated:** GRC Analyst  
**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Status:** Portfolio reflection  
**Version:** 1.0  
**Date:** 2026-09-20

---

## 1. Project Reflection

This project demonstrates how I would structure governance and risk management for an AI-assisted logistics system before deployment.

The central lesson is that AI governance is not only a model-performance exercise. RouteAssist risk emerges from the complete operating environment:

- Business purpose.
- Source data.
- System integrations.
- Vendor dependencies.
- Human behavior.
- Review and approval processes.
- Downstream operational actions.
- Monitoring and complaints.
- Incident response.
- Organizational culture.

A technically accurate model may still create unacceptable risk if the data is stale, the reviewer is overloaded, the vendor changes the system without notice, the interface encourages automation bias, or the organization cannot investigate an incident.

---

## 2. Project Objective

The project was designed to determine how Peachtree Logistics Group could responsibly govern an AI-assisted dispatch system that recommends:

- Delivery priorities.
- Driver and courier assignments.
- Routes and delivery sequences.
- Schedule adjustments.
- Operational exceptions.

The assessment focused on identifying risks before deployment and translating those risks into practical governance, controls, testing, monitoring, and remediation.

---

## 3. What I Built

I created an interconnected AI governance package containing:

- Project methodology and scope.
- Organizational context and AI use-case definition.
- Stakeholder and accountability mapping.
- AI system inventory.
- Impact screening and tier assignment.
- System-context and data-flow analysis.
- Trust-boundary analysis.
- AI risk taxonomy and scoring methodology.
- A 20-item AI risk register.
- NIST AI RMF, ISO, and OECD framework crosswalks.
- AI Governance Charter.
- A 30-control AI Control Matrix.
- Human Oversight and Escalation Plan.
- AI Evaluation and Testing Plan.
- Monitoring, Metrics, and Reporting Plan.
- AI Incident Response Plan.
- Third-Party and Vendor AI Risk Review.
- Gap Assessment and POA&M.
- Responsible AI Policy.
- AI Acceptable Use Standard.
- AI System Change and Revalidation Standard.
- Executive Summary and Recommendations.

Stable identifiers connect systems, risks, controls, tests, metrics, incidents, and corrective actions.

---

## 4. Major Lessons Learned

### 4.1 Context determines risk

The same recommendation may carry very different risk depending on its operating context.

A routing error involving a routine package may cause inconvenience or additional cost. The same error involving a time-sensitive medical delivery could cause severe harm.

This reinforced the importance of documenting:

- Intended purpose.
- Delivery type.
- Affected parties.
- Time sensitivity.
- Operating constraints.
- Human involvement.
- Downstream consequences.

AI risk cannot be assessed accurately by examining the model in isolation.

### 4.2 Human-in-the-loop is not automatically a control

A human reviewer adds value only when the person has:

- Adequate information.
- Sufficient time.
- Appropriate training.
- Clear authority.
- A practical way to challenge the output.
- Protection from retaliation.
- Access to escalation and fallback.

A review requirement becomes ceremonial if the interface hides uncertainty, users are overloaded, overrides are discouraged, or approval becomes the default.

The project therefore evaluates human-review quality rather than simply recording that a human clicked an approval button.

### 4.3 Planned controls are not current controls

One of the most important GRC lessons from this project is that a planned control cannot be credited as though it already reduces risk.

A policy, control matrix, or implementation plan may describe the desired future state, but it does not demonstrate:

- Implementation.
- Design effectiveness.
- Consistent operation.
- Evidence quality.
- Risk reduction.

For that reason, the project keeps RouteAssist’s current risk equal to its inherent risk until controls are implemented and tested.

Target residual ratings are planning objectives, not conclusions.

### 4.4 Aggregate metrics can conceal harm

Overall accuracy or average delivery efficiency may look acceptable while particular workers, routes, service types, or operating conditions experience poor outcomes.

Meaningful monitoring must consider relevant slices such as:

- Employed drivers versus independent couriers.
- New versus established workers.
- Urban, suburban, and rural routes.
- Day and night operations.
- Routine and urgent deliveries.
- Recommendation type.
- Workload level.
- System and model version.

Quantitative analysis must also be supported by complaints, interviews, overrides, and other qualitative information.

### 4.5 Traceability connects governance to action

Governance is difficult to enforce when decisions cannot be reconstructed.

PLG should be able to connect:

1. The source data.
2. Data timestamps and validation results.
3. The system and model version.
4. The recommendation and rationale.
5. The human reviewer.
6. The approval, modification, rejection, or override.
7. The downstream operational action.
8. The resulting outcome.
9. Any complaint or incident.
10. The corrective action and governance decision.

Traceability supports accountability, monitoring, investigations, audits, disputes, and lessons learned.

### 4.6 Vendor risk is product risk

When a vendor controls the model or service, PLG may have limited visibility into:

- Training and evaluation data.
- Model changes.
- Known limitations.
- Performance across operating conditions.
- Data retention and secondary use.
- Subprocessors.
- Security incidents.
- Service resilience.
- Exit feasibility.

However, PLG still owns the decision to rely on the vendor’s output.

Vendor governance is therefore part of system governance rather than a separate purchasing exercise.

### 4.7 Risk is interconnected

The assessment showed that AI risks should not be evaluated only as isolated register entries.

For example:

- Poor data quality may generate a bad recommendation.
- Automation bias may cause a dispatcher to approve it.
- Incomplete logging may prevent investigation.
- Weak monitoring may delay detection.
- Vendor opacity may hide the underlying change.
- Ineffective incident response may allow the harm to continue.

The combined event may be more severe than any single risk description suggests.

### 4.8 Efficiency cannot replace accountability

RouteAssist is intended to make dispatch operations faster and more consistent. However, efficiency should not justify:

- Unsafe decisions.
- Inadequate review.
- Excessive data collection.
- Unfair worker outcomes.
- Unapproved automation.
- Missing evidence.
- Weak incident response.

The project treats efficiency as a potential benefit that must be balanced against safety, rights, privacy, security, reliability, and trust.

---

## 5. Important Governance Decisions

### 5.1 Medical delivery remains excluded

RouteAssist was classified as Tier 4 because foreseeable medical-delivery use could create severe consequences.

The initial pilot therefore excludes medical-delivery prioritization, assignment, and routing.

This decision demonstrates risk avoidance rather than attempting to control every high-impact scenario immediately.

### 5.2 RouteAssist remains advisory-only

RouteAssist does not independently execute dispatch decisions.

A trained and authorized human must:

- Review the recommendation.
- Consider current operational conditions.
- Approve, modify, reject, or escalate it.
- Remain accountable for the final action.

### 5.3 Unproven controls receive no risk-reduction credit

The portfolio clearly distinguishes among:

- Planned control.
- Implemented control.
- Design-effective control.
- Operating-effective control.

This prevents the documentation from overstating the organization’s current maturity.

### 5.4 Pilot approval is not production approval

A limited pilot should have explicit boundaries involving:

- Users.
- Services.
- Geography.
- Volume.
- Duration.
- Data.
- Monitoring.
- Stop conditions.
- Expiration.

Successful pilot operation would provide evidence for a later production decision but would not automatically authorize unrestricted use.

---

## 6. Key Tradeoffs

| Tradeoff | Governance response |
| --- | --- |
| Efficiency versus meaningful review | Preserve reviewer time and authority; restrict volume when review becomes ceremonial |
| More data versus privacy | Apply purpose limitation, minimization, allowlists, retention, and secondary-use review |
| Faster vendor adoption versus evidence | Require critical due diligence and contractual protections before connection |
| Global performance versus subgroup impact | Use aggregate and slice analysis together |
| Continuous improvement versus uncontrolled change | Require versioning, impact assessment, regression testing, approval, and rollback |
| Operational continuity versus unsafe reliance | Maintain and exercise manual fallback |
| Detailed monitoring versus worker surveillance | Limit monitoring to defined risk and operational purposes |
| Standardization versus professional judgment | Provide structured review without removing authorized human challenge |
| Transparency versus cognitive overload | Present material information in a usable and prioritized format |
| Innovation versus risk tolerance | Use staged approval and restricted pilots rather than unrestricted deployment |

---

## 7. Project Limitations

This is a fictional predeployment assessment.

It does not include:

- A selected AI vendor.
- Vendor documentation or assurance evidence.
- Source-system access.
- Production data.
- Implemented technical controls.
- Executed evaluation results.
- Real pilot outcomes.
- Interviews with actual affected parties.
- Jurisdiction-specific legal advice.
- Independent audit.
- Certification.
- Production authorization.

These limitations are explicitly reflected in:

- Risk ratings.
- Control statuses.
- Evidence notices.
- Vendor decision.
- POA&M items.
- Executive recommendations.

The project intentionally avoids presenting hypothetical evidence as though it were real.

---

## 8. What I Would Do Next

If this were a real engagement, I would:

1. Facilitate stakeholder and affected-party workshops.
2. Confirm the business owner, executive sponsor, and governance committee.
3. Complete the legal, privacy, employment, and contractual obligations register.
4. Select and assess the vendor.
5. Obtain system, model, data, security, and assurance documentation.
6. Validate data lineage using representative source records.
7. Profile data quality and establish approved validation rules.
8. Implement the mandatory control set.
9. Approve evaluation metrics and thresholds.
10. Run technical, fairness, human-factor, security, privacy, fallback, and incident tests.
11. Remediate and retest blocking defects.
12. Conduct a limited non-medical pilot with enhanced monitoring.
13. Collect reviewer, worker, customer, and affected-party feedback.
14. Update current and residual risk using evidence.
15. Obtain independent review before production authorization.
16. Maintain ongoing monitoring, revalidation, incident response, and retirement planning.

---

## 9. Improvements for a Future Version

A future version of this project could include:

- Completed fictional vendor questionnaire.
- Sample model card.
- Sample dataset card.
- Completed test cases and results.
- Sample monitoring dashboard.
- Completed incident tabletop report.
- Human-review simulation results.
- Example risk-acceptance record.
- Example change-impact assessment.
- Sample complaint and correction record.
- Completed access-review evidence.
- Example control-testing workpaper.
- A visual executive briefing deck.
- A mock governance meeting packet.

These additions would demonstrate not only governance design but also evidence evaluation and control assurance.

---

## 10. Skills Demonstrated

### Governance and risk management

- AI governance.
- NIST AI RMF application.
- Risk taxonomy development.
- Risk identification and scenario analysis.
- Likelihood and impact scoring.
- Risk treatment and acceptance.
- Impact-tier classification.
- Governance charter development.
- Decision-rights and RACI analysis.

### Control and assurance

- Control-objective development.
- Preventive, detective, corrective, and directive controls.
- Risk-to-control traceability.
- Evidence requirements.
- Design and operating-effectiveness testing.
- Control-deficiency classification.
- POA&M development.
- Assurance and closure requirements.

### AI and data governance

- AI system inventory.
- Data-flow and trust-boundary analysis.
- Data lineage and ownership.
- Data quality and validation.
- Data minimization and purpose limitation.
- Fairness and harmful-impact analysis.
- Human oversight and automation-bias analysis.
- Model and data-drift monitoring.
- AI change and revalidation governance.

### Security, privacy, and resilience

- Role-based access control.
- Privileged-access governance.
- Integration security.
- Logging and traceability.
- Privacy-risk analysis.
- Vendor and supply-chain risk.
- Incident response.
- Business continuity and manual fallback.
- Return-to-service governance.

### Communication and project delivery

- Executive risk communication.
- Policy and standard development.
- Technical-to-business translation.
- GitHub repository organization.
- Markdown documentation.
- Cross-functional stakeholder communication.
- Roadmap and remediation planning.

---

## 11. Connection to My Operations Background

My logistics and operations background influenced the project in several ways.

I understand that dispatch decisions occur within:

- Time-sensitive workflows.
- Changing road and weather conditions.
- Staffing and capacity limitations.
- Customer commitments.
- Driver and courier constraints.
- High-volume environments.
- Escalation and exception processes.
- Real-world safety considerations.

That experience helped me avoid treating RouteAssist as only a technical system.

The governance design considers whether controls can work during actual operations, including peak volume, outages, incomplete data, urgent deliveries, and competing priorities.

This project demonstrates how operational knowledge can strengthen GRC work by connecting policy and controls to the realities of the business process.

---

## 12. Interview Narrative

> I designed an end-to-end AI governance and risk assessment for a fictional logistics company deploying an AI-assisted dispatch system. I classified the use case as high impact because routing and priority decisions could affect medical deliveries. I built a 20-risk register and 30-control matrix, then connected governance, human oversight, testing, monitoring, vendor risk, incident response, and remediation through stable identifiers. I intentionally did not claim that planned controls reduced current risk. My recommendation was to exclude medical use, implement and test mandatory controls, and permit only a restricted non-medical pilot after governance approval.

---

## 13. STAR Interview Example

### Situation

Peachtree Logistics Group wanted to evaluate an AI-assisted dispatch system that could recommend delivery priorities, routes, and driver assignments.

### Task

My role was to design an AI governance and risk-assessment approach that protected operations and affected parties without preventing responsible innovation.

### Action

I:

- Defined the intended and prohibited uses.
- Mapped stakeholders and decision rights.
- Classified the system as Tier 4.
- Documented the architecture and data flows.
- Created a 20-risk register.
- Designed 30 controls.
- Established human-oversight and testing requirements.
- Created monitoring, incident, vendor, and change-management plans.
- Prioritized 16 remediation actions in a POA&M.
- Recommended a restricted non-medical pilot only after mandatory controls passed testing.

### Result

The project produced a complete governance blueprint that leadership could use to decide whether to approve, restrict, remediate, suspend, or reject the proposed AI use.

Because the project is fictional and predeployment, the result is a governance design rather than a claim of actual risk reduction.

---

## 14. How This Project Supports My GRC Career

This project demonstrates my ability to:

- Translate operational processes into risk scenarios.
- Apply governance frameworks to a realistic business use case.
- Develop policies, standards, controls, and evidence requirements.
- Communicate risk to technical and executive audiences.
- Distinguish documentation from demonstrated effectiveness.
- Prioritize remediation based on impact and lifecycle needs.
- Build a traceable portfolio artifact using GitHub.

It also connects my logistics experience with my transition into cybersecurity and GRC by showing how operational knowledge can support stronger governance decisions.

---

## 15. NIST AI RMF Reflection

| Function | Project lesson |
| --- | --- |
| GOVERN | Responsible AI requires authority, accountability, policy, ownership, and a culture of effective challenge |
| MAP | Risk becomes understandable only when purpose, context, affected parties, data, and dependencies are documented |
| MEASURE | Evaluation must include technical behavior, human behavior, subgroup outcomes, uncertainty, and control evidence |
| MANAGE | Risk decisions require prioritization, treatment, restriction, monitoring, response, and continuing reassessment |

---

## 16. Final Reflection

The strongest part of this project is not any single document. It is the connection among the documents.

The project links:

- Business context to system scope.
- System scope to affected parties.
- Affected parties to risks.
- Risks to controls.
- Controls to evidence and tests.
- Tests to metrics and thresholds.
- Thresholds to escalation and incidents.
- Incidents to corrective actions.
- Corrective actions to governance decisions.

That traceability reflects how effective GRC programs operate.

The final lesson is straightforward: responsible AI governance is not about proving that an AI system is perfect. It is about ensuring that the organization understands the system, controls its use, detects failure, protects affected people, and remains accountable for every decision to deploy, continue, restrict, or stop it.

---

## 17. Document Control

| Field | Value |
| --- | --- |
| Document title | Lessons Learned and Portfolio Reflection |
| Repository path | `docs/17-lessons-learned-and-portfolio-reflection.md` |
| Version | 1.0 |
| Status | Portfolio reflection |
| Author | Tommy Marshall |
| Review frequency | At project completion and following major portfolio updates |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Documented project lessons, limitations, tradeoffs, skills demonstrated, career relevance, and future improvements. |

---

## 18. Related Documents

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
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Third-Party and Vendor AI Risk Review](14-third-party-and-vendor-ai-risk-review.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)
- [Executive Summary and Recommendations](16-executive-summary-and-recommendations.md)

---

## 19. Portfolio Notice

This reflection describes an educational portfolio exercise based on a fictional organization and AI system.

It does not claim real-world deployment, control implementation, testing, audit, certification, legal review, or production authorization.
