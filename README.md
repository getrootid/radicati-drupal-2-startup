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
  <summary>The details</summary>
   <br>
The default Pantheon upstream installs Drupal 9. Oddly enough, this older repo is the upstream used by Pantheon even if you choose Drupal 11 in the site creation wizard, but they use some secret sauce during the site creation to use the contents of the drupal 11 repo... We're going to use a patch to replicate that secret sauce.

</details>

## If you installed by cloning Pantheon's [drupal-11-composer-managed](https://github.com/pantheon-upstreams/drupal-11-composer-managed) upstream

(Or if you installed using the old composer managed upstream and just applied the previous patch)

### The code

From the root of your project, type

```bash
curl -L https://raw.githubusercontent.com/getrootid/radicati-drupal-2-startup/refs/heads/main/11-repo-to-dashboard.patch | git apply -v
```

Once that's complete, you'll be ready to move on to the next patch.

<details>
  <summary>The details</summary>
   <br>
The only difference between cloning this repo and running the dashboard D11 install is that the dashboard installs a pantheon.yml file (which we need to have cause the next patch updates it).

</details>

## If you installed using Pantheon's dashboard and picked Drupal 11

(Or if you've cloned one of the Pantheon repos and have been installing the above patches)

### The code

From the root of your project, type

```bash
curl -L https://raw.githubusercontent.com/getrootid/radicati-drupal-2-startup/refs/heads/main/11-dashboard-to-radicati-drupal-2.patch | git apply -v
```

<details>
  <summary>The details</summary>
   <br>
Here we add a bunch of goodies to the composer.json, as well as updating a couple of other files.

</details>

---

## Last but not least

If there's a composer.lock file (the wizard generates one) go ahead and delete it. Then you can run `composer install` and procede on your merry 😄
