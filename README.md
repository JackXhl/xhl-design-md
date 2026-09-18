# xhl-design-md

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![DESIGN.md Count](https://img.shields.io/badge/DESIGN.md%20count-3-10b981?style=classic)

Curated collection of [DESIGN.md](https://stitch.withgoogle.com/docs/design-md/overview/) files. Layout matches [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md): one folder per site, nine-section `DESIGN.md`, plus `preview.html` / `preview-dark.html`.

Copy a site's `DESIGN.md` into a project, tell an AI agent “build me a page that looks like this,” and keep the visual language consistent.

This repo holds **own products** and **extracted public landings** in the same Collection, grouped by product class — the same heading style as awesome-design-md (`### AI & LLM Platforms`, `### Fintech & Crypto`, …). We do **not** copy third-party DESIGN.md files from that repo; those stay as links under [references](references/awesome-design-md.md).

| File | Who reads it | What it defines |
|------|-------------|-----------------|
| `AGENTS.md` (in the product repo) | Coding agents | How to build the project |
| `DESIGN.md` (this repo) | Design agents | How the UI should look and feel |

## What is DESIGN.md?

[DESIGN.md](https://stitch.withgoogle.com/docs/design-md/overview/) is a plain-text design system introduced by Google Stitch. Agents read it to generate consistent UI. No Figma export required — markdown is what LLMs already parse well.

**This repo provides ready-to-use DESIGN.md files** measured from live CSS (own sites and public pages).

## Collection

分类对齐 awesome-design-md：按**产品类**分组，不按「自有 / 别人」分组。所有权写在条目的一句话里。

### Video Downloaders & Parser Landings

中文消费级无水印解析落地页：居中营销英雄 + 贴链接工具。和 SnapAny 同类。**不是** Cobalt 空白工具壳，也**不是** Linear / Cursor / Vercel 那种开发者站。

- [**柚见下载 C 端**](design-md/youjian/DESIGN.md) · [light](design-md/youjian/preview.html) · [dark](design-md/youjian/preview-dark.html) — Own product. White canvas, single green `#16a34a`, two-line clamp 32–72 / 800 hero, four rainbow pills, 56px paste field, 8px cards, near-black footer. Locked to the 2026-09-18 restored live site, not the rejected flatten.
- [**便捷下载**](design-md/flyinglife/DESIGN.md) · [light](design-md/flyinglife/preview.html) · [dark](design-md/flyinglife/preview-dark.html) — Extracted from [parse.flyinglife.cn](https://parse.flyinglife.cn/). Slate canvas `#f8fafc`, 48/800 hero with indigo→violet clipped title, mint trust pills `#07c160`, 24px parse card, gradient CTA. Same product class as 柚见, different skin — do not mix tokens.
- [**袋鼠下载**](design-md/daishu/DESIGN.md) · [light](design-md/daishu/preview.html) · [dark](design-md/daishu/preview-dark.html) — Extracted from [daishuxiazai.com](https://www.daishuxiazai.com/). Youjian’s layout cousin: white canvas, rainbow pills, 56px paste, 8px cards, `#020617` footer. Skin is blue→indigo wordmark, indigo-600「获取」, blue-600 login, H1 60/900 one line. Do not swap with 柚见 green or 便捷下载 24r cards.

同类活站、尚未拆条（只指路，没有本仓库 DESIGN.md）：

- [SnapAny](https://snapany.com/) — SEO parser landing, H1 ~48/700, field close to the title.
- [Cobalt](https://cobalt.tools/) — **不同子类**：页面即工具，几乎无营销英雄。可学优先级，不要当落地页皮肤。

### Productivity & SaaS · Fintech · Media（只指路）

完整品牌拆解以 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 为准。本仓库不收录别人的视觉版权文件。结构借鉴见 [references/awesome-design-md.md](references/awesome-design-md.md)。

视频下载网页优先看：

| awesome 条目 | 借 | 不借 |
|------|----|------|
| [Wise](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/wise/DESIGN.md) | 单强调色、重 Display、友好落地页 | 青柠 `#9fe870`、sage 画布、24px 当柚见默认圆角 |
| [Mintlify](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/mintlify/DESIGN.md) | 绿点缀 + 可读长文 | 文档三栏、黑胶囊主按钮 |
| [Spotify](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/spotify/DESIGN.md) | 绿只做功能色 | 近黑沉浸、全胶囊、英文大写钮 |
| [Webflow](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/webflow/DESIGN.md) | 营销站完成度 | 蓝强调、动效优先 |
| [Airbnb](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/airbnb/DESIGN.md) | 消费级圆角、胶囊标签 | 珊瑚红、大摄影 |
| [Stripe](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/stripe/DESIGN.md) | （便捷下载 CTA 已是紫渐变，勿再叠） | 签名紫当柚见皮肤 |
| [Linear](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/linear/DESIGN.md) / Vercel / Cursor | 不要当解析落地页气质 | 开发者黑白精密 |

## What's Inside Each DESIGN.md

Every file follows the [Stitch DESIGN.md format](https://stitch.withgoogle.com/docs/design-md/specification/) with the same nine sections as awesome-design-md:

| # | Section | What it captures |
|---|---------|-----------------|
| 1 | Visual Theme & Atmosphere | Mood, density, product class, locked identity |
| 2 | Color Palette & Roles | Semantic name + hex + functional role |
| 3 | Typography Rules | Font families, full hierarchy table |
| 4 | Component Stylings | Buttons, cards, inputs, navigation with states |
| 5 | Layout Principles | Spacing scale, grid, whitespace philosophy |
| 6 | Depth & Elevation | Shadow system, surface hierarchy |
| 7 | Do's and Don'ts | Design guardrails and anti-patterns |
| 8 | Responsive Behavior | Breakpoints, touch targets, collapsing strategy |
| 9 | Agent Prompt Guide | Quick color reference, ready-to-use prompts |

Each site includes:

| File | Purpose |
|------|---------|
| `DESIGN.md` | The design system (what agents read) |
| `preview.html` | Visual catalog: swatches, type, buttons, cards |
| `preview-dark.html` | Only dark surfaces that exist on the live site — do not invent a theme |

目录：`design-md/<slug>/DESIGN.md`

## Skills

- [`skills/youjian-video-downloader-web`](skills/youjian-video-downloader-web/SKILL.md) — 改柚见 C 端 UI 时强制读 `youjian/DESIGN.md`
- [`skills/extract-design-md`](skills/extract-design-md/SKILL.md) — 从现网拆新条目：先归类，再落盘

业务仓库 `video-tool-c-web/AGENTS.md` 指向本库。Cursor 侧技能在视频项目 `.cursor/skills/youjian-c-web-ui/`。

## How to Use

1. Open `design-md/<site>/DESIGN.md` (and glance at the matching preview)
2. Tell the agent to use that file. Do not run anti-slop passes that delete the locked hero.
3. Need structure ideas? Open links in `references/awesome-design-md.md`. Hex values still come from the site's own DESIGN.md.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

- **New site**: measure live CSS, pick the Collection heading (or add one in awesome style), land the three files, add one bullet
- **Improve existing files**: fix wrong hex, missing tokens, weak descriptions; sync previews

## License

MIT License — see [LICENSE](LICENSE).

This repository is a curated collection of design system documents. Own-product tokens come from our public CSS. Extracted files represent publicly visible CSS values from third-party sites. We do not claim ownership of any site's visual identity. These documents exist to help AI agents generate consistent UI. Do not paste a competitor's hex into 柚见.
