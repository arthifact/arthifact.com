---
title: "A post of Markdown elements"
description: "This post is for testing and listing a number of different markdown elements"
topic: "A"
publishDate: "22 Feb 2023"
updatedDate: 22 Jan 2024
tags: ["astro"]
---

## This is a H2 Heading

### This is a H3 Heading

#### This is a H4 Heading

##### This is a H5 Heading

###### This is a H6 Heading

## Horizontal Rules

---

---

---

## Emphasis

**This is bold text**

_This is italic text_

~~Strikethrough~~

## Quotes

"Double quotes" and 'single quotes'

## Blockquotes

> Blockquotes can also be nested...
>
> > ...by using additional greater-than signs right next to each other...

## References

An example containing a clickable reference[^1] with a link to the source.

Second example containing a reference[^2] with a link to the source.

[^1]: Reference first footnote with a return to content link.

[^2]: Second reference with a link.

If you check out this example in `src/content/post/markdown-elements/index.md`, you'll notice that the references and the heading "Footnotes" are added to the bottom of the page via the [remark-rehype](https://github.com/remarkjs/remark-rehype#options) plugin.

## Lists

Unordered

- Create a list by starting a line with `+`, `-`, or `*`
- Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    - Ac tristique libero volutpat at
    - Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
- Very easy!

Ordered

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

4. You can use sequential numbers...
5. ...or keep all the numbers as `1.`

Start numbering with offset:

57. foo
1. bar

## Code

Inline `code`

Indented code

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code

Block code "fences"

```
Sample text here...
```

Syntax highlighting

```js
var foo = function (bar) {
	return bar++;
};

console.log(foo(5));
```

### Expressive code examples

Adding a title

```js title="file.js"
console.log("Title example");
```

A bash terminal

```bash
echo "A base terminal example"
```

Highlighting code lines

```js title="line-markers.js" del={2} ins={3-4} {6}
function demo() {
	console.log("this line is marked as deleted");
	// This line and the next one are marked as inserted
	console.log("this is the second inserted line");

	return "this line uses the neutral default marker type";
}
```

[Expressive Code](https://expressive-code.com/) can do a ton more than shown here, and includes a lot of [customisation](https://expressive-code.com/reference/configuration/).

## Tables

| Option | Description                                                               |
| ------ | ------------------------------------------------------------------------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default.    |
| ext    | extension to be used for dest files.                                      |

### Table Alignment

| Item         | Price | # In stock |
| ------------ | :---: | ---------: |
| Juicy Apples | 1.99  |        739 |
| Bananas      | 1.89  |          6 |

### Keyboard elements

| Action                | Shortcut                                   |
| --------------------- | ------------------------------------------ |
| Vertical split        | <kbd>Alt+Shift++</kbd>                     |
| Horizontal split      | <kbd>Alt+Shift+-</kbd>                     |
| Auto split            | <kbd>Alt+Shift+d</kbd>                     |
| Switch between splits | <kbd>Alt</kbd> + arrow keys                |
| Resizing a split      | <kbd>Alt+Shift</kbd> + arrow keys          |
| Close a split         | <kbd>Ctrl+Shift+W</kbd>                    |
| Maximize a pane       | <kbd>Ctrl+Shift+P</kbd> + Toggle pane zoom |

## Images

Image in the same folder: `src/content/post/markdown-elements/logo.png`

![Astro theme cactus logo](./logo.png)

## Links

[Content from markdown-it](https://markdown-it.github.io/)


## What are admonitions

Admonitions (also known as “asides”) are useful for providing supportive and/or supplementary information related to your content.

## How to use them

To use admonitions in Astro Cactus, wrap your Markdown content in a pair of triple colons `:::`. The first pair should also include the type of admonition you want to use.

For example, with the following Markdown:

```md
:::note
Highlights information that users should take into account, even when skimming.
:::
```

Outputs:

:::note
Highlights information that users should take into account, even when skimming.
:::

## Admonition Types

The following admonitions are currently supported:

- `note`
- `tip`
- `important`
- `warning`
- `caution`

### Note

```md
:::note
Highlights information that users should take into account, even when skimming.
:::
```

:::note
Highlights information that users should take into account, even when skimming.
:::

### Tip

```md
:::tip
Optional information to help a user be more successful.
:::
```

:::tip
Optional information to help a user be more successful.
:::

### Important

```md
:::important
Crucial information necessary for users to succeed.
:::
```

:::important
Crucial information necessary for users to succeed.
:::

### Caution

```md
:::caution
Negative potential consequences of an action.
:::
```

:::caution
Negative potential consequences of an action.
:::

### Warning

```md
:::warning
Critical content demanding immediate user attention due to potential risks.
:::
```

:::warning
Critical content demanding immediate user attention due to potential risks.
:::

## Customising the admonition title

You can customise the admonition title using the following markup:

```md
:::note[My custom title]
This is a note with a custom title.
:::
```

Outputs:

:::note[My custom title]
This is a note with a custom title.
:::

## GitHub Repository Cards
You can add dynamic cards that link to GitHub repositories, on page load, the repository information is pulled from the GitHub API.

::github{repo="chrismwilliams/astro-theme-cactus"}

You can also link a Github user:

::github{user="withastro"}

To use this feature you just use the "Github" directive:

```markdown title="Linking a repo"
::github{repo="chrismwilliams/astro-theme-cactus"}
```

```markdown title="Linking a user"
::github{user="withastro"}
```
