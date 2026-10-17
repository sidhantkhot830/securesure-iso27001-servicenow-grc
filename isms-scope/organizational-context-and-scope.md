# SecureSure Insurance — Organizational Context and ISMS Scope

## 1. Document Information

| Field | Details |
|---|---|
| Organization | SecureSure Insurance (fictional) |
| Framework | ISO/IEC 27001:2022 |
| Document owner | Information Security Manager |
| Status | Draft — proposed scope |
| Review frequency | At least annually and when significant changes occur |

## 2. Organization Overview

SecureSure Insurance is a fictional Indian life and disability insurance company. Its business activities involve policy administration, underwriting, premium processing, disability claims processing and customer servicing.

The organization operates a hybrid IT environment consisting of an on-premises mainframe, newer applications, cloud services, software development environments and shared IT infrastructure.

The mainframe supports core insurance record processing and scheduled batch processing. Newer applications provide additional functionality and integrate with selected core insurance services.

An internal software development team develops, tests, maintains and releases applications supporting the insurance business.

## 3. Organizational Context

### 3.1 Internal Issues

The following internal issues are assumed for this project:

- Dependence on legacy mainframe applications for critical insurance processing.
- Integration between legacy systems and newer applications.
- Protection of policyholder information and disability claim records.
- Management of privileged access across mainframe, cloud and development environments.
- Separation of development, testing and production activities.
- Management of software changes, batch jobs and application releases.
- Availability and recoverability of systems supporting insurance operations.
- Potential limitations in monitoring or updating legacy technology.

### 3.2 External Issues

The following external issues are relevant to the proposed ISMS:

- Applicable Indian data protection, insurance and other legal or regulatory obligations.
- Cybersecurity threats targeting financial services and personal information.
- Dependence on cloud providers and external technology suppliers.
- Third-party access to systems and information.
- Technology changes that may affect legacy system compatibility or security.
- Business continuity expectations and contractual obligations.

Applicable laws and regulatory requirements will be identified and validated during a subsequent compliance assessment.

## 4. Interested Parties and Relevant Requirements

| Interested party | Relevant needs or expectations |
|---|---|
| Policyholders and claimants | Confidentiality of personal information, accurate records and reliable services |
| Executive management | Appropriate risk management, governance and business continuity |
| Information security team | Defined responsibilities, effective controls and reliable evidence |
| Software development team | Secure development practices, controlled changes and appropriate access |
| IT operations and mainframe administrators | Controlled privileged access, system availability and recoverability |
| Internal audit or assurance personnel | Traceable requirements, objective evidence and documented findings |
| Regulators and other authorities | Compliance with applicable legal and regulatory obligations |
| Cloud and technology providers | Clear security responsibilities and appropriate contractual arrangements |

The relevant requirements of each interested party will be validated and maintained as the project develops.

## 5. Proposed ISMS Scope

The proposed ISMS covers the information, people, processes, applications and supporting technology used to deliver SecureSure Insurance's life and disability insurance services and to develop, operate and maintain the supporting applications.

The scope includes:

### 5.1 Business Operations

- Life insurance policy administration and customer servicing.
- Underwriting and premium processing.
- Disability insurance claims processing.
- Management of associated policyholder and claims information.

### 5.2 Mainframe Environment

- Mainframe infrastructure and operating environment supporting scoped insurance services.
- Core insurance record processing.
- Scheduled batch processing and associated job scheduling.
- Mainframe access administration and privileged accounts.
- Relevant interfaces, data transfers, operational monitoring and backup or recovery arrangements.

### 5.3 Software Development

- Source code repositories and developer access.
- Software design, development and code review.
- Development and test environments.
- Build and deployment pipelines, where used.
- Change approval, release management and production deployment.
- Management of application secrets, test data and software vulnerabilities.

### 5.4 Cloud and Newer Applications

- Cloud-hosted applications and services supporting scoped insurance activities.
- Customer-facing applications and relevant integration services.
- Cloud identities, permissions, configurations and security monitoring.
- Interfaces between cloud applications and the mainframe.
- Relevant third-party hosting and technology services.

### 5.5 Shared IT Services

- Corporate endpoints used to administer or develop scoped systems.
- Identity and access management.
- Network security and connectivity supporting the scoped environment.
- Security logging and monitoring.
- Backup, recovery and continuity arrangements.
- Relevant third-party personnel and services.

## 6. Interfaces and Dependencies

The ISMS will consider dependencies and information flows between:

- Mainframe applications and newer insurance applications.
- Mainframe batch jobs and upstream or downstream data sources.
- Development and test environments and production systems.
- Cloud applications and the mainframe.
- Identity services and systems requiring authentication or privileged access.
- Internal technology teams and external service providers.

Specific data flows, protocols, trust boundaries and system ownership will be validated during architecture and asset documentation.

## 7. Exclusions and Boundaries

No final exclusions have been approved at this stage.

Corporate functions, applications, locations or services that do not directly support the proposed scope will be assessed before any exclusion is documented.

An exclusion must not be used to disregard a relevant dependency, interface, legal obligation or information security risk.

The final scope will identify the relevant organizational boundaries, physical or logical locations, technologies, activities and interfaces.

## 8. Assumptions and Limitations

- SecureSure Insurance is fictional and created for portfolio demonstration.
- The mainframe supports both core insurance record processing and scheduled batch processing.
- Newer applications integrate with selected mainframe services.
- Cloud services support selected applications and technology functions.
- The precise technology stack, physical locations, data flows and third-party arrangements are proposed assumptions pending further design.
- All assets, users, risks, evidence and assessment outcomes are simulated.
- The project demonstrates implementation knowledge and does not establish certification or compliance for a real organization.

## 9. ISO/IEC 27001:2022 References

This document supports the following clauses:

- Clause 4.1 — Understanding the organization and its context.
- Clause 4.2 — Understanding the needs and expectations of interested parties.
- Clause 4.3 — Determining the scope of the ISMS.
- Clause 4.4 — Information security management system.

## 10. Review and Approval

The proposed scope should be reviewed by executive management, the Information Security Manager, IT operations, the mainframe owner and the software development lead.

**Current status:** Draft — proposed scope.

**Next milestone:** Establish the asset inventory, validate dependencies and refine scope boundaries.
