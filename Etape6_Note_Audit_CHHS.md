# ÉTAPE 6 - ANOMALIES ET AUDIT INTERNE

*Données fictives construites à des fins pédagogiques et professionnelles.*

---

## A. Objectif
Vérifier la fiabilité des données financières utilisées depuis l'Étape 1 en auditant le journal comptable N, et cartographier les risques du processus activité → facturation → comptabilité → reporting → décision, afin de sécuriser le pilotage de CHHS.

## B. Données nécessaires
Journal comptable fictif de l'exercice N : 3 015 écritures réparties sur les 3 sites, comportant des anomalies volontairement introduites (139 lignes concernées, soit 4,6 % du journal) mais non signalées explicitement, à charge pour l'auditeur de les détecter par des tests.

## C. Méthodologie
1. Génération d'un journal comptable réaliste (comptes, fournisseurs, dates ouvrées, TVA cohérente par nature de charge).
2. Introduction de 9 familles d'anomalies représentatives d'un contexte réel d'audit (doublons, montants atypiques, week-end, hors période, TVA incohérente, comptes rares, montants ronds, factures sans référence, fournisseurs inhabituels).
3. Construction de 9 tests de contrôle automatisés (formules Excel) capables de détecter chaque famille d'anomalie sans connaître à l'avance les lignes concernées.
4. Cartographie des risques du processus activité → décision, avec probabilité, impact, niveau de risque et contrôle recommandé.
5. Évaluation du contrôle interne selon les 6 composantes retenues du référentiel COSO.

## D-E. Données et calculs
Voir `Etape6_Audit_Anomalies_CHHS.xlsx` : journal complet (onglet 01), formules de détection (onglet 02).

## F. Résultats des tests de contrôle

| Test | Lignes détectées |
|---|---:|
| Doublons | 30 |
| Montants atypiques (> 3x moyenne du compte) | 26 |
| Écritures le week-end (hors paie) | 17 |
| Écritures hors période comptable | 10 |
| Incohérence de taux de TVA | 11 |
| Comptes comptables inhabituels | 10 |
| Montants arrondis suspects (multiples de 1 000 €) | 20 |
| Factures sans référence | 20 |
| Fournisseurs hors référentiel habituel | 9 |

Les tests détectent un volume cohérent avec les anomalies effectivement présentes dans le journal, ce qui valide leur pertinence (aucun test n'est resté silencieux, aucun n'a produit un nombre disproportionné de faux positifs).

## G. Analyse

**Le point le plus critique est l'absence de référence de facture sur 20 écritures d'achat**, un contrôle bloquant élémentaire qui n'existe pas aujourd'hui dans le processus : sans référence, une charge ne peut être rapprochée d'aucune pièce justificative, ce qui constitue une porte ouverte à la fraude ou à l'erreur non détectée.

**Les 30 lignes en doublon** (15 paires) représentent un risque de surestimation directe des charges : si elles n'étaient pas détectées, elles gonfleraient artificiellement le total des coûts déjà analysé aux Étapes 1 à 3, sans qu'aucune réalité économique ne le justifie.

**Les 11 incohérences de TVA** exposent CHHS à un risque de redressement fiscal, d'autant plus sensible dans le secteur de la santé où plusieurs taux réduits coexistent (2,1 % sur les médicaments, 5,5 % sur certains dispositifs médicaux) : une erreur de paramétrage peut facilement passer inaperçue sans contrôle automatisé par compte.

**La cartographie des risques identifie trois zones de risque élevé** : l'écart entre activité réalisée et facturation émise, les factures sans référence, et l'absence de réconciliation systématique entre le reporting et la comptabilité. Ces trois risques partagent une cause commune : l'absence de contrôles bloquants automatisés, remplacés par des vérifications ponctuelles ou a posteriori.

**L'évaluation COSO confirme ce diagnostic** : sur les 6 composantes évaluées, une seule (rapprochements) est jugée partiellement satisfaisante ; les 5 autres sont jugées insuffisantes, notamment la séparation des tâches (une même personne peut saisir et valider un paiement sur certains sites) et le contrôle des données (aucun contrôle automatique de doublon ou de cohérence TVA à la saisie).

## H. Recommandations

1. Rendre la référence de facture **obligatoire et bloquante** à la saisie comptable - priorité 1, coût de mise en œuvre faible.
2. Implémenter les 9 tests de contrôle de l'onglet 02 comme **contrôles automatiques récurrents** (mensuels) plutôt que comme un exercice d'audit ponctuel.
3. Séparer strictement saisie, validation et paiement des factures fournisseurs, avec une matrice d'habilitations formalisée.
4. Paramétrer un taux de TVA par défaut et non modifiable par compte comptable, pour supprimer le risque de saisie manuelle erronée.
5. Systématiser le rapprochement mensuel activité/facturation, aujourd'hui seulement partiel - ce risque est classé élevé et concerne directement la fiabilité du chiffre d'affaires utilisé depuis l'Étape 1.

## I. Compétences mobilisées

Audit interne, construction de tests de détection d'anomalies, cartographie des risques et matrice de criticité, évaluation du contrôle interne selon le référentiel COSO, esprit critique sur la fiabilité d'une donnée avant son utilisation en pilotage.

## J. Livrables produits

- **Excel** : `Etape6_Audit_Anomalies_CHHS.xlsx` (journal de 3 015 écritures, 9 tests de contrôle, cartographie des risques avec matrice de criticité, grille COSO)
