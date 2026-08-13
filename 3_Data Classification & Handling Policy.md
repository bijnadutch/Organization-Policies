# Data Classification & Handling Policy
**XXAXX — Policy #3 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Data Classification & Handling Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) |
| Approved By | Management Body / Board of Directors |
| Classification | Internal |
| Version | 1.0 |
| Effective Date | [DATE] |
| Next Review Date | [DATE + 12 months] |
| Review Cycle | Annual, or upon material change to risk, regulation, or organization |
| Parent Policy | Information Security Policy (Policy #0) |

### Revision History

| Version | Date | Author | Summary of Changes |
|---|---|---|---|
| 1.0 | [DATE] | CISO | Initial version |

---

## Table of Contents

1. [Purpose](#1-purpose)
2. [Scope](#2-scope)
3. [Definitions](#3-definitions)
4. [Policy Statement](#4-policy-statement)
5. [Roles and Responsibilities](#5-roles-and-responsibilities)
6. [Compliance and Enforcement](#6-compliance-and-enforcement)
7. [Exceptions](#7-exceptions)
8. [Review and Update](#8-review-and-update)
9. [Related Documents](#9-related-documents)
10. [Appendix A — Regulatory & Standards Mapping](#appendix-a--regulatory--standards-mapping)

---

## 1. Purpose

This Policy defines how XXAXX classifies information according to its sensitivity and criticality, and the minimum handling requirements that apply at each classification level — covering storage, transmission, sharing, printing, and disposal. Consistent classification ensures that protective effort is concentrated where it matters most, and that everyone handling XXAXX data knows what is expected of them.

## 2. Scope

This Policy applies to all information created, received, processed, or stored by XXAXX, in any format (digital, paper, verbal) and in any location, including cloud services and third-party systems. It applies to all employees, contractors, and third parties who handle XXAXX information.

## 3. Definitions

- **Data Owner**: The individual or function accountable for a given data set, responsible for assigning its classification and approving access to it.
- **Data Custodian**: The individual or team responsible for the technical storage, processing, and protection of data on behalf of the Data Owner.
- **Data Subject**: An identified or identifiable natural person to whom personal data relates.
- **Classification Label**: The designation assigned to information indicating its required level of protection.

## 4. Policy Statement

### 4.1 Classification Levels

XXAXX uses a four-tier classification scheme applied consistently across all information assets:

| Level | Label | Description | Examples |
|---|---|---|---|
| 1 | **Public** | Information approved for unrestricted external release; no harm if disclosed. | Marketing materials, published press releases, public website content. |
| 2 | **Internal** | Information intended for use within XXAXX; limited harm if disclosed externally. | Internal policies, organization charts, internal newsletters. |
| 3 | **Confidential** | Sensitive business or personal information; disclosure could cause material harm. | Contracts, financial reports, employee personal data, customer data, source code. |
| 4 | **Restricted** | Highly sensitive information; disclosure could cause severe harm, regulatory sanction, or safety impact. | Special category personal data, authentication credentials/secrets, cryptographic keys, security incident details, M&A information. |

### 4.2 Classification Responsibility

The Data Owner assigns the classification level at the point of creation or receipt, based on the criteria above and any applicable legal or contractual requirements (e.g., data protection law, client confidentiality clauses). Where information combines multiple data types, it is classified at the level of its most sensitive component. Classification is reviewed when the nature, use, or sensitivity of the data changes, and periodically as part of data owner reviews.

### 4.3 Labeling

Confidential and Restricted information is labeled — in document headers/footers, file naming conventions, email subject tags, or system metadata as appropriate to the medium — to ensure handlers are aware of its classification. Public and Internal information may be labeled but labeling is not mandatory at these levels.

### 4.4 Handling Requirements by Classification

| Control Area | Public | Internal | Confidential | Restricted |
|---|---|---|---|---|
| Storage | No restriction | XXAXX-managed systems only | Access-controlled systems; encryption at rest recommended | Encryption at rest mandatory; access strictly limited to named roles |
| Transmission | No restriction | Internal channels | Encrypted in transit; approved channels only | Encrypted in transit; approved channels only; additional authorization required |
| Access Control | Public | All employees | Role-based, need-to-know | Named individual/role approval, logged access |
| External Sharing | Permitted | Not permitted without approval | Requires NDA/contractual basis and Data Owner approval | Requires Data Owner and CISO approval; formal agreement mandatory |
| Printing | Permitted | Permitted, standard handling | Marked as Confidential; collected promptly from printers | Discouraged; if unavoidable, controlled printing and immediate secure storage |
| Disposal | Standard | Standard secure deletion | Secure deletion/shredding per retention schedule | Secure deletion/shredding with disposal evidence retained |
| Removable Media / Cloud | No restriction | Approved corporate services only | Approved, encrypted, access-controlled services only | Prohibited on general-purpose removable media; approved encrypted/controlled storage only |

Detailed technical implementation of these controls (encryption standards, access control mechanisms, network transmission controls) is defined in the Cryptography & Key Management Policy, Access Control Policy, and Network Security Policy respectively.

### 4.5 Personal Data

Personal data is classified at a minimum of Confidential, and special category/sensitive personal data (as defined under applicable data protection law) is classified as Restricted. Handling of personal data additionally follows XXAXX's data protection obligations, including lawful basis, data minimization, retention limits, and data subject rights, which are addressed in XXAXX's separate data protection/privacy documentation.

### 4.6 Data in Cloud Services

Classification and handling requirements apply equally to data stored or processed in cloud services. Before Confidential or Restricted data is stored in a new cloud service, the service is assessed under the Supplier & Third-Party Security Policy and the Cloud Security Policy to confirm it meets the required controls (encryption, access control, data residency, sub-processor transparency).

### 4.7 Retention and Disposal

Information is retained only as long as necessary for business, legal, or regulatory purposes, in accordance with XXAXX's retention schedule. At the end of its retention period, information is securely disposed of in a manner appropriate to its classification, with disposal of Confidential and Restricted information logged.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; defines classification scheme and handling requirements; resolves classification disputes. |
| Data Owners | Assign and review classification for their data; approve access and external sharing requests. |
| Data Custodians | Implement technical handling controls appropriate to classification on behalf of Data Owners. |
| IT / Information Security Team | Provide and maintain tooling to support labeling, encryption, access control, and secure disposal. |
| All Employees & Contractors | Handle information in accordance with its classification; apply labels correctly; report suspected mishandling or misclassification. |
| Data Protection Officer / Privacy Lead (if applicable) | Advises on classification and handling of personal data. |

## 6. Compliance and Enforcement

Mishandling of Confidential or Restricted information (e.g., unauthorized disclosure, storage on unapproved services, missing encryption) is treated as a security incident and reported under the Incident Management Policy. Compliance is monitored through data loss prevention tooling (where deployed), access reviews, and internal audit.

## 7. Exceptions

Exceptions to standard handling requirements (e.g., a specific business need to share Confidential data through a non-standard channel) must be approved by the relevant Data Owner and the CISO, documented with compensating controls, and time-bound.

## 8. Review and Update

This Policy and the classification scheme are reviewed at least annually and upon significant change to applicable legal/regulatory requirements or XXAXX's data landscape.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Asset Management Policy (Policy #2)
- Access Control Policy (Policy #4)
- Supplier & Third-Party Security Policy (Policy #5)
- Cryptography & Key Management Policy (Policy #20)
- Network Security Policy (Policy #21)
- Cloud Security Policy (Policy #26)
- Data Retention Schedule (supporting document)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Information classification scheme | Art. 21(2)(h)/(i) | Cl. 8.1 | A.5.12 (classification of information) | PR.DS-01 |
| Labeling | Art. 21(2)(i) | Cl. 8.1 | A.5.13 (labelling of information) | PR.DS-01 |
| Handling requirements by classification | Art. 21(2)(h)/(i) | Cl. 8.1 | A.5.10, A.5.14 (transfer of information) | PR.DS-01, PR.DS-02 |
| Access control tied to classification | Art. 21(2)(i)/(j) | Cl. 8.1 | A.5.15, A.5.18 | PR.AA |
| Encryption of confidential/restricted data | Art. 21(2)(h) | Cl. 8.1 | A.8.24 (use of cryptography) | PR.DS-01, PR.DS-02 |
| Personal / special category data | Art. 21(2)(h)/(i) | Cl. 8.1 | A.5.34 (privacy and protection of PII) | PR.DS-01 |
| Retention and secure disposal | Art. 21(2)(a)/(h) | Cl. 8.1 | A.5.12, A.7.10, A.7.14, A.8.10 | PR.DS-03 |
| Cloud data handling (cross-ref.) | Art. 21(2)(d)/(h) | Cl. 8.1 | A.5.23 (use of cloud services) | PR.DS, GV.SC |
