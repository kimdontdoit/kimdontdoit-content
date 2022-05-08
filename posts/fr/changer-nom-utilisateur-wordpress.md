---
title: Changer son nom d’utilisateur WordPress
publish_date: 2021-11-20
authors:
  - Vladislav Kim
category: WordPress
type: Articles
status: published
---

Si vous vous retrouvez sur cet article, c’est probablement car vous avez à changer le nom d’un utilisateur dans votre panneau d’administration WordPress et vous réaliser que ce n’est malheureusement pas possible.

Pas d'inquiétude! Dans cette publication, je vous décris quelques manières pour changer un nom d’utilisateur, ainsi que la méthode la plus facile avec un plugin.

phpMyAdmin / MySQL quessé ça? [Utiliser la méthode avec l'extension recommandée](#)

## Changer son username dans la base de donnée
Pour cette méthode, vous devez savoir comment vous connecter à votre base de donnée WordPress. Je recommande ceci pour ceux qui sont plus à l'aise techniquement et qui ont déjà accéder leur base de donnée auparavant. Par contre, si pour quelconque raison, vous n'avez pas d'autres options, il faut simplement s'assurer de modifier seulement le champs qui est concerné.

Je ferais l'exemple avec phpMyAdmin, un outil web fourni par plusieurs services d'hébergement (Si vous avez CPanel, par exemple.) Si vous n'êtes pas certain de comment vous connecter, contacter votre service d'hébergement. J'utilise personnellement sur mes VPS, <a href="https://github.com/Sequel-Ace/Sequel-Ace" class="rank-math-link">Sequel Ace</a> sur macOS avec un tunnel SSH.

Une fois dans phpMyAdmin, il faut cliquer sur la base de donnée de votre site WordPress dans le menu à gauche. Il soit possible que vous en ayez plus qu'une si vous avez plus d'un site sur votre serveur.

Vous verrez dans le menu que vous avez cliqué et dans la fenêtre principale un défilement de tables de base de données. Par défaut, WordPress utilise un préfixe wp_ pour le nom des tables, mais qui peut varier d'une installation à l'autre, c'est tout a fait normal.

Ensuite, choisissez la table <code>wp_users</code> dans le côté gauche ou dans la fenêtre principale. Il se peut que le défilement des tables soit sur plus d'une page si vous ne le trouvez pas.

Dernière étape, trouvez l'utilisateur dont vous voulez changer le username et vous pouvez soit cliquer sur <code>Éditer</code> sur la rangée, ou double cliquer son nom d'utilisateur dans la colonne `user_login`.

Si vous avez cliqué sur <code>Éditer</code>, une fois le <code>user_login</code> changé, il ne restera qu'à sauvegarder en cliquant sur <code>Exécuter</code> dans le bas de la page, car c'est une commande MySql qui est exécutée pour faire la mise à jour.

C'est terminé! J'espère que cet article vous a été utile pour changer votre username WordPress. Si vous avez encore un utilisateur dont l'identifiant est <code>admin</code>, je vous recommande fortement d'utiliser l'une de ces méthode pour le changer à autre chose pour raison de sécurité.

## Changer son username avec un plugin
En premier, installer et activer l'extension <a href="https://wordpress.org/plugins/username-changer/" class="rank-math-link">Username Changer</a>. Une fois l'extension activée, naviguer sur le profil de l'utilisateur ( wp-admin -&gt; Comptes ) et à la place de voir "Les identifiants ne peuvent être modifiés", vous verrez l'option Change Username.

Une fois sauvegardé, l'identifiant sera mis à jour et le compte concerné devra se connecter à nouveau. Vous pouvez désinstaller l'extension sans danger si vous n'en avez plus besoin.