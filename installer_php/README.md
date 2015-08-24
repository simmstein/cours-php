# Installer PHP

Dans notre contexte, PHP sera utilisé au travers d'un serveur web. Il est donc nécessaire d'installer un ensemble d'outils en plus de PHP.

4 logiciels seront nécessaires pour travailler ensemble : un serveur web (Apache), PHP (version 5.4 minimum), MySQL et PhpMyAdmin.

Apache va vous permettre d'accéder à du contenu de votre machine via le protocole HTTP. PHP sera utilisé par Apache pour exécuter les documents PHP pour délivrer le résultat à votre navigateur. MySQL est un serveur de base de données. PhpMyAdmin est une GUI pour administrer MySQL.

Si vous être un warrior, ça sera via votre gestionnaire de paquet. Typiquement, la démarche à suivre sous Debian :

```bash
sudo aptitude install apache2 libapache2-mod-php5 mysql-server phpmyadmin
```

Les Mac users et les Windowsiens devront installer respectivement MAMP et WAMP qui contiennent tout ce qu'il faut avec en prime une jolie interface graphique pour (presque) tout gérer.

Une fois ces logiciels installés, vous aurez un répertoire de travail nommé ```www```,  ```htdocs``` ou similaire dans votre serveur web. Si vous êtes sous Linux, il sera par défaut dans ```/var/www```. Sur Mac, il est du coté de ```/Application/MAMP``` et concernant Windows, vous devriez avec un répertoire à la racine de votre disque C: (```C:\Wamp\```).
C'est ici que vous allez travailler.

## Votre premier script

Dans le répertoire de travail, ajoutez un répertoire ```test``` dans lequel vous placerez un fichier ```index.php```. Voici son contenu :

```php
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Mon premier script</title>
</head>
<body>

<p><?php echo 'Hello world'; ?></p>

</body>
</html>
```

En accédant à la page http://localhost/test/index.php, vous allez voir apparaître le message ```Hello World```.
