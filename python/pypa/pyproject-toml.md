# pyproject.toml

## [build-system] table

*   required

    *   `build-backend` (str) - Python path to build object (`uv_build`)
    *   `requires` (list[str]) - version specifiers (`[ "uv_build == 0.7.15" ]`)

## [dependency-groups] table

*   `<GROUP>` (list[str | dict]) - dependency specifiers for internal development (`test = [ "pytest", { include-group = "dev" } ]`)

## [project] table

*   required

    *   `name` (str) - kebab-case name (`pytest-mock`)
    *   `version` (str) - version specifier (`1.0.0`)

*   optional

    *   `authors` (list[dict[str, str]]) - tables with `name` and `email` keys (`[ { name = "Name", email = "email" } ]`)
    *   `classifiers` - PyPI classifiers (`Topic :: Utilities`)
    *   `dependencies` (list[str]) - required dependency specifiers (`[ "pytest >= 8" ]`)
    *   `description` (str) - oneline summary (`pytest plugin for X`)
    *   `license` (str) - license expression (`MIT`)
    *   `keywords` (list[str]) - tags (`[ "pytest", "plugin" ]`)
    *   `maintainers` (list[dict[str, str]]) - tables with `name` and `email` keys  (`[ { name = "Name", email = "email" } ]`)
    *   `requires-python` (str) - version specifier (`>= 3.13.5, <4`)
    *   `readme` (str) - relative path to README (`README.md`)

### [project.entry-points.\*] table

*   optional

    *   `*` - entry point group (`[project.entry-points.pytest11]`)
    *   `<NAME>` (str) - Python path to object (`pytest_mock = "pytest-mock"`)

### [project.optional-dependencies] table

*   optional

    *   `<EXTRA>` (list[str]) - optional dependency specifiers per extra (`redis = ["redis"]`)

### [project.scripts] table

*   optional

    *   `<COMMAND>` (str) - Python path to CLI object (`script = "package.cli:main"`)

### [project.urls] table

*   optional

    *   `changelog` (str) - changes (`https://github.com/user/repo/blob/main/CHANGELOG.md`)
    *   `documentation` (str) - docs (`https://docs.example.org`)
    *   `download` (str) - download (`https://github.com/user/repo/releases/latest`)
    *   `funding` (str) - sponsor (`https://github.com/sponsors/user`)
    *   `homepage` (str) - homepage (`https://example.org`)
    *   `issues` (str) - issue tracker (`https://github.com/user/repo/issues`)
    *   `releasenotes` (str) - release notes (`https://github.com/user/repo/releases`)
    *   `source` (str) - source code (`https://github.com/user/repo`)
    *   `*` (str) - custom label (`Discord = "https://discord.com"`)

## [tool.\*] tables

*   optional

    *   `*` - tools from PyPI (`[tool.ruff]`)

## See also

*   [PyPA Dependency groups](https://packaging.python.org/en/latest/specifications/dependency-groups/)
*   [PyPA License expression](https://packaging.python.org/en/latest/specifications/license-expression/)
*   [PyPA pyproject.toml specification](https://packaging.python.org/en/latest/specifications/pyproject-toml/)
*   [PyPA Well-known project URLs in metadata](https://packaging.python.org/en/latest/specifications/well-known-project-urls/)
*   [PyPI Classifiers](https://pypi.org/classifiers/)
