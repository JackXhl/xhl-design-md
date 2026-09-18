---
version: alpha
name: Youjian-C-Web-design-analysis
description: 柚见下载 C 端网页。白底消费级落地页，居中大标题 + 四色能力胶囊 + 56px 粘贴框是第一屏主角。品牌绿 #16a34a 只做主按钮和一句绿标题，卡片 8px 圆角白底描边，页脚整段翻成 #020617。中文系统黑体，不要换成 Inter。2026-09-18 曾把标题降到 48/600、删胶囊、拆等权卡，被判不如原版，已还原。本文件锁的是还原后的现网，不是那次改版。
source: video-tool-c-web (Vue 3 + Vite, /video-c/)
measured: 2026-09-18
viewport-reference: 1440x900 desktop, 393x852 iPhone 16

colors:
  green: "#16a34a"
  green-dark: "#15803d"
  green-soft: "#ecfdf3"
  green-ink: "#047857"
  green-ring: "#bbf7d0"
  ink: "#020617"
  text: "#0f172a"
  nav-link: "#334155"
  muted: "#475569"
  fine: "#64748b"
  platform: "#94a3b8"
  line: "#e2e8f0"
  input-border: "#cbd5e1"
  canvas: "#ffffff"
  band: "#f8fafc"
  paste-bg: "#f8fafc"
  danger: "#dc2626"
  badge-green-bg: "#ecfdf5"
  badge-green-fg: "#047857"
  badge-green-bd: "#a7f3d0"
  badge-blue-bg: "#eff6ff"
  badge-blue-fg: "#1d4ed8"
  badge-blue-bd: "#bfdbfe"
  badge-orange-bg: "#fff7ed"
  badge-orange-fg: "#c2410c"
  badge-orange-bd: "#fed7aa"
  badge-purple-bg: "#f5f3ff"
  badge-purple-fg: "#6d28d9"
  badge-purple-bd: "#ddd6fe"
  ico-a-bg: "#ecfdf5"
  ico-a-fg: "#059669"
  ico-b-bg: "#eff6ff"
  ico-b-fg: "#2563eb"
  ico-c-bg: "#f5f3ff"
  ico-c-fg: "#7c3aed"
  ico-d-bg: "#f0fdfa"
  ico-d-fg: "#0f766e"
  footer-text: "#cbd5e1"
  footer-mute: "#94a3b8"
  footer-bar: "#64748b"
  footer-line: "#1e293b"
  mask: "rgba(0, 0, 0, 0.45)"
  focus-ring: "rgba(22, 163, 74, 0.12)"
  cta-shadow: "0 1px 2px rgba(22, 163, 74, 0.25)"
  card-shadow: "0 1px 2px rgba(15, 23, 42, 0.04)"
  lift-shadow: "0 8px 20px rgba(15, 23, 42, 0.08)"
  nav-shadow: "0 10px 30px rgba(15, 23, 42, 0.08)"

typography:
  font-ui: "PingFang SC, Hiragino Sans GB, Microsoft YaHei, sans-serif"
  display:
    fontSize: "clamp(32px, 5.8vw, 72px)"
    fontWeight: 800
    lineHeight: 1.18
    letterSpacing: "-0.04em"
  h2:
    fontSize: "clamp(22px, 3vw, 30px)"
    fontWeight: 700
    letterSpacing: "-0.02em"
  legal-h1:
    fontSize: "clamp(28px, 4vw, 36px)"
    letterSpacing: "-0.03em"
  brand:
    fontSize: 20px
    fontWeight: 800
    letterSpacing: "-0.03em"
  lead:
    fontSize: "clamp(17px, 1.6vw, 20px)"
    fontWeight: 400
    lineHeight: 1.7
  body: { fontSize: 16px, lineHeight: 1.85 }
  card-title: { fontSize: 15px, fontWeight: 600 }
  card-body: { fontSize: 14px, lineHeight: 1.65 }
  nav: { fontSize: 14px, fontWeight: 500 }
  button-auth: { fontSize: 14px, fontWeight: 600 }
  button-cta: { fontSize: 16px, fontWeight: 700 }
  badge: { fontSize: 14px, fontWeight: 600 }
  faq-summary: { fontSize: 14px, fontWeight: 700 }
  caption: { fontSize: 14px, color: "#64748b" }
  platform-line: { fontSize: 12px, color: "#94a3b8" }
  step-num: { fontSize: 18px, fontWeight: 900 }

rounded:
  control: 8px
  paste-desktop: 6px
  dialog: 16px
  marquee-card: 16px
  cover: 12px
  thumb: 10px
  plan: 10px
  download-pill: 999px
  badge: 999px
  logo-dot: 50%
  field-mobile: 12px

spacing:
  nav-h: 64px
  hero-pad: "72px 24px 16px"
  hero-pad-m: "32px 16px 8px"
  band-y: 56px
  inner-gutter: 48px
  inner-gutter-m: 32px
  card-pad: 20px
  card-gap: 16px
  badge-gap: 10px
  field-h: 56px
  field-h-m: 48px
  icon: 48px

layout:
  nav-max: 1280px
  content-max: 1152px
  parse-max: 1024px
  faq-max: 768px
  about-max: 896px
  footer-max: 1280px
  dialog-max: 420px
  legal-max: 760px

breakpoints:
  nav-collapse: 720px
  parse-stack: 720px
  grid-2: 960px
  grid-1: 640px

components:
  nav-bar:
    height: 64px
    background: "rgba(255,255,255,0.95)"
    blur: 12px
    borderBottom: "1px solid #e2e8f0"
    zIndex: 20
  button-auth:
    background: "#16a34a"
    color: "#ffffff"
    padding: "8px 16px"
    rounded: 8px
    computedHeight: "~35px"
  button-cta:
    height: 56px
    background: "#16a34a"
    color: "#ffffff"
    padding: "0 28px"
    rounded: 8px
  field-parse:
    height: 56px
    padding: "0 92px 0 20px"
    rounded: 8px
    border: "1px solid #cbd5e1"
  badge-pill:
    padding: "8px 14px"
    rounded: 999px
  step-card:
    padding: 20px
    rounded: 8px
    border: "1px solid #e2e8f0"
    icon: 48px
  dialog:
    width: 420px
    padding: 20px
    rounded: 16px
    fieldHeight: 42px
    zIndex: 40
  footer:
    background: "#020617"
    columns: 5
---

# 柚见下载 · C 端网页

> 来源：`video-tool-c-web` 现网 CSS 实测，不是理想稿。2026-09-18 的扁平化改版已还原，本文件锁还原后的样子。
> 对标仓库：[VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 九段结构。绿色消费站可对照 Wise / Mintlify / Spotify，落地页结构可对照 Webflow / Airbnb，工具框可对照 Cobalt / SnapAny 的「框要近」，但视觉不要抄它们的字号和配色。

## 1. Visual Theme & Atmosphere

柚见 C 端是**白底中文消费落地页 + 贴链接工具**。第一屏不是应用壳，是营销英雄区：两行 72/800 标题（上一行绿、下一行墨），一句 17–20px 导语，四颗彩虹能力胶囊，再落到 56px 宽输入框。页面中段用等权白卡片讲步骤和卖点，平台用横向走马灯，FAQ 是描边折叠卡，页脚整段翻成近黑 `#020617`。

气质是「能下、好懂、有点热闹」，不是 Linear / Vercel 那种开发者克制，也不是 Cobalt 那种空白工具。绿 `#16a34a`（Tailwind green-600）是唯一品牌色，只出现在：一句英雄标题、主按钮、焦点环、步骤数字底、开通态。四色胶囊和四色图标是**能力装饰**，不是第二品牌色；改版时不许删，也不许收成单色。

字体只用中文系统黑体：PingFang SC / 冬青黑 / 微软雅黑。不要引入 Inter、Geist、Wise Sans。字重靠 800 标题和 700 按钮撑场，这是页面「好看」的来源。

**Key characteristics**
- 白画布，居中轴，营销英雄区在工具框之上
- Display `clamp(32px, 5.8vw, 72px)` / 800 / 字距 -0.04em / 行高 1.18
- 四色胶囊（绿蓝橙紫）+ 前置 `✓`
- 解析框 56×满宽（容器 1024），桌面输入与「一键提取」横排，「粘贴」叠在输入右侧
- 卡片：白底 + 1px `#e2e8f0` + 8px 圆角 + 20px 内边距 + 极淡投影
- 步骤三等分卡、卖点 2×2 卡，图标 48 方底，允许多色
- 页脚近黑五列，和上面浅色营销是刻意的两段
- 中文系统黑体，禁止换拉丁几何无衬线当 UI 字体

**Locked identity（改版否决记录）**
- 不要把 H1 降到 48/600，不要改成一行左对齐小标题
- 不要删彩虹胶囊
- 不要把三张步骤卡改成编号纯文本行
- 不要把 2×2 卖点卡改成无边框列表
- 不要把圆角统一成一套「更干净」的 8；走马灯卡 16、弹层 16、下载钮 999 都是现网
- 可接受的微调：登录钮加高到 44、弹层字段 16px 防 iOS 缩放、`safe-area`。这些不改变气质。

## 2. Color Palette & Roles

### Brand
- **Youjian Green** `{colors.green}` `#16a34a`：主按钮、焦点描边、英雄第一行
- **Green Dark** `{colors.green-dark}` `#15803d`：hover
- **Green Soft** `{colors.green-soft}` `#ecfdf3`：nav hover 底、步骤数字底、tab on
- **Green Ink** `{colors.green-ink}` `#047857`：额度文案、弹层文字链

### Surface
- **Canvas** `#ffffff`：页、卡、弹层
- **Band** `#f8fafc`：教程区 tint、粘贴钮底
- **Ink** `#020617`：页脚、H1 第二行、品牌字重色

### Text
- **Text** `#0f172a`：默认正文
- **Nav link** `#334155`：导航、粘贴钮字
- **Muted** `#475569`：导语、卡片说明、label
- **Fine** `#64748b`：辅助说明、法律更新
- **Platform** `#94a3b8`：12px 平台名单（对比度偏弱，现网如此，不要擅自加黑）

### Line / input
- **Line** `#e2e8f0`：卡边、导航底边
- **Input border** `#cbd5e1`：输入框默认边
- **Danger** `#dc2626`：解析错误

### Badge / icon (decorative, keep)
| Slot | bg | fg | border |
|---|---|---|---|
| 无水印 | `#ecfdf5` | `#047857` | `#a7f3d0` |
| 原画质 | `#eff6ff` | `#1d4ed8` | `#bfdbfe` |
| 整段也能贴 | `#fff7ed` | `#c2410c` | `#fed7aa` |
| 不用安装 | `#f5f3ff` | `#6d28d9` | `#ddd6fe` |
| ico-a 下载 | `#ecfdf5` | `#059669` | inset `#a7f3d0` |
| ico-b 图集 | `#eff6ff` | `#2563eb` | inset `#bfdbfe` |
| ico-c 文案 | `#f5f3ff` | `#7c3aed` | inset `#ddd6fe` |
| ico-d 网页 | `#f0fdfa` | `#0f766e` | inset `#99f6e4` |

### Footer
- bg `#020617`，正文 `#cbd5e1`，链 `#94a3b8` hover 白，底栏 `#64748b`，分割 `#1e293b`

### Overlay
- mask `rgba(0,0,0,0.45)`
- focus ring `0 0 0 4px rgba(22,163,74,0.12)`

## 3. Typography Rules

### Font
`"PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", sans-serif`

禁止 Google Fonts 外链，禁止 Inter 做默认 UI。

### Hierarchy

| Role | Size | Weight | LH | Tracking | Notes |
|---|---|---|---|---|---|
| Hero H1 | clamp(32px, 5.8vw, 72px) | 800 | 1.18 | -0.04em | 两行，max-width 18em，居中 |
| Hero line 1 | inherit | 800 | | | color `#16a34a` |
| Hero line 2 | inherit | 800 | | | color `#020617` |
| Lead | clamp(17px, 1.6vw, 20px) | 400 | 1.7 | | max-width 38em, `#475569` |
| Brand wordmark | 20px | 800 | 1 | -0.03em | 标 32×32 r8 |
| Section H2 | clamp(22px, 3vw, 30px) | ~700 | | -0.02em | 居中 |
| Legal H1 | clamp(28px, 4vw, 36px) | | | -0.03em | |
| Legal H2 | 18px | | | | margin 28 0 10 |
| Result title | 18px | | 1.4 | | |
| Card H3 | 15px | 600 | | | |
| Body / about | 16px | 400 | 1.85 | | |
| Nav / auth | 14px | 500 / 600 | | | |
| CTA parse | 16px | 700 | | | |
| Badge | 14px | 600 | | | `✓ ` prefix |
| FAQ summary | 14px | 700 | | | |
| Fine | 14px | 400 | 1.6 | | `#64748b` |
| Platform line | 12px | 400 | 1.7 | | `#94a3b8` |
| Step number | 18px | 900 | | | 48×48 方 |
| Footer | 14px / 13px bar | | 1.7 | | |
| Dialog label | 13px | | | | |
| Dialog input | 15px | | | | height 42 |

### Principles
- 标题靠 **字号 + 800**，不靠颜色渐变字
- 中文不需要再缩字距，但现网 Display 用了 -0.04em，保持
- 按钮字重：提取 700，登录 600，导航 500

## 4. Component Stylings

### Navigation
- 固定顶栏 64，`rgba(255,255,255,0.95)` + `backdrop-filter: blur(12px)` + 底边 `#e2e8f0`，z-index 20
- 内宽 `min(1280px, 100% - 48px)`，gap 16
- 链：8×12 pad，r8，`#334155` 14/500；hover 字 `#15803d` 底 `#ecfdf3`
- 登录：绿底白字，8×16，r8，14/600。**实测高度约 35px**（小于 44，是现网不是 bug 文档）
- 联系：hover / focus-within 出 16r 白面板 + `--yj-shadow`
- ≤720：出「菜单」钮，链收进右上绝对定位 12r 面板

### Parse tool（产品控件）
- 容器 `--yj-hero` 1024
- 桌面 grid：`1fr auto`，gap 12。输入 56h，pad `0 92px 0 20px`（右侧给粘贴），r8，边 `#cbd5e1`，16px 字，浅投影
- focus：边绿 + 4px 绿色晕
- 粘贴：叠在 field 右，margin-right 10，6r，6×12 pad，底 `#f8fafc`
- 一键提取：同高 56，pad 0 28，r8，16/700，绿阴影
- active：`scale(0.98)`；disabled opacity 0.55
- ≤720：输入一行 48h r12；下一行 粘贴 | 提取，gap 10

### Badges
- flex wrap 居中，gap **10**（不是 8）
- 8×14 pad，999r，14/600，四套配色，`::before` 为 `✓ `

### Cards
- **步骤卡**：三列，20 pad，8r，1px line，`0 1px 2px rgba(15,23,42,0.04)`；hover 上移 2px + `0 8px 20px ...0.08`
- 数字 48 方，底 `#ecfdf3`，字 `#15803d`，900/18，inset 1px `#bbf7d0`
- **卖点卡**：2×2，同样皮肤；图标 48 方，四色底，svg 24
- **FAQ 卡**：768 容器，16 pad，开态边 `#bbf7d0` 底 `#f0fdf4`
- **结果卡**：20 pad，封面 72 r12，下载钮 **999 胶囊** 8×14
- **走马灯卡**：min-width 220，16r（不是 8），16×18 pad，圆点 logo 44

### Buttons
| Kind | Fill | Radius | Pad / H | Weight |
|---|---|---|---|---|
| Auth 登录 | `#16a34a` | 8 | 8×16 (~35h) | 600 |
| Parse CTA | `#16a34a` | 8 / 12 mobile | 56 / 48 | 700 |
| Paste | `#f8fafc` + line | 6 / 12 m | 6×12 / 48h | 600 |
| Ghost | white + line | 8 | 10×16 | 400 |
| Download sm | green or ghost | **999** | 8×14 | 400 |
| Plan row | `#f8fafc` | 10 | 12×14 | 15px |
| Dialog CTA | green | 8 | 10×18 | 600 |

### Inputs
- 解析：56 / 16px（iOS 不缩放）
- 弹层：42h，15px，r8，边 `#cbd5e1`（15px 在 iOS 会触发缩放，若只做兼容可改 16，不要改皮肤）
- 验证码行 gap 8

### Dialog
- 宽 420，r16，pad 20，mask 居中 pad 16，z 40
- tab gap 6，8 高 pad，on 态 `#ecfdf5` / `#86efac`
- QR 登录 220，联系 240

### Footer
- `#020617`，pad 56 24 0
- 五列 `1.3fr 1fr 1fr 1fr 1fr`，gap 40，列宽 `min(1280px, 100%-24px)`
- 链块状，底 pad 10；底栏 20 上下，13px

## 5. Layout Principles

### Spacing（现网实测，不是 8px 严格刻度）
常用：4, 6, 8, 10, 12, 14, 16, 20, 24, 28, 32, 36, 40, 48, 56, 72。
**不要为了 8px 刻度去改 10 / 14 / 35 / 42。** 那正是上次改丑的原因。

| Zone | Desktop | ≤640 / ≤720 |
|---|---|---|
| Nav | 64 | 64 |
| Hero pad | 72 24 16 | 32 16 8 |
| H1 → lead | 20 | 20 |
| Lead → badges | 28 | 28 |
| Parse band | 8 24 28 | 8 16 24 |
| Section `.band` | 56 0 | 56 0 |
| H2 → sub | 12 | 12 |
| Sub → grid | 40 | 40 |
| Card gap / pad | 16 / 20 | 16 / 20 |

### Containers（多宽并存，现网如此）
| Surface | Max |
|---|---|
| Nav inner / footer | 1280 |
| Section inner | 1152 |
| Parse box | 1024 |
| About | 896 |
| FAQ | 768 |
| Legal | 760 |
| Dialog | 420 |

不要强行收成一个 1152。滚动时中线会微跳，这是现网节奏。

### Alignment
- Hero、步骤、卖点、FAQ 标题：**居中**
- About、结果、弹层表单：左齐
- 页脚：左齐多列

### Whitespace
英雄区疏（72 顶垫 + 大字），中段密（56 段垫 + 20 卡垫）。疏密倒挂是落地页感，不要「纠正」成工具站贴顶。

## 6. Depth & Elevation

| Level | Treatment | Use |
|---|---|---|
| 0 | 白底无影 | 页、about |
| 1 | 1px `#e2e8f0` + `0 1px 2px / 0.04` | 卡、FAQ、结果、走马灯 |
| 2 | hover `translateY(-2px)` + `0 8px 20px / 0.08` | 仅步骤卡 |
| 3 | `0 10px 30px / 0.08` | 下拉、移动菜单 |
| Nav | 半透明白 + blur 12 | 顶栏 |
| Overlay | 黑 45% | 弹层 |
| Input focus | 绿 4px 晕 | 解析框 |
| Tint band | `#f8fafc` + 上下 1px line | 教程 |

页脚用**颜色翻转**抬升，不用大阴影。

z-index：内容默认，nav 20，mask 40。不要再加 z-50 装饰。

## 7. Do's and Don'ts

### Do
- 保持两行 72/800 英雄和四色胶囊
- 品牌绿只做 CTA / 焦点 / 一行标题
- 步骤三卡、卖点四卡、走马灯、FAQ 卡，白底描边
- 中文系统黑体
- 解析框保持 56 桌面 / 48 手机，字号 ≥16 在解析框
- 用户文案短、动作向：粘贴、提取、保存。不写技术栈、不写和小程序的关系
- 新页先复用现网卡片和按钮，再开新形状

### Don't
- 不要再做「工具优先扁平化」（2026-09-18 已否）
- 不要把绿换成 Wise 青柠 `#9fe870` 或 Spotify `#1ed760`
- 不要上 AI 紫渐变、mesh、玻璃拟态当默认
- 不要 Inter / Geist 替换苹方
- 不要删多色图标改成全绿
- 不要把下载钮从胶囊改成方钮（结果区 999 是现网）
- 不要在英雄区加滚动提示、版本号、Trusted by
- 不要把页脚改回浅色

## 8. Responsive Behavior

| Name | Width | 变化 |
|---|---|---|
| Desktop | ≥961 | 步骤 3 列，卖点 2 列，页脚 5 列，解析横排 |
| Tablet | 721–960 | 步骤/卖点/页脚 2 列 |
| Nav / parse | ≤720 | 汉堡菜单；解析框分行；走马灯左右 32 |
| Phone | ≤640 | Hero 32 16 8；网格 1 列；inner 100%-32 |

**iPhone 16（393×852）**
- 现网 viewport **没有** `viewport-fit=cover`，灵动岛不会让出 safe-area
- H1 落到 32/800，解析约在 379px 附近（旧测），一屏能看到标题和框的上沿
- 触控：解析 48 合格；登录 ~35、弹层字段 42 偏小
- 输入 16px 的只有解析框；弹层 15px 可能被 iOS 放大页面
- 兼容增强允许：`viewport-fit=cover`、safe-area、登录 44、弹层 16px 字。不允许顺手改英雄结构和配色。

**Reduced motion**
- `prefers-reduced-motion: reduce` 时关掉 transition，走马灯停、改横向滚动

## 9. Agent Prompt Guide

### Quick color reference
- Canvas `#ffffff` · Ink `#020617` · Text `#0f172a` · Muted `#475569`
- Brand `#16a34a` / hover `#15803d` / soft `#ecfdf3`
- Line `#e2e8f0` · Danger `#dc2626`
- Footer `#020617`

### Copy into a prompt
```
Use design-md/youjian/DESIGN.md. White marketing landing for a Chinese video downloader.
Hero: two-line clamp 32-72 / weight 800 / tracking -0.04em, first line #16a34a, second #020617.
Keep four rainbow pills (green/blue/orange/purple) with ✓.
Parse input 56px desktop, 48px mobile, radius 8 desktop / 12 mobile, CTA #16a34a weight 700.
Cards: white, 1px #e2e8f0, radius 8, padding 20, icon 48.
Font: PingFang SC / Microsoft YaHei only. Footer #020617 five columns.
Do not flatten, do not drop the hero to 48/600, do not remove badges.
```

### Example component prompts
- 「导航 64 高，半透明白 blur 12，登录绿钮 8×16 r8 14/600，链 14/500 hover 浅绿底。」
- 「解析条：1024 容器，输入 56 + 右内粘贴 + 绿 CTA 56。手机两行 48 r12。」
- 「步骤三张等卡，48 绿数字方，hover 上移 2px。」
- 「弹层 420 r16，tab 三等分，字段 42，遮罩 45% 黑。」

### Iteration guide
1. 先画居中英雄（大字、胶囊、框），再画中段卡，最后翻页脚
2. 绿只给可点的主动作和一句标题
3. 新模块优先复制步骤卡皮肤，不要发明第三种圆角体系
4. 改移动端先改 pad 和列数，不动桌面字号上限 72
5. 对标 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 时只借结构（框近、单强调色、重 Display），不借它们的色值和字号

### Related files
- Light catalog: `design-md/youjian/preview.html`
- Dark catalog (footer / overlay tokens): `design-md/youjian/preview-dark.html`
- Benchmark map: `references/awesome-design-md.md`
- Agent skill: `skills/youjian-video-downloader-web/SKILL.md`
