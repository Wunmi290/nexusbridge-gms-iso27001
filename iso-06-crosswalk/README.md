# ISO-06: FedRAMP/NIST RMF vs. ISO 27001:2022 Framework Crosswalk

**Project Title:** FedRAMP/NIST RMF to ISO 27001:2022 Framework Crosswalk for NexusBridge GMS
**System Reference:** NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD
**Framework / Standard:** NIST SP 800-53 Rev 5 | ISO 27001:2022 | FedRAMP Moderate Baseline
**Author:** Omowumi Adisa, ISSO, NexusBridge Technologies
**Date:** May 2024
**Status:** Complete

## Purpose

NexusBridge GMS operates under a FedRAMP Moderate ATO and simultaneously maintains an ISO 27001:2022 ISMS. These two frameworks have significant overlap. Understanding the crosswalk between them helps the organization avoid duplicating effort, identify gaps that one framework covers but the other does not, and communicate security posture using either framework's language.

This crosswalk maps representative NIST SP 800-53 Rev 5 control families to their ISO 27001:2022 Annex A counterparts and maps ISO 27001:2022 ISMS clauses to the corresponding FedRAMP/RMF process steps.

## Section 1: NIST SP 800-53 Control Families to ISO 27001:2022 Annex A Controls

| NIST SP 800-53 Control Family | Key Controls | ISO 27001:2022 Annex A Mapping | Notes |
|---|---|---|---|
| Access Control (AC) | AC-1 through AC-25 | 5.15, 5.16, 5.17, 5.18, 8.2, 8.3, 8.5 | Strong alignment; both require RBAC, MFA, and access reviews |
| Audit and Accountability (AU) | AU-1 through AU-16 | 8.15, 8.16, 8.17 | NIST is more prescriptive on log content and retention; ISO focuses on monitoring |
| Configuration Management (CM) | CM-1 through CM-14 | 5.9, 8.9, 8.19 | NIST CM maps well to ISO asset management and configuration controls |
| Contingency Planning (CP) | CP-1 through CP-13 | 5.29, 5.30, 8.13, 8.14 | NIST CP is very detailed; ISO covers BCP/BCM at a higher level |
| Identification and Authentication (IA) | IA-1 through IA-13 | 5.16, 5.17, 8.5 | Near-identical requirements for identity management and authentication |
| Incident Response (IR) | IR-1 through IR-10 | 5.24, 5.25, 5.26, 5.27, 5.28 | Strong alignment; both require planning, detection, response, and post-incident review |
| Risk Assessment (RA) | RA-1 through RA-9 | 6.1.2, ISO 27005:2022 (entire standard) | NIST RA maps to ISO 27001 Clause 6 and ISO 27005 methodology |
| System and Communications Protection (SC) | SC-1 through SC-51 | 8.20, 8.21, 8.22, 8.24, 8.6 | Significant alignment; NIST SC is more technical and prescriptive |
| System and Information Integrity (SI) | SI-1 through SI-23 | 8.7, 8.8, 8.12 | SI-2 (patching) maps to 8.8; SI-3 (malware) maps to 8.7 |
| Personnel Security (PS) | PS-1 through PS-9 | 6.1, 6.2, 6.4, 6.5, 6.6 | Strong alignment; both require screening, training, and termination procedures |
| Physical and Environmental (PE) | PE-1 through PE-23 | 7.1 through 7.14 | Strong alignment; PE controls map directly to ISO Theme 7 Physical Controls |
| Supply Chain Risk Management (SR) | SR-1 through SR-12 | 5.19, 5.20, 5.21, 5.22 | New ISO 27001:2022 controls on cloud and supply chain mirror NIST SCRM additions |

## Section 2: NIST RMF Steps to ISO 27001:2022 ISMS Process Mapping

| NIST RMF Step | Description | ISO 27001:2022 Equivalent | Notes |
|---|---|---|---|
| Step 0: Prepare | Organizational-level preparation; context, roles, risk strategy | Clauses 4, 5, 6.1 | ISO context-setting and leadership clauses align with RMF preparation |
| Step 1: Categorize | FIPS 199 categorization; identify information types | Clause 4.3 (scope), Clause 8.1 (operational planning) | ISO does not have a formal categorization step; asset classification (5.12) is the closest |
| Step 2: Select | Choose controls from NIST SP 800-53B baseline; tailor | Clause 6.1.3 (SoA); risk treatment control selection | The SoA in ISO and the CRM in FedRAMP serve similar purposes |
| Step 3: Implement | Document control implementations in SSP | Clause 8.1 (Operational Planning and Control); Annex A controls | SSP = ISMS operational documentation + control implementation evidence |
| Step 4: Assess | 3PAO conducts SAP and SAR | Clause 9.2 (Internal Audit); external certification audit | FedRAMP uses 3PAO; ISO uses certification body. Both require independent assessment |
| Step 5: Authorize | AO makes risk-based authorization decision | Clause 9.3 (Management Review) | ATO decision (NIST) and management review (ISO) both involve leadership risk acceptance |
| Step 6: Monitor | Continuous monitoring; ConMon; POA&M | Clause 9.1 (Monitoring and Measurement); Clause 10 (Improvement) | Continuous monitoring in FedRAMP maps directly to Clause 9 performance evaluation |

## Section 3: Key Differences Between FedRAMP/NIST and ISO 27001

| Dimension | FedRAMP / NIST | ISO 27001:2022 |
|---|---|---|
| Mandatory or Voluntary | Mandatory for U.S. federal cloud systems | Voluntary (except where contractually required); international certification |
| Control Prescriptiveness | Very prescriptive: 325+ specific controls with detailed requirements | Principles-based: 93 controls at a high level; organization defines implementation |
| Third-Party Assessment | Required: must use an accredited 3PAO | Optional for internal ISMS; required only for certification |
| Authorization / Certification | ATO granted by federal AO | ISO 27001 certification granted by accredited certification body (e.g., BSI, DNV) |
| Privacy Controls | Separate privacy overlay (NIST SP 800-53B Privacy) | Covered in Annex A 5.34 at a general level |
| Risk Methodology | NIST SP 800-30 | ISO 27005:2022 |
| Documentation Output | SSP, SAP, SAR, POA&M, ConMon reports | ISMS documentation (policies, risk register, SoA, audit records) |
| Scope | System-specific (one ATO per system) | Organization-wide or defined ISMS scope |
| Continuous Monitoring | Formal FedRAMP ConMon requirements with monthly deliverables | No formal equivalent; Clause 9.1 requires defined monitoring activities |

## Section 4: Dual-Framework Efficiency for NexusBridge GMS

Because NexusBridge GMS operates under both FedRAMP and an ISO 27001 ISMS, several artifacts serve both frameworks simultaneously:

| Artifact | FedRAMP Use | ISO 27001 Use |
|---|---|---|
| Risk Register | Informs RA-3 risk assessment | Fulfills Clause 6.1.2 risk assessment |
| Incident Response Plan | Fulfills IR control family | Fulfills Clauses 5.24-5.28 |
| Monthly ConMon Report | Required FedRAMP deliverable | Evidence for Clause 9.1 monitoring |
| Access Review Records | Evidence for AC-2, IA-5 | Evidence for 5.15, 5.18 |
| Vulnerability Scan Reports | Required for RA-5; ConMon | Evidence for 8.8 |
| Business Continuity Plan | Fulfills CP family controls | Fulfills 5.29, 5.30 |
| Security Awareness Training Records | Fulfills AT-2 | Fulfills 6.3 |
| Vendor/Supplier Agreements | Fulfills SA-9, SR controls | Fulfills 5.19, 5.20 |

By maintaining both frameworks, NexusBridge GMS avoids creating duplicate documentation for overlapping requirements and instead maintains a single set of controls and evidence that satisfies both.

## Interview Defense Notes

**Why would a federal system running FedRAMP also use ISO 27001?**
ISO 27001 provides a management framework that complements FedRAMP. FedRAMP tells you what controls to implement. ISO 27001 tells you how to build and maintain the management system around those controls, including context analysis, leadership engagement, and continual improvement. Together, they produce a more mature security program.

**What is the most important difference between FedRAMP and ISO 27001?**
FedRAMP is mandatory for federal cloud systems and prescribes specific controls in a specific format. ISO 27001 is voluntary, principles-based, and internationally recognized. FedRAMP focuses on a specific system; ISO 27001 covers the whole organization's ISMS.

**How does the SoA in ISO 27001 compare to the CRM in FedRAMP?**
Both documents map controls to responsibility. The SoA states whether each ISO Annex A control is applicable and why. The CRM states whether each FedRAMP control is inherited, shared, or customer-responsible. Both serve as the organization's formal declaration of control scope.

**What is the benefit of doing a crosswalk between NIST SP 800-53 and ISO 27001?**
It prevents duplicated effort. If you already have a NIST-compliant implementation for AC-2 (account management), you can demonstrate that you have also addressed ISO 27001 controls 5.15, 5.16, and 5.18 without building separate documentation.

---
*Prepared by: Omowumi Adisa, ISSO, NexusBridge Technologies*
*System: NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD*
*[GitHub Portfolio](https://github.com/Wunmi290)*
