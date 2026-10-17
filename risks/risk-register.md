# SecureSure Insurance — Information Security Risk Register

## 1. Purpose

This register identifies hypothetical information security risks affecting the fictional SecureSure Insurance environment.

It supports risk evaluation, treatment planning and future mapping to ISO/IEC 27001:2022 requirements and applicable Annex A controls.

All scenarios, controls, ratings and treatment decisions are simulated for portfolio demonstration.

## 2. Risk Assessment Methodology

### 2.1 Likelihood

| Rating | Level | Definition |
|---|---|---|
| 1 | Rare | The event is considered highly unlikely under the assessed conditions |
| 2 | Unlikely | The event could occur but is not expected frequently |
| 3 | Possible | The event could occur under plausible conditions |
| 4 | Likely | The event is expected to occur in many circumstances |
| 5 | Almost Certain | The event is expected to occur frequently or is already recurring |

### 2.2 Impact

| Rating | Level | Definition |
|---|---|---|
| 1 | Insignificant | Minimal disruption or harm |
| 2 | Minor | Limited operational impact requiring routine correction |
| 3 | Moderate | Material disruption, data errors or additional recovery effort |
| 4 | Major | Significant business disruption, sensitive data exposure or substantial financial or regulatory consequences |
| 5 | Severe | Extensive disruption, serious information compromise or potentially severe legal, financial or customer consequences |

Impact should reflect the credible consequences for confidentiality, integrity, availability, customers, legal obligations and business operations.

### 2.3 Risk Scoring

**Risk score = Likelihood × Impact**

| Score | Risk level | Proposed response |
|---|---|---|
| 1–4 | Low | Monitor and manage through routine controls |
| 5–9 | Moderate | Evaluate and document proportionate treatment |
| 10–16 | High | Prioritize treatment and obtain appropriate risk-owner review |
| 17–25 | Critical | Escalate promptly for risk-owner and management attention |

These are proposed portfolio thresholds, not mandatory ISO requirements. A real organization should approve its own risk criteria and escalation rules.

## 3. Risk Register

| Risk ID | Risk scenario | Affected assets | Inherent L | Inherent I | Inherent score | Inherent level |
|---|---|---|---:|---:|---:|---|
| RSK-001 | Excessive developer permissions could allow unauthorized changes to source code or production resources. | AST-006, AST-007, AST-008 | 4 | 5 | 20 | Critical |
| RSK-002 | Inadequate code review or security testing could allow vulnerable software to reach production. | AST-006, AST-007, AST-008, AST-009 | 4 | 4 | 16 | High |
| RSK-003 | Unapproved or poorly tested changes could disrupt business applications or compromise data integrity. | AST-001, AST-004, AST-005, AST-008 | 3 | 5 | 15 | High |
| RSK-004 | Weak access management could allow unauthorized users or compromised accounts to access sensitive information. | AST-003, AST-004, AST-005, AST-011 | 4 | 5 | 20 | Critical |
| RSK-005 | Inadequately protected application integrations could expose information or permit unauthorized data modification. | AST-001, AST-004, AST-009, AST-010 | 3 | 5 | 15 | High |
| RSK-006 | Errors or failures in scheduled processing could result in incomplete business processing or incorrect customer correspondence. | AST-002, AST-003, AST-014 | 3 | 4 | 12 | High |
| RSK-007 | Insufficient monitoring could delay the detection and investigation of unauthorized activity or system failures. | AST-001, AST-008, AST-011, AST-013 | 3 | 4 | 12 | High |
| RSK-008 | Inadequate backup protection or recovery arrangements could prevent timely restoration following a disruptive event. | AST-003, AST-009, AST-014 | 3 | 5 | 15 | High |
| RSK-009 | Inappropriate handling of test data could expose confidential customer or claims information in non-production environments. | AST-005, AST-007, AST-012 | 3 | 4 | 12 | High |
| RSK-010 | Weak supplier oversight could expose information or disrupt services through a third-party technology provider. | AST-009, AST-015 | 3 | 4 | 12 | High |

**Rating note:** The inherent ratings are illustrative initial estimates. They have not been derived from actual incident statistics, interviews or technical testing.

## 4. Existing Controls and Residual Risk

For this learning exercise, the following controls are hypothetical assumptions used to demonstrate risk evaluation. Their existence and effectiveness have not been verified.

| Risk ID | Hypothetical existing controls | Residual L | Residual I | Residual score | Residual level |
|---|---|---:|---:|---:|---|
| RSK-001 | Role-based access, repository permissions and separate production access | 3 | 5 | 15 | High |
| RSK-002 | Peer reviews and pre-release testing | 3 | 4 | 12 | High |
| RSK-003 | Change approval and release validation | 2 | 5 | 10 | High |
| RSK-004 | Authentication controls, access reviews and privileged access restrictions | 3 | 5 | 15 | High |
| RSK-005 | Authenticated integrations and restricted service permissions | 2 | 5 | 10 | High |
| RSK-006 | Job monitoring, processing reconciliation and exception handling | 2 | 4 | 8 | Moderate |
| RSK-007 | Centralized logging, alerting and incident investigation procedures | 2 | 4 | 8 | Moderate |
| RSK-008 | Protected backups and documented recovery procedures | 2 | 5 | 10 | High |
| RSK-009 | Test-data handling rules and restricted access to non-production environments | 2 | 4 | 8 | Moderate |
| RSK-010 | Supplier due diligence, contractual security requirements and periodic reviews | 2 | 4 | 8 | Moderate |

Residual scores are calculated using the same likelihood-times-impact method. The impact rating is unchanged where the assumed controls primarily reduce likelihood rather than the severity of a successful event.

**Important:** These residual scores are scenario assumptions, not evidence of effective controls. If existing controls cannot be demonstrated, the residual ratings must be reassessed.

## 5. Proposed Risk Treatment Plan

| Risk ID | Proposed treatment action | Suggested owner | Target priority |
|---|---|---|---|
| RSK-001 | Review developer privileges, separate production access and periodically recertify permissions | Development Lead / IAM Owner | High |
| RSK-002 | Establish secure coding standards, code review requirements and security testing before release | Development Lead | High |
| RSK-003 | Require documented change approvals, testing evidence, release traceability and rollback planning | Change Manager / Application Owner | High |
| RSK-004 | Enforce least privilege, stronger authentication and periodic access reviews | IAM Owner | High |
| RSK-005 | Document integration ownership, restrict service permissions and review interface security | Application / Integration Owner | High |
| RSK-006 | Define processing success criteria, monitor failures and document exception recovery | IT Operations Owner | Moderate |
| RSK-007 | Define logging requirements, alert ownership and periodic monitoring reviews | Security Operations Lead | Moderate |
| RSK-008 | Validate backup coverage, protect backup access and periodically test restoration | IT Operations / Recovery Owner | High |
| RSK-009 | Use synthetic or appropriately masked test data and restrict access to sensitive datasets | Development Lead / Data Owner | High |
| RSK-010 | Assess supplier security risks, track assurance evidence and review contractual obligations | Vendor Relationship Owner | Moderate |

Priorities are proposed planning decisions. The organization would need to confirm ownership, deadlines, resources and treatment acceptance criteria.

## 6. Risk Treatment Options

For each risk, the risk owner should consider the following options:

- **Mitigate:** Implement or improve controls to reduce likelihood or impact.
- **Avoid:** Stop or redesign the activity creating the risk.
- **Transfer or share:** Allocate part of the financial or operational consequences through suitable contractual or insurance arrangements, while recognizing that accountability may remain.
- **Accept:** Retain the risk through a documented decision by an authorized risk owner, within approved acceptance criteria.

Acceptance should not be assumed simply because treatment is expensive or inconvenient. Legal, contractual and other mandatory requirements must still be addressed.

## 7. Risk Governance and Review

For a more complete GRC workflow, each risk record should eventually include:

- Risk owner and affected business service.
- Related assets and risk category.
- Inherent and residual assessments.
- Existing control references and supporting evidence.
- Treatment decision and planned actions.
- Target dates, action owners and status.
- Risk acceptance approval, where applicable.
- Review date and reassessment triggers.

Risks should be reviewed when significant changes, security incidents, control failures or new information materially affect the assessment.

## 8. ISO/IEC 27001:2022 Alignment

This register supports:

- Clause 6.1.2 — Information security risk assessment.
- Clause 6.1.3 — Information security risk treatment.
- Clause 8.2 — Information security risk assessment as part of operational planning.
- Clause 8.3 — Information security risk treatment.

Potential Annex A control mappings will be documented separately after the risks and proposed treatments are reviewed. A control should not be marked implemented or effective without appropriate supporting evidence.

## 9. Limitations

- SecureSure Insurance is fictional.
- All risks, ratings, owners and controls are simulated.
- No real vulnerabilities, incidents or findings are represented.
- No control implementation or effectiveness testing has been performed.
- Risk scores and acceptance thresholds are proposed for learning purposes.

**Status:** Initial risk register — pending review and treatment decisions.
