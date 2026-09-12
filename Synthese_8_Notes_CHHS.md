# Synthèse - Projet CHHS

*Centre Hospitalier Horizon Santé (CHHS) - cas fictif construit à des fins pédagogiques. Master 2 Contrôle de Gestion et Audit Organisationnel - URCA, Reims.*

Chaque étape a produit un classeur Excel et une note professionnelle associée. Ce document résume, pour chacune, le constat central et son lien avec les autres étapes - le détail des calculs et de l'analyse complète reste dans les notes elles-mêmes.

---

## Étape 1 - Diagnostic financier

Le CA progresse de 11,8 % sur trois exercices (38 000 → 42 500 k€), mais le taux de marge d'exploitation recule de 7,0 % à 4,3 %. La cause : les charges de personnel augmentent plus vite que l'activité (+16,6 % contre +11,8 %), passant de 59,0 % à 61,5 % du CA. En parallèle, le BFR se dégrade fortement (-200 → +2 600 k€) et la trésorerie chute de moitié (4 200 → 2 100 k€), alors que la structure financière reste globalement saine (autonomie financière en hausse, liquidité confortable). Ce diagnostic fixe les données de référence pour toutes les étapes suivantes.

## Étape 2 - Coûts et rentabilité par activité

La ventilation des charges par activité (répartition directe/indirecte, contrôle de cohérence à l'euro près avec l'Étape 1) révèle que deux activités détruisent de la valeur : le bloc opératoire (−2 261 k€, coût unitaire 3 197 € pour un prix moyen de 2 468 €) et le laboratoire (−700 k€, effet volume/prix inversé). Sans elles, la marge du groupe serait proche de 15 % au lieu de 4,3 % - ce sont les quatre autres activités qui financent ce déficit.

## Étape 3 - Budget et analyse des écarts

Le CA réalisé est quasi conforme au budget (−0,8 %), mais le résultat d'exploitation s'effondre de 48,7 % (3 562 → 1 826 k€) : un suivi limité au seul CA n'aurait rien détecté. La décomposition montre que l'effet volume est en réalité favorable (−577 k€) et que c'est l'effet coût unitaire (+1 991 k€) qui porte toute la dérive - cohérent avec la hausse des charges de personnel de l'Étape 1. Le bloc opératoire cumule les deux signaux défavorables (volume et coût unitaire hors budget).

## Étape 4 - Tableau de bord KPI

Sur 18 indicateurs suivis sur quatre dimensions, deux signaux RH ressortent comme cause racine : le turnover passe de 9 % à 13 % et l'absentéisme de 6,2 % à 7,5 %, et la masse salariale par ETP progresse deux fois plus vite (+10,6 %) que la productivité CA/ETP (+6,0 %). Le bloc opératoire est la seule activité en recul de volume (−6,1 %). La qualité perçue se dégrade sur la même période - un lien de causalité avec la tension RH est plausible et mérite d'être objectivé.

## Étape 5 - Modèle Power BI

Ce livrable ne remplace pas un fichier `.pbix` (non générable dans cet environnement) : il documente le modèle en étoile, 24 mesures DAX prêtes à copier, et la spécification de 4 pages de dashboard. Le choix des visuels découle directement des constats précédents plutôt que d'un parti pris esthétique : jauge de marge au seuil de 5 % (Direction), code couleur rouge/vert par activité pour isoler bloc opératoire et laboratoire (Activité), courbe croisée CA/ETP vs masse salariale/ETP pour matérialiser l'effet ciseaux RH (RH/Productivité).

## Étape 6 - Audit interne et cartographie des risques

Neuf tests automatisés appliqués à un journal de 3 015 écritures détectent un volume d'anomalies cohérent avec les 139 lignes effectivement altérées (doublons, TVA incohérente, écritures hors période...). Le risque le plus critique : 20 factures sans référence, soit l'absence d'un contrôle bloquant élémentaire. L'évaluation COSO confirme la fragilité du dispositif : 5 des 6 composantes sont jugées insuffisantes, notamment la séparation des tâches. Ce constat débouche directement sur une action corrective en Étape 8.

## Étape 7 - Prévisions N+1 et scénarios

Entre les scénarios prudent et optimiste, le CA ne varie que de 5 % (42 925 → 45 050 k€) mais le résultat d'exploitation varie d'un facteur 3 (1 030 → 3 154 k€) : l'écart se joue presque entièrement sur la masse salariale/CA (63,0 % → 60,0 %), pas sur l'activité. L'analyse de sensibilité le confirme : un point de masse salariale ou d'achats pèse deux fois plus (−440 k€) qu'un point de volume additionnel (+264 k€) - la même hiérarchie de leviers que l'Étape 3.

## Étape 8 - Plan d'amélioration de la performance

Onze actions issues des 7 étapes précédentes sont priorisées sur une matrice impact/effort, avec un chiffrage de +1 850 k€/an sur les 3 actions les mieux quantifiées (bloc opératoire, fidélisation RH, fournisseurs). Ce montant, cumulé sans tenir compte des recouvrements possibles entre leviers, est présenté comme un plafond théorique plutôt qu'un engagement - il dépasse d'ailleurs le scénario optimiste de l'Étape 7, ce qui invite à la prudence. Les actions de contrôle interne (Étape 6), non chiffrables, sont classées prioritaires car elles conditionnent la fiabilité de tous les chiffres pilotés en amont.

---

**Lecture transversale.** La tension RH (turnover, absentéisme) identifiée en Étape 4 explique la hausse du coût unitaire détectée en Étape 3, se retrouve comme premier facteur de sensibilité en Étape 7, et motive l'action la mieux chiffrée du plan d'Étape 8. En parallèle, le bloc opératoire et le laboratoire, repérés déficitaires en Étape 2, réapparaissent comme points de vigilance en Étape 3, en Étape 5 (dashboard) et en Étape 8 (action prioritaire). Ce n'est pas huit analyses indépendantes, mais un même diagnostic financier affiné et confirmé sous des angles différents à chaque étape.
