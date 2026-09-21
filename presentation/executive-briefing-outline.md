# Executive Briefing Outline

## Presentation Purpose

This outline supports a concise executive briefing on the governance and risk assessment of PLG RouteAssist (`AI-SYS-001`, use case `UC-001`). It is structured for a 15–20 minute presentation followed by questions.

---

## Slide 1 — RouteAssist AI Governance and Risk Assessment

### On-Slide Content

- PLG RouteAssist (`AI-SYS-001`)
- Executive governance decision briefing
- Presenter, role, and date

### Speaker Notes

State that RouteAssist is a decision-support system for dispatch routing. Emphasize that the assessment addresses whether the use case is governed, controlled, testable, and ready for a limited pilot—not whether the technology is impressive in isolation.

---

## Slide 2 — Decision Requested

### On-Slide Content

- Confirm the current Tier 4 impact classification
- Endorse the proposed risk-treatment plan
- Maintain the deployment hold until critical entry criteria are met
- Assign accountable owners and remediation resources

### Speaker Notes

Frame the briefing around a decision. The recommended decision is conditional: leadership may endorse the use case and remediation roadmap, but production or pilot authorization should wait until the specified safeguards are implemented and evidenced.

---

## Slide 3 — Business Context and Intended Value

### On-Slide Content

- Reduce dispatch planning time
- Improve route consistency and responsiveness
- Help dispatchers evaluate operational constraints
- Preserve human authority over final routing decisions

### Speaker Notes

Explain that the system supports, but does not replace, dispatch personnel. Benefits depend on reliable source data, usable explanations, trained reviewers, and a functioning manual fallback.

---

## Slide 4 — Scope and Prohibited Uses

### On-Slide Content

- In scope: non-medical courier route recommendations
- Users: trained dispatch personnel and supervisors
- Human approval required before operational action
- Out of scope: autonomous dispatch and medical routing

### Speaker Notes

Clarify the assessment boundary. The initial deployment excludes medical deliveries and any fully autonomous routing. Expansion requires a new impact and risk review rather than informal reuse.

---

## Slide 5 — Impact Classification

### On-Slide Content

- Classification: Tier 4 — High Impact
- Safety and service consequences are plausible
- Location and operational data create privacy concerns
- Third-party data and models create dependency risk
- Human review reduces, but does not eliminate, impact

### Speaker Notes

Describe classification as a governance trigger. Tier 4 requires stronger approval, testing, oversight, monitoring, incident response, documentation, and executive visibility.

---

## Slide 6 — Inherent and Target Risk Profile

### On-Slide Content

| Risk Level | Inherent | Target Residual |
| --- | ---: | ---: |
| Critical | 2 | 0 |
| High | 18 | 3 |
| Moderate | 0 | 14 |
| Low | 0 | 3 |

- Twenty risks assessed across the lifecycle
- Target profile assumes planned controls operate effectively

### Speaker Notes

Stress that target residual ratings are goals, not current facts. They become credible only when controls are implemented, tested, and supported by evidence.

---

## Slide 7 — Priority Risk Themes

### On-Slide Content

- Stale, incomplete, or inaccurate operational inputs
- Unsafe or infeasible route recommendations
- Automation bias and ineffective human challenge
- Incomplete logging and weak traceability
- Vendor, model-change, and service-continuity risk
- Privacy, security, and unauthorized-use risk

### Speaker Notes

Connect these themes to realistic failure modes: a route may appear efficient while relying on old closure data; a busy reviewer may accept it without challenge; and incomplete records may prevent reconstruction after an incident.

---

## Slide 8 — Governance and Control Design

### On-Slide Content

- Named executive, business, system, data, and control owners
- AI Governance Committee approval and oversight
- Twenty-four mapped controls across the lifecycle
- Formal change, exception, incident, and risk-acceptance processes
- Evidence-based monitoring and periodic reassessment

### Speaker Notes

Explain that accountability is distributed but explicit. Operational teams operate controls, specialist functions challenge and advise, the governance committee makes lifecycle decisions, and executives accept material residual risk within defined authority.

---

## Slide 9 — Human Oversight and Assurance

### On-Slide Content

- Reviewer can approve, modify, reject, or escalate
- Manual fallback remains available
- Decisions and reasons are logged
- Testing covers performance, safety, bias, robustness, and controls
- Challenge-rate and override trends are monitored

### Speaker Notes

Meaningful oversight requires more than placing a person in the workflow. Reviewers need adequate information, training, authority, time, and a process that detects both over-reliance and indiscriminate rejection.

---

## Slide 10 — Gap Assessment and POA&M

### On-Slide Content

| Priority | Open Actions |
| --- | ---: |
| Critical | 2 |
| High | 9 |
| Moderate | 5 |
| **Total** | **16** |

- Critical themes: scope enforcement and safety-critical input controls
- High-priority themes: logging, monitoring, vendor governance, testing, and incident readiness

### Speaker Notes

State that the plan of action and milestones assigns an owner, due date, evidence requirement, and validation method to every material gap. Overdue critical or high actions should be visible to the governance committee.

---

## Slide 11 — Readiness Gates and Roadmap

### On-Slide Content

1. Implement critical technical and procedural safeguards.
2. Complete independent control and model testing.
3. Train dispatchers and validate manual fallback.
4. Conduct an incident-response tabletop exercise.
5. Obtain governance approval for a constrained pilot.
6. Monitor pilot thresholds before any expansion.

### Speaker Notes

Present the roadmap as gated progression. A missed gate stops advancement; it does not simply become a post-launch action. Expansion in geography, user population, data, vendor, or purpose triggers reassessment.

---

## Slide 12 — Executive Actions

### On-Slide Content

- Endorse the Tier 4 classification and restricted scope
- Maintain the deployment hold pending entry-criteria evidence
- Confirm accountable executives and action owners
- Fund remediation, assurance, training, and fallback capacity
- Require committee review of residual risk before pilot approval

### Speaker Notes

Close with specific ownership and resourcing decisions. Avoid asking leadership to accept residual risk before control evidence is available.

---

## Slide 13 — Closing Position

### On-Slide Content

- Business value is plausible
- Current governance and control gaps are material
- Risk can be reduced through the defined roadmap
- Recommendation: proceed with remediation, not deployment

### Speaker Notes

Summarize the posture in one sentence: RouteAssist may advance toward a constrained pilot only after critical gaps are closed, high-priority controls are tested, and the AI Governance Committee confirms that residual risk is within tolerance.

---

## Anticipated Executive Questions

### Why is the system Tier 4 if a human makes the final decision?

Human review is an important control, but reviewers can face incomplete information, time pressure, and automation bias. The underlying recommendations may still influence safety- and service-relevant actions.

### What must be true before a pilot begins?

Prohibited-use enforcement, input validation, traceable logs, trained reviewers, tested fallback procedures, incident readiness, and defined monitoring thresholds must be implemented and validated.

### Who can stop the system?

Authorized operational supervisors and system owners may activate the approved pause and fallback procedures. The AI Governance Committee may suspend or withdraw lifecycle approval.

### How will leadership know the controls work?

Control testing, model evaluation, monitoring reports, human-review records, incident exercises, and remediation validation provide evidence. Target residual risk is not accepted solely on the basis of design documents.

### What would trigger reassessment?

Material changes to purpose, users, geography, data, vendors, model behavior, autonomy, integrations, or risk performance trigger review. Significant incidents or recurring threshold breaches also trigger reassessment.

## Suggested Appendix Slides

- Full AI risk register
- Risk heat map and residual-risk comparison
- Control crosswalk
- Testing matrix and acceptance thresholds
- Monitoring metrics and escalation thresholds
- POA&M detail
- System context, data flow, accountability, and oversight diagrams

## Source Deliverables

- `docs/01-organization-profile-and-ai-use-case.md`
- `docs/03-ai-system-inventory.md`
- `docs/06-ai-risk-register.md`
- `docs/09-ai-control-framework.md`
- `docs/11-ai-testing-and-assurance-plan.md`
- `docs/15-gap-assessment-and-poam.md`
- `docs/16-implementation-roadmap.md`
- `docs/17-executive-summary-and-portfolio-narrative.md`

## Repository Path

`presentation/executive-briefing-outline.md`
