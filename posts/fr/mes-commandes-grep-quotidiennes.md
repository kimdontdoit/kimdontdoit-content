---
template: single-post
title: Mes commandes grep quotidiennes
publish_date: 2022-02-12T11:03:11.324Z
authors:
  - Vladislav Kim
category: Serveur
type: Articles
status: published
---
Cet article est une "historique de mes commandes" et, heureusement, pas de mes commandes Uber Eats, mais de mes commandes `grep` ... 🥁

Quel que soit votre spécialisation, je vous assure que grep peut grandement vous servir, même si vous avez l'habitude de faire vos recherches ailleurs tel que directement dans votre IDE / éditeur de code. Si vous connaissez Linux sur le bout de vos doigts, cet article n'est peut être pas pour vous!

Vous pouvez directement obtenir plus d'information sur la commande en cas d'oubli sur [man7.org](https://man7.org/linux/man-pages/man1/grep.1.html) ou en utilisant la commande `man grep`.

*Sans plus tarder:*

## Faire une recherche récursive avec grep

La base de la base : la recherche récursive à travers tous les fichiers d'un dossier et ses sous-dossiers.

```
grep -r "pattern" .
```

## Inclure / exclure un dossier dans grep

Il est possible de fournir plusieurs dossiers à la commande.

```
grep -r --exclude-dir=node_modules "pattern" .
grep -r --exclude-dir={node_modules,vendor} "pattern" .
```

## Inclure / Exclure un type de fichier dans grep

```
grep -r --exclude=\*.min.css "pattern" .
```

## Utiliser grep en affichant le nom des fichiers seulement

Utile pour une meilleure visibilité dans son terminal.

```
grep -l
```