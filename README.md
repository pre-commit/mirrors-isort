isort mirror
============

Mirror of isort package for pre-commit.

For pre-commit: see https://github.com/pre-commit/pre-commit

For isort: see https://github.com/timothycrosley/isort


### Using isort with pre-commit

Add this to your `.pre-commit-config.yaml`:

```yaml
-   repo: https://github.com/pre-commit/mirrors-isort
    rev: ''  # Use the revision sha / tag you want to point at
    hooks:
    -   id: isort
```

### classification of imports

`isort` isn't always the best at classifying imports.

As of 4.3.5, `isort` now supports reading from project metadata in
order to identify which imports are third-party. To enable this, add
the requirements mentioned in
https://github.com/timothycrosley/isort/blob/develop/pyproject.toml#L39
for the appropriate metadata format you want. For example, for
`requirements.txt` support:

```yaml
-   repo: https://github.com/pre-commit/mirrors-isort
    rev: ''  # Use the revision sha / tag you want to point at
    hooks:
    -   id: isort
        additional_dependencies: [pipreqs, pip-api]
```

You may also find
[seed-isort-config](https://github.com/asottile/seed-isort-config)
useful for the same purpose.
