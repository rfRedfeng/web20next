---
title: 用 GitHub 零成本创建个人网站
description: 从一个网页开始，用 GitHub Pages 免费发布个人介绍、文章和作品，让别人通过一个链接认识你。
---
## 你会得到什么？

一个可以公开访问的个人网站，地址形如 `https://username.github.io`。GitHub 保存你的网页文件，GitHub Pages 将它们发布成网站。免费方案需要使用公开仓库，适合个人主页、博客和作品展示。参见 [GitHub Pages 入门指南](https://docs.github.com/en/pages/quickstart)。

这里的“零成本”指使用免费托管和平台提供的子域名，不购买服务器或独立域名。购买及续费自己的域名、付费模板或付费 Agent 的费用不包含在内。你可以只用浏览器完成下面的步骤。

## 1. 准备你的第一页

先写下三样内容：你是谁、你正在做什么、你希望别人看到的作品或文章。一个简单的首页就足够开始。

下面是可以直接使用的网页。把名字、介绍和链接换成自己的内容；`https://example.com` 只是示例地址。

```
<!doctype html>
<html lang="zh-Hans">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>小林的个人网站</title>
</head>
<body>
  <main>
    <h1>你好，我是小林。</h1>
    <p>我喜欢写作、摄影，也在学习做网站。</p>
    <h2>我的作品</h2>
    <p><a href="https://example.com">看看我的作品</a></p>
  </main>
</body>
</html>
```

如果你已经在使用 Agent，也可以把自己的介绍交给它：“请帮我做一个手机上也能阅读的个人主页，使用纯 HTML 和 CSS，首页命名为 index.html，不依赖后端或付费服务。”然后先检查内容，再发布。

## 2. 创建 GitHub 仓库

1. 注册并登录 [GitHub](https://github.com)。仓库（repository）就是存放网站文件的地方。
2. 选择 **New repository**，名称填写 `username.github.io`，把 `username` 换成自己的 GitHub 用户名，字母使用小写。
3. 可见性选择 **Public**，启用 **Add README**，然后创建仓库。
4. 在仓库中选择 **Add file → Create new file**，文件名填写 `index.html`，粘贴并修改上面的网页，选择 **Commit changes** 保存到 `main` 分支。如果已有网页文件，也可以选择 **Upload files** 上传。

`index.html` 应直接放在仓库根目录，而不是再套一层文件夹。公开仓库里的源文件也可以被别人查看，只放你愿意公开的内容。入口文件规则见 [创建 GitHub Pages 网站](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)。

## 3. 开启 GitHub Pages

1. 打开仓库的 **Settings → Pages**。
2. 在 **Build and deployment** 下，将 **Source** 设为 **Deploy from a branch**。
3. 分支选择 `main`，目录选择 `/(root)`，点击 **Save**。
4. 等待发布完成，再从 Pages 设置中点击 **Visit site**，打开 `https://username.github.io`。

发布可能需要几分钟。如果出现 404，先检查仓库名称、发布分支，以及根目录中是否有小写的 `index.html`；再到 **Actions** 查看发布是否成功。上面的步骤适用于纯 HTML 网页，需要构建的框架项目应使用对应的发布配置。

## 4. 更新网站，保持零成本

以后修改 `index.html` 或上传新文件，保存到 `main` 分支，Pages 就会重新发布。网页文件在仓库里有版本记录，可以查看以前的修改。

GitHub Pages 发布后的网站大小不能超过 1 GB，每月带宽软限制为 100 GB。它适合静态内容，不提供运行数据库或服务端程序的环境，也不应用来经营以交易或商业 SaaS 为主要目的的网站。限制以 [GitHub Pages 使用限制](https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits) 为准。

## 5. 让这个网址成为你的入口

用手机和电脑各打开一次，确认文字可读、作品链接能访问，再把网址放到个人简介或签名里。继续写文章、补充作品、链接到喜欢的网站，比一次做出很多功能更容易开始。

网站准备好后，可以通过下方的“分享你的网站”入口申请加入 Web 2.0 Next 名录。如果更想直接上传电脑里的文件，也可以阅读另一篇 Cloudflare 教程。

## 6. 给免费网站加上域名（可选，需付费）

网站上线后，你可以继续免费使用 `username.github.io`，也可以为它注册一个独立域名，例如自己的名字。网站仍然可以托管在 GitHub Pages 的免费方案上，域名的注册和续费则需要另行付费。

准备好拥有自己的地址时，可以阅读[如何注册域名](/zh/register-domain)，了解 Cloudflare、Vercel 等注册商的选择、申请步骤和续费成本，再按其中的 GitHub Pages 连接说明完成绑定。原有网页内容可以继续使用，不需要重新建站。
