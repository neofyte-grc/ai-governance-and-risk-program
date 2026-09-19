# Organization Profile and AI Use Case

## Peachtree Logistics Group — PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Document owner:** GRC Analyst  
**Business owner:** Dispatch Director  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** Annually and upon material use-case change

---

## 1. Document Purpose

This document defines the fictional organization, operating environment, business need, and proposed use of PLG RouteAssist. It establishes what the system is intended to do, what it is not permitted to do, who uses it, who may be affected by it, what decisions remain with people, and which conditions must be satisfied before PLG considers a pilot or operational deployment.

This profile provides the business and operational context required for later stakeholder analysis, impact screening, data-flow mapping, risk assessment, control design, evaluation, monitoring, and incident response.

---

## 2. Organization Profile

### 2.1 Company overview

**Peachtree Logistics Group (PLG)** is a fictional regional logistics company headquartered in Atlanta, Georgia. PLG coordinates warehousing, freight movement, last-mile delivery, and medical courier services throughout the southeastern United States.

PLG operates in a time-sensitive environment where delayed, misrouted, or improperly prioritized deliveries can create financial loss, service failures, contractual issues, safety concerns, customer dissatisfaction, and reputational harm.

| Attribute | Description |
| --- | --- |
| Organization | Peachtree Logistics Group |
| Status | Fictional organization created for this portfolio case study |
| Headquarters | Atlanta, Georgia |
| Region served | Southeastern United States |
| Approximate workforce | 225 employees plus independent couriers |
| Industry | Transportation, logistics, warehousing, and courier services |
| Operating model | Mixed office, warehouse, dispatch, mobile, and third-party operations |
| Technology model | Mixed cloud, on-premises, mobile, and vendor-hosted systems |
| Operating priority | Reliable and timely movement of goods without compromising safety, privacy, security, or contractual commitments |

### 2.2 Core services

PLG provides:

- Warehousing and inventory coordination
- Freight brokerage
- Regional transportation coordination
- Last-mile delivery
- Medical courier services
- Delivery scheduling and dispatch
- Shipment tracking and exception management
- Proof-of-delivery and customer reporting

### 2.3 Workforce groups

PLG's workforce includes:

- Executive and administrative staff
- Customer-service and order-intake personnel
- Dispatchers and dispatch supervisors
- Warehouse employees and supervisors
- PLG-employed drivers
- Independent couriers
- Billing and accounting personnel
- Information technology and security personnel
- GRC, privacy, legal, procurement, and vendor-management personnel

Employees and contractors may access PLG services using a combination of company-issued computers, company-issued mobile devices, warehouse terminals, vehicle-mounted devices, and approved personal mobile devices.

### 2.4 Technology environment

PLG's fictional technology environment includes:

| Technology | Business purpose |
| --- | --- |
| Microsoft 365 | Email, collaboration, document storage, and internal communication |
| Logistics and freight brokerage platform | Customer orders, shipment coordination, carrier activity, and freight records |
| Warehouse Management System | Inventory, warehouse activity, staging, and fulfillment information |
| Dispatch and delivery platform | Driver assignments, routes, status updates, proof of delivery, and exceptions |
| Billing and accounting system | Invoicing, payment records, costs, and financial reporting |
| Mapping and traffic services | Route, distance, travel-time, traffic, and geolocation information |
| Mobile applications | Driver and courier assignments, navigation, status, and delivery confirmation |
| Identity and access services | User authentication, authorization, and account administration |
| Logging and monitoring services | System activity, alerts, events, and operational reporting |
| RouteAssist | AI-assisted operational recommendations |

### 2.5 Information handled

PLG handles or may process:

- Employee and contractor records
- Driver and courier identity and availability information
- Customer and shipment information
- Delivery addresses and geolocation data
- Delivery dates, windows, priorities, and service levels
- Vehicle and route information
- Proof-of-delivery records
- Customer complaints and delivery exceptions
- Medical-delivery indicators and limited healthcare-client delivery details
- Payment and billing information
- Contracts and vendor information
- System logs, access records, and security events
- RouteAssist recommendations, reviewer decisions, overrides, and rationales

The presence of workforce, location, customer, and medical-delivery information increases the importance of access control, purpose limitation, data minimization, retention, monitoring, and human oversight.

---

## 3. Operating Context

### 3.1 Standard delivery lifecycle

PLG's simplified delivery lifecycle consists of:

| Process ID | Process | Description |
| --- | --- | --- |
| `P1` | Order intake | A commercial or healthcare customer submits a shipment or delivery request. |
| `P2` | Review and scheduling | PLG confirms requirements, delivery windows, service level, destination, and available capacity. |
| `P3` | Dispatch and assignment | Dispatch selects a driver or courier and determines priority, route, and timing. |
| `P4` | Pickup and delivery | The assigned driver or courier collects and transports the shipment. |
| `P5` | Delivery confirmation | PLG records delivery status, proof of delivery, exceptions, and recipient confirmation. |
| `P6` | Billing and records | PLG generates billing records and retains required operational documentation. |

RouteAssist primarily supports `P2` and `P3`, but its recommendations may influence `P4`, `P5`, and `P6`.

### 3.2 Operational characteristics

PLG operations include:

- High-volume and time-sensitive dispatch decisions
- Changing traffic and weather conditions
- Variable driver, courier, and vehicle availability
- Customer-specific delivery windows and service levels
- Routine and exceptional delivery scenarios
- Independent couriers with varying schedules and devices
- Urgent and time-sensitive medical deliveries
- Operational decisions made under time pressure
- Multiple upstream data sources and third-party services

These conditions can make AI-assisted recommendations useful, but they also increase the risk of incomplete context, automation bias, and inappropriate reliance on historical patterns.

---

## 4. Business Need

PLG dispatchers currently combine information from order records, delivery windows, driver availability, mapping tools, customer requirements, incident reports, and personal operational experience.

The process can become difficult during high-volume periods, disruptions, or staffing shortages. Relevant information may be distributed across multiple systems, and different dispatchers may make different decisions using similar facts.

PLG is evaluating RouteAssist to determine whether AI-assisted recommendations can:

- Reduce the time required to review routine delivery options
- Help dispatchers identify feasible routes and assignments
- Improve consistency in exception classification
- Surface potential delays earlier
- Support more timely operational adjustments
- Reduce repetitive manual comparison across systems
- Provide supervisors with a documented recommendation history
- Allow personnel to focus more attention on complex or high-impact exceptions

PLG does not assume that these benefits will occur. Each expected benefit must be evaluated against measurable criteria and balanced against risk.

---

## 5. AI Use-Case Statement

### 5.1 Use-case summary

PLG proposes using RouteAssist to analyze authorized operational data and generate recommendations that assist qualified dispatch and operations personnel with delivery planning and exception management.

RouteAssist may recommend:

- Delivery priority
- Driver or courier assignment
- Proposed route
- Estimated travel or delivery timing
- Operational exception category
- Potential schedule adjustment
- Need for supervisory review

### 5.2 Formal use-case statement

> PLG RouteAssist will provide advisory recommendations to authorized dispatch and operations personnel to support delivery prioritization, assignment, routing, scheduling, and exception classification. Qualified personnel will review relevant recommendations, consider operational context unavailable to the system, and retain authority to accept, modify, reject, override, or escalate the recommendation.

### 5.3 Intended outcome

The intended outcome is better-informed and more consistent operational decision support without removing human judgment, accountability, or escalation authority.

### 5.4 Decision role

RouteAssist is **advisory**.

The system may organize information and generate a recommendation. It may not be treated as the final decision maker for consequential operational, employment, service-access, or risk-acceptance decisions.

---

## 6. Proposed System Capabilities

The proposed RouteAssist capabilities are:

| Capability ID | Capability | Description | Human role |
| --- | --- | --- | --- |
| `CAP-001` | Delivery prioritization | Recommend an operational priority using delivery windows, service level, shipment indicators, and known conditions. | Dispatcher reviews and confirms; defined high-impact cases require supervisor approval. |
| `CAP-002` | Assignment recommendation | Recommend an eligible driver or courier using availability, location, vehicle, service, and scheduling information. | Dispatcher verifies eligibility and operational context before assignment. |
| `CAP-003` | Route recommendation | Recommend a route using authorized mapping, traffic, destination, and delivery-window information. | Driver or dispatcher may reject or modify based on safety and current conditions. |
| `CAP-004` | Exception classification | Suggest a category for delays, delivery failures, routing issues, or other operational exceptions. | Authorized employee validates the classification before downstream use. |
| `CAP-005` | Schedule-adjustment recommendation | Recommend a change in timing, sequence, or assignment when operating conditions change. | Dispatcher reviews affected deliveries and approves or rejects the change. |
| `CAP-006` | Escalation flag | Identify recommendations or conditions that may require supervisory review. | Human supervisor determines the appropriate action. |

These capabilities are proposed. They must be evaluated, controlled, and approved before operational reliance.

---

## 7. Intended Users

### 7.1 Primary users

| User group | Authorized use |
| --- | --- |
| Dispatchers | Review recommendations, compare operational context, and make routine dispatch decisions within assigned authority. |
| Dispatch supervisors | Review escalated or high-impact cases, monitor overrides, approve defined exceptions, and suspend reliance when necessary. |
| Operations managers | Review trends, performance, service effects, and operational risks. |

### 7.2 Supporting users

| User group | Authorized use |
| --- | --- |
| IT administrators | Maintain approved integrations, access, logging, availability, and configuration. |
| Data or AI personnel | Conduct approved evaluation, monitoring, troubleshooting, and revalidation. |
| Information security personnel | Monitor security events and investigate misuse or compromise. |
| GRC personnel | Assess risk, monitor controls, review evidence, manage exceptions, and report findings. |
| Internal assurance personnel | Test selected controls and review evidence independently. |
| Vendor-support personnel | Provide contractually authorized support using controlled access. |

### 7.3 Unauthorized users

Customers, delivery recipients, drivers, independent couriers, and unrelated PLG personnel may not directly change RouteAssist models, thresholds, configurations, or governance records unless separately authorized for a defined role.

---

## 8. Stakeholders and Affected Parties

People may be affected even when they do not directly use the system.

| Stakeholder or affected party | Relationship to RouteAssist | Potential benefit | Potential adverse effect |
| --- | --- | --- | --- |
| Dispatchers | Direct users | Faster comparison and decision support | Automation bias, alert fatigue, reduced discretion, or accountability confusion |
| Dispatch supervisors | Review and escalation | Better visibility into recommendations and exceptions | Increased review burden or false confidence in system output |
| PLG-employed drivers | Subject to assignments and routes | More efficient scheduling and routing | Unequal workload, impractical routes, or repeated undesirable assignments |
| Independent couriers | Subject to assignment recommendations | Better matching of available work | Unequal opportunity, inaccurate eligibility assumptions, or opaque rejection |
| Warehouse personnel | Coordinate shipment readiness | Better alignment with dispatch timing | Disruption caused by inaccurate schedule recommendations |
| Commercial customers | Receive logistics services | Improved timeliness and visibility | Delay, service inconsistency, or inaccurate exception classification |
| Healthcare clients | Submit medical-delivery requests | Faster and more consistent planning | Inappropriate prioritization or delay of time-sensitive delivery |
| Shipment recipients | Receive deliveries | Improved delivery reliability | Delayed, misrouted, or denied service |
| Customer-service personnel | Respond to inquiries and complaints | Better access to recommendation history | Reliance on inaccurate system explanations |
| PLG leadership | Own business outcomes | Improved performance information | Financial, contractual, regulatory, or reputational harm |
| IT, security, and data teams | Maintain and monitor the system | Centralized visibility and control | Operational burden or incomplete vendor visibility |
| Vendor | Supplies AI or supporting services | Commercial relationship and feedback | Contractual or reputational exposure |
| Regulators and contractual partners | External oversight or obligations | Better documented governance | Concern if documentation, controls, or outcomes are inadequate |

The detailed role, accountability, and RACI analysis will be documented in [`02-stakeholder-and-accountability-map.md`](02-stakeholder-and-accountability-map.md).

---

## 9. Input Information

RouteAssist may use only approved data necessary for the defined use case.

| Data ID | Input category | Illustrative fields | Primary purpose |
| --- | --- | --- | --- |
| `DATA-001` | Order and shipment data | Order ID, service type, size, status, destination, and delivery window | Identify delivery requirements |
| `DATA-002` | Service-level and priority data | Contracted service level, urgency indicator, and approved medical-delivery flag | Support prioritization |
| `DATA-003` | Driver and courier availability | Availability, general location, assigned workload, vehicle type, and approved service eligibility | Support assignment recommendations |
| `DATA-004` | Route and geolocation data | Origin, destination, distance, road restrictions, and estimated travel time | Support route recommendations |
| `DATA-005` | Traffic and environmental data | Traffic conditions, closures, severe weather alerts, and travel disruption | Adjust route and schedule recommendations |
| `DATA-006` | Operational history | Prior travel times, delays, exception categories, and delivery outcomes | Support pattern analysis and evaluation |
| `DATA-007` | Incident and exception data | Delay reason, failed delivery, safety concern, complaint, and resolution | Support exception classification and risk monitoring |
| `DATA-008` | System and human-review records | Recommendation, confidence or uncertainty indicator, decision, override, rationale, user, and timestamp | Support traceability, monitoring, and investigation |

Final data definitions, sources, retention, access, and flows will be documented in [`04-data-flow-and-system-context.md`](04-data-flow-and-system-context.md).

---

## 10. System Outputs

| Output ID | Output | Intended recipient | Permitted downstream action |
| --- | --- | --- | --- |
| `OUT-001` | Recommended delivery priority | Dispatcher or supervisor | Human reviews and records the final priority decision. |
| `OUT-002` | Recommended driver or courier | Dispatcher | Human verifies eligibility, workload, and relevant context before assignment. |
| `OUT-003` | Recommended route | Dispatcher or driver | Human may accept, modify, or reject based on safety and current conditions. |
| `OUT-004` | Estimated timing | Dispatcher or operations personnel | Used for planning; not represented as guaranteed delivery time. |
| `OUT-005` | Suggested exception category | Authorized operations employee | Human validates before the classification is finalized or communicated. |
| `OUT-006` | Schedule-adjustment recommendation | Dispatcher or supervisor | Human assesses effects on all relevant deliveries before approval. |
| `OUT-007` | Escalation flag | Supervisor or designated owner | Human reviews and determines the appropriate response. |
| `OUT-008` | Recommendation rationale or contributing factors | Authorized reviewer | Supports review; does not replace independent judgment. |

System outputs are recommendations, estimates, or flags. They are not guarantees, legal conclusions, clinical decisions, or substitutes for authorized human judgment.

---

## 11. Human Decision Points

| Decision point | Human responsibility | Minimum action |
| --- | --- | --- |
| Routine assignment | Dispatcher | Verify eligibility, availability, delivery requirements, and obvious conflicts before acceptance. |
| Route selection | Dispatcher or driver | Consider current safety, traffic, road, vehicle, and delivery conditions. |
| Medical-delivery prioritization | Authorized dispatcher and, when required, supervisor | Verify the approved service level and relevant operational context before confirming or changing priority. |
| Material schedule change | Dispatcher or supervisor | Review effects on other deliveries, customers, and service commitments. |
| Exception classification | Authorized employee | Confirm that the suggested category accurately represents the event. |
| Repeated or unusual recommendation | Supervisor | Investigate, document, and escalate when defined thresholds are reached. |
| Recommendation override | Authorized reviewer | Record the decision and rationale when required by policy. |
| System suspension | Designated manager or incident authority | Restrict or suspend use when defined safety, security, performance, or risk conditions occur. |
| Return to service | Authorized governance and technical roles | Confirm remediation, testing, residual-risk review, and approval before restoration. |

The detailed oversight design will be maintained in [`10-human-oversight-and-escalation-plan.md`](10-human-oversight-and-escalation-plan.md).

---

## 12. Permitted Uses

Subject to approval and required controls, RouteAssist may be used to:

- Support routine delivery planning.
- Recommend eligible drivers or couriers for authorized delivery types.
- Recommend routes using approved operational inputs.
- Surface potential schedule conflicts or delays.
- Suggest operational exception categories for human validation.
- Identify cases requiring supervisory attention.
- Support approved evaluation, monitoring, audit, and incident investigation.
- Produce aggregate operational and risk metrics using authorized data.

Permitted use does not eliminate the need for human review, documentation, access control, evaluation, or monitoring.

---

## 13. Restricted Uses

Restricted uses require additional review, documented controls, and explicit approval before use.

| Restricted use | Reason for restriction | Required approval or control |
| --- | --- | --- |
| Time-sensitive medical-delivery prioritization | Delay or error may create severe consequences | Documented human review, defined escalation, scenario testing, and supervisor approval rules |
| Recommendations affecting repeated driver or courier workload | May create unequal or harmful distribution | Impact monitoring, workload analysis, dispute process, and management oversight |
| Use of new sensitive data | May increase privacy, security, or legal risk | Data review, purpose justification, access controls, and governance approval |
| Expansion to a new geography or service type | Performance may not generalize | Impact review, representative testing, and reapproval |
| Automated communication of explanations to customers | Explanation may be inaccurate or misleading | Human-approved content, disclosure rules, and monitoring |
| Material vendor, model, data, configuration, or integration change | May invalidate prior evaluation | Change assessment, regression testing, and revalidation |
| Use during emergency or severely degraded operations | Inputs and patterns may differ from evaluated conditions | Defined emergency procedure and heightened human authority |

---

## 14. Prohibited Uses

RouteAssist may not independently or indirectly be used to:

- Make hiring, termination, disciplinary, performance-rating, promotion, or compensation decisions.
- Rank workers for adverse employment action.
- Deny a driver or courier access to work without documented human review and an appropriate dispute process.
- Deny a customer or shipment recipient access to services.
- Make medical, clinical, or patient-care decisions.
- Change or remove the priority of a time-sensitive medical delivery without authorized human review.
- Infer protected or highly sensitive characteristics that are unnecessary for the approved use case.
- Use personal or sensitive data collected for an unrelated purpose without review and authorization.
- Conduct covert employee surveillance or productivity scoring outside approved operational needs.
- Generate final legal, compliance, safety, or risk-acceptance decisions.
- Approve its own model, data, configuration, vendor, or use-case changes.
- Suppress complaints, exceptions, overrides, incidents, or evidence.
- Resume operation after a severe incident without authorized approval.
- Operate outside the approved geography, service type, user population, or system boundary.
- Be represented as error-free, unbiased, safe, compliant, or guaranteed to produce the correct outcome.

Attempts to use RouteAssist for a prohibited purpose must be blocked where feasible, logged, and escalated.

---

## 15. Foreseeable Misuse

Foreseeable misuse includes both intentional abuse and predictable inappropriate reliance.

| Misuse ID | Foreseeable misuse | Potential consequence | Preliminary response |
| --- | --- | --- | --- |
| `FM-001` | Dispatcher accepts every recommendation without review | Automation bias and unmanaged errors | Training, review prompts, sampling, override monitoring, and supervisory review |
| `FM-002` | Manager uses assignment data to evaluate employee performance outside the approved purpose | Unfair employment effect and loss of trust | Purpose limitation, access restriction, policy enforcement, and audit logging |
| `FM-003` | User changes a medical-delivery priority based only on RouteAssist output | Harmful delay or service failure | Mandatory human verification and escalation control |
| `FM-004` | User enters unapproved personal or sensitive data into a free-text field | Privacy or data-exposure risk | Input restrictions, validation, training, and monitoring |
| `FM-005` | Administrator changes thresholds without approval | Invalid evaluation and unsafe recommendations | Role-based access, change control, logging, and revalidation |
| `FM-006` | User treats an estimated delivery time as a guarantee | Misleading customer communication | Clear labels, communication standards, and human review |
| `FM-007` | Attacker manipulates input or integration data | Unsafe route, assignment, or priority output | Security monitoring, input validation, access control, and incident response |
| `FM-008` | PLG expands the system to a new service without reassessment | Unrecognized risks and performance failure | Use-case inventory, material-change trigger, and governance approval |
| `FM-009` | Vendor support accesses PLG information beyond approved need | Confidentiality and contractual exposure | Restricted access, session logging, approval, and vendor oversight |
| `FM-010` | Supervisor pressures reviewers not to override the system | Ineffective human oversight and concealed errors | Non-retaliation expectation, override monitoring, escalation, and assurance review |

These scenarios will inform the risk register, controls, evaluations, monitoring metrics, and incident exercises.

---

## 16. Expected Benefits and Measurement Approach

Benefits are hypotheses until supported by evidence.

| Benefit ID | Expected benefit | Possible measure | Important countermeasure |
| --- | --- | --- | --- |
| `BEN-001` | Faster review of routine delivery options | Median time from complete order to reviewed recommendation | Error, override, and escalation rate |
| `BEN-002` | Improved consistency in routine dispatch decisions | Variation in comparable decision outcomes | Harmful uniformity or repeated bias |
| `BEN-003` | Earlier identification of likely delays | Percentage of material delays flagged within the defined window | False-alert rate and missed-delay rate |
| `BEN-004` | Improved route efficiency | Change in travel time, distance, or on-time performance | Safety events and service failures |
| `BEN-005` | Better documentation of decisions | Percentage of material decisions with complete records | Record accuracy and unauthorized access |
| `BEN-006` | More attention to complex cases | Reviewer time allocated to high-impact exceptions | Review backlog and alert fatigue |
| `BEN-007` | Better visibility into operational patterns | Timeliness and usefulness of aggregate reports | Privacy, inappropriate secondary use, and misleading aggregation |

A benefit will not justify deployment if risk remains unacceptable or required controls are ineffective.

---

## 17. Known Limitations

RouteAssist may be limited by:

- Incomplete, inaccurate, stale, inconsistent, or delayed input data
- Historical data that does not represent future conditions
- Underrepresentation of unusual routes, disruptions, delivery types, or geographic areas
- Limited visibility into real-time road, weather, safety, vehicle, or customer conditions
- Vendor opacity regarding model design, training sources, subcontractors, or validation
- Performance changes after model, data, integration, or configuration updates
- Difficulty communicating uncertainty or the reasons behind a recommendation
- False confidence created by precise-looking scores or estimated times
- Human automation bias, time pressure, confirmation bias, or alert fatigue
- Feedback loops in which prior recommendations influence future training or evaluation data
- Inability to understand informal operational knowledge held by experienced personnel
- Limited ability to measure every possible affected-party impact
- Reliance on third-party mapping, traffic, cloud, identity, or vendor services
- Potential security attacks, manipulated inputs, compromised credentials, or insecure integrations

Limitations must be communicated to users and considered in evaluation, approval, monitoring, and incident response.

---

## 18. Preliminary Impact Considerations

The formal impact screening will be completed in [`03-ai-system-inventory-and-impact-screening.md`](03-ai-system-inventory-and-impact-screening.md). Initial concerns include:

### 18.1 Operational impact

Incorrect recommendations may cause delays, missed delivery windows, increased costs, failed customer commitments, or disruption across connected deliveries.

### 18.2 Safety impact

Unsafe or impractical route recommendations may expose drivers, couriers, recipients, shipments, or the public to harm.

### 18.3 Medical-delivery impact

Improper prioritization or routing of a time-sensitive medical delivery may create severe consequences for healthcare clients or recipients.

### 18.4 Workforce impact

Assignment patterns may affect workload, opportunity, travel burden, compensation, performance perception, or worker trust.

### 18.5 Fairness impact

Historical patterns, location data, operational proxies, or incomplete information may produce materially different outcomes across workers, service areas, customers, or delivery types.

### 18.6 Privacy impact

RouteAssist may process identity, availability, location, delivery, customer, and medical-delivery information. Improper access or secondary use may create privacy harm.

### 18.7 Security impact

Unauthorized access, manipulated inputs, compromised integrations, insecure vendor access, or altered outputs may affect decisions and expose sensitive information.

### 18.8 Reputational and contractual impact

Unexplained delays, repeated errors, harmful outcomes, weak governance, or inadequate vendor response may damage customer trust and contractual relationships.

The presence of potentially significant consequences supports heightened review for defined use cases, especially medical-delivery prioritization and repeated workforce assignment effects.

---

## 19. Preliminary Risk Themes

The following themes will be assessed formally in the AI risk register:

| Theme | Preliminary question |
| --- | --- |
| Accountability | Is a person clearly accountable for the system and each consequential decision? |
| Use limitation | Can the system be prevented from expanding into unapproved purposes? |
| Data suitability | Is the input data accurate, representative, timely, lawful, and appropriate? |
| Performance | Does the system work under the conditions PLG expects to encounter? |
| Reliability | Does performance remain acceptable during unusual or degraded conditions? |
| Fairness and harmful impact | Are effects distributed in ways that create unjustified disadvantage or harm? |
| Human oversight | Can reviewers understand, challenge, reject, override, and escalate recommendations? |
| Privacy | Is personal and sensitive data minimized, protected, and limited to approved purposes? |
| Security | Are users, data, integrations, configurations, outputs, and logs protected? |
| Vendor risk | Can PLG obtain sufficient information, assurance, notification, and exit support? |
| Change management | Do material changes trigger impact review, testing, and reapproval? |
| Monitoring | Can PLG detect drift, degradation, repeated overrides, complaints, or harmful effects? |
| Incident response | Can PLG contain failures, preserve evidence, notify stakeholders, and recover safely? |

---

## 20. Dependency and Integration Assumptions

RouteAssist depends on or may integrate with:

- Logistics and freight brokerage records
- Dispatch and delivery-platform records
- Driver and courier availability information
- Mapping, traffic, and geolocation services
- Customer order and service-level data
- Incident and exception-management records
- Identity and access-management services
- Logging, alerting, and reporting tools
- Vendor-hosted AI infrastructure or APIs

Failure, delay, corruption, compromise, or unauthorized change in an upstream service may affect RouteAssist output. Downstream systems and people must not treat RouteAssist output as trustworthy solely because it was generated successfully.

---

## 21. Transparency and Communication Requirements

Authorized users should be informed that:

- RouteAssist provides recommendations rather than final decisions.
- Outputs may be incomplete, inaccurate, or inappropriate for current conditions.
- Users remain responsible for applying authorized judgment.
- Defined recommendations require supervisory review.
- Users may reject or override a recommendation within their authority.
- Required decisions, overrides, and rationales must be documented.
- Suspected errors, harmful patterns, misuse, security concerns, and incidents must be reported.
- Use outside the approved purpose is prohibited.

PLG should also determine when customers, healthcare clients, workers, couriers, or other affected parties require notice, explanation, complaint, appeal, or escalation mechanisms.

---

## 22. Initial Approval Conditions

RouteAssist should not proceed to a limited pilot until PLG has documented evidence that:

1. The intended use, restricted uses, and prohibited uses are approved.
2. Business, technical, data, risk, security, privacy, and control owners are assigned.
3. The system inventory and impact screening are complete.
4. Data sources, flows, access, retention, and trust boundaries are documented.
5. Material risks have owners and treatment plans.
6. Required governance policies and controls are designed.
7. Human-review, override, escalation, suspension, and recordkeeping procedures are defined.
8. Evaluation scenarios, datasets, metrics, and acceptance thresholds are approved before testing.
9. Required test results meet the approved thresholds or have documented treatment and authorization.
10. Security, privacy, vendor, and contractual reviews are complete.
11. Logging, monitoring, complaint, override, and incident processes are operational.
12. Users and reviewers receive role-appropriate training.
13. Residual risks are documented and accepted by authorized personnel.
14. Pilot scope, duration, users, data, geography, service types, and stop conditions are defined.

Approval may be denied or conditioned even when individual performance metrics are met.

---

## 23. Pilot Boundaries

If approved, an initial pilot should be limited by:

| Boundary | Initial position |
| --- | --- |
| Purpose | Advisory support for approved delivery planning and exception scenarios |
| Users | Trained dispatchers and supervisors with named accounts |
| Geography | Defined operating areas represented in the evaluation data |
| Service types | Routine delivery types that have completed impact and risk review |
| Medical deliveries | Excluded or subject to separately approved heightened controls during initial pilot |
| Data | Approved, minimized, and documented sources only |
| Duration | Time-limited pilot with scheduled review points |
| Decision authority | Human personnel retain final authority |
| Monitoring | Enhanced logging, sampling, overrides, complaints, errors, and threshold reporting |
| Stop conditions | Severe incident, material threshold breach, unsafe behavior, control failure, or unauthorized use |

Final pilot boundaries will depend on the completed risk assessment and evaluation plan.

---

## 24. Success Measures

The use case may be considered successful only when both benefit and risk criteria are satisfied.

Potential success measures include:

- Defined performance thresholds are met across relevant operating conditions.
- High-impact scenarios receive required human review.
- Reviewers can understand, reject, override, and escalate recommendations.
- Override and disagreement patterns are investigated rather than discouraged.
- Material differences across delivery types, geographies, workers, or service conditions remain within approved limits or receive treatment.
- Security, privacy, logging, access, change, and incident controls operate as designed.
- Operational benefits do not create unacceptable safety, workforce, customer, or medical-delivery effects.
- Complaints, incidents, and harmful outcomes remain within approved thresholds and receive timely response.
- Residual risk remains within PLG's approved tolerance.

Detailed metrics and thresholds will be established in [`11-ai-evaluation-and-testing-plan.md`](11-ai-evaluation-and-testing-plan.md) and [`12-monitoring-metrics-and-reporting-plan.md`](12-monitoring-metrics-and-reporting-plan.md).

---

## 25. Conditions Requiring Reassessment

The use case must be reassessed when:

- PLG proposes a new purpose or user group.
- RouteAssist expands to a new geography, customer type, service, or delivery category.
- Medical-delivery or other high-impact use materially changes.
- A new sensitive data category or data source is introduced.
- The model, vendor, algorithm, threshold, configuration, interface, or architecture materially changes.
- A third-party dependency or subcontractor changes.
- Performance or impact monitoring shows material degradation or disparity.
- Override, complaint, incident, or error patterns exceed defined thresholds.
- A severe incident or previously unanticipated harm occurs.
- A material security, privacy, contractual, legal, or policy requirement changes.
- The system is inactive long enough that prior evaluation may no longer represent current conditions.

Reassessment may result in continued use, additional controls, retesting, restricted use, suspension, rollback, or retirement.

---

## 26. Use-Case Decision Record

| Field | Initial decision |
| --- | --- |
| Use-case identifier | `UC-001` |
| AI system | `AI-SYS-001` — PLG RouteAssist |
| Business need | Improve consistency and efficiency of authorized delivery planning and exception management |
| Decision role | Advisory |
| Current lifecycle stage | Proposed / predeployment assessment |
| Preliminary benefit | Potential operational decision support and earlier exception awareness |
| Preliminary impact | Potentially significant due to workforce, customer, location, and time-sensitive delivery effects |
| Initial decision | Proceed to detailed impact screening and risk assessment |
| Production approval | Not granted |
| Required next step | Complete stakeholder mapping, system inventory, impact screening, data-flow mapping, and risk assessment |
| Accountable business owner | Dispatch Director |
| Executive sponsor | Chief Operating Officer |
| Governance oversight | AI Governance Committee |

The decision to continue assessment is not approval to pilot or deploy the system.

---

## 27. Key Questions for Subsequent Deliverables

Later artifacts must answer:

1. Which roles are responsible, accountable, consulted, and informed for each lifecycle activity?
2. Which affected parties may experience benefit or harm?
3. What is RouteAssist's impact tier and required review path?
4. Where does each data category originate, flow, persist, and influence a decision?
5. Which risks are inherent to the use case, and how severe are they?
6. Which controls reduce each risk, and what evidence proves operation?
7. How will human oversight remain meaningful during time-sensitive decisions?
8. Which evaluation metrics and thresholds determine pilot readiness?
9. How will PLG monitor performance, drift, human behavior, complaints, and harmful effects?
10. How will PLG respond when RouteAssist fails, is misused, or is compromised?
11. What vendor information and contractual rights are necessary?
12. Which gaps must be remediated before pilot or production use?

---

## 28. Document Control

| Field | Value |
| --- | --- |
| Document title | Organization Profile and AI Use Case |
| Repository path | `docs/01-organization-profile-and-ai-use-case.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Business owner | Dispatch Director |
| Approver | AI Governance Committee |
| Review frequency | Annually and upon material use-case change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-19 | Tommy Marshall | Initial organization profile and RouteAssist use case established. |

---

## 29. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)

---

## 30. Portfolio Notice

This document is part of an educational portfolio project based on a fictional organization and fictional AI system. It does not contain real PLG, employee, courier, customer, patient, shipment, or delivery information.

It does not provide legal advice, regulatory advice, certification, independent assurance, or a guarantee that any AI system is safe, fair, secure, compliant, reliable, or suitable for production use.
