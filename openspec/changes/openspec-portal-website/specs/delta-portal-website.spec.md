# Delta Specs: OpenSpec 门户网站

## ADDED: SPEC-101 — 网站入口文件

> Given 用户访问门户网站根路径
> When 浏览器加载 index.html
> Then 页面正常渲染，包含完整的 HTML 结构
> And 页面标题为 "OpenSpec — 规范驱动开发"
> And 页面引用 css/style.css 和 js/main.js

## ADDED: SPEC-102 — Hero 区块

> Given 页面已加载完成
> When 用户看到页面顶部的 Hero 区块
> Then 显示 OpenSpec 品牌名称和标语
> And 显示核心价值主张描述文字
> And 显示至少一个 CTA 按钮（如"快速上手"或"了解更多"）
> And Hero 区块具有视觉吸引力的背景样式

## ADDED: SPEC-103 — What is OpenSpec 区块

> Given 用户滚动到 "What is OpenSpec" 区块
> When 该区块进入视口
> Then 显示 OpenSpec 的简要介绍文字
> And 说明 SDD（Spec-Driven Development）方法论的核心理念
> And 内容清晰易读，排版合理

## ADDED: SPEC-104 — 核心概念区块

> Given 用户滚动到核心概念区块
> When 该区块进入视口
> Then 以卡片或图标列表形式展示以下概念：
>   - Spec（规范）
>   - Change（变更）
>   - Proposal（提案）
>   - Design（设计）
>   - Tasks（任务）
> And 每个概念包含名称、图标/标识和简短描述

## ADDED: SPEC-105 — 工作流程区块

> Given 用户滚动到工作流程区块
> When 该区块进入视口
> Then 以可视化方式展示 SDD 工作流步骤：
>   - Proposal → Delta Specs → Design → Tasks → Implementation → Archive
> And 每个步骤包含名称和简短说明
> And 步骤之间有箭头或连接线表示流程方向

## ADDED: SPEC-106 — 快速上手区块

> Given 用户滚动到快速上手区块
> When 该区块进入视口
> Then 显示 OpenSpec 的基本使用步骤
> And 包含代码示例（如目录结构、命令示例）
> And 代码示例使用等宽字体和语法高亮样式

## ADDED: SPEC-107 — 页脚

> Given 用户滚动到页面底部
> When 页脚区块可见
> Then 显示版权信息（包含当前年份）
> And 显示 GitHub 仓库链接
> And 页脚样式与整体设计一致

## ADDED: SPEC-108 — 响应式布局

> Given 用户使用不同设备访问网站
> When 视口宽度在 320px 到 1920px 之间变化
> Then 页面布局自适应调整
> And 在移动端（< 768px）核心概念卡片变为单列布局
> And 在移动端导航和内容保持可读性
> And 不出现水平滚动条

## ADDED: SPEC-109 — 平滑滚动与交互

> Given 用户点击导航链接或 CTA 按钮
> When 链接指向页面内锚点
> Then 页面平滑滚动到目标区块
> And 滚动动画流畅自然

## ADDED: SPEC-110 — 纯静态无依赖

> Given 网站部署到静态托管平台
> When 服务器仅提供静态文件服务
> Then 网站所有功能正常运行
> And 不依赖任何后端 API 或服务端渲染
> And 不依赖任何 npm 包或构建工具
> And 所有资源（CSS、JS、字体、图片）均为本地文件或 CDN 引用
