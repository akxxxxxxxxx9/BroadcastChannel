# BroadcastChannel

**Turn your Telegram Channel into a MicroBlog.**

---

English | [简体中文](./README.zh-cn.md)

## ✨ Features

- **Turn your Telegram Channel into a MicroBlog**
- **SEO friendly** `/sitemap.xml`
- **0 JS on the browser side**
- **RSS and RSS JSON** `/rss.xml` `/rss.json`

## 🪧 Demo

### Real users

- [面条实验室](https://memo.miantiao.me/)
- [Find Blog👁发现博客](https://broadcastchannel.pages.dev/)
- [Memos 广场 🎪](https://now.memobbs.app/)
- [APPDO 数字生活指南](https://mini.appdo.xyz/)
- [85.60×53.98卡粉订阅/提醒](https://tg.docofcard.com/)
- [新闻在花频道](https://tg.istore.app/)
- [ALL About RSS](https://blog.rss.tips/)
- [Charles Chin's Whisper](https://memo.eallion.com/)
- [PlayStation 新闻转发](https://playstationnews.pages.dev)
- [Yu's Life](https://daily.pseudoyu.com/)
- [Leslie 和朋友们](https://tg.imlg.co/)
- [OKHK 分享](https://tg.okhk.net/)
- [gledos 的微型博客](https://microblogging.gledos.science)
- [Steve Studio](https://tgc.surgeee.me/)
- [LiFePO4:沙雕吐槽](https://lifepo4.top)
- [Hotspot Hourly](https://hourly.top/)
- [大河马中文财经新闻分享](https://a.xiaomi318.com/)
- [\_My. Tricks 🎩 Collection](https://channel.mykeyvans.com)
- [小报童专栏精选](https://xiaobaotong.genaiprism.site/)
- [Fake news](https://fake-news.csgo.ovh/)
- [miyi23's Geekhub资源分享](https://gh.miyi23.top/)
- [Magazine｜期刊杂志｜财新周刊](https://themagazine.top)
- [Remote Jobs & Cooperation](https://share-remote-jobs.vercel.app/)
- [甬哥侃侃侃--频道发布](https://ygkkktg.pages.dev)
- [Fugoou.log](https://fugoou.xyz)
- [Bboysoul的博客](https://tg.bboy.app/)
- [MakerHunter](https://share.makerhunter.com/)
- [ChatGPT/AI新闻聚合](https://g4f.icu/)
- [Abner's memos](https://memos.abnerz6.top/)
- [Appinn Talk](https://talk.appinn.net/)
- [小报童优惠与排行榜](https://youhui.xiaobaoto.com/)

### Platform

1. [Cloudflare](https://broadcast-channel.pages.dev/)
2. [Netlify](https://broadcast-channel.netlify.app/)
3. [Vercel](https://broadcast-channel.vercel.app/)

BroadcastChannel supports deployment on serverless platforms like Cloudflare, Netlify, Vercel that support Node.js SSR, or on a VPS.
For detailed tutorials, see [Deploy your Astro site](https://docs.astro.build/en/guides/deploy/).

## 🧱 Tech Stack

- Framework: [Astro](https://astro.build/)
- CMS: [Telegram Channels](https://telegram.org/tour/channels)
- Template: [Sepia](https://github.com/Planetable/SiteTemplateSepia)

## 🏗️ Deployment

### Docker

1. `docker pull ghcr.io/ccbikai/broadcastchannel:main`
2. `docker run -d --name broadcastchannel -p 4321:4321 -e CHANNEL=miantiao_me ghcr.io/ccbikai/broadcastchannel:main`

### Serverless

1. [Fork](https://github.com/ccbikai/BroadcastChannel/fork) this project to your GitHub
2. Create a project on Cloudflare/Netlify/Vercel
3. Select the `BroadcastChannel` project and the `Astro` framework
4. Configure the environment variable `CHANNEL` with your channel name. This is the minimal configuration, for more configurations see the options below
5. Save and deploy
6. Bind a domain (optional).
7. Update code, refer to the official GitHub documentation [Syncing a fork branch from the web UI](https://docs.github.com/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork#syncing-a-fork-branch-from-the-web-ui).

## ⚒️ Configuration

```env
## Telegram 频道用户名，必须配置。 t.me/ 后面那串字符
CHANNEL=DiggooChannel

## 语言和时区设置，语言选项见[dayjs](https://github.com/iamkun/dayjs/tree/dev/src/locale)
LOCALE=zh-cn
TIMEZONE=Asia/Shanghai

## 社交媒体用户名
TELEGRAM=ccbikai
TWITTER=digoodigu
GITHUB=diggooltd

## 下面两个社交媒体需要为 URL
DISCORD=https://DISCORD.com
PODCASRT=https://PODCASRT.com

## 头部尾部代码注入，支持 HTML
FOOTER_INJECT=FOOTER_INJECT
HEADER_INJECT=HEADER_INJECT

## SEO 配置项，可不让搜索引擎索引内容
NO_FOLLOW=false
NO_INDEX=false

## Sentry 配置项，收集服务端报错
SENTRY_AUTH_TOKEN=SENTRY_AUTH_TOKEN
SENTRY_DSN=SENTRY_DSN
SENTRY_PROJECT=SENTRY_PROJECT

## Telegram 主机名称和静态资源代理，不建议修改
HOST=telegram.dog
STATIC_PROXY=

## 启用谷歌站内搜索
GOOGLE_SEARCH_SITE=channel.diggoo.xzy

## 启用标签页, 标签使用英文逗号分割
TAGS=标签A,标签B,标签C

## 展示评论
COMMENTS=true

## 链接页面中的超链接, 使用英文逗号和分号分割
LINKS=Title1,URL1;Title2,URL3;Title3,URL3;

## 侧边栏导航项, 使用英文逗号和分号分割
NAVS=Title1,URL1;Title2,URL3;Title3,URL3;

## 启用 RSS 美化
RSS_BEAUTIFY=true

```

## 🙋🏻 FAQs

1. Why is the content empty after deployment?
   - Check if the channel is public, it must be public
   - The channel username is a string, not a number
   - Turn off the "Restricting Saving Content" setting in the channel
   - Redeploy after modifying environment variables
   - Telegram blocks public display of some sensitive channels, you can verify by visiting `https://t.me/s/channelusername`.

## ☕ Sponsor

1. [Follow me on Telegram](https://t.me/miantiao_me)
2. [Follow me on 𝕏](https://404.li/kai)
3. [Sponsor me on GitHub](https://github.com/sponsors/ccbikai)
