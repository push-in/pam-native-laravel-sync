# pushinbr/pam-native-laravel-sync

This name is retained only for migration compatibility. The package is now
[`pushinbr/pam-native-sync-laravel`](https://packagist.org/packages/pushinbr/pam-native-sync-laravel).

## Start here

```bash
curl -fsSL https://push-in.github.io/pam/install.sh | sh
pam doctor
pam composer remove pushinbr/pam-native-laravel-sync
pam composer require pushinbr/pam-native-sync-laravel
```

Existing projects may keep resolving this package temporarily because it
depends on the replacement. New code must require `pushinbr/pam-native-sync-laravel` directly.
