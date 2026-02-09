# radicati-drupal-2-startup

This repository has files and install directions to get your Drupal 11 site ready for development with the Radicati 2.0 base theme and our standard modules.

<br>
<br>

## How To:

### Radicati Base Theme, without Diffy Integration

- Copy the composer.json and composer.libraries.json files to the root of your project.
- Copy the pantheon.yml file to the root of your project
- If you've got a composer.lock file, just delete it
- Run `composer install`
- Change directories to /web, and run `drush recipe ../recipes/radicati-recipe-site-base`

<br>
<br>

---

<br>

### Radicati Base Theme, With Diffy Integration

- Copy the composer.json and composer.libraries.json files to the root of your project.
- Copy the pantheon-with-diffy.yml file to the root of your project and rename it to pantheon.yml
- Copy the diffyVisualRegression.php file to `/web/private/scripts/diffyVisualRegression.php`
- If you've got a composer.lock file, just delete it
- Run `composer install`
- Change directories to /web, and run `drush recipe ../recipes/radicati-recipe-site-base`

Meanwhile, follow the [instructions on our Notion Site](https://www.notion.so/rootidpartnerview/Diffy-Visual-Regression-7505657491c44951b690566898b4cb5f?source=copy_link) to finish setting up Diffy (this took care of step 3 on the list)

<br>
<br>

---

## What's being installed:

The composer.json file sets you up with a bunch of modules we've found useful on our sites. It also installs some of our recipes by default:

- [getrootid/radicati-recipe-layout-builder](https://github.com/getrootid/radicati_recipe_layout_builder)
- [getrootid/radicati-recipe-admin](https://github.com/getrootid/radicati_recipe_admin)
- [getrootid/radicati-recipe-content-base](https://github.com/getrootid/radicati_recipe_content_base)
- [getrootid/radicati-recipe-people](https://github.com/getrootid/radicati_recipe_people)
- [getrootid/radicati-recipe-press](https://github.com/getrootid/radicati_recipe_press)
- [getrootid/radicati-recipe-search](https://github.com/getrootid/radicati_recipe_search)
- [getrootid/radicati-recipe-blog-basic](https://github.com/getrootid/radicati_recipe_blog_basic)
- [getrootid/radicati-recipe-media](https://github.com/getrootid/radicati_recipe_media)
- [getrootid/radicati_drupal_theme](https://github.com/getrootid/radicati_drupal_theme/tree/2.0.x)

## Other recipes that you might want to install and run:

- [radicati_recipe_advanced_components](https://github.com/getrootid/radicati_recipe_advanced_components)
- [radicati_recipe_alerts](https://github.com/getrootid/radicati_recipe_alerts)
- [radicati_recipe_events](https://github.com/getrootid/radicati_recipe_events)

## Other modules that might be useful:

- [Our go-to Drupal Modules](https://docs.google.com/spreadsheets/d/1a1YJ5nxg6vyhcOir9xdKc-daC3PH_JjtasrQQkJwR6k/edit?usp=sharing)
