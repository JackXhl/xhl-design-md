---
name: extract-design-md
description: "从现网站点拆 DESIGN.md 并按 xhl-design-md / awesome-design-md 标准落盘。新增自有产品或公开落地页视觉规范、补 preview、写分类时使用。"
---

# 从现网提取 DESIGN.md

目标仓库：`D:/git-project/xhl-design-md`。格式对齐 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md)：产品类 Collection 标题、九段、YAML、两份 preview。

## 步骤

1. **先分类。** 对照根 README 的 `###` 标题（awesome 写法：`### Video Downloaders & Parser Landings`）。同一产品类才放同一节。所有权写进条目一句话（`Own product` / `Extracted from <url>`），不要用「自有 / 别人」当一级分类。新类名要像 awesome 那样按行业/产品分，不要叫 Miscellaneous。
2. **量，不要想。** 读实际 CSS / 计算样式：颜色、字号、字重、行高、字距、半径、pad、gap、容器宽、z-index、断点。
3. **建目录** `design-md/<slug>/`
4. **YAML 头**：`name`、`description`、`colors`、`typography`、`rounded`、`spacing`、`components`（能填尽填）。`description` 里写清分类和「不要和谁混 token」。
5. **九段正文**（英文小标题保持，内容可用中文）：
   1. Visual Theme & Atmosphere（产品类、气质、Locked identity）
   2. Color Palette & Roles
   3. Typography Rules（表格）
   4. Component Stylings（含 hover/focus/disabled）
   5. Layout Principles
   6. Depth & Elevation
   7. Do's and Don'ts
   8. Responsive Behavior
   9. Agent Prompt Guide（可粘贴 prompt + quick colors）
6. **preview.html**：自包含，`:root` token，色板、字阶、按钮、卡、输入
7. **preview-dark.html**：只画站点真正存在的深色表面；没有整页 dark 就写明，不要发明一套皮肤
8. 在根 `README.md` **对应 Collection 分类**下加一条，格式：`[**Name**](design-md/<slug>/DESIGN.md) · [light](...) · [dark](...) — 一句话`
9. 需要结构灵感时在 `references/awesome-design-md.md` 加一行借/不借，**不要复制**第三方 DESIGN.md 全文

## 分类速查

| 活站 | Collection |
|---|---|
| 中文消费落地页 + 贴链接解析（柚见、便捷下载、SnapAny） | `### Video Downloaders & Parser Landings` |
| 空白工具壳（Cobalt） | 先当子类说明，不要塞进柚见皮肤 |
| 开发者工具 / 金融 / 媒体品牌 | 不在本仓库拆全文，链到 awesome-design-md |

## 质量

- hex 必须能在源 CSS 里搜到
- 不要把「最佳实践」写进 token（例如硬改成 8px 刻度）
- 用户否过的改版写进 Locked identity
- 禁止把竞品 hex 写进柚见 CSS
- 对标链接用 awesome-design-md 的 blob URL
