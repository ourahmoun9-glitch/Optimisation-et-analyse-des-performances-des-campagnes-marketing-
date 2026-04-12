# 📊 Optimisation et Analyse des Performances des Campagnes Marketing

> Projet réalisé dans le cadre de la formation **Simplon Maghreb** — Analyste Data Junior

---

## 📝 Contexte

Vous êtes analyste data junior dans une entreprise qui souhaite mesurer l'efficacité de ses campagnes marketing et identifier les produits les plus achetés par ses clients.

Le projet s'appuie sur un dataset clients incluant des informations démographiques, transactionnelles, liées aux campagnes et aux produits achetés.

---

## 🎯 Objectifs

1. Réaliser une **Analyse Exploratoire des Données (EDA)** pour comprendre le dataset.
2. Effectuer des **tests statistiques** afin d'analyser les relations et l'impact des campagnes sur les ventes.
3. **Transformer et préparer** les données dans Power Query pour faciliter l'analyse.
4. Créer une **modélisation des données** dans Power BI pour visualiser les campagnes et produits.
5. Construire un **dashboard interactif et lisible** focalisé sur la performance des campagnes.

---

## 🗂️ Structure du projet

```
📁 projet-campagnes-marketing/
├── 📁 data/                   # Dataset brut et données nettoyées
├── 📁 notebooks/              # Scripts Python pour l'EDA et les tests statistiques
├── 📁 powerbi/                # Fichier Power BI (.pbix)
├── 📁 assets/                 # Captures d'écran du dashboard
└── README.md
```

---

## ⚙️ Étapes du projet

### Étape 1 — Analyse Exploratoire des Données (Python)

- Chargement du dataset avec `pandas` et identification des types de variables (continues vs discrètes).
- Analyse des statistiques descriptives : moyenne, médiane, min, max, écart-type.
- Visualisation des données :
  - Histogrammes et boxplots pour les ventes et montants des produits.
  - Bar charts pour le nombre de clients ayant accepté chaque campagne.
- Vérification des anomalies, valeurs manquantes et doublons.
- Interprétation des résultats pour tirer des insights initiaux.

### Étape 2 — Tests Statistiques

- Vérification de l'impact des campagnes sur les ventes :
  - **t-test ou ANOVA** pour comparer les montants moyens des ventes.
  - **Chi²** pour les variables catégorielles (ex. campagne acceptée vs pays).
- Exploration des corrélations entre les variables démographiques et le comportement d'achat.
- Interprétation des p-values pour identifier les facteurs significatifs.

### Étape 3 — Transformation des Données (Power Query)

- Création de tables pivot/unpivot :
  - Campagnes → colonne unique pour toutes les campagnes acceptées.
  - Produits → colonne unique pour les ventes par produit.
  - Plateformes → colonne unique pour le type d'achat (Web, Store, Catalogue).
- Nettoyage et renommage des colonnes pour un modèle clair et logique.
- Vérification des relations entre les tables : `ID client → campagnes, produits, plateformes`.
- Validation que les données sont prêtes pour la modélisation et les visualisations.

### Étape 4 — Modélisation des Données (Power BI)

- Définition des relations entre les tables en utilisant `ID client` comme clé principale.
- Vérification de la direction des filtres pour que les mesures et visualisations fonctionnent correctement.
- Création de mesures DAX :
  - Total des ventes par campagne et par produit.
  - Nombre de clients ayant accepté chaque campagne.
- Validation que les tables pivotées communiquent correctement entre elles.

### Étape 5 — Dashboard Power BI (Campaign Performance)

- Visualisations interactives et lisibles :
  - Nombre de clients par campagne.
  - Chiffre d'affaires par campagne et par produit.
  - Répartition des ventes par produit pour chaque campagne (stacked bar chart).
  - Répartition des achats par plateforme (Web, Catalogue, Magasin).
- Filtres et slicers pour faciliter l'analyse dynamique.
- Dashboard clair, intuitif et orienté business, permettant de tirer des conclusions exploitables.

---

## 🛠️ Technologies utilisées

| Outil | Usage |
|---|---|
| Python (pandas, matplotlib, scipy) | EDA & tests statistiques |
| Power Query | Transformation et nettoyage des données |
| Power BI | Modélisation et dashboard |

---

## 📈 Aperçu du Dashboard

**KPIs principaux :**
- 🧑‍🤝‍🧑 Clients en campagne : **463**
- ✅ Taux d'acceptation : **20,67 %**
- 👥 Nombre total de clients : **2 240K**
- 💰 Revenu moyen par client : **$605,80**