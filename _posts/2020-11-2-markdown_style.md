---
title:  "A Note of Markdown Style"
date:   2020-11-02
categories: /posts/Markdown
tags: Markdown
author_profile: true
---

Markdown is a way to style text on the web. In this post, I will show a brief markdown style. 


## Header
<b>Script:</b>

```
# This is an H1

## This is an H2
```
<b>Result:</b>
# This is an H1

## This is an H2


## Quote Block

<b>Script:</b>
```
> This is quote block
>> This is sub quote block
```
<b>Result:</b>
> This is quote block
>> This is sub quote block


## Emphasis

<b>Script:</b>
```
*This text will be italic*
<i>This text will be italic</i>
**This text will be bold**
<b>This text will be bold</b>
```
<b>Result:</b><br>
*This text will be italic*<br>
<i>This text will be italic</i><br>
**This text will be bold**<br>
<b>This text will be bold</b>


## code

<b>Script:</b>
```
`int` is locate the integer memory.
```
<b>Result:</b>
`int` is locate the integer memory.<br>

* * *

<b>Script:</b>
<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>```c
int a = 0; 
```
</code></pre></div></div>
<b>Result:</b>
```c
int a = 0; 
```

* * *

<b>Script:</b>

```
<p>This is a normal paragraph:</p>

<pre><code>This is a code block.
</code></pre>
```
<b>Result:</b>
<p>This is a normal paragraph:</p>

<pre><code>This is a code block.
</code></pre>


## Unordered lists

<b>Script:</b>
```
* Item 1
* Item 2
  * Item 2a
  * Item 2b
<ul>
<li>Item 1</li>
<li>Item 2</li>
</ul>
```
<b>Result:</b>
* Item 1
* Item 2
  * Item 2a
  * Item 2b
<ul>
<li>Item 1</li>
<li>Item 2</li>
</ul>


## Ordered lists

<b>Script:</b>
```
1. Item 1<br>
Here will indent.
2. Item 2
3. Item 3

Extra line will be no indent.<br>
1\. This is not item. 
2\. This is not item. 
<ol>
<li>Item 1</li>
<li>Item 2</li>
</ol>
```
<b>Result:</b>
1. Item 1<br>
Here will indent.
2. Item 2
3. Item 3

Extra line will be no indent.<br>
1\. This is not item. 
2\. This is not item. 
<ol>
<li>Item 1</li>
<li>Item 2</li>
</ol>

## Break line
<b>Script:</b>
```
* * *
- - -
```
<b>Result:</b>
* * *
- - -

## Link
<b>Script:</b>
```
[Here](https://singyuan.github.io/)
```
<b>Result:</b>
[Here](https://singyuan.github.io/)
