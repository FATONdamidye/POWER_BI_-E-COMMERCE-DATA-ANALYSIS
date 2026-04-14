# 📊 Dashboard April — E-Commerce Analytics Challenge

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-20%2B%20mesures-0078D4?logo=microsoft&logoColor=white)
![Dataset](https://img.shields.io/badge/Dataset-70%20052%20lignes-10B981)
![Status](https://img.shields.io/badge/Status-Completed-8B5CF6)

> Dashboard analytique Power BI sur un dataset e-commerce de **70 052 transactions** (Nov 2018 – Avr 2019) — analyse des ventes, retours, clients et segmentation RFM pour orienter les décisions marketing, logistiques et commerciales.

---

---

## 🗂️ Pages du Dashboard

| # | Page | Visuels | KPIs principaux |
|---|------|---------|-----------------|
| 1 | **Page de garde** | 2 | Navigation |
| 2 | **Ventes** | 16 | CA Net, Panier moyen, Impact remises |
| 3 | **Retours** | 15 | Taux retour, CA perdu, catégories à risque |
| 4 | **Clients** | 15 | LTV, Taux rétention, Actifs/Inactifs |
| 5 | **Segmentation** | 15 | VIP / Actif / Risque / Dormant |
| 6 | **Synthèse** |
| 5 | **Recommandation** | 

---

## 📊 Chiffres clés du dataset

| Métrique | Valeur |
|----------|--------|
| Lignes brutes | 70 052 |
| Lignes après nettoyage | **59 337** |
| Période | Nov 2018 – Avr 2019 |
| **CA Net Total** | **3 976 716 €** |
| CA Brut | 4 327 554 € |
| Remises | −346 751 € (−8,0 %) |
| Commandes | 29 593 |
| Panier moyen | 134,38 € |
| Clients uniques | **24 874** |
| LTV moyenne | 159,87 € |
| Taux de retour | **0,12 %** |
| Catégories produit | 23 |

---

*Nettoyage Power Query : exclusion des SKUs non vendus (quantité_commandée ≤ 0) → −10 715 lignes*

---

## ⚡ Mesures DAX clés

```dax
-- Ventes
CA_Net_Total     = SUM(Fait_commande[montant_net])
Nb_Commandes     = DISTINCTCOUNT(Fait_commande[id_commande])
Panier_Moyen     = DIVIDE([CA_Net_Total], [Nb_Commandes])
Impact_Remises   = SUM(Fait_commande[remises])

-- Retours
Taux_Retour          = DIVIDE(SUM(retournée), SUM(commandée))
Qte_Retournee        = SUM(Fait_commande[quantite_retournée])
Impact_Retours_CA    = SUM(Fait_commande[retours])   -- = −4 087 €

-- Clients
Nombre_Total_Clients = DISTINCTCOUNT(Fait_commande[id_client])
Life_Time_Value      = DIVIDE([CA_Net_Total], [Nombre_Total_Clients])
Taux_Retention       = DIVIDE([Clients_multi_commandes], [Total_Clients])

-- Segmentation (basée sur nb_commandes + taux_retour)
Segment_VIP      -- ≥3 commandes, retour faible → 3 939 clients, LTV 369 €
Segment_Actif    -- 2 commandes, retour faible  → 5 598 clients, LTV 187 €
Segment_Dormant  -- 1 commande                  → 15 300 clients, LTV 96 €
Segment_Risque   -- retour > 10 %               → 37 clients, taux moy 35,8 %
```

---

## 💡 Insights clés

### Ventes
- **Product P + H = 56,6 % du CA total** (1,376 M€ + 876 K€) → forte concentration
- Pic de CA en **novembre 2018 (964 K€)**, creux en **février 2019 (453 K€)** — saisonnalité 2,1×
- **Vendredi = jour le plus actif** (5 365 commandes, +22 % vs moyenne)
- 8 % du CA brut part en remises — Product W/H/P les plus remisés

### Retours
- Taux global **0,12 %** — remarquablement bas, signe de qualité produit
- **Product N anomalie** : 0,67 % de retour (5,5× la moyenne), prix moyen 40 €
- Seulement 51 clients ont retourné un article (0,2 % de la base)

### Clients & Segmentation
- **61,5 % des clients = 1 seule commande** (Dormants) → levier de conversion majeur
- Les VIP (15,8 % des clients) génèrent **36,5 % du CA** avec LTV 369 € (2,3× la moyenne)
- Top client : 20 commandes, 2 609 € CA, 0 retour sur 6 mois

---

## 🎯 Recommandations

| # | Action | Cible | Impact estimé |
|---|--------|-------|---------------|
| 01 | **Réactiver les Dormants** via email J+30 + code promo | 15 300 clients | +219 K€ si 10 % convertis |
| 02 | **Programme fidélité VIP** + up-sell Product A/J | 3 939 VIP | +145 K€ si LTV +10 % |
| 03 | **Rationaliser remises** P/H/W (conditionnelles) | Budget 346 K€ | Marge +2-3 pts |
| 04 | **Auditer Product N** (fiches produit, motifs retour) | 23 retours évitables | Satisfaction ↑ |

---

## 🛠️ Stack technique

- **Power BI Desktop** — Modélisation, DAX, visualisation
- **Power Query** — Nettoyage, transformation, exclusion SKUs invalides
- **DAX** — 20+ mesures calculées, segmentation RFM, KPIs métier
- **Architecture** — Modèle en étoile (5 tables)

---



---

*Challenge Data Analytics E-Commerce — Avril 2026*
