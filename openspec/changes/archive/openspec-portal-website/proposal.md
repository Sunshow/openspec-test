# Proposal: OpenSpec 介绍门户网站

## Motivation

OpenSpec 作为一套规范驱动开发（SDD）方法论，目前缺少一个面向公众的介绍页面。开发者和团队在了解 OpenSpec 时，没有一个直观、集中的入口来获取核心概念、工作流程和快速上手指南。

创建一个纯静态门户网站可以：
- 为 OpenSpec 提供一个专业的公开展示窗口
- 降低新用户的学习门槛，通过可视化方式呈现 SDD 工作流
- 无需后端服务，部署简单，可托管在 GitHub Pages / Netlify / Vercel 等静态托管平台

## What

创建一个纯静态（HTML + CSS + JS）的 OpenSpec 介绍门户网站，包含以下页面/区块：

1. **Hero 区块** — 品牌标语、核心价值主张、CTA 按钮
2. **What is OpenSpec 区块** — 简要介绍 OpenSpec 和 SDD 方法论
3. **核心概念区块** — 展示 Spec、Change、Proposal、Design、Tasks 等核心概念
4. **工作流程区块** — 可视化展示 OpenSpec 的 SDD 工作流（Proposal → Spec → Design → Tasks → Archive）
5. **快速上手区块** — 展示基本的 openspec init 和 change 创建流程
6. **页脚** — 版权信息、GitHub 链接

## Impact

- **新文件**: 静态网站文件（`index.html`、`css/style.css`、`js/main.js`、`assets/` 目录）
- **现有代码**: 不影响任何现有代码或 OpenSpec 基础设施
- **部署**: 可直接部署到任意静态托管平台，零依赖

## Non-goals

- 不引入任何构建工具（如 Webpack、Vite）或框架（如 React、Vue）
- 不实现后端 API 或动态数据加载
- 不包含用户认证或数据库
- 不实现多语言国际化（首版仅中文）
- 不实现 CMS 或内容管理功能
