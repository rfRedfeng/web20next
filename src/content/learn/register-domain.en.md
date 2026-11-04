---
title: How to register a domain for your personal website
description: Choose a name and registrar, register and renew your domain, and connect it to your site. Explore Cloudflare, Vercel, Name.com, GoDaddy, and other registrars.
---
## A domain is the address; your site is the content

A domain such as `example.com` is how people find you. Hosting stores and publishes your website files; DNS points the name to the service hosting your site. Registering a domain does not create a website, and your registrar and host do not have to be the same company.

You can publish with a free GitHub Pages `github.io` or Cloudflare Pages `pages.dev` address first. A custom domain usually costs an annual fee and needs renewal. It lets you keep your public address when you move to another host.

## 1. Choose a name you want to keep

Start with your name, usual nickname, or a lasting creative interest. Keep it short, easy to spell, and easy to say aloud. Prepare a few alternatives, then compare availability and costs for extensions such as `.com`, `.me`, and `.dev`.

Check first-year and renewal prices, minimum registration terms, taxes, and included privacy protection. An introductory discount does not guarantee cheap renewals; Premium domains may also cost more to register or renew. Estimate three years as “first-year price + two annual renewals” rather than comparing promotional prices alone. Actual costs may change with registrar and registry pricing.

## 2. Our first recommendations: Cloudflare and Vercel

### Cloudflare Registrar

Consider [Cloudflare Registrar](https://www.cloudflare.com/domains/) first if you plan to use Cloudflare Pages or want your domain and DNS in one place. It offers registration and renewal at cost, without marking up registry and ICANN charges. This does not mean prices never change or that every extension is the cheapest available.

Domains registered there must use Cloudflare nameservers; you cannot simply switch them to another DNS provider. Your site can still live on GitHub Pages, Vercel, or another host by setting the appropriate DNS records in Cloudflare. See the [Cloudflare registration guide](https://developers.cloudflare.com/registrar/get-started/register-domain/) for supported extensions and requirements.

### Vercel Domains

If you already manage a site on Vercel, consider [Vercel Domains](https://vercel.com/domains) first to keep the domain and project in one dashboard. After purchase, you can assign it to a project and manage DNS in domain settings. See [Working with domains on Vercel](https://vercel.com/docs/domains/working-with-domains).

Check [Vercel’s domain pricing](https://vercel.com/domains/pricing) for registration, renewal, transfer, and privacy details for your chosen extension. Domain registration is charged separately from hosting; a free hosting plan does not include a free custom domain.

## 3. Other registrars worth comparing

Alongside Cloudflare and Vercel, search for the same domain on these platforms and compare first-year and renewal prices before choosing where to register it.

- [Name.com](https://www.name.com/): An established option for domain search, registration, and management. Check renewal prices and privacy conditions for your chosen extension.
- [GoDaddy](https://www.godaddy.com/domains): Another established domain registration platform. Check the minimum purchase term, renewal total, and cart extras when comparing offers, and select only what you need.
- [Namecheap](https://www.namecheap.com/): An option for comparing registration and transfer prices. Distinguish introductory discounts from later renewal costs.
- [Spaceship](https://www.spaceship.com/): Also offers domain registration. Compare registration, renewal, and transfer costs for the same extension rather than choosing solely on first-year pricing.
- [Dynadot](https://www.dynadot.com/): Another option for registering and managing domains. Check availability, then review the registration term and total price.

Your registrar does not determine where you must host your website. Prioritize ongoing costs, DNS management, and an interface you find comfortable to use.

## 4. Complete registration

1. **Create your own account.** Use an email address you expect to keep and enable two-factor authentication. Keep the domain in an account you control.
2. **Search the complete name.** Use **Register domains** in Cloudflare, the Domains search on Vercel, or the registrar’s search box. Check spelling, extension, and final availability.
3. **Review the purchase.** Confirm the term, initial total, renewal price, and auto-renewal choice. A domain alone does not require a website builder, email, or hosting bundle.
4. **Enter contact details and pay.** Provide accurate registrant information and complete any email or identity verification required by the provider and extension. Privacy protection hides some public details; it does not remove the need for accurate information.
5. **Confirm the domain is in your account.** Check registration status and expiration date, keep the receipt, and make sure renewal reminders can reach you.

If an agent helps you compare options, ask: “Compare these domains’ first-year and renewal costs at Cloudflare, Vercel, and other registrars. Show three-year estimates, DNS restrictions, and privacy conditions.” Check the final checkout total before purchasing.

## 5. Connect the domain to your website

Add the domain to your hosting platform first, then set records where DNS is actually managed. Your registrar and DNS provider may differ: the current nameservers determine where to edit records. Replace `example.com`, `username`, and project names below with your own values.

### Connect GitHub Pages

You can start with `www.example.com`. Follow GitHub’s instructions to verify ownership, then save it under the repository’s **Settings → Pages → Custom domain**. In your DNS dashboard, create a `CNAME` for `www` pointing to `username.github.io`, without `https://` or a repository path. Enable **Enforce HTTPS** once verification and the certificate are ready. To also use the apex domain `example.com`, follow the records in [GitHub’s custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

### Connect Cloudflare Pages

Open the Pages project’s **Custom domains → Set up a domain** and follow the instructions. An apex domain such as `example.com` requires Cloudflare DNS in the same Cloudflare account as the Pages project; the registrar can be elsewhere. For a subdomain such as `www.example.com`, you can keep external DNS and point a `CNAME` to the project’s `pages.dev` address. Add the domain in Pages before changing DNS. See [Cloudflare Pages custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/).

DNS changes and HTTPS certificates can take time. Preserve existing email and other records when changing DNS providers, then check your site using its full `https://` address. Update your profile links once it works.

## 6. Keep the address yours

Enable auto-renewal, keep your payment method and contact email current, and set a separate expiration reminder. Registration is an ongoing commitment, not permanent ownership from a single purchase.

If you do not have a site yet, start with [GitHub](/github-pages) or [Cloudflare](/cloudflare-pages). Publish your content, then choose an address you want to keep.
