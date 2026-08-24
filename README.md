<div align="center">

# pushinbr/pam-native-laravel-sync

## Compatibility package — do not use in new applications

This repository exists so older Composer projects keep installing safely. The maintained product is **[PAM Native Sync for Laravel](https://github.com/push-in/pam-native-sync-laravel)**.

[![Replacement](https://img.shields.io/badge/replacement-pushinbr/pam--native--sync--laravel-2563eb?style=flat-square)](https://packagist.org/packages/pushinbr/pam-native-sync-laravel)
![Status](https://img.shields.io/badge/status-migration%20only-f59e0b?style=flat-square)

</div>

---

## Use this instead

```bash
pam composer require pushinbr/pam-native-sync-laravel
```

[PAM Native Sync for Laravel](https://github.com/push-in/pam-native-sync-laravel) contains the active documentation, API examples, releases, issue tracker, and production guidance.

## Why the name changed

The canonical name groups the server adapter under PAM Native Sync and matches the `pam-native-<capability>-<adapter>` package convention.

## Migrate an existing project

Commit your current `composer.json` and `composer.lock`, then run:

```bash
pam composer remove pushinbr/pam-native-laravel-sync
pam composer require pushinbr/pam-native-sync-laravel
pam doctor
```

Run the application test suite before committing the new lockfile. Composer may continue to resolve this bridge transitively during a staged migration; application code should target the replacement package directly.

## Support policy

- No new features are added here.
- Security or resolution fixes may be published only to preserve migration safety.
- New documentation and issues belong to [PAM Native Sync for Laravel](https://github.com/push-in/pam-native-sync-laravel).
- The package is marked abandoned on Packagist in favor of `pushinbr/pam-native-sync-laravel`.

This explicit compatibility repository is intentional: old installs remain understandable without making the current PAM ecosystem ambiguous.
