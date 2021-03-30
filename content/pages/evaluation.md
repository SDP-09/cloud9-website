---
title: "Evaluation"
date: 2020-04-18T10:07:21+06:00
# post image
image: "images/blog/post-1.jpg"
# post type (regular/featured)
type: "featured"
# meta description
description: "This is meta description"
# post draft
draft: false
---


| Table | Goal Pose            | Mean Achieved Pose    | Success |
| ----- | -------------------- | --------------------- | ------- |
| 1     | 0.35 0.90 0.70 0.70  | 0.46 0.99 0.80 0.61   | 5/5     |
| 2     | -1.20 0.50 0.70 0.70 | -1.33 0.53 0.50 0.87  | 4/5     |
| 3     | 0.3 -4.7 0.0 1.0     | 0.24 -4.5 5 0.10 0.96 | 4/5     |
| 4     | 0.3 -3.7 0.0 1.0     | 0.23 -3.62  0.21 0.95 | 5/5     |
| 5     | 0.3 -2.7 0.0 1.0     | 0.18 -2.81  0.09 0.99 | 5/5     |
| 6     | 1.8 -4.7 0.0 1.0     | 1.77 -4.88 -0.09 1.11 | 3/5     |
| 7     | 1.8 -3.7 0.0 1.0     | 1.64 -3.58 -0.03 1.06 | 4/5     |
| 8     | 1.8 -2.7 0.0 1.0     | 1.73 -2.64  0.05 0.91 | 3/5     |


| **Attr. to change ↓** | **Brightness/cd** | **Obs. pos** | **Obs. size** | **Obs. color** | **Table color** | **Reflect light** | **Shadow   (Gradient)** | **Outcome** |
| --------------------- | ----------------- | ------------ | ------------- | -------------- | --------------- | ----------------- | ----------------------- | ----------- |
| **Illumination**      |                   |              |               |                |                 |                   |                         |
|                       | 0-20              | middle       | middle        | light          | brown           | None              | None                    | Success     |
|                       | 20-40             | middle       | middle        | green          | brown           | None              | None                    | Success     |
|                       | 40-60             | middle       | middle        | green          | brown           | None              | None                    | Success     |
|                       | 60-80             | middle       | middle        | green          | brown           | None              | None                    | Success     |
| **Position**          |                   |              |               |                |                 |                   |                         |
|                       | 40-60             | left         | middle        | green          | brown           | None              | None                    | Success     |
|                       | 40-60             | right        | middle        | green          | brown           | None              | None                    | Success     |
|                       | 40-60             | top          | middle        | green          | brown           | None              | None                    | Success     |
|                       | 40-60             | bottom       | middle        | green          | brown           | None              | None                    | Success     |
| **Size**              |                   |              |               |                |                 |                   |                         |
|                       | 40-60             | middle       | small         | green          | brown           | None              | None                    | Success     |
|                       | 40-60             | middle       | large         | green          | brown           | None              | None                    | Success     |
| **Obs. Colour**       |                   |              |               |                |                 |                   |                         |
|                       | 40-60             | middle       | middle        | brown          | brown           | None              | None                    | Success     |
|                       | 40-60             | middle       | middle        | black          | black           | None              | None                    | Fail        |
| **Table color**       |                   |              |               |                |                 |                   |                         |
|                       | 40-60             | middle       | middle        | brown          | dark            | None              | None                    | Success     |
| **Reflected light**   |                   |              |               |                |                 |                   |                         |
|                       | 40-60             | middle       | middle        | green          | brown           | Yes               | None                    | Success     |
| **Shadow**            |                   |              |               |                |                 |                   |                         |
|                       | 40-60             | middle       | middle        | green          | brown           | None              | low                     | Success     |
|                       | 40-60             | middle       | middle        | green          | brown           | None              | high                    | Fail        |


| Angle/degree | Distance/meter | Detected | Graph                                   |
| ------------ | -------------- | -------- | --------------------------------------- |
| 10           | 5              | no       | ![image](../media/evaluation/105.png)  |
| 10           | 10             | no       | ![image](../media/evaluation/110.png)  |
| 10           | 15             | no       | ![image](../media/evaluation/115.png)  |
| 30           | 5              | yes      | ![image](../media/evaluation/305.png)  |
| 30           | 10             | no       | ![image](../media/evaluation/310.png)  |
| 30           | 15             | no       | ![image](../media/evaluation/315.png)  |
| 45           | 5              | yes      | ![image](../media/evaluation/455.png)  |
| 45           | 10             | yes      | ![image](../media/evaluation/4510.png) |
| 45           | 15             | no       | ![image](../media/evaluation/4515.png) |
| 60           | 5              | yes      | ![image](../media/evaluation/605.png)  |
| 60           | 10             | yes      | ![image](../media/evaluation/6010.png) |
| 60           | 15             | yes      | ![image](../media/description/6015.png) |




#### Heading example

Here is example of hedings. You can use this heading by following markdownify rules. For example: use `#` for heading 1 and use `######` for heading 6.

# Heading 1 
<br>

## Heading 2 

<br>

### Heading 3 

<br>

#### Heading 4 

<br>

##### Heading 5 

<br>

###### Heading 6


<hr>

##### Emphasis

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

<hr>

##### Link
[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.themefisher.com
[1]: https://gethugothemes.com
[link text itself]: https://www.getjekyllthemes.com

<hr>

##### Paragraph

Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.

<hr>

##### Ordered List

1. List item
2. List item
3. List item
4. List item
5. List item

<hr>

##### Unordered List

* List item
* List item
* List item
* List item
* List item

<hr>

##### Code and Syntax Highlighting

Inline `code` has `back-ticks around` it.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```

<hr>

##### Blockquote

> This is a blockquote example.

<hr>

##### Inline HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>


<hr>

##### Tables

Colons can be used to align columns.

| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

| Markdown | Less      | Pretty     |
| -------- | --------- | ---------- |
| *Still*  | `renders` | **nicely** |
| 1        | 2         | 3          |

<hr>

##### Image

![image](../../images/blog/post-6.jpg)

<hr>

##### Youtube video

{{< youtube C0DPdy98e4c >****