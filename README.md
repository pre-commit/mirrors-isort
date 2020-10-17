This mirror repository is deprecated, use [isort] directly.

[isort]: https://github.com/PyCQA/isort

isort mirror
============

Mirror of isort package for pre-commit.

For pre-commit: see https://github.com/pre-commit/pre-commit

For isort: see https://github.com/PyCQA/isort


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

You may find [seed-isort-config](https://github.com/asottile/seed-isort-config)
useful!
