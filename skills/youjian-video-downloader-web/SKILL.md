---
name: youjian-video-downloader-web
description: "柚见下载 C 端网页 UI。改 video-tool-c-web 的落地页、解析框、导航、弹层、页脚时必须使用。先读 xhl-design-md 里的 youjian DESIGN.md，禁止套 anti-slop 把 72/800 英雄、彩虹胶囊、三等分步骤卡拆掉。"
---

# 柚见 C 端网页 UI

改 `video-tool-c-web` 外观前，先读并遵守：

`D:/git-project/xhl-design-md/design-md/youjian/DESIGN.md`

预览：`design-md/youjian/preview.html`。对标只看 `references/awesome-design-md.md`，不要把 Wise / Spotify 的色值写进柚见。

## 硬锁（2026-09-18 改版已否，已还原）

- H1 保持 `clamp(32px, 5.8vw, 72px)` / **800** / 两行（绿 + 墨），居中
- 四色胶囊保留（绿蓝橙紫 + `✓`）
- 步骤三张等权白卡、卖点 2×2 白卡，48 图标
- 字体：PingFang SC / 微软雅黑。不要 Inter、Geist
- 品牌绿只有 `#16a34a` / hover `#15803d`
- 页脚保持 `#020617`

允许：登录高度提到 44、弹层 input 16px、`viewport-fit=cover` + safe-area。这些不算换皮。

## 现网尺子（不要「纠正」）

- 解析框桌面 56、手机 48
- 卡片 pad 20、gap 16、半径 8（走马灯卡 16、弹层 16、结果下载钮 999）
- 容器多宽并存：1280 nav/footer、1152 内容、1024 解析、768 FAQ、896 about
- 段垫 56，英雄顶垫 72。不要收成 8 的倍数刻度去重排

## 文案

面向操作：粘贴、提取、保存。不写技术栈、不写和小程序关系、不承诺无限次。

## 流程

1. 打开 DESIGN.md 第 4–5 节对一下要改的组件
2. 改 CSS 用已有 hex，不新增强调色
3. 桌面 1440 和 393 宽（iPhone 16）各看第一屏：标题、胶囊、输入框都在
4. 若和 DESIGN.md 冲突，停下来问，不要自行扁平化
