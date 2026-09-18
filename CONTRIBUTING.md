# Contributing

This repository is a curated collection of DESIGN.md files, in the same shape as [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md): nine Stitch sections, YAML front matter, `preview.html`, `preview-dark.html`, and a README Collection grouped by **product class**.

We accept:

1. **Own products** (example: 柚见下载)
2. **Extracted public sites** measured from live CSS (example: [便捷下载](https://parse.flyinglife.cn/))

We do **not** accept wholesale copies of someone else's DESIGN.md from awesome-design-md. Point to those files from `references/` instead.

## New site

1. **Classify first.** Pick or add a Collection heading in the same style as awesome-design-md (`### Video Downloaders & Parser Landings`, not “misc”). The heading is the product class, not “ours vs theirs”. Ownership goes in the one-line blurb (`Own product` / `Extracted from <url>`).
2. Measure the live page. Read computed CSS. Do not invent a nicer palette.
3. Create `design-md/<slug>/`
4. Fill YAML + all nine sections (see `design-md/youjian/DESIGN.md` or `design-md/flyinglife/DESIGN.md`)
5. Add self-contained `preview.html` and `preview-dark.html` (`:root` tokens). If the site has no page-level dark theme, say so — only catalog overlays / chrome that exist.
6. Add one Collection bullet in the README under the right `###` heading. Bump the count badge if you keep one.
7. Record rejected redesigns under section 1 Locked identity.

### Classification cheat sheet

| Live site looks like | Collection heading |
|---|---|
| 中文消费落地页 + 贴链接解析框（柚见 / 便捷下载 / SnapAny） | `### Video Downloaders & Parser Landings` |
| 几乎无标题的纯工具壳（Cobalt） | 先开 issue：可能是同一大类的子类，不要塞进柚见皮肤 |
| 开发者文档 / IDE / 部署 | 不要新造条目；链到 awesome-design-md 对应类 |
| 金融 / 设计工具 / 媒体品牌 | 同上，只指路 |

## Improve an existing file

Compare against the live site (or the owning frontend repo). Hex, type, radius, and spacing changes must update both previews.

Do not “correct” measured values onto an 8px grid, and do not mix 柚见 tokens into 便捷下载 or the reverse.

## Skills

Interactive rules live in `skills/`. The extract flow is `skills/extract-design-md`. Youjian UI work also has a Cursor skill in the video repo.
