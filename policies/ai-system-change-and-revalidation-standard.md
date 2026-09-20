# AI System Change and Revalidation Standard

## Peachtree Logistics Group

**Standard owner:** AI Governance Committee  
**Process owner:** CIO / IT Director  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Effective date:** Upon approval  
**Review frequency:** At least annually and upon material change

---

## 1. Purpose

This standard requires AI changes to be identified, assessed, tested, approved, deployed, monitored, and made reversible in proportion to their risk.

It prevents an approved AI system from becoming materially different from the system PLG originally assessed and authorized.

---

## 2. Scope

This standard applies to changes involving:

- Purpose.
- Capability.
- Autonomy.
- Downstream action.
- Model.
- Service version.
- Prompt.
- Rule.
- Algorithm.
- Threshold.
- Configuration.
- Training data.
- Tuning data.
- Evaluation data.
- Feedback data.
- Input field.
- Data source.
- Transformation.
- Retention.
- Output.
- Vendor.
- Subprocessor.
- Hosting.
- Integration.
- Critical dependency.
- User interface.
- Explanation.
- Human-review workflow.
- Escalation.
- Manual fallback.
- User population.
- Affected population.
- Service.
- Geography.
- Security control.
- Privacy control.
- Logging.
- Monitoring.
- Incident response.
- Continuity process.

---

## 3. Objectives

The standard is designed to ensure that:

- Changes are identified before deployment.
- Risk determines the level of review.
- Material changes receive cross-functional assessment.
- Acceptance criteria are established before testing.
- Deployed versions match approved versions.
- Regression testing covers affected risks and controls.
- Rollback remains available.
- Users receive necessary communication and training.
- Monitoring detects unintended effects.
- Emergency changes receive retrospective review.
- Change evidence remains traceable.

---

## 4. Change Classification

| Class | Description | Minimum requirement |
| --- | --- | --- |
| Standard | Low-risk, repeatable, preauthorized maintenance with no material effect on behavior or scope | Ticket, testing, technical approval, and version record |
| Significant | Could affect performance, data, users, controls, explanations, or operations | Impact assessment, targeted risk update, regression testing, and owner approval |
| Material | Changes purpose, autonomy, high-impact behavior, vendor or model, sensitive data, affected population, or critical control | Full cross-functional assessment and AI Governance Committee approval |
| Emergency | Urgent change needed to contain harm or restore critical operations | Emergency authority, minimum safe testing, documentation, and prompt retrospective review |

When classification is uncertain, the change must be treated at the higher level until an assessment supports reducing the classification.

---

## 5. Material Change Triggers

A change is material when it may:

- Introduce a new AI use case.
- Expand an approved use case.
- Affect medical delivery.
- Affect safety.
- Affect rights.
- Affect employment or work opportunity.
- Affect privacy.
- Increase autonomy.
- Reduce human review.
- Add sensitive data.
- Introduce a new data purpose.
- Replace or materially alter the model.
- Replace or materially alter the vendor.
- Change a critical integration.
- Change known limitations.
- Affect fairness.
- Affect security.
- Affect explanations.
- Affect reliability or resilience.
- Change risk tolerance.
- Change approval conditions.
- Change monitoring or stop conditions.
- Change manual fallback.
- Expand to a new geography.
- Expand to a new service.
- Expand to a new worker, customer, or recipient population.

---

## 6. Standard Change Examples

Potential Standard changes include:

- Documentation correction that does not change requirements.
- Approved certificate rotation.
- Minor interface correction with no workflow or meaning change.
- Routine patch that does not affect AI behavior.
- Preapproved monitoring-dashboard maintenance.
- Non-functional metadata correction.

A change may not be classified as Standard merely because the vendor labels it minor.

---

## 7. Significant Change Examples

Potential Significant changes include:

- Adjustment to a non-safety threshold.
- New reporting view.
- Updated workflow step.
- New operational data field.
- Changed explanation format.
- Modified alert routing.
- Updated source-system interface.
- Expanded user role.
- Performance improvement that does not change approved purpose.

Significant changes require targeted risk and regression analysis.

---

## 8. Material Change Examples

Potential Material changes include:

- Enabling medical-delivery recommendations.
- Allowing automatic downstream execution.
- Replacing the AI vendor.
- Deploying a new model family or major version.
- Adding employee-performance use.
- Adding sensitive personal information.
- Expanding to a new worker population or geography.
- Removing mandatory human review.
- Changing fairness or safety logic.
- Changing vendor training or data-reuse rights.
- Adding a critical subprocessor.
- Changing the manual fallback process.
- Reducing logging or monitoring coverage.

---

## 9. Required Change Record

Each change must include:

- Unique change identifier.
- Requester.
- Business owner.
- Technical owner.
- Implementer.
- Tester.
- Approver.
- Business reason.
- Expected benefit.
- Current version.
- Proposed version.
- Affected capabilities.
- Affected data.
- Affected users and parties.
- Affected components and vendors.
- Related risks and controls.
- Change classification and rationale.
- Impact assessment.
- Privacy and security review, when applicable.
- Test and acceptance criteria.
- Implementation plan.
- Communication and training plan.
- Rollback criteria.
- Rollback procedure.
- Monitoring period and owner.
- Approval records.
- Deployment and validation evidence.
- Closure decision.

---

## 10. Change Workflow

### Step 1 — Submit

The requester records the proposed change before implementation.

### Step 2 — Classify

The change is classified as:

- Standard.
- Significant.
- Material.
- Emergency.

### Step 3 — Assess

The assessment considers:

- Purpose and scope.
- Business benefit.
- Affected parties.
- Risk.
- Data.
- Privacy.
- Security.
- Fairness.
- Human oversight.
- Vendor impact.
- Legal and contractual requirements.
- Continuity.
- Documentation.
- Training.
- Monitoring.

### Step 4 — Approve testing

The appropriate owner confirms:

- Test environment.
- Test data.
- Procedures.
- Acceptance criteria.
- Tester independence.
- Evidence requirements.
- Rollback readiness.

### Step 5 — Test

The change undergoes functional and risk-based regression testing.

### Step 6 — Approve deployment

Approval authority is based on the change classification.

### Step 7 — Deploy

Deployment must use:

- Controlled release.
- Authorized access.
- Version control.
- Backup or prior approved state.
- Logging.
- Rollback readiness.

### Step 8 — Validate

PLG confirms:

- The correct version was deployed.
- Required controls function.
- Logs are complete.
- Monitoring is active.
- Users received necessary communication.
- Approval conditions remain satisfied.

### Step 9 — Monitor

The change receives heightened monitoring during the approved stabilization period.

### Step 10 — Close or roll back

The change is closed with evidence or rolled back to the prior approved state.

---

## 11. Revalidation Requirements

| Change effect | Required revalidation |
| --- | --- |
| Functional behavior | Relevant normal, edge, failure, and regression scenarios |
| Routing or safety | Route feasibility, unsafe-condition, constraint, and stop-condition tests |
| Assignment logic | Fairness, workload, opportunity, burden, and feedback-loop analysis |
| Data | Lineage, quality, minimization, privacy, validation, and retention tests |
| Human interface | Usability, explanation, automation-bias, override, and time-pressure tests |
| Security or integration | Authentication, authorization, integrity, replay, secrets, logging, and safe-failure tests |
| Vendor or model | Due diligence, version traceability, limitations, contract, regression, and rollback review |
| Monitoring or logging | Metric calculation, completeness, alert routing, evidence, and reconstruction tests |
| Continuity | Outage, fallback, recovery, and backlog exercise |
| High-impact use | Full impact, risk, control, evaluation, oversight, monitoring, incident, and governance review |

Material changes require the AI Governance Committee to determine whether full lifecycle reassessment is necessary.

---

## 12. Approval Authority

| Change class | Required approval |
| --- | --- |
| Standard | Technical owner operating under an approved procedure |
| Significant | Business owner and technical owner, with GRC review |
| Material | AI Governance Committee; executive approval when High-impact scope or risk acceptance changes |
| Emergency | Designated emergency authority, followed by retrospective committee review |

The requester may not be the sole tester and approver of a Significant or Material change.

---

## 13. Separation of Duties

Where risk warrants, the following responsibilities should be separated:

- Requesting.
- Developing.
- Configuring.
- Testing.
- Approving.
- Deploying.
- Validating.
- Accepting residual risk.

Conflicts or unavoidable role combinations must be documented and reviewed.

---

## 14. Emergency Changes

Emergency changes must:

- Address an active safety, security, privacy, continuity, or severe operational need.
- Use the least risky effective change.
- Preserve available evidence.
- Maintain rollback where possible.
- Receive available emergency authorization.
- Be documented during or immediately after implementation.
- Undergo retrospective assessment.
- Undergo required testing as soon as practical.
- Be removed or formally approved if temporary.

Emergency status must not be used to avoid normal governance.

---

## 15. Deployment Requirements

Before deployment, PLG must confirm:

- Approved change artifact.
- Approved version.
- Successful required tests.
- Closed blocking defects.
- Backup or prior approved state.
- Rollback owner.
- Rollback triggers.
- Rollback procedure.
- User communication.
- Required training.
- Logging readiness.
- Monitoring readiness.
- Incident-response readiness.
- Manual-fallback readiness.
- Appropriate approval.

---

## 16. Rollback Requirements

Rollback must be initiated when:

- Mandatory acceptance criteria fail.
- Severe harm emerges.
- The deployed version differs from the approved version.
- Critical controls fail.
- Logs or monitoring are unreliable.
- Human review cannot be completed.
- Security or privacy compromise is suspected.
- The change creates an unapproved use or impact.
- Safe operation cannot be confirmed.

Rollback activity must be logged and reviewed.

---

## 17. Vendor Changes

Contracts should require:

- Identifiable versions.
- Advance notice of material changes.
- Release notes.
- Impact information.
- Updated limitations.
- Updated performance evidence.
- Subprocessor notice.
- Security and privacy change notice.
- Rollback or delayed-adoption options.

PLG may:

- Delay adoption.
- Request additional evidence.
- Conduct independent testing.
- Restrict affected use.
- Reject the change.
- Roll back.
- Suspend the service.
- Terminate the relationship.

An unannounced material vendor change is an escalation and possible AI incident.

---

## 18. Post-Implementation Monitoring

The change owner must define:

- Monitoring period.
- Metrics.
- Baseline.
- Thresholds.
- Alert recipients.
- Review frequency.
- Stop conditions.
- Stabilization exit criteria.

Monitoring should consider:

- Performance.
- Safety.
- Data quality.
- Fairness.
- Human-review behavior.
- Complaints.
- Incidents.
- Security.
- Privacy.
- Availability.
- Control effectiveness.

---

## 19. Records and Metrics

PLG will monitor:

- Changes by class, owner, and system.
- Emergency changes.
- Unauthorized or unrecorded changes.
- Change failure rate.
- Rollback rate.
- Defects linked to changes.
- Incidents linked to changes.
- Changes deployed without complete evidence.
- Vendor notice compliance.
- Time from deployment to validation.
- Time from deployment to closure.
- Repeated changes affecting the same control or risk.

---

## 20. Exceptions

Exceptions to this standard require:

- Documented business justification.
- Defined scope.
- Risk assessment.
- Compensating controls.
- Accountable owner.
- Approval.
- Expiration date.
- Monitoring requirements.

Exceptions must not remove required review for a Material or high-impact change.

---

## 21. Enforcement

Unauthorized or unrecorded changes may result in:

- Rollback.
- Access suspension.
- Incident investigation.
- Vendor escalation.
- Corrective training.
- Disciplinary or contractual action.
- System suspension.

---

## 22. NIST AI RMF Alignment

| Function | Standard contribution |
| --- | --- |
| GOVERN | Establishes change authority, ownership, approval, documentation, and separation of duties |
| MAP | Requires assessment of changed context, purpose, affected parties, data, and dependencies |
| MEASURE | Requires regression testing, validation, monitoring, and evidence |
| MANAGE | Supports controlled deployment, restriction, rollback, suspension, and reassessment |

---

## 23. Document Control

| Field | Value |
| --- | --- |
| Document title | AI System Change and Revalidation Standard |
| Repository path | `policies/ai-system-change-and-revalidation-standard.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | AI Governance Committee |
| Process owner | CIO / IT Director |
| Approver | Chief Operating Officer |
| Review frequency | At least annually and upon material change |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial AI System Change and Revalidation Standard. |

---

## 24. Related Documents

- [Responsible AI Policy](responsible-ai-policy.md)
- [AI Acceptable Use Standard](ai-acceptable-use-standard.md)
- [AI Governance Charter](../docs/08-ai-governance-charter.md)
- [AI Control Matrix](../docs/09-ai-control-matrix.md)
- [AI Evaluation and Testing Plan](../docs/11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](../docs/12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](../docs/13-ai-incident-response-plan.md)

---

## 25. Portfolio Notice

This standard is an educational artifact for a fictional organization.

It does not establish a real change-management, compliance, authorization, or production-deployment process.
