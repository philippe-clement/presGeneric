# La Base de données

---

## Présentation

- PostgresSQL version 11
- partitionnée par enquête
- Modèle de données généric au départ

---

## Partitionnement

- Partition de type liste sur la colonne uid_enquete
- Table ddl_partition
- Script PG-SQL pour création et modification partition
- Trigger sur table enquête

---

## Partitionnement : Avantages

- Intégration d'une nouvelle enquête facile (ajout d'une partition)
- Purge d'enquête facile (suppression d'une partition)
- Performance non altérée avec l'ajout de nouvelles enquêtes
- Pas de base d'archivage

---

## Partitionnement : Inconvénients

- PG-SQL contraire au CTT mais ...
- Peu utlisée actuellement mais ...
- Intégration avec Hibernate

---

## Modèle généric : quesako

- Peu de colonne par entités
- Identifiants techniques pour clés primaires Référentiel (enquete par exemple)
- Identifiants composites pour clés Gestion (valeur par exemple)

---

## Modèle généric : changement

- Rajout de colonnes dans certaines tables : dossier, valeur
- Création de tables references communes non partitionnées
