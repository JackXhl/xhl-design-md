---
version: alpha
name: Flyinglife-Bianjie-Xiazai-design-analysis
description: 便捷下载（parse.flyinglife.cn）。中文消费级无水印解析落地页：slate 画布 + 居中 48/800 英雄（首行 indigo→violet 渐变字）+ 全薄荷信任胶囊 + 24px 大圆角解析卡。主 CTA 是 indigo-violet 渐变，不是单色绿。微信绿 #07c160 只做信任/页脚点缀。无整页 dark mode，页脚保持浅色。本文件是现网拆解，禁止把这些 token 写进柚见。
source: https://parse.flyinglife.cn/ (public CSS, measured)
measured: 2026-09-18
viewport-reference: 1440x900 desktop, 768px collapse

colors:
  primary: "#6366f1"
  primary-dark: "#4f46e5"
  secondary: "#8b5cf6"
  accent: "#07c160"
  canvas: "#f8fafc"
  card: "#ffffff"
  text: "#1e293b"
  muted: "#64748b"
  fine: "#94a3b8"
  line: "#e2e8f0"
  tab-track: "#f1f5f9"
  prompt-a: "#eff6ff"
  prompt-b: "#f5f3ff"
  prompt-bd: "#c7d2fe"
  amber: "#f59e0b"
  overlay: "rgba(0, 0, 0, 0.5)"
  preview-overlay: "rgba(0, 0, 0, 0.92)"
  phone-chrome: "#1a1a1a"
  phone-inset: "#2a2a2a"
  cta-shadow: "0 4px 12px rgba(99, 102, 241, 0.3)"
  cta-shadow-hover: "0 6px 20px rgba(99, 102, 241, 0.4)"
  focus-ring: "0 0 0 4px rgba(99, 102, 241, 0.1)"
  nav-bg: "rgba(255, 255, 255, 0.8)"
  badge-bg: "rgba(7, 193, 96, 0.08)"
  badge-bd: "rgba(7, 193, 96, 0.2)"
  commit-wash: "linear-gradient(135deg, rgba(7, 193, 96, 0.04), rgba(99, 102, 241, 0.04))"

typography:
  font-ui: "-apple-system, BlinkMacSystemFont, Segoe UI, PingFang SC, Hiragino Sans GB, Microsoft YaHei, sans-serif"
  display:
    fontSize: 48px
    fontWeight: 800
    lineHeight: 1.2
  display-mobile:
    fontSize: 28px
  lead: { fontSize: 18px, fontWeight: 400, color: "#64748b" }
  lead-mobile: { fontSize: 15px }
  brand: { fontSize: 20px, fontWeight: 700 }
  section: { fontSize: 28px, fontWeight: 700 }
  section-mobile: { fontSize: 22px }
  card-title: { fontSize: 18px, fontWeight: 700 }
  tutorial-title: { fontSize: 17px, fontWeight: 600 }
  platform-name: { fontSize: 15px, fontWeight: 600 }
  body: { fontSize: 16px, lineHeight: 1.6 }
  nav-btn: { fontSize: 14px, fontWeight: 500 }
  parse-cta: { fontSize: 16px, fontWeight: 500 }
  badge: { fontSize: 13px, fontWeight: 500 }
  caption: { fontSize: 13px, color: "#94a3b8" }
  stat: { fontSize: 36px, fontWeight: 700 }
  stat-suffix: { fontSize: 16px }

rounded:
  control: 8px
  field: 12px
  card: 16px
  parse-card: 24px
  modal: 24px
  badge: 100px
  logo: 10px
  icon-sq: 12px
  platform-icon: 14px
  phone: 24px

spacing:
  nav-h: 71px
  nav-pad: "16px 32px"
  main-pad: "60px 32px 80px"
  main-pad-m: "32px 16px 48px"
  hero-mb: 48px
  parse-mb: 64px
  parse-card-pad: 32px
  field-gap: 12px
  badge-gap: 10px
  section-gap: 24px
  icon: 56px

layout:
  nav-max: 1400px
  main-max: 1400px
  tutorial-max: 960px
  commit-grid-max: 900px
  modal-max: 440px
  contact-max: 360px
  platform-card-w: 160px

breakpoints:
  collapse: 768px

components:
  nav-bar:
    height: "~71px"
    background: "rgba(255,255,255,0.8)"
    blur: 12px
    borderBottom: "1px solid #e2e8f0"
    zIndex: 100
  button-nav-outline:
    padding: "10px 20px"
    rounded: 8px
    height: "~38px"
    border: "1.5px solid #6366f1"
  button-parse:
    padding: "16px 32px"
    rounded: 12px
    height: "~57px"
    fill: "linear-gradient(135deg, #6366f1, #8b5cf6)"
  field-parse:
    padding: "16px 20px"
    rounded: 12px
    border: "2px solid #e2e8f0"
    height: "~57px"
    background: "#f8fafc"
  parse-card:
    padding: 32px
    rounded: 24px
    shadow: "shadow-lg"
  badge-pill:
    padding: "6px 14px"
    rounded: 100px
  dialog:
    width: 440px
    padding: 40px
    rounded: 24px
    zIndex: 1000
---

# 便捷下载 · parse.flyinglife.cn

> 来源：[parse.flyinglife.cn](https://parse.flyinglife.cn/) 现网 CSS 实测（2026-09-18，1440×900），不是理想稿。
> **分类**：Video Downloaders & Parser Landings（中文消费级无水印解析落地页）。和柚见、SnapAny 同一产品类：营销英雄 + 贴链接工具。不是 Cobalt 那种空白工具壳，也不是 Linear / Vercel 开发者站。
> 对标仓库：[VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 九段结构。
> **禁止**：把本文件的 indigo / 48px 标题 / 24px 卡半径写进柚见。柚见锁的是绿 `#16a34a` + 72/800。

## 1. Visual Theme & Atmosphere

便捷下载是 **slate 画布上的消费级解析落地页**。第一屏是居中营销英雄：两行 48/800 标题（上一行 indigo→violet 渐变裁剪字，下一行 slate 墨），一句 18px 灰导语，四颗**同一薄荷色**信任胶囊，再落到一张 24px 大圆角白卡里的解析条。登录墙是一张蓝紫浅渐变 `prompt-card`，不是把输入框藏掉。

气质是「干净工具站 + 渐变 SaaS CTA」：无广告承诺用薄荷胶囊讲，真正可点的主按钮走 indigo-violet 斜向渐变。微信绿 `#07c160` 是**信任色**不是品牌主色。页脚保持浅底居中一行，不像柚见那样整段翻黑。

字体是系统栈（苹方 / Segoe / 微软雅黑），标题靠 800 字重和渐变裁剪，不靠自研 Display 字体。桌面 H1 **锁 48px**，不是 clamp 到 72。

**Key characteristics**
- 画布 `#f8fafc`，卡片白，居中轴
- H1 固定 **48px / 800 / 行高 1.2**；≤768 降到 28
- 首行 `.gradient-text`：`linear-gradient(135deg, #6366f1, #8b5cf6)` + `background-clip: text`
- 信任胶囊全薄荷 `#07c160`，不是彩虹四色
- 解析卡 24px 圆角 + Tailwind `shadow-lg` + 32 pad；输入与 CTA 横排，高约 57
- 主 CTA 渐变填充 + indigo 0.3 投影，字重 **500**（不是 700）
- 导航描边钮（indigo 1.5px），默认不是实心绿
- 中段：4 列信任数字 → 横向走马灯平台卡 → 3 步教程 → 3×2 卖点卡 → 手机框展示 → 承诺 3×2
- 页脚浅色居中，一句薄荷字距标语
- 无整页 dark mode

**Product class（分类，写入 Collection 时用这一档）**
| 是 | 不是 |
|---|---|
| 中文消费级无水印解析落地页 | Developer Tools & IDEs（Cursor / Linear） |
| 营销英雄 + 贴链接工具 | 空白工具壳（Cobalt） |
| Media-adjacent consumer utility | Fintech 紫渐变签名站（Stripe）——这里的紫是 CTA 填充，同时另有薄荷信任色 |
| 与柚见 / SnapAny 同类 | 柚见的视觉皮肤（绿 72/800 / 彩虹胶囊 / 近黑页脚） |

**Locked identity**
- 不要把 H1 做成柚见的 72，也不要去掉首行渐变字改成纯色
- 不要把四颗胶囊改成四套颜色；现网全是薄荷
- 不要把解析卡半径从 24 收到 8
- 不要把 CTA 改成单色绿或实心 indigo（现网是 135deg 双色渐变）
- 不要把页脚改成近黑五列（那是柚见）
- 不要发明整页 dark theme

## 2. Color Palette & Roles

### Brand / action
- **Indigo** `{colors.primary}` `#6366f1`：描边钮、焦点边、图标色、走马灯卡 hover 边
- **Indigo Dark** `{colors.primary-dark}` `#4f46e5`：token 里有，主路径少用
- **Violet** `{colors.secondary}` `#8b5cf6`：只与 indigo 组成 135deg 渐变（标题字、CTA、教程圆标）
- **Mint / WeChat green** `{colors.accent}` `#07c160`：信任胶囊、统计数字渐变一端、承诺卡 hover 边、页脚副句、footer 链 hover

### Surface
- **Canvas** `#f8fafc`：`body`、输入默认底
- **Card** `#ffffff`：解析卡、卖点卡、平台卡、弹层、信任条底
- **Tab track** `#f1f5f9`：登录 tab 槽、关闭钮 hover
- **Prompt wash** `#eff6ff` → `#f5f3ff`：未登录提示卡
- **Commit wash** mint 4% → indigo 4% 斜向：承诺整块底

### Text
- **Text** `#1e293b`：默认、H1 第二行、品牌字
- **Muted** `#64748b`：导语、说明、页脚正文
- **Fine** `#94a3b8`：解析 tip、页脚链、占位

### Line
- **Line** `#e2e8f0`：卡边、导航底边、输入默认边（输入是 **2px**）
- **Prompt border** `#c7d2fe`
- **Amber** `#f59e0b`：教程区小徽章（仅此一处暖色）

### Overlay / chrome
- 弹层遮罩 `rgba(0,0,0,0.5)` + blur 4
- 预览全屏 `rgba(0,0,0,0.92)`
- 手机框 `#1a1a1a`，inset 2px `#2a2a2a`

### Trust / gradient type
- 胶囊底 `rgba(7,193,96,0.08)` 边 `rgba(7,193,96,0.2)`
- 统计数字：`linear-gradient(135deg, #07c160, #6366f1)` + `background-clip: text`

## 3. Typography Rules

### Font
`-apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", sans-serif`

系统栈，无 Google Fonts，无 Inter 作为指定 UI 字体（系统回退里可能碰到 Segoe）。

### Hierarchy

| Role | Size | Weight | LH | Notes |
|---|---|---|---|---|
| Hero H1 | **48px** desktop / **28px** ≤768 | 800 | 1.2 | 居中，mb 16。不是 clamp |
| Hero line 1 | inherit | 800 | 1.2 | indigo→violet 渐变裁剪字 |
| Hero line 2 | inherit | 800 | 1.2 | `#1e293b` |
| Lead | 18 / 15 mobile | 400 | | `#64748b`，mb 8 |
| Brand | 20px | 700 | 32px logo 行 | 标 36×36 r10 |
| Section H2 | 28 / 22 mobile | 700 | | 平台 / 教程 / APP / 承诺 |
| Login H2 | 28 / 22 mobile | 700 | | 「欢迎回来」 |
| Prompt H3 | 20 | 700 | | 登录墙标题 |
| Feature H3 | 18 | 700 | | 卖点卡 |
| Tutorial H4 | 17 | 600 | | |
| Platform name | 15 / 14 mobile | 600 | 24 | |
| Body | 16 | 400 | 1.6 | |
| Nav / outline btn | 14 | 500 | 1 | pad 10×20 |
| Parse CTA | 16 / 15 mobile | **500** | 1 | 不是 700 |
| Badge | 13 / 12 mobile | 500 | 20.8 | |
| Parse tip | 13 | 400 | 20.8 | `#94a3b8` 居中 |
| Platform desc | 12 | 400 | 1.4 | `#64748b` |
| Stat num | 36 / 28 mobile | 700 | 1.2 | 渐变字；后缀 16 |
| Stat label | 14 | 400 | | mb 上 4 |
| Commit body | 13 | 400 | 1.6 | |
| Footer | 14 body / 13 sub | | | sub `#07c160` letter-spacing 1px |
| Form label | 14 | 500 | | mb 8 |
| Form input | 15 | 400 | | pad 12×16 |

### Principles
- 标题场靠 **48 + 800 + 渐变裁剪**，不要再加字距负值（现网 Display 无 tracking）
- CTA 字重 500，和柚见提取钮 700 不同
- 数字墙用双色渐变字，和标题渐变方向相同但色停是 mint→indigo

## 4. Component Stylings

### Navigation
- `position: sticky; top: 0; z-index: 100`
- 底 `rgba(255,255,255,0.8)` + `backdrop-filter: blur(12px)` + 底边 1px `#e2e8f0`
- 内宽 1400，pad **16×32**，flex space-between；实测栏高约 **71**
- Logo：36 方 r10 + 20/700 字，gap 10
- 右侧 gap 12：问题反馈 / APP下载 / VIP / 登录，均为 `.btn.btn-outline`
- Outline：透明底、字 `#6366f1`、**1.5px** 实线、r8、10×20、14/500、高约 38
- hover：底变 indigo、字变白
- active：`scale(0.98)`
- ≤768：汉堡 36 方 r8 描边显示；品牌字隐藏；钮 pad 8×12、13px、min-height 36

### Parse tool
- `.parse-card`：白、r24、pad 32、`shadow-lg`、1px line。桌面几乎拉满 1400 内容宽
- 输入行 flex，gap 12，mb 12
- 输入：flex 1，pad 16×20，**2px** `#e2e8f0`，r12，16px 字，底 `#f8fafc`，高约 57
- focus：边 indigo、底改白、`0 0 0 4px rgba(99,102,241,0.1)`
- `.parse-btn`：覆盖 pad 16×32、16px、**r12**（比通用 btn 的 r8 更大），渐变填充、白字、indigo 0.3 阴影
- hover：阴影 0.4 + `translateY(-1px)`
- disabled：opacity 0.6
- tip：居中 13 `#94a3b8`
- ≤768：输入列排；CTA 全宽 pad 14×24 / 15px；卡 pad 16

### Login wall (`.prompt-card`)
- 未登录时挡在解析卡下方：`linear-gradient(135deg, #eff6ff, #f5f3ff)`，边 `#c7d2fe`，r16，pad 40，居中
- H3 20、说明 muted、再放一颗渐变主钮「立即登录」
- 这是产品门，不是空状态插画

### Badges
- flex 居中 wrap，gap **10**（≤768 gap 6）
- pad 6×14，r100，13/500，全薄荷皮肤 + 前置勾
- 文案现网：无广告 / 无后台 / 无推送 / 稳定运营 7 年

### Trust strip
- 白卡 r16 pad 32×24，4 列 gap 16，mb 48
- 数字 36/700 渐变字（mint→indigo），标签 14 muted
- ≤768：2 列，数字 28

### Platform marquee
- 段标题 28 居中，说明 16 muted mb 32
- 卡宽 **160**，pad 20×16，r16，白底描边
- 图标底 56 方 r14；hover 上移 4px + 边变 indigo + `0 12px 40px / 0.1`
- 轨道 flex gap 20，`marqueeScroll` 40s 线性无限，hover 暂停
- 左右 100px fade 接到画布色
- ≤768：卡宽 140

### Tutorial
- 顶上 amber 小胶囊（4×14，r999，底 amber 10%，字 `#f59e0b`）+ H3 28
- 三列 max 960 gap 24
- 卡 r16 pad 28×24；圆标 56，填充 indigo→violet 渐变
- hover：`0 12px 32px / 0.08` + 上移 4px
- ≤768：1 列

### Feature / commit cards
- 卖点：3 列 gap 24；卡 pad 32 r16 描边居中；图标 56 r12，底 indigo/violet 10% 斜向
- hover：上移 4px + shadow-lg + 边变透明
- 承诺块：整段 r24 pad 56×40 + mint/indigo 4% 洗底；内 3 列 max 900；子卡 pad 28×20 r12
- 承诺 hover：**边变 mint**（不是 indigo）+ 上移 2px
- ≤768：卖点 1 列；承诺 1 列 pad 32×20

### App showcase
- 4 列手机框，max-width 220，aspect 9/19，chrome `#1a1a1a` r24 pad 8
- hover 上移 8px + 更重投影
- 这是页面里几乎唯一的深色物体

### Buttons
| Kind | Fill | Radius | Pad / H | Weight |
|---|---|---|---|---|
| Nav outline | transparent + 1.5px indigo | 8 | 10×20 ~38h | 500 |
| Parse CTA | 135deg indigo→violet | **12** | 16×32 ~57h | 500 |
| Generic primary | 同上渐变 | 8 | 10×20 | 500 |
| Prompt 立即登录 | 渐变 primary | 8 | 10×20 | 500 |
| Tab | 透明；active 白 + shadow-sm | 8 | 10 | 500 |
| Modal close | 透明圆 36 | 50% | | muted |

### Inputs
- 解析：16px 字、2px 边、r12、底 canvas
- 弹层：15px、1.5px 边、r8、pad 12×16（iOS 可能缩放，现网如此）

### Dialog
- z-index **1000**，遮罩黑 50% + blur 4
- 内容 max 440，宽 90%，**r24**，shadow-xl，`modalIn` 0.3s
- `.login-modal` pad 40；header 居中 mb 32
- tabs：底 `#f1f5f9` pad 4 r12 gap 8 mb 28
- 关闭 36 圆，右上 16
- 联系作者 max 360 pad 40×32
- 媒体预览 z 3000、底 92% 黑
- ≤768：login pad 24×20，宽 95%

### Footer
- 居中，pad 40×20×60，顶边 1px line，mt 40
- 链 flex wrap gap 12，`#94a3b8`，hover mint
- 副句 mint 13px letter-spacing 1px
- **浅色页脚**，不要画成柚见的 `#020617`

## 5. Layout Principles

### Spacing（现网，不是严格 8 刻度）
常用：4, 6, 8, 10, 12, 14, 16, 20, 24, 28, 32, 40, 48, 56, 60, 64, 80。
**10 / 38 / 57 / 71 都是实测，不要收成 8 的倍数。**

| Zone | Desktop | ≤768 |
|---|---|---|
| Nav | 16×32，高 ~71 | 10×12 |
| Main | 60×32×80，max 1400 | 32×16×48 |
| Hero mb | 48 | 32 |
| Parse mb | 64 | 40 |
| Parse card pad | 32 | 16 |
| Trust mb | 48 | |
| Section 纵向 | 教程 32×0×24；平台 16×0×32 | |
| Showcase / commit 上下 | 64 | |
| Card gap | 24 | 16 / 12 |

### Containers
| Surface | Max |
|---|---|
| Nav inner / main / marquee | 1400 |
| Tutorial grid | 960 |
| Commit inner grid | 900 |
| Login modal | 440 |
| Contact modal | 360 |
| Platform card | 160（固定宽，不是流体） |
| Phone frame | 220 |

柚见是 1280 / 1152 / 1024 多宽并存；这里更接近 **一条 1400 中线**，解析卡拉满内容宽。

### Alignment
- Hero、解析 tip、平台、教程、承诺、页脚：**居中**
- 解析输入行桌面左齐横排
- 弹层表单左齐，header 居中

### Whitespace
英雄到解析卡的距离靠 hero mb 48 + 解析卡自身，没有柚见那种「框要贴标题」的压缩。中段用 48–64 段垫拉开数字墙、走马灯、教程。疏密是「SaaS 落地页」而不是「工具贴顶」。

## 6. Depth & Elevation

| Level | Treatment | Use |
|---|---|---|
| 0 | slate 画布无影 | 页、英雄 |
| 1 | 1px line，无影 | 卖点卡默认、承诺子卡、平台卡默认 |
| 2 | `shadow-lg`（0 10px 15px / 0.1） | 解析卡默认；卖点 hover |
| 3 | `0 12px 40px / 0.1` 或 `0 12px 32px / 0.08` | 平台 / 教程 hover |
| 4 | `shadow-xl` | 弹层 |
| 5 | 手机框 `0 20px 50px / 0.15` | APP 演示 |
| Nav | 半透明白 + blur 12 | 顶栏 |
| Overlay | 黑 50% + blur 4 | 登录 |
| CTA | indigo 0.3 投影，hover 0.4 + 上移 1px | 主按钮 |
| Focus | indigo 4px 10% 晕 | 输入 |

z-index：marquee fade 10，nav 100，modal 1000，preview 3000。

## 7. Do's and Don'ts

### Do
- 画布用 `#f8fafc`，卡用白，主动作用 indigo→violet 135deg
- 薄荷只给信任：胶囊、数字渐变一端、承诺 hover、页脚副句
- H1 桌面 48/800，首行渐变裁剪，第二行实色
- 解析卡 r24 + shadow-lg；输入 2px 边 r12；CTA r12 字重 500
- 登录墙用蓝紫浅渐变 prompt-card
- 系统中文字体栈
- 页脚保持浅、居中、窄

### Don't
- 不要抄进柚见（绿 72、彩虹胶囊、8px 卡、近黑页脚）
- 不要把 CTA 改成单色、不要把字重加到 700 当「更稳」
- 不要把信任胶囊改成四色
- 不要上 Inter / Geist 当指定 UI 字体
- 不要做整页 dark，不要把页脚翻黑
- 不要把解析卡收成工具条贴在标题下（那是另一类：Cobalt / 柚见「框近」实验）
- 不要加 mesh 英雄、滚动提示、开发者等宽

## 8. Responsive Behavior

现网**几乎只认 768**。没有柚见那套 720 / 640 / 960 三档。

| Name | Width | 变化 |
|---|---|---|
| Desktop | ≥769 | 解析横排；信任 4 列；卖点 3 列；展示 4 列；承诺 3 列；汉堡隐藏 |
| Phone / tablet | ≤768 | H1 28、导语 15；解析竖排 CTA 全宽；main pad 32×16×48；信任 2 列；卖点/承诺 1 列；展示 2 列；汉堡显示；品牌文字隐藏 |

**触控**
- 解析 CTA 竖排后全宽，高度仍来自 14×24 pad，可用
- 导航描边钮桌面 ~38，合格边缘；移动 36 min-height
- 汉堡 36、关闭 36
- 弹层输入 15px，iOS 可能放大页面（现网如此）

**Motion**
- 走马灯 40s；hover 暂停
- 卡 hover 上移 2–4px（展示框 8px）
- 无 `prefers-reduced-motion` 规则（现网没有）。若复刻，应停 marquee、去 transform

## 9. Agent Prompt Guide

### Quick color reference
- Canvas `#f8fafc` · Card `#ffffff` · Text `#1e293b` · Muted `#64748b`
- Action `#6366f1` → `#8b5cf6` 135deg
- Trust mint `#07c160`
- Line `#e2e8f0` · Overlay `rgba(0,0,0,0.5)`

### Copy into a prompt
```
Use design-md/flyinglife/DESIGN.md. Chinese consumer video-parser landing.
Slate canvas #f8fafc. Centered hero: 48px/800 (28px on ≤768). First line indigo→violet
gradient clipped text, second line #1e293b. Four mint #07c160 pills, not rainbow.
Parse card radius 24, padding 32, shadow-lg. Input 2px #e2e8f0 radius 12 height ~57
on #f8fafc. CTA linear-gradient(135deg,#6366f1,#8b5cf6) radius 12 weight 500.
Nav outline indigo buttons, sticky white 80% blur 12. Footer stays light, centered.
No full-page dark mode. Do not use Youjian tokens (#16a34a, 72px hero, 8px cards).
```

### Example component prompts
- 「顶栏 sticky 71，白 80% blur 12，右侧一排 indigo 描边钮 10×20 r8。」
- 「解析白卡 r24 pad 32：输入 16×20 r12 2px 边 + 渐变 CTA 16×32 r12。」
- 「信任条 4 列白卡 r16，数字 36 用 mint→indigo 渐变字。」
- 「登录弹层 440 r24 pad 40，tab 槽 #f1f5f9 r12，遮罩黑 50% blur 4。」

### Iteration guide
1. 先画 slate 画布 + 48 渐变标题 + 薄荷胶囊 + 24r 解析卡
2. 主按钮只允许 indigo-violet 渐变；薄荷不进 CTA
3. 中段按 数字墙 → 走马灯 → 教程 → 卖点 → 手机框 → 承诺 的节奏，不要删段并成一屏工具
4. 移动端只折叠列数和 768 字号，不要另做一套颜色
5. 和柚见对照时只借「英雄 + 框」结构，色值和半径以本文件为准

### Related files
- Light catalog: `design-md/flyinglife/preview.html`
- Dark catalog (overlay / phone chrome only): `design-md/flyinglife/preview-dark.html`
- Sibling (own product, different skin): `design-md/youjian/DESIGN.md`
- Collection category: Video Downloaders & Parser Landings
