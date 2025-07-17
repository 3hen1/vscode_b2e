Slidev 是如何实现暗黑模式（Dark Mode）和日间模式（Light Mode）的，以及你该如何在自定义组件中适配这两种模式。

  总的来说，Slidev 的深色模式切换主要依赖于以下两种技术的结合：

   1. HTML 根元素上的 `dark` class：当用户切换到暗黑模式时，Slidev 会在 <html> 标签上添加一个名为 dark 的 CSS class。这是整个机制的核心。
   2. UnoCSS 的 `dark:` 变体：Slidev 使用 UnoCSS (https://unocss.dev/) 作为其主要的原子化 CSS 框架。UnoCSS 内置了对暗黑模式的支持，只要在工具类前面加上 dark:
      前缀，这个样式就只会在暗黑模式下生效。

  ---

  1. Slidev 的实现原理

  当你点击 Slidev 界面右下角的模式切换按钮时：

   * 切换到暗黑模式：JavaScript 会执行，给 <html> 元素添加 class="dark"。
   * 切换回日间模式：JavaScript 会移除 <html> 元素上的 dark class。

  所有的样式（无论是 Slidev 内置的，还是主题提供的，或是你自定义的）都可以通过这个 .dark class 作为钩子，来应用不同的样式。

  例如，一个主题的 theme.css 文件里可能会有类似这样的代码，通过 CSS 变量来控制颜色：

    1 /* 日间模式下的默认值 */
    2 :root {
    3   --slidev-background-color: #ffffff;
    4   --slidev-text-color: #000000;
    5 }
    6
    7 /* 当 html.dark 存在时，覆盖这些变量 */
    8 .dark {
    9   --slidev-background-color: #121212;
   10   --slidev-text-color: #ffffff;
   11 }

  ---

  2. 如何让你的自定义组件支持双模式

  你有两种主要的方法来实现，推荐使用第一种，因为它更符合 Slidev 的开发习惯。

  方法一：使用 UnoCSS 的 dark: 前缀 (推荐)

  这是最简单、最直接的方式。你只需要在编写 Vue 组件时，为你希望在暗黑模式下改变的样式提供一个 dark: 的变体。

  示例：

  假设你要创建一个卡片组件 MyCard.vue。

    1 <!-- components/MyCard.vue -->
    2 <template>
    3   <div
    4     class="
    5       p-4 m-2 border rounded-lg
    6       bg-gray-100 text-gray-900
    7       dark:bg-gray-800 dark:text-gray-100 dark:border-gray-600
    8     "
    9   >
   10     <h3 class="text-xl font-bold text-teal-600 dark:text-teal-400">
   11       这是一个自定义组件
   12     </h3>
   13     <p class="mt-2">
   14       这段文字和背景颜色会自动适应日间和暗黑模式。
   15     </p>
   16   </div>
   17 </template>

  代码解释:

   * bg-gray-100: 在日间模式下，背景色为浅灰色。
   * dark:bg-gray-800: 在暗黑模式下（即 <html> 有 .dark class 时），背景色变为深灰色。
   * text-gray-900: 日间模式下的文字颜色。
   * dark:text-gray-100: 暗黑模式下的文字颜色。
   * text-teal-600: 日间模式下标题的颜色。
   * dark:text-teal-400: 暗黑模式下标题的颜色。

  你不需要做任何其他配置，Slidev 的构建过程会自动处理这一切。

  方法二：使用传统的 CSS <style> 块

  如果你有一些 UnoCSS 无法轻松实现的复杂样式，或者你更偏爱写传统的 CSS，你也可以在 Vue 组件的 <style> 块中手动处理。

  示例：

    1 <!-- components/MyStyledCard.vue -->
    2 <template>
    3   <div class="my-styled-card">
    4     <h3>自定义标题</h3>
    5     <p>使用 &lt;style&gt; 标签来定义样式。</p>
    6   </div>
    7 </template>
    8
    9 <style>
   10 /* 日间模式样式 */
   11 .my-styled-card {
   12   padding: 1rem;
   13   margin: 0.5rem;
   14   border: 1px solid #ddd;
   15   border-radius: 8px;
   16   background-color: #f9f9f9;
   17   color: #333;
   18   transition: background-color 0.3s, color 0.3s;
   19 }
   20
   21 .my-styled-card h3 {
   22   color: #005b96;
   23 }
   24
   25 /* 暗黑模式样式 */
   26 /* 通过 .dark 选择器来指定在暗黑模式下的样式 */
   27 .dark .my-styled-card {
   28   background-color: #2d3748; /* A dark blue-gray */
   29   border-color: #4a5568;
   30   color: #e2e8f0;
   31 }
   32
   33 .dark .my-styled-card h3 {
   34   color: #63b3ed; /* A lighter blue */
   35 }
   36 </style>

  代码解释:

   * 我们为 .my-styled-card 定义了默认（日间模式）的样式。
   * 然后，我们使用 .dark .my-styled-card 这样的组合选择器来定义当这个组件处于一个带有 .dark class 的父元素（即 <html>）内部时的样式。

  总结


  ┌───────────────┬──────────────────────────────┬────────────────────────────────┐
  │ 方法          │ 优点                         │ 缺点                           │
  ├───────────────┼──────────────────────────────┼────────────────────────────────┤
  │ UnoCSS (推荐) │ 简洁、快速、符合 Slidev 生态 │ 需要熟悉原子化 CSS 的概念      │
  │ 传统 CSS      │ 灵活，适合复杂样式           │ 代码量稍多，需要手动编写选择器 │
  └───────────────┴──────────────────────────────┴────────────────────────────────┘


  对于绝大多数场景，强烈建议你使用 UnoCSS 的 `dark:` 前缀，这是在 Slidev 中实现动态主题样式的最地道、最高效的方式。