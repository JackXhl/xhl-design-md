# Contributing

本仓库只收**我们自己产品**的 DESIGN.md，格式对齐 [awesome-design-md](https://github.com/VoltAgent/awesome-design-md)。

## 新增一个站点

1. 从现网量 token，不要凭记忆或「更好看」改写
2. 建 `design-md/<slug>/`
3. 写满九段 + YAML 头（见 `design-md/youjian/DESIGN.md`）
4. 补 `preview.html` 和 `preview-dark.html`（自包含，token 写在 `:root`）
5. 在根 README Collection 加一条
6. 若有被否改版，写进第 1 节 Locked identity

## 改已有文件

对照活站或对应前端仓库 CSS。改 hex / 字号 / 圆角必须同步 preview。

不要从 awesome-design-md 整文件搬品牌 DESIGN.md 进来。对标只写在 `references/`。

## Skill

改交互规则时同步 `skills/`，并视情况更新视频项目里的 `.cursor/skills/youjian-c-web-ui/SKILL.md`。
