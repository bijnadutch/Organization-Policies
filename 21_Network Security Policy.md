# Network Security Policy
**XXAXX — Policy #21 (Technological)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Network Security Policy |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) / Head of IT Operations |
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

This Policy defines how XXAXX designs, segments, protects, and monitors its network infrastructure — on-premises and cloud — to prevent unauthorized access, limit the spread of a compromise, and maintain the availability and integrity of network-dependent services.

## 2. Scope

This Policy applies to all XXAXX-owned or -operated network infrastructure, including local area networks (LAN), wireless networks, wide area network (WAN) connectivity, cloud virtual networks, and any network boundary between XXAXX and external parties (internet, suppliers, partners). It applies to IT Operations, Information Security, and any third party managing network infrastructure on XXAXX's behalf.

## 3. Definitions

- **Network Segmentation**: Dividing a network into distinct zones to limit the ability of a threat to move laterally between systems.
- **Firewall**: A network security control that enforces rules governing permitted traffic between network zones.
- **DMZ (Demilitarized Zone)**: A network segment that exposes external-facing services while isolating them from the internal network.
- **IDS/IPS (Intrusion Detection/Prevention System)**: A control that monitors network traffic for malicious activity and, in the case of IPS, can automatically block it.
- **VPN (Virtual Private Network)**: A technology providing an encrypted connection over an untrusted network.
- **Zero Trust**: A security model that does not implicitly trust any user or device based on network location alone, requiring continuous verification.

## 4. Policy Statement

### 4.1 Network Architecture and Segmentation

XXAXX's network is segmented into distinct zones based on trust level, function, and data sensitivity (e.g., corporate/user network, server/data zones, DMZ for external-facing services, guest network, OT/IoT network where applicable), with traffic between zones controlled through firewalls or equivalent controls enforcing least-privilege connectivity. Critical systems and systems processing Confidential/Restricted data are placed in more restricted segments, with access from lower-trust zones limited to what is explicitly required.

### 4.2 Perimeter and Boundary Protection

Boundaries between XXAXX's network and external networks (the internet, supplier connections, partner networks) are protected by firewalls configured on a default-deny basis, permitting only explicitly required traffic. Firewall rule sets are documented, reviewed periodically to remove unnecessary or overly permissive rules, and changes follow the Change Management Policy.

### 4.3 Wireless Network Security

Corporate wireless networks use strong, current encryption and authentication standards (e.g., WPA2-Enterprise or WPA3), with separate, isolated guest wireless networks that do not have access to internal corporate systems. Default credentials on wireless infrastructure are changed before deployment.

### 4.4 Remote Access

Remote access to XXAXX's internal network is provided through approved, encrypted mechanisms (e.g., VPN, zero-trust network access) requiring multi-factor authentication, consistent with the Remote Working & BYOD Policy and Multi-Factor Authentication Policy. Split-tunneling and other configurations that could expose the internal network to a compromised remote endpoint are restricted or compensated for through additional endpoint controls.

### 4.5 Network Monitoring and Intrusion Detection

Network traffic is monitored for anomalous or malicious activity using intrusion detection/prevention capability proportionate to risk, with alerts integrated into XXAXX's logging and monitoring capability per the Logging & Monitoring Policy. Monitoring covers both perimeter traffic and, where feasible, internal (east-west) traffic to detect lateral movement.

### 4.6 Denial-of-Service Protection

Internet-facing services are protected against denial-of-service attacks through a combination of capacity planning, upstream provider/CDN-based mitigation, and rate-limiting controls proportionate to the criticality of the service, coordinated with the Business Continuity Policy for services where availability is critical.

### 4.7 Network Device Hardening

Network devices (routers, switches, firewalls, wireless access points) are configured according to a documented hardening baseline, with default credentials changed, unnecessary services disabled, and management interfaces restricted to authorized administrative access only, consistent with the Access Control Policy's privileged access requirements. Network device firmware/software is kept current per the Vulnerability Management Policy.

### 4.8 Cloud Network Security

Cloud virtual networks are configured with segmentation and access control equivalent in rigor to on-premises networks — including security groups/network ACLs restricting traffic to the minimum required, private connectivity for internal service-to-service communication where feasible, and avoidance of unnecessarily broad public exposure of cloud resources. Cloud network configuration is reviewed through cloud security posture management tooling to detect misconfiguration, coordinated with the Cloud Security Policy.

### 4.9 Third-Party and Supplier Network Connections

Network connections to suppliers or partners are limited to the minimum access required for the business purpose, documented, and reviewed periodically, consistent with the Supplier & Third-Party Security Policy. Connections no longer required are decommissioned promptly.

### 4.10 Network Access Control

Devices connecting to XXAXX's internal network are subject to network access control mechanisms, where feasible, to verify device identity/compliance (e.g., managed device status, up-to-date security posture) before granting network access, reducing risk from unmanaged or non-compliant devices.

## 5. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Head of IT Operations | Owns day-to-day network infrastructure operations; maintains network architecture documentation. |
| CISO | Owns this Policy; oversees network security control effectiveness; approves significant network architecture changes affecting security posture. |
| Network / Infrastructure Engineers | Configure and maintain firewalls, segmentation, wireless infrastructure, and network monitoring tooling. |
| Information Security Team | Monitors network security alerts; supports incident response for network-based threats; reviews firewall rules and cloud network configuration. |
| All Employees | Connect only authorized devices to XXAXX networks; do not introduce unauthorized wireless access points or bypass network controls. |

## 6. Compliance and Enforcement

Introduction of unauthorized network devices (e.g., rogue wireless access points), circumvention of network segmentation, or firewall changes made outside the Change Management Policy process are treated as policy breaches. Compliance is monitored through firewall rule audits, network configuration scanning, and internal audit.

## 7. Exceptions

Exceptions to standard network security requirements (e.g., a temporary, broader firewall rule for a specific project) must be approved by the CISO or Head of IT Operations, documented with compensating controls and an expiry date, and reviewed at expiry.

## 8. Review and Update

This Policy, network architecture documentation, and firewall rule sets are reviewed at least annually and upon significant change to XXAXX's network or cloud environment.

## 9. Related Documents

- Information Security Policy (Policy #0)
- Risk Management Policy (Policy #1)
- Access Control Policy (Policy #4)
- Supplier & Third-Party Security Policy (Policy #5)
- Vulnerability Management Policy (Policy #7)
- Business Continuity Policy (Policy #10)
- Change Management Policy (Policy #13)
- Remote Working & BYOD Policy (Policy #17)
- Multi-Factor Authentication Policy (Policy #22)
- Logging & Monitoring Policy (Policy #24)
- Cloud Security Policy (Policy #26)
- Network Architecture Diagram and Firewall Rule Documentation (supporting documents)

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Network segmentation | Art. 21(2)(a)/(j) | Cl. 8.1 | A.8.22 (segregation of networks) | PR.IR-01 |
| Networks security / perimeter protection | Art. 21(2)(j) | Cl. 8.1 | A.8.20 (networks security) | PR.IR-01 |
| Security of network services | Art. 21(2)(j) | Cl. 8.1 | A.8.21 (security of network services) | PR.IR-01 |
| Wireless network security | Art. 21(2)(j) | Cl. 8.1 | A.8.20 | PR.IR-01 |
| Remote access (cross-ref.) | Art. 21(2)(i)/(j) | Cl. 8.1 | A.6.7, A.8.5 | PR.AA-03, PR.IR-01 |
| Network monitoring / IDS-IPS | Art. 21(2)(b) | Cl. 8.1 | A.8.16 (monitoring activities) | DE.CM-01 |
| DoS protection & availability | Art. 21(2)(c)/(j) | Cl. 8.1 | A.8.14, A.8.20 | PR.IR-04, RC.RP |
| Network device hardening | Art. 21(2)(a)/(j) | Cl. 8.1 | A.8.9 (configuration management), A.8.20 | PR.PS-01 |
| Cloud network security (cross-ref.) | Art. 21(2)(d)/(j) | Cl. 8.1 | A.5.23, A.8.20 | PR.IR-01, GV.SC |
| Third-party network connections (cross-ref.) | Art. 21(2)(d)/(j) | Cl. 8.1 | A.5.19, A.8.20 | GV.SC, PR.IR-01 |
