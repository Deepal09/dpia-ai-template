# Data Protection Impact Assessment (DPIA) for AI Systems
### GDPR Art. 35 × EU AI Act Art. 9 - Combined Template

---

**Version:** 1.0  
**Date:** _______________  
**Reference number:** DPIA-AI-_______________  
**Controller:** _______________  
**DPO:** _______________  
**System / Project name:** _______________  
**Assessment lead:** _______________  
**Next review date:** _______________  

---

## How to use this template

Complete each section sequentially. Sections 3 and 6 are specific to AI systems and have no equivalent in a standard DPIA - do not skip them. Where a field does not apply, write N/A and briefly explain why.

A completed DPIA is a living document. Schedule a review whenever the AI system changes materially (new training data, new use case, new jurisdictions, new automated decisions).

---

## Section 1 — System Description & Processing Context

### 1.1 What does the system do?

Provide a plain-language description of the AI system: its purpose, how it works, and what it produces as output (prediction, classification, recommendation, decision, generated content, etc.).

> _Description:_

### 1.2 Processing activities involved

| Field | Detail |
|-------|--------|
| **Purpose(s) of processing** | |
| **Legal basis (GDPR Art. 6)** | |
| **Special category data? (Art. 9)** | Yes / No - if yes, which categories and additional legal basis: |
| **Criminal data? (Art. 10)** | Yes / No |
| **Estimated number of data subjects** | |
| **Categories of data subjects** | (e.g., employees, customers, patients, minors) |
| **Categories of personal data processed** | |
| **Data sources** | (e.g., internal databases, third-party feeds, web scraping, user input) |
| **Training data includes personal data?** | Yes / No - if yes, describe: |
| **Recipients / processors** | |
| **Third-country transfers?** | Yes / No - if yes, transfer mechanism (SCCs, adequacy decision, BCRs): |
| **Retention period (training data)** | |
| **Retention period (outputs / logs)** | |
| **Automated decision-making (Art. 22)?** | Yes / No - if yes, see Section 6.4 |

### 1.3 Stakeholders involved

| Role | Name / Team |
|------|------------|
| System owner | |
| Data engineering / ML team | |
| Legal / compliance | |
| Procurement (if third-party AI) | |
| End users (internal) | |
| Affected data subjects (external) | |

---

## Section 2 - AI Act Classification

> **Why this section comes before risk assessment:** The AI Act risk tier determines the baseline obligations (Art. 9 risk management system, Art. 13 transparency, Art. 14 human oversight). Knowing the tier shapes what you must assess in Sections 4 and 5.

### 2.1 Prohibited practices check (Art. 5)

Answer each question. If any answer is YES, **stop** - the system cannot be deployed under EU law.

| # | Question | Yes / No |
|---|----------|----------|
| 1 | Does the system use subliminal techniques to manipulate behaviour without the person's awareness in a way that causes harm? | |
| 2 | Does it exploit vulnerabilities of specific groups (age, disability, social/economic situation)? | |
| 3 | Is it a social scoring system by a public authority used to detrimental treatment? | |
| 4 | Is it real-time remote biometric identification in public spaces for law enforcement? (with limited exceptions) | |
| 5 | Does it infer emotions in workplace or educational settings? | |
| 6 | Does it use biometric categorisation to infer sensitive attributes (race, political opinion, sexual orientation)? | |
| 7 | Does it create or expand facial recognition databases through untargeted scraping? | |

**Result:** All No - proceed to 2.2. Any Yes — **system is prohibited under AI Act Art. 5. Do not deploy.**

### 2.2 High-risk AI system check (Annex III)

Does the system fall into any of these categories?

| Annex III Area | In scope? |
|---------------|----------|
| 1. Biometric identification and categorisation of natural persons | |
| 2. Management and operation of critical infrastructure | |
| 3. Education and vocational training (access, assessment, monitoring) | |
| 4. Employment, workers management, access to self-employment | |
| 5. Access to and enjoyment of essential private services and public services and benefits | |
| 6. Law enforcement | |
| 7. Migration, asylum and border control management | |
| 8. Administration of justice and democratic processes | |

**Annex III classification:** In scope / Not in scope

If in scope: the system is a **high-risk AI system**. AI Act Art. 9 risk management obligations apply in full. Continue.

If not in scope: determine limited-risk or minimal-risk below.

### 2.3 Risk tier

| Tier | Criteria | This system? |
|------|----------|-------------|
| **Unacceptable risk** | Meets any Art. 5 prohibited practice | |
| **High risk** | Listed in Annex III or Annex II | |
| **Limited risk** | Interacts with humans (chatbot), generates synthetic content - transparency obligations apply (Art. 50) | |
| **Minimal risk** | None of the above | |

**Final AI Act tier:** _______________

### 2.4 Interaction with GDPR Art. 35

| Trigger | Applies? |
|---------|---------|
| Large-scale processing of special category data | |
| Systematic monitoring of publicly accessible areas | |
| Automated decision-making with legal/significant effects (Art. 22) | |
| High-risk AI system AND processes personal data | |
| Processing of data of vulnerable persons at scale | |

**DPIA legally required:** Yes / No  
**Reason:** _______________

> Even where not legally required, completing this assessment is recommended as an accountability measure under GDPR Art. 5(2).

---

## Section 3 - Necessity & Proportionality

*GDPR Art. 35(7)(b) requires assessing "the necessity and proportionality of the processing operations in relation to the purposes."*

### 3.1 Necessity

| Question | Response |
|----------|----------|
| Could the purpose be achieved without processing personal data (or with less)? | |
| Could it be achieved with anonymised or synthetic data instead? | |
| Is the legal basis the most appropriate one for this purpose? | |
| Is the data collected limited to what is necessary (Art. 5(1)(c) minimisation)? | |
| Is training data filtered to exclude irrelevant personal data? | |

### 3.2 Proportionality

| Question | Response |
|----------|----------|
| Are retention periods justified and minimised for both training data and outputs? | |
| Are data subjects informed (transparency, Art. 13/14)? | |
| Do data subjects have meaningful rights (access, erasure, objection, portability)? | |
| Is the scope of automated decision-making limited to what is necessary? | |
| Are measures in place to prevent function creep (using data beyond original purpose)? | |

### 3.3 Data minimisation measures

Describe specific measures taken to reduce data collected, retained, or shared:

> _Response:_

---

## Section 4 - Risk Assessment

### 4.1 Risk identification

For each risk, assess likelihood (1–3) and severity (1–3). Risk score = likelihood × severity.

| # | Risk to data subjects | Likelihood (1–3) | Severity (1–3) | Score | Notes |
|---|-----------------------|-----------------|---------------|-------|-------|
| R1 | Unauthorised access to training data or model outputs | | | | |
| R2 | Data subject unaware of AI-mediated processing | | | | |
| R3 | Re-identification of anonymised training data | | | | |
| R4 | Unlawful profiling or inference of sensitive attributes | | | | |
| R5 | Inability to exercise data subject rights (erasure, access) | | | | |
| R6 | Cross-border transfer without adequate safeguards | | | | |
| R7 | Retention beyond necessity | | | | |
| R8 | Processor / vendor breach or non-compliance | | | | |
| R9 | _[Add system-specific risk]_ | | | | |

**Likelihood scale:** 1 = Remote, 2 = Possible, 3 = Likely  
**Severity scale:** 1 = Minor inconvenience, 2 = Significant impact, 3 = Severe / irreversible harm  
**Score:** 1-3 Low, 4-6 Medium, 7-9 High

### 4.2 Risk threshold

| Score range | Level | Action |
|-------------|-------|--------|
| 1-3 | Low | Accept with standard controls |
| 4-6 | Medium | Mitigate before deployment |
| 7-9 | High | Mitigate; if residual risk remains high -> prior consultation (Art. 36) |

---

## Section 5 - AI-Specific Risk Assessment

*These risks are not covered by standard DPIA templates. They are specific to AI systems and required under AI Act Art. 9.*

### 5.1 Bias and discrimination

| Question | Response |
|----------|----------|
| Has training data been audited for demographic gaps or historical bias? | |
| Could the model produce systematically different outcomes for protected groups (GDPR Art. 9 categories, equal treatment law)? | |
| Is there a process to detect and remediate bias post-deployment? | |
| Are performance metrics disaggregated by demographic group where feasible? | |

**Residual bias risk:** Low / Medium / High

### 5.2 Explainability and transparency

| Question | Response |
|----------|----------|
| Can the system explain its outputs to data subjects in plain language (Art. 13/14, GDPR recital 71)? | |
| Can it explain outputs to internal teams for auditing? | |
| Where explainability is technically limited (black-box models), what compensating measures exist? | |
| Are AI Act Art. 13 transparency obligations met (instructions for use, capabilities and limitations disclosure)? | |

**Explainability level:** Full / Partial (mitigated) / Limited (justified)

### 5.3 Automated decision-making (GDPR Art. 22)

*Complete only if the system makes or substantially influences decisions with legal or similarly significant effects.*

| Question | Response |
|----------|----------|
| Does the system make solely automated decisions affecting data subjects? | Yes / No |
| Legal basis for Art. 22 processing (contract, explicit consent, Union/Member State law): | |
| What information is provided to data subjects about the logic involved? | |
| Is there a meaningful human review process before consequential decisions are enforced? | |
| Can data subjects contest the decision and obtain human intervention? | |

### 5.4 Training data quality and provenance

| Question | Response |
|----------|----------|
| Is the provenance of training data documented (source, collection date, consent basis if applicable)? | |
| Has training data been reviewed for personal data that should be excluded or minimised? | |
| Is there a process for data subjects to request erasure of their data from training sets? | |
| If third-party datasets are used: have they been assessed for GDPR compliance? | |

### 5.5 Human oversight (AI Act Art. 14)

| Question | Response |
|----------|----------|
| Can a human operator halt, override, or correct the system's outputs in real time? | |
| Are operators trained to recognise system limitations and anomalies? | |
| Is there a fallback process for when the system produces unreliable outputs? | |
| For high-risk AI systems: is human oversight built into the deployment design, not added as an afterthought? | |

### 5.6 AI-specific risk summary

| AI Risk | Residual Level | Mitigation measure |
|---------|---------------|-------------------|
| Bias / discrimination | | |
| Lack of explainability | | |
| Art. 22 automated decisions | | |
| Training data quality | | |
| Human oversight gaps | | |

---

## Section 6 -- Measures to Address Risks

### 6.1 Technical measures

| Measure | Implemented? | Detail |
|---------|-------------|--------|
| Encryption (data at rest and in transit) | | |
| Pseudonymisation of training data | | |
| Access controls and audit logs | | |
| Differential privacy or synthetic data techniques | | |
| Model output monitoring / anomaly detection | | |
| Data lineage tracking | | |
| Automated deletion / retention enforcement | | |

### 6.2 Organisational measures

| Measure | Implemented? | Detail |
|---------|-------------|--------|
| AI governance policy | | |
| Data processor agreements (GDPR Art. 28) with AI vendors | | |
| Staff training on AI Act and GDPR obligations | | |
| Incident response procedure covering AI-related breaches | | |
| Defined process for data subject rights requests (including model outputs) | | |
| Regular DPIA review cadence | | |

### 6.3 AI Act Art. 9 risk management measures (high-risk systems only)

*Required for Annex III systems.*

| Requirement | Measure implemented |
|-------------|-------------------|
| Iterative risk identification throughout lifecycle | |
| Risk estimation and evaluation against performance metrics | |
| Testing against intended purpose and reasonably foreseeable misuse | |
| Post-market monitoring plan | |
| Incident reporting procedure (AI Act Art. 73) | |

### 6.4 Residual risk after measures

| Risk (from Section 4) | Residual score | Acceptable? |
|-----------------------|---------------|------------|
| R1 | | |
| R2 | | |
| R3 | | |
| R4 | | |
| R5 | | |
| R6 | | |
| R7 | | |
| R8 | | |

**Overall residual risk level:** Low / Medium / High

If any residual risk remains **High** -> prior consultation with supervisory authority required (GDPR Art. 36). Go to Section 8.

---

## Section 7 - DPO & Stakeholder Consultation

*GDPR Art. 35(2) requires seeking the advice of the DPO. Art. 35(9) requires seeking the views of data subjects where appropriate.*

### 7.1 DPO advice

| Field | Detail |
|-------|--------|
| DPO consulted on (date): | |
| DPO opinion summary: | |
| DPO recommendations: | |
| Recommendations implemented: | Yes / No / Partial - explain: |
| DPO signature: | |

### 7.2 Data subject consultation

| Question | Response |
|----------|----------|
| Were data subjects or their representatives consulted? | Yes / No |
| If no: justification for not consulting: | |
| If yes: method of consultation, dates, and summary of feedback: | |
| How was feedback incorporated into the design? | |

### 7.3 Other stakeholders consulted

| Stakeholder | Date | Key input |
|------------|------|-----------|
| IT / Security | | |
| Legal | | |
| ML / Data Science team | | |
| Business owner | | |
| External counsel / auditor | | |

---

## Section 8 - Prior Consultation (Art. 36)

*Complete only if residual risk in Section 6.4 is HIGH.*

| Field | Detail |
|-------|--------|
| Supervisory authority to consult: | (e.g., CNIL for France) |
| Date submitted: | |
| Reference number: | |
| Authority response / opinion: | |
| Deployment decision following consultation: | Proceed / Modify / Halt |

---

## Section 9 - Sign-off & Review Schedule

### 9.1 Approval

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Assessment lead | | | |
| DPO | | | |
| Controller representative | | | |
| Legal / compliance | | | |

### 9.2 Review schedule

This DPIA must be reviewed if any of the following occur:

- [ ] Material change to the AI system (new model, new training data, new use case)
- [ ] New categories of personal data added
- [ ] New data subjects or jurisdictions in scope
- [ ] Regulatory change affecting AI Act or GDPR obligations
- [ ] Data breach or AI incident involving this system
- [ ] Prior consultation outcome requires reassessment
- [ ] Scheduled review (recommended: annually, or as required by sector regulation)

**Next scheduled review:** _______________  
**Review owner:** _______________

### 9.3 Version history

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | | | Initial assessment |
| | | | |

---

## Annex A - Regulatory Cross-Reference

| Obligation | GDPR | EU AI Act |
|-----------|------|-----------|
| DPIA / risk assessment required | Art. 35 | Art. 9 (high-risk AI) |
| Necessity and proportionality | Art. 35(7)(b), Art. 5(1)(c) | Art. 9(2)(a) |
| Risk identification and evaluation | Art. 35(7)(c) | Art. 9(2)(b)(c) |
| Measures to address risks | Art. 35(7)(d) | Art. 9(2)(d) |
| Human oversight | Recital 71 | Art. 14 |
| Transparency to data subjects | Art. 13/14 | Art. 13, Art. 50 |
| Automated individual decisions | Art. 22 | Art. 9, Art. 14 |
| DPO consultation | Art. 35(2) | — |
| Prior consultation (supervisory authority) | Art. 36 | Art. 9(9) |
| Post-market monitoring | — | Art. 72 |

## Annex B - Glossary

| Term | Definition |
|------|-----------|
| AI system | A machine-based system designed to operate with varying levels of autonomy that generates outputs such as predictions, recommendations, decisions, or content (EU AI Act Art. 3(1)) |
| High-risk AI system | An AI system listed in Annex III of the EU AI Act, or used as safety component of a product listed in Annex II |
| DPIA | Data Protection Impact Assessment - systematic analysis of processing likely to result in high risk (GDPR Art. 35) |
| Profiling | Any form of automated processing of personal data to evaluate personal aspects (GDPR Art. 4(4)) |
| Solely automated decision | A decision based exclusively on automated processing, without meaningful human involvement (GDPR Art. 22) |
| Prior consultation | Mandatory consultation of the supervisory authority before processing where residual risk remains high after mitigation (GDPR Art. 36) |
| Post-market monitoring | Systematic collection and review of experience gained from AI systems after deployment (AI Act Art. 72) |

---

*Template version 1.0 - June 2026*  
*Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*  
*Source: [github.com/deepal-khatri/dpia-ai-template](https://github.com/deepal-khatri/dpia-ai-template)*
