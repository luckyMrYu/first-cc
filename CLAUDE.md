# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库概况

这是一个纯静态 HTML 内容仓库,存放中文(`lang="zh-CN"`)的大模型调研/总结页面与使用指南。没有构建系统、包管理器、测试或 lint —— 每个 `.html` 文件都是完全自包含的单文件页面(内联 `<style>`,无 JavaScript,无外部依赖),直接在浏览器中打开即可预览。

- `coding-vision-models-2026.html` — 编程 + 图片理解大模型总结
- `video-generation-models-2026.html` — 视频生成大模型总结
- `claude-code-guide.html` — Claude Code 新手指南

## 页面模板约定

两个 `*-models-2026.html` 调研页共用同一套设计模板,新增同类页面时应复制该结构保持一致:

- `<style>` 顶部用 `:root` CSS 变量定义配色(`--bg`、`--card`、`--ink`、`--muted`、`--line`、`--accent`、`--ok`、`--warn`),GitHub 风格浅色系
- 布局骨架:`div.wrap`(max-width 1000px 居中)→ `header`(h1 + `.meta` 日期/说明)→ 若干 `div.card` 章节 → `footer`(来源链接)
- 章节用 `h2` 中文序号标题(一、二、三…);卡片内用表格对比模型,`.tag` 彩色胶囊标注厂商/类别,`.yes`/`.no` 标注支持情况,`.note` 黄色提示框
- `claude-code-guide.html` 是独立的另一套样式(紫色渐变风格),不遵循上述模板

## 其他约定

- 提交信息使用简体中文,直接提交到 `main` 分支
- `.claude/settings.local.json` 为本机个人配置,已被 `.gitignore` 排除,不要提交
- 调研页中的数据(价格、模型能力)是撰写时的快照,页脚注明来源;更新内容时应同步更新页面上的日期标注
