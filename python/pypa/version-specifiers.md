# Version specifiers cheat sheet

## Version scheme

1.  dev release

    ```
    <RELEASE_SEGMENT>.devN  # 1.0.0.dev0
    ```

1.  pre-release (alpha, beta, release candidate)

    ```
    <RELEASE_SEGMENT>.aN   # 1.0.0.a1
    <RELEASE_SEGMENT>.bN   # 1.0.0.b1
    <RELEASE_SEGMENT>.rcN  # 1.0.0.rc1
    ```

1.  final release (CalVer, SemVer)

    ```
    X      # 1
    X.Y    # 1.0
    X.Y.Z  # 1.0.0
    ```

1.  post-release

    ```
    <RELEASE_SEGMENT>.postN  # 1.0.0.post1
    ```

## Version specifiers

*   `==` - equal to
*   `!=` - not equal to
*   `<` - less than
*   `>` - greater than
*   `<=` - less than or equal to
*   `>=` - greater than or equal to
*   `,` - logical AND

## Direct references

*   file

    ```
    file://host/path
    file:///path
    ```

*   Git

    ```
    git+https://github.com/user/repo.git@branch
    git+https://github.com/user/repo.git@commit
    git+https://github.com/user/repo.git@tag

    https://github.com/user/repo.git
    https://github.com/user/repo.git#egg=name
    https://github.com/user/repo.git#egg=name[extra]
    https://github.com/user/repo.git#egg=name&subdirectory=path/to/package
    https://github.com/user/repo.git#subdirectory=path/to/package
    ```

*   URL

    ```
    https://example.org/archive.tar.gz
    https://example.org/archive.zip
    https://example.org/wheel.whl
    ```

## See also

*   [Calendar Versioning (CalVer)](https://calver.org)
*   [PyPA Version specifiers](https://packaging.python.org/en/latest/specifications/version-specifiers)
*   [Semantic Versioning (SemVer)](https://semver.org)
