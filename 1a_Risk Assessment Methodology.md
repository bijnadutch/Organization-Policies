# Risk Assessment Methodology
**XXAXX — Supporting Document to Policy #1 (Risk Management Policy)**

---

## Document Control

| Field | Value |
|---|---|
| Document Title | Risk Assessment Methodology |
| Organization | XXAXX |
| Document Owner | Chief Information Security Officer (CISO) |
| Approved By | CISO (technical standard; endorsed by Management Body) |
| Classification | Internal |
| Version | 1.0 |
| Effective Date | [DATE] |
| Next Review Date | [DATE + 12 months] |
| Review Cycle | Annual, or upon material change to risk criteria |
| Parent Policy | Risk Management Policy (Policy #1) |

### Revision History

| Version | Date | Author | Summary of Changes |
|---|---|---|---|
| 1.0 | [DATE] | CISO | Initial version |

---

## Table of Contents

1. [Purpose](#1-purpose)
2. [Scope](#2-scope)
3. [Likelihood Scale](#3-likelihood-scale)
4. [Impact Scale](#4-impact-scale)
5. [Risk Scoring Matrix](#5-risk-scoring-matrix)
6. [Risk Rating Bands and Required Response](#6-risk-rating-bands-and-required-response)
7. [Risk Appetite and Tolerance](#7-risk-appetite-and-tolerance)
8. [Escalation and Acceptance Authority](#8-escalation-and-acceptance-authority)
9. [Inherent vs. Residual Risk](#9-inherent-vs-residual-risk)
10. [Worked Example](#10-worked-example)
11. [Review and Update](#11-review-and-update)
12. [Appendix A — Regulatory & Standards Mapping](#appendix-a--regulatory--standards-mapping)

---

## 1. Purpose

This document defines the standardized methodology XXAXX uses to assess and rate information security and cybersecurity risks under the Risk Management Policy. It ensures risk ratings are consistent, comparable, and repeatable across teams, systems, and time, regardless of who performs the assessment.

## 2. Scope

This methodology applies to every risk entered into XXAXX's risk register, including risks identified through asset reviews, vulnerability management, audits, incidents, supplier assessments, and business impact analysis. It is used consistently by all topic-specific policy owners when assessing risks within their domain.

## 3. Likelihood Scale

Likelihood reflects the probability that a given threat will exploit a given vulnerability within the next 12 months, considering existing controls.

| Level | Label | Description | Indicative Frequency |
|---|---|---|---|
| 1 | Rare | Would only occur in exceptional circumstances | Less than once in 5 years |
| 2 | Unlikely | Could occur at some point | Once in 2–5 years |
| 3 | Possible | Might occur at some point | Once in 1–2 years |
| 4 | Likely | Will probably occur in most circumstances | Once or more per year |
| 5 | Almost Certain | Expected to occur in most circumstances | Multiple times per year |

## 4. Impact Scale

Impact is assessed across seven dimensions. The overall impact rating for a risk is the **highest** rating scored across any single dimension (a "worst-dimension" approach), to avoid understating risk through averaging.

| Level | Label | Confidentiality | Integrity | Availability | Financial | Operational | Legal / Regulatory | Reputational |
|---|---|---|---|---|---|---|---|---|
| 1 | Negligible | No sensitive data exposed | No data alteration | No disruption | < [X] | No noticeable impact | No breach | No noticeable impact |
| 2 | Minor | Limited internal data exposed | Minor, correctable data error | Disruption < 1 hour, single team | [X]–[Y] | Localized, short-term | Minor non-reportable issue | Limited, internal only |
| 3 | Moderate | Confidential/internal data exposed | Data error affecting a process | Disruption of hours, single service | [Y]–[Z] | Noticeable, contained | Reportable to regulator, no fine expected | Local/customer-visible, recoverable |
| 4 | Major | Sensitive personal/customer data exposed | Significant data corruption | Disruption of a day+, multiple services | [Z]–[W] | Significant, cross-team | Regulatory investigation, possible fine | Regional/national media attention |
| 5 | Severe | Large-scale sensitive data breach | Widespread, hard-to-reverse corruption | Extended outage of essential/important service, multi-day | > [W] | Organization-wide, extended recovery | Significant fine, sanctions, management liability | Sustained national/international damage |

*Note: XXAXX finalizes the financial thresholds [X]/[Y]/[Z]/[W] based on its own turnover and risk appetite; these are intentionally left as placeholders for the CISO and Finance to populate.*

## 5. Risk Scoring Matrix

The raw risk score is calculated as: **Risk Score = Likelihood (1–5) × Impact (1–5)**, producing a score between 1 and 25.

| Likelihood ↓ / Impact → | 1 Negligible | 2 Minor | 3 Moderate | 4 Major | 5 Severe |
|---|---|---|---|---|---|
| **5 Almost Certain** | 5 | 10 | 15 | 20 | 25 |
| **4 Likely** | 4 | 8 | 12 | 16 | 20 |
| **3 Possible** | 3 | 6 | 9 | 12 | 15 |
| **2 Unlikely** | 2 | 4 | 6 | 8 | 10 |
| **1 Rare** | 1 | 2 | 3 | 4 | 5 |

## 6. Risk Rating Bands and Required Response

| Score Range | Rating | Required Response |
|---|---|---|
| 1–4 | **Low** | Accept and monitor; no mandatory treatment plan; re-assess at next scheduled cycle. |
| 5–9 | **Medium** | Treatment plan recommended within 90 days; owner assigned; reviewed quarterly. |
| 10–15 | **High** | Treatment plan mandatory within 30 days; reported to CISO; reviewed monthly; acceptance requires Risk Owner + CISO sign-off. |
| 16–25 | **Critical** | Immediate treatment plan and interim compensating controls required; reported to Management Body within 5 business days; reviewed continuously until reduced; acceptance requires Management Body sign-off. |

## 7. Risk Appetite and Tolerance

XXAXX's management body defines and periodically reaffirms the organization's risk appetite: the maximum level of risk XXAXX is willing to accept in pursuit of its objectives, expressed per risk category (e.g., data protection, operational resilience, third-party/supply chain, financial).

- **Default tolerance**: Risks rated Low or Medium fall within standing tolerance and may be managed at operational level.
- **Reduced tolerance areas**: For risks affecting essential service delivery, personal data at scale, or critical third parties, the tolerance threshold is one band lower (e.g., a Medium-rated risk in these categories is treated as High).
- Risk appetite statements and category-specific thresholds are maintained in a separate Risk Appetite Statement, reviewed and approved annually by the management body.

## 8. Escalation and Acceptance Authority

| Risk Rating | Assessment Reviewed By | Acceptance Authority |
|---|---|---|
| Low | Risk Owner | Risk Owner |
| Medium | Risk Owner + Policy Owner | Risk Owner |
| High | CISO | Risk Owner + CISO |
| Critical | CISO + Management Body | Management Body |

Acceptance of any risk above standing tolerance must be documented in the risk register with rationale, compensating controls (if any), an expiry/review date, and named sign-off.

## 9. Inherent vs. Residual Risk

Every risk entry records both:

- **Inherent risk**: the likelihood × impact score assuming no controls are in place;
- **Residual risk**: the likelihood × impact score after accounting for existing and planned controls.

Treatment plans target a defined reduction in residual risk and are considered complete only once the residual score is verified (e.g., through testing, audit, or control evidence) rather than assumed.

## 10. Worked Example

**Risk**: Unpatched critical vulnerability on an internet-facing application server.

- Inherent Likelihood: 4 (Likely) — actively exploited vulnerability class, internet-facing.
- Inherent Impact: 4 (Major) — server processes customer data; potential service disruption.
- Inherent Score: 4 × 4 = 16 → **Critical**.
- Treatment: Emergency patching within 72 hours; WAF rule as interim compensating control; network segmentation review.
- Residual Likelihood (post-treatment): 2 (Unlikely).
- Residual Impact: 3 (Moderate) — reduced blast radius due to segmentation.
- Residual Score: 2 × 3 = 6 → **Medium**, within standing tolerance once verified.

## 11. Review and Update

This methodology is reviewed at least annually alongside the Risk Management Policy, and whenever the risk scoring approach, impact thresholds, or escalation authorities change materially.

---

## Appendix A — Regulatory & Standards Mapping

| Topic / Section | NIS2 Directive | ISO/IEC 27001:2022 | ISO/IEC 27002:2022 | NIST CSF v2.0 |
|---|---|---|---|---|
| Risk assessment methodology | Art. 21(2)(a) | Cl. 6.1.2 | A.5.1 | ID.RA-01 |
| Likelihood & impact criteria | Art. 21(1) | Cl. 6.1.2(a)–(b) | A.5.1 | GV.RM-02 |
| Risk scoring & rating bands | Art. 21(2)(a) | Cl. 6.1.2(c)–(d) | A.5.1 | ID.RA-05 |
| Risk appetite & tolerance | Art. 21(1) | Cl. 6.1.2(a) | A.5.1 | GV.RM-01, GV.RM-02 |
| Escalation & acceptance authority | Art. 20(1); Art. 21(2)(f) | Cl. 6.1.3(e), 5.3 | A.5.2, A.5.3 | GV.RM-04 |
| Inherent vs. residual risk tracking | Art. 21(2)(a) | Cl. 6.1.3, 8.3 | A.5.1 | ID.RA-06 |
