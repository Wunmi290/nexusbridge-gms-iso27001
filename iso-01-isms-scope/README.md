# ISO-01: ISMS Scope, Context, and Leadership Document

**Project Title:** Information Security Management System (ISMS) Scope, Context, and Leadership Document
**System Reference:** NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD
**Framework / Standard:** ISO 27001:2022, Clauses 4, 5, and 6
**Author:** Omowumi Adisa, ISSO, NexusBridge Technologies
**Date:** May 2024
**Status:** Complete

## Purpose

ISO 27001:2022 Clause 4 requires the organization to understand its internal and external context before establishing an ISMS. Clause 5 requires leadership commitment and the assignment of roles and responsibilities. Clause 6 requires the organization to address risks and opportunities and establish information security objectives.

This document captures all three clauses for NexusBridge Technologies as they apply to the NexusBridge Grant Management System (GMS). This is the foundational document of the NexusBridge ISMS.

## Section 1: Organizational Context (ISO 27001:2022, Clause 4)

### 4.1 Understanding the Organization and Its Context

NexusBridge Technologies is a cloud service provider (CSP) that develops and operates federal grants management software for government agencies. The NexusBridge GMS is its primary federal product, supporting approximately 18,000 researchers across 8 DOE regional offices.

**Internal factors affecting the ISMS:**
- NexusBridge is a mid-size technology company with approximately 220 employees, of which 38 are in engineering and operations roles that interact with GMS.
- The company operates under a FedRAMP Moderate authorization and is subject to DOE agency security requirements.
- The engineering culture prioritizes rapid deployment cycles, which creates a need for strong change management controls to maintain ATO compliance.
- The company has experienced growth of 28% in the past 18 months, increasing the risk of role sprawl and access control gaps.

**External factors affecting the ISMS:**
- NexusBridge operates under FISMA, the FedRAMP Authorization Act (2022), and the Privacy Act of 1974.
- The threat landscape for federal grants systems is active: CISA has issued advisories on targeting of federal financial systems by ransomware operators and nation-state actors.
- AWS GovCloud provides the infrastructure foundation. AWS security posture changes can affect the NexusBridge security architecture.
- The regulatory environment continues to evolve: NIST SP 800-53 Rev 5 introduced significant changes to privacy and supply chain controls that affect NexusBridge's ISMS scope.

### 4.2 Understanding the Needs and Expectations of Interested Parties

| Interested Party | Relationship to NexusBridge GMS | Key Information Security Requirements |
|---|---|---|
| DOE (Sponsoring Agency) | System authorizer and data owner | FedRAMP Moderate compliance, monthly ConMon reporting, FISMA compliance |
| Federal Researchers | System users (indirect) | Confidentiality of grant application data; availability of grant submission services |
| NSF (National Science Foundation) | Data sharing partner via ISA | Secure handling of interagency grant data; ISA compliance |
| Treasury BFS | Payment processing partner via MOU | Integrity of disbursement instructions; secure API connection |
| DOE OIG (Office of Inspector General) | Oversight body | Audit readiness; accurate records and logs |
| NexusBridge Employees | Internal stakeholders | Clear security policies; security awareness training |
| AWS GovCloud | Infrastructure provider | Compliance with FedRAMP High P-ATO; customer responsibility matrix |
| ClearPoint Assurance LLC (3PAO) | Independent assessor | Access to SSP, scan results, and system personnel for assessments |
| DOE Privacy Officer (Helen R. Nguyen) | Privacy oversight | Compliance with Privacy Act and PIA requirements |

### 4.3 Determining the Scope of the ISMS

The scope of the NexusBridge ISMS covers all information assets, processes, and personnel involved in the development, operation, and security monitoring of the NexusBridge Grant Management System (GMS) within the AWS GovCloud (US-West) authorization boundary.

**In scope:**
- All NexusBridge-managed AWS GovCloud resources (EC2, RDS, S3, CloudTrail, CloudWatch, ALB, KMS, Systems Manager)
- All NexusBridge employees and contractors with access to GMS systems or data
- All NexusBridge processes related to security operations, change management, incident response, vulnerability management, and access management for GMS
- All physical locations where NexusBridge employees with GMS access work

**Out of scope:**
- AWS infrastructure layer (covered by AWS FedRAMP High P-ATO)
- DOE internal systems (covered by DOE agency ATO)
- NexusBridge non-GMS product lines

## Section 2: Leadership (ISO 27001:2022, Clause 5)

### 5.1 Leadership and Commitment

Top management at NexusBridge Technologies (represented by Daniel R. Osei, VP Engineering and CSP Representative) demonstrates commitment to the ISMS by approving the ISMS scope, information security policy, and security objectives; ensuring that resources required for the ISMS are available; and communicating the importance of information security compliance to all staff.

### 5.2 Information Security Policy

The NexusBridge Information Security Policy key statements:
- NexusBridge Technologies will protect the confidentiality, integrity, and availability of all federal grant data entrusted to it by DOE.
- All employees and contractors with access to GMS data must comply with the ISMS policies and complete annual security awareness training.
- Information security risks will be assessed annually and whenever significant changes occur.
- NexusBridge will maintain FedRAMP Moderate authorization for the GMS and will comply with all continuous monitoring requirements.

**Policy Owner:** Daniel R. Osei, VP Engineering, NexusBridge Technologies | **Approved:** January 15, 2024 | **Review:** Annually

### 5.3 Organizational Roles, Responsibilities, and Authorities

| Role | Name | ISMS Responsibilities |
|---|---|---|
| Top Management / CSP Rep | Daniel R. Osei | ISMS executive sponsor; approves policy and resources |
| ISSO | Omowumi Adisa | Day-to-day ISMS implementation, risk management, ConMon, AO liaison |
| Cloud Ops Lead | Jerome K. Okafor | Technical implementation of controls; vulnerability remediation |
| Privacy Officer (DOE) | Helen R. Nguyen | Privacy controls; PIA review and approval |
| System Owner (DOE) | Dr. Marcus T. Webb | Business requirements; ATO decisions |
| Authorizing Official (DOE) | Patricia L. Donovan | ATO authorization; risk acceptance |

## Section 3: Planning (ISO 27001:2022, Clause 6)

### 6.1 Actions to Address Risks and Opportunities

The NexusBridge ISMS uses a formal risk assessment and treatment process (documented in ISO-03 and ISO-04) to identify, evaluate, and treat information security risks. Risk assessments are conducted annually and triggered by significant changes. The risk assessment methodology is aligned with ISO 27005:2022.

**Risk criteria:**
- Likelihood scale: 1 (Very Low) to 5 (Very High)
- Impact scale: 1 (Negligible) to 5 (Catastrophic)
- Risk score = Likelihood x Impact (range: 1-25)
- Risk acceptance threshold: Risk scores below 9 are accepted. Scores 9-15 are treated or accepted with documentation. Scores above 15 require mandatory treatment.

### 6.2 Information Security Objectives

| Objective | Measure | Target | Frequency |
|---|---|---|---|
| Maintain FedRAMP Moderate ATO | ATO status | Active ATO at all times | Continuous |
| Close all High-risk POA&M items within 30 days | POA&M tracking | Zero overdue High items | Monthly |
| Complete monthly vulnerability scans | Scan completion rate | 100% on schedule | Monthly |
| Achieve 100% security awareness training completion | Training completion rate | 100% annually | Annual |
| Patch Critical vulnerabilities within 15 days | Mean time to remediate (Critical) | 15 days or less | Monthly |
| Respond to all Moderate+ incidents within 1 hour | Incident response time | 100% within SLA | As needed |

## Interview Defense Notes

**What is the purpose of an ISMS scope document?**
It defines what is inside the ISMS, what the organization is trying to protect, and why. Without a clear scope, you cannot determine which controls apply and which risks need to be assessed.

**What is an interested party in ISO 27001?**
An interested party is any person or organization that has a stake in the security of your information. For NexusBridge, that includes DOE, researchers, NSF, Treasury, and regulators. You need to understand what each interested party requires so your ISMS addresses their expectations.

**How does ISO 27001 relate to FedRAMP for NexusBridge?**
FedRAMP requires a specific set of controls and processes aligned with NIST SP 800-53. ISO 27001 provides a management framework for implementing and improving those controls. Running both in parallel means the risk register, incident response plan, and ConMon activities serve both frameworks simultaneously.

---
*Prepared by: Omowumi Adisa, ISSO, NexusBridge Technologies*
*System: NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD*
*[GitHub Portfolio](https://github.com/Wunmi290)*
