# radicati-drupal-2-startup

This repository has files and install directions to get your Drupal 11 site ready for development with the Radicati 2.0 base theme and our standard modules.

<br>
<br>

## Radicati Base Theme, without Diffy Integration

- Copy the composer.json and composer.libraries.json files to the root of your project.
- Copy the pantheon.yml file to the root of your project
- If you've got a composer.lock file, just delete it
- Run `composer install`
- Change directories to /web, and run `drush recipe ../recipes/radicati-recipe-site-base`

<br>
<br>

---

<br>

## Radicati Base Theme, With Diffy Integration

- Copy the composer.json and composer.libraries.json files to the root of your project.
- Copy the pantheon-with-diffy.yml file to the root of your project and rename it to pantheon.yml
- Copy the diffyVisualRegression.php file to `/web/private/scripts/diffyVisualRegression.php`
- If you've got a composer.lock file, just delete it
- Run `composer install`
- Change directories to /web, and run `drush recipe ../recipes/radicati-recipe-site-base`

Meanwhile, follow the [instructions on our Notion Site](https://www.notion.so/rootidpartnerview/Diffy-Visual-Regression-7505657491c44951b690566898b4cb5f?source=copy_link) to finish setting up Diffy (this took care of step 3 on the list)
