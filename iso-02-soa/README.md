# ISO-02: Statement of Applicability (SoA)

**Project Title:** ISO 27001:2022 Statement of Applicability for NexusBridge Grant Management System
**System Reference:** NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD
**Framework / Standard:** ISO 27001:2022 Annex A (all 93 controls across 4 themes)
**Author:** Omowumi Adisa, ISSO, NexusBridge Technologies
**Date:** May 2024
**Status:** Complete

## Purpose

The Statement of Applicability (SoA) is a mandatory deliverable required by ISO 27001:2022 Clause 6.1.3. It documents each Annex A control, states whether it is applicable to the organization, documents the justification for inclusion or exclusion, and indicates the current implementation status.

The SoA is one of the most important documents in an ISO 27001 ISMS. It demonstrates that the organization has thoughtfully considered all 93 controls rather than blindly applying all of them or arbitrarily excluding them.

## SoA Summary

| Theme | Controls in Theme | Applicable | Not Applicable |
|---|---|---|---|
| 5. Organizational Controls | 37 | 35 | 2 |
| 6. People Controls | 8 | 8 | 0 |
| 7. Physical Controls | 14 | 8 | 6 |
| 8. Technological Controls | 34 | 32 | 2 |
| **Total** | **93** | **83** | **10** |

## Theme 5: Organizational Controls (37 Controls) — Representative Sample

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 5.1 | Policies for information security | Yes | Core ISMS requirement; NexusBridge InfoSec Policy approved Jan 2024 | Implemented |
| 5.2 | Information security roles and responsibilities | Yes | Roles assigned in SSP and ISMS scope document | Implemented |
| 5.3 | Segregation of duties | Yes | IAM roles separate developer, ops, and admin functions | Implemented |
| 5.7 | Threat intelligence | Yes | CISA alerts reviewed weekly; integrated into risk register | Implemented |
| 5.9 | Inventory of information and other associated assets | Yes | ServiceNow CMDB maintained; asset inventory reviewed monthly | Implemented |
| 5.12 | Classification of information | Yes | Data classification policy: Grant Data/PII (Sensitive), operational (Internal), public | Implemented |
| 5.15 | Access control | Yes | RBAC enforced via AWS IAM; quarterly access reviews | Implemented |
| 5.16 | Identity management | Yes | DOE IdP via SAML 2.0; hardware MFA for privileged users | Implemented |
| 5.19 | Information security in supplier relationships | Yes | AWS contract includes security requirements; vendor risk register | Implemented |
| 5.23 | Information security for use of cloud services | Yes | AWS GovCloud selected specifically for federal compliance | Implemented |
| 5.24 | Information security incident management planning and preparation | Yes | Incident Response Plan v2.1 approved | Implemented |
| 5.26 | Response to information security incidents | Yes | IRP includes containment, eradication, and recovery steps | Implemented |
| 5.29 | Information security during disruption | Yes | Business Continuity Plan and BCP tested annually | Implemented |
| 5.31 | Legal, statutory, regulatory and contractual requirements | Yes | FISMA, FedRAMP, Privacy Act compliance requirements mapped | Implemented |
| 5.34 | Privacy and protection of PII | Yes | PIA completed; DOE Privacy Officer oversight | Implemented |
| 5.35 | Independent review of information security | Yes | Annual 3PAO assessment; internal audit conducted | Implemented |
| 5.37 | Documented operating procedures | Yes | Runbooks and SOPs maintained in Confluence | Implemented |

## Theme 6: People Controls (8 Controls)

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 6.1 | Screening | Yes | Background checks for all staff with GMS access | Implemented |
| 6.2 | Terms and conditions of employment | Yes | Security responsibilities in employment agreements | Implemented |
| 6.3 | Information security awareness, education and training | Yes | Annual security awareness training; 100% completion tracked | Implemented |
| 6.4 | Disciplinary process | Yes | HR disciplinary policy covers security policy violations | Implemented |
| 6.5 | Responsibilities after termination or change of employment | Yes | Access revoked within 4 hours of departure notification | Implemented |
| 6.6 | Confidentiality or non-disclosure agreements | Yes | NDAs signed by all employees and contractors | Implemented |
| 6.7 | Remote working | Yes | Remote work security policy; VPN and MFA required | Implemented |
| 6.8 | Information security event reporting | Yes | SIEM alerts and incident reporting procedures in place | Implemented |

## Theme 7: Physical Controls (14 Controls)

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 7.1 | Physical security perimeters | Partially | AWS manages data center perimeters; NexusBridge office has badge access | Inherited/Implemented |
| 7.3 | Securing offices, rooms and facilities | Yes | NexusBridge office: badge access for secure areas | Implemented |
| 7.5 | Protecting against physical and environmental threats | No | Not applicable: NexusBridge runs no on-premises infrastructure | N/A |
| 7.7 | Clear desk and clear screen | Yes | Clean desk policy; screen lock after 5 minutes | Implemented |
| 7.8 | Equipment siting and protection | No | No on-premises servers; not applicable to cloud-only environment | N/A |
| 7.9 | Security of assets off-premises | Yes | Laptop security policy for remote work | Implemented |
| 7.10 | Storage media | No | No physical media in use for GMS; all data in AWS S3/RDS | N/A |
| 7.11 | Supporting utilities | No | AWS manages power/cooling for all computing; not applicable | N/A |
| 7.12 | Cabling security | No | No on-premises cabling for GMS infrastructure | N/A |
| 7.13 | Equipment maintenance | Partially | AWS handles hardware maintenance; NexusBridge manages laptops | Partial |
| 7.14 | Secure disposal or re-use of equipment | Yes | Laptop disposal policy; certified erasure required | Implemented |

## Theme 8: Technological Controls (34 Controls) — Representative Sample

| Control ID | Control Name | Applicable | Justification / Notes | Status |
|---|---|---|---|---|
| 8.1 | User endpoint devices | Yes | Endpoint protection on all NexusBridge laptops; MDM enrolled | Implemented |
| 8.2 | Privileged access rights | Yes | Privileged access restricted to named individuals with MFA and session logging | Implemented |
| 8.3 | Information access restriction | Yes | RBAC enforced; data access limited by role and need-to-know | Implemented |
| 8.5 | Secure authentication | Yes | MFA enforced for all users; PIV or Okta Verify | Implemented |
| 8.7 | Protection against malware | Yes | AWS GuardDuty; endpoint EDR on NexusBridge laptops | Implemented |
| 8.8 | Management of technical vulnerabilities | Yes | Monthly Nessus scans; patch SLAs enforced | Implemented |
| 8.9 | Configuration management | Yes | CIS Benchmarks; ServiceNow CMDB; AWS Config rules | Implemented |
| 8.12 | Data leakage prevention | Yes | AWS Macie monitors S3 for sensitive data exposure | Implemented |
| 8.13 | Information backup | Yes | RDS automated daily backups; S3 versioning; restore tested quarterly | Implemented |
| 8.15 | Logging | Yes | CloudTrail; CloudWatch; SIEM integration | Implemented |
| 8.16 | Monitoring activities | Yes | SIEM alerts; weekly log review by ISSO | Implemented |
| 8.20 | Networks security | Yes | VPC with subnets; NACLs; security groups; WAF on ALB | Implemented |
| 8.24 | Use of cryptography | Yes | TLS 1.2+; AES-256 at rest; KMS key rotation; HMAC signing for API | Implemented |
| 8.25 | Secure development lifecycle | Yes | SAST integrated in CI/CD pipeline; PR security reviews | Implemented |
| 8.28 | Secure coding | Yes | OWASP Top 10 training required; secure code review checklist | Implemented |
| 8.30 | Outsourced development | No | No software development outsourced outside NexusBridge | N/A |
| 8.31 | Separation of development, test and production environments | Yes | Separate AWS accounts for dev, staging, and production | Implemented |
| 8.32 | Change management | Yes | CAB approves all changes; change freeze periods enforced | Implemented |

## Interview Defense Notes

**What is a Statement of Applicability and why is it required?**
The SoA is a required ISO 27001 document that lists all 93 Annex A controls, states whether each one is applicable, and justifies the inclusion or exclusion. It is required because ISO 27001 does not require every control in every context. The SoA is the organization's formal declaration of what controls it needs and why.

**Can you exclude controls from the SoA?**
Yes, but you must justify every exclusion. You cannot exclude a control just because it is difficult to implement. Exclusions are appropriate when a control is genuinely not relevant to the context. For NexusBridge, physical infrastructure controls like 7.8 and 7.10 are excluded because all infrastructure is in AWS GovCloud with no on-premises components.

**What is the difference between the 2013 and 2022 versions of ISO 27001 Annex A?**
ISO 27001:2013 had 114 controls organized in 14 domains. ISO 27001:2022 reorganized to 93 controls in 4 themes: Organizational, People, Physical, and Technological. Several controls were merged and 11 new controls were added, including controls for threat intelligence, cloud services, and data masking.

---
*Prepared by: Omowumi Adisa, ISSO, NexusBridge Technologies*
*System: NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD*
*[GitHub Portfolio](https://github.com/Wunmi290)*
