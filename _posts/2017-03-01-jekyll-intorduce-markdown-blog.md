---
layout: post
title:  jekyll+Markdown发表博文
categories: jekyll
tags:  jekyll Markdown
author: 郭金文
---
* content
{:toc}

## jekyll博客简介

jekyll是一个简单的免费的Blog生成工具，与其他博客生成工具如wordpress不同的是，它只生成静态网页，不需要数据库支持。但是可以配合第三方服务,例如评论系统Disqus、多说等。最关键的是jekyll可以免费部署在Github上，而且可以绑定自己的域名。

![](/images/guojinwen/jekyll-log.png)



此外，jekyll还可以自己编辑网页生成自己独特风格的页面，也可以直接引用别人已经写好的theme，主题可以在：[http://themes.jekyllrc.org/](http://themes.jekyllrc.org/) 进行下载，在此非常感谢github上多位牛人的辛苦付出。
更多关于jekyll博客系统的介绍，请到[jekyll网站](https://jekyllrb.com/)查看。

## 关于本博客

本团队博客(WishTeam)主题支持团队多人发表博文，博客的theme会持续进行更新优化，优化的日志在团队介绍中的"更新日志"中说明，本博客theme可以点击页面下的联系我们进入我们的github主页进行下载。
博文使用kramdown插件对markdown标记语法进行解析，发表博文时按照markdown语法规范进行书写。可以使用markdown编辑器，如MaHua、sublineText、Marxico等,有条件的建议使用sublineText，可以预览效果，本文使用sublineText编辑。

## 博文发表

博文发表，jetyll博客系统由于只生成静态的html文件，并没有将文章内容存入数据库保存。因此，写文章并不像wordpress等博客系统那样直接调用Uedit或百度编辑插件，就可以写出一篇文章。jetyll写博文相对麻烦一点，但是它可以利用markdown等语法，提供了更自由的书写方式，更为自由的布局，还有独特的代码块，使得文章看起来更专业。如果是将博客托管在GitHub上，博文的发表如下。

### github工程下载

首先需要安装git版本控制系统，从github上pull本博客工程代码。
工程目录如下：

  ![](/images/guojinwen/jekyll-content.png)

- 在_post文件夹下，新建md文件，文件命名必须遵循：yyyy-mm-dd-title，且文件名称不能使用中文，否则会出现url解析错误的情况。例如本文章的文件命名方式：

>2017-03-01-jekyll-intorduce-markdown-blog.md


### 文章文件头

博文文章的md文件，需要遵循一定的格式。

博文文件头必须包含如下:

    ```java
    ---
    layout: post
    title:  jekyll文章发表-markdown语法
    categories: JavaScript
    tags:  countdown JavaScript
    author: 郭金文
    ---
    
    * content
    {:toc}
    ```

这个文件头“- - -”包起来的部分指定使用html的layout模板post，文章的标题，文章的分类categories，还有标签tags，文章的作者。除了categories，tags外，所有的信息字段信息都是必须的，为了更好的对文章进行分类建议所有的字段都必填，“- - -”外的两段代码是生成文章目录，也是必须的。
>PS:   <font color="blue">定义字段"："后面必须要有空格,否则会报错</font>

### 文章内容
定义好文件头后，我们就可以自由的创作啦！氮素！首先，在开始正文前，我们需要注意一点就是，文章的提示内容，查看博文的首页的文章列表，我们可以发现，每篇文章除了标题信息外，还包括一小段的引言部分：

![](/images/guojinwen/bref.png)

为了实现控制这部分引言的展示段落，在正文的书写时，书写好一小段正文后，需要至少4个回车换行符。

![](/images/guojinwen/4huiche.png)

好了，一切准备就绪，我们可以开始我们的文章啦！O(∩_∩)O_)

## 文章预览及Markdown语法

为了更好的展现我们的文章，我们需要了解一些基本的markdown语法。

Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。它不仅可以它不仅可以呈现不同的文字字体效果，还可以嵌入图片、代码块，实现超链接等等，很多人将它看成html语言的精简版。

### 预览

本博客使用markdown作为博文发表的组件，jekyll可以将markdown标记语言生成.html文件。如果没有装jekyll环境，可以直接使用markdown编辑插件实现md文件的预览。本文使用sublineTxt预览，预览时会自动编译生成html文件，在浏览器中呈现：

![预览效果](/images/guojinwen/preview.png)

但是由于有一些jetyll语法存在，预览效果并不是最终的效果，只能看出大致排版情况。如果使用jetyll环境编译后预览，那么结果就是最终的呈现效果如下：

![预览效果](/images/guojinwen/preview_jetyll.png)

目前我还不清楚不在jetyll下，有没更好的预览方式，有知道的朋友，可以给我留言，学习学习。

### Markdown语法简介

一些常用的mardown基础语法：

**粗体**：
```js
**文字**
```
*斜体*：
```java
*文字*
```
[超链接](http://github.com)：
```
[连接文字内容](http://超链接地址)：
```
图片引入：
```
![](图片地址，网络图片：http//,本地图片：/images/)：
```
标题：
```
[连接文字内容](http://超链接地址)：
```

<font size="6" color="red">代码块(最关键的)：</font>

    ```java
        public void main(arg[] String){

            System.out.println("hello，world！");//输出hello，world！
        
        }
    ```



输出结果：

```java
    public void main(arg[] String){

        System.out.println("hello，world！");//输出hello，world！
    
    }
```

本篇博文包含大多数常用的markdown语法，可以查看博文的md文件。

*更多的语法，请参考：[Markdown 语法说明(简体中文版)](http://www.appinn.com/markdown/)*