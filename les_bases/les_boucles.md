# Les boucles

La boucle est une structure qui permet de faire d'itérer du code suivant une condition ou une donnée.

## La boucle for

```php
for ($u = 0; $u < 10; $u++) {
    // le code qui s'exécute tant que la condition $u < 10 est vraie
}
```

Cette boucle prend 3 paramètres :
- un paramètre d'initialisation des données, ici ```$u = 0```
- une condition : ici ```$u < 10```
- une opération : ici ```$u++```

Si ```$u``` n'est pas modifié dans le code exécuté, alors cette boucle sera exécutée 10 fois.

## La boucle while

```php
while (condition) {
    // code qui s'exécute tant que la condition est vraie
}

do {
    // code qui s'exécute une fois puis tant que la condition est vraie
} while (condition);
```

## La boucle foreach

```php
foreach ($tableauDeDonnees as $index => $valeur) {
    // parcours toutes les valeurs de $tableauDeDonnees
}
```

Les boucles ```while``` et ```for``` sont des cas d'erreur fréquent : quand la condition est toujours vraie, elles n'exécutent indéfiniment et le serveur crash.
