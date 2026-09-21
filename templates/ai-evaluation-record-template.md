# AI Evaluation Record Template

## 1. Test Identification

| Field | Response |
| --- | --- |
| Test run ID | `[TEST-RUN-###]` |
| Test ID | `[TST-###]` |
| System and use-case IDs | `[AI-SYS-### / UC-###]` |
| Test objective | `[Objective]` |
| Risks and controls | `[AIR-### / AIC-###]` |
| Tester | `[Name / role]` |
| Independent reviewer | `[Name / role]` |
| Test date | `[YYYY-MM-DD]` |

---

## 2. Test Configuration

| Item | Version or description |
| --- | --- |
| Environment | `[Development / Test / Simulation / Pilot]` |
| Model or service | `[Version]` |
| Configuration | `[Version]` |
| Dataset | `[Dataset ID and version]` |
| Scenario set | `[Scenario version]` |
| Tools | `[Tools]` |

---

## 3. Test Method

- **Procedure:** `[Numbered test steps]`
- **Population:** `[Population]`
- **Sample:** `[Size and selection method]`
- **Metric:** `[Metric and formula]`
- **Acceptance criterion:** `[Preapproved threshold]`
- **Known limitations:** `[Limitations]`

---

## 4. Test Results

| Metric or scenario | Expected | Actual | Pass / Fail | Evidence reference |
| --- | --- | --- | --- | --- |
| `[Item]` | `[Expected]` | `[Actual]` | `[Result]` | `[Evidence ID]` |

---

## 5. Slice Analysis

| Slice | Sample size | Result | Difference | Explanation |
| --- | ---: | ---: | ---: | --- |
| `[Slice]` | `[n]` | `[Result]` | `[Difference]` | `[Explanation]` |

---

## 6. Human-Factor Results

| Measure | Result | Threshold | Status |
| --- | ---: | ---: | --- |
| Correct-challenge rate | `[Result]` | `[Threshold]` | `[Pass / Fail]` |
| Escalation accuracy | `[Result]` | `[Threshold]` | `[Pass / Fail]` |
| Documentation completeness | `[Result]` | `[Threshold]` | `[Pass / Fail]` |
| Average review time | `[Result]` | `[Threshold]` | `[Pass / Fail]` |

---

## 7. Defects

| Defect ID | Description | Severity | Risks affected | Owner | Due date | Retest required |
| --- | --- | --- | --- | --- | --- | --- |
| `[DEF-###]` | `[Description]` | `[Critical / High / Moderate / Low]` | `[AIR-###]` | `[Owner]` | `[Date]` | `[Yes / No]` |

---

## 8. Conclusion

- **Overall result:** `[Pass / Conditional pass / Fail / Inconclusive]`
- **Uncertainty:** `[Describe remaining uncertainty.]`
- **Required corrective action:** `[Action]`
- **Recommended decision:** `[Approve / Restrict / Retest / Reject]`
- **Reviewer sign-off:** `[Name / date]`
- **Approver:** `[Name / role / date]`

---

## 9. Document Control

**Repository path:** `templates/ai-evaluation-record-template.md`  
**Template version:** 1.0
