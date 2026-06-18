# DPIA for AI Systems — Template Repository

**Bilingual (EN/FR) · GDPR Art. 35 + EU AI Act Art. 9 · Open Source**

---

A practical Data Protection Impact Assessment (DPIA) template designed specifically for AI systems. Combines the GDPR Art. 35 methodology with EU AI Act Art. 9 risk management requirements — updated for full AI Act applicability (August 2026).

Available in English and French (AIPD).

## Why this template exists

Standard DPIA templates were designed before the EU AI Act. They miss:

- AI Act risk tier classification (Annex III high-risk systems)
- AI-specific risks: bias, explainability, training data quality, automated decision-making
- The interface between GDPR Art. 35 and AI Act Art. 9 obligations
- Prior consultation triggers specific to AI deployments

This template fills that gap.

## Templates

| Language | File | Format |
|----------|------|--------|
| English | [templates/DPIA-AI-Systems-EN.md](templates/DPIA-AI-Systems-EN.md) | Markdown |
| Français | [templates/AIPD-Systemes-IA-FR.md](templates/AIPD-Systemes-IA-FR.md) | Markdown |

## Structure

Each template has 9 sections:

1. **Document Control** — version, scope, controller, DPO
2. **System Description & Processing Context** — what the AI does, what data it uses
3. **AI Act Classification** — risk tier, Annex III check, prohibited use check
4. **Necessity & Proportionality** — GDPR Art. 35(7)(b) requirements
5. **Risk Assessment** — threats to data subjects, likelihood/severity matrix
6. **AI-Specific Risk Assessment** — bias, explainability, Art. 22 ADM, data quality
7. **Measures to Address Risks** — technical + organisational + AI Act Art. 9 measures
8. **DPO & Stakeholder Consultation** — GDPR Art. 35(2), (9)
9. **Sign-off, Prior Consultation & Review Schedule** — Art. 36 trigger check

## Who this is for

- DPOs and privacy professionals deploying or procuring AI systems
- Data protection consultants advising on AI Act compliance
- Legal and compliance teams at companies subject to GDPR + AI Act
- Researchers and students studying privacy-by-design for AI

## Regulatory basis

| Requirement | Source |
|-------------|--------|
| DPIA obligation for high-risk processing | GDPR Art. 35 |
| Measures for necessity and proportionality | GDPR Art. 35(7)(b) |
| Risk assessment methodology | GDPR Art. 35(7)(c) |
| Prior consultation trigger | GDPR Art. 36 |
| AI risk management system | EU AI Act Art. 9 |
| High-risk AI system list | EU AI Act Annex III |
| Prohibited AI practices | EU AI Act Art. 5 |
| Transparency obligations | EU AI Act Art. 13 |
| CNIL AIPD methodology | CNIL guidelines (2018, updated 2024) |

## Contributing

Issues and PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

Areas where contributions are especially valuable:
- Sector-specific annexes (healthcare, finance, HR)
- Additional language versions
- Real-world test cases (anonymised)
- Updates as AI Act delegated acts and guidance are published

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE)

Free to use, adapt, and redistribute with attribution.

---

*Maintained by [Deepal Khatri](https://linkedin.com/in/deepal-khatri/) — CIPP/E certified privacy professional, Paris.*
