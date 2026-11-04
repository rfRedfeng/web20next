---
title: 用 Cloudflare 零成本创建个人网站
description: 把网页文件拖进 Cloudflare Pages，免费发布自己的主页，不需要先学会 Git 或使用命令行。
---
## 你会得到什么？

一个托管在 Cloudflare Pages 上的个人网站，使用平台分配的 `pages.dev` 子域名。本文采用网页拖拽上传的方式，只需要 Cloudflare 账号和一个装有网页文件的文件夹，不需要 GitHub 仓库。

这里的“零成本”指使用免费方案、平台子域名和纯静态网页。静态网页由 HTML、CSS、图片等文件组成，不需要运行服务端程序。Pages 对不调用 Functions 的静态资源请求免费且不限次数；动态功能另有额度或计费规则，参见 [Cloudflare Pages 计费说明](https://developers.cloudflare.com/pages/functions/pricing/)。购买及续费独立域名、付费模板或付费 Agent 的费用不包含在内。

## 1. 准备网页文件

在电脑上新建文件夹 `my-site`，用纯文本编辑器创建 `index.html`，保存为 UTF-8 编码。把下面的内容粘贴进去，换成自己的名字、介绍和作品链接；`https://example.com` 只是示例地址。注意文件名不要变成 `index.html.txt`。

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

双击 `index.html`，先在浏览器里看看效果。以后可以把图片、CSS 和其他页面放进同一文件夹，并在网页中引用。

如果你已经在使用 Agent，也可以请它：“帮我制作一个手机上也能阅读的纯静态个人主页，输出可直接上传的文件夹，根目录包含 index.html，不使用后端或付费服务。”如果使用需要构建的框架，应上传构建后的静态输出，而不是整个源码工程。

## 2. 上传到 Cloudflare Pages

1. 注册并登录 [Cloudflare 控制台](https://dash.cloudflare.com)，进入 **Workers & Pages**。
2. 选择 **Create application**，进入 Pages 的 **Get started → Drag and drop your files** 上传入口。
3. 填写项目名，例如 `my-personal-site`，上传 `my-site` 文件夹或其 ZIP 压缩包，确保上传内容的根目录包含 `index.html`。
4. 点击 **Deploy site** 完成发布，打开控制台显示的正式 `pages.dev` 地址。如果名称已被占用，实际地址可能附加字符，以控制台显示为准。

完整操作见 [Direct Upload 官方指南](https://developers.cloudflare.com/pages/get-started/direct-upload/)。如果首页出现 404，先检查 `index.html` 的位置和文件名；图片不显示时，检查引用路径和大小写。

## 3. 更新网站

在电脑上修改网页并预览，随后进入同一个 Pages 项目，选择 **Create a new deployment**，使用 **Production** 环境上传完整的网站文件夹。发布成功后，正式网址会显示新版本，不需要每次新建项目。

保留本地文件的备份，方便继续编辑或迁移。上传内容会成为公开网页，只放你愿意公开的文件。

## 4. 免费范围与后续选择

控制台拖拽上传最多支持 1,000 个文件，单个文件最大 25 MiB。超过 1,000 个文件需要其他上传方式，Pages 免费方案的网站文件总量上限为 20,000 个。使用 Git 集成时，免费方案每月提供 500 次构建。具体以 [Pages 平台限制](https://developers.cloudflare.com/pages/platform/limits/) 为准。

保持纯静态网站并使用 `pages.dev` 地址，就不需要购买服务器或域名。添加 Functions、数据库、付费服务或独立域名前，再核对对应的额度和费用。

如果你希望以后每次修改仓库都自动发布，可以在创建项目时选择 [Git 集成](https://developers.cloudflare.com/pages/get-started/git-integration/)，连接 GitHub 或 GitLab。已创建的 Direct Upload 项目不能直接改成 Git 集成，需要另建项目；如果你已经确定要用自动发布，可以一开始就选 Git 集成。

## 5. 分享你的网站

用手机和电脑检查正式网址，确认介绍、图片和作品链接都正常，再把它放到个人简介或签名里。一个有真实内容的小网站，就可以成为别人认识你的入口。

网站准备好后，可以通过下方的“分享你的网站”入口申请加入 Web 2.0 Next 名录。想把网页文件和修改记录一起保存在 GitHub，也可以阅读另一篇 GitHub 教程。

## 6. 给免费网站加上域名（可选，需付费）

网站上线后，你可以继续免费使用平台分配的 `pages.dev` 地址，也可以为它注册一个独立域名。网站仍然可以托管在 Cloudflare Pages 的免费方案上，域名的注册和续费则需要另行付费。

准备好拥有自己的地址时，可以阅读[如何注册域名](/zh/register-domain)，了解 Cloudflare、Vercel 等注册商的选择、申请步骤和续费成本，再按其中的 Cloudflare Pages 连接说明完成绑定。域名可以接到现有 Pages 项目，不需要重新建站。
