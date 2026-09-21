# AI Model Card Template

## 1. Model Identification

| Field | Response |
| --- | --- |
| Model card ID | `[MC-###]` |
| System ID | `[AI-SYS-###]` |
| Model or service name | `[Name]` |
| Version | `[Version]` |
| Provider | `[Internal team / vendor]` |
| Release date | `[YYYY-MM-DD]` |
| Business owner | `[Role]` |
| Technical owner | `[Role]` |
| Lifecycle status | `[Development / Test / Pilot / Production / Retired]` |

---

## 2. Purpose

- **Intended use:** `[Purpose]`
- **Intended users:** `[Users]`
- **Supported decisions:** `[Decisions]`
- **Operating environment:** `[Environment]`
- **Out-of-scope uses:** `[Uses]`
- **Prohibited uses:** `[Uses]`

---

## 3. Model and System Description

- **Model or technique:** `[Description]`
- **Architecture:** `[High-level architecture]`
- **Inputs:** `[Inputs]`
- **Outputs:** `[Outputs]`
- **Human role:** `[Review and approval]`
- **Dependencies:** `[Services, APIs, and vendors]`
- **Update method:** `[Static / periodically retrained / vendor-managed]`

---

## 4. Data

| Dataset | Purpose | Source | Period | Sensitive data | Known limitations |
| --- | --- | --- | --- | --- | --- |
| `[Dataset ID]` | `[Training / validation / test / operation]` | `[Source]` | `[Period]` | `[Yes / No]` | `[Limitations]` |

---

## 5. Performance

| Metric | Overall result | Slice results | Threshold | Status |
| --- | ---: | --- | ---: | --- |
| `[Metric]` | `[Result]` | `[Slices]` | `[Threshold]` | `[Pass / Fail]` |

---

## 6. Safety Evaluation

- **Safety scenarios tested:** `[Scenarios]`
- **High-impact scenarios tested:** `[Scenarios]`
- **Failure behavior:** `[Behavior]`
- **Stop conditions:** `[Conditions]`
- **Manual fallback:** `[Process]`
- **Unresolved safety concerns:** `[Concerns]`

---

## 7. Fairness and Harmful-Impact Evaluation

- **Relevant groups or slices:** `[Groups]`
- **Outcomes evaluated:** `[Outcomes]`
- **Material differences:** `[Findings]`
- **Legitimate operational factors considered:** `[Factors]`
- **Mitigations:** `[Mitigations]`
- **Remaining uncertainty:** `[Uncertainty]`

---

## 8. Privacy and Security

- **Privacy safeguards:** `[Safeguards]`
- **Data minimization:** `[Approach]`
- **Retention and deletion:** `[Requirements]`
- **Access controls:** `[Controls]`
- **Integration security:** `[Controls]`
- **Security testing:** `[Summary]`
- **Known vulnerabilities or limitations:** `[Limitations]`

---

## 9. Human Oversight

- **Required reviewer:** `[Role]`
- **Information presented:** `[Information]`
- **Available actions:** `[Approve / modify / reject / escalate / stop]`
- **Training requirements:** `[Training]`
- **Human-factor test results:** `[Results]`
- **Override monitoring:** `[Method]`

---

## 10. Known Limitations

| Limitation | Affected context | Potential impact | Mitigation |
| --- | --- | --- | --- |
| `[Limitation]` | `[Context]` | `[Impact]` | `[Mitigation]` |

---

## 11. Monitoring and Change

- **Production metrics:** `[Metrics]`
- **Drift indicators:** `[Indicators]`
- **Alert thresholds:** `[Thresholds]`
- **Material-change triggers:** `[Triggers]`
- **Rollback method:** `[Method]`
- **Retirement criteria:** `[Criteria]`

---

## 12. Approval

| Field | Response |
| --- | --- |
| Evaluation result | `[Pass / Conditional / Fail]` |
| Approved scope | `[Scope]` |
| Conditions | `[Conditions]` |
| Residual risks | `[AIR-###]` |
| Approver | `[Role]` |
| Approval date | `[YYYY-MM-DD]` |
| Expiration or review date | `[YYYY-MM-DD]` |

---

## 13. Document Control

**Repository path:** `templates/ai-model-card-template.md`  
**Template version:** 1.0
