# Executive Summary and Recommendations

## PLG RouteAssist AI Governance and Risk Assessment

**Prepared for:** Peachtree Logistics Group leadership  
**Prepared by:** Tommy Marshall, GRC Analyst  
**System:** `AI-SYS-001` — PLG RouteAssist  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Date:** 2026-09-20

---

## 1. Executive Decision

PLG should **not authorize unrestricted or production use** of RouteAssist at this stage.

PLG may continue design, vendor review, control implementation, and evaluation. A limited non-medical pilot may be considered only after the mandatory pre-pilot controls are implemented, tested, and approved.

Medical-delivery use should remain excluded until a separate high-impact assessment, successful testing, validated human oversight, and executive approval are completed.

---

## 2. Business Context

RouteAssist is intended to support dispatchers with:

- Delivery-priority recommendations.
- Driver or courier assignment recommendations.
- Route and delivery-sequence recommendations.
- Schedule-adjustment recommendations.
- Exception identification.
- Supporting rationale for human review.

Potential benefits include:

- Faster planning and exception handling.
- More consistent use of operational information.
- Improved route and capacity coordination.
- Better visibility into dispatch decisions and outcomes.
- Reduced administrative burden on dispatch personnel.

These benefits depend on trustworthy data, safe recommendations, effective human review, reliable logging, and timely response when the system fails.

---

## 3. Assessment Scope

The assessment examined:

- Business context and intended use.
- Affected parties and stakeholders.
- Accountability and decision rights.
- System components, integrations, and data flows.
- Impact classification.
- AI risk taxonomy and scoring.
- Governance and control design.
- Human oversight and escalation.
- Evaluation and testing requirements.
- Monitoring and reporting.
- Incident response and operational continuity.
- Third-party and vendor risk.
- Gaps and remediation priorities.

The assessment used the NIST AI Risk Management Framework as its primary organizing framework, supported by ISO/IEC 42001, ISO/IEC 23894, and OECD AI principles.

---

## 4. Overall Risk Posture

RouteAssist is classified as **Tier 4 — Critical Impact** because foreseeable use may affect time-sensitive medical delivery and other safety-sensitive operations.

The initial risk register contains:

| Rating | Inherent risks | Target residual risks |
| --- | ---: | ---: |
| Critical | 2 | 0 |
| High | 18 | 3 |
| Moderate | 0 | 14 |
| Low | 0 | 3 |
| **Total** | **20** | **20** |

Current risk remains equal to inherent risk because planned controls have not been implemented or validated.

Target residual ratings represent planning objectives. They are not evidence that risks have already been reduced or accepted.

---

## 5. Most Significant Findings

### 5.1 Safety and medical-delivery exposure

An inappropriate priority or unsafe route could cause severe delay, service failure, or harm to a recipient.

Medical-delivery use must be blocked during the initial pilot. Future medical use requires:

- A separate high-impact assessment.
- Verified delivery classification.
- Enhanced human review.
- Medical-specific testing.
- Validated fallback.
- Heightened monitoring.
- Executive authorization.

### 5.2 Human oversight is not yet demonstrated

Advisory status alone does not ensure safety.

Dispatchers must be able to:

- Detect incorrect, incomplete, unsafe, or unfair recommendations.
- Recognize stale or conflicting data.
- Understand rationale and uncertainty.
- Resist automation bias.
- Override or reject recommendations.
- Escalate concerns.
- Invoke manual fallback.
- Perform these activities under realistic workload and time pressure.

### 5.3 Data and traceability are foundational gaps

PLG has not yet demonstrated:

- Complete data inventory and lineage.
- Approved data ownership.
- Data minimization and purpose limitation.
- Input validation and freshness controls.
- Complete decision and version logging.
- End-to-end reconstruction of material decisions.

Without reliable data and traceability, PLG cannot confidently evaluate performance, investigate incidents, or validate control effectiveness.

### 5.4 Workforce impact requires active governance

Historical assignment patterns and operational proxies may create unequal outcomes involving:

- Workload.
- Assignment opportunity.
- Route distance.
- Undesirable routes.
- Scheduling burden.
- Earnings-related opportunity.
- Complaint or dispute rates.

RouteAssist information must not be used for unauthorized employee ranking, discipline, termination, compensation, or performance evaluation.

### 5.5 Vendor dependence creates material uncertainty

PLG lacks vendor evidence concerning:

- Model and service design.
- Training and evaluation data.
- Performance limitations.
- Security and privacy controls.
- Data retention and reuse.
- Subprocessors.
- Material-change notification.
- Incident cooperation.
- Resilience and recovery.
- Portability and exit.

Vendor selection and production connection should remain pending.

### 5.6 Monitoring and response are not operational

PLG has designed, but not implemented or tested:

- Performance and drift monitoring.
- Assignment-outcome analysis.
- Human-review and override monitoring.
- Complaint and dispute handling.
- Security and privacy alerts.
- Manual fallback.
- AI incident response.
- Return-to-service procedures.

---

## 6. Critical and High-Priority Risks

| Risk ID | Risk | Inherent rating | Target rating |
| --- | --- | --- | --- |
| `AIR-001` | Inappropriate medical-delivery priority or route | Critical | High |
| `AIR-002` | Unsafe or impractical route recommendation | Critical | High |
| `AIR-003` | Inaccurate, incomplete, or stale input data | High | Moderate |
| `AIR-004` | Unequal driver or courier assignment outcomes | High | Moderate |
| `AIR-005` | Automation bias and ineffective human review | High | Moderate |
| `AIR-007` | Excessive or unauthorized personal-data processing | High | Moderate |
| `AIR-008` | Unauthorized access or privileged misuse | High | Moderate |
| `AIR-009` | Manipulated inputs, integrations, or outputs | High | High |
| `AIR-010` | Vendor opacity or unannounced material change | High | Moderate |
| `AIR-011` | Model or data drift degrades recommendations | High | Moderate |
| `AIR-014` | Incomplete logging and weak traceability | High | Moderate |
| `AIR-015` | Monitoring fails to detect harmful patterns | High | Moderate |
| `AIR-017` | Delayed or ineffective AI incident response | High | Moderate |

The target state retains three High risks because severe impact cannot be eliminated solely through preventive controls. These risks require continuing executive awareness, strong evidence, monitoring, and formal acceptance.

---

## 7. Priority Recommendations

### Priority 1 — Establish enforceable governance

- Approve the AI Governance Charter.
- Confirm committee membership, quorum, and authority.
- Assign accountable risk and control owners.
- Implement lifecycle approval gates.
- Enforce approved and prohibited uses.
- Require documented, time-limited risk acceptance.

### Priority 2 — Block high-impact exposure

- Exclude medical delivery from the initial pilot.
- Enforce advisory-only operation.
- Require human approval before downstream execution.
- Implement safety stop conditions.
- Establish emergency restriction and suspension authority.
- Preserve a tested manual process.

### Priority 3 — Build trustworthy data and evidence

- Complete data inventory, lineage, ownership, classification, and minimization.
- Implement schema, completeness, plausibility, conflict, and freshness validation.
- Capture model and system version.
- Log the recommendation, human decision, override, downstream action, and outcome.
- Demonstrate end-to-end decision reconstruction.

### Priority 4 — Validate technical and human performance

- Approve evaluation thresholds before testing.
- Test normal, edge, high-impact, adversarial, misuse, and failure scenarios.
- Conduct assignment-outcome and feedback-loop analysis.
- Test reviewers under realistic workload and time pressure.
- Correct and retest all blocking defects.

### Priority 5 — Control vendors and material changes

- Complete vendor due diligence.
- Require model and service documentation.
- Establish contractual data-use and security restrictions.
- Require advance material-change and incident notice.
- Preserve audit, testing, rollback, suspension, portability, and deletion rights.
- Do not connect the vendor until critical evidence is approved.

### Priority 6 — Prepare for operation and failure

- Implement governance dashboards and alert routing.
- Establish complaint, dispute, and correction channels.
- Exercise manual fallback.
- Conduct an AI incident-response tabletop.
- Complete all blocking POA&M actions.
- Require return-to-service approval following a material incident.

---

## 8. Recommended Roadmap

| Phase | Objective | Exit criterion |
| --- | --- | --- |
| Phase 1 — Governance and boundaries | Approve charter, scope, risk methodology, use restrictions, and owners | Authority and approval gates documented |
| Phase 2 — Vendor, data, and control implementation | Complete vendor review, data governance, access, integrations, logging, and procedures | Mandatory controls implemented |
| Phase 3 — Evaluation and exercises | Execute technical, fairness, human-factor, security, fallback, and incident tests | Mandatory thresholds pass and blocking defects are remediated |
| Phase 4 — Limited non-medical pilot | Operate within restricted users, services, geography, volume, and duration | Pilot evidence supports controlled continuation |
| Phase 5 — Production decision | Review residual risk, assurance, open POA&M items, and conditions | Formal authorization, restriction, deferment, or rejection |
| Phase 6 — Continuous governance | Monitor, reassess, respond, improve, and retire safely | Continuing compliance with approval conditions |

---

## 9. Pilot Conditions

If leadership authorizes a limited pilot, the authorization should define:

- Non-medical use only.
- Approved users and named accounts.
- Approved delivery and service types.
- Approved geography.
- Maximum volume and duration.
- Mandatory human review.
- Required logging.
- Enhanced monitoring.
- Daily supervisor review.
- Complaint and incident channels.
- Stop conditions.
- Manual fallback.
- Pilot success and failure criteria.
- Pilot expiration date.
- Required committee review before expansion.

Pilot approval must not be treated as production approval.

---

## 10. POA&M Summary

The initial POA&M contains 16 remediation items:

| Priority | Count |
| --- | ---: |
| Critical | 2 |
| High | 9 |
| Moderate | 5 |
| **Total** | **16** |

The two Critical actions address:

1. Exclusion and control of unauthorized medical-delivery functionality.
2. Validation of route-safety performance and edge-case behavior.

The remaining High-priority actions address governance, data, vendor evidence, access control, integration security, fairness, human oversight, logging, monitoring, incident response, and fallback.

---

## 11. Leadership Decisions Required

Leadership should decide whether to:

1. Approve the AI Governance Charter and committee authority.
2. Confirm medical-delivery exclusion from the initial pilot.
3. Fund required data, logging, monitoring, testing, and continuity work.
4. Require vendor evidence and contractual protections before connection.
5. Approve POA&M owners and milestone dependencies.
6. Require a formal pre-pilot readiness review.
7. Require executive approval before any future medical-delivery use.
8. Confirm that Critical residual risk is outside normal risk appetite.

---

## 12. Conditions That Should Block Deployment

Pilot or production use should be blocked when:

- Medical use is not effectively excluded.
- Severe route-safety defects remain.
- Mandatory human review can be bypassed.
- Critical data validation is absent or unreliable.
- Required logs cannot reconstruct decisions.
- Unauthorized access or integration-manipulation weaknesses remain.
- Vendor identity, version, or material-change practices are unknown.
- Manual fallback is unavailable.
- Incident-response roles and authority are unclear.
- Mandatory evaluation thresholds fail.
- Critical or High POA&M items remain unresolved without authorized treatment.

---

## 13. Conclusion

RouteAssist may create operational value, but PLG does not yet have evidence sufficient to support deployment.

The appropriate decision is controlled progression:

1. Establish governance.
2. Implement controls.
3. Validate technical and human performance.
4. Run a restricted non-medical pilot.
5. Evaluate pilot evidence.
6. Authorize broader use only when evidence supports the residual risk.

This approach protects operational value without treating speed, automation, or vendor claims as substitutes for accountability.

---

## 14. NIST AI RMF Alignment

| Function | Executive application |
| --- | --- |
| GOVERN | Establish accountable leadership, authority, policies, risk tolerance, and oversight |
| MAP | Define context, purpose, affected parties, impacts, dependencies, and boundaries |
| MEASURE | Evaluate performance, safety, fairness, privacy, security, human oversight, and uncertainty |
| MANAGE | Prioritize treatment, restrict high-impact use, respond to incidents, and authorize lifecycle decisions |

---

## 15. Document Control

| Field | Value |
| --- | --- |
| Document title | Executive Summary and Recommendations |
| Repository path | `docs/16-executive-summary-and-recommendations.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | GRC Analyst |
| Approver | Chief Operating Officer |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial executive risk summary, deployment recommendation, priority actions, roadmap, and leadership decisions. |

---

## 16. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [AI Risk Register](06-ai-risk-register.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Third-Party and Vendor AI Risk Review](14-third-party-and-vendor-ai-risk-review.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)
- [Lessons Learned and Portfolio Reflection](17-lessons-learned-and-portfolio-reflection.md)

---

## 17. Portfolio Notice

This executive summary describes a fictional organization and AI system.

It is not a real authorization, legal opinion, compliance determination, certification, independent assurance conclusion, or guarantee that an AI system is safe, fair, secure, private, reliable, or appropriate for deployment.
