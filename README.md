
# 🏆 CAN 2025 - Pipeline Data Engineering End-to-End

## 📋 Aperçu du projet
Pipeline complet d'ingestion, transformation et analyse des données **simulées** de scans de billets pour la Coupe d'Afrique des Nations 2025.


**Auteur** : Abdellah Samani  
**Email** : abdellah.samani.data@gmail.com  
**Date** : Décembre 2025

## 🎯 Objectifs
- Centraliser les sources hétérogènes (bases SQL + fichiers CSV)
- Construire un pipeline fiable, scalable et automatisé
- Produire des données prêtes pour l'analyse (gold layer)
- Assurer audit et traçabilité des données

## 📊 Résultats
| Métrique | Valeur |
|----------|--------|
| Données traitées | 1.46 million de scans |
| Qualité données | 99.88% valides |

## 🏗️ Architecture
```
Architecture Médaillon :
Bronze (Parquet) → Silver (Delta) → Gold (Star Schema Delta)
```

### Stack technique :
- **Orchestration** : Azure Data Factory
- **Transformation** : Azure Databricks (PySpark)
- **Stockage** : Azure Data Lake Gen2
- **Visualisation** : Power BI
- **Sécurité** : Azure Key Vault
- **Format** : Parquet → Delta → Delta

## 📁 Structure du projet
```
can2025-data-pipeline/
├── 01-ingestion/          # Pipelines ADF et configurations
├── 02-transformation/     # Notebooks Databricks
├── 03-documentation/      # Documentation 
├── 04-dashboard/          # Fichiers Power BI
└── 05-scripts/            # Scripts utilitaires
```

### Outils et technologies
- Azure Data Factory
- Azure Sql Database
- Azure Databricks Workspace
- Azure Data Lake Gen2
- Azure Key Vault
- Power BI


## 🔧 Composants principaux

### Ingestion (ADF)
- `pl_to_bronze_parquet` : Pipeline principal d'ingestion
- Configuration dynamique via fichiers CSV

### Transformation (Databricks)
- **01_silver_dimensions_processing** : Nettoyage des dimensions
- **02_silver_fact_tickets_cleaning** : Nettoyage des faits (1.46M lignes)
- **03_silver_fact_tickets_enriching** : Enrichissement des données
- **04_gold_star_schema_creation** : Création du schéma en étoile

### Consommation (Power BI)
- Dashboard analytique basé sur données batch
- Connexion via Unity Catalog
- KPI : billets scannés, participation par stade, répartition par canal

## 📈 Métriques de qualité
- **Complétude** : 100% des champs obligatoires
- **Validité** : Formats validés (ticket_id, fan_id, dates)
- **Cohérence** : Relations référentielles vérifiées
- **Unicité** : Pas de doublons dans les clés

## 🛡️ Sécurité
- Tous les secrets dans Azure Key Vault



## 🏆 Concours Étudiant

Ce projet a été réalisé dans le cadre du **SBI Student Challenge – CAN 2025 Edition.**.

Je tiens à exprimer ma profonde gratitude à **SBI Group** pour :
- L'organisation de ce concours stimulant qui permet aux étudiants de mettre en pratique leurs compétences
- L'opportunité de travailler sur un cas réel de data engineering

Ce concours a été une expérience formatrice qui m'a permis de :

✅ Appliquer les concepts théoriques à un projet concret  
✅ Développer un pipeline de production end-to-end   
✅ Améliorer mes compétences en architecture cloud Azure  

**Merci SBI Group pour cette initiative inspirante !**


## 📄 Licence
Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.


