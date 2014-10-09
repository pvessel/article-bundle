PvesselArrayBundle
===========================

This bundle allow to create and view Articles.


### Installation


#### Step 1: Download PvesselArticleBundle using composer

Tell composer to require PvesselArticleBundle by running the command:

``` bash
$ php composer.phar require "pvessel/article-bundle:dev-master"
```

Composer will install the bundle to your project's `vendor/pvessel/article-bundle` directory.


#### Step 2: Enable the bundle

Enable the bundle in the kernel:

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...

        new Pvessel\ArticleBundle\PvesselArticleBundle(),
    );
}
```

#### Step 3: Add to router

Add to your routing.yml

``` yml
article:
    resource: "@PvesselArticleBundle/Controller"
    type:     annotation
```

### Step 4: Update database

In order to work with this bundle you must update your database (and create one if you don't use it yet).

``` bash
$ app/console doctrine:schema:update --dump-sql
```
### Step 5: Enjoy!

Run your web server and browser and try it! ( use /article path to start)