# radicati-drupal-2-startup

This repository is basically just a holding place for two git patches that adjust your composer file and ready your project so that after applying them, running `composer install` will install the Radicati Drupal Theme (2.0) and several helpful radicati recipes.

## If you installed by cloning Pantheon's [drupal-composer-managed](https://github.com/pantheon-upstreams/drupal-composer-managed) upstream

### The code

From the root of your project, type

```bash
curl -L https://raw.githubusercontent.com/getrootid/radicati-drupal-2-startup/refs/heads/main/composer-managed-to-11.patch | git apply -v
```

Once that's complete, you'll be ready to move on to the next patch.

<details>
  <summary>The nitty gritty details</summary>

The default Pantheon upstream installs Drupal 9. Oddly enough, this repo is the upstream used by Pantheon even if you choose Drupal 11 in the site creation wizard, but they use some secret sauce during the site creation to use the contents of the drupal 11 repo... We're going to use a patch to replicate that secret sauce.

</details>

### If you installed using Pantheon's dashboard and picked Drupal 11

The wizard uses the same upstream, but pulls in a different composer.json file (which is what the other patch does). Now you're ready for the Radicati Magic (TM)

From the root of your project, type `curl -L https://raw.githubusercontent.com/getrootid/radicati-drupal-2-startup/refs/heads/main/11-to-radicati-drupal-2.patch | git apply -v`.

Then you can run `composer install` and procede as usual 😄
