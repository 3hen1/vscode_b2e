---
# 'default' 'apple-basic' 'seriph'
theme: ./theme
themeConfig:
  primary: "#5d8392"
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://bing.biturl.top/?resolution=1920&format=image&index=0&mkt=zh-CN
# some information about your slides (markdown enabled)
title: VSCode IDE from Beginner to Expert in Vibe Coding Era
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# base path for GitHub Pages deployment
base: /vscode_b2e/
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
aspectRatio: 16/8.3
---

# IDE Mastery: Integration & Usage  

VSCode IDE from Beginner to Expert

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right animate-ping/>
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://3hen1.github.io/vscode_b2e/1" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github animate-bounce/>
  </a>
</div>

<style>
.slidev-layout h1 {
  font-size: 3.25rem !important; /* 75% of text-4xl (2.25rem) = 1.6875rem, but using 1.875rem for 75% of 2.5rem */
}
</style>

<!--
目标客群：新的即将加入部门项目开发的 Java 、Go 工程师

课程目的：新同事可快速上手部门 Java、Go 项目
-->

---
transition: fade-out
---

# What is IDE?

An Integrated Development Environment (IDE) is a software application that provides comprehensive facilities for software development. 

- 📝 **Primary Goal** - To boost programmer productivity by integrating and simplifying the development workflow.
- 🎨 **Core Components** - Source Code Editor, Build Automation Tools, Debugger, Git
- 🧑‍💻 **Other Common Features** - Refactoring Tools, Testing Tools, Plugins
- 🤹 **Types and Evolution** - From command-line tools to multi-language, language-specific, and collaborative cloud-based environments.
- 🎥 **Modern Trends** - Language Server Protocol, AI-Assisted Programming
<br>
<br>

> Read more about [2024 IDE Survey - Stack Overflow](https://survey.stackoverflow.co/2024/technology#1-integrated-development-environment)




<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
**1. 定义 (Definition)**
集成开发环境（Integrated Development Environment, IDE）是一种软件应用程序，它将程序员进行软件开发所需的基本工具整合到一个图形用户界面（GUI）中，提供一个全面的开发环境。

**2. 主要目标 (Primary Goal)**
IDE 的核心目标是通过整合和简化开发流程来**提高程序员的生产力**。开发者无需在多个独立的工具（如文本编辑器、编译器、调试器）之间切换，所有操作都在一个统一的环境中完成，大大减少了配置和学习成本。

**3. 核心组件 (Core Components)**
一个典型的 IDE 通常包含以下几个关键部分：
*   **源代码编辑器 (Source Code Editor):** 不仅仅是文本编辑，还提供**语法高亮**、**智能代码补全 (IntelliSense)**、代码折叠和自动格式化等功能。
*   **构建自动化工具 (Build Automation Tools):** 集成了**编译器 (Compiler)** 或 **解释器 (Interpreter)**，允许开发者一键编译、链接和执行代码。
*   **调试器 (Debugger):** 允许开发者设置**断点 (Breakpoints)**，单步执行代码，检查变量值和内存状态，从而高效地定位和修复错误。
*   **版本控制系统集成 (Version Control Integration):** 通常内置了对 Git 等版本控制系统的支持，方便开发者进行代码提交、分支管理和历史追溯。

**4. 其他常见功能 (Other Common Features)**
*   **插件机制 
*   **重构工具 (Refactoring Tools):** 帮助开发者安全地改进和重组现有代码，而不会改变其外部行为。
*   **测试工具 (Testing Tools):** 集成单元测试框架，方便编写和运行测试用例。

**5. 类型与发展 (Types and Evolution)**
IDE 从早期的命令行工具集合演变而来，经历了多个阶段：
*   **多语言 IDE:** 支持多种编程语言，如 Visual Studio Code, Eclipse, JetBrains 系列 (IntelliJ IDEA, PyCharm 等)。
*   **特定语言 IDE:** 专为某一特定语言或平台设计，如 Xcode (用于 Apple 开发), IDLE (用于 Python)。
*   **Web/云 IDE:** 基于浏览器或云端，无需本地安装，如 GitHub Codespaces, AWS Cloud9，支持协作编程。

**6. 现代趋势 (Modern Trends)**
*   **语言服务器协议 (Language Server Protocol, LSP):** 由微软提出，它将语言特定的功能（如代码补全、定义跳转）从编辑器中分离出来，使得任何编辑器都可以通过集成 LSP 来支持任何语言，极大地促进了生态发展。
*   **AI 辅助编程 (AI-Assisted Programming):** 集成人工智能工具（如 GitHub Copilot），可以根据上下文自动生成代码片段甚至整个函数，进一步提升开发效率。
-->

---
transition: slide-up
level: 2
---

# Navigation

Hover on the bottom-left corner to see the navigation's controls panel, [learn more](https://sli.dev/guide/ui#navigation-bar)

## Keyboard Shortcuts

|                                                     |                             |
| --------------------------------------------------- | --------------------------- |
| <kbd>right</kbd> / <kbd>space</kbd>                 | next animation or slide     |
| <kbd>left</kbd>  / <kbd>shift</kbd><kbd>space</kbd> | previous animation or slide |
| <kbd>up</kbd>                                       | previous slide              |
| <kbd>down</kbd>                                     | next slide                  |

<!-- https://sli.dev/guide/animations.html#click-animation -->
<img
  v-click
  class="absolute -bottom-9 -left-7 w-80 opacity-50"
  src="https://sli.dev/assets/arrow-bottom-left.svg"
  alt=""
/>
<p v-after class="absolute bottom-23 left-45 opacity-30 transform -rotate-10">Here!</p>

---
layout: two-cols
layoutClass: gap-16
---

# Table of contents

You can use the `Toc` component to generate a table of contents for your slides:

```html
<Toc minDepth="1" maxDepth="1" />
```

The title will be inferred from your slide content, or you can override it with `title` and `level` in your frontmatter.

::right::

<Toc text-sm minDepth="1" maxDepth="2" />


---
layout: fact
---

| name | count |
| ---- | ----- |
| yyy  | 1000  |
| sss  | 1200  |

---
layout: center
---
 
center layout

| name | count |
| ---- | ----- |
| yyy  | 1000  |
| sss  | 1200  |

---
layout: intro
---

# intro title

short description

author: xxx

---
layout: quote
---

> # this is quote
> aa

---
layout: full
---

# full

| name | count |
| ---- | ----- |
| yyy  | 1000  |
| sss  | 1200  |

---
layout: section
---

this is section

---
layout: statement
---

this is statement

---
layout: two-cols-header-fixed
---

<Transform :scale="0.8">

# This spans both

</Transform>

::left::

<Transform :scale="0.6">

## Left

</Transform>

<v-clicks every="2">

- Item 1.1
- Item 1.2
- Item 2.1
- Item 2.2

</v-clicks>

::right::

## Right

<div v-click> visible after 1 click </div>
<v-click at="+2"><div> visible after 3 clicks </div></v-click>
<div v-click.hide="'-1'"> hidden after 2 clicks </div>

```js {none|1|2}{at:'+5'}
1  // highlighted after 7 clicks
2  // highlighted after 8 clicks
```

---
layout: image-left-fixed
image: ./research/stackoverflow-dev-survey-2024-technology-most-popular-technologies-new-collab-tools-social.png
---

<IDEVoting />


<!--
# Integrated development environment

Visual Studio Code is used by more than twice as many developers than its nearest (and related) alternative, Visual Studio.

[Stackoverflow Survey](https://survey.stackoverflow.co/2024/technology#1-integrated-development-environment)


-->



---
layout: iframe-left-fixed
url: https://tauc.tplinkcloud.com/#/auth/login
width: 1280
height: 800
scale: 0.3828
---

github

---
layout: image-right
image: https://cover.sli.dev
---

## Code

<AutoFitText :max="200" :min="10" modelValue="Use code snippets and get the highlighting directly, and even types hover!"/>

```ts [filename-example.ts] {all|4|6|6-7|9|all} twoslash
// TwoSlash enables TypeScript hover information
// and errors in markdown code blocks
// More at https://shiki.style/packages/twoslash
import { computed, ref } from 'vue'

const count = ref(0)
const doubled = computed(() => count.value * 2)

doubled.value = 2
```

<arrow v-click="[4, 5]" x1="350" y1="310" x2="195" y2="342" color="#953" width="2" arrowSize="1" />

<!-- This allow you to embed external code blocks -->
<<< @/snippets/external.ts#snippet

<!-- Footer -->

[Learn more](https://sli.dev/features/line-highlighting)

<!-- Inline style -->
<style>
.footnotes-sep {
  @apply mt-5 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

<!--
Notes can also sync with clicks

[click] This will be highlighted after the first click

[click] Highlighted with `count = ref(0)`

[click:3] Last click (skip two clicks)
-->

---
level: 2
---

# Shiki Magic Move

Powered by [shiki-magic-move](https://shiki-magic-move.netlify.app/), Slidev supports animations across multiple code snippets.

Add multiple code blocks and wrap them with <code>````md magic-move</code> (four backticks) to enable the magic move. For example:

````md magic-move {lines: true}
```ts {*|2|*}
// step 1
const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})
```

```ts {*|1-2|3-4|3-4,8}
// step 2
export default {
  data() {
    return {
      author: {
        name: 'John Doe',
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      }
    }
  }
}
```

```ts
// step 3
export default {
  data: () => ({
    author: {
      name: 'John Doe',
      books: [
        'Vue 2 - Advanced Guide',
        'Vue 3 - Basic Guide',
        'Vue 4 - The Mystery'
      ]
    }
  })
}
```

Non-code blocks are ignored.

```vue
<!-- step 4 -->
<script setup>
const author = {
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
}
</script>
```
````

---

# Components

<div grid="~ cols-2 gap-4">
<div>

You can use Vue components directly inside your slides.

We have provided a few built-in components like `<Tweet/>` and `<Youtube/>` that you can use directly. And adding your custom components is also super easy.

```html
<Counter :count="10" />
```

<!-- ./components/Counter.vue -->
<Counter :count="10" m="t-4" />

Check out [the guides](https://sli.dev/builtin/components.html) for more.

</div>
<div>

```html
<Tweet id="1390115482657726468" />
```

<Tweet id="1390115482657726468" scale="0.65" />

</div>
</div>

<!--
Presenter note with **bold**, *italic*, and ~~striked~~ text.

Also, HTML elements are valid:
<div class="flex w-full">
  <span style="flex-grow: 1;">Left content</span>
  <span>Right content</span>
</div>
-->

---
class: px-20
---

# Themes

Slidev comes with powerful theming support. Themes can provide styles, layouts, components, or even configurations for tools. Switching between themes by just **one edit** in your frontmatter:

<div grid="~ cols-2 gap-2" m="t-2">

```yaml
---
theme: default
---
```

```yaml
---
theme: seriph
---
```

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-default/01.png?raw=true" alt="">

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-seriph/01.png?raw=true" alt="">

</div>

Read more about [How to use a theme](https://sli.dev/guide/theme-addon#use-theme) and
check out the [Awesome Themes Gallery](https://sli.dev/resources/theme-gallery).

---

# Clicks Animations

You can add `v-click` to elements to add a click animation.

<div v-click>

This shows up when you click the slide:

```html
<div v-click>This shows up when you click the slide.</div>
```

</div>

<br>

<v-click>

The <span v-mark.red="3"><code>v-mark</code> directive</span>
also allows you to add
<span v-mark.circle.orange="4">inline marks</span>
, powered by [Rough Notation](https://roughnotation.com/):

```html
<span v-mark.underline.orange>inline markers</span>
```

</v-click>

<div mt-20 v-click>

[Learn more](https://sli.dev/guide/animations#click-animation)

</div>

---

# Motions

Motion animations are powered by [@vueuse/motion](https://motion.vueuse.org/), triggered by `v-motion` directive.

```html
<div
  v-motion
  :initial="{ x: -80 }"
  :enter="{ x: 0 }"
  :click-3="{ x: 80 }"
  :leave="{ x: 1000 }"
>
  Slidev
</div>
```

<div class="w-60 relative">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-square.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-triangle.png"
      alt=""
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 30, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

[Learn more](https://sli.dev/guide/animations.html#motion)

</div>

---

# LaTeX

LaTeX is supported out-of-box. Powered by [KaTeX](https://katex.org/).

<div h-3 />

Inline $\sqrt{3x-1}+(1+x)^2$

Block
$$ {1|3|all}
\begin{aligned}
\nabla \cdot \vec{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \vec{B} &= 0 \\
\nabla \times \vec{E} &= -\frac{\partial\vec{B}}{\partial t} \\
\nabla \times \vec{B} &= \mu_0\vec{J} + \mu_0\varepsilon_0\frac{\partial\vec{E}}{\partial t}
\end{aligned}
$$

[Learn more](https://sli.dev/features/latex)

---

# Diagrams

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<div class="grid grid-cols-4 gap-5 pt-4 -mb-6">

```mermaid {scale: 0.5, alt: 'A simple sequence diagram'}
sequenceDiagram
    Alice->John: Hello John, how are you?
    Note over Alice,John: A typical interaction
```

```mermaid {theme: 'neutral', scale: 0.8}
graph TD
B[Text] --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```

```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```

```plantuml {scale: 0.7}
@startuml

package "Some Group" {
  HTTP - [First Component]
  [Another Component]
}

node "Other Groups" {
  FTP - [Second Component]
  [First Component] --> FTP
}

cloud {
  [Example 1]
}

database "MySql" {
  folder "This is my folder" {
    [Folder 3]
  }
  frame "Foo" {
    [Frame 4]
  }
}

[Another Component] --> [Example 1]
[Example 1] --> [Folder 3]
[Folder 3] --> [Frame 4]

@enduml
```

</div>

Learn more: [Mermaid Diagrams](https://sli.dev/features/mermaid) and [PlantUML Diagrams](https://sli.dev/features/plantuml)

---
foo: bar
dragPos:
  square: 691,32,167,_,-16
---

# Draggable Elements

Double-click on the draggable elements to edit their positions.

<br>

###### Directive Usage

```md
<img v-drag="'square'" src="https://sli.dev/logo.png">
```

<br>

###### Component Usage

```md
<v-drag text-3xl>
  <div class="i-carbon:arrow-up" />
  Use the `v-drag` component to have a draggable container!
</v-drag>
```

<v-drag pos="663,206,261,_,-15">
  <div text-center text-3xl border border-main rounded>
    Double-click me!
  </div>
</v-drag>

<img v-drag="'square'" src="https://sli.dev/logo.png">

###### Draggable Arrow

```md
<v-drag-arrow two-way />
```

<v-drag-arrow pos="67,452,253,46" two-way op70 />

---
src: ./pages/imported-slides.md
hide: false
---

---

# Monaco Editor

Slidev provides built-in Monaco Editor support.

Add `{monaco}` to the code block to turn it into an editor:

```ts {monaco}
import { ref } from 'vue'
import { emptyArray } from './external'

const arr = ref(emptyArray(10))
```

Use `{monaco-run}` to create an editor that can execute the code directly in the slide:

```ts {monaco-run}
import { version } from 'vue'
import { emptyArray, sayHello } from './external'

sayHello()
console.log(`vue ${version}`)
console.log(emptyArray<number>(10).reduce(fib => [...fib, fib.at(-1)! + fib.at(-2)!], [1, 1]))
```

---
layout: center
class: text-center
---

# Learn More

[Documentation](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/resources/showcases)

<PoweredBySlidev mt-10 />
