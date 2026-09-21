# Sample AI Incident Tabletop Record

> **Fictional exercise record — no real incident occurred.**

**Exercise ID:** `TTX-AI-001`  
**System:** `AI-SYS-001` — PLG RouteAssist  
**Scenario date:** 2026-09-20  
**Facilitator:** Business Continuity / Incident Manager

## Scenario

A vendor update changes route behavior without advance notice. RouteAssist recommends an unsafe route for several simulated deliveries. One dispatcher overrides the recommendation, but another approves it. Decision logs are incomplete, and the vendor support contact is initially unavailable.

## Objectives

- Test detection and severity assignment.
- Test suspension and manual fallback authority.
- Test evidence preservation with incomplete logs.
- Test vendor escalation.
- Test return-to-service decision-making.

## Participants

| Function | Role in Exercise |
| --- | --- |
| Incident Management | Incident commander |
| Dispatch | Operational containment |
| IT | Version verification and rollback |
| Security | Integrity and access review |
| Data / AI | Behavior analysis |
| Legal / Privacy | Notification assessment |
| Vendor Management | Vendor escalation |
| GRC | Risk, control, and POA&M updates |

## Exercise Timeline

| Time | Event | Decision |
| --- | --- | --- |
| 09:00 | Unsafe-route complaint received | Open incident and assign Severity 2 |
| 09:08 | Similar recommendations identified | Pause route capability |
| 09:15 | Unapproved vendor version confirmed | Activate manual fallback and vendor escalation |
| 09:28 | Log gaps discovered | Preserve available evidence and widen scope |
| 10:05 | Prior version available | Require regression testing before rollback |
| 11:30 | Tests pass in simulation | Recommend controlled restoration with heightened monitoring |

## Observed Strengths

- Dispatch used override authority.
- Suspension authority was understood.
- Manual fallback was activated.
- Cross-functional incident command was established.

## Gaps

| Gap | Priority | Corrective Action |
| --- | --- | --- |
| Vendor contact path was outdated | High | Establish primary and alternate contacts |
| Version alert did not reach GRC | High | Correct alert distribution |
| Decision logs lacked one required field | High | Correct schema and test completeness |
| Fallback staffing was insufficient at peak volume | High | Update staffing and exercise again |

## Exercise Decision

The scenario would remain restricted until rollback testing, log correction, vendor explanation, and governance approval were complete.

**Repository path:** `evidence/04-sample-ai-incident-tabletop-record.md`
