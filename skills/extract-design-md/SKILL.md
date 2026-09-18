---
name: extract-design-md
description: "从现网站点拆 DESIGN.md 并按 xhl-design-md / awesome-design-md 标准落盘。新增自有产品视觉规范、补 preview、写对标时使用。"
---

# 从现网提取 DESIGN.md

目标仓库：`D:/git-project/xhl-design-md`。格式对齐 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 九段 + YAML。

## 步骤

1. **量，不要想。** 读实际 CSS / 计算样式：颜色、字号、字重、行高、字距、半径、pad、gap、容器宽、z-index、断点。
2. **建目录** `design-md/<slug>/DESIGN.md`
3. **YAML 头**：`name`、`description`、`colors`、`typography`、`rounded`、`spacing`、`components`（能填尽填）
4. **九段正文**（英文小标题保持，内容可用中文）：
   1. Visual Theme & Atmosphere（含被否方向）
   2. Color Palette & Roles
   3. Typography Rules（表格）
   4. Component Stylings（含 hover/focus/disabled）
   5. Layout Principles
   6. Depth & Elevation
   7. Do's and Don'ts
   8. Responsive Behavior
   9. Agent Prompt Guide（可粘贴 prompt + quick colors）
5. **preview.html**：自包含，`:root` token，色板、字阶、按钮、卡、输入
6. **preview-dark.html**：只画站点真正存在的深色表面；没有整页 dark 就写明，不要发明一套皮肤
7. 更新根 `README.md` Collection
8. 需要结构灵感时在 `references/awesome-design-md.md` 加一行借/不借，**不要复制**第三方 DESIGN.md 全文

## 质量

- hex 必须能在源 CSS 里搜到
- 不要把「最佳实践」写进 token（例如硬改成 8px 刻度）
- 用户否过的改版写进 Locked identity
- 对标链接用 awesome-design-md 的 blob URL
