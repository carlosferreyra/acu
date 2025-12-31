# ACU CLI Roadmap (Draft)

Planned CLI surface aligned with the infra model and validation rules.

## Core Commands

- init: scaffold a new infra file; flags --name, --version, --with-scopes, --with-connections.
- add resource: add a typed resource with defaults; flags --type, --id, --name, --label key=val,
  --property key=val, --no-defaults.
- add connection: connect two resources; flags --from, --to, --kind, --property key=val.
- add scope: create a scope and members; flags --id, --member id, --purpose.
- list types: show allowed resource types and defaults; flags --json, --yaml.
- list kinds: show allowed connection kinds.
- inspect: display a resource or scope; flags --file, --id, --show-defaults, --show-connections.

## Validation and Formatting

- validate: check types/kinds, uniqueness, required fields; flags --file, --strict,
  --no-default-fill, --schema-version.
- fmt: normalize ordering/indentation; flags --in-place, --check.
- plan: show defaults that would be applied plus inferred values; flags --file, --output json|yaml,
  --diff.
- apply: write a file with defaults applied; flags --file, --out, --backup, --force.
- lint: opinionated checks (naming, label conventions, required values); flags --file, --ruleset,
  --ignore.

## Diffing and Conversion

- diff: compare two infra files or working vs formatted/defaulted; flags --from, --to, --format
  unified|json.
- convert: translate between yaml/json; flags --in, --out.
- schema export: emit JSON Schema/OpenAPI for the spec; flags --version, --out.

## Visualization and Examples

- graph: render connection graph; flags --file, --format dot|mermaid|png, --focus id, --kinds.
- generate examples: emit snippets per resource type or connection kind; flags --type, --kind,
  --out.
- stats: summarize counts by type/kind/labels; flags --file, --by type|label|scope.

## Common Flags

- -f/--file: input infra file (default infra.yml).
- -o/--out: output path.
- --set key=val: override top-level fields (e.g., version/name).
- -v/--verbose, -q/--quiet, --color auto|never|always.
- --strict: fail on unknown fields or undeclared types/kinds.
- --no-default-fill: validate without auto-injecting defaults.
- --schema-version: choose spec version.
- --format json|yaml: control output format.
