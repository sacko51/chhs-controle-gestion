# PHASE 0 - CADRAGE DU PROJET

*Données fictives construites à des fins pédagogiques et professionnelles.*

---

## 1. Présentation de CHHS

**Centre Hospitalier Horizon Santé (CHHS)** est un groupe de santé privé fictif implanté dans la région Grand Est, spécialisé dans l'offre de soins de proximité et de spécialité.

- **Statut** : société de gestion d'établissements de santé privés (SAS fictive)
- **Chiffre d'affaires consolidé N (fictif)** : environ 42 M€
- **Effectif fictif** : environ 480 ETP
- **Nombre de sites** : 3 établissements
- **Environnement économique** : secteur concurrentiel, tarification à l'activité (T2A) pour une partie des recettes, pression sur les coûts (masse salariale soignante, dispositifs médicaux, énergie), exigences croissantes de qualité et de traçabilité imposées par les tutelles.

### 1.1 Les trois sites fictifs

| Site | Localisation fictive | Vocation principale | Taille (lits/places) |
|---|---|---|---|
| CHHS Reims | Reims | Polyclinique généraliste : consultations, hospitalisation complète, bloc opératoire, imagerie | 120 lits |
| CHHS Châlons | Châlons-en-Champagne | Hospitalisation de jour, laboratoire, imagerie légère | 40 places |
| CHHS Troyes | Troyes | Consultations externes, ambulatoire, urgences de proximité | 30 places |

### 1.2 Activités du groupe

- Consultations externes (médecine générale et spécialités)
- Hospitalisation complète (chirurgie, médecine)
- Hospitalisation de jour (ambulatoire)
- Bloc opératoire
- Imagerie médicale (radiologie, échographie, scanner)
- Laboratoire d'analyses
- Urgences et soins ambulatoires (site de Troyes uniquement)

---

## 2. Organigramme

```
Direction Générale
│
├── Direction Financière
│ ├── Comptabilité
│ └── Contrôle de Gestion
│
├── Direction des Opérations Médicales
│ ├── Site Reims
│ ├── Site Châlons
│ └── Site Troyes
│
├── Direction des Ressources Humaines
│
├── Direction des Achats
│
├── Direction Informatique
│
├── Direction Qualité
│
└── Services Généraux
 ├── Maintenance
 ├── Administration des patients
 └── Facturation
```

---

## 3. Problématique

> **Comment CHHS peut-il améliorer sa performance économique et opérationnelle tout en renforçant la fiabilité de son pilotage et de son contrôle interne ?**

Cette problématique guide l'ensemble des huit étapes du projet : elle relie le diagnostic financier, l'analyse des coûts, le suivi budgétaire, le pilotage par KPI, la fiabilisation des données (audit interne), les prévisions et, enfin, le plan d'action.

---

## 4. Objectifs du projet

| Dimension | Objectif |
|---|---|
| Financier | Évaluer la rentabilité et la solidité financière du groupe sur 3 exercices |
| Opérationnel | Identifier les activités les plus et les moins performantes |
| Économique | Comprendre la structure de coûts et les leviers de productivité |
| RH | Analyser l'évolution des effectifs, de la masse salariale et de la productivité |
| Qualité | Suivre la satisfaction patient et les indicateurs de parcours |
| Contrôle interne | Sécuriser la chaîne activité → facturation → comptabilité → reporting |

---

## 5. Périmètre et périodes d'analyse

- **Périmètre** : les 3 sites de CHHS, l'ensemble des activités médicales et des fonctions support.
- **Périodes retenues** :
 - N-2 : exercice historique de référence
 - N-1 : exercice historique intermédiaire
 - N : exercice de référence (analyse détaillée)
 - N+1 : exercice de prévision (Étape 7)

---

## 6. Architecture générale des données

Le projet repose sur **un modèle de données unique** (règle de source unique), organisé en étoile : des tables de faits (mesures) reliées à des tables de dimensions (axes d'analyse).

### 6.1 Tables de dimensions

| Table | Contenu | Clé primaire |
|---|---|---|
| Dim_Date | Calendrier journalier, mois, trimestre, année, exercice (N-2/N-1/N/N+1) | ID_Date |
| Dim_Site | Les 3 sites de CHHS | ID_Site |
| Dim_Activite | Consultations, hospitalisation complète, HDJ, bloc, imagerie, laboratoire, urgences | ID_Activite |
| Dim_Service | Services cliniques et support | ID_Service |
| Dim_Employe | Effectifs fictifs (poste, service, site, statut) | ID_Employe |
| Dim_Type_Charge | Nature de charge (personnel, achats, externes, amortissements) | ID_TypeCharge |
| Dim_Fournisseur | Fournisseurs fictifs (médicaments, dispositifs médicaux, prestataires) | ID_Fournisseur |
| Dim_Patient_Fictif | Identifiants patients anonymisés, sans donnée médicale identifiante | ID_Patient |
| Dim_Centre_Cout | Centres de coûts (par service/site) | ID_CentreCout |
| Dim_Compte_Comptable | Plan comptable simplifié | ID_Compte |
| Dim_Type_Recette | Nature de recette (T2A, consultations, forfaits, autres) | ID_TypeRecette |

### 6.2 Tables de faits

| Table | Contenu | Grain |
|---|---|---|
| Fact_Activite | Volumes d'actes/séjours par activité, site, date | Jour × Site × Activité |
| Fact_CA | Chiffre d'affaires par activité, site, type de recette, date | Jour × Site × Activité × TypeRecette |
| Fact_Charges | Charges par type, centre de coût, site, date | Jour/Mois × Site × CentreCout × TypeCharge |
| Fact_Budget | Budget par site, activité, poste, période | Mois × Site × Activité × Poste |
| Fact_RH | Effectifs, ETP, masse salariale, absentéisme par employé/service/mois | Mois × Employé |
| Fact_Ecritures | Écritures comptables (journal), avec anomalies volontaires (Étape 6) | Écriture |
| Fact_Qualite | Indicateurs qualité (satisfaction, réclamations, délais) par site/mois | Mois × Site |
| Fact_Tresorerie | Flux de trésorerie mensuels | Mois × Site |

### 6.3 Relations

- `Dim_Date[ID_Date]` → toutes les tables de faits (relation 1-à-plusieurs)
- `Dim_Site[ID_Site]` → Fact_Activite, Fact_CA, Fact_Charges, Fact_Budget, Fact_Qualite, Fact_Tresorerie
- `Dim_Activite[ID_Activite]` → Fact_Activite, Fact_CA, Fact_Budget
- `Dim_Employe[ID_Employe]` → Fact_RH
- `Dim_Centre_Cout[ID_CentreCout]` → Fact_Charges
- `Dim_Compte_Comptable[ID_Compte]` → Fact_Ecritures
- `Dim_Fournisseur[ID_Fournisseur]` → Fact_Ecritures

---

## 7. Dictionnaire initial des données

| Variable | Définition | Type | Unité | Table |
|---|---|---|---|---|
| CA | Chiffre d'affaires | Numérique | € | Fact_CA |
| Volume | Nombre d'actes/séjours | Numérique | Nombre | Fact_Activite |
| Cout_Direct | Coût directement affectable à une activité | Numérique | € | Fact_Charges |
| Cout_Indirect | Coût réparti via une clé de répartition | Numérique | € | Fact_Charges |
| DMS | Durée moyenne de séjour | Numérique | Jours | Fact_Activite |
| ETP | Équivalent temps plein | Numérique | ETP | Fact_RH |
| Masse_Salariale | Coût total du personnel | Numérique | € | Fact_RH |
| Ecart_Budget | Réalisé − Budget | Numérique | € / % | Fact_Budget |
| Taux_Occupation | Volume réalisé / capacité disponible | Numérique | % | Fact_Activite |
| Tresorerie_Nette | Trésorerie disponible après dettes court terme | Numérique | € | Fact_Tresorerie |

*(Le dictionnaire complet sera enrichi à chaque étape avec les nouvelles variables introduites.)*

---

## 8. Méthodologie globale

1. **Cadrage** (Phase 0 - ce document)
2. **Collecte** : génération des données fictives cohérentes
3. **Nettoyage** : contrôles de qualité des données
4. **Analyse** : financière, coûts, budgétaire
5. **Contrôle** : audit interne, détection d'anomalies
6. **Visualisation** : Power BI
7. **Prévision** : modèle N+1 et scénarios
8. **Recommandation** : plan d'amélioration de la performance

---

## 9. Planning des 8 étapes

| Étape | Contenu | Livrable principal |
|---|---|---|
| 1 | Diagnostic financier (N-2/N-1/N) | Modèle Excel + note 3-4 p. |
| 2 | Analyse des coûts et de la rentabilité par activité | Modèle Excel + note 3-4 p. |
| 3 | Budget et analyse des écarts | Excel + graphiques + note 2-3 p. |
| 4 | Tableau de bord de performance (KPI) | Note 2 p. + définitions KPI |
| 5 | Power BI (modèle + DAX + dashboard 4 pages) | Fichier Power BI |
| 6 | Anomalies et audit interne | Excel + cartographie des risques + note 2-3 p. |
| 7 | Prévisions N+1 et scénarios | Excel + note 2-3 p. |
| 8 | Plan d'amélioration de la performance | Matrice d'actions |
| Finale | Portfolio + bilan de compétences | Portfolio complet |

---

## 10. Liste complète des livrables attendus

- **Excel** : classeur unique structuré (00_Mode_Emploi → 16_Synthèse)
- **Power BI** : dashboard 4 pages (Direction, Activité, Qualité/Parcours patient, RH/Productivité)
- **Notes professionnelles** : une par étape (contexte, problématique, méthodologie, résultats, analyse, recommandations)
- **Portfolio final** : synthèse en 10 parties (présentation, CHHS, diagnostic, coûts, budget, data, audit, prévisions, recommandations, bilan de compétences)

---

## 11. Compétences CGAO mobilisées

Contrôle de gestion · comptabilité analytique · analyse financière · contrôle budgétaire · analyse des écarts · reporting · Excel avancé · Power Query · Power BI · DAX · audit interne · contrôle interne · cartographie des risques · prévisions financières · analyse de scénarios · aide à la décision · recommandations de performance.

---

## 12. Règles de cohérence des données

- Un seul système de données source : les chiffres Excel, Power BI et notes doivent toujours coïncider.
- CA analytique = CA du reporting = CA Power BI.
- Charges comptables = charges de l'analyse financière (tout retraitement analytique est documenté).
- Tout écart entre comptabilité générale et comptabilité analytique est expliqué.
- Toute donnée modifiée est répercutée dans l'ensemble des analyses liées.
- Aucune donnée personnelle réelle de patient n'est utilisée ; aucune donnée médicale identifiante n'est créée.
