---
template: snippet
title: Changer ou désactiver le vidage de la corbeille automatique dans Wordpress
publish_date: 2019-11-17T05:10:43.105Z
authors:
  - Vladislav Kim
type: Snippets
category: WordPress
needs_update: true
status: draft
---

À ajouter dans le fichier `wp-config.php` 

```php
define('EMPTY_TRASH_DAYS', 0);
```

Pour seulement retirer l'action qui efface les posts dans la corbeille:

```php
function wpb_remove_schedule_delete() {

    remove_action('wp_scheduled_delete', 'wp_scheduled_delete');

}

add_action('init', 'wpb_remove_schedule_delete');
```