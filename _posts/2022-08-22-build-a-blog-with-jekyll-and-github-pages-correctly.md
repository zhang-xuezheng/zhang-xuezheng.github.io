---
layout: post
title: "基于 Jekyll 和 GitHub Pages 正确地搭建博客"
---

使用 GitHub Pages 搭建博客是个一劳永逸的过程，开头配置好了，以后只管内容创作，无需再操心技术层面的事。本文面向希望专注内容创作的博主，无技术基础要求。

## 准备工作

打开 [GitHub 官网](https://github.com)，注册、登入，点击页面右上角加号按钮，再点击 “New repository” 按钮以新建一个 GitHub 仓库。

> GitHub Pages is available in public repositories with GitHub Free and GitHub Free for organizations.
>
> 免费账号只能在公开仓库中使用 GitHub Pages 功能。

如果想使用内置主题：Settings - Pages - Theme Chooser - Choose a theme

## 配置

点击 “creating a new file” 链接，新建一个 `_config.yml` 文件，内容如下：

```yaml
theme: minima # 如果上一步没使用 Theme Chooser 的主题，则可在此手动指定主题
title: 张学征 # 博客名
description: 自由开发者 # 博客描述
permalink: /:categories/:title:output_ext # 建议指定文章链接格式（域名/分类名/文章标题.html）
```

链接：[GitHub Pages 内置主题仓库列表](https://pages.github.com/themes/)

所有字段都是可选的，不提供也没问题。建议设置 `permalink` ，可使文章 URL 更优雅。

点击绿色的 “Commit new file” 按钮保存。

## 主页

新建一个 `index.md` 文件：

```yaml
---
layout: home # 使用 home 布局
---
```

保存后前往 Settings - Pages 可以看到 GitHub Pages 已经自动执行了一次部署。点击 “Visit site” 按钮就能看到效果。

## 关于页面

新建一个 `about.md` 文件：

```yaml
---
layout: page # 使用 page 布局
title: 关于 # 页面标题
permalink: /about.html # 指定页面渲染后的 URL
---

联系我：`zhang+xuezheng#foxmail.com`（加号换点，井号换@）
```

## 第一篇文章

新建一个 `_post/2022-08-22-hello-world.md` 文件：

```yaml
---
layout: post # 使用 post 布局
title: "世界你好"
---

这是文章正文，开始尽情创作吧。
```

保存，稍等几分钟后访问：[https://zhang-xuezheng.github.io](https://zhang-xuezheng.github.io)

一个拥有主页、文章列表、RSS订阅、关于页面的博客已经运行起来，麻雀虽小五脏俱全。

Happy Jekylling!
