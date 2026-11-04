---
title: Create a personal website for free with GitHub
description: Start with one page and publish your introduction, writing, and work with GitHub Pages. Give people a link to get to know you.
---
## What will you get?

A public personal website at an address such as `https://username.github.io`. GitHub stores your files; GitHub Pages publishes them as a website. The free option requires a public repository and suits personal homepages, blogs, and portfolios. See the [GitHub Pages quickstart](https://docs.github.com/en/pages/quickstart).

“Free” here means free hosting and a platform subdomain, with no server or custom domain to buy. Domain registration and renewal, paid templates, and paid agents are separate expenses. You can complete these steps in your browser.

## 1. Prepare your first page

Start with three things: who you are, what you are doing, and the work or writing you want people to see. A simple homepage is enough.

You can use the page below. Replace the name, introduction, and link with your own; `https://example.com` is only a placeholder.

```
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Lin's personal website</title>
</head>
<body>
  <main>
    <h1>Hello, I'm Lin.</h1>
    <p>I enjoy writing and photography, and I'm learning to make websites.</p>
    <h2>My work</h2>
    <p><a href="https://example.com">Explore my work</a></p>
  </main>
</body>
</html>
```

If you already use an agent, give it your introduction and ask: “Make a personal homepage that also reads well on a phone. Use plain HTML and CSS, name the homepage index.html, and avoid backends or paid services.” Review the result before publishing.

## 2. Create a GitHub repository

1. Sign up for [GitHub](https://github.com) and sign in. A repository is where your website files live.
2. Select **New repository**. Name it `username.github.io`, replacing `username` with your GitHub username in lowercase.
3. Choose **Public**, enable **Add README**, and create the repository.
4. Select **Add file → Create new file**, name it `index.html`, and paste and personalize the page above. Select **Commit changes** to save to `main`. If you already have website files, use **Upload files** instead.

Put `index.html` directly in the repository root, without an extra enclosing folder. The source files in a public repository are visible too, so include only what you want to share. See the entry-file requirements in [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## 3. Turn on GitHub Pages

1. Open the repository’s **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose `main` and `/(root)`, then click **Save**.
4. Wait for publication, then click **Visit site** in the Pages settings to open `https://username.github.io`.

Publication can take a few minutes. If you see a 404, check the repository name, publishing branch, and lowercase `index.html` in the root. Check **Actions** for deployment results. These steps cover plain HTML; frameworks that require a build need their own deployment configuration.

## 4. Update your site and keep it free

Edit `index.html` or upload new files and save to `main` to publish an update. The repository keeps a version history of your changes.

A published GitHub Pages site must be no larger than 1 GB, with a soft bandwidth limit of 100 GB per month. Pages serves static content, with no runtime for databases or server-side programs. It must not host sites primarily intended for commercial transactions or commercial SaaS. See [GitHub Pages limits](https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits).

## 5. Make this your place on the web

Open the site on a phone and computer, check the text and work links, then add the address to your profile or signature. Start with writing, work, and links to websites you enjoy; you can add more features over time.

Once your site is ready, use “Share your website” below to apply for the Web 2.0 Next directory. If you would prefer to upload files directly from your computer, read the companion Cloudflare guide.

## 6. Add a custom domain to your free website (optional, paid)

Once your site is live, you can keep using `username.github.io` for free or register a custom domain, perhaps based on your name. Your website can remain on GitHub Pages’ free hosting plan, with domain registration and renewal paid separately.

When you are ready for your own address, read [How to register a domain](/register-domain) to compare registrars such as Cloudflare and Vercel, learn the registration steps, and understand renewal costs. Then follow its GitHub Pages connection instructions. You can keep your existing content without rebuilding the site.
