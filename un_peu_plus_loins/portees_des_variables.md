# Portées des variables

La portée d'une variable définie dans quelle portion de code elle est accessible.

```php
$a = "foo";

function bar($a) {
    $a = strtolower($a);

    return $a;
}

echo bar($a);

```

À présent, quelle est la valeur de ```$a``` ?

## Comment ça marche ?

Pour faire simple :


```php
$a = 10;

if ($a) {
    // $a est accessible
    $b = 20;

    while  ($b) {
        // $a est accessible
        // $b est accessible

        $c = 30;

        function foo() {
            global $b;

            // $a est inaccessible
            // $b est accessible

            $d = 40;
        }

        $b = null;
    }
}

// $b n'est pas accessible si la condition n'est pas remplie
// $c n'est pas accessible si la condition est la boucle sont exécutées
// $d ne sera jamais accessible

// Se code ne pourra jamais s'exécuter car la création
// des la fonction ```foo``` 10 fois de suite n'est pas possible

```
