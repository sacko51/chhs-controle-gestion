# ÉTAPE 3 - BUDGET ET ANALYSE DES ÉCARTS

*Données fictives construites à des fins pédagogiques et professionnelles.*

---

## A. Objectif

Confronter le budget N, construit en fin d'exercice N-1 par extrapolation raisonnée de l'activité et des coûts, au réalisé N établi aux Étapes 1 et 2. L'objectif est de répondre à la question : **les objectifs budgétaires ont-ils été atteints, et pourquoi existe-t-il des écarts ?**

## B. Données nécessaires

- Volumes, prix et coûts unitaires **budgétés** par activité (hypothèses posées en fin de N-1)
- Volumes, CA et coûts **réalisés** par activité, repris strictement de l'Étape 2 (règle de source unique de données)

## C. Méthodologie

1. Reconstitution du budget N par activité : CA budget = volume budgété × prix budgété ; coût budget = volume budgété × coût unitaire budgété.
2. Calcul des écarts CA, coût et marge (réalisé − budget), en valeur et en %.
3. Décomposition de l'écart de CA en **effet volume** [(volume réel − volume budget) × prix budget] et **effet prix** [(prix réel − prix budget) × volume réel].
4. Décomposition de l'écart de coût en **effet volume** [coût unitaire budget × (volume réel − volume budget)] et **effet coût unitaire** [(coût unitaire réel − coût unitaire budget) × volume réel].
5. Application de seuils d'alerte sur les écarts en % : vert (< 5 %), orange (5 % à 10 %), rouge (≥ 10 %).

## D. Données fictives (budget par activité, exercice N)

| Activité | Volume budget | Prix budget | Coût unitaire budget |
|---|---:|---:|---:|
| Consultations externes | 82 000 | 76 € | 60 € |
| Hospitalisation complète | 4 300 | 3 950 € | 3 500 € |
| Hospitalisation de jour | 6 500 | 760 € | 560 € |
| Bloc opératoire | 3 400 | 2 500 € | 2 900 € |
| Imagerie médicale | 21 000 | 195 € | 160 € |
| Laboratoire | 90 000 | 23 € | 27 € |

Le détail complet figure dans `Etape3_Budget_Ecarts_CHHS.xlsx` (onglets 01_Budget_vs_Reel, 02_Decomposition_Ecarts).

## E. Calculs - voir méthodologie (C)

## F. Résultats

### Synthèse Budget / Réalisé (k€)

| Indicateur | Budget | Réalisé | Écart € | Écart % | Alerte |
|---|---:|---:|---:|---:|:---:|
| Chiffre d'affaires | 42 822 | 42 500 | -322 | -0,8 % | 🟢 |
| Coûts d'exploitation | 39 260 | 40 674 | +1 414 | +3,6 % | 🟢 |
| **Résultat d'exploitation** | **3 562** | **1 826** | **-1 736** | **-48,7 %** | 🔴 |

### Écarts par activité (les plus significatifs)

| Activité | Écart CA % | Écart coût unitaire % | Écart marge % | Alerte |
|---|---:|---:|---:|:---:|
| Bloc opératoire | -10,0 % | +10,2 % | -66,2 % | 🔴 |
| Laboratoire | +2,7 % | +10,1 % | -94,5 % | 🔴 |
| Hospitalisation de jour | +3,2 % | +4,7 % | -14,5 % | 🟠/🔴 |
| Imagerie médicale | +3,8 % | +2,6 % | -13,2 % | 🔴 |
| Hospitalisation complète | +0,1 % | +3,3 % | -6,3 % | 🟠 |
| Consultations externes | +2,3 % | +1,0 % | -6,7 % | 🟠 |

### Décomposition des écarts (k€)

| | Effet Volume | Effet Prix / Coût unitaire | Total |
|---|---:|---:|---:|
| **Écart de CA** | -379 | +57 | **-322** |
| **Écart de coût** | -577 | +1 991 | **+1 414** |

## G. Analyse

**Un résultat d'exploitation inférieur de près de moitié à l'objectif budgétaire, alors que le chiffre d'affaires est quasiment atteint.** Le CA réalisé (42 500 k€) n'est en retrait que de 0,8 % par rapport au budget (42 822 k€) - un écart classé vert. Le vrai problème se situe sur les coûts : ils dépassent le budget de 1 414 k€ (+3,6 %), ce qui suffit à faire chuter le résultat d'exploitation de 3 562 k€ budgétés à 1 826 k€ réalisés, soit un écart de -1 736 k€ (-48,7 %), classé rouge. Un pilotage qui se limiterait au seul suivi du CA global n'aurait rien détecté.

**La décomposition confirme que l'écart de coût n'est pas un effet volume, mais un effet coût unitaire massif.** L'effet volume sur les coûts est en réalité favorable (-577 k€, car l'activité globale a été globalement proche du budget, portée notamment par un déficit de volume au bloc opératoire). C'est l'effet coût unitaire qui explique la totalité de la dérive : +1 991 k€, soit davantage que l'écart total de coût. Ce résultat est directement cohérent avec le diagnostic de l'Étape 1 : la hausse du poids des charges de personnel (59,0 % → 61,5 % du CA) se traduit ici, activité par activité, par un coût unitaire supérieur aux hypothèses budgétaires.

**Le bloc opératoire cumule les deux signaux d'alerte : volume inférieur au budget ET coût unitaire hors budget.** Le budget avait déjà anticipé un déficit sur cette activité (marge budgétée : -1 360 k€, le coût unitaire budgété de 2 900 € dépassant déjà le prix moyen budgété de 2 500 €) - un point que la Direction connaissait donc en amont. Mais la réalité a été plus sévère : volume inférieur de 300 interventions au budget (-750 k€ de CA, effet volume défavorable), et surtout un coût unitaire réel de 3 197 € contre 2 900 € budgétés (+10,2 %, effet coût unitaire de +921 k€). La marge s'est donc dégradée de -900 k€ par rapport à un budget déjà négatif, portant le déficit réalisé à -2 261 k€.

**Le laboratoire présente le même profil de coût unitaire hors norme (+10,1 %) sur un volume supérieur au budget (+5 000 analyses).** Cette combinaison est la plus pénalisante : plus de volume à un coût unitaire plus élevé que prévu, sur une activité déjà structurellement peu rémunératrice (prix moyen réel 22,4 € pour un coût réel de 29,7 €). La marge s'effondre de -340 k€ par rapport à un budget déjà négatif (-360 k€), portant le déficit réalisé à -700 k€.

**Les quatre autres activités restent globalement dans la zone verte à orange sur le CA, mais affichent toutes un coût unitaire supérieur au budget** (de +1,0 % pour les consultations à +4,7 % pour l'hospitalisation de jour), confirmant que la dérive de la masse salariale touche l'ensemble du groupe et n'est pas circonscrite aux deux activités déficitaires.

## H. Recommandations

1. Faire du **coût unitaire par activité** (et non du seul CA) l'indicateur de premier niveau du reporting mensuel : c'est lui qui a porté la totalité de la dérive de résultat.
2. Sur le **bloc opératoire**, engager une revue du process budgétaire lui-même : un budget qui anticipe déjà une perte doit déclencher une action structurelle (revue du panier d'actes, négociation tarifaire, plan d'optimisation des salles) et non une simple reconduction l'année suivante.
3. Sur le **laboratoire**, objectiver la baisse tendancielle des tarifs de biologie médicale dans les hypothèses budgétaires futures pour éviter de rebudgéter un déficit sans plan d'action associé (cf. recommandations de l'Étape 2).
4. Décliner un **budget flexible** (budget ajusté au volume réel) dans le prochain exercice, afin de neutraliser l'effet volume et d'isoler plus tôt en cours d'année les dérives de coût unitaire.

## I. Compétences mobilisées

Construction et suivi budgétaire · analyse des écarts (volume / prix / coût unitaire) · définition de seuils d'alerte · priorisation des zones de risque financier · Excel avancé (mise en forme conditionnelle, décomposition d'écarts).

## J. Livrables produits

- **Excel** : `Etape3_Budget_Ecarts_CHHS.xlsx` (comparaison budget/réel par activité avec alertes couleur, décomposition volume/prix et volume/coût unitaire)
