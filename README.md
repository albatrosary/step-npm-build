# npm-install step

Executes the `npm run build` command with leveraging the wercker cache mechanism
to improve installation time (optional).

If `npm run build` fails, it will be retried three times before failing, and
optionally the cache will be cleared in between.

## Options

- `clear-cache-on-failed` (optional, default: `true`) If npm fails, clear the
  cache before trying again.
- `use-cache` (optional, default: `true`) Use the npm cache.
- `options` (optional) Allow for passing arbitrary arguments to npm.

## Example

```yaml
build:
    steps:
        - npm-build
```

# License

The MIT License (MIT)

# Changelog

## 0.0.1

- Initial release
