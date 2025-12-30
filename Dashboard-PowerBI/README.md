# 📊 Tableau de bord Power BI – CAN 2025 (Scans de billets)

## Présentation
Ce tableau de bord permet de visualiser la fréquentation des stades,
les scans de billets et les indicateurs de revenus à partir de la couche
**Gold** de la plateforme de données.

Le dashboard représente la **couche de consommation** du projet
et illustre comment les données préparées par les pipelines
sont exploitées par les utilisateurs métiers.

---

## 📁 Accès au fichier Power BI
En raison des limitations de taille des plateformes de dépôt,
le fichier Power BI (.pbix) est hébergé sur un espace externe.

👉 **Télécharger le tableau de bord (.pbix)**  
https://drive.google.com/XXXXXXXX

*(Accès en lecture seule)*

---

## 🔌 Sources de données
- Azure Databricks (couche Gold)
- Données ingérées et transformées via :
  - Azure Data Factory
  - Azure Databricks
  - Architecture Medallion (Bronze / Silver / Gold)

---

## 📐 Grain des données
- **Scan de billet** (fait principal)
- 1 scan = 1 entrée au stade
- Séparation claire entre billets et spectateurs afin d’éviter toute ambiguïté métrique

---

## 📊 Indicateurs clés
- Fréquentation totale (nombre de scans)
- Revenu total (MAD)
- Nombre de billets uniques
- Nombre de spectateurs par ville
- Taux d’occupation des stades



## 🖼️ Aperçu du tableau de bord
Des captures d’écran sont disponibles dans le dossier `/screenshots`.
