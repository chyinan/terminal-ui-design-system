# Terminal UI Design System

一个完整的终端风格 UI 设计系统，包含 macOS 风格的窗口装饰、等宽字体排版和温暖的配色方案。专为开发者工具、代码市场、技术文档网站等需要命令行美学的界面设计。

## ✨ 特性

- 🎨 **完整的配色系统** - 暖陶土色主色调 (#cc7a60)，荧光绿命令前缀，完整的语法高亮配色
- 🔤 **等宽字体系统** - 基于 JetBrains Mono 的完整字体规范
- 📐 **精确的间距系统** - 基于 4px 的间距倍数系统
- 🪟 **macOS 风格组件** - 终端窗口、命令按钮、代码块等完整组件库
- 🎭 **丰富的动画效果** - 平滑的过渡动画和交互反馈
- 📱 **响应式设计** - 完整的移动端、平板、桌面适配方案
- ♿ **无障碍支持** - 符合 WCAG 标准的颜色对比度和焦点指示

## 🎨 设计系统概览

### 配色方案

**主色调：**
- 主色：`#cc7a60` - 温暖的陶土色，用于主要操作和强调
- 命令前缀：`#39ff14` - 荧光绿色，仅用于 `$` 符号
- 成功色：`#22c55e` - 绿色，用于成功状态和字符串
- 蓝色：`#3b82f6` - 用于命令关键字和代码关键字

**完整配色系统：**
- 语义颜色（背景、前景、边框、状态色）
- 语法高亮颜色（关键字、字符串、数字、注释）
- macOS 窗口按钮颜色（红/黄/绿）

### 字体系统

- **主字体**：JetBrains Mono（400-800 字重）
- **字体大小**：从 0.75rem 到 3.75rem 的完整尺寸系统
- **行高**：紧密 (1.25) 和宽松 (1.625) 两种模式

### 组件库

- 终端窗口组件（带 macOS 风格圆点）
- 导航命令按钮
- 代码块显示
- 技能/卡片组件
- 搜索框
- 分页器
- FAQ 组件
- 等等...

## 📦 安装

### 使用 pnpm

```bash
pnpm dlx skills add chyinan/terminal-ui-design-system
```

### 手动安装

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

## 📚 使用方法

### 在 Cursor 中使用

当你在 Cursor 中需要创建终端风格的界面时，只需提到：

```
使用 terminal-ui-design-system 设计系统创建一个登录页面
```

或者：

```
参考 terminal-ui-design-system 的风格创建一个开发者工具界面
```

### 直接使用 CSS 变量

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

### 使用组件模板

查看 `references/component-templates.html` 获取所有组件的 HTML 模板。

## 📖 文档

### 核心文档

- **[SKILL.md](./SKILL.md)** - 完整的设计系统文档，包含所有设计规范、组件说明和使用指南

### 参考资源

- **[complete-css-variables.css](./references/complete-css-variables.css)** - 完整的 CSS 变量定义
- **[component-templates.html](./references/component-templates.html)** - 所有组件的 HTML 模板
- **[design-tokens.json](./references/design-tokens.json)** - 设计令牌 JSON 格式（用于工具集成）

## 🎯 设计原则

1. **终端美学** - 模仿 macOS 终端窗口，使用等宽字体和命令行语法
2. **开发者优先** - 使用语法高亮颜色、代码结构和终端隐喻
3. **温暖友好** - 暖陶土色主色调营造友好、不令人生畏的感觉
4. **高对比度** - 清晰的视觉层次，使用不同的文本颜色和背景
5. **功能美学** - 每个设计元素都有目的，同时保持视觉吸引力

## 🎨 快速开始

### 创建一个终端窗口

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

### 创建一个命令按钮

```html
<button class="nav-cmd">
  <span class="cmd-prefix">$</span>
  <span class="cmd-keyword">npm</span>
  <span class="cmd-flag">install</span>
</button>
```

### 显示代码块

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

## 📐 设计令牌

### 颜色

```css
--primary: #cc7a60;           /* 主色 */
--cmd-prefix-color: #39ff14;   /* 命令前缀 */
--success: #22c55e;            /* 成功色 */
--foreground: #111827;         /* 前景色 */
--border: #8b929e;             /* 边框色 */
```

### 间距

```css
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 32px;
--spacing-2xl: 48px;
```

### 字体大小

```css
--text-xs: 0.75rem;    /* 12px */
--text-sm: 0.875rem;   /* 14px */
--text-base: 1rem;     /* 16px */
--text-lg: 1.125rem;   /* 18px */
--text-xl: 1.25rem;    /* 20px */
```

完整的设计令牌请查看 [design-tokens.json](./references/design-tokens.json)。

## 🌐 浏览器支持

- ✅ Chrome/Edge (最新版本)
- ✅ Firefox (最新版本)
- ✅ Safari (最新版本，需要 `-webkit-` 前缀用于 backdrop-filter)

## 📝 响应式设计

- **移动端** (< 640px): 单列布局，简化导航
- **平板** (640px - 1024px): 两列布局，中等字体
- **桌面** (1024px - 1200px): 三列布局，完整导航
- **大屏** (> 1200px): 四列布局，最大内容宽度 1400px

## 🎬 动画效果

- 平滑的过渡动画 (0.15s - 0.3s)
- 光标闪烁效果
- 边框脉冲动画
- 淡入上移动画（卡片入场）

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License

## 🙏 致谢

设计灵感来源于 [skillsmp.com](https://skillsmp.com) 的终端风格界面设计。

## 📞 联系方式

如有问题或建议，请通过以下方式联系：

- 提交 [Issue](https://github.com/chyinan/terminal-ui-design-system/issues)
- 创建 [Pull Request](https://github.com/chyinan/terminal-ui-design-system/pulls)

---

**Made with ❤️ for developers who love terminal aesthetics**
