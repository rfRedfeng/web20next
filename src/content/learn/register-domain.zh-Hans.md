---
title: 如何注册域名，让个人网站拥有自己的地址
description: 从挑选名字、选择注册商到付款、续费和连接网站，认识 Cloudflare、Vercel、Name.com、GoDaddy 等域名注册平台。
---
## 域名是地址，网站是内容

域名是别人找到你的地址，例如 `example.com`；托管服务负责保存和发布网站文件；DNS 则把这个名字指向网站所在的服务。注册域名不会自动生成网站，也不需要在同一家公司购买域名和托管。

你可以先用 GitHub Pages 的 `github.io` 或 Cloudflare Pages 的 `pages.dev` 免费地址发布，再决定是否注册独立域名。独立域名通常按年付费，需要续费；它让你在更换托管平台后，仍能沿用同一个对外地址。

## 1. 选一个愿意长期使用的名字

优先考虑自己的名字、常用昵称或长期创作主题，尽量简短、容易拼写和口头转述。想好两三个备选，再比较 `.com`、`.me`、`.dev` 等后缀的可用性和费用。

结算前一起看首年价格、续费价格、最低注册年限、税费及隐私保护是否包含。首年促销不等于每年都便宜；标记为 Premium 的域名也可能有更高的注册或续费费用。用“首年价格 + 两年的续费价格”估算三年成本，比只看促销价更实用，实际费用仍可能随平台和注册局定价调整。

## 2. 优先推荐：Cloudflare 和 Vercel

### Cloudflare Registrar

如果你准备使用 Cloudflare Pages，或希望把域名和 DNS 放在一起管理，可以优先考虑 [Cloudflare Registrar](https://www.cloudflare.com/domains/)。它对域名注册和续费采用成本价模式，不在注册局和 ICANN 收费上加价；这不代表价格永远固定，也不保证每一种后缀都是市场最低价。

在 Cloudflare 注册的域名必须使用 Cloudflare 的 nameservers（域名服务器），不能直接切换到其他 DNS 服务商。网站仍然可以托管在 GitHub Pages、Vercel 等平台，只需在 Cloudflare 配置相应的 DNS 记录。支持的后缀和注册条件见 [Cloudflare 域名注册指南](https://developers.cloudflare.com/registrar/get-started/register-domain/)。

### Vercel Domains

如果你已经在 Vercel 上管理网站，可以优先考虑 [Vercel Domains](https://vercel.com/domains)，把域名和项目放在同一个控制台里。购买后可以分配给项目，并在域名设置中管理 DNS；具体操作见 [Vercel 域名管理说明](https://vercel.com/docs/domains/working-with-domains)。

购买前查看 [Vercel 域名价格表](https://vercel.com/domains/pricing)，分别确认注册、续费和转入费用，以及所选后缀的隐私保护。域名注册费与网站托管方案分开计算，免费托管不代表独立域名免费。

## 3. 其他值得比较的注册商

除了 Cloudflare 和 Vercel，也可以在下面几个平台搜索同一个域名，比较首年与续费价格，再决定在哪里买。

- [Name.com](https://www.name.com/)：提供域名搜索、注册和管理，可以作为老牌注册商的备选。购买时查看所选后缀的续费价格及隐私保护条件。
- [GoDaddy](https://www.godaddy.com/domains)：另一个老牌域名注册平台。比较优惠时看清最低购买年限、续费金额和购物车中的附加服务，只选择自己需要的项目。
- [Namecheap](https://www.namecheap.com/)：可以用来比较域名注册和转入价格，尤其要区分首年促销与后续续费。
- [Spaceship](https://www.spaceship.com/)：也提供域名注册。将同一后缀的注册、续费和转入费用一起比较，避免仅按首年价格选择。
- [Dynadot](https://www.dynadot.com/)：另一个域名注册和管理选择。先确认想要的域名是否可注册，再核对年限和总价。

域名在哪家注册，不决定网站必须托管在哪里。选择时优先考虑长期费用、DNS 管理方式和自己是否用得顺手。

## 4. 完成注册

1. **创建自己的账号。** 使用能长期收信的邮箱，并开启双重验证。域名应放在你自己掌握的账号里。
2. **搜索完整域名。** Cloudflare 控制台使用 **Register domains**；Vercel 使用 Domains 搜索入口；其他平台使用域名搜索框。确认拼写、后缀及最终可注册状态。
3. **确认购买内容。** 核对年限、首年总额、续费价格和自动续费选项。只需要域名时，不必额外购买建站、邮箱或主机套餐。
4. **填写联系信息并付款。** 使用准确的注册人资料；按平台及后缀要求完成邮箱或身份验证。隐私保护是对外隐藏部分资料，不是免填真实信息。
5. **确认域名已进入账号。** 查看注册成功状态和到期日，保存订单，确保续费提醒能够送达。

如果让 Agent 帮你筛选，可以这样说：“帮我比较这几个域名在 Cloudflare、Vercel 和其他注册商的首年与续费费用，列出三年成本、DNS 限制和隐私保护条件。”购买前再核对最终结算金额。

## 5. 把域名连接到个人网站

先在托管平台添加域名，再到实际管理 DNS 的平台设置记录。注册商和 DNS 服务商可以不同：修改记录的位置由当前 nameservers 决定。下面的 `example.com`、`username` 和项目名都要换成自己的值。

### 连接 GitHub Pages

可以从 `www.example.com` 开始。先按 GitHub 的指引验证域名归属，再在仓库 **Settings → Pages → Custom domain** 中填写并保存。到 DNS 控制台添加 `www` 的 `CNAME` 记录，目标为 `username.github.io`，不含 `https://` 或仓库路径。等待验证和证书就绪后启用 **Enforce HTTPS**。若要同时使用根域名 `example.com`，按 [GitHub 自定义域名指南](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) 配置对应记录。

### 连接 Cloudflare Pages

打开 Pages 项目的 **Custom domains → Set up a domain**，填写域名后跟随指引。根域名 `example.com` 需要把 DNS 托管到 Cloudflare，并与 Pages 项目处于同一 Cloudflare 账号；注册商可以是其他公司。只连接 `www.example.com` 等子域名时，可以保留外部 DNS，再设置 `CNAME` 指向项目的 `pages.dev` 地址。必须先在 Pages 中添加域名，不能只改 DNS。参见 [Cloudflare Pages 自定义域名指南](https://developers.cloudflare.com/pages/configuration/custom-domains/)。

DNS 更新和 HTTPS 证书签发可能需要等待。切换 DNS 服务商时保留原有邮箱等记录，最后用完整的 `https://` 地址检查网站；绑定成功后再更新个人简介中的链接。

## 6. 保持这个地址属于你

打开自动续费，保持付款方式和联系邮箱有效，并另外设置到期提醒。域名是持续维护的地址，注册一次不等于永久拥有。

还没有网站，可以从[用 GitHub 创建个人网站](/zh/github-pages)或[用 Cloudflare 创建个人网站](/zh/cloudflare-pages)开始。先发布内容，再为它选择一个愿意长期使用的地址。
