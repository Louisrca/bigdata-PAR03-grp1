# Projet Data Lake - Architecture Medallion

## Composition du groupe 1 
Louis ROCCA, Nicolas BELLANGER, Yanis ARAR

## Description

Ce projet implémente une architecture de type Medallion (Bronze-Silver-Gold) sur Databricks, permettant la transformation progressive des données tout en assurant leur qualité et leur traçabilité.

## Structure du Projet

- Fichiers notebooks Databricks au format HTML zippé
- Architecture en couches :
  - Bronze : données brutes ingérées
  - Silver : données nettoyées et validées
  - Gold : données agrégées prêtes pour l'analyse

## Prérequis Technique

Installation requise sur le cluster Databricks :

```
Librairie Maven : org.apache.iceberg:iceberg-spark-runtime-3.2_2.12:1.3.1
```

### Installation d'Iceberg

1. Dans Databricks : Cluster → Libraries → Install New
2. Sélectionner "Maven"
3. Ajouter la coordonnée ci-dessus
4. Installer

## Utilisation

1. Importer les notebooks HTML dans votre workspace Databricks
2. Configurer le cluster avec la librairie Iceberg
3. Exécuter les notebooks dans l'ordre : Bronze → Silver → Gold
