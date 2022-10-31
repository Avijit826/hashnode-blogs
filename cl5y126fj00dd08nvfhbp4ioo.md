# A quick note about markdown.md

# Markdown

>Markdown is a lightweight markup language intended for one purpose, to be used to format text on the web with plain text formatting syntax. We denote these files marked as .md

- ## Headings

>To create heading we use `#` symbol

`# Heading level 1`
# Heading level 1

`## Heading level 2`
## Heading level 2

`### Heading level 3` 
### Heading level 3

`#### Heading level 4`

#### Heading level 4

`##### Heading level 5`
##### Heading level 5

`####### Heading level 6`
###### Heading level 6

>Add Space after # sign

`# Heading` is correct ✔️

`#Heading` is not correct ❌

- ## Paragraphs and Line Breaks

>To start a new paragraph, leave a blank line between lines of text.

    This is
    a single paragraph

`This is
a single line paragraph`

    This is

    a single paragraph

This is multi-line

paragraph

>To create a new line, end a line with two space

- ## Bold

>To bold text, add two asterisks `**`  or underscores `__` before and after a word or phrase.

`Make me **bold** `

Make me **bold**

`Another __bold__`

Another __bold__

>Don't leave space between `**` sign

`**bold**` is correct ✔️

`** bold **` is not correct ❌

- ## Italic

>To italic text, add one asterisk `*`  or underscore `_` before and after a word or phrase.

`Make me *italic* `

Make me *italic*

`Another _italic_`

Another _italic_

>Don't leave space between `*` sign

`*italic*` is correct ✔️

`* italic *` is not correct ❌

>>You can use `bold` and `italic` togather.

`***I'm italic and bold also.***`

***I'm italic and bold also.***

OR

`___I'm italic and bold also.___`

___I'm italic and bold also.___

OR

`*__I'm italic and bold also.__*`

*__I'm italic and bold also.__*

OR

`**_I'm italic and bold also._**`

**_I'm italic and bold also._**

- ## Strikethrough

>It putting a horizontal line through the center of them.

   ` ~~Cut this~~`

~~Cut this~~
- ## Blockquotes

>To create a blockquote, add a > in front of a paragraph.

```
>This is parent blockquote

```


>This is parent blockquote


    `>>This is child blockquote`


>This is parent blockquote   
>>This is child blockquote



    `>>>This is grand child blockquote`



> This is parent blockquote   
>>This is child blockquote
>>>This is grand child blockquote



Like this create as many hirearchy as you want



- ## Odered Lists

>To create an ordered list, add line items with numbers followed by periods.

``` 
1. List Item 1
2. List Item 2
3. List Item 3
4. List Item 4
```
1. List Item 1
2. List Item 2
3. List Item 3
4. List Item 4

>The numbers don’t have to be in numerical order.

LIKE

```
1. List Item 1
2. List Item 2
5. List Item 3
5. List Item 4
```

1. List Item 1
2. List Item 2
5. List Item 3
5. List Item 4

>But the list should start with the number one.

```
5. List Item 1
2. List Item 2
3. List Item 3
4. List Item 4
```

5. List Item 1
2. List Item 2
3. List Item 3
4. List Item 4

>We also create sub odered list
```
1. List Item 1
2. List Item 2
3. List Item 3
4. List Item 4
    1. Sub list 1
    1. Sub list 2
    1. Sub list 3
```

1. List Item 1
2. List Item 2
3. List Item 3
4. List Item 4
    1. Sub list 1
    1. Sub list 2
    1. Sub list 3

>Add Space after `.` sign

`1. List` is correct ✔️

`1.List` is not correct ❌


- ## Unorderd Lists

>To create an unordered list, add dashes `-`, asterisks `*`, or plus signs `+` in front of line items.

``` 
- List Item 1
- List Item 2
- List Item 3
- List Item 4
```
- List Item 1
- List Item 2
- List Item 3
- List Item 4

>You can use different signs togather
>>but don't do that

LIKE

```
+ List Item 1
- List Item 2
* List Item 3
+ List Item 4
```

+ List Item 1
- List Item 2
* List Item 3
+ List Item 4

>We also create sub unodered list
```
- List Item 1
- List Item 2
- List Item 3
- List Item 4
    + Sub list 1
    + Sub list 2
    + Sub list 3
```

- List Item 1
- List Item 2
- List Item 3
- List Item 4
    - Sub list 1
    - Sub list 2
    - Sub list 3

>Add Space after `-`,`+` or `*` sign

`- List` is correct ✔️

`-List` is not correct ❌

- ## Horizontal Rules

>To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves. 

`***`
***
`---`

---

- ## Links

>To create a link, enclose the link text in brackets `[]` and then follow it immediately with the URL in parentheses `()`

    Check my [blog](https://avicreation.hashnode.dev/)
Check my [blog](https://avicreation.hashnode.dev/)

>Also you add title in it within " " after the link inside end of the `()` braces

To directly put visible link **enclose it in angle brackets.**

<https://avicreation.hashnode.dev>

>It also work with emails

<example@example.com>

- ## Rendering Images

>To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parentheses.

    ![img alt txt](image link)

```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658573529700/Ris19kIOq.png)
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658573529700/Ris19kIOq.png align="left")


- ## Block code

>To create a fenced code block that spans multiple lines of code, set the text inside three or more backquotes (```) or tildes (~~~).


~~~
```
    let items = 23
    console.log(items);
```
~~~

```javascript
    let items = 23
    console.log(items);
```

- ## Inline code
>Use `` to create inline code

` `console.log("Single line code")` `


- ## Tables

>Tables are a great tool for adding structure to your content. Use the following syntax to create tables:
- To create columns, use vertical bars (|). The outer bars are optional.
- Separate the header row from the rest of the table with three or more dashes (---).

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

>You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens within the header row.
```
| Heading 1    | Heading 2      | Heading 3     |
| :---         |    :----:      |       ---:    |
| Left         | Center         | Right         |
```

| Heading 1    | Heading 2      | Heading 3     |
| :---         |    :----:      |       ---:    |
| Left         | Center         | Right         |





