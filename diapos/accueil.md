# Sonarqube


---

## Rappel Qualité d'un produit logiciel:

Norme ISO 25010 :
Adéquation fonctionnelle, Efficience des performances, Compatibilité, Facilité d'utilisation, Portabilité
Fiabilité (sans bug), Maintenabilité (facilité de modification, testabilité, audit qualité logicielle),  sécurité (audit de code)

La qualité du code peut être notamment mesurée au regard :
•De mesures des taux de couverture du code 
•De métriques relatives à la lisibilité du code et à sa complexité
•Du respect d’un ensemble de pratiques définies dans un référentiel de règles de codage.


---


## Sonarqube

Le logiciel open source de mesure de la qualité du code source d'un produit (en développement ,en maintenance), analyse statique.
Se base sur le code source (Java, Python, PHP, JavaScript...) ainsi que sur les tests automatisés et le taux de couverture associés

Schéma sonar 
https://docs.sonarqube.org/latest/setup/install-server/

https://sonar.insee.fr/
https://sonar.recette.insee.fr/


---


## Métrique de SonarQube

Système de note de A (Très bien) à E (à très mauvais)
Dépendant des règles du profil qualité (par défaut sonar-way), règle classé par catégorie, niveau de sévérité, temps de remédiation
L'important est d'améliorer la qualité petit à petit. La note est là pour encourager au progrès

Catégorie :  Bug, Vulnérabilité, Mauvaise pratique (code smells), Sécurité

Niveau    :  Bloquant , Critique ,Majeur, Mineur 


---


## Etape pour l'analyse SonarQube - cas avec Maven

1 - Génération d'un token à partir de son compte Sonarqube
Token personnel ou un token dédié projet

2 - Scanner maven: 
Configuration du pom.xml (notamment pour le plugin jacoco)
Commande maven minimale
mvn clean verify sonar:sonar -Dsonar.login=myAuthenticationToken
	1 Tester sur l'environnement de recette http://sonar.recette.insee.fr/ (en mode anonyme authorisé)
	2 Intégration à un pipeline

3. Gestion des branches 
Long live branch, Short live branch

4. Lancement du pipeline 

5. visualisation du rapport SonarQube


