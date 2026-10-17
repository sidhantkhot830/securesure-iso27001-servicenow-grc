# SecureSure Insurance — Information Asset Inventory

## 1. Purpose

This inventory identifies the initial information assets and supporting technology within the proposed SecureSure Insurance ISMS scope.

The inventory will support risk assessment, control selection, ownership assignment and evidence planning.

## 2. Asset Inventory

| Asset ID | Asset name | Asset type | Business purpose | Proposed owner | Information handled | Initial impact classification |
|---|---|---|---|---|---|---|
| AST-001 | Mainframe Core Insurance System | Application/platform | Processes and maintains core insurance records | Mainframe Service Owner | Policy and premium records | High |
| AST-002 | Mainframe Batch Processing | Application/process platform | Executes scheduled insurance processing jobs | Mainframe Operations Lead | Processing files, policy updates and job outputs | High |
| AST-003 | Mainframe Data Stores | Data asset | Stores records supporting core insurance operations | Data Owner / Mainframe Service Owner | Policyholder and insurance records | High |
| AST-004 | Customer Portal | Application | Enables customer access to insurance services | Application Owner | Customer identity and policy information | High |
| AST-005 | Disability Claims Application | Application | Supports disability claims processing | Claims Systems Owner | Claim records and potentially sensitive personal information | High |
| AST-006 | Source Code Repository | Development asset | Stores application source code and version history | Development Lead | Source code and configuration | High |
| AST-007 | Development Environment | IT environment | Supports application development and testing | Development Lead | Source code, test data and configuration | High |
| AST-008 | CI/CD and Release Pipeline | Development asset | Builds, tests and deploys application changes | DevOps / Development Lead | Build artifacts, deployment configurations and secrets references | High |
| AST-009 | Cloud Application Infrastructure | Infrastructure | Hosts selected applications and integration services | Cloud / Infrastructure Owner | Application data and operational configuration | High |
| AST-010 | Integration Interfaces | Integration asset | Exchanges information between mainframe and newer applications | Integration Service Owner | Policy, claims and processing data | High |
| AST-011 | Identity and Access Management | Shared IT service | Manages authentication and access to scoped systems | IAM Service Owner | Identity records, access assignments and authentication data | High |
| AST-012 | Corporate Developer Endpoints | Endpoint asset | Enables development and administration activities | Endpoint / IT Operations Owner | Source code, credentials and business information | High |
| AST-013 | Security Logs and Monitoring | Security service | Supports detection, investigation and accountability | Security Operations Lead | Authentication, access and system events | Medium |
| AST-014 | Backup and Recovery Services | Resilience service | Supports recovery of critical systems and information | IT Operations / Recovery Owner | Backup copies and recovery metadata | High |
| AST-015 | Technology Supplier Services | Third-party service | Provides hosting, maintenance or technical support | Vendor Relationship Owner | Access and information determined by each supplier relationship | To be assessed |

## 3. Asset Ownership and Responsibilities

Asset owners are accountable for ensuring that assets are appropriately managed and protected.

Technical custodians may administer infrastructure or applications on behalf of the asset owner.

The asset owner, data owner and technical custodian may be different people. Their responsibilities should be recorded where applicable.

The roles listed above are proposed role titles, not confirmed employees or configured ServiceNow users.

## 4. Inventory Limitations

This is an initial logical asset inventory. It does not yet represent a verified configuration inventory or complete hardware and software register.

The following information remains to be established:

- Actual asset identifiers and technical hostnames.
- Mainframe platform and operating environment details.
- Database and storage technologies.
- Network zones and connectivity paths.
- Application and data-flow dependencies.
- Information classification criteria.
- Availability, recovery and retention requirements.
- Asset criticality and approved business impact ratings.
- Confirmed owners and supporting service providers.

## 5. Next Steps

1. Validate the asset list against the proposed ISMS scope.
2. Identify important relationships and dependencies between assets.
3. Establish information classification and asset criticality criteria.
4. Identify threats, vulnerabilities and risk scenarios.
5. Perform risk assessment using an approved methodology.

**Status:** Initial proposed inventory — pending risk and dependency analysis.
