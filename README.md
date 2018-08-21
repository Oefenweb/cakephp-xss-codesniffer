# Oefenweb Code Sniffer for CakePHP 2 (XSS)

This code works with [phpcs](https://github.com/squizlabs/PHP_CodeSniffer) and checks code against the coding standards used at Oefenweb.

## Installation

It's generally recommended to install these code sniffs with `composer`:

```sh
mkdir CakePHPXSSOefenweb && cd $_ && composer require oefenweb/cakephp-xss-codesniffer=^2.0.0;
```

```sh
vendor/bin/phpcs \
  --config-set installed_paths "${PWD}/vendor/cakephp/cakephp-codesniffer,${PWD}/vendor/oefenweb/cakephp-xss-codesniffer" \
;
```

This lets `phpcs` know where to find your new sniffs. Ensure that you do not overwrite any existing `installed_paths` value.

## Usage

```sh
vendor/bin/phpcs --standard=CakePHPXSSOefenweb ~/foo/bar/index.php;
```
