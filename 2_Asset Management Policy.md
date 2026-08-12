# Asset Management Policy
**XXAXX — Policy #2 (Organizational)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Asset Management Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) / IT Operations Manager |
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

This Policy establishes how XXAXX identifies, records, classifies, and manages its information assets throughout their lifecycle. An accurate, current asset inventory is the foundation for effective risk management, vulnerability management, access control, and incident response — without knowing what it has, XXAXX cannot reliably protect it.

## 2. Scope

This Policy applies to all information assets owned, leased, licensed, or otherwise used by XXAXX, including:

- **Hardware**: servers, workstations, laptops, mobile devices, network equipment, removable media, IoT/OT devices;
- **Software**: applications, operating systems, licensed products, open-source components;
- **Data**: structured and unstructured information in any format or location, including cloud-hosted data;
- **Cloud assets**: virtual machines, containers, storage buckets, managed services, SaaS accounts;
- **Intangible assets**: intellectual property, certificates, cryptographic keys (ownership/inventory only — handling is defined in the Cryptography & Key Management Policy).

This Policy applies to all employees, contractors, and third parties who create, use, or manage XXAXX assets.

## 3. Definitions

- **Asset**: Anything of value to XXAXX that supports its information processing activities.
- **Asset Inventory**: The authoritative, centrally maintained register of all in-scope assets.
- **Asset Owner**: The individual or function accountable for an asset throughout its lifecycle, including its classification, protection, and eventual decommissioning.
- **Asset Custodian**: The individual or team responsible for the day-to-day operation and technical maintenance of an asset on behalf of the Asset Owner.
- **End of Life (EOL)**: The point at which an asset is no longer supported, maintained, or fit for use and must be decommissioned or replaced.

## 4. Policy Statement

### 4.1 Asset Inventory

XXAXX maintains a complete, accurate, and current inventory of all in-scope information assets. At minimum, each inventory record includes: a unique identifier, description, type/category, location (physical or logical, including cloud region/account), Asset Owner, Asset Custodian, classification level, and status (active, in maintenance, decommissioned). The inventory is reconciled against technical discovery tools (e.g., endpoint management, cloud asset discovery, network scanning) on a regular schedule to identify unmanaged or "shadow IT" assets.

### 4.2 Ownership

Every asset has a named Asset Owner assigned at the time of acquisition or creation. Asset Owners are accountable for ensuring their assets are appropriately classified, protected in line with that classification, used in accordance with this Policy, and securely decommissioned at end of life. Ownership is reassigned promptly when an Owner changes role or leaves XXAXX.

### 4.3 Acceptable Use

Assets provided by XXAXX are to be used primarily for business purposes in support of XXAXX's objectives. Detailed rules governing acceptable use of IT assets, internet, email, and personal use are set out in the Acceptable Use Policy. Asset Owners and Custodians ensure users are made aware of applicable acceptable use terms at the point assets are issued.

### 4.4 Classification Handling

All assets, particularly data assets, are classified and handled in accordance with the Data Classification & Handling Policy. Classification determines the minimum protective controls (e.g., encryption, access restriction, logging) applicable to an asset.

### 4.5 Asset Lifecycle

Assets are managed through a defined lifecycle: **procurement/creation → registration in inventory → deployment/use → maintenance → decommissioning/disposal**. Security requirements are considered at each stage:

- **Procurement**: new hardware, software, and cloud services are assessed for security fit (including supply chain considerations per the Supplier & Third-Party Security Policy) prior to acquisition.
- **Registration**: assets are entered into the inventory before being connected to XXAXX's network or granted access to XXAXX data, with limited documented exceptions for time-bound testing.
- **Maintenance**: assets are kept patched and supported in line with the Vulnerability Management Policy; unsupported/EOL software and hardware are tracked and remediated.
- **Decommissioning**: assets are removed from active service in a controlled manner, access is revoked, and data is securely erased or the asset is securely destroyed in accordance with its classification, with disposal evidence retained.

### 4.6 Return of Assets

Upon termination of employment, contract, or engagement, all XXAXX assets (devices, media, access credentials, documents) issued to an individual are returned or securely wiped, coordinated with HR offboarding under the HR Security Policy. Outstanding assets are tracked to closure before final access revocation is confirmed.

### 4.7 Removable Media and BYOD

Use of removable media and personally owned devices is restricted and governed by the Remote Working & BYOD Policy; asset inventory obligations extend to any personally owned device authorized to access XXAXX data.

### 4.8 Cloud Asset Management

Cloud resources (accounts, subscriptions, workloads, storage) are inventoried with the same rigor as on-premises assets. Cloud accounts are provisioned only through approved processes; auto-discovery/cloud security posture tooling is used to detect unmanaged or misconfigured cloud resources on an ongoing basis.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; oversees asset management process effectiveness; reports gaps (e.g., shadow IT, EOL assets) as risks. |
| IT Operations / Asset Management Function | Maintains the asset inventory tooling; performs reconciliation and discovery scans; coordinates decommissioning. |
| Asset Owners | Accountable for classification, protection, appropriate use, and lifecycle management of assigned assets. |
| Asset Custodians | Perform day-to-day technical maintenance and operational tasks for assets on behalf of Owners. |
| HR | Coordinates asset return as part of onboarding/offboarding processes. |
| All Employees & Contractors | Use assigned assets appropriately; report lost, stolen, or unregistered assets promptly. |
| Procurement | Ensures new assets are registered and security-assessed prior to or at the point of acquisition. |

## 6. Compliance and Enforcement

Connecting unregistered devices or provisioning unregistered cloud resources without going through the approved process is a breach of this Policy. Compliance is verified through periodic inventory audits, reconciliation against discovery tooling, and internal audit review. Significant discrepancies between the inventory and discovered assets are logged as risks under the Risk Management Policy.

## 7. Exceptions

Exceptions (e.g., time-limited test devices, research equipment) must be approved by the CISO or IT Operations Manager, documented with scope and expiry, and reviewed at expiry to confirm removal or formal registration.

## 8. Review and Update

This Policy is reviewed at least annually and upon significant change to XXAXX's IT environment, cloud footprint, or organizational structure.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Data Classification & Handling Policy (Policy #3)
- Access Control Policy (Policy #4)
- Supplier & Third-Party Security Policy (Policy #5)
- Vulnerability Management Policy (Policy #7)
- HR Security Policy (Policy #14)
- Acceptable Use Policy (Policy #16)
- Remote Working & BYOD Policy (Policy #17)
- Cloud Security Policy (Policy #26)
- Asset Inventory (living operational record)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Asset inventory | Art. 21(2)(a) | Cl. 4.3, 8.1 | A.5.9 (inventory of info & assets) | ID.AM-01, ID.AM-02 |
| Asset ownership | Art. 21(2)(i) | Cl. 5.3 | A.5.9, A.5.2 | ID.AM-01 |
| Acceptable use of assets | Art. 21(2)(g)/(i) | Cl. 8.1 | A.5.10 (acceptable use of information and assets) | PR.AT, PR.PS |
| Classification handling (cross-ref.) | Art. 21(2)(h)/(i) | Cl. 8.1 | A.5.12, A.5.13 | PR.DS-01 |
| Return of assets | Art. 21(2)(i) | Cl. A.6.5 (context) | A.5.11 (return of assets) | PR.AA-05 |
| Asset lifecycle & maintenance | Art. 21(2)(a) | Cl. 8.1 | A.7.9, A.7.13, A.8.1 | ID.AM-08, PR.MA |
| Secure disposal / decommissioning | Art. 21(2)(a)/(h) | Cl. 8.1 | A.7.10, A.7.14, A.8.10 | PR.DS-03 |
| Removable media & BYOD (cross-ref.) | Art. 21(2)(i)/(j) | Cl. 8.1 | A.7.10, A.8.1 | PR.PS-04 |
| Cloud asset management | Art. 21(2)(d)/(j) | Cl. 8.1 | A.5.9, A.8.1, A.5.23 | ID.AM-01, PR.PS |
