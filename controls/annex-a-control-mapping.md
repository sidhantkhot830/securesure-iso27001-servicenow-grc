# ISO/IEC 27001:2022 Annex A Control Mapping

## 1. Purpose

This document maps selected information security risks in the fictional SecureSure Insurance environment to relevant ISO/IEC 27001:2022 Annex A controls.

The mapping is intended to demonstrate risk-based control selection, control rationale, and the types of evidence that could support an audit or control assessment.

**Important:** This is a proposed learning exercise. The controls, evidence examples, and organizational arrangements described here are hypothetical. No control implementation or effectiveness has been verified.

## 2. Mapping Methodology

Controls are selected based on:

- The information security risks documented in `risks/risk-register.md`.
- The logical assets and dependencies documented in the asset inventory and dependency map.
- The potential confidentiality, integrity, and availability impacts.
- The need for preventive, detective, and corrective measures.
- The relevance of each control to the organization's proposed ISMS scope.

A control may address multiple risks, and a single risk may require multiple controls.

Annex A is a reference set of controls, not a checklist requiring every control to be implemented automatically. Applicability decisions must be assessed and documented in the Statement of Applicability (SoA), with appropriate justification.

## 3. Risk-to-Control Mapping

| Risk ID | Risk scenario | Relevant Annex A controls |
|---|---|---|
| RSK-001 | Excessive developer permissions allow unauthorized source code or production changes | A.5.15 Access control; A.5.18 Access rights; A.8.2 Privileged access rights; A.8.4 Access to source code; A.8.31 Separation of development, test and production environments |
| RSK-002 | Inadequate code review or security testing allows vulnerable software into production | A.8.8 Management of technical vulnerabilities; A.8.25 Secure development life cycle; A.8.26 Application security requirements; A.8.28 Secure coding; A.8.29 Security testing in development and acceptance; A.8.32 Change management |
| RSK-003 | Unapproved or poorly tested changes disrupt applications or data integrity | A.8.9 Configuration management; A.8.29 Security testing in development and acceptance; A.8.31 Separation of development, test and production environments; A.8.32 Change management |
| RSK-004 | Weak access management permits unauthorized access to sensitive information | A.5.15 Access control; A.5.16 Identity management; A.5.18 Access rights; A.8.2 Privileged access rights; A.8.3 Information access restriction; A.8.5 Secure authentication |
| RSK-005 | Inadequately protected integrations expose information or permit unauthorized data modification | A.5.14 Information transfer; A.8.20 Network security; A.8.21 Security of network services; A.8.24 Use of cryptography; A.8.26 Application security requirements |
| RSK-006 | Scheduled processing failures or errors cause incomplete processing or incorrect customer correspondence | A.5.37 Documented operating procedures; A.8.15 Logging; A.8.16 Monitoring activities; A.8.32 Change management |
| RSK-007 | Insufficient monitoring delays detection or investigation of unauthorized activity or failures | A.5.24 Information security incident management planning and preparation; A.5.25 Assessment and decision on information security events; A.5.26 Response to information security incidents; A.5.28 Collection of evidence; A.8.15 Logging; A.8.16 Monitoring activities |
| RSK-008 | Inadequate backup protection or recovery prevents timely restoration | A.5.30 ICT readiness for business continuity; A.8.13 Information backup; A.8.14 Redundancy of information processing facilities |
| RSK-009 | Poor test-data handling exposes confidential customer or claims information in non-production | A.5.34 Privacy and protection of PII; A.8.3 Information access restriction; A.8.11 Data masking; A.8.33 Test information |
| RSK-010 | Weak supplier oversight exposes information or disrupts services through a third party | A.5.19 Information security in supplier relationships; A.5.20 Addressing information security within supplier agreements; A.5.21 Managing information security in the ICT supply chain; A.5.22 Monitoring, review and change management of supplier services; A.5.23 Information security for use of cloud services, where applicable |

*Control titles follow the ISO/IEC 27001:2022 Annex A control set. Confirm exact wording against an authorized copy of the standard when using this document for formal audit work.*

## 4. Control Rationale and Potential Evidence

The following examples explain why selected controls matter and what evidence an auditor or GRC analyst could request.

All evidence examples are illustrative. They must not be represented as existing SecureSure records.

### 4.1 Development access and source code — RSK-001

**Relevant controls:** A.5.18, A.8.2, A.8.4 and A.8.31.

**Rationale:** Developers require access to repositories and development tools, but excessive privileges or unrestricted production access can enable unauthorized code changes.

**Potential evidence:**
- Approved developer access requests.
- Repository permission exports.
- Privileged access reviews.
- Documented separation between development and production.
- Records of access removal following role changes.

**Assessment question:** Are source code and production privileges restricted to authorized personnel according to business need?

### 4.2 Secure software development — RSK-002

**Relevant controls:** A.8.8, A.8.25, A.8.26, A.8.28 and A.8.29.

**Rationale:** A defined secure development lifecycle should identify security requirements, promote secure coding, address technical vulnerabilities, and test security before release.

**Potential evidence:**
- Secure development lifecycle procedure.
- Documented application security requirements.
- Peer-review records.
- Security testing reports.
- Vulnerability remediation tickets.
- Release approval records.

**Assessment question:** Is security testing performed at appropriate stages, and are material findings addressed before production release?

### 4.3 Change and release management — RSK-003

**Relevant controls:** A.8.9, A.8.29, A.8.31 and A.8.32.

**Rationale:** Changes to applications, configurations, integrations and mainframe processing can affect data integrity or service availability. Controlled approval, testing and release procedures reduce this risk.

**Potential evidence:**
- Change tickets with approval history.
- Test results linked to a change.
- Release records.
- Emergency-change reviews.
- Rollback or recovery procedures.

**Assessment question:** Can a sample production change be traced from request and approval through testing and implementation?

### 4.4 Identity and access management — RSK-004

**Relevant controls:** A.5.15, A.5.16, A.5.18, A.8.2, A.8.3 and A.8.5.

**Rationale:** Access to customer information, claims data, administrative functions and sensitive systems should be authorized, appropriately restricted and periodically reviewed.

**Potential evidence:**
- Access control policy.
- Joiner, mover and leaver records.
- Periodic access certification results.
- Privileged account inventory.
- Authentication configuration evidence.
- Remediation records for inappropriate access.

**Assessment question:** Are access rights approved, proportionate to assigned duties, and removed or adjusted when no longer required?

### 4.5 Integration security — RSK-005

**Relevant controls:** A.5.14, A.8.20, A.8.21, A.8.24 and A.8.26.

**Rationale:** Websites, cloud applications, internal systems and mainframe interfaces may exchange sensitive information. Integration security should address authorization, transmission protection, network security and application requirements.

**Potential evidence:**
- Interface inventory and ownership records.
- Approved integration security requirements.
- Service-account permission reviews.
- Encryption configuration records where applicable.
- Interface testing results.
- Documented data-transfer procedures.

**Assessment question:** Are information transfers authorized, protected appropriately and limited to the data and operations required by the receiving service?

### 4.6 Mainframe batch processing — RSK-006

**Relevant controls:** A.5.37, A.8.15, A.8.16 and A.8.32.

**Rationale:** Scheduled processing supports activities such as insurance record updates and customer correspondence. Failed or incomplete jobs may affect data accuracy and business operations.

**Potential evidence:**
- Documented batch operating procedures.
- Job completion and exception reports.
- Reconciliation records.
- Incident tickets for failed processing.
- Change approvals for job schedules or processing logic.

**Assessment question:** Are processing failures detected, investigated, reconciled and resolved through a documented procedure?

### 4.7 Security monitoring and incident handling — RSK-007

**Relevant controls:** A.5.24, A.5.25, A.5.26, A.5.28, A.8.15 and A.8.16.

**Rationale:** Appropriate logging and monitoring support detection, investigation and response. Relevant logs must be sufficiently protected and available to authorized personnel.

**Potential evidence:**
- Logging and monitoring standards.
- Defined alert ownership and escalation procedures.
- Sample alert investigation records.
- Incident response procedures.
- Log access and retention configurations.
- Evidence-handling procedures.

**Assessment question:** Are important events logged and reviewed, and can suspected incidents be investigated using reliable records?

### 4.8 Backup and recovery — RSK-008

**Relevant controls:** A.5.30, A.8.13 and A.8.14.

**Rationale:** Critical applications and information require appropriate backup and recovery arrangements. Backup availability alone does not prove that information can be restored within business requirements.

**Potential evidence:**
- Backup schedules and completion reports.
- Backup access restrictions.
- Recovery plans and assigned responsibilities.
- Restoration test results.
- Business continuity requirements and recovery objectives.
- Remediation records for failed recovery tests.

**Assessment question:** Have restoration procedures been tested, and do the results support the required recovery objectives?

### 4.9 Test-data protection — RSK-009

**Relevant controls:** A.5.34, A.8.3, A.8.11 and A.8.33.

**Rationale:** Development and test environments may not require real customer information. Data masking, access restrictions and controlled test-data handling can reduce unnecessary exposure.

**Potential evidence:**
- Test-data management procedure.
- Records demonstrating synthetic or masked test data use.
- Non-production access reviews.
- Data masking configuration or test results.
- Approved exceptions for use of sensitive data.

**Assessment question:** Is sensitive information prevented from entering non-production environments unnecessarily, and are exceptions approved and controlled?

### 4.10 Supplier security — RSK-010

**Relevant controls:** A.5.19, A.5.20, A.5.21, A.5.22 and A.5.23 where cloud services are used.

**Rationale:** Third-party providers may process information, host applications or support critical technology services. Supplier risk management should continue throughout the relationship, not stop at contract signing.

**Potential evidence:**
- Supplier risk assessments.
- Security clauses in contracts.
- Relevant assurance reports or certifications.
- Supplier review records.
- Documented cloud-service responsibilities.
- Remediation tracking for supplier findings.

**Assessment question:** Are supplier security requirements defined, assessed and reviewed according to the sensitivity and criticality of the service?

## 5. How to Use This Mapping in a Control Assessment

For each selected control:

1. Confirm whether the control is applicable to the ISMS scope.
2. Record the justification for including or excluding it in the Statement of Applicability.
3. Identify the accountable control owner.
4. Define the control objective and expected operation.
5. Request appropriate evidence.
6. Assess design adequacy separately from operating effectiveness.
7. Record any gap as a finding or improvement action, where appropriate.
8. Link the finding to its risk and track remediation.

Do not mark a control as effective merely because a policy or procedure exists. Evidence should support the control's actual design and operation.

## 6. Limitations and Assumptions

- The company, assets, risks and evidence are fictional.
- This is an initial risk-to-control mapping, not a completed Statement of Applicability.
- The mapping does not establish compliance or certification readiness.
- Control applicability depends on the final ISMS scope, risk assessment, legal and contractual obligations, and organizational decisions.
- The exact implementation of a control may differ between mainframe, cloud, application development and shared IT environments.
- Evidence must be assessed for authenticity, relevance, completeness and period of coverage before drawing audit conclusions.
- Residual risk and control effectiveness must be reassessed using actual implementation and assessment evidence in a real engagement.

## 7. References

- ISO/IEC 27001:2022 — Information security management systems — Requirements.
- ISO/IEC 27001:2022, Annex A — Information security controls reference.
- ISO/IEC 27002:2022 — Information security controls guidance.

Use authorized copies of the standards for formal interpretations and audit work.

## 8. Next Step

The next phase is to develop a **Statement of Applicability (SoA)** that records selected controls, applicability decisions, justifications, implementation status and references to supporting evidence.
