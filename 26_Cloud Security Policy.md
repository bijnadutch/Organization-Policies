# Cloud Security Policy
**XXAXX — Policy #26 (Technological)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Cloud Security Policy |
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

This Policy defines how XXAXX secures its use of cloud services — infrastructure, platform, and software as a service (IaaS/PaaS/SaaS) — consolidating cloud-specific requirements that are referenced throughout this policy suite into a single, coherent set of expectations. As a cloud-reliant organization, XXAXX's effective security posture depends heavily on how well it configures, governs, and oversees the cloud services it consumes, in addition to the controls its cloud providers themselves operate.

## 2. Scope

This Policy applies to all cloud services (IaaS, PaaS, SaaS) used by XXAXX to store, process, or transmit business data, whether procured centrally by IT or adopted by individual business functions. It applies to IT Operations, Information Security, Development/DevOps teams, and all employees who provision, administer, or use cloud services on XXAXX's behalf.

## 3. Definitions

- **IaaS (Infrastructure as a Service)**: Cloud service providing virtualized computing infrastructure (compute, storage, networking) managed by the customer.
- **PaaS (Platform as a Service)**: Cloud service providing a managed platform (e.g., managed databases, application runtimes) on which customers deploy applications.
- **SaaS (Software as a Service)**: Cloud service providing complete, provider-managed applications accessed by customers.
- **Shared Responsibility Model**: The division of security responsibility between a cloud provider and its customer, which varies by service type (IaaS, PaaS, SaaS) and specific service.
- **CSPM (Cloud Security Posture Management)**: Tooling that continuously assesses cloud environments for misconfiguration and compliance deviations.
- **CASB (Cloud Access Security Broker)**: A control point (or capability) that enforces security policies between users and cloud service providers, often used to discover and govern unsanctioned ("shadow IT") cloud use.
- **Shadow IT**: Cloud services adopted and used without going through XXAXX's formal approval and security assessment process.

## 4. Policy Statement

### 4.1 Shared Responsibility Model

For every cloud service in use, XXAXX identifies and documents where provider responsibility ends and XXAXX's own responsibility begins, based on the service type (IaaS/PaaS/SaaS) and the specific provider's shared responsibility model. This determination explicitly covers, at minimum: data encryption and key management (per the Cryptography & Key Management Policy), identity and access management, network configuration, backup (per the Backup & Disaster Recovery Policy), patching (for IaaS operating systems and above), and logging/monitoring (per the Logging & Monitoring Policy) — since assuming the provider handles something it does not is one of the most common sources of cloud security gaps.

### 4.2 Cloud Service Approval and Onboarding

New cloud services are approved through XXAXX's supplier due diligence process before being adopted for business use, per the Supplier & Third-Party Security Policy, including assessment of the provider's security certifications, data residency options, sub-processor transparency, and shared responsibility boundaries. Use of unapproved cloud services ("shadow IT") to process XXAXX business data is prohibited under the Acceptable Use Policy, and XXAXX uses discovery tooling (e.g., CASB, network/proxy logs, expense report review) where feasible to identify unsanctioned cloud use.

### 4.3 Identity and Access Management for Cloud Services

Access to cloud services follows the same least-privilege and identity governance principles as on-premises systems, per the Access Control Policy, with federated identity/single sign-on used wherever possible to centralize authentication and enforcement of the Multi-Factor Authentication Policy, rather than relying on cloud-service-local credentials. Cloud administrative/console access is treated as privileged access and subject to enhanced controls accordingly.

### 4.4 Secure Configuration and Posture Management

Cloud environments are configured according to documented security baselines (e.g., aligned to CIS Benchmarks or provider-specific hardening guides) covering identity, network, storage, and logging configuration. XXAXX uses CSPM tooling, where proportionate to its cloud footprint, to continuously detect misconfiguration (e.g., publicly exposed storage, overly permissive security groups, disabled logging) and tracks identified issues to remediation per the Vulnerability Management Policy's severity-based approach.

### 4.5 Data Protection in the Cloud

Data stored or processed in cloud services is classified and handled per the Data Classification & Handling Policy, encrypted at rest and in transit per the Cryptography & Key Management Policy, and subject to explicit determination of data residency and cross-border transfer implications, particularly for personal data, consistent with applicable data protection law.

### 4.6 Network Architecture and Segmentation

Cloud network architecture follows the segmentation and least-privilege connectivity principles defined in the Network Security Policy, using private connectivity between services where feasible, and avoiding unnecessary public exposure of cloud resources.

### 4.7 Container and Serverless Security

Where XXAXX uses containerized or serverless architectures, container images are scanned for known vulnerabilities and malware prior to deployment per the Secure Development Policy and Malware & Endpoint Protection Policy, base images are kept current and minimized, and serverless functions are configured with least-privilege execution roles rather than broad, standing permissions.

### 4.8 Logging and Monitoring

Cloud control-plane and data-plane logs (e.g., administrative activity, API calls, resource changes) are enabled, retained, and monitored consistent with the Logging & Monitoring Policy, providing visibility equivalent to on-premises environments rather than treating cloud activity as a blind spot.

### 4.9 Backup and Resilience

Backup responsibility for each cloud/SaaS service is explicitly determined under the shared responsibility model, per the Backup & Disaster Recovery Policy, with XXAXX implementing supplementary backup measures where the provider does not offer adequate native recovery capability for data XXAXX cannot afford to lose.

### 4.10 Incident Response in the Cloud

Cloud-specific incident scenarios (e.g., compromised cloud credentials, misconfigured public storage exposing data, compromised CI/CD pipeline with cloud deployment access) are addressed in the Security Incident Response Procedure's playbooks, and XXAXX ensures it retains sufficient log access and provider cooperation (per contractual terms established under the Supplier & Third-Party Security Policy) to investigate cloud-related incidents effectively.

### 4.11 Multi-Cloud and Vendor Concentration Risk

Where XXAXX relies significantly on a single cloud provider for critical services, this concentration risk is assessed under the Risk Management Policy and Business Continuity Policy, considering the feasibility and cost of multi-cloud or exit strategies for its most critical workloads, balanced against operational complexity.

### 4.12 Cloud Service Exit and Offboarding

Before adopting a cloud service for a critical function, XXAXX considers data portability and exit arrangements (e.g., data export capability, format, and any contractual notice/assistance obligations), and ensures data is retrievable and securely deleted from a provider's environment at contract termination, consistent with the Supplier & Third-Party Security Policy's offboarding requirements.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; oversees cloud security posture and shared responsibility documentation; approves cloud architecture decisions with significant security implications. |
| IT Operations / Cloud Platform Team | Implements and maintains cloud security configuration, CSPM tooling, and cloud identity federation. |
| Development / DevOps Teams | Implement secure container/serverless practices; integrate cloud security checks into CI/CD pipelines. |
| Information Security Team | Monitors cloud security alerts; performs cloud configuration reviews; supports cloud-related incident response. |
| Procurement / Supplier Management | Ensures cloud service due diligence is completed before onboarding, per the Supplier & Third-Party Security Policy. |
| All Employees | Use only approved cloud services for business data; do not provision unsanctioned cloud resources. |

## 6. Compliance and Enforcement

Provisioning of unsanctioned cloud services or resources, or deployment of cloud infrastructure that bypasses required security baselines, is a breach of this Policy. Compliance is monitored through CSPM findings, cloud access reviews, shadow IT discovery, and internal audit.

## 7. Exceptions

Exceptions to standard cloud security requirements (e.g., a temporary configuration deviation for testing) must be approved by the CISO, documented with compensating controls and an expiry date.

## 8. Review and Update

This Policy and the cloud security baseline are reviewed at least annually and upon significant change to XXAXX's cloud footprint, providers, or architecture.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Asset Management Policy (Policy #2)
- Data Classification & Handling Policy (Policy #3)
- Access Control Policy (Policy #4)
- Supplier & Third-Party Security Policy (Policy #5)
- Secure Development Policy (Policy #6)
- Vulnerability Management Policy (Policy #7)
- Security Incident Response Procedure (Policy #8a)
- Business Continuity Policy (Policy #10)
- Backup & Disaster Recovery Policy (Policy #11)
- Acceptable Use Policy (Policy #16)
- Cryptography & Key Management Policy (Policy #20)
- Network Security Policy (Policy #21)
- Multi-Factor Authentication Policy (Policy #22)
- Logging & Monitoring Policy (Policy #24)
- Malware & Endpoint Protection Policy (Policy #25)
- Cloud Security Baseline / Hardening Standard (supporting document)
- Cloud Service Inventory (operational record)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Use of cloud services / shared responsibility | Art. 21(2)(d)/(j) | Cl. 8.1 | A.5.23 (information security for use of cloud services) | GV.SC-06, PR.PS |
| Cloud service approval & shadow IT prevention | Art. 21(2)(d) | Cl. 8.1 | A.5.23, A.5.19 | GV.SC-04, ID.AM |
| Identity & access management for cloud | Art. 21(2)(i)/(j) | Cl. 8.1 | A.5.16, A.5.18, A.8.5 | PR.AA |
| Secure configuration / CSPM | Art. 21(2)(a) | Cl. 8.1 | A.8.9 (configuration management), A.5.23 | PR.PS-01 |
| Cloud data protection & residency | Art. 21(2)(h) | Cl. 8.1 | A.8.24, A.5.34 | PR.DS-01 |
| Cloud network security (cross-ref.) | Art. 21(2)(j) | Cl. 8.1 | A.8.20, A.5.23 | PR.IR-01 |
| Container / serverless security | Art. 21(2)(a)/(e) | Cl. 8.1 | A.8.28, A.8.29 | PR.PS-06 |
| Cloud logging & monitoring (cross-ref.) | Art. 21(2)(b) | Cl. 8.1 | A.8.15, A.8.16 | DE.CM |
| Cloud backup & resilience (cross-ref.) | Art. 21(2)(c) | Cl. 8.1 | A.8.13, A.5.30 | RC.RP |
| Vendor concentration risk | Art. 21(2)(d) | Cl. 6.1.2 | A.5.22 | GV.SC-06, ID.RA-10 |
| Cloud exit / data portability | Art. 21(2)(d) | Cl. 8.1 | A.5.20, A.5.11 | GV.SC-06 |
