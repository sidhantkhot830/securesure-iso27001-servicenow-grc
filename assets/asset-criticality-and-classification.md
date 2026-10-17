# SecureSure Insurance — Asset Criticality and Information Classification

## 1. Purpose

This document defines a preliminary method for classifying information and assessing the business criticality of assets within the proposed Information Security Management System (ISMS).

The method supports consistent risk assessment and prioritization of security controls. All classifications and ratings are illustrative and must be validated by the relevant asset or business owners in a real organization.

## 2. Information Classification

| Classification | Definition | Illustrative examples |
|---|---|---|
| Public | Approved for unrestricted public disclosure | Published security policies, public product information |
| Internal | Intended for authorized internal use; unauthorized disclosure would cause limited harm | Internal process documentation, generic procedures |
| Confidential | Unauthorized disclosure could cause significant business, privacy or contractual harm | Customer information, non-public business records, internal risk assessments |
| Restricted | Highly sensitive information requiring stringent access restrictions | Authentication secrets, sensitive personal information, privileged credentials and highly sensitive security records |

Classification should be based on the sensitivity of the information, applicable obligations and potential harm from unauthorized disclosure.

An asset may contain information at multiple classification levels. The handling requirements should reflect the most sensitive information it processes, unless appropriate segregation is established.

## 3. Confidentiality, Integrity and Availability Impact

Assess each asset against three dimensions.

| Rating | Confidentiality impact | Integrity impact | Availability impact |
|---|---|---|---|
| 1 — Low | Limited harm from unauthorized disclosure | Minor errors with limited consequences | Short disruption with minimal business impact |
| 2 — Moderate | Meaningful business, privacy or contractual harm | Errors could affect business decisions or require significant correction | Disruption could delay important activities |
| 3 — High | Serious harm from unauthorized disclosure | Incorrect or unauthorized changes could materially affect business operations or records | Disruption could interrupt critical services or create significant business impact |

These ratings are preliminary. The organization should define measurable criteria, impact thresholds and approval responsibilities before using them for formal risk decisions.

## 4. Asset Criticality Method

For this portfolio, calculate a simple preliminary impact score:

**Asset impact score = Confidentiality rating + Integrity rating + Availability rating**

| Score | Preliminary criticality |
|---|---|
| 3–4 | Low |
| 5–6 | Moderate |
| 7–8 | High |
| 9 | Critical |

The score is a learning aid, not a mandatory ISO/IEC 27001 formula. A real organization should validate whether an additive score is appropriate and consider dependencies, legal obligations, recovery objectives and severe impacts that might otherwise be hidden by averaging.

A high-impact dependency may justify a higher criticality rating even when the numerical score is lower.

## 5. Preliminary Asset Assessment

| Asset ID | Generic asset | C | I | A | Score | Preliminary criticality |
|---|---|---:|---:|---:|---:|---|
| AST-001 | Core business application platform | 2 | 3 | 3 | 8 | High |
| AST-002 | Scheduled processing capability | 2 | 3 | 3 | 8 | High |
| AST-003 | Business data stores | 3 | 3 | 3 | 9 | Critical |
| AST-004 | Customer-facing application | 3 | 3 | 3 | 9 | Critical |
| AST-005 | Claims processing application | 3 | 3 | 3 | 9 | Critical |
| AST-006 | Source code repository | 2 | 3 | 2 | 7 | High |
| AST-007 | Development and test environment | 2 | 2 | 2 | 6 | Moderate |
| AST-008 | Build and deployment services | 2 | 3 | 3 | 8 | High |
| AST-009 | Cloud application infrastructure | 2 | 3 | 3 | 8 | High |
| AST-010 | Application integration services | 2 | 3 | 3 | 8 | High |
| AST-011 | Identity and access management | 3 | 3 | 3 | 9 | Critical |
| AST-012 | Corporate developer endpoints | 2 | 2 | 2 | 6 | Moderate |
| AST-013 | Security logging and monitoring | 2 | 2 | 2 | 6 | Moderate |
| AST-014 | Backup and recovery services | 3 | 3 | 3 | 9 | Critical |
| AST-015 | Third-party technology services | To be assessed | To be assessed | To be assessed | — | Pending |

**Rating key:** C = Confidentiality; I = Integrity; A = Availability.

These example ratings are not final approved values. The existing asset inventory should be updated with validated ratings rather than treated as independently verified.

## 6. Development-Specific Considerations

Development assets require assessment beyond whether they store customer information.

- **Source code repository:** Unauthorized modification could introduce vulnerabilities or compromise software integrity.
- **Development environment:** Inadequately protected test data or credentials could expose sensitive information.
- **Build and deployment services:** Compromise could allow unauthorized changes to production software.
- **Developer endpoints:** Malware or credential theft could provide access to source code or privileged services.
- **Release and change records:** Missing approvals or incomplete traceability could weaken accountability.

The criticality of each asset depends on its actual access, permissions, data and dependencies.

## 7. Ownership and Review

The proposed asset owner should:

1. Validate the asset's business purpose and information handled.
2. Review confidentiality, integrity and availability impacts.
3. Confirm the preliminary criticality rating.
4. Identify dependencies and applicable security requirements.
5. Reassess ratings after significant changes or incidents.

The Information Security Manager should define the assessment methodology and oversee consistent application. Business and technical owners remain responsible for validating the impact of their assets.

## 8. ISO/IEC 27001:2022 Relevance

This assessment supports risk identification and evaluation under Clause 6.1.2 and helps inform risk treatment under Clause 6.1.3.

It can also support selection and implementation of relevant Annex A controls. The classification and scoring method in this document is a proposed portfolio methodology, not a method prescribed by ISO/IEC 27001 itself.

## 9. Assumptions and Limitations

- SecureSure Insurance is fictional.
- Asset ratings and examples are simulated.
- No real organizational assets or sensitive information are described.
- The scoring thresholds are proposed for learning purposes.
- No formal business impact analysis or risk approval has been performed.

**Status:** Initial methodology and illustrative ratings — pending validation.
