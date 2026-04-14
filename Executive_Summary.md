# Executive Summary — Dashboard April E-Commerce

**Projet :** Challenge Data Analytics E-Commerce
**Outil :** Microsoft Power BI Desktop
**Période analysée :** Novembre 2018 – Avril 2019 (6 mois)
**Dataset :** 70 052 lignes brutes · 59 337 après nettoyage Power Query

---

## Vue d'ensemble

Ce projet présente un dashboard Power BI complet développé pour analyser la performance d'une activité e-commerce à travers **4 axes stratégiques** : Ventes, Retours, Clients et Segmentation RFM. L'objectif : transformer 70 052 lignes de transactions brutes en **insights actionnables** pour orienter les décisions marketing, commerciales et logistiques.

---

## Résultats financiers

| KPI | Valeur |
|-----|--------|
| CA Brut | 4 327 554 € |
| Remises accordées | −346 751 € |
| **CA Net** | **3 976 716 €** |
| CA perdu (retours) | −4 087 € |
| Panier moyen | 134,38 € |
| Commandes | 29 593 |

---

## Insights par axe

### 1. Ventes — Forte concentration, saisonnalité marquée

**Product P et Product H représentent à eux seuls 56,6 % du CA net** (respectivement 1 376 318 € et 876 499 €). Cette concentration sur deux catégories constitue un risque de dépendance mais aussi le levier le plus direct pour agir sur le chiffre d'affaires.

La courbe mensuelle révèle une **saisonnalité forte** : le pic de novembre 2018 (964 K€) est suivi d'une érosion progressive jusqu'au creux de février 2019 (453 K€, −53 % vs le pic), avant un rebond en mars-avril. Cette dynamique suggère un fort effet de lancement ou de promotions saisonnières en fin d'année, non maintenu en début d'année.

Les remises représentent 8 % du CA brut — un niveau significatif concentré sur les trois catégories les plus vendues (Product W : 9,6 %, H : 9,5 %, P : 8,9 %), ce qui interroge leur nécessité sur des produits déjà leaders.

### 2. Retours — Signal très positif avec une anomalie à surveiller

Le taux de retour global est de **0,12 %** (70 unités retournées sur 60 054 commandées), un niveau remarquablement bas qui témoigne d'une forte adéquation offre/demande et d'une bonne qualité des fiches produit dans l'ensemble.

L'anomalie notable est **Product N** avec un taux de 0,67 % — soit **5,5 fois la moyenne globale** — avec 19 unités retournées. Son prix moyen bas (40 €) et ses faibles remises excluent une cause prix : il s'agit probablement d'un problème de conformité produit (description inexacte, guide taille manquant, qualité perçue).

Seuls **51 clients sur 24 874 (0,2 %)** ont retourné un article, confirmant l'excellente satisfaction générale de la base client.

### 3. Clients — Base large mais peu fidélisée

La base compte **24 874 clients uniques** avec une LTV moyenne de 159,87 € et une LTV médiane de 118,70 € — l'écart entre moyenne et médiane signale une distribution asymétrique avec quelques clients très valeureux tirant la moyenne vers le haut.

**61,5 % des clients n'ont passé qu'une seule commande.** Avec une fréquence d'achat moyenne de 1,69 commandes par client, la fidélisation reste le principal chantier. Les 38,5 % de clients multi-commandes génèrent pourtant une LTV entre 1,9 et 3,8 fois supérieure selon leur segment.

Le top client réalise 20 commandes pour 2 609 € de CA — avec **zéro retour** — illustrant parfaitement le profil idéal à reproduire.

### 4. Segmentation — Deux segments à fort enjeu stratégique

La segmentation RFM construit sur deux critères (nombre de commandes + taux de retour) révèle une structure client déséquilibrée mais porteuse d'opportunités :

**Clients VIP (3 939 clients · 15,8 % de la base) :**
LTV moyenne de **369 €** (2,3× la moyenne), 3,9 commandes moyennes, taux de retour quasi nul. Ces clients génèrent **36,5 % du CA** malgré leur faible poids numérique. Ils sont le socle de la croissance rentable.

**Clients Dormants (15 300 clients · 61,5 % de la base) :**
LTV de seulement 96 € (une seule commande). Ils représentent néanmoins **36,9 % du CA total** — preuve que même un achat unique de valeur contribue significativement. La conversion d'une fraction de cette base en clients Actifs est le levier de croissance le plus accessible.

**Clients Risque (37 clients) :**
Minoritaires en nombre mais avec un taux de retour moyen de 35,8 % — profil à surveiller et à contacter proactivement avant escalade.

---

## Recommandations & impact estimé

| Priorité | Action | Levier | Impact estimé |
|----------|--------|--------|---------------|
| 🔵 **Haute** | Campagne réactivation Dormants (email J+30 + code promo) | 15 300 clients à 1 commande | **+219 K€** si 10 % convertis en Actifs |
| 🟡 **Haute** | Programme fidélité VIP + up-sell Product A/J | 3 939 clients LTV 369 € | **+145 K€** si LTV +10 % |
| 🟠 **Moyenne** | Remises conditionnelles sur Product P/H/W | 346 K€ de remises à rationaliser | **+2-3 pts de marge** sur ces catégories |
| 🔴 **Opérat.** | Audit fiches produit Product N + analyse retours | 0,67 % taux retour (anomalie) | Réduction satisfaction et retours Product N |

**Potentiel global estimé : +350 à +400 K€ de CA additionnel** sur les 6 prochains mois, sans acquisition de nouveaux clients — uniquement par optimisation de la base existante.

---

## Ce que ce projet démontre

| Compétence | Application concrète |
|------------|---------------------|
| **Modélisation Power BI** | Schéma en étoile, table de mesures DAX dédiée, relations optimisées |
| **Nettoyage Power Query** | Exclusion des SKUs non vendus (−10 715 lignes), typage, normalisation |
| **DAX avancé** | 20+ mesures : CA, LTV, taux retour, segmentation RFM, rétention |
| **Data storytelling** | 5 pages, 61 visuels, navigation fluide, slicers dynamiques |
| **Analyse métier** | Vision 360° commercial + opérationnel + CRM avec chiffrage des recommandations |

---

*Ce dashboard transforme des données brutes en décisions concrètes. Chaque recommandation est ancrée dans les chiffres réels du dataset — pas de généralités, mais des actions avec des cibles mesurables.*

---

*Challenge Data Analytics E-Commerce — Avril 2026*
