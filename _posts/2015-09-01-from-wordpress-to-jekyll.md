---
layout: post
title: "从虚拟主机到github，搭配Jekyll就是爽 "
modified:
categories: tech
excerpt:
tags: [GIT]
---
{% include JB/setup %}

很早的时候就有了自己的博客了，那时候是用wordpress搭建的，买的一个香港的虚拟主机，很慢，每年都要续费之类的，后来写着写着就没坚持。

前几年经常在群里听到说他博客迁移到github上，我当时挺纳闷，那是怎么弄的，刚好我现在有个同事博客是用jekyll搭建的，再加上某天在网上搜到github page 可以免费托管，如是我看完了那篇wiki，马上就想自己也来重新把博客搞起来。就这样我的博客从wordpress 切换为jekyll，使用Github page 搭配jekyll有很多优点：


* 轻量级的博客系统，配置简单
* 无需自己搭建服务器，主机免费
* 使用标记语言Markdown语法
* Github方便管理控制

下面介绍下如何搭建自己的博客


## 注册以及配置Github

###1、注册Github
首先打开[Github](http://github.com), 如果打不开，可能被墙了。填入注册信息， 用户名最好不要太长。注册完成后，你的github主页就是https://github.com/yourname。

###2、绑定 Github
参考 [生成 ssh，并与 Github 帐号绑定](https://help.github.com/articles/generating-ssh-keys/)

###3、设置Git
	git config --global user.name "Your Name Here"
	git config --global user.email "your_email@example.com"
	git config --global user.name    # 确保设置成功
	git config --global user.email


##使用GitHub Pages建立博客

与GitHub建立好链接之后，就可以方便的使用它提供的Pages服务，GitHub Pages分两种，一种是你的GitHub用户名建立的username.github.io这样的用户&组织页（站），另一种是依附项目的pages。

创建一个新的项目，命名为 yourname.github.io, （这里千万要注意，yourname必须跟你Github的帐户是一致的）具体参考[这里](https://pages.github.com/)。

项目创建OK后，在命令行新建个文件夹，然后进当前目录，git clone下来，开始搭建本地环境

以下介绍下mac下的安装流程

首先安装rvm，rvm的安装可以参考[这里](https://rvm.io/rvm/install)，或者敲入以下命令。

	$ \curl -sSL https://get.rvm.io | bash -s stable

然后安装ruby

	$ rvm install 2.2.0
	$ rvm use 2.2.0 --default



然后安装jekyll

	$ gem install jekyll


启动本地环境

	$ jekyll serve

这个时候，你就可以通过localhost:4000来访问了。



##后续

###绑定自己的域名
在项目根目录新建CNAME文件，填入你申请好的域名

###评论

评论插件为Disqus

###代码语法高亮

如果写技术博客，代码高亮少不了，本地需要安装Pygments，具体可以参考[这里](http://havee.me/internet/2013-08/support-pygments-in-jekyll.html)






