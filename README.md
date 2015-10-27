[![Build Status](https://travis-ci.org/balsama/d8contrib.svg?branch=8.x-1.x)](https://travis-ci.org/balsama/d8contrib)

## Install

1. Download this module and place it in your modules directory
2. From docroot:

```
drush make --no-core -y modules/d8contrib/d8contrib.make

#install address dependencies
php modules/composer_manager/scripts/init.php
composer drupal-update

drush en -y d8contrib
```
## Test
1. Move the `d8contrib_tests` directory into docroot.
2. From within the moved `d8contrib_tests` directory, run `composer install`.
3. Execute the test scenarios tagged as d8contrib:

```
bin/behat --tags=d8contrib --profile=dev
```

