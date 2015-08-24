# Les fomulaires

Une très grande partie du travail d'un développeur de site web consiste à traiter des données émises au travers de formulaire.

Tâchons de réaliser un formulaire de contact. Les personnes pourront laisser leurs informations de contact (nom, prénom, email) et un message. Un email sera envoyé à la personne qui gère la communication avec toutes les données saisies depuis le formulaire.

Nous allons découper notre outil de prise de contact via :
- une page qui affiche le formulaire : ```contact.php```
- une page qui traite la réception du message : ```contactFormulaireSoumission.php```

## contact.php

```php
<!DOCTYPE HTML>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page de contact</title>
</head>
<body>

<?php if (isset($_GET['erreur'])): ?>
	<?php if ((int) $_GET['erreur'] === 0): ?>
		<p>Le message a été envoyé, merci !</p>
	<?php elseif ((int) $_GET['erreur'] === 1): ?>
		<p>Il y a des erreurs dans le formulaire.</p>
	<?php endif; ?>
<?php endif; ?>

<section>
	<form action="contactFormulaireSoumission.php" method="POST">
		<p>
			<label for="nom">Nom :</label>
			<input type="text" name="nom" id="nom" placeholder="Nom" required />
		</p>
		<p>
			<label for="prenom">Prénom :</label>
			<input type="text" name="prenom" id="prenom" placeholder="Prénom" required />
		</p>
		<p>
			<label for="email">Email :</label>
			<input type="email" name="email" id="email" placeholder="Email" required />
		</p>
		<p>
			<label for="message">Message :</label>
			<textarea type="message" name="message" id="message" required cols="42" rows="10"></textarea>
		</p>
		<p>
			<input type="submit" value="Envoyer !" />
		</p>
	</form>
</section>

</body>
</html>
```

## contactFormulaireSoumission.php

```php
<?php

if (isset($_POST['nom'], $_POST['prenom'], $_POST['email'], $_POST['message'])) {
    $nom = $_POST['nom'];
    $prenom = $_POST['prenom'];
    $email = $_POST['email'];
    $message = $_POST['message'];

    $contenuEmail = <<< EOF
Message de $nom $prenom
Email : $email

$message
EOF;

    mail(
        'communication@deblan.fr',
        'Prise de contact',
        $contenuEmail
    );

    header('Location: contact.php?erreur=0');
    die();
}

header('Location: contact.php?erreur=1');
```
