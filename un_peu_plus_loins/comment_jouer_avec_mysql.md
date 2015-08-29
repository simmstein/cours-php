# Comment jouer avec MySQL ?

Au même titre qu'un serveur web, un serveur de mail, ou un serveur SVN, MySQL est un service qui écoute sur un port.

Typiquement, quand vous lancer MySQL, un socket est créé afin que vous puissiez communiquer avec.

Pour accéder un serveur MySQL, vous devez ouvrir une connexion TCP vers l'adresse IP du serveur MySQL en indiquant le port d'écoute. Par défaut le port est 3306.

Une fois connecté à MySQL, vous devez communiquer avec le langage SQL.

Voici un exemple en ligne de commande :

```bash
$ mysql -uroot -proot -hlocalhost
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 1457
Server version: 5.5.39-1-log (Debian)

Copyright (c) 2000, 2014, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| SRC2_2011_12_07    |
| SRCe2c             |
| bookstore_schemas  |
| brightgamepanel    |
| cmg_sf_preprod     |
| cmg_sf_preprod2    |
| cmg_sf_preprod3    |
| cmsintaller        |
+--------------------+
9 rows in set (0.02 sec)
```
