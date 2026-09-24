# ÉTAPE 5 - POWER BI

*Données fictives construites à des fins pédagogiques et professionnelles.*

> **Précision de méthode** : je ne peux pas générer directement un fichier `.pbix` (Power BI Desktop n'est pas accessible depuis cet environnement). Cette étape livre donc tout le nécessaire pour le construire toi-même en quelques dizaines de minutes : le modèle de données, les mesures DAX prêtes à copier, et la spécification complète des 4 pages. Le fichier `Etape5_PowerBI_Guide_CHHS.xlsx` peut aussi servir de source de données à importer dans Power BI (Obtenir les données → Classeur Excel) pour un premier prototypage rapide.

## A. Objectif
Transformer les analyses des Étapes 1 à 4 en un dashboard interactif orienté décision, cohérent avec les données déjà validées (règle de source unique).

## B. Données nécessaires
Le modèle en étoile défini en Phase 0 (Dim_Date, Dim_Site, Dim_Activite, Dim_Employe, Dim_Centre_Cout, Fact_CA, Fact_Charges, Fact_Budget, Fact_RH, Fact_Qualite, Fact_Activite), alimenté avec les valeurs des Étapes 1 à 4.

## C. Méthodologie
1. Importer/recréer les tables du modèle en étoile dans Power BI Desktop (onglet `01_Modele_Donnees`).
2. Créer une table calendrier continue et la marquer comme "table de dates" (nécessaire pour `SAMEPERIODLASTYEAR`).
3. Créer les relations en cardinalité 1 → N, dimension vers fait, filtre à sens unique.
4. Copier les 24 mesures DAX du catalogue (onglet `02_Mesures_DAX`).
5. Construire les 4 pages selon la spécification (onglet `03_Pages_Dashboard`) : objectif, KPI, graphiques, filtres.

## D-E. Données et calculs
Voir le classeur `Etape5_PowerBI_Guide_CHHS.xlsx` : modèle de données, 24 mesures DAX documentées avec leur formule exacte, spécification des 4 pages (Direction, Activité, Qualité/Parcours patient, RH/Productivité).

## F-G. Résultats et analyse
Le choix des visuels par page découle directement des constats des étapes précédentes plutôt que d'un choix esthétique :
- **Page Direction** : une jauge sur le taux de marge (seuil 5 %) rend immédiatement visible l'écart avec le résultat réel de 4,3 % constaté en Étape 1.
- **Page Activité** : un code couleur rouge/vert sur la marge par activité fait ressortir en un coup d'œil le bloc opératoire et le laboratoire, identifiés comme destructeurs de valeur en Étape 2.
- **Page RH/Productivité** : la courbe croisée CA/ETP vs Masse salariale/ETP matérialise "l'effet ciseaux" mis en évidence en Étape 4 (masse salariale/ETP +10,6 % contre CA/ETP +6,0 %).
- **Page Qualité** : le suivi de la satisfaction et du taux de réclamation permet de vérifier si la corrélation avec la tension RH (turnover, absentéisme) se confirme mois après mois.

## H. Recommandations
1. Donner à la page Direction un accès en un clic vers la page Activité pour tout écart de marge dépassant le seuil rouge (drill-through Power BI).
2. Programmer un rafraîchissement mensuel aligné sur la clôture comptable, pour que le dashboard reste la source de référence unique du reporting.

## I. Compétences mobilisées
Modélisation de données en étoile, écriture de mesures DAX, conception de dashboard orienté décision, articulation entre besoin métier et choix de visualisation.

## J. Livrables
- **Excel** (guide de construction) : `Etape5_PowerBI_Guide_CHHS.xlsx` (modèle de données, mesures DAX, spécification des 4 pages)
