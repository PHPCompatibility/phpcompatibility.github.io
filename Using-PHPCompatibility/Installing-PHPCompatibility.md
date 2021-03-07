---
sort: 2
---

# Installing PHPCompatibility

## Requirements

* PHP 5.4+
* [PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer): 2.6.0+ or 3.1.0+.

The sniffs are designed to give the same results regardless of which PHP version you are using to run PHP CodeSniffer. You should get consistent results independently of the PHP version used in your test environment, though for the best results it is recommended to run the sniffs on a recent PHP version in combination with a recent PHP_CodeSniffer version.

As the underlying code of PHP_CodeSniffer has needed updates for cross-version PHP compatibility over time as well, please take the following guidelines into account

PHP | PHP_CodeSniffer runtime support | PHP_CodeSniffer syntax support
--- | --- | ---
PHP 5.4 | PHPCS 2.6.0+ or 3.1.0+ |
PHP 5.5 - 7.2 | PHPCS 2.6.0+ or 3.1.0+ | PHPCS >= 3.1.0
PHP 7.3 | PHPCS >= 3.3.1 | PHPCS >= 3.3.1
PHP 7.4 | PHPCS >= 3.5.0 | PHPCS >= 3.5.6
PHP 8.0 | PHPCS >= 3.5.7 | PHPCS >= 3.6.0


## Before you install

**TODO**: _add some information about the polyfill rulesets_

{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}]({{ repository.html_url }})
{% endfor %}


## Installation in a Composer project

From the root directory of the project, run:
```bash
composer require {{ site.mainrepo.packagist }}:"^{{ site.mainrepo.version }}"
```

Composer will install all project dependencies, including PHP_CodeSniffer and will register itself with PHP_CodeSniffer.


## Composer system global installation

Run:
```bash
composer global require {{ site.mainrepo.packagist }}:"^{{ site.mainrepo.version }}"
```

```tip
Make sure the `bin` directory of the Composer global home directory has been added to your system `$PATH` to make the `phpcs` command available system-wide.

To find out where the Composer global home directory is located, run:
`composer global config bin-dir --absolute`
```

## Updating PHPCompatibility

Run:
```bash
composer [global] update {{ site.mainrepo.packagist }} --update-with-dependencies
```

It is important to always use `--update-with-dependencies` to make sure the underlying project dependencies are also updated.


## Verifying your installation

For a project based install, run the following from the root directory of the project:
```bash
vendor/bin/phpcs -i
```

For a global install, run:
```bash
phpcs -i
```

If all went well, `PHPCompatibility` will be listed as one of the available standards.

Typically the output of the command will look something like:
```
The installed coding standards are MySource, PEAR, PSR1, PSR12, PSR2, Squiz, Zend and PHPCompatibility
```
