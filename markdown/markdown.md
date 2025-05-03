# Markdown (CommonMark) 0.31.2 cheat sheet

## Blocks

### Container blocks

#### Block quotes

```markdown
> First paragraph
>
> Second paragraph
> > Nested paragraph
```

#### Lists

*   bullet list

    ```markdown
    *   first item
    *   second
        item
        *   nested item
    ```

*   ordered list

    ```markdown
    1.  first item
    1.  second
        item
        1. nested item
    ```

### Leaf blocks

#### Code blocks

````markdown
```
code
```
````

#### Headings

```markdown
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
```

#### HTML blocks

```markdown
<!-- comment -->
```

#### Paragraphs

```markdown
First paragraph.

Second paragraph.
```

#### Thematic breaks

```markdown
---
```

## Inlines

### Code spans

```markdown
`code`
```

### Emphasis

```markdown
*italic*
**bold**
***bold and italic***
```

### Escapes

```markdown
\*not emphasized*
```

### Images

*   inline image link with(out) alt text

    ```markdown
    ![](URI)
    ![alt text](URI)
    ```

*   full image reference link with(out) alt text

    ```markdown
    ![][reference]
    ![alt text][reference]

    [reference]: URI
    ```

*   shortcut image reference link

    ```markdown
    ![alt text]

    [alt text]: URI
    ```

### Line breaks

*   hard

    ```markdown
    line\
    break
    ```

*   soft

    ```markdown
    line
    break
    ```

### Links

*   autolink

    ```markdown
    <URI>
    <email_address>
    ```

*   inline link

    ```markdown
    [text](URI)
    ```

*   full reference link

    ```markdown
    [text][reference]

    [reference]: URI
    ```

*   shortcut reference link

    ```markdown
    [text]

    [text]: URI
    ```

### Raw HTML

```markdown
H<sub>2</sub>O
```

## See also

*   [CommonMark](https://commonmark.org)
*   [CommonMark - Spec 0.31.2](https://spec.commonmark.org/0.31.2/)
