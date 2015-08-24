# Commentaires

Un commentaire est un morceau de texte qui ne sera pas interprété.

Pour rédiger des commentaires, plusieurs écritures sont possibles :

```php
// Un commentaire sur une seule ligne
```
ou
```php
# Un autre commentaire sur une seule ligne
```
et

```php
/* Un commentaire
sur plusieurs
lignes
*/
```

Il existe des commentaires particuliers nommées "annotations". Ces commentaires sont suceptibles d'êtres interprétés par des outils externes. Typiquement, quand vous souhaitez générer une documentation technique, vous en avez besoin.

```php
/*
 * @return String
 * @param $name String Le nom de la personne à qui dire bonjour
 */
function helloWorld($name) {
    return 'Hello world, ', $name;
}

```
