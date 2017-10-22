# SymfonyRollbar bundle for Symfony Framework 3
[![codecov](https://codecov.io/gh/OxCom/symfony3-rollbar-bundle/branch/master/graph/badge.svg)](https://codecov.io/gh/OxCom/symfony3-rollbar-bundle)
[![Build Status](https://travis-ci.org/OxCom/symfony3-rollbar-bundle.svg?branch=master)](https://travis-ci.org/OxCom/symfony3-rollbar-bundle)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)

Bundle for Symfony3 that integrates Rollbar tracker

# Work in progress
Current realization is used in one of my projects, so You can expect fast reactions on issues, features request and e.t.c.

# Install
1. Add SymfonyRollbarBundle with composer: ``` composer require oxcom/symfony-rollbar-bundle```
2. Register SymfonyRollbarBundle in AppKernel::registerBundles()
    ```php
        public function registerBundles()
        {
            $bundles = [
                // ...
                new \Symfony\Bundle\FrameworkBundle\FrameworkBundle(),
                // ...
                new \SymfonyRollbarBundle\SymfonyRollbarBundle(),
                // ...
            ];
    
            return $bundles;
        }
    ```
3. Setup configuration
```php
symfony_rollbar:
  rollbar:
    access_token: 'some-secret-token-here'
    environment: '%kernel.environment%'
```

More docs [here](https://github.com/OxCom/symfony3-rollbar-bundle/tree/master/docs)

# Test
To run test You have to provide an access token and then run test
```bash
$ export ROLLBAR_ACCESS_TOKEN="token here"
$ ./vendor/bin/phpunit -c tests/
```

# Bugs and Issues
Please, if You found a bug or something, that is not working properly, contact me and tell what's wrong. It's nice to have an example how to reproduce a bug, or any idea how to fix it in Your request. I'll take care about it ASAP.
