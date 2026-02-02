# Terminal UI Design System

[English](#english) | [中文](#中文)

---

<a name="english"></a>
## English

A complete terminal-style UI design system featuring macOS-style window decorations, monospace typography, and a warm color palette. Designed for developer tools, code marketplaces, technical documentation sites, and any interface that benefits from a command-line aesthetic.

### ✨ Features

- 🎨 **Complete Color System** - Warm terracotta primary color (#cc7a60), fluorescent green command prefix, full syntax highlighting palette
- 🌙 **Dark Mode Support** - Complete dark mode implementation with smooth theme switching, system preference detection, and localStorage persistence
- 🔤 **Monospace Typography** - Complete font system based on JetBrains Mono
- 📐 **Precise Spacing System** - Spacing scale based on 4px multiples
- 🪟 **macOS-style Components** - Terminal windows, command buttons, code blocks, skill cards with line numbers, category cards with color themes, and complete component library
- 🎭 **Rich Animations** - Smooth transitions and interactive feedback
- 📱 **Responsive Design** - Complete mobile, tablet, and desktop adaptation
- ♿ **Accessibility Support** - WCAG-compliant color contrast and focus indicators

### 🎨 Design System Overview

#### Color Scheme

**Primary Colors:**
- Primary: `#cc7a60` - Warm terracotta for main actions and emphasis
- Command Prefix: `#39ff14` - Fluorescent green, used only for `$` symbol
- Success: `#22c55e` - Green for success states and strings
- Blue: `#3b82f6` - For command keywords and code keywords

**Complete Color System:**
- Semantic colors (backgrounds, foregrounds, borders, status colors)
- Syntax highlighting colors (keywords, strings, numbers, comments)
- macOS window button colors (red/yellow/green)
- **Dark Mode Colors**: Lighter primary (#d99178), dark backgrounds (#0a0a0a, #111), light text (#ededed), adjusted syntax colors for better contrast

#### Typography

- **Primary Font**: JetBrains Mono (weights 400-800)
- **Font Sizes**: Complete scale from 0.75rem to 3.75rem
- **Line Heights**: Tight (1.25) and relaxed (1.625) modes

#### Component Library

- Terminal window components (with macOS-style dots)
- Navigation command buttons with theme toggle
- Code block displays with syntax highlighting
- Skill cards with line numbers, avatars, and star ratings
- Category cards with color themes (Cyan, Blue, Purple, Amber)
- Search boxes
- Pagination
- FAQ components
- Theme toggle button with sun/moon icons
- And more...

### 📦 Installation

#### Using pnpm

```bash
pnpm dlx skills add chyinan/terminal-ui-design-system
```

#### Manual Installation

1. Clone this repository:
```bash
git clone https://github.com/chyinan/terminal-ui-design-system.git
```

2. Copy the `terminal-ui-design-system` folder to your Cursor Skills directory:
```bash
# Windows
cp -r terminal-ui-design-system "C:\Users\YourUsername\.cursor\skills\"

# macOS/Linux
cp -r terminal-ui-design-system ~/.cursor/skills/
```

### 📚 Usage

#### Using in Cursor

When you need to create a terminal-style interface in Cursor, simply mention:

```
Use the terminal-ui-design-system design system to create a login page
```

Or:

```
Create a developer tool interface following the terminal-ui-design-system style
```

#### Direct CSS Variables Usage

Import the CSS variables file in your project:

```html
<link rel="stylesheet" href="path/to/references/complete-css-variables.css">
```

Then use CSS variables:

```css
.my-component {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: var(--spacing-md);
  color: var(--foreground);
  font-family: var(--default-mono-font-family);
}
```

#### Using Component Templates

Check `references/component-templates.html` for HTML templates of all components.

### 📖 Documentation

#### Core Documentation

- **[SKILL.md](./SKILL.md)** - Complete design system documentation with all design specifications, component descriptions, and usage guidelines

#### Reference Resources

- **[complete-css-variables.css](./references/complete-css-variables.css)** - Complete CSS variable definitions
- **[component-templates.html](./references/component-templates.html)** - HTML templates for all components
- **[design-tokens.json](./references/design-tokens.json)** - Design tokens in JSON format (for tool integration)

### 🎯 Design Principles

1. **Terminal Aesthetic** - Mimics macOS terminal windows with monospace fonts and command-line syntax
2. **Developer-First** - Uses syntax highlighting colors, code structures, and terminal metaphors
3. **Warm & Friendly** - Warm terracotta primary color creates a friendly, approachable feel
4. **High Contrast** - Clear visual hierarchy with distinct text colors and backgrounds
5. **Functional Beauty** - Every design element serves a purpose while maintaining visual appeal

### 🎨 Quick Start

#### Create a Terminal Window

```html
<div class="terminal-window">
  <div class="window-header">
    <div class="window-dots">
      <span class="dot red"></span>
      <span class="dot yellow"></span>
      <span class="dot green"></span>
    </div>
    <span class="window-title">app.ts</span>
    <span class="window-status">ready</span>
  </div>
  <div class="window-content">
    <p>Your content</p>
  </div>
</div>
```

#### Create a Command Button

```html
<button class="nav-cmd">
  <span class="cmd-prefix">$</span>
  <span class="cmd-keyword">npm</span>
  <span class="cmd-flag">install</span>
</button>
```

#### Display Code Block

```html
<div class="stats-code-block">
  <div class="code-line">
    <span class="keyword">const</span>
    <span class="variable-name">count</span>
    <span class="operator">=</span>
    <span class="number">42</span>
    <span class="operator">;</span>
  </div>
  <div class="code-comment">
    <span class="comment-symbol">// </span>This is a comment
  </div>
</div>
```

### 📐 Design Tokens

#### Colors (Light Mode)

```css
--primary: #cc7a60;           /* Primary color */
--cmd-prefix-color: #39ff14;   /* Command prefix */
--success: #22c55e;            /* Success color */
--foreground: #111827;         /* Foreground color */
--border: #8b929e;             /* Border color */
```

#### Colors (Dark Mode)

```css
--primary: #d99178;           /* Lighter primary for contrast */
--foreground: #ededed;         /* Light text */
--background: #0a0a0a;         /* Deep black */
--card: #111;                  /* Slightly lighter */
--border: #606068;             /* Lighter for visibility */
```

#### Spacing

```css
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 32px;
--spacing-2xl: 48px;
```

#### Font Sizes

```css
--text-xs: 0.75rem;    /* 12px */
--text-sm: 0.875rem;   /* 14px */
--text-base: 1rem;     /* 16px */
--text-lg: 1.125rem;   /* 18px */
--text-xl: 1.25rem;    /* 20px */
```

See [design-tokens.json](./references/design-tokens.json) for complete design tokens.

### 🌐 Browser Support

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest, requires `-webkit-` prefix for backdrop-filter)

### 📝 Responsive Design

- **Mobile** (< 640px): Single column layout, simplified navigation
- **Tablet** (640px - 1024px): Two column layout, medium fonts
- **Desktop** (1024px - 1200px): Three column layout, full navigation
- **Large Screen** (> 1200px): Four column layout, max content width 1400px

### 🎬 Animations

- Smooth transitions (0.15s - 0.3s)
- Cursor blink effect
- Border pulse animation
- Fade-in-up animation (card entrance)
- Theme switching with smooth color transitions
- Card hover effects with lift and shadow

### 🌙 Dark Mode

The design system includes a complete dark mode implementation:

- **Automatic Theme Detection** - Detects system preference on first load
- **Manual Toggle** - Theme toggle button with sun/moon icons
- **Persistent Preference** - Saves theme choice in localStorage
- **Smooth Transitions** - All color changes animate smoothly (0.2s)
- **Complete Coverage** - All components adapt to dark mode
- **Enhanced Contrast** - Optimized colors for dark backgrounds

**Dark Mode Colors:**
- Primary: `#d99178` (lighter for better contrast)
- Background: `#0a0a0a` (deep black)
- Card: `#111` (slightly lighter)
- Foreground: `#ededed` (light gray)
- Borders: `#606068` (lighter for visibility)

See [SKILL.md](./SKILL.md) for complete dark mode documentation.

### 🤝 Contributing

Issues and Pull Requests are welcome!

### 📄 License

MIT License

### 🙏 Acknowledgments

Design inspiration from [skillsmp.com](https://skillsmp.com)'s terminal-style interface design.

### 📞 Contact

For questions or suggestions:

- Open an [Issue](https://github.com/chyinan/terminal-ui-design-system/issues)
- Create a [Pull Request](https://github.com/chyinan/terminal-ui-design-system/pulls)

---

<a name="中文"></a>
## 中文

一个完整的终端风格 UI 设计系统，包含 macOS 风格的窗口装饰、等宽字体排版和温暖的配色方案。专为开发者工具、代码市场、技术文档网站等需要命令行美学的界面设计。

### ✨ 特性

- 🎨 **完整的配色系统** - 暖陶土色主色调 (#cc7a60)，荧光绿命令前缀，完整的语法高亮配色
- 🌙 **暗色模式支持** - 完整的暗色模式实现，支持平滑主题切换、系统偏好检测和本地存储持久化
- 🔤 **等宽字体系统** - 基于 JetBrains Mono 的完整字体规范
- 📐 **精确的间距系统** - 基于 4px 的间距倍数系统
- 🪟 **macOS 风格组件** - 终端窗口、命令按钮、代码块、带行号的技能卡片、多色主题分类卡片等完整组件库
- 🎭 **丰富的动画效果** - 平滑的过渡动画和交互反馈
- 📱 **响应式设计** - 完整的移动端、平板、桌面适配方案
- ♿ **无障碍支持** - 符合 WCAG 标准的颜色对比度和焦点指示

### 🎨 设计系统概览

#### 配色方案

**主色调：**
- 主色：`#cc7a60` - 温暖的陶土色，用于主要操作和强调
- 命令前缀：`#39ff14` - 荧光绿色，仅用于 `$` 符号
- 成功色：`#22c55e` - 绿色，用于成功状态和字符串
- 蓝色：`#3b82f6` - 用于命令关键字和代码关键字

**完整配色系统：**
- 语义颜色（背景、前景、边框、状态色）
- 语法高亮颜色（关键字、字符串、数字、注释）
- macOS 窗口按钮颜色（红/黄/绿）
- **暗色模式配色**：更亮的主色 (#d99178)，深色背景 (#0a0a0a, #111)，浅色文字 (#ededed)，优化的语法高亮颜色以提升对比度

#### 字体系统

- **主字体**：JetBrains Mono（400-800 字重）
- **字体大小**：从 0.75rem 到 3.75rem 的完整尺寸系统
- **行高**：紧密 (1.25) 和宽松 (1.625) 两种模式

#### 组件库

- 终端窗口组件（带 macOS 风格圆点）
- 导航命令按钮（带主题切换）
- 代码块显示（语法高亮）
- 技能卡片（带行号、头像、星标）
- 分类卡片（多色主题：青色、蓝色、紫色、琥珀色）
- 搜索框
- 分页器
- FAQ 组件
- 主题切换按钮（太阳/月亮图标）
- 等等...

### 📦 安装

#### 使用 pnpm

```bash
pnpm dlx skills add chyinan/terminal-ui-design-system
```

#### 手动安装

1. 克隆此仓库：
```bash
git clone https://github.com/chyinan/terminal-ui-design-system.git
```

2. 将 `terminal-ui-design-system` 文件夹复制到你的 Cursor Skills 目录：
```bash
# Windows
cp -r terminal-ui-design-system "C:\Users\你的用户名\.cursor\skills\"

# macOS/Linux
cp -r terminal-ui-design-system ~/.cursor/skills/
```

### 📚 使用方法

#### 在 Cursor 中使用

当你在 Cursor 中需要创建终端风格的界面时，只需提到：

```
使用 terminal-ui-design-system 设计系统创建一个登录页面
```

或者：

```
参考 terminal-ui-design-system 的风格创建一个开发者工具界面
```

#### 直接使用 CSS 变量

在你的项目中引入 CSS 变量文件：

```html
<link rel="stylesheet" href="path/to/references/complete-css-variables.css">
```

然后使用 CSS 变量：

```css
.my-component {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  padding: var(--spacing-md);
  color: var(--foreground);
  font-family: var(--default-mono-font-family);
}
```

#### 使用组件模板

查看 `references/component-templates.html` 获取所有组件的 HTML 模板。

### 📖 文档

#### 核心文档

- **[SKILL.md](./SKILL.md)** - 完整的设计系统文档，包含所有设计规范、组件说明和使用指南

#### 参考资源

- **[complete-css-variables.css](./references/complete-css-variables.css)** - 完整的 CSS 变量定义
- **[component-templates.html](./references/component-templates.html)** - 所有组件的 HTML 模板
- **[design-tokens.json](./references/design-tokens.json)** - 设计令牌 JSON 格式（用于工具集成）

### 🎯 设计原则

1. **终端美学** - 模仿 macOS 终端窗口，使用等宽字体和命令行语法
2. **开发者优先** - 使用语法高亮颜色、代码结构和终端隐喻
3. **温暖友好** - 暖陶土色主色调营造友好、不令人生畏的感觉
4. **高对比度** - 清晰的视觉层次，使用不同的文本颜色和背景
5. **功能美学** - 每个设计元素都有目的，同时保持视觉吸引力

### 🎨 快速开始

#### 创建一个终端窗口

```html
<div class="terminal-window">
  <div class="window-header">
    <div class="window-dots">
      <span class="dot red"></span>
      <span class="dot yellow"></span>
      <span class="dot green"></span>
    </div>
    <span class="window-title">app.ts</span>
    <span class="window-status">ready</span>
  </div>
  <div class="window-content">
    <p>你的内容</p>
  </div>
</div>
```

#### 创建一个命令按钮

```html
<button class="nav-cmd">
  <span class="cmd-prefix">$</span>
  <span class="cmd-keyword">npm</span>
  <span class="cmd-flag">install</span>
</button>
```

#### 显示代码块

```html
<div class="stats-code-block">
  <div class="code-line">
    <span class="keyword">const</span>
    <span class="variable-name">count</span>
    <span class="operator">=</span>
    <span class="number">42</span>
    <span class="operator">;</span>
  </div>
  <div class="code-comment">
    <span class="comment-symbol">// </span>这是注释
  </div>
</div>
```

### 📐 设计令牌

#### 颜色（亮色模式）

```css
--primary: #cc7a60;           /* 主色 */
--cmd-prefix-color: #39ff14;   /* 命令前缀 */
--success: #22c55e;            /* 成功色 */
--foreground: #111827;         /* 前景色 */
--border: #8b929e;             /* 边框色 */
```

#### 颜色（暗色模式）

```css
--primary: #d99178;           /* 更亮的主色以提升对比度 */
--foreground: #ededed;         /* 浅色文字 */
--background: #0a0a0a;         /* 深黑色 */
--card: #111;                  /* 稍亮 */
--border: #606068;             /* 更亮以提升可见性 */
```

#### 间距

```css
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 32px;
--spacing-2xl: 48px;
```

#### 字体大小

```css
--text-xs: 0.75rem;    /* 12px */
--text-sm: 0.875rem;   /* 14px */
--text-base: 1rem;     /* 16px */
--text-lg: 1.125rem;   /* 18px */
--text-xl: 1.25rem;    /* 20px */
```

完整的设计令牌请查看 [design-tokens.json](./references/design-tokens.json)。

### 🌐 浏览器支持

- ✅ Chrome/Edge (最新版本)
- ✅ Firefox (最新版本)
- ✅ Safari (最新版本，需要 `-webkit-` 前缀用于 backdrop-filter)

### 📝 响应式设计

- **移动端** (< 640px): 单列布局，简化导航
- **平板** (640px - 1024px): 两列布局，中等字体
- **桌面** (1024px - 1200px): 三列布局，完整导航
- **大屏** (> 1200px): 四列布局，最大内容宽度 1400px

### 🎬 动画效果

- 平滑的过渡动画 (0.15s - 0.3s)
- 光标闪烁效果
- 边框脉冲动画
- 淡入上移动画（卡片入场）
- 主题切换时的平滑颜色过渡
- 卡片悬停效果（上浮和阴影）

### 🌙 暗色模式

设计系统包含完整的暗色模式实现：

- **自动主题检测** - 首次加载时检测系统偏好
- **手动切换** - 带太阳/月亮图标的主题切换按钮
- **持久化偏好** - 在 localStorage 中保存主题选择
- **平滑过渡** - 所有颜色变化平滑动画 (0.2s)
- **完整覆盖** - 所有组件都适配暗色模式
- **增强对比度** - 针对暗色背景优化的颜色

**暗色模式配色：**
- 主色：`#d99178`（更亮以提升对比度）
- 背景：`#0a0a0a`（深黑色）
- 卡片：`#111`（稍亮）
- 前景：`#ededed`（浅灰色）
- 边框：`#606068`（更亮以提升可见性）

完整暗色模式文档请查看 [SKILL.md](./SKILL.md)。

### 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 📄 许可证

MIT License

### 🙏 致谢

设计灵感来源于 [skillsmp.com](https://skillsmp.com) 的终端风格界面设计。

### 📞 联系方式

如有问题或建议，请通过以下方式联系：

- 提交 [Issue](https://github.com/chyinan/terminal-ui-design-system/issues)
- 创建 [Pull Request](https://github.com/chyinan/terminal-ui-design-system/pulls)

---

**Made with ❤️ for developers who love terminal aesthetics**
