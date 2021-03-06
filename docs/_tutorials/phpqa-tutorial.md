---
layout: page
title: Using docker-phpqa
date: 2017-07-10 08:35:43 +00:00
author:
    name: Bruno Ricardo Siqueira, Joao Paulo Vendramini Martins, & Ivan Rosolen
    website: http://herdphp.org
    twitter: https://twitter.com/herdphp
image:
    url: /images/photos/lucas-gallone-228252.jpg
    alt: Colorful graffiti art
    title: Thousand Colors by Lucas Gallone
    credit: Photo by [Lucas Gallone](https://unsplash.com/photos/PVw_vtpCGaM).
summary: >
    This is a small tutorial on how to use PHPQA, a set of Docker tools to easily create and run tests for the PHP-SRC. The intent of this library is to help any PHP developer to create PHPT tests for the language engine and its core extensions.
---

_**Contributing**: If you notice any bug or typo, please feel free to [create an issue and/or open a pull request](https://github.com/herdphp/docker-phpqa)._

[PHPQA](https://github.com/herdphp/docker-phpqa)—or docker-phpqa—is a set of Docker tools to easily create and run tests for the PHP-SRC. The intent of this library is to help any PHP developer to create PHPT tests for the language engine and its core extensions.

## How to get it?

* You will need to have [Docker](https://www.docker.com/) installed on your machine.
* Run our installer:

```
curl -s https://raw.githubusercontent.com/herdphp/docker-phpqa/master/bin/installer.sh | bash
```

**Start PHPTesting!!!**

## How to use it?

* Write a PHPT test in any folder;
* Run the `phpqa` command passing as arguments the filepath (relative or full) and the PHP version to run the test (`72`, `71`, `70`, `56`, `55`):


```
# Without a version the test will run against PHP 7.1 codebase
phpqa phpt/examples/closure_061.phpt

# With a version the test will run against the specified version
phpqa phpt/examples/closure_061.phpt 56

# If you want you can pass `all` as second argument and the test will run against all versions
phpqa phpt/examples/closure_061.phpt all
```

Note that when running the test suite there will be an output message reminding you to run `make test`. This is a standard message and you don't need to run it.

```
Build complete.
Don't forget to run 'make test'.
```

## PHP versions available

PHP 5.5, 5.6, 7.0, 7.1 and 7.2 (Alpha3) are fully available and supported.
