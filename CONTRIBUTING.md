# Contributing

ACU's infrastructure project is retired. Please direct infrastructure development and
issues to [SCU](https://github.com/carlosferreyra/scu).

The documents in `docs/` are preserved historical proposals, not implemented features.
The repository may be unarchived for a future, separately announced purpose for ACU.

To verify the retirement package locally:

```sh
uv build
uvx --from ./dist/acu-0.1.7-py3-none-any.whl acu --help
```
