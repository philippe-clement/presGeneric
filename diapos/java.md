# Le projet java

---

## Présentation

- Projet parent de Spring-boot (spring-boot-starter-parent)
- 3 modules (batch, core, api)
- Pas d'insee-config
- Inspiré des projets Prisme et Toucan

---

## Sprint DATA JPA

- Interfaces pour DAO
- Classes DaoSQL quand problèmes avec partitionnement
- Utilisation de classes DTO pour récupération des resulset SQL

---

## Api REST

- Surcharges des properties dans le SpringApplicationBuilder
- Controleur par anotation @GetMapping,@PostMapping ...
- Swagger de documentation des WebService

---

## Api REST (suite)

- Intercepteur pour la sécurité : suivant liste des habilitations d'un agent.
- Controleur uniquement avec lancement de services (pas de traitement dans le controleur)
- Controleur d'interception des exceptions levées afin de renvoyer l'erreur avec le bon status HTTP

---

## Api REST - piste amélioration

- Améliorer la récupération de l'enquete , dossier ...(resolver, cache ?)
- tests unitaires ...
- tests fontionnels ...

---

## Generic core

- package model pour le mapping des classes de la bdd
- package récupéré de coltrane pour leur model
- package récupéré de GenModC pour le module de contrôle
- package DAO et Service


---

## Generic core - améliorations

- tests unitaires
- nettoyage de classes qui ne sont pas utiles
- ajout de JAVA-DOC
