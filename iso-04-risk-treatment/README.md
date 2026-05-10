# ISO-04: Risk Treatment Plan

**Project Title:** Information Security Risk Treatment Plan for NexusBridge Grant Management System
**System Reference:** NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD
**Framework / Standard:** ISO 27005:2022 | ISO 27001:2022 Clause 6.1.3
**Author:** Omowumi Adisa, ISSO, NexusBridge Technologies
**Date:** May 2024
**Status:** Complete (Top 5 risks treated)

## Purpose

ISO 27001:2022 Clause 6.1.3 requires the organization to select and document risk treatment options for information security risks. ISO 27005:2022 identifies four treatment options: Modify (implement controls to reduce likelihood or impact), Retain (accept the risk within the defined threshold), Avoid (eliminate the activity that creates the risk), and Share (transfer the risk to a third party such as an insurer).

This Risk Treatment Plan documents the treatment approach for the five highest-residual risks identified in the NexusBridge GMS Risk Register (ISO-03).

## Treatment Decision Matrix

| Risk ID | Risk Title | Residual Score | Treatment Option | Justification |
|---|---|---|---|---|
| RISK-001 | Unauthorized access to grant data via compromised credentials | 10 (Moderate) | Modify | Residual risk exceeds acceptance threshold; additional technical controls feasible |
| RISK-002 | Ransomware encryption of production data | 8 (Low-Mod) | Accept with monitoring | Strong controls in place; cost of further reduction disproportionate to residual risk |
| RISK-003 | Exploitation of unpatched vulnerability in EC2 AMI | 8 (Low-Mod) | Modify + Accept | Automated patching improvements feasible; residual risk acceptable after improvement |
| RISK-004 | Integrity failure in Treasury disbursement API | 5 (Low) | Accept | Controls are strong; residual risk within threshold |
| RISK-005 | Unauthorized data exfiltration by malicious insider | 8 (Low-Mod) | Modify + Accept | UEBA enhancement feasible; risk not fully accepted without improvement |

## Risk Treatment Detail

### RISK-001: Unauthorized Access to Grant Data via Compromised Credentials

**Current Residual Score:** 10 (Moderate) | **Target Residual Score:** 6 (Low)
**Treatment Option:** Modify

**Current Controls:** MFA via DOE IdP; RBAC; quarterly access reviews; SIEM alerts on failed logins.

**Additional Controls to Implement:**

| Control | Description | ISO 27001 Reference | Owner | Target Date |
|---|---|---|---|---|
| Implement UEBA | Configure SIEM Splunk to baseline normal user behavior and alert on anomalies: logins from new geographies, off-hours access, bulk data queries | ISO Annex A 8.16 (Monitoring Activities) | Jerome K. Okafor, Cloud Ops | August 30, 2024 |
| Implement privileged access workstations (PAWs) | Require all admin access to occur from a dedicated, hardened device | ISO Annex A 8.2 (Privileged Access Rights) | Jerome K. Okafor, Cloud Ops | September 30, 2024 |
| Reduce MFA session duration for privileged accounts | Reduce re-authentication interval from 8 hours to 1 hour for admin accounts | ISO Annex A 8.5 (Secure Authentication) | Jerome K. Okafor, Cloud Ops | August 15, 2024 |
| Implement just-in-time (JIT) privileged access | Replace standing privileged access with JIT access via AWS Systems Manager | ISO Annex A 5.18 (Access Rights) | Jerome K. Okafor, Cloud Ops | October 31, 2024 |

**Resource Estimate:** 80 hours engineering time; existing Splunk license covers UEBA functionality.

**Success Criteria:** Post-implementation residual risk score of 6 or below; UEBA alerts tested and tuned within 30 days of deployment.

**Risk Owner:** Omowumi Adisa, ISSO

### RISK-002: Ransomware Encryption of Production Data

**Current Residual Score:** 8 (Low-Moderate) | **Treatment Option:** Accept with monitoring

**Justification:** The existing controls are strong. AWS GuardDuty with threat intelligence provides real-time detection. S3 Object Lock provides immutable backups with 30-day retention. EC2 image backups are taken daily and tested quarterly. The cost of further risk reduction is disproportionate to the residual risk given the cloud-native architecture.

**Monitoring Commitment:** Monthly review of GuardDuty findings; quarterly restore tests of RDS and S3 backups; annual review of this risk acceptance decision.

**Risk Owner:** Jerome K. Okafor, Cloud Ops

### RISK-003: Exploitation of Unpatched Vulnerability in EC2 AMI

**Current Residual Score:** 8 (Low-Moderate) | **Target Residual Score:** 4 (Low)
**Treatment Option:** Modify + Accept

**Additional Controls to Implement:**

| Control | Description | ISO 27001 Reference | Owner | Target Date |
|---|---|---|---|---|
| Implement automated OS patching for non-production instances | Extend AWS Systems Manager Patch Manager to cover dev and staging environments on the same SLA as production | ISO Annex A 8.8 (Technical Vulnerability Management) | Jerome K. Okafor, Cloud Ops | August 15, 2024 |
| Enable Amazon Inspector for continuous vulnerability scoring | Replace monthly scheduled scans with continuous Amazon Inspector scanning tied to new AMI deployments | ISO Annex A 8.8 | Jerome K. Okafor, Cloud Ops | September 30, 2024 |

**Resource Estimate:** 20 hours engineering time; Amazon Inspector Standard tier at approximately $160/month.

**Success Criteria:** Zero High/Critical unpatched vulnerabilities older than 30 days on any in-scope instance, including non-production.

**Risk Owner:** Jerome K. Okafor, Cloud Ops

### RISK-004: Integrity Failure in Treasury Disbursement API

**Current Residual Score:** 5 (Low) | **Treatment Option:** Accept

**Justification:** The combination of HMAC-SHA256 transaction signing, mutual TLS authentication, daily reconciliation between GMS and Treasury records, and immutable CloudTrail logging of all API calls reduces the probability of an undetected integrity failure to near zero.

**Risk Owner:** Omowumi Adisa, ISSO

### RISK-005: Unauthorized Data Exfiltration by Malicious Insider

**Current Residual Score:** 8 (Low-Moderate) | **Target Residual Score:** 6 (Low)
**Treatment Option:** Modify + Accept

**Additional Controls to Implement:**

| Control | Description | ISO 27001 Reference | Owner | Target Date |
|---|---|---|---|---|
| Tune Macie DLP rules for grant data patterns | Update AWS Macie custom identifiers to detect NexusBridge-specific grant application patterns; create alerts for large S3 downloads | ISO Annex A 8.12 (Data Leakage Prevention) | Jerome K. Okafor, Cloud Ops | August 30, 2024 |
| Implement network traffic analysis for anomalous data transfers | Configure AWS VPC Flow Logs with Athena queries to detect unusual outbound data volumes from EC2 | ISO Annex A 8.16 (Monitoring Activities) | Jerome K. Okafor, Cloud Ops | September 30, 2024 |
| Add data access auditing for bulk record queries | Log all queries returning more than 50 grant records; alert ISSO immediately | ISO Annex A 8.15 (Logging) | Jerome K. Okafor, Cloud Ops | September 30, 2024 |

**Resource Estimate:** 60 hours engineering time; no additional licensing cost (uses existing AWS services).

**Risk Owner:** Omowumi Adisa, ISSO

## Treatment Plan Summary and Timeline

| Risk ID | Treatment | Key Action | Owner | Due Date | Status |
|---|---|---|---|---|---|
| RISK-001 | Modify | Implement UEBA, PAWs, JIT access | Jerome K. Okafor | October 31, 2024 | In progress |
| RISK-002 | Accept | Monthly monitoring, quarterly restore tests | Jerome K. Okafor | Ongoing | Active |
| RISK-003 | Modify | Extend automated patching; enable Inspector | Jerome K. Okafor | September 30, 2024 | In progress |
| RISK-004 | Accept | Annual review | Omowumi Adisa | April 2025 | Active |
| RISK-005 | Modify | Tune Macie; VPC Flow Logs; bulk query alerts | Jerome K. Okafor | October 31, 2024 | In progress |

## Interview Defense Notes

**What are the four ISO 27005 risk treatment options?**
Modify (add controls to reduce the risk), Retain (accept the risk as-is), Avoid (stop the activity that creates the risk), and Share (transfer the risk to a third party like an insurer). Most practical treatment plans use a combination of Modify and Retain.

**Why would you choose to accept a risk rather than always treating it?**
Because the cost of treatment can exceed the expected loss from the risk. Risk acceptance is a legitimate business decision, not laziness. The key is that it must be documented and formally approved by the risk owner.

**What is the relationship between the Risk Treatment Plan and the POA&M?**
They address similar problems but in different frameworks. The Risk Treatment Plan is the ISO 27005 document tracking risk-based control improvements. The POA&M is the FedRAMP document tracking findings from the 3PAO assessment. For NexusBridge, both exist simultaneously, and many items appear in both.

---
*Prepared by: Omowumi Adisa, ISSO, NexusBridge Technologies*
*System: NexusBridge Grant Management System (GMS) | DOE-NB-GMS-2024-MOD*
*[GitHub Portfolio](https://github.com/Wunmi290)*
