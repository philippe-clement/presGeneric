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

- Configuration récupérée de Prisme et Toucan
- Surcharges des properties dans le SpringApplicationBuilder
- Controleur par anotation @GetMapping,@PostMapping ...
- Swagger de documentation des WebService

---

## Api REST (suite)

- Intercepteur pour la sécurité : suivant liste des habilitations d'un agent.
- Controleur uniquement avec lancement de services (pas ou peu de traitement dans le controleur)
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
- package service sans interface

---

## Generic core - améliorations

- interface pour les services - Est ce utile ?
- tests unitaires
- nettoyage de classes qui ne sont pas utiles
- ajout de JAVA-DOC
