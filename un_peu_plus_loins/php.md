# PHP

Plusieurs bibliothèques PHP existent pour travailler avec MySQL.

Celle qu'il faut utiliser est PDO. Comme SQL est un langage utilisé à la fois chez MySQL, PostgreSQL, Oracle, etc., des gens ont travaillé sur un outil qui permet de jouer avec ces sgbd sans modifier le code des applications. PDO est donc une couche d'abstraction.

Voici comment se connecter à MySQL avec PDO :

```php
<?php
$dsn = 'mysql:dbname=cours_wp;host=localhost';
$user = 'root';
$password = 'root';

$pdo = new PDO($dsn, $user, $password);
```

Une fois connecté, on peut balancer de la requête SQL :

```php
$query = $pdo->prepare('insert into wp_posts(post_title, post_date) values(:title, now()');

$query->execute(array(
    ':title' => "Comment faire pousser des pommes ?",
));

$query = $pdo->query('select post_title, post_date from wp_posts');
$results = $query->fetchAll();

var_dump($results);
```

Le résultat est :

```
array(3) {
  [0]=>
  array(4) {
    ["post_title"]=>
    string(28) "Bonjour tout le monde&nbsp;!"
    [0]=>
    string(28) "Bonjour tout le monde&nbsp;!"
    ["post_date"]=>
    string(19) "2014-10-13 18:59:55"
    [1]=>
    string(19) "2014-10-13 18:59:55"
  }
  [1]=>
  array(4) {
    ["post_title"]=>
    string(20) "Page d&rsquo;exemple"
    [0]=>
    string(20) "Page d&rsquo;exemple"
    ["post_date"]=>
    string(19) "2014-10-13 18:59:55"
    [1]=>
    string(19) "2014-10-13 18:59:55"
  }
  [2]=>
  array(4) {
    ["post_title"]=>
    string(34) "Je vais devenir le maître du monde"
    [0]=>
    string(34) "Je vais devenir le maître du monde"
    ["post_date"]=>
    string(19) "2014-10-15 22:32:47"
    [1]=>
    string(19) "2014-10-15 22:32:47"
  }
}
```

Vous remarquerez que les données sont dans un format similaire au dernier TP.
