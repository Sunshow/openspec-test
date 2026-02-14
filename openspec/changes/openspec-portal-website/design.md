# Design: OpenSpec 门户网站

## Overview

创建一个纯静态的 OpenSpec 介绍门户网站，使用原生 HTML5 + CSS3 + Vanilla JavaScript 实现，无任何框架或构建工具依赖。网站采用单页面设计（Single Page），通过锚点导航在不同区块间跳转。

## Technical Approach

### 1. 项目结构

```
site/
├── index.html          # 主页面（单页应用）
├── css/
│   └── style.css       # 全局样式（含响应式）
├── js/
│   └── main.js         # 交互逻辑（平滑滚动、动画）
└── assets/
    └── favicon.svg      # 网站图标
```

### 2. HTML 结构（index.html）

采用语义化 HTML5 标签：

```html
<body>
  <nav>        — 顶部导航栏（锚点链接）
  <header>     — Hero 区块
  <section#about>      — What is OpenSpec
  <section#concepts>   — 核心概念（卡片网格）
  <section#workflow>   — 工作流程（步骤可视化）
  <section#quickstart> — 快速上手（代码示例）
  <footer>     — 页脚
</body>
```

### 3. CSS 方案（css/style.css）

- 使用 CSS Custom Properties（变量）统一管理配色方案
- 使用 CSS Grid / Flexbox 实现响应式布局
- 移动端优先（Mobile First）的媒体查询策略
- 断点设计：
  - `< 768px`：移动端（单列布局）
  - `768px ~ 1024px`：平板（双列布局）
  - `> 1024px`：桌面端（多列布局）
- 使用 `scroll-behavior: smooth` 实现平滑滚动
- 工作流程区块使用 Flexbox + CSS 伪元素绘制箭头连接线

### 4. JavaScript 方案（js/main.js）

- 导航栏滚动时的 sticky 效果和背景变化
- 移动端汉堡菜单的展开/收起
- 可选：使用 Intersection Observer API 实现区块进入视口时的淡入动画
- 无任何第三方库依赖

### 5. 设计风格

- 配色：以深蓝/靛蓝为主色调，搭配白色背景和浅灰辅助色，体现专业技术感
- 字体：系统字体栈（`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`）
- 图标：使用 CSS/SVG 内联图标，不依赖图标库
- 代码块：深色背景 + 等宽字体，模拟终端风格

## Data Flow

```
用户浏览器
  │
  ├── GET /index.html
  │     └── 解析 HTML → 加载 CSS + JS
  │
  ├── CSS 渲染
  │     └── style.css → 布局、配色、响应式、动画
  │
  └── JS 交互
        ├── 导航栏 sticky 效果
        ├── 移动端菜单切换
        ├── 平滑滚动到锚点
        └── 区块进入动画（Intersection Observer）
```

无后端交互，所有内容均为静态渲染。

## File Changes

| Action  | File                  | Description                          |
|---------|-----------------------|--------------------------------------|
| Created | `site/index.html`     | 主页面，包含所有区块的 HTML 结构       |
| Created | `site/css/style.css`  | 全局样式，含响应式布局和动画           |
| Created | `site/js/main.js`     | 交互逻辑，导航、滚动、动画            |
| Created | `site/assets/favicon.svg` | 网站 SVG 图标                     |
