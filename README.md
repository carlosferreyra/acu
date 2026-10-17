# ACU — infrastructure project retired

ACU's infrastructure work continues in [SCU — System Composition Utility](https://github.com/carlosferreyra/scu).
Follow SCU's README for its current status and installation instructions.

ACU was an early prototype. Its proposed infrastructure commands and provider integrations were not implemented.
Version 0.1.7 replaces the greeting scaffold with a migration notice:

```sh
uvx acu
# or, for an existing installation:
uv tool upgrade acu
acu --help
```

Every invocation prints the notice and exits successfully. ACU does not install or execute SCU.
The retirement release is pure Python and requires Python 3.14 or newer.

## Historical design

The [historical design index](docs/README.md) preserves ACU's proposed YAML model,
resource types, and CLI roadmap. These are unimplemented proposals, not SCU's specification.
Earlier source remains available in Git history and earlier PyPI releases remain available.

## Future of this package

The ACU infrastructure project is inactive and this repository will be archived after the
retirement release is verified. The PyPI project is retained; the name may be reused for a
different purpose in a clearly announced future release. It is not a permanent alias for SCU.

To resume work, unarchive the repository, update the documentation and package metadata,
review the publishing workflow, and explicitly re-enable publishing before releasing.
