# Les batchs

---

## Présentation

- Utilisation de Spring batch minimale
- 4 chaines donc 4 packages pour les batchs
- Des services spécifiques pour chaques batchs

---

## Sprint BATCH

- Lanceur de job
- utilisation minimale car chaque job ne lance qu'un step
- Pas d'utilisation de flux (chunck)

---

## Sprint BATCH

- pourrait permettre un suivi des batchs mais ...
- nécessité de valider le fichier avant d'écrire en base.
- optimisation trouvée pour avoir des performances correctes.

---

## Batch properties

- surcharge par fichier externe que si non présence dans jar.
- création de 3 properties vers les répertoires entrants, sortants, archives
- gestion de l'arborescence au niveau des batchs

---

## Batch import valeur N-1

- premier jet : 12h
- dernier jet : 2 minutes
- réduire les appels à la base de données
- gestion du flush et utlisation du mode batch de Spring Data JPA.

---

## Batch coltrane

- résultat de la séance de travail sur le sujet au sein du domaine
- utlisation des classes récupérées de Coltrane
- utilisation de jackson pour marshaller / unmarshaller
- conversion objet generic => objet coltrane
- on pourrait peut etre passer directement de la Bdd à des objets Coltrane
