# uv 0.7.20

## Commands

### uv add

`uv add <PACKAGES>`

*   add or update project dependencies

    *   `<DEPENDENCIES>` - dependency specifiers (`'django == 5.0.0'`)
    *   `--dev` - to the dev group as internal dependency (shorthand to `--group dev`)
    *   `--editable` - as editable
    *   `--group <GROUP>` - to the group as internal dependency (`dev`)
    *   `--index <INDEX>` - from the private PyPI index (`https://pypi.example.org/simple`)
    *   `--optional <EXTRA>` - to the extra as optional dependency (`cache`)
    *   `--package <PACKAGE>` - to the workspace member (`app-common`)

### uv build

`uv build`

*   build both sdist and wheel into `dist` directory

    *   `--all-packages` - all workspace members
    *   `--package <PACKAGE>` - only the workspace member (`app-api`)
    *   `--sdist` - only source distribution (`.tar.gz`)
    *   `--wheel` - only wheel (`.whl`)

### uv cache

`uv cache <COMMAND>`

*   manage global cache

    *   `clean` - remove all objects

        *   `[DEPENDENCIES]` - only the dependency names (`requests`)

    *   `dir` - show path to cache
    *   `prune` - remove unused objects

        *   `--ci` - remove aggressively for CI

### uv generate-shell-completion

`uv generate-shell-completion <SHELL>`

*   generate completion for the shell

    *   `<SHELL>` - shell name (`fish`)

### uv lock

`uv lock`

*   generate or update lock file

    *   `--check` - check if lock file is up-to-date
    *   `--dry-run` - show changes without writing lock file
    *   `--upgrade` - upgrade all packages within constraints
    *   `--upgrade-package <DEPENDENCY>` - upgrade only the dependency (`flask`)

### uv init

`uv init [PATH]`

*   create project structure in current working directory

    *   `[PATH]` - create in the path
    *   `--author-from none` - without `authors` in `pyproject.toml`
    *   `--bare` - only with minimal `pyproject.toml`
    *   `--build-backend uv` - using uv as build backend
    *   `--lib` - library structure
    *   `--name <NAME>` - using the name instead of directory name (`api`)
    *   `--no-description` - without description in `pyproject.toml`
    *   `--no-pin-python` - without `.python-version`
    *   `--no-readme` - without `README.md`
    *   `--no-workspace` - as standalone project
    *   `--python <PYTHON>` - using the Python version (`3.15`)
    *   `--vcs none` - without `.git` and `.gitignore`

### uv python

`uv python <COMMAND>`

*   manage Python versions

    *   `dir` - show path to installation directory
    *   `find` - show path to interpreter

        *   `[TARGET]` - for the Python version (`3.13`)
        *   `--show-version` - show resolved version instead of path
        *   `--system` - ignore project interpreter

    *   `install` - install latest version

        *   `[TARGETS]` - the Python versions (`3.12.11`)

    *   `list` - show latest supported versions

        *   `[TARGET]` - for the Python version (`3`)
        *   `--all-versions` - show all supported versions
        *   `--only-downloads` - only versions for download by uv
        *   `--only-installed` - only installed versions

    *   `pin` - show pinned project version

        *   `[TARGET]` - pin project version (`3.13.5`)
        *   `--global` - globally instead of project
        *   `--rm` - remove pinned version

    *   `uninstall` - uninstall version

        *   `<TARGETS>` - the Python versions (`3.11.13`)
        *   `--all` - all managed versions by uv

### uv pip

`uv pip <COMMAND>`

*   manage venv dependencies without modifying `pyproject.toml` and `uv.lock`

    *   `install` - add dependencies

        *   `<PACKAGES>` - dependency specifiers (`flask == 3.0.0`)

    *   `uninstall` - remove dependencies

        *   `<PACKAGES>` - dependency names (`flask`)

### uv publish

`uv publish`

*   publish builds to PyPI

    *   `[FILES]` - the builds to upload (default `dist/*`)
    *   `--index <INDEX>` - to the private PyPI instead
    *   `--token <TOKEN>` - using the auth token

### uv remove

`uv remove`

*   remove project dependencies

    *   `<DEPENDENCIES>` - dependency names (`ruff`)
    *   `--dev` - from the dev group (shorthand for `--group dev`)
    *   `--group <GROUP>` - from the group (`dev`)
    *   `--optional <EXTRA>` - from the extra (`cache`)
    *   `--package <PACKAGE>` - from the workspace member (`app-common`)

### uv run

`uv run`

*   show available commands

    *   `[COMMAND]` - run the command name or script (`main.py`)
    *   `--env-file <ENV_FILE>` - using environment variables from the file (`.env`)
    *   `--no-sync` - do not sync venv
    *   `--python <PYTHON>` - using specific Python version (`3.12`)

### uv sync

`uv sync`

*   create or update venv from lock file

    *   `--all-groups` - include all groups
    *   `--all-extras` - include all extras
    *   `--check` - check if venv is synchronized
    *   `--dry-run` - show changes without modifying venv
    *   `--group <GROUP>` - include the group (`test`)
    *   `--extra <EXTRA>` - include the extra (`cache`)
    *   `--no-dev` - exclude the dev group (synced by default)
    *   `--only-dev` - only dev group dependencies (shorthand to `--only-group dev`)
    *   `--only-group <GROUP>` - only the group (excludes project / workspace members)
    *   `--package <PACKAGE>` - include the workspace member (`app-common`)
    *   `--frozen` - do not modify lock file
    *   `--inexact` - do not remove extraneous dependencies via `uv pip install`
    *   `--no-install-project` - exclude project
    *   `--no-install-workspace` - exclude workspace members

### uv tree

`uv tree`

*   show project dependency tree

    *   `--all-groups` - include all groups
    *   `--depth <DEPTH>` - limit display depth (`1`)
    *   `--frozen` - do not modify lock file
    *   `--group <GROUP>` - include the group (`test`)
    *   `--invert` - reverse dependency tree
    *   `--no-dedupe` - no deduplication
    *   `--no-dev` - exclude the dev group (synced by default)
    *   `--only-dev` - only dev group dependencies (shorthand to `--only-group dev`)
    *   `--only-group <GROUP>` - only the group (excludes project / workspace members)
    *   `--outdated` - include latest available versions
    *   `--package <PACKAGE>` - only the package (dependency or workspace member)
    *   `--prune <PACKAGE>` - hide the package (dependency or workspace member)

### uv tool

`uv tool <COMMAND>`

*   manage globally Python tools (PyPI packages)

    *   `dir` - show path to installation directory

        *   `--bin` - show path to executables

    *   `install` - install tool or reinstall with different constraint

        *   `<PACKAGE>` - dependency specifier (`mkdocs == 1.0.0`)
        *   `--with <PACKAGE>` - include additional requirements (`mkdocs-material`)

    *   `list` - show installed tools

        *   `--show-extras` - include extras if installed too
        *   `--show-with` - include additional requirements if installed too

    *   `run` - show available installed tools

        *   `[TOOL]` - run the installed tool or temporarily install and run the tool if not found `ruff`
        *   `--env-file <ENV_FILE>` - using environment variables from the file (`.env`)
        *   `--from <PACKAGE>` - from the package if tool name differs (`httpie`)
        *   `--python <PYTHON>` - using specific Python version (`3.12`)
        *   `--with <PACKAGE>` - include additional requirements (`mkdocs-material`)

    *   `uninstall` - uninstall tools

        *   `<PACKAGES>` - dependency names (`mkdocs`)
        *   `--all` - all tools

    *   `upgrade` - upgrade tools within constraints

        *   `--all` - all tools

### uv version

`uv version`

*   show or update project version

    *   `[VERSION]` - set the version (`0.1.1`)
    *   `--bump <BUMP>` - update to the bump (`major`, `minor`, `patch`)
    *   `--dry-run` - show new version without modifying `pyproject.toml` and `uv.lock`
    *   `--package <PACKAGE>` - update the workspace member version (`app-common`)
    *   `--short` - only version without project name

### uvx

`uvx`

*   shorthand to `uv tool run`

## Settings

`pyproject.toml`

### [tool.uv] table

*   `default-groups` (str | list[str]) - group(s) to sync by default (`[ "dev" ]` by default or `"all"`)
*   `publish-url` (str) - PyPI location for uploading distributinos (`"https://upload.pypi.org/legacy/"` by default)
*   `required-version` (str) - minimal uv version (`null` by default)

### [tool.uv.build-backend] table

*   `module-name` (str | list[str]) - modules names under module root (`"app"`)
*   `module-root` (str) - module directory (`"src"` by default or `""` for flat directory)
*   `source-exclude` (list[str]) - files to exclude from distribution (`[ "README.md"]`)
*   `source-include` (list[str]) - files to include in distribution (`[ "src/**/*.json" ]`)

### [[tool.uv.index]] tables

*   `explicit` (bool) - use the index only for dependencies in uv sources (`false` by default)
*   `name` (str) - PyPI name (`company`)
*   `url` (str) - PyPI location (`https://pypi.example.org/simple`)

### [tool.uv.sources] table

*   `<DEPENDENCY>` (dict) - where to find the dependency (`{ index = private-pypi }`)

### [tool.uv.workspace] table

*   `members` (list[str]) - packages as workspace members (`[ "app-common", "app-api" ]`)

## Environment variables

*   `UV_CACHE_DIR` (str) - path to cache (`$HOME/.cache/uv` by default)
*   `UV_COMPILE_BYTECODE` (bool) - compile project after installation (`true` for containers)
*   `UV_ENV_FILE` (list[str]) - space separated list of env files (`.env`)
*   `UV_FROZEN` (bool) - no lock file modification (`true` for containers)
*   `UV_INDEX_{name}_PASSWORD` (str) - PyPI password for installation (`password`)
*   `UV_INDEX_{name}_USERNAME` (str) - PyPI username for installation (`__token__`)
*   `UV_LINK_MODE` (clone|copy|hardlink|symlink) - package installation method (`copy` for containers)
*   `UV_NATIVE_TLS` (bool) - use system certificates (`false` by default)
*   `UV_PROJECT_ENVIRONMENT` (str) - path to venv (`.venv` by default)
*   `UV_PUBLISH_PASSWORD` (str) - PyPI password for publishing (`password`)
*   `UV_PUBLISH_TOKEN` (str) - PyPI API token for publishing (`token`)
*   `UV_PUBLISH_USERNAME` (str) - PyPI username for publishing (`username`)
*   `UV_SYSTEM_PYTHON` (bool) - use system Python (`true` for containers)

## See also

*   [uv](https://docs.astral.sh/uv/)
*   [uv - Commands](https://docs.astral.sh/uv/reference/cli/)
*   [uv - Environment variables](https://docs.astral.sh/uv/reference/environment/)
*   [uv - Settings](https://docs.astral.sh/uv/reference/settings/)
