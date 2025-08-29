---
title: Markdown Examples
date: 2024-04-01
summary: This is a sample Markdown post. It demonstrates Markdown syntax and how it renders in Astro.
category: Examples
tags: [Markdown]
---

Below are some basic Markdown syntax examples you can use when writing content in Astro.

## Headings

You should avoid repeating the article title inside the Markdown body — the title is automatically generated from the `frontmatter` field `title`.

> Avoid nesting headings too deeply. Three levels are usually enough.

# H1

## H2

### H3 with `inline code`

#### H4

##### H5

###### H6

## Paragraphs

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Use two spaces at the end of a line to create a line break within a paragraph:

All work and no play makes Jack a dull boy.  
All work and no play makes Jack a dull boy.

## Images

Small image:

![Alt text](https://picsum.photos/seed/picsum/250/400)

Large image:

![Alt text](https://picsum.photos/seed/picsum/1200/900)

Image with caption:

![Alt text](https://picsum.photos/seed/picsum/400/300 'Image title')

## Emphasis

This is **important text**, this is _less important text_.

## Strikethrough

~~This text is deleted.~~

## Blockquotes

The blockquote element represents content quoted from another source. You can include citations in `footer` or `cite` elements, and also mix in inline formatting.

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Note** that you can use _Markdown syntax_ inside blockquotes.

Nested blockquote:

> Quote
>
> > Nested quote

With citation:

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is from Rob Pike’s [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) at Gopherfest, November 18, 2015.

## Horizontal Rule

---

## Links

Internal link: [Gyoza Guide](/posts/guide)

External link: [React **Docs**](https://react.dev/)

Auto-link: <https://github.com>

Email: <mail@example.com>

## Tables

With alignment:

| Name  | Age |  Fruit |
| :---- | :-: | -----: |
| Bob   | 27  |  Apple |
| Alice | 23  | Banana |
| John  | 28  | Orange |

Supports inline Markdown:

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

Table overflow example:

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------------- |
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

## Code Blocks

### Syntax

Use triple backticks ```to wrap code. To enable syntax highlighting, add the language name (e.g.`html`, `javascript`, `css`, `markdown`, `typescript`, `bash`) right after the opening backticks.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

```
const var text = "hello world"
```

## KaTeX Formulas

Wrap inline formulas with `$`, e.g. `$E = mc^2$`.

Use `$$` for block formulas:

$$
e^{i\pi} + 1 = 0
$$

Or use a code block with `math`:

```math
\oint_{\partial V} \mathbf{E} \cdot d\mathbf{A} = \frac{Q}{\epsilon_0}
```

## Lists

### Ordered List

#### Syntax

```markdown
1. First item
2. Second item
3. Third item
```

#### Output

1. First item
2. Second item
3. Third item

### Unordered List

#### Syntax

```markdown
- List item
- Another item
- And another item
```

#### Output

- List item
- Another item
- And another item

### Nested List

#### Syntax

```markdown
- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese
```

#### Output

- Fruit
  - Apple
  - Orange
  - Banana

- Dairy
  - Milk
  - Cheese

## Other Elements — abbr, sub, sup, kbd, mark

### Syntax

```markdown
<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
```

#### Output

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.

## Spoiler

```md
||hidden content||
```

By default, this content stays hidden: ||hidden content||. It only appears on hover.
