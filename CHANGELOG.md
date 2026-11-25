# Changelog

## Unreleased

### Development

- `composer test` runs `phpunit` without a path, so the `exclude` in `phpunit.xml.dist` applies. Passing `./tests` bypassed it, and CI tried to run `FunctionalTest.php`, which needs `Zend_Test`.

## 2.0.0

Fork of `diablomedia/zendframework1-layout`, published as `gizmocraft/zendframework1-layout`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-layout` to `gizmocraft/zendframework1-layout`. It now requires the `gizmocraft/zendframework1-*` packages `exception` `^2.0.0`, `config` `^3.0.0`, `loader` `^2.0.0`, `controller` `^2.0.0`, `filter` `^2.0.0` and `view` `^2.0.0`.

### Other changes

- No library code changes and no public signature changes were needed for PHP 8.5 and 8.6.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 (`#[Group]` and `#[DoesNotPerformAssertions]` attributes).
- CI runs PHP 8.5 and 8.6.
