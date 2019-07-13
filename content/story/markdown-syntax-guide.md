---
title: "Markdown Syntax Guide"
date: 2019-07-12T21:41:16+07:00
tags: []
categories: []
draft: false
series: "getting-started"
---

This article offers a sample of basic Markdown syntax that can be used in Hugo content files, also it shows whether basic HTML elements are decorated with CSS in a Hugo theme.
<!--more-->

## Headings

The following HTML `<h1>`—`<h6>` elements represent six levels of section headings. `<h1>` is the highest section level while `<h6>` is the lowest.

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Paragraph

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Blockquotes

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

#### Blockquote without attribution

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.

#### Blockquote with attribution

> Don't communicate by sharing memory, share memory by communicating.</p>
> — <cite>Rob Pike[^1]</cite>


[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tables

Tables aren't part of the core Markdown spec, but Hugo supports supports them out-of-the-box.

   Name | Age
--------|------
    Bob | 27
  Alice | 23

#### Inline Markdown within tables

| Inline&nbsp;&nbsp;&nbsp;     | Markdown&nbsp;&nbsp;&nbsp;  | In&nbsp;&nbsp;&nbsp;                | Table      |
| ---------- | --------- | ----------------- | ---------- |
| *italics*  | **bold**  | ~~strikethrough~~&nbsp;&nbsp;&nbsp; | `code`     |

## Code Blocks

#### Code block with backticks

```html
<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="utf-8" />
<link rel="icon" href="favicon.png" />
<title>Line Numbers ▲ Prism plugins</title>
<base href="../.." />
<link rel="stylesheet" href="style.css" />
<link rel="stylesheet" href="themes/prism.css" data-noprefix />
<link rel="stylesheet" href="plugins/line-numbers/prism-line-numbers.css" data-noprefix />
<script src="scripts/prefixfree.min.js"></script>

<script>var _gaq = [['_setAccount', 'UA-33746269-1'], ['_trackPageview']];</script>
<script src="https://www.google-analytics.com/ga.js" async></script>
</head>
<body>

<header>
  <div class="intro" data-src="templates/header-plugins.html" data-type="text/html"></div>

  <h2>Line Numbers</h2>
  <p>Line number at the beginning of code lines.</p>
</header>

<section class="language-markup">
  <h1>How to use</h1>

  <p>Obviously, this is supposed to work only for code blocks (<code>&lt;pre>&lt;code></code>) and not for inline code.</p>
  <p>Add the <code>line-numbers</code> class to your desired <code>&lt;pre></code> or any of its ancestors, and the line-numbers plugin will take care of the rest. To give all code blocks line numbers, add the <code>line-numbers</code> class to the <code>&lt;body></code> of the page.</p>
  <p>Optional: You can specify the <code>data-start</code> (Number) attribute on the <code>&lt;pre></code> element. It will shift the line counter.</p>
  <p>Optional: To support multiline line numbers using soft wrap, apply the CSS <code>white-space: pre-line;</code> or <code>white-space: pre-wrap;</code> to your desired <code>&lt;pre></code>.</p>
</section>

<section class="line-numbers">
  <h1>Examples</h1>

  <h2>JavaScript</h2>
  <pre class="line-numbers" data-src="plugins/line-numbers/prism-line-numbers.js"></pre>

  <h2>CSS</h2>
  <p>Please note that this <code class="language-markup">&lt;pre></code> does not have the <code>line-numbers</code> class but its parent does.</p>
  <pre data-src="plugins/line-numbers/prism-line-numbers.css"></pre>

  <h2>HTML</h2>
  <p>Please note the <code>data-start="-5"</code> in the code below.</p>
  <pre class="line-numbers" data-src="plugins/line-numbers/index.html" data-start="-5"></pre>

  <h2>Unknown languages</h2>
  <pre class="language-none line-numbers"><code>This raw text
is not highlighted
but it still has
line numbers</code></pre>

  <h2>Soft wrap support</h2>
  <p>Please note the <code>style="white-space:pre-wrap;"</code> in the code below.</p>
  <pre class="line-numbers" data-src="plugins/line-numbers/index.html" data-start="-5" style="white-space:pre-wrap;"></pre>

</section>

<footer data-src="templates/footer.html" data-type="text/html"></footer>

<script src="prism.js"></script>
<script src="plugins/line-numbers/prism-line-numbers.js"></script>
<script src="scripts/utopia.js"></script>
<script src="components.js"></script>
<script src="scripts/code.js"></script>


</body>
</html>
```
#### Code block indented with four spaces

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### Code block with Hugo's internal highlight shortcode
{{< highlight html >}}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

## List Types

#### Ordered List

1. First item
2. Second item
3. Third item

#### Unordered List

* List item
* Another item
* And another item

#### Nested list

* Item
1. First Sub-item
2. Second Sub-item

## Other Elements — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.