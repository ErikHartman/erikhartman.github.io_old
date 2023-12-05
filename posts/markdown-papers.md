# Writing scientific articles in `Markdown`

I've been on the search for a lightweight and reliable way to write academic articles, but it's more difficult than you'd think. Today, the gold standards are LaTeX (for math, physics and engineering) and Word for basically everything else. While both of these tools are good, they're lacking in several aspects.

Word has too much functionality. For scientific articles, all you really need is the abilities to:
1. create headers.
2. insert figures.
3. insert tables.
4. write mathematical expressions/chemical formulae etc.
5. reference and cite.

Beyond this, Word offers a bunch of things which really is just bloat, like different fonts, shapes, colors, etc. It also is severely lacking in points 4 and 5. Also, it uses the .docx-format, which is impossible to read without using Word.

LaTeX is way better in points 4 and 5, as writing mathematical expressions and referencing using .bib is extremely easy. It also cuts down on the bloat. However, it has a bit of a learning curve, is a pain to set up and has several quirks that you have to get used to. You can skip the setup by using Overleaf, but then you restrict your writing to having internet access, and you're relying on Overleaf servers.

In the end, I've settled on writing in pure **Markdown** and use a set of tools to get everything you need to write scientific articles.

## What is Markdown
Markdown is a lightweight markup language that uses plain text formatting syntax to create structured documents.

Here are some basic examples of Markdown syntax:

Headers:
```
# Heading 1
## Heading 2
### Heading 3
```
Emphasis:
```
*italic* or _italic_
**bold** or __bold__
```
Lists:
```
- Item 1
- Item 2
  - Subitem 2.1
  - Subitem 2.2
1. Numbered item 1
2. Numbered item 2
```
Links:
```
[Link text](http://example.com)
```
Images:
```
![Alt text](image.jpg)
```
Code:
```
`inline code`
```

## Markdown Preview Enhanced 
**This requires Visual Studio Code*

Markdown Preview Enhanced (https://shd101wyy.github.io/markdown-preview-enhanced/#/) is an extension available in Visual Studio Code that allows you to preview your Markdown-files while writing them. It also supports Mathematical expressions in a LaTeX-style. In general, this creates the best writing experience I've had.

![MPE](../img/MPE.png)

## Converting to .html, .tex, .pdf, .docx using Pandoc

The magic sets in when you combine Markdown Preview Enhanced with Pandoc. Pandoc is a versatile document converter and markup language processor that allows for the conversion between different document formats, and it integrates with Markdown Preview Enhanced.

By specifying arguments in the header of your document, you can export your .md file to many other formats. I've used it for creating .docx and .pdf-files, and in both cases it has created well-stylized files.

<div>
    <img source="../img/md_word.png">
    <img source="../img/md_pdf.png">
</div>