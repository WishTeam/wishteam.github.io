---
layout: post
title: 使用github pages和jekyll搭建博客
tags:
- github pages
- jekyll
- blog
categories: jekyll
author: linyuliang
description: 使用github pages和jekyll搭建博客的教程。
---
# 使用github pages和jekyll搭建博客
如果你想要搭建一个免费流量，免费公网域名，简单的中小型博客，那么使用github pages+jekyll可以很好的满足你的需求。搭建博客，你需要准备的东西有：
* 注册一个自己的[github](https://github.com/)的账号。
* 了解什么是[github-pages](https://help.github.com/categories/github-pages-basics/)，以及它的使用限制，并且发布一个自己的Github Pages，也就是博客。特别要注意的是：不要将自己的敏感信息（例如：各类账号密码等）放到博客的代码上，因为这个博客的代码是公开，且所有人可见的。
* 会使用git客户端工具（windows可以使用[tortoisegit](https://tortoisegit.org/download)），本地clone一个github pages的代码库。
* 本地jekyll的开发环境，需要安装[ruby和rubyGems](https://rubyinstaller.org/downloads/)
* 了解什么是[jekyll](http://jekyll.com.cn/)，jekyll的[基本用法](http://jekyll.com.cn/docs/usage/)，选择一个漂亮的[jekyll主题模板](http://jekyllthemes.org/)
* 编写博客需要了解的[Liquid](https://liquid.bootcss.com/)模板语言，[Markdown](http://wowubuntu.com/markdown/)语法以及HTML & CSS的基本网页编写知识。




<!-- more -->
## 注册一个github的账号
这个不用写了，请注册完，登录github

## 创建github-pages博客
1. 登录后，点击下图中的绿色按钮，新建一个代码库
![新建一个代码库](/images/githubJekyllBlog/newRepository.bmp)
2. 新建一个个人的博客代码库，域名为github注册用户名.github.io
![新建一个个人博客](/images/githubJekyllBlog/newGithubPages.bmp)
3. 创建后，在该代码库的settings标签页下面，为GitHub Pages挑选一个jekyll初始主题

  选择settings标签页
  ![选择settings标签页](/images/githubJekyllBlog/settings.bmp)
  选择一个主题，在里面选择完主题后，会弹出一个readMe的文件提交，直接提交
  ![选择jekyll主题](/images/githubJekyllBlog/chooseJekyllTheme.bmp)
4. 最后直接访问域名，刷新即可看见初始博客
![显示第一个jekyll博客](/images/githubJekyllBlog/showFirstBlog.bmp)

到这里，实际上你的jekyll博客已经搭建好了。后续就是定制化jekyll模板，以及提交博客文章。

## clone一个上面新建的博客代码库到本地进行编辑
1. 这里使用[tortoisegit](https://tortoisegit.org/download)直接clone博客的代码库到本地
![clone博客代码](/images/githubJekyllBlog/gitClone.bmp)

## 选择一个定制化的博客模板
1. 在[jekyll主题模板站](http://jekyllthemes.org/)上挑选一个漂亮的博客模板（本博客使用的模板为[jacman](https://github.com/simpleyyt/jekyll-jacman)），将代码下载下来。（模板大部分都是个人简历和博客类的，了解jekyll的，也可以自己编写模板，实际上就是静态网页组织起来，最主要是_config.yml配置文件，用于定制化配置）
2. 将下载下来的博客模板代码，解压覆盖到本地的github博客代码库目录
![替换jekyll主题](/images/githubJekyllBlog/replaceTheme.bmp)
3. 上图中的Gemfile.lock文件可以删除，不然有可能报各类gem源找不到问题

## 本地运行jekyll服务进行编辑调试
1. 首先安装ruby环境：[ruby和rubyGems](https://rubyinstaller.org/downloads/)
2. 安装完毕后，打开cmd窗口，使用ruby -v和gem -v命令，验证是否安装好，正常应该会返回版本号
![ruby gem安装验证](/images/githubJekyllBlog/rubyInstall.bmp)
3. cmd窗口移动到博客代码库目录下，执行jekyll serve --watch命令，启动web服务
![启动jekyll的web服务](/images/githubJekyllBlog/jekyllBlog.bmp)
4. 使用http://127.0.0.1:4000/来查看博客页面
![查看博客页面](/images/githubJekyllBlog/jekyllShowBlog.bmp)
5. 修改模板中的个性化配置，主要是_config.yml文件。（其他文件也可能有个性化修订，大部分主题都有使用说明，请认真阅读主题使用说明）

## 提交修改后的博客代码
1. 使用tortoisegit提交代码到master分支，并push到github上
2. 然后就可以使用 https://你的github用户名.github.io 访问你的博客了

## 编写博客步骤
1. 选择博客的编辑工具，个人推荐[Atom](https://atom.io/),另一个最常见的编辑工具是[sublime](http://www.sublimetext.com/)。
2. 在你的代码库的_posts目录下新建博客文件，由于模板不同，博客头信息应该略用不同。具体怎么编写博客，可以参考你下载jekyll主题里面的例子，主题对应github库上的说明，以及[jekyll](http://jekyll.com.cn/)上的说明教程。
3. 编写博客前一定要先熟悉jekyll整个工程目录结构，需要了解的[Liquid](https://liquid.bootcss.com/)模板语言，[Markdown](http://wowubuntu.com/markdown/)语法以及HTML & CSS的基本网页编写知识。
4. 编写完博客后，可以在本地使用jekyll serve --watch先自己预览，没问题后，再提交github，刷新博客域名，即可看见自己发的博客

## 参考其他建博客教程
* [blogways上的jekyll博客搭建教程](http://www.blogways.net/categories/jekyll/)
* [阮一峰的《搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门》](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)

## 最后
1. 关于jekyll插件：github上有一些，最常用的评论插件多说关闭了，Disqus被墙了，有人自建评论服务，目前我还没有选择，没评论功能，博客功能等于少一半。。。
2. 关于jekyll模板，实际还是看静态代码组织能力，有时间的话，倒是可以自己写个漂亮的静态jekyll模板，目前这个博客模板对我来说足够，也就不折腾了。
3. 嗯嗯，最后也搞个微信打赏二维码，希望我的cube代码框架和博客都能写的越来越好，关注的人越来越多。
![微信扫码捐赠](/images/linyuliang_weixin_tip.jpg)
