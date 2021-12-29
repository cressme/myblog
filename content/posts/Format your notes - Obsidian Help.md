---
title: Obsidian的markdown语法规则
description: 相关的规则以及展示
toc: true
authors:
  - herrisen
tags:
  - tips
categories:
series:
date: '2021-12-29'
lastmod: '2021-12-20'
draft: false
---


> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [help.obsidian.md](https://help.obsidian.md/How+to/Format+your+notes)

> Format your notes

Obsidian is a Markdown-based note-taking and knowledge base app.

We currently support the formats below:

```
Link to a page: [[Internal link]].
```

Embed another file (read more about [Embed files](https://help.obsidian.md/How+to/Embed+files)). Here's an embedded section:

```
![[Obsidian#What is Obsidian]]
```

What is Obsidian" src="Obsidian#What is Obsidian">

Obsidian is a both a Markdown editor and a knowledge base app.

Used in the most basic way, you can edit and preview Markdown files. But its true power lies in managing densely networked knowledge base.

How do we start creating a network, you ask? Let's first start making some [internal links](https://help.obsidian.md/How+to/Internal+link)!

```
# This is a heading 1
## This is a heading 2
### This is a heading 3 
#### This is a heading 4
##### This is a heading 5
###### This is a heading 6
```

```
*This text will be italic*
_This will also be italic_
```

_This text will be italic_  
_This will also be italic_

```
**This text will be bold**
__This will also be bold__
```

**This text will be bold**  
**This will also be bold**

```
_You **can** combine them_
```

_You **can** combine them_

```
- Item 1
- Item 2
  - Item 2a
  - Item 2b

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

*   Item 1
*   Item 2
    *   Item 2a
    *   Item 2b

1.  Item 1
2.  Item 2
3.  Item 3
    1.  Item 3a
    2.  Item 3b

```
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

Example of this above image resized to 100 pixels wide:

```
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

Markdown style links can be used to refer to either external objects, such as web pages, or an internal page or image.

```
http://obsidian.md - automatic!
[Obsidian](http://obsidian.md)
```

[Obsidian URI](https://help.obsidian.md/Advanced+topics/Using+obsidian+URI) links can be used to open notes in Obsidian either from another Obsidian vault or another program.

For example, you can link to a file in a vault like so (please note the [required encoding](https://help.obsidian.md/Advanced+topics/Using+obsidian+URI#Encoding)):

```
[Link to note](obsidian://open?path=D:%2Fpath%2Fto%2Ffile.md)
```

You can link to a note by its vault name and file name instead of path as well:

```
[Link to note](obsidian://open?vault=MainVault&file=MyNote.md)
```

If there are spaces in the url, they can be escaped by either using `%20` as a space, such as:

```
[Export options](Pasted%20image)
```

Or you can enclose the target in `<>`, such as:

```
[Slides Demo](<Slides Demo>)
```

```
> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961
```

> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

- Doug Engelbart, 1961

```
Text inside `backticks` on a line will be formatted like code.
```

Text inside `backticks` on a line will be formatted like code.

Syntax highlight is supported with the language specified after the first set of backticks. We use prismjs for syntax highlighting, a list of supported languages can be found [at their site](https://prismjs.com/#supported-languages)

```
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
```

```
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

```
Text indented with a tab is formatted like this, and will also look like a code block in preview.
```

```
Text indented with a tab is formatted like this, and will also look like a code block in preview.
```

```
- [x] #tags, [links](), **formatting** supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [?] this is also a complete item (works with every character)
- [x] this is an incomplete item
- [ ] tasks can be clicked in Preview to be checked off
 ==原来输入完成之后会自动变为checkbox,在未输入完成的时候没有显示==
 
 
```

*   [#tags](https://publish.obsidian.md/#tags), links, **formatting** supported
*   list syntax required (any unordered or ordered list supported)
*   this is a complete item
*   this is also a complete item (works with every character)
*   this is an incomplete item
*   tasks can be clicked in Preview to be checked off

You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and then separating each column with a pipe `|`:

```
First Header | Second Header
------------ | ------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```

<table><thead><tr><th>First Header</th><th>Second Header</th></tr></thead><tbody><tr><td>Content from cell 1</td><td>Content from cell 2</td></tr><tr><td>Content in the first column</td><td>Content in the second column</td></tr></tbody></table>

```
Tables can be justified with a colon | Another example with a long title
:----------------|-------------:
because of the `:` | these will be justified

If you put links in tables, they will work, but if you use Piped Links, the pipe must be escaped with a `\` to prevent it being read as a table element.
```

<table><thead><tr><th>Tables can be justified with a colon</th><th>Another example with a long title</th></tr></thead><tbody><tr><td>because of the <code>:</code></td><td>these will be justified</td></tr></tbody></table>

If you put links in tables, they will work, but if you use Piped Links, the pipe must be escaped with a `\` to prevent it being read as a table element.

```
First Header | Second Header
------------ | ------------
[[Format your notes\|Formatting]]   |  [[Keyboard shortcuts\|hotkeys]]
```

```
Any word wrapped with two tildes (like ~~this~~) will appear crossed out.
```

Any word wrapped with two tildes (like ~this~) will appear crossed out.

```
Use two equal signs to ==highlight text==.
```

Use two equal signs to highlight text.

```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: meaningful!

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
```

Here's a simple footnote, and here's a longer one.

```
You can also use inline footnotes. ^[notice that the carat goes outside of the brackets on this one.]
```

You can also use inline footnotes.

```
$$\begin{vmatrix}a & b\\
c & d
\end{vmatrix}=ad-bc$$
```

You can also do inline math like  .

Obsidian uses [Mathjax](http://docs.mathjax.org/en/latest/basic/mathjax.html). You can check which packages are supported in Mathjax [here](http://docs.mathjax.org/en/latest/input/tex/extensions/index.html).

Use `%%` to enclose comments, which will be parsed as Markdown, but will not show up in the preview.

```
Here is some inline comments: %%You can't see this text%% (Can't see it)

Here is a block comment:
%%
It can span
multiple lines
%%
```

Here is some inline comments: (can't see it in preview)

Here is a block comment: (can't see it in preview either)

```
```mermaid
sequenceDiagram
    Alice->>+John: Hello John, how are you?
    Alice->>+John: John, can you hear me?
    John-->>-Alice: Hi Alice, I can hear you!
    John-->>-Alice: I feel great!
```
```

AliceJohnHello John, how are you?John, can you hear me?Hi Alice, I can hear you!I feel great!AliceJohn

Obsidian supports linking to notes in Mermaid:

```
```mermaid
graph TD

Biology --> Chemistry

class Biology,Chemistry internal-link;
```
```

An easier way to do it is the following:

```
```mermaid
graph TD

A[Biology]
B[Chemistry]

A --> B

class A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,V,W,X,Y,Z internal-link;
```
```

This way, all the note names (at least until `Z[note name]`) are all automatically assigned the class `internal-link` when you use this snippet.

If you use special characters in your note names, you need to put the note name in double quotes.  
`"⨳ special character"`  
It looks like this if you follow the [second option](https://help.obsidian.md/How+to/Format+your+notes#^376b9d):  
`A["⨳ special character"]`

We strive for maximum capability without breaking any existing formats, therefore we use a slightly unorthodox combination of flavors of markdown. It is broadly CommonMark, with the addition of some functionality from GitHub Flavored Markdown (GFM), some latex support, and our chosen embed syntax, which you can read more about at [Accepted file formats](https://help.obsidian.md/Advanced+topics/Accepted+file+formats).

```

