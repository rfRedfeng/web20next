---
title: Create a personal website for free with Cloudflare
description: Drag your website files into Cloudflare Pages and publish a free personal homepage, without learning Git or using the command line.
---
## What will you get?

A personal website hosted on Cloudflare Pages, using an assigned `pages.dev` subdomain. This guide uses browser uploads. You need a Cloudflare account and a folder of website files, with no GitHub repository required.

“Free” here means the free plan, a platform subdomain, and a static website. Static sites consist of HTML, CSS, images, and other files without server-side programs. Pages offers free, unlimited static asset requests that do not invoke Functions. Dynamic features have separate quotas or charges; see [Cloudflare Pages pricing](https://developers.cloudflare.com/pages/functions/pricing/). Domain registration and renewal, paid templates, and paid agents are separate expenses.

## 1. Prepare your website files

Create a folder called `my-site` on your computer. Use a plain-text editor to create `index.html` with UTF-8 encoding. Paste the page below and replace the name, introduction, and work link; `https://example.com` is a placeholder. Make sure the filename is not `index.html.txt`.

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

Double-click `index.html` to preview it in your browser. You can later add images, CSS, and more pages to the folder and reference them from your site.

If you already use an agent, ask: “Make a static personal homepage that also reads well on a phone. Give me a folder ready to upload, with index.html at its root and no backend or paid services.” If your framework requires a build, upload its generated static output, not the entire source project.

## 2. Upload to Cloudflare Pages

1. Sign up and sign in to the [Cloudflare dashboard](https://dash.cloudflare.com). Open **Workers & Pages**.
2. Select **Create application**, then the Pages **Get started → Drag and drop your files** option.
3. Name your project, for example `my-personal-site`. Upload the `my-site` folder or a ZIP archive, with `index.html` at the upload’s root.
4. Select **Deploy site** and open the production `pages.dev` address shown in the dashboard. A taken name may receive extra characters; use the address provided.

See the [Direct Upload guide](https://developers.cloudflare.com/pages/get-started/direct-upload/). For a homepage 404, check the name and location of `index.html`. For missing images, check paths and capitalization.

## 3. Update your website

Edit and preview the files locally. In the same Pages project, select **Create a new deployment**, choose **Production**, and upload the complete website folder. After deployment succeeds, your existing production address shows the new version.

Keep a local backup for future edits or migration. Uploaded files become public website content, so include only what you want to share.

## 4. Free limits and next steps

Dashboard uploads support up to 1,000 files, each no larger than 25 MiB. More than 1,000 files requires another upload method; a Pages site on the free plan can contain up to 20,000 files. Git integration includes 500 builds per month on the free plan. See [Pages platform limits](https://developers.cloudflare.com/pages/platform/limits/).

With a static site and a `pages.dev` address, you do not need to buy a server or domain. Check the relevant quotas and prices before adding Functions, databases, paid services, or a custom domain.

For automatic publication after repository changes, choose [Git integration](https://developers.cloudflare.com/pages/get-started/git-integration/) when creating a project and connect GitHub or GitLab. An existing Direct Upload project cannot switch to Git integration; you need a new project. Choose Git integration from the start if you already know you want automatic deployments.

## 5. Share your website

Check the production address on a phone and computer. Once the introduction, images, and work links look right, put the URL in your profile or signature. A small site with real content gives people a place to get to know you.

Use “Share your website” below to apply for the Web 2.0 Next directory when your site is ready. For a way to keep your website files and their edit history on GitHub, read the companion GitHub guide.

## 6. Add a custom domain to your free website (optional, paid)

Once your site is live, you can keep using its assigned `pages.dev` address for free or register a custom domain. Your website can remain on Cloudflare Pages’ free hosting plan, with domain registration and renewal paid separately.

When you are ready for your own address, read [How to register a domain](/register-domain) to compare registrars such as Cloudflare and Vercel, learn the registration steps, and understand renewal costs. Then follow its Cloudflare Pages connection instructions. You can connect the domain to your existing Pages project without rebuilding the site.
