# Les types de données

Un type est ce qui caractérise une donnée. Suivant le type d'une donnée, des opérations seront possibles ou pas. PHP n'est pas un langage fortement typé. On dit qu'il fait  du typage dynamique : une variable peut sucessivement contenu des types différents.

```php
$entier = 10;

$flottant = 5.5; // notation anglaise de la virgule

$chaine = "Je suis une chaine de caractères";

$tableau = array(
    "première valeur",
    "deuxième valeur",
    3,
); // ou bien ["a", "b", "c",] depuis PHP 5.4

$booleen = true;

$autreBooleen = false;

$objet = new DateTime();

$closure = function() {
    // code
}
```

Connaître le type d'une variable est essentiel pour ne pas générer de bug. Dans le cadre d'un développement, vous pourrez analyser ce que contient une donnée avec ```var_dump``` :

```php
$variable = "foo";

var_dump($variable); // Affiche : string(3) "foo"
```
