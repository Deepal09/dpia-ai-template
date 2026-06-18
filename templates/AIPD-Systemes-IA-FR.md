# Analyse d'Impact relative à la Protection des Données (AIPD) pour les systèmes d'IA
### RGPD Art. 35 × Règlement IA Art. 9 — Modèle combiné

---

**Version :** 1.0  
**Date :** _______________  
**Référence :** AIPD-IA-_______________  
**Responsable du traitement :** _______________  
**DPO :** _______________  
**Système / Projet :** _______________  
**Responsable de l'analyse :** _______________  
**Prochaine révision :** _______________  

---

## Comment utiliser ce modèle

Compléter les sections dans l'ordre. Les sections 2 et 5 sont spécifiques aux systèmes d'IA et n'ont pas d'équivalent dans une AIPD standard — ne pas les ignorer. Si une rubrique ne s'applique pas, indiquer N/A en précisant brièvement pourquoi.

Une AIPD est un document vivant. Prévoir une révision à chaque changement matériel du système (nouvelles données d'entraînement, nouvel usage, nouvelles juridictions, nouvelles décisions automatisées).

La méthodologie suivie est conforme aux lignes directrices du G29 (WP248 rev.01) et à la méthode CNIL (mise à jour 2024).

---

## Section 1 — Description du système et contexte du traitement

### 1.1 Que fait le système ?

Décrire en langage clair le système d'IA : son objectif, son fonctionnement, et la nature de ses sorties (prédiction, classification, recommandation, décision, contenu généré, etc.).

> _Description :_

### 1.2 Activités de traitement concernées

| Champ | Détail |
|-------|--------|
| **Finalité(s) du traitement** | |
| **Base légale (RGPD Art. 6)** | |
| **Données de catégorie particulière ? (Art. 9)** | Oui / Non — si oui, catégories et base légale complémentaire : |
| **Données relatives à des condamnations ? (Art. 10)** | Oui / Non |
| **Nombre estimé de personnes concernées** | |
| **Catégories de personnes concernées** | (ex. salariés, clients, patients, mineurs) |
| **Catégories de données personnelles traitées** | |
| **Sources des données** | (ex. bases internes, flux tiers, scraping web, saisie utilisateur) |
| **Données d'entraînement contenant des données personnelles ?** | Oui / Non — si oui, préciser : |
| **Destinataires / sous-traitants** | |
| **Transferts hors EEE ?** | Oui / Non — si oui, mécanisme (CCT, décision d'adéquation, BCR) : |
| **Durée de conservation (données d'entraînement)** | |
| **Durée de conservation (sorties / journaux)** | |
| **Décision automatisée (Art. 22) ?** | Oui / Non — si oui, voir Section 5.3 |

### 1.3 Parties prenantes

| Rôle | Nom / Équipe |
|------|-------------|
| Propriétaire du système | |
| Équipe data / ML | |
| Juridique / conformité | |
| Achats (si IA tierce) | |
| Utilisateurs finaux (internes) | |
| Personnes concernées (externes) | |

---

## Section 2 — Classification au regard du Règlement IA

> **Pourquoi cette section précède l'évaluation des risques :** Le niveau de risque au regard du Règlement IA détermine les obligations de base (système de gestion des risques Art. 9, transparence Art. 13, supervision humaine Art. 14). La classification oriente ce qui doit être évalué aux sections 4 et 5.

### 2.1 Vérification des pratiques interdites (Art. 5)

Répondre à chaque question. Si l'une des réponses est OUI, **arrêter** — le système ne peut pas être déployé dans l'UE.

| # | Question | Oui / Non |
|---|----------|-----------|
| 1 | Le système utilise-t-il des techniques subliminales pour manipuler le comportement d'une personne à son insu et lui causer un préjudice ? | |
| 2 | Exploite-t-il les vulnérabilités de groupes spécifiques (âge, handicap, situation sociale/économique) ? | |
| 3 | Est-il un système de notation sociale utilisé par une autorité publique conduisant à un traitement défavorable ? | |
| 4 | S'agit-il d'une identification biométrique à distance en temps réel dans des espaces publics à des fins répressives ? (sauf exceptions limitées) | |
| 5 | Infère-t-il des émotions en milieu professionnel ou éducatif ? | |
| 6 | Utilise-t-il la catégorisation biométrique pour inférer des attributs sensibles (origine, opinion politique, orientation sexuelle) ? | |
| 7 | Crée-t-il ou enrichit-il des bases de données de reconnaissance faciale par collecte non ciblée ? | |

**Résultat :** Toutes les réponses sont Non — passer à 2.2. Une réponse Oui — **le système est interdit par l'Art. 5 du Règlement IA. Ne pas déployer.**

### 2.2 Vérification des systèmes d'IA à haut risque (Annexe III)

Le système relève-t-il d'une des catégories suivantes ?

| Domaine — Annexe III | Concerné ? |
|----------------------|-----------|
| 1. Identification biométrique et catégorisation des personnes physiques | |
| 2. Gestion des infrastructures critiques | |
| 3. Éducation et formation professionnelle (accès, évaluation, suivi) | |
| 4. Emploi, gestion des travailleurs, accès au travail indépendant | |
| 5. Accès aux services privés essentiels et aux services et prestations publics | |
| 6. Application de la loi | |
| 7. Gestion des migrations, de l'asile et du contrôle aux frontières | |
| 8. Administration de la justice et processus démocratiques | |

**Classification Annexe III :** Concerné / Non concerné

Si concerné : le système est un **système d'IA à haut risque**. Les obligations de gestion des risques (Art. 9) s'appliquent pleinement. Continuer.

### 2.3 Niveau de risque

| Niveau | Critères | Ce système |
|--------|----------|-----------|
| **Risque inacceptable** | Relève d'une pratique interdite (Art. 5) | |
| **Haut risque** | Inscrit à l'Annexe III ou II | |
| **Risque limité** | Interaction avec des humains (chatbot), génération de contenu synthétique — obligations de transparence (Art. 50) | |
| **Risque minimal** | Aucun des cas ci-dessus | |

**Niveau de risque final (Règlement IA) :** _______________

### 2.4 Articulation avec l'obligation d'AIPD (RGPD Art. 35)

| Critère CNIL / G29 | Applicable ? |
|--------------------|-------------|
| Traitement à grande échelle de données de catégorie particulière | |
| Surveillance systématique d'espaces accessibles au public | |
| Décisions automatisées avec effets juridiques ou significatifs (Art. 22) | |
| Système d'IA à haut risque traitant des données personnelles | |
| Traitement de données de personnes vulnérables à grande échelle | |
| Croisement ou combinaison de jeux de données | |

**AIPD légalement obligatoire :** Oui / Non  
**Motif :** _______________

> Même en l'absence d'obligation légale, la réalisation de cette analyse est recommandée au titre de l'obligation de responsabilité (RGPD Art. 5(2)).

---

## Section 3 — Nécessité et proportionnalité

*L'Art. 35(7)(b) du RGPD exige d'évaluer « la nécessité et la proportionnalité des opérations de traitement au regard des finalités ».*

### 3.1 Nécessité

| Question | Réponse |
|----------|---------|
| La finalité pourrait-elle être atteinte sans traitement de données personnelles (ou avec moins de données) ? | |
| Des données anonymisées ou synthétiques pourraient-elles être utilisées à la place ? | |
| La base légale retenue est-elle la plus appropriée au regard de la finalité ? | |
| Les données collectées sont-elles limitées au strict nécessaire (Art. 5(1)(c) minimisation) ? | |
| Les données d'entraînement sont-elles filtrées pour exclure les données personnelles non nécessaires ? | |

### 3.2 Proportionnalité

| Question | Réponse |
|----------|---------|
| Les durées de conservation sont-elles justifiées et minimisées pour les données d'entraînement et les sorties ? | |
| Les personnes concernées sont-elles informées (transparence, Art. 13/14) ? | |
| Les personnes concernées disposent-elles de droits effectifs (accès, effacement, opposition, portabilité) ? | |
| Le périmètre des décisions automatisées est-il limité au nécessaire ? | |
| Des mesures préviennent-elles le détournement de finalité (utilisation des données au-delà de leur objet initial) ? | |

### 3.3 Mesures de minimisation des données

Décrire les mesures concrètes prises pour réduire les données collectées, conservées ou partagées :

> _Réponse :_

---

## Section 4 — Évaluation des risques

### 4.1 Identification des risques

Pour chaque risque, évaluer la vraisemblance (1–3) et la gravité (1–3). Score = vraisemblance × gravité.

| # | Risque pour les personnes concernées | Vraisemblance (1–3) | Gravité (1–3) | Score | Observations |
|---|--------------------------------------|--------------------|--------------:|-------|--------------|
| R1 | Accès non autorisé aux données d'entraînement ou aux sorties du modèle | | | | |
| R2 | Personne concernée ignorant le traitement par le système d'IA | | | | |
| R3 | Réidentification de données d'entraînement anonymisées | | | | |
| R4 | Profilage illicite ou inférence d'attributs sensibles | | | | |
| R5 | Impossibilité d'exercer les droits (effacement, accès) | | | | |
| R6 | Transfert hors EEE sans garanties adéquates | | | | |
| R7 | Conservation au-delà de la durée nécessaire | | | | |
| R8 | Violation ou non-conformité du sous-traitant / fournisseur | | | | |
| R9 | _[Ajouter un risque spécifique au système]_ | | | | |

**Échelle de vraisemblance :** 1 = Peu probable, 2 = Possible, 3 = Probable  
**Échelle de gravité :** 1 = Désagrément mineur, 2 = Impact significatif, 3 = Préjudice grave / irréversible  
**Score :** 1–3 Faible, 4–6 Moyen, 7–9 Élevé

### 4.2 Seuils de risque

| Score | Niveau | Action |
|-------|--------|--------|
| 1–3 | Faible | Accepter avec les contrôles standards |
| 4–6 | Moyen | Atténuer avant déploiement |
| 7–9 | Élevé | Atténuer ; si le risque résiduel reste élevé → consultation préalable (Art. 36) |

---

## Section 5 — Évaluation des risques spécifiques à l'IA

*Ces risques ne sont pas couverts par les modèles d'AIPD standard. Ils sont propres aux systèmes d'IA et requis au titre de l'Art. 9 du Règlement IA.*

### 5.1 Biais et discrimination

| Question | Réponse |
|----------|---------|
| Les données d'entraînement ont-elles été auditées pour identifier des lacunes démographiques ou des biais historiques ? | |
| Le modèle pourrait-il produire des résultats systématiquement différents pour des groupes protégés (données Art. 9 RGPD, droit à l'égalité de traitement) ? | |
| Existe-t-il un processus de détection et de correction des biais après déploiement ? | |
| Les indicateurs de performance sont-ils désagrégés par groupe démographique lorsque c'est possible ? | |

**Risque résiduel de biais :** Faible / Moyen / Élevé

### 5.2 Explicabilité et transparence

| Question | Réponse |
|----------|---------|
| Le système peut-il expliquer ses sorties aux personnes concernées en langage clair (Art. 13/14 RGPD, considérant 71) ? | |
| Peut-il expliquer ses sorties aux équipes internes à des fins d'audit ? | |
| Lorsque l'explicabilité est techniquement limitée (modèles boîte noire), quelles mesures compensatoires existent ? | |
| Les obligations de transparence de l'Art. 13 du Règlement IA sont-elles respectées (notice d'utilisation, divulgation des capacités et limites) ? | |

**Niveau d'explicabilité :** Complet / Partiel (atténué) / Limité (justifié)

### 5.3 Décision automatisée (RGPD Art. 22)

*À compléter uniquement si le système prend ou influence substantiellement des décisions à effets juridiques ou significatifs.*

| Question | Réponse |
|----------|---------|
| Le système prend-il des décisions fondées exclusivement sur un traitement automatisé ? | Oui / Non |
| Base légale du traitement Art. 22 (contrat, consentement explicite, droit de l'UE ou d'un État membre) : | |
| Quelles informations sont fournies aux personnes concernées sur la logique en jeu ? | |
| Existe-t-il un processus de révision humaine effective avant application des décisions conséquentes ? | |
| Les personnes concernées peuvent-elles contester la décision et obtenir une intervention humaine ? | |

### 5.4 Qualité et provenance des données d'entraînement

| Question | Réponse |
|----------|---------|
| La provenance des données d'entraînement est-elle documentée (source, date de collecte, base légale le cas échéant) ? | |
| Les données d'entraînement ont-elles été vérifiées pour identifier les données personnelles à exclure ou minimiser ? | |
| Existe-t-il un processus permettant aux personnes concernées de demander l'effacement de leurs données des jeux d'entraînement ? | |
| Si des jeux de données tiers sont utilisés : leur conformité RGPD a-t-elle été vérifiée ? | |

### 5.5 Supervision humaine (Règlement IA Art. 14)

| Question | Réponse |
|----------|---------|
| Un opérateur humain peut-il interrompre, corriger ou contrecarrer les sorties du système en temps réel ? | |
| Les opérateurs sont-ils formés pour reconnaître les limites et anomalies du système ? | |
| Existe-t-il un processus de repli lorsque le système produit des sorties peu fiables ? | |
| Pour les systèmes à haut risque : la supervision humaine est-elle intégrée dès la conception, et non ajoutée après coup ? | |

### 5.6 Synthèse des risques IA

| Risque IA | Niveau résiduel | Mesure d'atténuation |
|-----------|----------------|---------------------|
| Biais / discrimination | | |
| Manque d'explicabilité | | |
| Décisions automatisées Art. 22 | | |
| Qualité des données d'entraînement | | |
| Lacunes de supervision humaine | | |

---

## Section 6 — Mesures pour traiter les risques

### 6.1 Mesures techniques

| Mesure | Mise en œuvre ? | Détail |
|--------|----------------|--------|
| Chiffrement (données au repos et en transit) | | |
| Pseudonymisation des données d'entraînement | | |
| Contrôles d'accès et journaux d'audit | | |
| Techniques de confidentialité différentielle ou données synthétiques | | |
| Surveillance des sorties du modèle / détection d'anomalies | | |
| Traçabilité des données (data lineage) | | |
| Suppression automatique / application des durées de conservation | | |

### 6.2 Mesures organisationnelles

| Mesure | Mise en œuvre ? | Détail |
|--------|----------------|--------|
| Politique de gouvernance de l'IA | | |
| Contrats de sous-traitance (RGPD Art. 28) avec fournisseurs d'IA | | |
| Formation du personnel sur le Règlement IA et le RGPD | | |
| Procédure de gestion des incidents couvrant les violations liées à l'IA | | |
| Processus défini pour les demandes d'exercice des droits (incluant les sorties du modèle) | | |
| Calendrier de révision périodique de l'AIPD | | |

### 6.3 Mesures de gestion des risques — Règlement IA Art. 9 (systèmes à haut risque uniquement)

*Obligatoire pour les systèmes inscrits à l'Annexe III.*

| Exigence | Mesure mise en œuvre |
|----------|---------------------|
| Identification itérative des risques tout au long du cycle de vie | |
| Estimation et évaluation des risques par rapport aux indicateurs de performance | |
| Tests dans les conditions d'utilisation prévues et d'utilisation abusive raisonnablement prévisible | |
| Plan de surveillance post-commercialisation | |
| Procédure de signalement des incidents (Règlement IA Art. 73) | |

### 6.4 Risque résiduel après mesures

| Risque (Section 4) | Score résiduel | Acceptable ? |
|--------------------|---------------|-------------|
| R1 | | |
| R2 | | |
| R3 | | |
| R4 | | |
| R5 | | |
| R6 | | |
| R7 | | |
| R8 | | |

**Niveau de risque résiduel global :** Faible / Moyen / Élevé

Si un risque résiduel reste **Élevé** → consultation préalable de l'autorité de contrôle obligatoire (RGPD Art. 36). Aller à la Section 8.

---

## Section 7 — Consultation du DPO et des parties prenantes

*L'Art. 35(2) du RGPD impose de recueillir l'avis du DPO. L'Art. 35(9) prévoit de consulter les personnes concernées lorsque cela est approprié.*

### 7.1 Avis du DPO

| Champ | Détail |
|-------|--------|
| DPO consulté le (date) : | |
| Synthèse de l'avis du DPO : | |
| Recommandations du DPO : | |
| Recommandations mises en œuvre : | Oui / Non / Partiel — préciser : |
| Signature du DPO : | |

### 7.2 Consultation des personnes concernées

| Question | Réponse |
|----------|---------|
| Les personnes concernées ou leurs représentants ont-ils été consultés ? | Oui / Non |
| Si non : justification de l'absence de consultation : | |
| Si oui : modalités, dates et synthèse des retours : | |
| Comment les retours ont-ils été pris en compte dans la conception ? | |

### 7.3 Autres parties prenantes consultées

| Partie prenante | Date | Contribution principale |
|----------------|------|------------------------|
| DSI / Sécurité | | |
| Juridique | | |
| Équipe ML / Data Science | | |
| Responsable métier | | |
| Conseil externe / auditeur | | |

---

## Section 8 — Consultation préalable (Art. 36)

*À compléter uniquement si le risque résiduel en Section 6.4 est ÉLEVÉ.*

| Champ | Détail |
|-------|--------|
| Autorité de contrôle à consulter : | (ex. CNIL pour la France) |
| Date de soumission : | |
| Numéro de référence : | |
| Réponse / avis de l'autorité : | |
| Décision de déploiement suite à consultation : | Poursuivre / Modifier / Suspendre |

---

## Section 9 — Validation et calendrier de révision

### 9.1 Validation

| Rôle | Nom | Date | Signature |
|------|-----|------|-----------|
| Responsable de l'analyse | | | |
| DPO | | | |
| Représentant du responsable de traitement | | | |
| Juridique / conformité | | | |

### 9.2 Calendrier de révision

Cette AIPD doit être révisée si l'un des événements suivants survient :

- [ ] Modification matérielle du système d'IA (nouveau modèle, nouvelles données, nouvel usage)
- [ ] Ajout de nouvelles catégories de données personnelles
- [ ] Nouvelles personnes concernées ou nouvelles juridictions dans le périmètre
- [ ] Évolution réglementaire affectant le Règlement IA ou le RGPD
- [ ] Violation de données ou incident lié au système d'IA
- [ ] Suite à la consultation préalable
- [ ] Révision périodique planifiée (recommandée : annuelle, ou selon les exigences sectorielles)

**Prochaine révision planifiée :** _______________  
**Responsable de la révision :** _______________

### 9.3 Historique des versions

| Version | Date | Auteur | Modifications |
|---------|------|--------|--------------|
| 1.0 | | | Analyse initiale |
| | | | |

---

## Annexe A — Tableau de correspondance réglementaire

| Obligation | RGPD | Règlement IA |
|-----------|------|-------------|
| AIPD / analyse des risques obligatoire | Art. 35 | Art. 9 (IA à haut risque) |
| Nécessité et proportionnalité | Art. 35(7)(b), Art. 5(1)(c) | Art. 9(2)(a) |
| Identification et évaluation des risques | Art. 35(7)(c) | Art. 9(2)(b)(c) |
| Mesures pour traiter les risques | Art. 35(7)(d) | Art. 9(2)(d) |
| Supervision humaine | Considérant 71 | Art. 14 |
| Transparence envers les personnes concernées | Art. 13/14 | Art. 13, Art. 50 |
| Décisions automatisées individuelles | Art. 22 | Art. 9, Art. 14 |
| Consultation du DPO | Art. 35(2) | — |
| Consultation préalable (autorité de contrôle) | Art. 36 | Art. 9(9) |
| Surveillance post-commercialisation | — | Art. 72 |

## Annexe B — Glossaire

| Terme | Définition |
|-------|-----------|
| Système d'IA | Système à base de machine conçu pour fonctionner avec différents niveaux d'autonomie et générant des sorties telles que des prédictions, recommandations, décisions ou contenus (Règlement IA Art. 3(1)) |
| Système d'IA à haut risque | Système d'IA inscrit à l'Annexe III du Règlement IA, ou utilisé comme composant de sécurité d'un produit inscrit à l'Annexe II |
| AIPD | Analyse d'Impact relative à la Protection des Données — analyse systématique des traitements susceptibles d'engendrer un risque élevé (RGPD Art. 35) |
| Profilage | Toute forme de traitement automatisé visant à évaluer des aspects personnels (RGPD Art. 4(4)) |
| Décision exclusivement automatisée | Décision fondée exclusivement sur un traitement automatisé, sans intervention humaine significative (RGPD Art. 22) |
| Consultation préalable | Consultation obligatoire de l'autorité de contrôle avant traitement lorsque le risque résiduel reste élevé après atténuation (RGPD Art. 36) |
| Surveillance post-commercialisation | Collecte et analyse systématiques des retours d'expérience après déploiement du système d'IA (Règlement IA Art. 72) |
| CNIL | Commission Nationale de l'Informatique et des Libertés — autorité de contrôle française compétente en matière de RGPD |

---

*Modèle version 1.0 — Juin 2026*  
*Sous licence [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)*  
*Source : [github.com/deepal-khatri/dpia-ai-template](https://github.com/deepal-khatri/dpia-ai-template)*
