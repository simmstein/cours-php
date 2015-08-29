# L'architecture générale

Une installation de MySQL permet d'identifier un premier niveau de données : les bases. Par exemple, si on doit créer 5 sites internet, on pourra imaginer avoir une base de données par site.

Dans une base de données sont définies des tables. Dans le cas d'un blog, on pourrait avoir ces tables :

* utilisateurs
* articles
* catégories
* tags
* commentaires

Une tables est caractérisée par des champs (nommés colonnes ou attributs). Ces champs ont bien sûr un nom, mais aussi plein de caractéristiques :
* le type (entier, chaine, date, etc.)
* la valeur par défaut
* si c'est un index ou pas
* ...

On a enfin une gestion des permissions fines qui permet d'accorder à un utilisateur :
* quelle(s) bases de données il peut accéder
* quelle(s) tables il peut accéder
* quel(s) champ(s) il peut accéder

L'accès se détermine par :
* le droit de lire
* le droit d'écrire

