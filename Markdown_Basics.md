# Markdown Basics

## 段落、标题、区块代码


一个段落是由一个以上的连接的行句组成，而一个以上的空行则会划分出不同的段落（空行的定义是显示上看起来像是空行，就被视为空行，例如有一行只有空白和 tab，那该行也会被视为空行），一般的段落不需要用空白或换行缩进。

Markdown 支持两种标题的语法，Setext 和 atx 形式。Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题），Atx 形式在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶。

区块引用则使用 email 形式的 '>' 角括号。
```markdown
A First Level Header
====================
A Second Level Header
---------------------
Now is the time for all good men to come to
the aid of their country. This is just a
regular paragraph.

The quick brown fox jumped over the lazy
dog's back.
### Header 3

> This is a blockquote.
> 
> This is the second paragraph in the blockquote.

## This is an H2 in a blockquote
```

A First Level Header
====================
A Second Level Header
---------------------
Now is the time for all good men to come to
the aid of their country. This is just a
regular paragraph.

The quick brown fox jumped over the lazy
dog's back.
### Header 3

> This is a blockquote.
>   
> This is the second paragraph in the blockquote.
 
## This is an H2 in a blockquote

## 修辞和强调
Markdown使用星号和底线来标记需要强调的区段。

```markdown
Some of these words *are emphasized*.  
Some of these words _are emphasized also_.  
Use two asterisks for **strong emphasis**.  
Or, if you prefer, __use two underscores instead__.  
```

Some of these words *are emphasized*.  
Some of these words _are emphasized also_.  
Use two asterisks for **strong emphasis**.  
Or, if you prefer, __use two underscores instead__.  


## 列表
无序列表使用星号、加号和减号来作为列表的项目标记。这些符号都是可以使用的。 <p> 使用星号：

```markdown
* Candy.
* Gum.
* Booze.
```

* Candy.
* Gum.
* Booze.

加号：

```markdown
+ Candy.
+ Gum.
+ Booze.
```

+ Candy.
+ Gum.
+ Booze.

减号：

```markdown
- Candy.
- Gum.
- Booze.
```

- Candy.
- Gum.
- Booze.

有序列表则是使用一般数字接着一个英文句点作为项目标记：

```markdown
1. Red
2. Green
3. Blue
```

1. Red
2. Green
3. Blue

如果你在项目之间插入空行，那项目的内容会用 `<p>` 包起来，你也可以在一个项目内放上多个段落，只要在它前面缩排 4 个空白或 1 个 tab 。

```markdown
* A list item
	with multiple paragraphs
* Another item in the list.
```

* A list item
	with multiple paragraphs  
* Another item in the list.  


## 链接

Markdown 支持两种形式的链接语法： 行内和参考两种形式，两种都是使用角括号来把文字转成链接。  
行内形式是直接在后面用括号直接接上链接：

```markdown
This is an [example link](http://example.com/).    
你也可以选择性的加上 title 属性：  
This is an [example link](http://example.com/ "With a Title").  
参考形式的链接让你可以为链接定一个名称，之后你可以在文件的其他地方定义该链接的内容：  
I get 10 times more traffic from [Google][1] than from
[Yahoo][2] or [MSN][3].  

[1]: http://google.com/ "Google"
[2]: http://search.yahoo.com/ "Yahoo Search"
[3]: http://search.msn.com/ "MSN Search"
```

This is an [example link](http://example.com/).    
你也可以选择性的加上 title 属性：  
This is an [example link](http://example.com/ "With a Title").  
参考形式的链接让你可以为链接定一个名称，之后你可以在文件的其他地方定义该链接的内容：  
I get 10 times more traffic from [Google][1] than from
[Yahoo][2] or [MSN][3].  

[1]: http://google.com/ "Google"
[2]: http://search.yahoo.com/ "Yahoo Search"
[3]: http://search.msn.com/ "MSN Search"

title 属性是选择性的，链接名称可以用字母、数字和空格，但是不分大小写：  

```markdown
I start my morning with a cup of coffee and
[The New York Times][NY Times].  

[ny times]: http://www.nytimes.com/
```

I start my morning with a cup of coffee and
[The New York Times][NY Times].  

[ny times]: http://www.nytimes.com/

## 图片
图片的语法和链接很像。行内形式（title是选择性的）：

```markdown
![Image text]( https://raw.githubusercontent.com/JeromeYao/PyNotes/master/Tips/wordcloud.png "Title")
```

![Image text]( https://raw.githubusercontent.com/JeromeYao/PyNotes/master/Tips/wordcloud.png "Title")

参考形式：

```markdown
![alt text][id] 

[id]: https://raw.githubusercontent.com/JeromeYao/PyNotes/master/Tips/wordcloud.png "Title"
```

![alt text][id] 

[id]: https://raw.githubusercontent.com/JeromeYao/PyNotes/master/Tips/wordcloud.png "Title"

## 代码
在一般的段落文字中，你可以使用反引号 \` 来标记代码区段，区段内的 &、< 和 > 都会被自动的转换成 HTML 实体，这项特性让你可以很容易的在代码区段内插入 HTML 码：

```markdown
I strongly recommend against using any `<blink>` tags.  

I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entites like `&#8212;`.
```

I strongly recommend against using any `<blink>` tags.  

I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entites like `&#8212;`.

如果要建立一个已经格式化好的代码区块，只要每行都缩进 4 个空格或是一个 tab 就可以了，而 &、< 和 > 也一样会自动转成 HTML 实体。

```markdown
If you want your page to validate under XHTML 1.0 Strict,
you've got to put paragraph tags in your blockquotes:
	<blockquote>
	<p>For example.</p>
	</blockquote>
```

If you want your page to validate under XHTML 1.0 Strict,
you've got to put paragraph tags in your blockquotes:
	<blockquote>
	<p>For example.</p>
	</blockquote>
