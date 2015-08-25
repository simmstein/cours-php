# Les fonctions

Les fonctions peuvent être assimilées à des robots. Elles sont utilisées pour énormément de choses et vous avez la possibilité d'en créer.

Elles sont créées pour réaliser une tâche bien précise qui est suceptible d'être répétée plusieurs fois dans l'application.

Exemple : j'ai besoin de calculer la surface de 10 carrés donc je connais les dimensions : 10, 198, 72, 17, 92, 7293, 1287, 32, 1238, 7 (en m).

Un code naïf aurait cette forme :

```php
echo 'La surface du rectangle avec la dimension 10 est '.(10 * 10).'m²';
echo 'La surface du rectangle avec la dimension 198 est '.(198 * 198).'m²';
echo 'La surface du rectangle avec la dimension 72 est '.(72 * 72).'m²';
echo 'La surface du rectangle avec la dimension 17 est '.(17 * 17).'m²';
echo 'La surface du rectangle avec la dimension 92 est '.(92 * 92).'m²';
echo 'La surface du rectangle avec la dimension 7293 est '.(7293 * 7293).'m²';
[...]
```
On réalise ici que le code, bien qu'il fonctionne, est très répétitif. On se doute que si la phrase doit être modifiée, alors ça prendrait un temps important pour tout modifier.

On remarque qu'on répète toujours la même chose : afficher une phrases contenant 2 éléments variants : la dimension et la surface.

```
function surface($dimension) {
    $surface = $dimension * $dimension;
    return 'La surface du rectangle avec la dimension '.$dimension.' est '.$surface.'m²';
}

echo surface(10);
echo surface(198);
echo surface(72);
echo surface(17);
echo surface(92);
echo surface(7293);
echo surface(1287);
echo surface(32);
echo surface(1238);
```

En plus d'avoir du code plus simple à lire (et à comprendre), il est aussi plus simple à débugger.

Mais du coup, on peut aller un peu plus loin encore. Finalement, la dizaine de dimensions est une liste qu'il suffirait de parcourir avec une boucle.

```php
function surface($dimension) {
    $surface = $dimension * $dimension;
    return 'La surface du rectangle avec la dimension '.$dimension.' est '.$surface.'m²';
}

$dimensions = [10, 198, 72, 17, 92, 7293, 1287, 32, 1238, 7];

foreach ($dimensions as dimension) {
    echo surface($dimension);
}
```

Quand in introduit un ```return``` dans une fonction, elle stop son exécution et retourne la valeur indiquée. Si aucun ```return``` n'est placé alors elle va retourner ```null```.

