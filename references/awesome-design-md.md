# awesome-design-md 对标

源：[VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)

本仓库 Collection 按产品类分组（和 awesome 的 `### Fintech & Crypto` 同一套写法）。柚见与便捷下载都属于 **Video Downloaders & Parser Landings**，但皮肤不同：柚见用 `design-md/youjian/DESIGN.md`，便捷下载用 `design-md/flyinglife/DESIGN.md`，禁止互抄 hex。

下面这些 awesome 条目适合**结构借鉴**。色值、字体、圆角一律以目标站点自己的 DESIGN.md 为准。

## 必读（视频下载网页）

| 条目 | 路径 | 借 | 不借 |
|------|------|----|------|
| Wise | [design-md/wise/DESIGN.md](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/wise/DESIGN.md) | 单强调绿、重 Display、卡片坐在浅底上 | `#9fe870`、sage `#e8ebe6`、24px 圆角、Wise Sans/Inter、hero 126px |
| Mintlify | [design-md/mintlify/DESIGN.md](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/mintlify/DESIGN.md) | 绿点缀、营销 + 长文切换 | 黑胶囊 CTA、文档三栏、天空渐变英雄 |
| Spotify | [design-md/spotify/DESIGN.md](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/spotify/DESIGN.md) | 绿是功能色不是装饰底 | `#121212` 沉浸、全 pill、英文大写钮 |
| Webflow | [design-md/webflow/DESIGN.md](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/webflow/DESIGN.md) | 营销站完成度、区块节奏 | 蓝强调、motion-first |
| Airbnb | [design-md/airbnb/DESIGN.md](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/airbnb/DESIGN.md) | 消费级圆角、标签胶囊 | 珊瑚、大图英雄 |
| Cal.com | [design-md/cal/DESIGN.md](https://github.com/VoltAgent/awesome-design-md/blob/main/design-md/cal/DESIGN.md) | 干净中性工具感 | 过素、开发者导向 |

## 明确不要当柚见皮肤

| 条目 | 原因 |
|------|------|
| Linear / Vercel / Cursor | 开发者黑白精密，和中文下载站气质反了 |
| Stripe | 紫渐变签名，踩 AI 紫雷 |
| Tesla / Apple | 摄影全屏，柚见没有素材体系 |
| Nintendo 2001 / Dell 1996 | 怀旧实验，不是产品方向 |

## 活站（仓库外或已拆）

- [便捷下载](https://parse.flyinglife.cn/)：**已拆** → `design-md/flyinglife/`。同类落地页，slate + indigo/violet 渐变 CTA + 薄荷信任胶囊。48/800，不是柚见 72。
- [SnapAny](https://snapany.com/)：SEO 落地页，H1 约 48/700，输入框顶边约 277px。可学「框近」，不要把柚见 H1 从 72/800 砍掉（已试过，不好看）。
- [Cobalt](https://cobalt.tools/)：页面即工具，几乎无营销。可学优先级，不要抄空白和等宽。

## 使用方式

Agent 改柚见时：

1. 先读 `design-md/youjian/DESIGN.md`
2. 需要对齐「完成度」时打开本表链接，只抄布局策略
3. 任何新 hex 必须能在柚见 YAML `colors:` 里找到，否则不许进 CSS
