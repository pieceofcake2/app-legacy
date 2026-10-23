# CakePHP 2.x Application Skeleton

[![GitHub License](https://img.shields.io/github/license/pieceofcake2/app-legacy?label=License)](LICENSE)
[![Packagist Version](https://img.shields.io/packagist/v/pieceofcake2/app-legacy?label=Packagist)](https://packagist.org/packages/pieceofcake2/app-legacy)
![PHP](https://img.shields.io/packagist/dependency-v/pieceofcake2/app-legacy/php?logo=php&logoColor=%23FFFFFF&label=PHP&labelColor=%23777BB4&color=%23FFFFFF)
![CakePHP](https://img.shields.io/packagist/dependency-v/pieceofcake2/app-legacy/pieceofcake2/cakephp?logo=cakephp&logoColor=%23FFFFFF&label=CakePHP&labelColor=%23D33C43&color=%23FFFFFF)
[![PHPStan](https://img.shields.io/badge/PHPStan-level%205-brightgreen?label=PHPStan)](https://github.com/pieceofcake2/app-legacy/actions/workflows/CI.yml)

The application skeleton for CakePHP 2 applications running on
[pieceofcake2/cakephp](https://github.com/pieceofcake2/cakephp), with a directory layout
compatible with CakePHP 5 (`config/`, `src/`, `templates/`, `tests/`, `webroot/`), `.env`
support, and the home page, layouts, error pages and styles of the CakePHP 5 skeleton.

This skeleton keeps the application classes global and the templates as `.ctp` files. For an
application with namespaced classes (`App\`) and `.php` templates, use
[pieceofcake2/app](https://github.com/pieceofcake2/app).

> [!WARNING]
> CakePHP 2.x is for the maintenance of existing applications. For new projects, use
> the current major version of CakePHP instead.

## Documentation

The documentation is the [Application Skeleton with Global Classes](https://pieceofcake2.github.io/docs/installation/application-skeleton-legacy.html)
page of the CakePHP 2 book (日本語: https://pieceofcake2.github.io/docs/ja/installation/application-skeleton-legacy.html;
Markdown: [en](https://github.com/pieceofcake2/docs/blob/2.x/docs/en/installation/application-skeleton-legacy.md),
[ja](https://github.com/pieceofcake2/docs/blob/2.x/docs/ja/installation/application-skeleton-legacy.md)).
It covers what differs from pieceofcake2/app and links the shared sections: the installation,
the configuration and `.env` files, the pages and styles, and running tests and PHPStan. To move
an existing application to the modern layout, see
[Migrating to the Modern Layout](https://pieceofcake2.github.io/docs/appendices/migrating-to-the-modern-layout.html).

For AI coding tools, the Markdown docs of the CakePHP 2 book are installed as a dev dependency (`pieceofcake2/docs`, files in `vendor/pieceofcake2/docs/docs/en/`).

## Requirements

- PHP 8.0+
- Composer
- MySQL 5.6+, PostgreSQL 9.4+, SQLite 3 or SQL Server 2022+

## Installation

```bash
composer create-project pieceofcake2/app-legacy my_app
```

Then copy `config/database.php.default` to `config/database.php`, set the database with
`DATABASE_URL` in `config/.env.local` (and the test database in `config/.env.test.local`) or
the environment, and
change the security salts in `config/core.php` (see
[Generating the Security Salts](https://pieceofcake2.github.io/docs/installation/application-skeleton.html#generating-the-security-salts)).

The Bake and DebugKit plugins are development dependencies. `config/bootstrap.php` loads
them when they are installed, so `bin/cake bake` works out of the box and
`composer install --no-dev` still works in production.

## Contributing

See the [contribution guidelines](https://github.com/pieceofcake2/.github/blob/master/CONTRIBUTING.md).

## Origin

This package is based on the `app/` directory of
[cakephp/cakephp](https://github.com/cakephp/cakephp) (`cakephp/cakephp` on Packagist, last upstream
version 2.10.24), originally by the CakePHP community (Cake Software Foundation, Inc.). It was
extracted into a separate package and is maintained for CakePHP 2 on modern PHP by
[pieceofcake2](https://github.com/pieceofcake2). Changes from the original are listed in the
[commit history](https://github.com/pieceofcake2/app-legacy/commits/2.x).

## License

Licensed under the MIT License. See [LICENSE](LICENSE).

`webroot/css/normalize.min.css` (normalize.css) and `webroot/css/milligram.min.css`
(Milligram) are MIT licensed, see their headers. The Raleway font in `webroot/font/` is
licensed under the SIL Open Font License 1.1, see `webroot/font/Raleway-License.txt`.
