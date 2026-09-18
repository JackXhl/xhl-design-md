---
version: alpha
name: Daishu-Xiazai-design-analysis
description: 袋鼠下载（daishuxiazai.com）。中文消费级无水印解析落地页，结构和柚见极近（白底、彩虹胶囊、56px 粘贴条、8px 卡、近黑页脚），但品牌是蓝→indigo 渐变字 + indigo-600 CTA + blue-600 登录，H1 桌面 60/900 单行全墨，不是柚见的绿 72/800 两行。禁止把 indigo 写进柚见，也禁止把柚见绿写进本文件。
source: https://www.daishuxiazai.com/ (public Tailwind CSS, measured)
measured: 2026-09-18
viewport-reference: 1440x900 desktop; Tailwind sm 640 / md 768 / lg 1024 / xl 1280

colors:
  indigo: "#4f46e5"
  indigo-hover: "#4338ca"
  indigo-focus: "#6366f1"
  indigo-50: "#eef2ff"
  indigo-100: "#e0e7ff"
  indigo-200: "#c7d2fe"
  blue: "#2563eb"
  blue-50: "#eff6ff"
  canvas: "#ffffff"
  band: "#f8fafc"
  ink: "#020617"
  text: "#0f172a"
  nav: "#374151"
  muted: "#475569"
  fine: "#64748b"
  slate-400: "#94a3b8"
  line: "#e2e8f0"
  input-border: "#cbd5e1"
  footer-text: "#cbd5e1"
  footer-line: "#1e293b"
  badge-emerald-bg: "#ecfdf5"
  badge-emerald-fg: "#047857"
  badge-emerald-bd: "#a7f3d0"
  badge-blue-bg: "#eff6ff"
  badge-blue-fg: "#1d4ed8"
  badge-blue-bd: "#bfdbfe"
  badge-violet-bg: "#f5f3ff"
  badge-violet-fg: "#6d28d9"
  badge-violet-bd: "#ddd6fe"
  badge-orange-bg: "#fff7ed"
  badge-orange-fg: "#c2410c"
  badge-orange-bd: "#fed7aa"
  ico-rose-bg: "#fff1f2"
  ico-rose-ring: "#ffe4e6"
  ico-teal-bg: "#f0fdfa"
  ico-teal-ring: "#ccfbf1"
  chat-from: "#059669"
  chat-to: "#0d9488"
  cta-shadow: "0 1px 2px rgba(99, 102, 241, 0.2)"
  card-shadow: "0 1px 2px rgba(0, 0, 0, 0.05)"

typography:
  font-ui: "ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
  display:
    fontSize: "36px / 48px sm / 60px lg"
    fontWeight: 900
    lineHeight: 1.06
    letterSpacing: "-1.5px at 60"
  lead: { fontSize: "20px desktop / 18px base", fontWeight: 400, lineHeight: "28px measured" }
  brand: { fontSize: 20px, fontWeight: 900 }
  section: { fontSize: "30px sm / 24px base", fontWeight: 700, letterSpacing: "-0.75px" }
  card-title: { fontSize: 14px, fontWeight: 700 }
  why-title: { fontSize: 14px, fontWeight: 700 }
  body: { fontSize: 16px, lineHeight: 1.75 }
  nav: { fontSize: 14px, fontWeight: 400 }
  button-login: { fontSize: 14px, fontWeight: 500 }
  button-cta: { fontSize: 16px, fontWeight: 700 }
  badge: { fontSize: 14px, fontWeight: 600 }
  faq-summary: { fontSize: 14px, fontWeight: 700 }
  caption: { fontSize: 14px, color: "#64748b" }
  legal: { fontSize: 12px, color: "#94a3b8" }
  footer-label: { fontSize: 12px, fontWeight: 700, letterSpacing: "0.16em" }

rounded:
  control: 8px
  paste: 6px
  badge: 9999px
  logo: 8px
  chat: 9999px

spacing:
  nav-h: 64px
  hero-pad: "48px 32px 36px"
  parse-band-y: 24px
  section-y: 64px
  card-pad: 20px
  card-gap: 16px
  badge-gap: 10px
  field-h: 56px
  icon: 48px

layout:
  nav-max: 1280px
  hero-max: 1152px
  parse-max: 1024px
  section-inner: 1088px
  faq-max: 768px
  about-max: 832px
  footer-max: 1280px

breakpoints:
  sm: 640px
  md: 768px
  lg: 1024px
  xl: 1280px

components:
  nav-bar:
    height: 64px
    background: "rgba(255,255,255,0.95)"
    blur: "backdrop-blur-md"
    borderBottom: "1px solid #e2e8f0"
    zIndex: 50
  button-login:
    background: "#2563eb"
    padding: "8px 16px"
    rounded: 8px
    height: "~36px"
  button-cta:
    background: "#4f46e5"
    height: 56px
    padding: "0 28px"
    rounded: 8px
  field-parse:
    height: 56px
    padding: "0 112px 0 20px"
    rounded: 8px
    border: "1px solid #cbd5e1"
  badge-pill:
    padding: "8px 14px"
    rounded: 9999px
  step-card:
    padding: 20px
    rounded: 8px
  footer:
    background: "#020617"
    columns: 4
---

# 袋鼠下载 · daishuxiazai.com

> 来源：[www.daishuxiazai.com](https://www.daishuxiazai.com/) 现网 Tailwind 类名 + 计算样式实测（2026-09-18，1440×900），不是理想稿。
> **分类**：Video Downloaders & Parser Landings。和柚见、便捷下载、SnapAny 同一产品类。
> 对标仓库：[VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 九段结构。
> **和柚见**：版式几乎同族（白底、四色胶囊、56 粘贴条、8px 白卡、`#020617` 页脚）。差异在品牌色和标题场。**禁止互抄 hex。**

## 1. Visual Theme & Atmosphere

袋鼠下载是 **白底中文消费落地页 + 贴链接工具**。第一屏：一行 60/900 墨色标题，一句 20px 灰导语，四颗彩虹能力胶囊，再落到 1024 宽的 56px 解析条（输入内叠「粘贴」，右侧 indigo「获取」）。中段 slate 色带和白底交替：4 步卡 → 3×2 卖点卡 → 平台网格 → FAQ → 关于长文。页脚整段翻成 `#020617`。右下角有一颗 emerald→teal 客服圆钮。

气质和柚见同族，但品牌是 **蓝 / indigo 双色**：字标 `from-blue-600 to-indigo-600` 裁剪字，登录实心 `#2563eb`，解析 CTA 实心 `#4f46e5`。绿只出现在「100% 免费」胶囊、部分卖点图标、客服 FAB，**不是主按钮色**。

H1 是 **单行、全墨、font-black 900**，桌面 60px（`lg:text-6xl`），不是柚见的两行 72/800、也不是便捷下载的 48 渐变裁剪字。

字体是 Tailwind 默认 `ui-sans-serif` 系统栈（含 Segoe / Roboto 回退），没有指定苹方。

**Key characteristics**
- 白画布，居中轴，营销英雄在工具框之上
- H1：`text-4xl / sm:text-5xl / lg:text-6xl` → 36 / 48 / **60**，字重 **900**，行高 1.06，字距约 -1.5px，色 `#020617`
- 四色胶囊（emerald / blue / violet / orange）+ 前置 `✓`，gap 10，8×14 pad
- 解析条 56，容器 `max-w-5xl` 1024；桌面横排 gap 12；粘贴叠在输入右
- CTA indigo-600 16/700 pad 0 28 r8；登录 blue-600 14/500 8×16
- 卡：白底 1px `#e2e8f0` r8 pad 20 + shadow-sm
- 步骤 **4** 列（不是柚见的 3）；卖点 **3 列 × 2 行**，图标 48 方，六套浅色底
- 页脚近黑 4 列，列标题 12/700 大写字距 0.16em
- 客服 FAB 56 圆，emerald-600 → teal-600

**Product class**
| 是 | 不是 |
|---|---|
| 中文消费级无水印解析落地页 | Developer Tools（Linear / Cursor） |
| 营销英雄 + 贴链接 | 空白工具壳（Cobalt） |
| 柚见的近亲版式 | 柚见皮肤（绿 CTA、72/800 两行） |
| | 便捷下载皮肤（slate 画布、24r 卡、渐变 CTA、浅页脚） |

**Locked identity**
- 不要把 H1 做成柚见 72 两行绿+墨，也不要做成便捷下载 48 渐变字
- 不要删彩虹胶囊，不要收成单色薄荷
- 不要把「获取」改成绿或改成 135deg 紫渐变
- 不要把页脚改回浅色
- 不要把步骤从 4 卡收成 3，除非复刻的是柚见而不是本站

## 2. Color Palette & Roles

### Brand / action
- **Indigo** `{colors.indigo}` `#4f46e5`：解析 CTA「获取」、步骤数字
- **Indigo hover** `#4338ca`
- **Indigo focus** `#6366f1`：输入 focus 边
- **Indigo 50/100** `#eef2ff` / `#e0e7ff`：步骤数字底、focus ring、FAQ 开态洗底
- **Blue** `{colors.blue}` `#2563eb`：登录钮、导航 hover 字、字标渐变起点
- **Wordmark** `linear-gradient(to right, #2563eb, #4f46e5)` + `background-clip: text`

### Surface
- **Canvas** `#ffffff`：页、卡、FAQ、解析输入底
- **Band** `#f8fafc`：步骤 / 平台色带 + 上下 `#e2e8f0`
- **Ink** `#020617`：H1、H2、页脚底

### Text
- **Text** `#0f172a`：默认、FAQ 题
- **Nav** `#374151`（gray-700）
- **Muted** `#475569`：导语、卡说明、关于正文
- **Fine** `#64748b`：解析辅助行
- **Legal** `#94a3b8`：12px 协议行
- **Footer body** `#cbd5e1`

### Line / input
- **Line** `#e2e8f0`
- **Input border** `#cbd5e1`
- **Footer line** `#1e293b`（slate-800）

### Badge / icon（装饰，保留多色）
| Slot | bg | fg / ring |
|---|---|---|
| ✓ 100% 免费 | `#ecfdf5` | `#047857` / `#a7f3d0` |
| ✓ 无水印 | `#eff6ff` | `#1d4ed8` / `#bfdbfe` |
| ✓ 高清画质 | `#f5f3ff` | `#6d28d9` / `#ddd6fe` |
| ✓ 无需登录 | `#fff7ed` | `#c2410c` / `#fed7aa` |
| 步骤数字 | `#eef2ff` | `#4f46e5` + ring indigo-100 |
| 完全免费 ico | `#ecfdf5` | ring `#d1fae5` |
| 极速下载 ico | `#eff6ff` | ring `#dbeafe` |
| 隐私保护 ico | `#f5f3ff` | ring `#ede9fe` |
| 多平台 ico | `#fff7ed` | ring `#ffedd5` |
| 高清画质 ico | `#fff1f2` | ring `#ffe4e6` |
| 无需安装 ico | `#f0fdfa` | ring `#ccfbf1` |

### Chat FAB
- `linear-gradient(to bottom right, #059669, #0d9488)`，白图标，shadow-lg

绿在本站是 **信任/客服点缀**，不是 CTA。

## 3. Typography Rules

### Font
`ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`

现网没有锁苹方。复刻本站可以跟系统栈；**不要把这套栈写进柚见**（柚见锁苹方/雅黑）。

### Hierarchy

| Role | Size | Weight | LH | Tracking | Notes |
|---|---|---|---|---|---|
| Hero H1 | 36 / 48 sm / **60 lg** | **900** | 1.06 | -1.5px @60 | 单行居中，`#020617`，max 1024 |
| Lead | 18 base / **20** sm+ | 400 | ~28 | | `#475569`，max 768，mb 28 |
| Brand | 20 | 900 | 28 | | 蓝→indigo 裁剪字；标 32×32 r8 |
| Section H2 | 24 / **30** sm | 700 | 36 | -0.75px | 居中；关于/教程左齐 |
| Section sub | 16 | 400 | 28 | | `#475569`，max 672，mb 40 |
| Card H3 | 14 | 700 | | | `#020617` 居中 |
| Body / about | 16 | 400 | 28 | | prose-slate |
| Nav | 14 | 400 | | | gray-700；hover blue-600 |
| Login | 14 | 500 | 20 | | |
| CTA 获取 | 16 | **700** | 24 | | |
| Badge | 14 | 600 | 20 | | |
| FAQ summary | 14 | 700 | | | |
| Support line | 14 | 400 | 20 | | `#64748b` |
| Legal | 12 | 400 | 20 | | `#94a3b8` |
| Footer label | 12 | 700 | 16 | 0.16em | 白、uppercase |
| Footer link | 14 | | | | slate-300 |

### Principles
- 标题场靠 **60 + 900 + 紧行高**，不靠颜色渐变字（渐变只给字标）
- CTA 700，登录 500，和柚见提取 700 / 登录 600 接近，但填充色不同
- 步骤数字 18/900 indigo，不是柚见的绿底绿字

## 4. Component Stylings

### Navigation
- `fixed` 顶栏，高 64，`bg-white/95` + `backdrop-blur-md` + 底边 `#e2e8f0`，z-50
- 内宽 `max-w-7xl` 1280，pad `lg:px-8` = 32
- 字标 20/900 蓝→indigo 裁剪；logo 图 32 r8
- 链：14 gray-700，pad 8×12 r8；hover 字 blue-600 底 blue-50/80
- 登录：blue-600 白字，8×16 r8，14/500，高约 36；`hidden sm:inline-flex`（&lt;640 藏）
- 汉堡：`xl:hidden`（&lt;1280 显示），8 pad r8 gray-600，hover 蓝
- 下拉：项 14 gray-700，pad 10×16，hover 底 blue-50

### Parse tool
- 容器 `max-w-5xl` 1024，居中
- 桌面 `md:flex-row` gap 12：输入 flex-1 高 56 + CTA 高 56
- 输入：白底，1px `#cbd5e1`，r8，16px 字，`#0f172a`，pad `0 112px 0 20px`，shadow-sm
- focus：边 `#6366f1` + `ring-4 ring-indigo-100`
- 粘贴：绝对右 12，6×12 pad，r6，底 `#f8fafc`，边 `#e2e8f0`，字 `#334155`，14/600，高约 34
- 获取：`#4f46e5`，pad 0 28，r8，16/700，阴影 indigo 0.2；hover `#4338ca`；disabled opacity 50
- ≤768：列排 gap 12，CTA 全宽
- 辅助行 14 `#64748b` 居中 mt 8；协议 12 `#94a3b8`

### Badges
- flex wrap 居中，gap **10**
- 8×14 pad，9999r，14/600，四套配色，文案带 `✓ `

### Cards
- **步骤**：`lg:grid-cols-4` gap 16，白卡 r8 pad 20 描边 shadow-sm；hover `-translate-y-0.5` + shadow-md
- 数字 48 方 r8，底 indigo-50 + ring indigo-100，字 18/900 indigo-600
- **卖点**：`md:grid-cols-3` gap 16，同样卡皮，无强制 hover 上移（现网 why 卡只有 shadow-sm）
- 图标 48 方 r8，六套浅色底
- **FAQ**：`max-w-3xl` 768；`details` r8 pad 16 描边；`open:` 边 indigo-200、底 indigo-50/30
- summary 14/700 slate-900

### Buttons
| Kind | Fill | Radius | Pad / H | Weight |
|---|---|---|---|---|
| Login | `#2563eb` | 8 | 8×16 ~36h | 500 |
| Parse CTA | `#4f46e5` | 8 | 56 / 0 28 | 700 |
| Paste | `#f8fafc` + line | 6 | 6×12 ~34h | 600 |
| Nav link | 透明 | 8 | 8×12 | 400 |
| Chat FAB | emerald→teal | 9999 | 56 | — |

### Inputs
- 解析 56 / 16px
- 现网首页未见独立登录弹层字段（登录走按钮，未在首屏展开）

### Footer
- `#020617`，正文 `#cbd5e1`
- 内宽 1280，pad 56×32
- 4 列 gap 40（lg）；sm 2 列；默认 1 列
- 列标题 12/700 白、uppercase、字距 0.16em
- 底栏顶边 `#1e293b`

### Chat
- 固定右下 56 圆，emerald→teal，shadow-lg，z 高于内容

## 5. Layout Principles

### Spacing（Tailwind，实测保留 10 / 36 / 56）
常用：2.5=10, 3=12, 3.5=14, 4=16, 5=20, 6=24, 7=28, 8=32, 10=40, 14=56, 16=64。

| Zone | Desktop | 折叠 |
|---|---|---|
| Nav | 64，px 32 | px 16 / 24 |
| Hero | pt 48 pb 36，max 1152 | 较小 pad |
| H1 → lead | mb 20 | |
| Lead → badges | mb 28 | |
| Parse band | py 24–24 | |
| Section | py 64 | py 56 @ default |
| Sub → grid | mb 40 | |
| Card gap / pad | 16 / 20 | |

### Containers
| Surface | Max |
|---|---|
| Nav / footer | 1280 |
| Hero block | 1152（外）/ H1 1024 |
| Parse | 1024 |
| Section grids | ~1088（1152-32×2） |
| FAQ | 768 |
| About prose | 832 |
| Lead | 768 |

### Alignment
- Hero、步骤、卖点、平台、FAQ 标题：**居中**
- 关于 / 如何使用：左齐
- 页脚：左齐 4 列

### Whitespace
英雄疏（48 顶垫 + 60 标题），解析条贴在英雄下（band 只有 24 竖垫）。中段 64 段垫。比便捷下载更「框近标题」，和柚见同一策略。

## 6. Depth & Elevation

| Level | Treatment | Use |
|---|---|---|
| 0 | 白底无影 | 页、关于 |
| 1 | 1px line + shadow-sm | 卡、FAQ、输入 |
| 2 | hover shadow-md + 上移 2px | 仅步骤卡 |
| Nav | 白 95% + blur | 顶栏 |
| CTA | indigo 0.2 细影 | 获取 |
| FAB | shadow-lg | 客服 |
| Focus | indigo-100 4px ring | 输入 |
| Tint band | `#f8fafc` + 上下 line | 步骤、平台 |
| Footer | 颜色翻转 | 底栏 |

z-index：nav 50，客服更高。不要加装饰 z。

## 7. Do's and Don'ts

### Do
- 白底 + 一行 60/900 墨标题 + 四色胶囊 + 56 解析条
- CTA 只用 indigo-600；登录只用 blue-600
- 字标保持蓝→indigo 裁剪
- 步骤 4 卡、卖点 6 卡多色图标
- 页脚近黑 4 列 + 大写细标签
- 绿只给免费胶囊 / 部分图标 / 客服钮

### Don't
- 不要把本站皮肤套到柚见（尤其 indigo CTA、60/900、蓝登录）
- 不要把柚见绿 `#16a34a` 或便捷下载 24r / 浅页脚抄过来
- 不要删彩虹胶囊或改成全薄荷
- 不要上 mesh 英雄、渐变大标题、开发者等宽
- 不要把「获取」做成描边钮或渐变胶囊

## 8. Responsive Behavior

Tailwind 四档，和柚见的 720/640/960 不同。

| Name | Width | 变化 |
|---|---|---|
| xl / desktop | ≥1280 | 汉堡隐藏；完整导航 |
| lg | ≥1024 | H1 60；步骤 4 列；平台 3 列；页脚 4 列 |
| md | ≥768 | 解析横排；卖点 3 列；平台 2 列 |
| sm | ≥640 | H1 48；lead 20；登录显示；步骤 2 列；页脚 2 列 |
| base | &lt;640 | H1 36；解析竖排 CTA 全宽；网格 1 列；登录隐藏、汉堡仍要到 xl 才隐藏——**&lt;1280 都有汉堡** |

**触控**
- 解析 56 合格；粘贴 34、登录 36 偏小
- 客服 FAB 56 合格
- 输入 16px，iOS 不缩放

## 9. Agent Prompt Guide

### Quick color reference
- Canvas `#ffffff` · Band `#f8fafc` · Ink `#020617` · Text `#0f172a`
- CTA indigo `#4f46e5` / hover `#4338ca` · Login blue `#2563eb`
- Line `#e2e8f0` · Input `#cbd5e1` · Footer `#020617`
- Wordmark gradient `#2563eb` → `#4f46e5`

### Copy into a prompt
```
Use design-md/daishu/DESIGN.md. White Chinese video-parser landing.
Hero: single-line 36/48/60 font-black 900, color #020617, no gradient title.
Keep four rainbow pills (emerald/blue/violet/orange) with ✓.
Parse: max-width 1024, input 56px radius 8, paste overlay, CTA #4f46e5 weight 700.
Login button #2563eb. Brand wordmark blue→indigo clipped text.
Cards: white, 1px #e2e8f0, radius 8, padding 20. Steps = 4 columns. Why = 3×2.
Footer #020617 four columns. Chat FAB emerald→teal circle 56.
Do not use Youjian green #16a34a or Flyinglife 24px cards / slate canvas.
```

### Example component prompts
- 「顶栏 fixed 64，白 95% blur，登录蓝钮 8×16 r8，链 hover 浅蓝底。」
- 「解析 1024：输入 56 + 右内粘贴 + indigo 获取 56。手机两行。」
- 「步骤四张等卡，48 indigo 数字方，hover 上移 2px。」
- 「FAQ 768，details r8，开态 indigo 浅底。」

### Iteration guide
1. 先画白底单行 60 标题 + 彩虹胶囊 + 56 框
2. 主按钮 indigo，登录蓝，绿不进 CTA
3. 中段按 4 步 → 6 卖点 → 平台 → FAQ → 长文 → 黑页脚
4. 对标柚见只借结构，色值和 60/900 以本文件为准

### Related files
- Light catalog: `design-md/daishu/preview.html`
- Dark catalog (footer / FAB only): `design-md/daishu/preview-dark.html`
- Sibling own product: `design-md/youjian/DESIGN.md`
- Sibling extracted: `design-md/flyinglife/DESIGN.md`
- Collection: Video Downloaders & Parser Landings
