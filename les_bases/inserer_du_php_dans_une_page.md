# Insérer du php dans une page

PHP est un langage qui a pour objectif principal de générer du code HTML. Il est donc possible d'écrire du PHP dans du code HTML. Pour que PHP soit interprété comme tel, il doit être utilisé entre des balises particulières :

```php
<p>Voici du code html <?php et du code PHP (qui ne fonctionne pas tel quel) ?></p>
```

Il existe aussi les notations ```<? ?>``` et ```<% %>``` mais elles sont très dépréciées.

Quand un document est terminé par du PHP, il n'est pas nécessaire d'utiliser la balise de fermeture.

