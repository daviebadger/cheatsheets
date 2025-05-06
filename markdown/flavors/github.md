# GitHub Flavored Markdown (GFM) cheat sheet

## Blocks

### Container blocks

#### Alerts

*   note

    ```markdown
    > [!NOTE]
    > text
    ```

*   tip

    ```markdown
    > [!TIP]
    > text
    ```

*   important

    ```markdown
    > [!IMPORTANT]
    > text
    ```

*   warning

    ```markdown
    > [!WARNING]
    > text
    ```

*   caution

    ```markdown
    > [!CAUTION]
    > text
    ```

#### Collapsed sections

```markdown
<details>
<summary>Summary</summary>

text

</details>
```

#### Task lists

```markdown
- [x] done
- [ ] to do
    - [ ] nested
          to do
```

### Leaf blocks

#### Code blocks

*   diagram via Mermaid

    ````markdown
    ```mermaid
    flowchart LR
        start --> stop
    ```
    ````

    ````
    ```mermaid
      version
    ```
    ````

*   syntax highlight via Linquist

    ````markdown
    ```markdown
    # Highlighted Markdown Code
    ```
    ````

#### Math blocks

*   LaTeX/Mathematics via MathJax

    ```markdown
    $$
    \sqrt{4}
    $$
    ```

#### Tables

```markdown
| Left-aligned | Center-aligned | Right-aligned |
| :----------- | :------------: | ------------: |
| A1           |       A2       |            A3 |
```

## Inlines

### Colors

(discussions, issues, pull requests)

```markdown
`#000000`
`rgb(0, 0, 0)`
```

### Emojis

```markdown
:+1:
```

### Emphasis

```markdown
<ins>underline</ins>
<sub>subscript</sub>
<sup>superscript</sup>
~~strikethrough~~
```

### Footnotes

```markdown
[^reference]

[^reference]: text
```

### Inline math

*   LaTeX/Mathematics via MathJax

    ```markdown
    $n^2$
    ```

### Keywords

*   close issue (pull request description)

    ```markdown
    Closes #issue_id
    Closes organization/repository#issue_id
    Closes user/repository#issue_id
    ```

*   mark duplicate (issue or pull request comment)

    ```markdown
    Duplicate of #issue_id
    Duplicate of #pull_request_id
    ```

### Links

*   anchor

    ```markdown
    <a name="my-anchor"></a>

    [Link to my anchor][#my-anchor]
    ```

*   autolink

    ```markdown
    URI
    ```

*   commit

    ```markdown
    SHA

    organization/repository@SHA
    user/repository@SHA
    ```

*   heading

    ```markdown
    # Title

    ## First section

    [text](#title)
    [text](#first-section)
    ```

*   discussion or issue or pull request (discussions, issues, pull requests)

    ```markdown
    #discussion_id
    #issue_id
    #pull_request_id

    organization/repository#id
    user/repository#id
    ```

*   path

    ```markdown
    [text](/root/file.txt)
    ```

### Mentions

*   organization or user

    ```markdown
    @organization
    @user
    ```

*   organization's team

    ```markdown
    @organization/team
    ```

## See also

*   [Emoji cheat sheet](https://github.com/ikatyang/emoji-cheat-sheet)
*   [GitHub - Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github)
*   [GitHub Linguist - Languages](https://github.com/github-linguist/linguist/blob/main/lib/linguist/languages.yml)
*   [LaTeX/Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)
*   [Mermaid diagrams](https://mermaid.js.org/intro/#diagram-types)
