# xhl-design-md

自己的 [DESIGN.md](https://stitch.withgoogle.com/docs/design-md/overview/) 收藏。格式对齐 [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)：每个站点一份九段 `DESIGN.md`，外加 `preview.html` / `preview-dark.html`。

复制某个站点的 `DESIGN.md` 到项目里，让 agent 按它画 UI，而不是每次从零猜。

| 文件 | 谁读 | 定义什么 |
|------|------|----------|
| `AGENTS.md`（业务仓库） | 编码 agent | 怎么做这个项目 |
| `DESIGN.md`（本仓库） | 设计 agent | 做成什么样 |

## Collection

### 自有产品

- [**柚见下载 C 端**](design-md/youjian/DESIGN.md) · [light](design-md/youjian/preview.html) · [dark](design-md/youjian/preview-dark.html) — 白底中文视频下载落地页。绿 `#16a34a`，72/800 居中英雄，四色胶囊，56px 粘贴框，8px 白卡片，近黑页脚。锁的是 2026-09-18 还原后的现网，不是被否的扁平版。

### 对标（不收录别人的视觉版权，只指路）

完整品牌拆解仍以 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 为准。本仓库只写「借什么 / 不借什么」，见 [references/awesome-design-md.md](references/awesome-design-md.md)。

视频下载网页优先看：

| 对标 | 借 | 不借 |
|------|----|------|
| [Wise](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/wise/DESIGN.md) | 单绿强调、重 Display、友好落地页 | 青柠 `#9fe870`、sage 画布、24px 大圆角、Inter |
| [Mintlify](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/mintlify/DESIGN.md) | 绿点缀 + 可读长文 | 文档三栏、黑胶囊主按钮 |
| [Spotify](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/spotify/DESIGN.md) | 绿只做功能色 | 近黑沉浸、全胶囊、英文大写钮 |
| [Webflow](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/webflow/DESIGN.md) | 营销站完成度 | 蓝强调、动效优先 |
| [Airbnb](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/airbnb/DESIGN.md) | 消费级圆角、胶囊标签 | 珊瑚红、大摄影 |
| SnapAny / Cobalt（活站，不在 awesome 里） | 框要近、输入即产品 | Cobalt 无标题空白；SnapAny 48/700 短标题 |

## What's inside each DESIGN.md

跟 awesome-design-md / [Stitch spec](https://stitch.withgoogle.com/docs/design-md/specification/) 相同的九段：

| # | Section | 写什么 |
|---|---------|--------|
| 1 | Visual Theme & Atmosphere | 气质、密度、被否过的方向 |
| 2 | Color Palette & Roles | 语义名 + hex + 用途 |
| 3 | Typography Rules | 字体、层级表 |
| 4 | Component Stylings | 按钮、卡、输入、导航、状态 |
| 5 | Layout Principles | 间距、容器、留白 |
| 6 | Depth & Elevation | 阴影、层级 |
| 7 | Do's and Don'ts | 护栏 |
| 8 | Responsive Behavior | 断点、触控、折叠 |
| 9 | Agent Prompt Guide | 可粘贴提示词 |

每个站点目录：

| 文件 | 作用 |
|------|------|
| `DESIGN.md` | agent 主输入 |
| `preview.html` | 浅色 token 图鉴 |
| `preview-dark.html` | 深色已上线表面（柚见 = 页脚/遮罩） |

## Skills

- [`skills/youjian-video-downloader-web`](skills/youjian-video-downloader-web/SKILL.md) — 改柚见 C 端 UI 时强制读 `youjian/DESIGN.md`
- [`skills/extract-design-md`](skills/extract-design-md/SKILL.md) — 从现网拆新条目，按本仓库标准落盘

业务仓库 `video-tool-c-web/AGENTS.md` 里有指向本库的短链。Cursor 侧技能在视频项目 `.cursor/skills/youjian-c-web-ui/`。

## How to use

1. 打开 `design-md/<site>/DESIGN.md`
2. 告诉 agent：按这份画，先看 preview，不要套 anti-slop 把胶囊和等权卡拆掉
3. 需要结构灵感时再读 `references/awesome-design-md.md` 里的链接，色值仍以自有 DESIGN.md 为准

## License

MIT。自有产品的 token 来自我们站点的公开 CSS。对标链接指向第三方仓库，不复制其视觉资产。
