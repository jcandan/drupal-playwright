# Drupal Playwright

A vanilla Drupal instance with DDEV and Playwright.

## Requirements

- DDEV

## Getting Started

1. Clone the project locally

   ```
   git clone git@github.com:jcandan/drupal-playwright.git
   ```

   > You will need to have your public SSH key listed in your [Github settings](https://github.com/settings/keys).

2. Start DDEV.

   ```
   ddev start
   ```

3. Install site dependencies.

   ```
   ddev composer install
   ```

4. Install a clean Drupal instance.

   ```
   ddev drush site:install web/recipes/custom/simple
   ```

   > Run this again if you want to start from a clean database.

5. Install Playwright dependencies and cache them for later.

   ```
   ddev install-playwright
   ```

## Working With This Project

Run the following commands as needed.

### Log into Drupal

```
ddev launch $(ddev drush user:login)
```

### To run Playwright's test command.

```
ddev playwright test
```

### To run with the UI.

```
ddev playwright test --headed
```

### To generate playwright code by browsing.

```
ddev playwright codegen
```
