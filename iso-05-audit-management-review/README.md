# ISO-05: Internal Audit Checklist and Management Review Template

**Project Title:** Internal Audit Checklist and Management Review Template for NexusBridge GMS ISMS
**System Reference:** NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD
**Framework / Standard:** ISO 27001:2022 Clauses 9.2 (Internal Audit) and 9.3 (Management Review)
**Author:** Omowumi Adisa, ISSO, NexusBridge Technologies
**Date:** May 2024
**Status:** Complete

## Purpose

ISO 27001:2022 Clause 9 covers Performance Evaluation. Two of its most important requirements are the internal audit (Clause 9.2) and the management review (Clause 9.3). The internal audit verifies ISMS effectiveness. The management review is a formal meeting where top management reviews the ISMS outputs and makes decisions about improvements.

## PART A: INTERNAL AUDIT CHECKLIST

### Audit Overview

| Field | Detail |
|---|---|
| Audit Scope | NexusBridge GMS ISMS, all clauses of ISO 27001:2022 |
| Audit Period | Q2 2024 (April-June) |
| Lead Auditor | Omowumi Adisa, ISSO (Internal Auditor) |
| Supporting Auditor | Gerald F. Muñoz, DOE SAISO (Independent Reviewer) |
| Audit Dates | June 2-6, 2024 |
| Audit Report Date | June 13, 2024 |

### Clause 4: Context of the Organization

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 4.1 | Is the internal and external context documented and current? | ISMS Scope document (ISO-01), last updated April 2024 | Current and complete | Conformant |
| 4.2 | Are interested parties and their requirements documented? | ISO-01 interested parties table | 9 interested parties documented with requirements | Conformant |
| 4.3 | Is the ISMS scope clearly defined with justified inclusions and exclusions? | ISO-01 scope section | Scope covers AWS GovCloud boundary and NexusBridge employees | Conformant |
| 4.4 | Is the ISMS established, implemented, and maintained? | SSP, risk register, policies | ISMS artifacts current and reviewed within 12 months | Conformant |

### Clause 5: Leadership

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 5.1 | Is there evidence of top management commitment? | Signed InfoSec Policy (Jan 2024); CAB meeting minutes | Policy signed by VP Engineering; management participates in CAB | Conformant |
| 5.2 | Is the information security policy documented and communicated? | InfoSec Policy v1.2; staff acknowledgment records | Policy distributed; 96% of staff have acknowledged | Minor Finding (4 new hires have not yet acknowledged) |
| 5.3 | Are ISMS roles and responsibilities assigned? | ISMS roles table in ISO-01; SSP roles | Roles assigned with names for all key positions | Conformant |

### Clause 6: Planning

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 6.1 | Is a risk assessment process defined and applied? | Risk register (ISO-03); methodology documentation | 12 risks assessed; methodology documented | Conformant |
| 6.2 | Are information security objectives defined, measurable, and tracked? | ISO-01 objectives table; monthly ConMon reports | 6 measurable objectives with targets; 5 of 6 on track | Conformant |
| 6.1.3 | Is a Statement of Applicability produced and current? | SoA (ISO-02) | All 93 controls addressed; 10 exclusions with documented justifications | Conformant |

### Clause 7: Support

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 7.2 | Is documented evidence of staff competence maintained? | Training records; certification records | Annual security training 96% complete; ISSO maintains certifications | Minor Finding (4 users overdue for training) |
| 7.3 | Are staff aware of the information security policy and their responsibilities? | Policy acknowledgment records; training completion records | 96% acknowledgment rate | Minor Finding (same 4 users as above) |
| 7.5 | Is documented information controlled and maintained? | Document control log; version history in Confluence | Version control applied; document reviews documented | Conformant |

### Clause 8: Operation

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 8.1 | Are operational plans and controls in place? | SSP; runbooks; ConMon plan | Documented and operational | Conformant |
| 8.2 | Are risk assessments conducted at planned intervals or when changes occur? | Risk register dated April 2024; change log | Annual assessment completed; no significant changes without risk review | Conformant |
| 8.3 | Are risk treatment plans being implemented? | Risk treatment plan (ISO-04); POA&M | Treatment actions underway; timelines tracked | Conformant |

### Clause 9: Performance Evaluation

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 9.1 | Are monitoring and measurement processes defined? | ConMon plan; monthly reports | Monthly monitoring activities documented and executed | Conformant |
| 9.3 | Was a management review conducted? | Management review minutes (see Part B) | Q1 2024 review completed April 5, 2024 | Conformant |

### Clause 10: Improvement

| # | Audit Question | Evidence Reviewed | Finding | Status |
|---|---|---|---|---|
| 10.1 | Are nonconformities documented and corrective actions tracked? | Audit finding tracker; POA&M | 2 minor findings from prior quarter; both closed | Conformant |
| 10.2 | Is the ISMS continually improved based on audit results and reviews? | Risk treatment plan updates; policy revisions | Risk treatment plan updated post-assessment | Conformant |

### Audit Summary

| Finding Type | Count |
|---|---|
| Conformant | 20 |
| Minor Finding | 2 |
| Major Nonconformity | 0 |

**Minor Findings:**
- **MF-001:** 4 staff members have not acknowledged the information security policy (Clause 5.2). **Corrective Action:** ISSO to send reminders; confirm acknowledgment within 30 days.
- **MF-002:** 4 staff members are overdue for annual security awareness training (Clause 7.2/7.3). **Corrective Action:** Tracked in POA-013; completion confirmed August 11, 2024.

## PART B: MANAGEMENT REVIEW TEMPLATE (Q2 2024)

**Management Review Meeting:** NexusBridge GMS ISMS
**Date:** July 7, 2024
**Location:** NexusBridge Technologies HQ, Conference Room A (virtual participation for DOE attendees)

### Attendees

| Name | Role | Organization |
|---|---|---|
| Daniel R. Osei | VP Engineering / CSP Representative | NexusBridge Technologies |
| Omowumi Adisa | ISSO | NexusBridge Technologies |
| Jerome K. Okafor | Cloud Ops Lead | NexusBridge Technologies |
| Dr. Marcus T. Webb | System Owner | DOE, Research Programs |
| Gerald F. Muñoz | SAISO | DOE CISO Office |

### Review Agenda and Minutes

**1. Status of Actions from Previous Management Review (Q1 2024)**

- Action 1: Complete FedRAMP RAR remediation actions. **Status:** Completed. All High-priority RAR findings closed by April 30, 2024.
- Action 2: Expand vulnerability scanning to cover all API endpoints. **Status:** Completed (POA-004 closed).
- Action 3: Execute ISA with NSF. **Status:** Completed June 28, 2024.

**2. Information Security Performance Feedback**

- ATO maintained: Yes. ATO granted July 21, 2024.
- High-risk POA&M items closed within 30 days: Yes. POA-001 and POA-002 closed July 31, 2024.
- Monthly scans on schedule: Yes. 100% completion rate.
- Security awareness training: 96% as of review date (4 users in progress).
- Critical patch SLA: 100% compliance. No Critical vulnerabilities past 15 days.
- Incident response SLA: No Moderate+ incidents in period; 1 Low event handled appropriately.

**3. Risk Assessment Results**

ISSO presented the updated risk register (ISO-03). No new risks above the acceptance threshold were identified. RISK-001 and RISK-005 treatment plans are underway and on schedule. No residual risk exceeds 10.

**4. Management Decisions and Resource Allocations**

Daniel R. Osei approved:
- Allocation of 60 additional engineering hours for RISK-001 treatment (UEBA, JIT access) in Q3 2024.
- Procurement of Amazon Inspector Standard tier ($160/month).
- Automation of policy acknowledgment tracking in LMS by Q4 2024.

**5. Next Review Date**

Next management review scheduled: October 6, 2024.

## Interview Defense Notes

**What is the purpose of an internal audit in ISO 27001?**
The internal audit verifies that the ISMS is implemented as intended and conforms to the organization's own requirements and to ISO 27001. It is not a third-party certification audit. It is an internal health check that identifies nonconformities before they become bigger problems.

**What is the difference between a minor finding and a major nonconformity?**
A minor finding means a requirement is partially met or has an isolated gap. A major nonconformity means a requirement is systematically not met or absent, which would prevent certification.

**Why is management review a required part of ISO 27001?**
Because an ISMS requires leadership engagement to work. If management never reviews security performance, they cannot allocate resources, make decisions, or set direction. ISO 27001 mandates the review as an accountability mechanism.

---
*Prepared by: Omowumi Adisa, ISSO, NexusBridge Technologies*
*System: NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD*
*[GitHub Portfolio](https://github.com/Wunmi290)*
