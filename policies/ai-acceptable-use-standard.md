# AI Acceptable Use Standard

## Peachtree Logistics Group

**Standard owner:** AI Governance Committee  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Effective date:** Upon approval  
**Review frequency:** At least annually and upon material change

---

## 1. Purpose

This standard defines permitted, restricted, and prohibited use of artificial intelligence for PLG business.

It supports the Responsible AI Policy by giving personnel practical rules for using AI systems and services.

---

## 2. Scope

This standard applies to all personnel using AI with:

- PLG work.
- PLG systems.
- PLG data.
- Customers.
- Employees.
- Drivers.
- Independent couriers.
- Shipment recipients.
- Vendors.
- Business decisions.
- Operational processes.

It applies whether the AI service is:

- Developed internally.
- Purchased from a vendor.
- Embedded in another platform.
- Publicly available.
- Free or paid.
- Used on a corporate or personal device.

---

## 3. Core Rule

Personnel may use only:

- PLG-approved AI services.
- Registered use cases.
- Approved data.
- Assigned access.
- Approved human-review procedures.

AI output is a recommendation or draft unless an approved use case explicitly states otherwise.

The authorized human user remains responsible for:

- Validation.
- Final decisions.
- Downstream actions.
- Escalation.
- Compliance with PLG requirements.

---

## 4. Permitted Use

Subject to use-case approval and data restrictions, personnel may:

- Use RouteAssist for approved non-medical advisory dispatch recommendations.
- Review, modify, reject, override, or escalate RouteAssist recommendations.
- Use approved synthetic or de-identified data for authorized testing.
- Create low-risk drafts or summaries using approved tools.
- Use approved AI for administrative assistance that does not create consequential decisions.
- Analyze approved non-sensitive information.
- Report errors, limitations, harmful outcomes, complaints, and incidents.
- Participate in authorized evaluation, monitoring, and training.

Permitted use does not remove the requirement to verify output.

---

## 5. Restricted Use

The following activities require documented assessment and approval:

- Safety-sensitive operations.
- Time-critical operations.
- Medical-delivery routing, priority, or assignment.
- Decisions affecting employment, scheduling, workload, compensation, or work opportunity.
- Personal, sensitive, confidential, regulated, or location data.
- New vendors or models.
- New integrations.
- New data sources.
- New geographic areas.
- New affected populations.
- Automated downstream actions.
- Model training or tuning using PLG information.
- External publication of AI-generated PLG content.
- Customer-facing AI interactions.
- Biometric or behavioral analysis.
- High-impact recommendations.
- Use that materially changes an approved business process.

Restricted use may not begin until the required approval is documented.

---

## 6. Prohibited Use

Personnel must not:

- Use an unapproved AI service for PLG business.
- Use AI for an unregistered purpose.
- Enter passwords or authentication secrets into an AI system.
- Enter payment information into an unapproved AI system.
- Enter PHI, medical-delivery details, personal records, confidential contracts, or restricted information into an unapproved service.
- Use RouteAssist for medical delivery during the excluded pilot.
- Allow RouteAssist to execute dispatch decisions without required human approval.
- Use AI output as the sole basis for hiring, discipline, termination, compensation, or performance ratings.
- Infer protected or highly sensitive characteristics.
- Use protected characteristics or unjustified proxies to allocate work or opportunity.
- Create deceptive, fraudulent, harassing, discriminatory, illegal, or unsafe content or action.
- Circumvent access control, logging, monitoring, validation, approval, or stop conditions.
- Conceal material AI use when disclosure is required.
- Treat unverified AI output as confirmed fact.
- Repurpose PLG or personal data for unrelated vendor training.
- Continue using a suspended capability or known unsafe workflow.
- Use AI to impersonate an individual without authorization.
- Upload copyrighted, licensed, or third-party information without appropriate rights.
- Use AI-generated code or configuration without required review and testing.

---

## 7. User Responsibilities

Before using AI, users must:

1. Confirm that the service is approved.
2. Confirm that the use case is registered.
3. Confirm that they are authorized.
4. Use only necessary and permitted data.
5. Follow data-classification and privacy requirements.
6. Review source data, rationale, uncertainty, and limitations.
7. Validate output before acting on or sharing it.
8. Consider safety, fairness, privacy, security, and affected-party impact.
9. Document approval, modification, rejection, override, or escalation when required.
10. Report suspected errors, misuse, incidents, complaints, or policy violations.
11. Stop and use the approved fallback when safe use cannot be confirmed.

---

## 8. Output Validation

Users must evaluate AI output for:

- Accuracy.
- Completeness.
- Relevance.
- Current information.
- Unsupported assumptions.
- Bias or harmful impact.
- Confidentiality.
- Security concerns.
- Legal or contractual restrictions.
- Operational feasibility.
- Appropriate tone and audience.

Users must not represent AI-generated output as independently verified when it has not been validated.

---

## 9. Data-Handling Rules

### 9.1 Approved data

Only data included in the approved use-case data inventory or field allowlist may be entered into the AI system.

### 9.2 Sensitive data

Sensitive data requires documented approval and appropriate safeguards.

Examples include:

- Personal information.
- Precise location.
- Employee records.
- Driver or courier performance records.
- Customer information.
- Recipient information.
- Medical-delivery information.
- Payment information.
- Confidential contracts.
- Security information.

### 9.3 Data minimization

Users must provide only the minimum data needed for the approved task.

### 9.4 Free-text fields

Free-text fields must not be used to bypass approved data restrictions.

### 9.5 Output handling

AI output must be classified and protected according to the information it contains.

---

## 10. RouteAssist-Specific Rules

RouteAssist remains advisory-only.

Users must comply with the following:

- Named accounts are required.
- MFA is required where supported.
- Dispatchers must complete competency training before access.
- Medical deliveries are blocked during the initial pilot.
- Every recommendation requires authorized human review.
- Reviewers may modify, reject, override, or escalate recommendations.
- Good-faith override and escalation are protected from retaliation.
- Missing, stale, conflicting, unsafe, or out-of-scope cases must be rejected or escalated.
- RouteAssist records may not be used for unauthorized worker surveillance or performance management.
- Decisions must remain traceable to the reviewer and approved action.
- Users must activate fallback when RouteAssist cannot be used safely.
- Users must obey stop conditions and suspension notices.

---

## 11. Human-Review Requirements

A reviewer must not approve a recommendation unless the reviewer can:

- Confirm the use is within scope.
- Review the material input information.
- Assess data quality and freshness.
- Consider operational feasibility.
- Understand the recommendation basis.
- Review relevant limitations or uncertainty.
- Consider affected-party impact.
- Select an appropriate action.
- Document the decision.
- Confirm the approved action was executed.

If meaningful review cannot be completed, the recommendation must not be approved.

---

## 12. Reporting and Escalation

Personnel must immediately report:

- Severe safety concerns.
- Medical-use exclusion failures.
- Human-review bypass.
- Unauthorized sensitive data.
- Suspected account or integration compromise.
- Harmful assignment disparity.
- Missing or unreliable decision logs.
- Unapproved model or vendor changes.
- Use outside approved scope.
- Inability to activate manual fallback.
- A formal stop condition.

Routine errors and feedback should be submitted through the designated support or complaint channel.

---

## 13. Use of Public AI Services

Public AI services may be used for PLG work only when expressly approved.

Users must not assume that:

- Free services are private.
- Prompts will not be retained.
- Data will not be used for training.
- Output is confidential.
- Output is accurate.
- Vendor terms satisfy PLG requirements.

Browser extensions, plug-ins, personal accounts, and mobile AI applications are subject to the same approval requirements.

---

## 14. AI-Generated Communications

AI-generated communications must be reviewed before distribution.

The reviewer must confirm:

- Accuracy.
- Appropriate audience.
- Confidentiality.
- Tone.
- Legal and contractual restrictions.
- Whether disclosure of AI involvement is required.
- That the communication does not mislead the recipient.

High-impact, legal, medical, financial, HR, or security communications require appropriate subject-matter review.

---

## 15. AI-Generated Code and Configuration

AI-generated code, scripts, rules, formulas, or configurations must:

- Be reviewed by an authorized person.
- Be tested in a controlled environment.
- Undergo security review appropriate to risk.
- Avoid embedded credentials or secrets.
- Follow change-management requirements.
- Include rollback capability where appropriate.
- Not be placed into production based solely on AI output.

---

## 16. Exceptions

Exceptions require prior written approval.

The exception must identify:

- The restricted requirement.
- Business rationale.
- Scope.
- Risk.
- Compensating controls.
- Owner.
- Approver.
- Effective date.
- Expiration date.
- Monitoring requirements.

Emergency use must follow the emergency-change and incident-response processes.

---

## 17. Monitoring

PLG may monitor approved AI use for:

- Security.
- Privacy.
- Compliance.
- Performance.
- Safety.
- Cost.
- Access.
- Data handling.
- Prohibited use.
- Incident investigation.

Monitoring must itself comply with PLG privacy, workforce, and access requirements.

---

## 18. Enforcement

Violations may result in:

- Access removal.
- Corrective training.
- Investigation.
- Contractual action.
- Disciplinary action.
- Incident-response activation.
- System restriction or suspension.
- Vendor escalation.

Enforcement should be consistent, documented, and proportionate.

---

## 19. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Acceptable Use Standard |
| Repository path | `policies/ai-acceptable-use-standard.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | AI Governance Committee |
| Approver | Chief Operating Officer |
| Review frequency | At least annually and upon material change |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial PLG AI Acceptable Use Standard. |

---

## 20. Related Documents

- [Responsible AI Policy](responsible-ai-policy.md)
- [AI System Change and Revalidation Standard](ai-system-change-and-revalidation-standard.md)
- [Human Oversight and Escalation Plan](../docs/10-human-oversight-and-escalation-plan.md)
- [AI Incident Response Plan](../docs/13-ai-incident-response-plan.md)

---

## 21. Portfolio Notice

This standard is an educational artifact for a fictional organization.

It is not legal advice and has not been adopted as a real workplace rule.
