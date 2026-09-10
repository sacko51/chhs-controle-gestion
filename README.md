# CHHS - Diagnostic, Pilotage et Amélioration de la Performance

*Le Centre Hospitalier Horizon Santé (CHHS) est un groupe de santé privé fictif, construit à des fins pédagogiques et professionnelles. Toutes les données (financières, RH, qualité, comptables) sont fictives.*

## Overview

CHHS est un groupe de santé privé implanté dans le Grand Est (3 sites : Reims, Châlons-en-Champagne, Troyes), pour un chiffre d'affaires consolidé d'environ 42 M€ et 480 ETP. Ce projet répond à une problématique unique posée par la Direction :

![Problématique](https://img.shields.io/badge/PROBLÉMATIQUE-D32F2F?style=for-the-badge)

> ### 💡 Comment CHHS peut-il améliorer sa performance économique et opérationnelle tout en renforçant la fiabilité de son pilotage et de son contrôle interne ?

Le projet se déroule en 8 étapes, chacune s'appuyant strictement sur les données produites par les étapes précédentes (règle de source unique de données), depuis le diagnostic financier initial jusqu'au plan d'action chiffré final.

## Structure du projet

```
chhs-controle-gestion/
├── README.md
├── 00_cadrage/
│   └── Phase0_Cadrage_CHHS.md
├── 01_diagnostic_financier/
│   ├── Etape1_Diagnostic_Financier_CHHS.xlsx
│   └── Etape1_Note_Diagnostic_Financier_CHHS.md
├── 02_couts_rentabilite/
│   ├── Etape2_Couts_Rentabilite_CHHS.xlsx
│   └── Etape2_Note_Couts_Rentabilite_CHHS.md
├── 03_budget_ecarts/
│   ├── Etape3_Budget_Ecarts_CHHS.xlsx
│   └── Etape3_Note_Budget_Ecarts_CHHS.md
├── 04_kpi/
│   ├── Etape4_KPI_CHHS.xlsx
│   └── Etape4_Note_KPI_CHHS.md
├── 05_powerbi/
│   ├── Etape5_PowerBI_Guide_CHHS.xlsx
│   └── Etape5_Note_PowerBI_CHHS.md
├── 06_audit_anomalies/
│   ├── Etape6_Audit_Anomalies_CHHS.xlsx
│   └── Etape6_Note_Audit_CHHS.md
├── 07_previsions_scenarios/
│   ├── Etape7_Previsions_Scenarios_CHHS.xlsx
│   └── Etape7_Note_Previsions_CHHS.md
└── 08_plan_action/
    ├── Etape8_Plan_Action_CHHS.xlsx
    └── Etape8_Note_Plan_Action_CHHS.md
```

## Les 8 étapes

| # | Étape | Contenu | Résultat clé |
|---|---|---|---|
| 0 | **Cadrage** | Présentation de CHHS, organigramme, modèle de données en étoile (10 dimensions, 8 tables de faits) | Architecture de données unique pour tout le projet |
| 1 | **Diagnostic financier** | Compte de résultat et bilan sur 3 exercices (N-2/N-1/N), calcul de ratios | Taux de marge d'exploitation en baisse : 7,0 % → 4,3 % |
| 2 | **Coûts et rentabilité par activité** | Comptabilité analytique, clés de répartition, coût complet par activité | Bloc opératoire et laboratoire déficitaires (−2 261 k€ et −700 k€) |
| 3 | **Budget et analyse des écarts** | Confrontation budget/réalisé, décomposition volume/coût unitaire | Résultat d'exploitation −48,7 % vs budget, porté par l'effet coût unitaire |
| 4 | **Tableau de bord KPI** | 18 indicateurs sur 4 dimensions (activité, économique, RH, qualité) | Le couple turnover/absentéisme identifié comme cause racine |
| 5 | **Power BI** | Modèle en étoile, 24 mesures DAX, dashboard 4 pages | Guide complet de construction (modèle, DAX, spécification des pages) |
| 6 | **Audit interne et anomalies** | Journal de 3 015 écritures, 9 tests de détection automatisés, grille COSO | 139 anomalies détectées, 5 composantes COSO sur 6 jugées insuffisantes |
| 7 | **Prévisions N+1 et scénarios** | Modèle prévisionnel à 3 scénarios, analyse de sensibilité | La masse salariale explique l'essentiel de l'écart entre scénarios |
| 8 | **Plan d'amélioration de la performance** | Matrice de 11 actions, priorisation impact × effort, chiffrage global | Gain potentiel cumulé estimé à +1 850 k€/an |

## Méthodologie transversale

- **Règle de source unique** : chaque étape reprend strictement les chiffres validés à l'étape précédente ; tout écart entre comptabilité générale et comptabilité analytique est documenté.
- **Traçabilité** : chaque note professionnelle suit la même trame (objectif, données, méthodologie, résultats, analyse, recommandations, compétences mobilisées, livrables).
- **Aucune donnée réelle** : toutes les données (financières, RH, patients) sont fictives et anonymisées ; aucune donnée médicale identifiante n'a été créée.

## Compétences mobilisées

Analyse financière · comptabilité analytique · contrôle budgétaire et analyse des écarts · construction de tableaux de bord et définition de KPI · modélisation de données en étoile · écriture de mesures DAX et conception de dashboard Power BI · audit interne et cartographie des risques (référentiel COSO) · modélisation prévisionnelle multi-scénarios et analyse de sensibilité · construction d'un plan d'action priorisé (matrice impact/effort) · Excel avancé (modèles multi-onglets, contrôle de cohérence inter-étapes) · rédaction de notes professionnelles à destination d'une Direction.

## Outils utilisés

Excel avancé (formules liées, mise en forme conditionnelle) · Power BI (modèle de données, DAX) · Power Query.

## Auteur

**Bakary SACKO**
Master 2 Contrôle de Gestion et Audit Organisationnel — URCA, Reims
[sacko_bakary@outlook.com](mailto:sacko_bakary@outlook.com)
