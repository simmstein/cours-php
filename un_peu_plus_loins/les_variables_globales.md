# Les variables superglobales

Les variables superglobales sont générées automatiquement par l'environnement PHP. Elles incluent tout un tas de choses telles que des informations sur le serveur et les données envoyées par l'utilisateur. Elles sont accessibles partout dans une application mais varient en fonction du serveur et de l'internaute.

Il en existe quelques-unes dont les plus importantes sont :

- ```$_GET``` : un tableau contenant les données de la **query_string** d'une requête HTTP. Typiquement, la partie en rouge de cette url : https://www.qwant.com/?<span style="color: red">**q=deblans&client=opensearch**</span>

```
array(2) {
  'q' =>
  string(6) "deblan"
  'client' =>
  string(10) "opensearch"
}
```

- Vous avez la variantes avec les requêtes HTTP Post où les données sont dans l'entête : ```$_POST```.
- La variable ```$_SERVER``` détails toutes les informations du système : OS, mémoire, configuration, etc.

```
array(62) {
  'MAIL' =>
  string(15) "/var/mail/simon"
  'USER' =>
  string(5) "simon"
  'XDG_SEAT' =>
  string(5) "seat0"
  'SSH_AGENT_PID' =>
  string(4) "3490"
  'SHLVL' =>
  string(1) "1"
  'HOME' =>
  string(11) "/home/simon"
  [...]
```

- Les cookies sont accessibles via ```$_COOKIE``` et les données stockées en session (coté serveur et coté client) avec ```$_SESSION```
- ```$_FILES``` permet de gérer l'upload de fichiers

http://php.net/manual/fr/reserved.variables.php

