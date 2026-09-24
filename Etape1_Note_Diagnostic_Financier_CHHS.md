# ÉTAPE 1 - DIAGNOSTIC FINANCIER

*Données fictives construites à des fins pédagogiques et professionnelles.*

---

## A. Objectif

Cette étape vise à évaluer la situation financière de CHHS sur trois exercices (N-2, N-1, N), à partir du compte de résultat et du bilan simplifiés, afin de répondre à trois questions posées par la Direction :
- Quelle est la situation financière du groupe ?
- Cette situation s'améliore-t-elle ou se dégrade-t-elle ?
- Quels risques financiers doivent être surveillés à court terme ?

Ce diagnostic sert de socle de référence : tous les chiffres utilisés dans les étapes suivantes (coûts, budget, KPI, Power BI, prévisions) devront rester cohérents avec ceux produits ici.

## B. Données nécessaires

- Chiffre d'affaires, charges d'exploitation (achats, charges externes, personnel, impôts et taxes, amortissements) sur N-2/N-1/N
- Résultat financier et résultat exceptionnel
- Bilan simplifié : immobilisations, stocks, créances, trésorerie, capitaux propres, dettes financières, dettes fournisseurs, autres dettes court terme

Source fictive : extraction simulée de la comptabilité générale de CHHS, consolidée sur les 3 sites.

## C. Méthodologie

1. Construction du compte de résultat sur les 3 exercices et calcul des évolutions (N-1/N-2, N/N-1)
2. Calcul du résultat d'exploitation, du résultat courant, du résultat net et des taux de marge associés
3. Construction du bilan simplifié et vérification de l'équilibre comptable (Total actif = Total passif)
4. Calcul des agrégats de structure financière : fonds de roulement (FR), besoin en fonds de roulement (BFR), trésorerie nette (FR − BFR)
5. Calcul d'un tableau de ratios (rentabilité, structure de coûts, structure financière, liquidité) et interprétation professionnelle de chaque ratio

## D. Données fictives (synthèse)

| Poste (k€) | N-2 | N-1 | N |
|---|---:|---:|---:|
| Chiffre d'affaires | 38 000 | 40 200 | 42 500 |
| Charges de personnel | 22 420 | 24 120 | 26 138 |
| Achats consommés | 5 700 | 6 110 | 6 588 |
| Charges externes | 4 560 | 4 744 | 4 888 |
| Impôts et taxes | 760 | 804 | 850 |
| Dotations aux amortissements | 1 900 | 2 010 | 2 210 |
| **Résultat d'exploitation** | **2 660** | **2 412** | **1 826** |
| Résultat financier | -150 | -180 | -220 |
| **Résultat net** | **1 920** | **1 652** | **1 220** |

Le détail complet, avec formules et données du bilan, figure dans le classeur Excel `Etape1_Diagnostic_Financier_CHHS.xlsx` (onglets 01_Compte_Resultat, 02_Bilan, 03_Ratios).

## E. Calculs

- Résultat d'exploitation = CA − (achats + charges externes + personnel + impôts et taxes + amortissements)
- Résultat courant avant impôt = Résultat d'exploitation + Résultat financier
- Résultat net = Résultat avant impôt − Impôt sur les sociétés (taux retenu : 25 %)
- Fonds de roulement = (Capitaux propres + Dettes financières LT) − Immobilisations nettes
- Besoin en fonds de roulement = (Stocks + Créances) − (Dettes fournisseurs + Autres dettes court terme)
- Trésorerie nette = FR − BFR (vérifiée cohérente avec la trésorerie active du bilan)

## F. Résultats - Tableau de ratios

| Ratio | N-2 | N-1 | N | Évolution |
|---|---:|---:|---:|---|
| Taux de marge d'exploitation | 7,0 % | 6,0 % | 4,3 % | -2,7 pt |
| Taux de rentabilité nette | 5,1 % | 4,1 % | 2,9 % | -2,2 pt |
| Poids des charges de personnel / CA | 59,0 % | 60,0 % | 61,5 % | +2,5 pt |
| Poids des charges externes / CA | 12,0 % | 11,8 % | 11,5 % | -0,5 pt |
| Fonds de roulement (k€) | 4 000 | 4 500 | 4 700 | +700 |
| BFR (k€) | -200 | 1 100 | 2 600 | +2 800 |
| Trésorerie nette (k€) | 4 200 | 3 400 | 2 100 | -2 100 |
| Autonomie financière (CP/Total actif) | 50,4 % | 52,8 % | 54,1 % | +3,7 pt |
| Taux d'endettement (Dettes fin./CP) | 57,1 % | 57,9 % | 61,9 % | +4,8 pt |
| Liquidité générale | 1,69x | 1,94x | 2,27x | +0,58x |

## G. Analyse

**Une croissance du chiffre d'affaires qui masque une érosion de la rentabilité.** Le CA progresse de 11,8 % entre N-2 et N (38,0 M€ → 42,5 M€), mais le taux de marge d'exploitation recule de 7,0 % à 4,3 % sur la même période. La cause principale est la charge de personnel, qui passe de 59,0 % à 61,5 % du CA : elle augmente plus vite (+16,6 %) que le chiffre d'affaires (+11,8 %), ce qui est cohérent avec un secteur de la santé où la masse salariale soignante est le premier poste de coût et où les tensions de recrutement tirent les rémunérations vers le haut.

**Une dégradation progressive du besoin en fonds de roulement.** Le BFR passe de -200 k€ en N-2 (situation favorable où les dettes d'exploitation finançaient le cycle) à +2 600 k€ en N. Cette dégradation résulte à la fois de la hausse des créances clients (délais de paiement des organismes payeurs) et de la baisse des « autres dettes court terme ». Combiné à un fonds de roulement qui progresse plus lentement (+700 k€ contre +2 800 k€ de BFR supplémentaire), ce mouvement absorbe la trésorerie : elle chute de 4 200 k€ à 2 100 k€ en trois ans, soit -50 %.

**Une structure financière qui reste solide, mais un endettement qui progresse.** L'autonomie financière s'améliore (50,4 % → 54,1 %) grâce à la mise en réserve des résultats successifs, et la liquidité générale reste confortable (1,69x → 2,27x). Cependant, le taux d'endettement grimpe de 57,1 % à 61,9 %, révélant un recours croissant à l'emprunt pour financer les investissements (immobilisations : 18,0 M€ → 21,2 M€) alors que l'autofinancement dégagé par l'exploitation diminue.

**Points forts** : croissance d'activité soutenue, structure financière encore équilibrée, liquidité confortable, autonomie financière en hausse.

**Points faibles** : effet de ciseaux entre CA et charges de personnel, dégradation rapide de la trésorerie, dépendance croissante à l'endettement.

**Risques identifiés** : si la tendance N-2 → N se poursuit, le taux de marge d'exploitation pourrait devenir insuffisant pour couvrir le service de la dette et les investissements nécessaires (renouvellement des équipements d'imagerie notamment), ce qui justifie une analyse fine des coûts par activité (Étape 2) avant toute décision d'investissement supplémentaire.

## H. Recommandations

1. Engager sans attendre l'analyse des coûts par activité (Étape 2) pour identifier les activités qui contribuent le plus à la hausse du poids des charges de personnel.
2. Mettre sous surveillance mensuelle le délai de recouvrement des créances clients afin de contenir la dérive du BFR.
3. Conditionner tout nouvel investissement significatif à une analyse de capacité de remboursement, compte tenu de la hausse du taux d'endettement.
4. Fixer un objectif de stabilisation du taux de marge d'exploitation au-dessus de 5 % dans le cadre du budget N+1 (Étape 3).

## I. Compétences mobilisées

Analyse financière, lecture et construction du compte de résultat et du bilan, calcul et interprétation de ratios (rentabilité, structure financière, liquidité), diagnostic et rédaction d'une note à destination d'une Direction financière, Excel avancé (modèle financier avec formules liées).

## J. Livrables produits

- **Excel** : `Etape1_Diagnostic_Financier_CHHS.xlsx` (compte de résultat, bilan, ratios - formules liées, contrôle d'équilibre)
