# Dependency specifiers cheat sheet

```
<DEPENDENCY> [EXTRAS] [VERSION_SPECIFIERS] [; ENVIRONMENT_MARKERS]
<DIRECT_REFERENCE> [; ENVIRONMENT_MARKERS]
```

## Dependency

```
kebab-case  # pytest-cov
```

## Extras

```
[extra]              # celery[auth]
[extra1,extra2,...]  # celery[memcache,redis]
```

## Version specififers

```
<OPERATOR> <VERSION>       # django==5.0.0
<OPERATOR> <VERSION>, ...  # django>=5.0.0,!=5.0.1
```

## Environment markers

```
; <VARIABLE> <OPERATOR> "<VALUE>"                    # flask;python_version>"3.13"
; <VARIABLE> <OPERATOR> "<VALUE>" and ...
; <VARIABLE> <OPERATOR> "<VALUE>" or ...
; (<VARIABLE> <OPERATOR> "<VALUE>" and ... ) or ...
```

### Variables

*   `platform_machine` (str) - architecture (`aarch64`, `arm64`, `x86_64`)
*   `platform_system` (str) - operating system (`Darwin`, `Linux`, `Windows`)
*   `python_version` (str) - X.Y version (`3.13`)

## See also

*   [PyPA Dependency specifiers](https://packaging.python.org/en/latest/specifications/dependency-specifiers/)
*   [Version specifiers](/python/pypa/version-specifiers.md)
