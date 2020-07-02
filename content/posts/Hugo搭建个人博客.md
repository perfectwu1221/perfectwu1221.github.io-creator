---
title: "第二篇博客"
date: 2020-07-01T07:35:49+08:00
draft: false
---
#### 步骤1：安装
[安装HUGO](https://github.com/gohugoio/hugo/releases)
下载windows-64bit.zip的版本
解压后把hugo.exe放到【自己设置的常用位置】如D:\software\hugo\,把路径加到PATH中。
重启终端，试试成功没，运行hugo version，查看版本。
#### 步骤2：创建一个新站
找个空目录打开终端，hugo new site perfectwu1221.github.io-creater，创建
#### 步骤3：加个皮肤主题
```
cd quickstart
git init
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
```
#### 步骤4：加点内容
**在 xxx.github.io-creator 目录（注意确保自己不在 public 目录）**里运行`hugo new posts/文章名字.md`
执行命令`code posts/文章名字.md` 对文件进行编辑。
```
---
title: "My First Post"
date: 2019-03-26T08:47:11+01:00
draft: true //这里改成false才能发表，draft是草稿的意思，true就是不发表
---
```
#### 步骤5：开始Hugo server
`hugo server -D`,第一次运行，会添加public目录，下次有新文章更新，得先`hugo -D`更新public目录再去目录里git add . ; git commit -m 更新描述 ; git push -f
#### 步骤6：配置博客
打开config.toml编辑
```
baseURL = "https://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "ananke"
```
改动一下
```
baseURL = "你的GitHub pages，在GitHub new repostories后，settings里面找，注意repostories取名必须[你的用户名.github.io]"
languageCode = "zh-Hans"
title = "博客网站的名字，不是博客文章名字"
```
#### 如何创建第二篇博客
在 xxx.github.io-creator 目录（注意确保自己不在 public 目录）里运行 hugo new posts/第二篇博客.md
运行 code posts/第二篇博客.md 对文件进行编辑，注意不要把文件原本的内容给删了，直接在后面另起一行写新内容。
运行 hugo -D，得到新的 public 目录
进入 public 目录，执行一下操作
git add . 注意有一个点
git commit -m update
git push -f 其中 -f 是强制上传的意思
等待几分钟后，你的博客就会出现第二篇文章了！