# Les variables

Les variables permettent de stocker des données. En PHP, une variable peut recevoir plusieurs type de données qu'on verra dans le slide suivant.

Pour déclarer une variable, on utiliser le signe ```$``` suivi de son nom. Il ne peut comporter que des lettres non accentuées (majuscules et minuscules), des chiffres et des "_". Les chiffres ne sont pas autorisés en début de nom.

```php
$prenom = "Simon";
$nom = "Vieille";
$age = 26;
$une_autre_variable = "foo"; // la norme PSR-2 déprécie cette écriture non camelCase
```

À tout moment le contenu d'une variable pour être modifié.

Pour afficher le contenu d'une variable, on utilise la fonction ```echo```.

```php
$prenom = 'Simon';
echo $prenom; // Affiche : Simon
```

Vous pouvez remarquer qu'à chaque fin d'instruction, il y a un ";". Il est impératif de l'ajouter sinon vous aurez des erreurs.
