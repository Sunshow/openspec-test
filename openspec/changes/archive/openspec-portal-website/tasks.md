# Tasks: OpenSpec 门户网站

## 项目结构

- [x] 创建 `site/` 目录及子目录（`css/`、`js/`、`assets/`）

## HTML 页面（site/index.html）

- [x] 创建 HTML5 基础结构（doctype、head、meta、title）
- [x] 添加顶部导航栏（nav），包含锚点链接：关于、核心概念、工作流程、快速上手
- [x] 实现 Hero 区块（header）：品牌名称、标语、价值主张、CTA 按钮
- [x] 实现 "What is OpenSpec" 区块：SDD 方法论介绍文字
- [x] 实现核心概念区块：Spec、Change、Proposal、Design、Tasks 五张概念卡片
- [x] 实现工作流程区块：Proposal → Spec → Design → Tasks → Implementation → Archive 步骤可视化
- [x] 实现快速上手区块：目录结构示例 + 基本命令示例
- [x] 实现页脚：版权信息 + GitHub 链接

## 样式（site/css/style.css）

- [x] 定义 CSS 变量（配色方案、字体、间距）
- [x] 实现全局基础样式（reset、body、typography）
- [x] 实现导航栏样式（sticky、背景渐变）
- [x] 实现 Hero 区块样式（渐变背景、居中布局、CTA 按钮样式）
- [x] 实现 "What is OpenSpec" 区块样式
- [x] 实现核心概念卡片网格布局
- [x] 实现工作流程步骤可视化样式（Flexbox + 箭头连接线）
- [x] 实现快速上手区块代码块样式（深色背景、等宽字体）
- [x] 实现页脚样式
- [x] 添加响应式媒体查询（移动端 < 768px、平板 768-1024px）
- [x] 添加平滑滚动（scroll-behavior: smooth）

## 交互（site/js/main.js）

- [x] 实现导航栏滚动 sticky 效果和背景变化
- [x] 实现移动端汉堡菜单展开/收起
- [x] 实现 Intersection Observer 区块进入动画

## 资源文件

- [x] 创建 `site/assets/favicon.svg`（OpenSpec 图标）

## 验证

- [x] 在浏览器中验证所有区块正常渲染
- [x] 验证响应式布局在不同视口宽度下表现正确
- [x] 验证平滑滚动和导航锚点跳转功能
- [x] 验证纯静态部署可用性（无后端依赖）
