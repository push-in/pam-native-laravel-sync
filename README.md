<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset=".github/assets/banner-dark.svg">
  <img src=".github/assets/banner-light.svg" width="880" alt="pam-native-laravel-sync: Compatibility package: use pushinbr/pam-native-sync-laravel.">
</picture>

**Compatibility package: do not use in new applications.**<br>
It exists so older Composer projects keep installing safely. The maintained product is [PAM Native Sync for Laravel](https://github.com/push-in/pam-native-sync-laravel).

[![Packagist](https://img.shields.io/packagist/v/pushinbr/pam-native-laravel-sync?label=packagist&color=f53003)](https://packagist.org/packages/pushinbr/pam-native-laravel-sync)
![PHP 8.5](https://img.shields.io/badge/php-8.5-777bb4)
[![License](https://img.shields.io/github/license/push-in/pam-native-laravel-sync?color=1f6feb)](LICENSE)
[![Replacement](https://img.shields.io/badge/replacement-pushinbr%2Fpam--native--sync--laravel-f53003)](https://packagist.org/packages/pushinbr/pam-native-sync-laravel)
![Status](https://img.shields.io/badge/status-migration%20only-e3a008)

[Use this instead](#install) · [Migrate](#migrate) · [Support policy](#support-policy) · [Replacement](https://github.com/push-in/pam-native-sync-laravel)

</div>

<a id="install"></a>
## <picture><img src=".github/assets/icons/terminal.svg" width="22" height="22" alt=""></picture> Install

Use the replacement in the Laravel backend instead (on a PAM-served Laravel app, `pam init my-api --template laravel`):

```sh
pam composer require pushinbr/pam-native-sync-laravel
```

[PAM Native Sync for Laravel](https://github.com/push-in/pam-native-sync-laravel) contains the active documentation, API examples, releases, issue tracker, and production guidance.

<a id="migrate"></a>
## <picture><img src=".github/assets/icons/cloud-sync.svg" width="22" height="22" alt=""></picture> Migrate an existing project

Commit your current `composer.json` and `composer.lock`, then run:

```sh
pam composer remove pushinbr/pam-native-laravel-sync
pam composer require pushinbr/pam-native-sync-laravel
pam doctor
```

Run the application test suite before committing the new lockfile. Composer may continue to resolve this bridge transitively during a staged migration (it requires `pushinbr/pam-native-sync-laravel` `^0.2`); application code should target the replacement package directly.

**Why the name changed:** the canonical name groups the server adapter under PAM Native Sync and matches the `pam-native-<capability>-<adapter>` package convention.

<a id="support-policy"></a>
## <picture><img src=".github/assets/icons/shield.svg" width="22" height="22" alt=""></picture> Support policy

- No new features are added here.
- Security or resolution fixes may be published only to preserve migration safety.
- New documentation and issues belong to [PAM Native Sync for Laravel](https://github.com/push-in/pam-native-sync-laravel).
- The package is marked abandoned on Packagist in favor of `pushinbr/pam-native-sync-laravel`.

This explicit compatibility repository is intentional: old installs remain understandable without making the current PAM ecosystem ambiguous.

<a id="pam-ecosystem"></a>
## <picture><img src=".github/assets/icons/plug.svg" width="22" height="22" alt=""></picture> Part of the PAM ecosystem

<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset=".github/assets/pam-wordmark-dark.svg">
  <img src=".github/assets/pam-wordmark-light.svg" height="56" alt="PAM">
</picture></p>

PAM runs PHP natively on servers, desktops and phones. This repository is one piece of it.

| [**PAM**](https://github.com/push-in/pam) | [**PAM Desktop**](https://github.com/push-in/pam-desktop) | [**PAM Native**](https://github.com/push-in/pam-native) | [**Ecosystem**](https://github.com/push-in/pam#ecosystem) |
| --- | --- | --- | --- |
| the runtime and CLI | native desktop apps in PHP | native Android and iOS apps in PHP | every official package and plugin |

<sub>Docs: [push-in.github.io/pam-docs](https://push-in.github.io/pam-docs/introduction/) · [Issues](https://github.com/push-in/pam-native-laravel-sync/issues)</sub>

<p align="center"><sub><a href="LICENSE">Apache License 2.0</a> · Made in Brazil by Pushin</sub></p>
