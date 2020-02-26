# Doctrine2-Spatial
Doctrine2 multi-platform support for spatial types and functions. 
Currently MySQL and PostgreSQL with PostGIS are supported. 
Could potentially add support for other platforms if an interest is expressed.

## Project origins
This useful project was created by Derek J. Lambert. 
Alexandre Tranchant forked it from [creof/doctrine2-spatial](https://github.com/creof/doctrine2-spatial) 
because project seems to be unactive since 2017.

## Developments in progress
This fork will upgrade this package to the last doctrine version and the [PHP supported versions](https://www.php.net/supported-versions.php).

Feel free to [contribute](./CONTRIBUTING.md)!

## Current status
[![Build Status](https://travis-ci.org/Alexandre-T/doctrine2-spatial.svg?branch=master)](https://travis-ci.org/Alexandre-T/doctrine2-spatial)
[![Code Climate](https://codeclimate.com/github/Alexandre-T/doctrine2-spatial/badges/gpa.svg)](https://codeclimate.com/github/Alexandre-T/doctrine2-spatial)
[![Coverage Status](https://coveralls.io/repos/Alexandre-T/doctrine2-spatial/badge.svg?branch=master&service=github)](https://coveralls.io/github/Alexandre-T/doctrine2-spatial?branch=master)
[![Downloads](https://img.shields.io/packagist/dm/Alexandre-T/doctrine2-spatial.svg)](https://packagist.org/packages/Alexandre-T/doctrine2-spatial)

### [Documentation](./doc/index.md)

### Installation

Update your composer.json to add this package:
```yaml
    "require": {
         ....
         "alexandret/doctrine2-spatial": "~1"
         ....
    }
```

You will also have to change the version requirement of doctrine to the stable version 2.7:
```yaml
   "doctrine/orm": ">=2.7",
```

Compatibility
-------------

**Doctrine dev version**

Continuous integration tests libraries with 2.8.x-dev version. We try to be compatible with this version.
Continuous integration tests libraries with 2.8.x-dev version. We **DO NOT* try to be compatible with this version, 
currently. There is too much difference between interface declarations.

**MySQL 5.7 and 8.0**

A lot of functions change their names between this two versions. Currently, tests works with MySQL5.7 and 
failed with MySQL8.0, [because function names have 
changed](https://stackoverflow.com/questions/60377271/why-some-spatial-functions-does-not-exists-on-my-mysql-server).

**MariaDB 10**

This version is not compatible with MariaDB version. Some spatial functions seems to work but their results are 
different from MySQL version (Contains function is a good example)

**PostgreSQL**

 
 