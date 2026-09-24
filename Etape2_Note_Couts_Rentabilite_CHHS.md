# ÉTAPE 2 - ANALYSE DES COÛTS ET DE LA RENTABILITÉ

*Données fictives construites à des fins pédagogiques et professionnelles.*

---

## A. Objectif

Le diagnostic financier (Étape 1) a montré une érosion du taux de marge d'exploitation (7,0 % → 4,3 % entre N-2 et N), portée par la hausse du poids des charges de personnel. Cette étape descend au niveau de l'activité pour répondre à la question posée par la Direction : **quelles activités sont rentables, et lesquelles détruisent de la valeur ?**

## B. Données nécessaires

- Volume et chiffre d'affaires N par activité (consultations externes, hospitalisation complète, hospitalisation de jour, bloc opératoire, imagerie médicale, laboratoire)
- Les pools de coûts N de l'Étape 1 (achats, personnel, charges externes, impôts et taxes, amortissements), scindés en part directe et part indirecte
- Des clés de répartition par activité pour ventiler les coûts indirects

## C. Méthodologie

1. **Scission des charges de l'Étape 1 en direct/indirect** : achats consommés (100 % direct), charges de personnel (75 % direct / 25 % indirect), charges externes et impôts et taxes (100 % indirect), amortissements (60 % direct / 40 % indirect selon qu'ils portent sur un équipement médical dédié ou sur un bâtiment).
2. **Répartition des coûts directs** : achats via une clé de consommation par activité (intensité en médicaments/dispositifs médicaux), personnel via une clé ETP affectés, amortissements directs via une clé d'équipement médical dédié.
3. **Répartition des coûts indirects** : clé unique ETP affectés (cohérente avec la répartition du personnel direct, sous l'hypothèse que les besoins en support administratif suivent l'effectif clinique de chaque activité).
4. **Calcul, pour chaque activité** : total coût, coût unitaire (coût total / volume), marge (CA − coût total), taux de marge.
5. **Contrôle de cohérence** : la somme des CA et des coûts par activité doit reconstituer exactement le chiffre d'affaires (42 500 k€) et le total des charges d'exploitation (40 674 k€) de l'Étape 1 - vérifié dans l'onglet `03_Controle_Coherence` du classeur (écart nul).

## D. Données fictives (volumes et CA N)

| Activité | Volume | CA (k€) | Prix moyen |
|---|---:|---:|---:|
| Consultations externes | 85 000 actes | 6 375 | 75 € |
| Hospitalisation complète | 4 200 séjours | 17 000 | 4 048 € |
| Hospitalisation de jour | 6 800 séjours | 5 100 | 750 € |
| Bloc opératoire | 3 100 interventions | 7 650 | 2 468 € |
| Imagerie médicale | 22 000 actes | 4 250 | 193 € |
| Laboratoire | 95 000 analyses | 2 125 | 22 € |

Le détail des clés de répartition et des calculs figure dans `Etape2_Couts_Rentabilite_CHHS.xlsx` (onglets 01_Cles_Repartition, 02_Couts_Rentabilite).

## E. Calculs

- Coût direct d'une activité = (poids achats × pool achats) + (poids personnel × pool personnel direct) + (poids amortissements × pool amortissements directs)
- Coût indirect d'une activité = poids ETP × pool coûts indirects (personnel indirect + charges externes + impôts et taxes + amortissements indirects)
- Coût total = coût direct + coût indirect ; coût unitaire = coût total / volume
- Marge = CA − coût total ; taux de marge = marge / CA

## F. Résultats

| Activité | Total coût (k€) | Coût unitaire | Marge (k€) | Taux de marge |
|---|---:|---:|---:|---:|
| Consultations externes | 5 151 | 60,6 € | **+1 224** | 19,2 % |
| Hospitalisation complète | 15 186 | 3 616 € | **+1 814** | 10,7 % |
| Hospitalisation de jour | 3 988 | 586 € | **+1 112** | 21,8 % |
| **Bloc opératoire** | 9 911 | 3 197 € | **−2 261** | **−29,6 %** |
| Imagerie médicale | 3 612 | 164 € | **+638** | 15,0 % |
| **Laboratoire** | 2 825 | 30 € | **−700** | **−32,9 %** |
| **TOTAL CHHS** | 40 674 | - | **1 826** | 4,3 % |

La somme des marges par activité (1 826 k€) est strictement égale au résultat d'exploitation N de l'Étape 1 : la règle de source unique de données est respectée.

## G. Analyse

**Deux activités détruisent de la valeur et absorbent les excédents des quatre autres.** Le bloc opératoire (−2 261 k€, taux de marge −29,6 %) et le laboratoire (−700 k€, −32,9 %) affichent un coût unitaire supérieur à leur prix moyen : 3 197 € de coût pour 2 468 € de recette au bloc, 29,7 € de coût pour 22,4 € de recette en laboratoire. Sans ces deux activités, le taux de marge du groupe serait proche de 15 % au lieu de 4,3 %.

**Le déficit du bloc opératoire s'explique par une structure de coûts lourde rapportée à un volume limité.** L'activité concentre 35 % des achats de médicaments/dispositifs médicaux et 30 % des amortissements directs (équipements chirurgicaux) pour seulement 3 100 interventions sur l'année, soit un poids fixe élevé par intervention. Deux hypothèses doivent être vérifiées lors de l'étape budgétaire : un taux d'occupation des salles insuffisant, ou une tarification (T2A) qui ne couvre pas le coût réel de certains actes chirurgicaux.

**Le déficit du laboratoire résulte d'un effet volume/prix inversé.** Avec 95 000 analyses à 22,4 € en moyenne, le laboratoire est l'activité la plus volumineuse mais la moins rémunératrice à l'acte ; son coût unitaire (29,7 €) dépasse le tarif moyen. Ce constat est cohérent avec la tendance nationale de baisse des tarifs de biologie médicale.

**Les activités d'hospitalisation (complète et de jour) et les consultations restent les moteurs de rentabilité du groupe**, avec des taux de marge de 10,7 % à 21,8 %. L'imagerie médicale dégage également une marge positive (15,0 %) malgré un poids d'amortissement élevé (équipements coûteux), grâce à un volume d'actes important.

**Limite méthodologique à signaler** : les clés de répartition (ETP affectés, intensité de consommation) sont des hypothèses de modélisation ; une mission réelle s'appuierait sur une comptabilité analytique déjà en place ou sur des relevés d'activité horodatés pour affiner la clé "ETP" en heures réellement travaillées par activité.

## H. Recommandations

1. **Bloc opératoire** : analyser le taux d'occupation des salles et le coût par type d'intervention afin d'identifier les actes structurellement déficitaires ; étudier une renégociation des achats de dispositifs médicaux (35 % du pool achats) auprès des fournisseurs.
2. **Laboratoire** : évaluer une mutualisation de certains examens avec un laboratoire partenaire ou une automatisation des analyses à fort volume pour réduire le coût unitaire.
3. **Consultations, hospitalisation, imagerie** : sécuriser ces activités rentables en maintenant leur taux d'occupation, qui compense actuellement le déficit des deux autres.
4. Affiner en Étape 3 (budget et écarts) les hypothèses de clés de répartition à partir des écarts observés entre budget et réalisé par activité.

## I. Compétences mobilisées

Comptabilité analytique, calcul de coûts complets par activité, choix et justification de clés de répartition, analyse de rentabilité par activité, détection d'activités destructrices de valeur, Excel avancé (modèle multi-onglets avec contrôle de cohérence inter-étapes).

## J. Livrables produits

- **Excel** : `Etape2_Couts_Rentabilite_CHHS.xlsx` (clés de répartition, coûts et rentabilité par activité, contrôle de cohérence avec l'Étape 1 - écart nul)
