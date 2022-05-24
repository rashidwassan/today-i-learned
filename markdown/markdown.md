# Markdown

### What is markdown?
- A lightweight markup language with a plaintext formatting syntax.
- Created by John Gruber in 2004, Markdown is now one of the world’s most popular markup languages.
- Can be converted into HTML/XHTML and other formats.
- Its main purpose is readability and ease of use.

### Popular uses:
- Readme files.
- Forum & blog posts.
- Used in many static site generators.

### Some of the things that you can format
- Images
- Headings
- Lists
- Emphasis
- Links
- Blocks of code
- Blockquotes
- Horizontal rules

### Markdown Editors
- Text Editor Extensions like VS Code.
- MarkPad
- HarooPad
- MarkdownPad 2
- Typora

### Comments
- Comments can be added like in HTML
<!-- This is a comment -->
``` markdown
<!-- This is a comment -->
```

## Headings
Here, the number of leading hash characters define type.
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
> Code:
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
---

## Horizontal line
``` markdown
---
```
---
## Italics
To make specifi part *Italic*
``` markdown
The word *italic* is italic.
```
OR
``` markdown
The word _italic_ is italic.
```
Result: The word *italic* is italic.

## Strikethrough
OP: ~~Hello World!~~

>Syntax:
```
~~Hello World~~
```

## Showing special symbols
- Backslash is used just like in some programming languages.

OP: \~~Hello World!~~
> Syntax:
```
\~~Hello World!~~
```

## Blockquote
> This is a quote

> Code:
```
> This is a quote.
```

## Links
To display a link, the title to be shown is written in square brackets and link goes in succeeding parenthesis.

OP: [Rashid's Portfolio](https://www.rashidwassan.tech)

> Code:
```
[Rashid's Portfolio](https://www.rashidwassan.tech)
```

# Lists
## Unordered List
We can create an unordered list usign * in start.
* Item 1
* Item 2
* Item 3

> Code:
```
* Item 1
* Item 2
* Item 3

```
## Nested lists
Nested lists can be easily created with tab identation.
* Item 1
  * Item 2
    * Item 3
      * Item 4
    * Item 5
  * Item 6
* Item 7

> Code:
```
* Item 1
  * Item 2
    * Item 3
      * Item 4
    * Item 5
  * Item 6
* Item 7
```

## Ordered List

1. Item 1
1. Item 2
1. Item 3
1. Item 4

OR

1. Item 1
   1. SubItem
      1. Micro item
      2. Micro item 2
2. Item 2
3. Item 3

> Code:
``` markdown
1. Item 1
1. Item 2
1. Item 3
1. Item 4

OR

1. Item 1
   1. SubItem
      1. Micro item
      2. Micro item 2
2. Item 2
3. Item 3
```
---
## Inline Codeblock
`This is some inline code`.
``` markdown
`This is some inline code`.
``` 

## Code Block
Code block is displayed by wrapping code with ```. Syntax highlighting can be enabled when defining the language name after inital three quote marks.
``` dart
// This is dart code
void main(){ print('Hello'); }
```
## Image
```
![Markdown logo](https://exampleimagelink.com)
```

---
## Tables
Table:
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

> Code
```
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```