# Exercices

Le formulaire réalisé pour la page de contact comporte quelques failles. Il est en effet possible de réaliser un robot qui posterais indéfinilent le formulaire. Par ailleurs, aucune données n'a été vérifée.

## Format des données

Réalisez un correctif qui testerais les données saisies. On souhaitons que tous les champs ont été saisis et que l'email soit au format d'un email.

### Aide

Une liste de fonctions qui pourraient vous intéresser :

- ```empty```
- ```trim```
- ```filter_var```

##  YOU SHALL NOT PASS

Mettez un système qui enregistre un cookie indiquant que l'internaute a déjà envoyé un message. Vous devrez bloqué l'envoi de nouveau message quand l'internaute a ce fameux cookie.

### Aide

Une liste de fonctions qui pourraient vous intéresser :

- ```isset```
- ```setcookie```

##  YOU SHALL NOT PASS (variante)

Mettez un système qui enregistre l'IP de l'internaute dans un fichier Vous devrez bloqué l'envoi de nouveau message quand l'internaute a son IP dans le fichier.

### Aide

Une liste de fonctions qui pourraient vous intéresser :

- ```isset```
- ```file_get_contents```
- ```file_put_contents```

## Un peu d'ergonomie…

Imaginez un système qui permet à l'utilisateur de corriger une erreur de saisie sans devoir tout remplir à nouveau.
**Attention à la sécurité !**
