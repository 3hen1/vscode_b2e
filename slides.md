---
# 'default' 'apple-basic' 'seriph'
theme: ./theme
themeConfig:
  primary: "#5d8392"
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://bing.biturl.top/?resolution=1920&format=image&index=0&mkt=en-US
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
transition: fade-out | fade
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
transition: slide-left | slide-right
level: 2
title: navigation
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
transition: slide-left | slide-right
title: what is ide
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
title: survey
layout: image-left-fixed
level: 2
image: /images/stackoverflow-dev-survey-2024-technology-most-popular-technologies-new-collab-tools-social.png
transition: slide-left | slide-right
---

<IDEVoting />


<!--
# Integrated development environment

Visual Studio Code is used by more than twice as many developers than its nearest (and related) alternative, Visual Studio.

[Stackoverflow Survey](https://survey.stackoverflow.co/2024/technology#1-integrated-development-environment)


-->

---
title: contents
layoutClass: gap-16
---

# Table of contents

<Transform :scale="0.68">

<Toc text-sm minDepth="1" maxDepth="2" columns="5" />

</Transform>

---
title: getting started
layout: center
class: px-8 py-4
transition: slide-left | slide-right
---

<div class="max-h-screen overflow-y-auto">
  <div class="mb-6">
    <h5 class="text-xl font-semibold mb-4 text-gray-700">Getting started</h5>
    <div class="grid grid-cols-3 gap-4 mb-8">
      <div class="border border-gray-200 rounded-lg p-4 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:download class="w-5 h-5 text-blue-600" />
          </div> 
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Download Visual Studio Code</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Download VS Code for Windows, macOS, or Linux.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-4 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:play class="w-5 h-5 text-green-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Getting started</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Discover the key features of VS Code with the step-by-step tutorial.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-4 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:bot class="w-5 h-5 text-purple-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Code faster with AI</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Get started with GitHub Copilot, your AI coding assistant.</p>
          </div>
        </div>
      </div>
    </div>
    <h5 class="text-xl font-semibold mb-4 text-gray-700">Code with rich features</h5>
    <div class="grid grid-cols-3 gap-3">
      <div class="border border-gray-200 rounded-lg p-3 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-8 h-8 bg-orange-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:code class="w-4 h-4 text-orange-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Code in any language</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Write code in your favorite programming language.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-3 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-8 h-8 bg-red-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:version-major class="w-4 h-4 text-red-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Version control</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Built-in support for git and many other source control providers.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-3 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-8 h-8 bg-yellow-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:debug class="w-4 h-4 text-yellow-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Debugging</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Debug your code without leaving your editor.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-3 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-8 h-8 bg-teal-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:test-tool class="w-4 h-4 text-teal-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Testing</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Run automated tests and view test coverage to validate your code.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-3 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-8 h-8 bg-indigo-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:cloud class="w-4 h-4 text-indigo-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Code anywhere</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Use a container, remote machine, or WSL as your development environment.</p>
          </div>
        </div>
      </div>
      <div class="border border-gray-200 rounded-lg p-3 hover:shadow-lg transition-shadow bg-white">
        <div class="flex items-start space-x-3">
          <div class="w-8 h-8 bg-pink-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <carbon:video class="w-4 h-4 text-pink-600" />
          </div>
          <div>
            <h6 class="font-semibold text-gray-900 mb-1 text-sm">Videos</h6>
            <p class="text-xs text-gray-600 !m-0 leading-none">Watch the introduction videos to learn more.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
.slidev-layout h1 {
  background: linear-gradient(45deg, #007ACC, #4EC5D4);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 2rem;
}
</style>




---

## Slide 7: Installation & Getting Started (5 minutes)

*   **Objective:** Guide users through installation and familiarize them with VS Code's user interface.
*   **Content:**
    *   **Installation:**
        *   Download from official website: [Download the Insiders build](https://code.visualstudio.com/insiders)
        *   Install "codei" command to command line (Command Palette: `Shell Command: Install 'code-insider' command in PATH`)
    *   **User Interface (UI) Tour:**
        *   **Activity Bar:** Files, Search, Git, Debug, Extensions
        *   **Side Bar:** Displays detailed information for the active view
        *   **Editor:** Where you write code
        *   **Panel:** Terminal, Output, Problems, Debug Console
        *   **Status Bar:** Git branch, errors/warnings, language mode
    *   **Command Palette:** `Ctrl+Shift+P` / `Cmd+Shift+P` - The central nervous system of VS Code

---
layout: "center"
class: "text-center"
---

# Course Outline

We will strictly follow the structure of the official documentation to ensure a systematic and authoritative learning experience.

1.  **Setup**: Installation and Environment Configuration
2.  **Get Started**: Quick Start
3.  **Configure**: Personalize Your Editor
4.  **Edit code**: Efficient Coding Techniques
5.  **Build, Debug, Test**: The Full Development Workflow
6.  **GitHub Copilot**: Your AI Partner
7.  **Source Control**: Git Integration
8.  **Terminal**: Integrated Terminal
9.  **Languages**: In-depth Support for Java & Go
10. **Reference**: Reference Manual

---

# 1.1 Setup: Overview

- **Core Concept**: VS Code is a free, lightweight, cross-platform code editor.
- **Installation Steps**:
  1.  Download and install the main VS Code application.
  2.  Install additional components, such as Git and language-specific runtimes (JDK, Go).
  3.  Install language support, debuggers, and themes through the Extension Marketplace.
- **Key Features**:
  - **Monthly Updates**: Official new versions are released monthly with support for automatic updates.
  - **Insiders Version**: A daily build for early access to new features.
  - **Portable Mode**: Allows you to configure VS Code on portable devices like a USB drive.

<!--
这是我们课程的第一部分：安装。

- 首先要明确，VS Code 本身只是一个编辑器框架。它的强大之处在于其可扩展性。
- 对于我们后端开发来说，“安装附加组件”这一步至关重要。这意味着我们需要事先独立安装好 JDK、Go 的工具链以及 Git。VS Code 会利用这些已经存在的工具链来提供语言服务。
- VS Code 没有像传统 IDE 那样的“新建项目”向导。我们通常是先用构建工具（如 Maven, Gradle）或命令行创建好项目结构，然后用 VS Code 打开项目文件夹。
- 课外引申：可以向学员介绍“便携模式”的用途，比如在不同电脑上保持开发环境一致，或者在受限环境中使用。同时，可以鼓励学员尝试 Insiders 版本，以了解最新的功能动态。
-->

---

# 1.2 Setup: Windows Installation

- **Installer Types**:
  - **User Setup**: **Recommended**. No administrator privileges required, installs in the user directory, and provides smoother updates.
  - **System Setup**: Requires administrator privileges, installs for all users on the system.
- **Important Tip**:
  - Check "Add to PATH" during installation. You can then launch VS Code from any terminal in the current directory using the `code .` command.
- **Core for Backend Development**: **Windows Subsystem for Linux (WSL)**
  - Combined with the **WSL extension**, it provides a native Linux development and debugging experience on Windows, which is an excellent choice for Java/Go applications that need to be deployed to Linux servers.

<!--
这页我们关注 Windows 用户的安装要点。

- 重点强调 **User Setup** 的好处。对于个人开发者来说，这是最方便、最无痛的选项。
- `code .` 命令是日常使用频率非常高的命令，务必让学员掌握。
- **WSL 是本页的重中之重**。对于后端开发，很多时候我们的生产环境是 Linux。WSL + VS Code Remote Development 插件可以让我们在 Windows 上拥有和 Linux 完全一致的开发环境，解决了环境差异带来的诸多问题。可以现场演示一下，在 Windows Terminal 中进入 WSL，然后用 `code .` 启动 VS Code，整个环境（包括终端、调试器）就都运行在 Linux 子系统里了，体验非常无缝。
- 课外引申：可以简单提及 Windows Terminal，它是 WSL 的好伴侣。
-->

---

# 2.1 Get Started: VS Code Tutorial

- **Core Workflow**: **Open Folder (Workspace)** -> Code -> Debug -> Commit.
- **The Big Four (UI)**:
  - **Editor**: Your main coding battlefield.
  - **Side Bar**: Entry point for Files, Search, Git, Debug, and Extensions.
  - **Panel**: Integrated Terminal, Output, Problems, etc.
  - **Command Palette**: `Ctrl+Shift+P`, the universal command entry point.
- **Core Capabilities Come from Extensions**: VS Code gains support for specific languages (like Java, Go) for IntelliSense, debugging, and refactoring by installing extensions.

<!--
这一页是新用户入门的基石。

- **动手演示是关键**：强烈建议讲师按照官方文档的流程，现场创建一个 `vscode101` 文件夹，并实际操作一遍：创建文件、使用智能提示、在集成终端里执行命令、通过 Source Control 视图提交一次 commit、安装一个 Java 或 Go 的扩展。
- **强调心智模型**：帮助学员建立“以文件夹为中心”的工作模式，而不是“以文件为中心”。
- **反复强调命令面板**：告诉学员，当不知道一个功能在哪里时，第一反应应该是按 `Ctrl+Shift+P` 搜索它。
- **Workspace Trust**: 简单解释一下工作区信任机制，因为它是在打开新项目时第一个弹出的对话框。让学员明白这是为了安全，自己创建的项目直接点“信任”即可。
-->

---

# 2.2 Get Started: User Interface

- **Core Layout**: Main Editor, Primary/Secondary Side Bars, Activity Bar, Status Bar, Panel area.
- **Efficient Layout Techniques**:
  - **Side by side Editing**: `Alt+Click` a file or use the split button to greatly improve code comparison and reference efficiency.
  - **Editor Groups**: Organize related files into different groups to keep the workspace tidy.
  - **Floating Windows**: Drag editors or terminals out of the main window to make full use of multiple monitors.
- **Navigation Tools**:
  - **Breadcrumbs**: File path + code structure navigation for quick jumps.
  - **Outline View**: View the symbol structure (functions, variables, etc.) in a file.
  - **Timeline View**: View the Git commit history and local save history of a file.

<!--
本页的目的是让学员熟悉并能高效利用VS Code的UI布局。

- **动手演示**：
  - 演示如何将一个编辑器拖拽到另一个的侧边，实现分屏。
  - 演示如何创建一个新的编辑器组，并将几个文件拖进去。
  - **重点演示**：将一个终端或编辑器拖拽成一个独立的浮动窗口，这对于多显示器用户来说非常实用。
- **介绍导航工具**：
  - 点击面包屑中的任意部分，展示如何快速在文件和符号层级间跳转。
  - 展示大纲视图，并演示如何通过点击大纲中的条目来跳转到对应的函数。
  - 展示时间线视图，特别是本地历史记录（Local History），这是一个“后悔药”功能，可以找回未提交的修改。
- **课外引申**：可以引导学员自行探索 Zen Mode (禅模式) 和 Centered Layout (居中布局)，这些对于希望免打扰、专注编码的场景很有帮助。
-->

---

# 2.3 Get Started: Personalize VS Code

- **Settings**: `Ctrl+,`
  - **User Settings**: Global settings that define your personal coding style.
  - **Workspace Settings**: Project-level settings that override user settings, used for unifying team standards.
- **Keyboard Shortcuts**: `Ctrl+K Ctrl+S`
  - You can change the shortcuts for almost any command to match your muscle memory.
  - **Keymap Extensions**: Allow you to set shortcuts to match Vim, Sublime Text, IntelliJ IDEA, etc. with one click.
- **Themes**: `Ctrl+K Ctrl+T`
  - **Color Themes**: Change the overall UI and code highlighting colors.
  - **File Icon Themes**: Change the icons in the file explorer.

<!--
这一页的核心是告诉学员，VS Code可以被塑造成任何他们想要的样子。

- **设置的哲学**：重点解释 **用户设置** 和 **工作区设置** 的区别和应用场景。用户设置是你自己的偏好（比如字体、主题），而工作区设置是项目规范（比如代码缩进、格式化规则），后者应该被提交到Git仓库，保证团队成员环境一致。
- **快捷键的迁移成本**：对于从其他IDE转过来的开发者，**Keymap扩展** 是一个巨大的福音。可以现场演示一下，在扩展市场搜索 "IntelliJ IDEA Keymap" 并安装，这样很多熟悉的快捷键就都能用了，大大降低了学习成本。
- **视觉体验**：快速演示如何切换颜色主题和文件图标主题。一个舒适的视觉环境可以显著提升编程体验。
- **课外引申**：可以引导学员了解如何通过安装“Language Pack”来改变VS Code的显示语言。
-->

---

# 2.4 Get Started: Install Extensions

- **Extensions are the soul of VS Code**: They add language support, debuggers, new tools, and new commands to VS Code.
- **How to manage extensions**:
  - Search, install, and uninstall in the **Extensions View** (`Ctrl+Shift+X`).
  - **Recommended Extensions**: VS Code intelligently recommends relevant extensions based on the project type you open.
- **Essential Extension Packs for Backend Development**:
  - **Extension Pack for Java**: One-click installation of the full toolset for Java development.
  - **Go**: The official Go language support extension maintained by Google.
  - **Remote Development**: An essential suite for remote development, supporting SSH, WSL, and Dev Containers.

<!--
本页是整个培训的重点之一，因为扩展决定了VS Code对特定语言的能力。

- **动手演示**：
  - 打开扩展视图，搜索 "Java"，找到并展示 **Extension Pack for Java**，解释“扩展包”的概念（一个扩展包含了其他多个扩展）。
  - 同样地，搜索并展示 **Go** 官方扩展。
  - 搜索并展示 **Remote Development** 扩展包，并预告我们后面会深入讲解它的强大功能。
- **强调官方和社区**：提醒学员，安装扩展时要注意发布者（Publisher）。比如，Java 扩展要认准 Microsoft，Go 扩展要认准 Google。对于其他工具，比如 Docker、GitLens，也要选择信誉好、安装量高的扩展。
- **课外引申**：可以介绍 **Profiles** 功能，它允许你为不同的开发任务（比如Java项目、Go项目、写Markdown）创建不同的扩展集合，避免不必要的扩展在不相关的项目中加载，保持编辑器轻快。
-->

---

# 2.5 Get Started: Tips and Tricks

- **Command Palette**: `Ctrl+Shift+P`
  - Not just for commands; remove the `>` to search for filenames directly (`Ctrl+P`).
  - Type `@` to search for symbols (functions, variables).
  - Type `:` to jump to a line number.
- **Efficient Editing**:
  - **Multiple Cursors**: `Alt+Click` to add cursors; `Ctrl+D` to select the next match.
  - **Column (Box) Selection**: `Shift+Alt+Drag` or configure a keyboard shortcut.
  - **Move/Copy Lines**: `Alt+Up/Down` to move lines; `Shift+Alt+Up/Down` to copy lines.
- **Navigation**:
  - `Ctrl+Tab`: Navigate through the history of opened editors.
  - `Ctrl+G`: Go to a specific line.

<!--
这一页的目标是分享一些能立刻提升生产力的“黑魔法”。

- **再次强调命令面板**：命令面板是VS Code的瑞士军刀。演示如何用它快速打开文件、跳转到符号和行号，这比在文件浏览器里手动找要快得多。
- **多光标是神器**：现场演示如何使用多光标同时修改多个地方的文本。这是重构和批量修改的利器，一旦掌握就离不开了。
- **列选择的威力**：演示如何使用列选择来对齐代码或在多行同一位置插入文本。
- **代码行操作**：演示如何快速移动和复制整行代码，这是日常编码中使用频率非常高的操作。
- **课外引申**：鼓励学员下载并打印官方的键盘快捷键备忘单 (Keyboard Shortcut Reference Sheet)，贴在显示器旁边，时常查阅，形成肌肉记忆。
-->

---


# 3.1 Configure: Display Language

- **Core Concept**: VS Code's interface is in English by default. Other languages are enabled by installing **Language Packs** extensions.
- **How to Configure**:
  1.  Open the **Command Palette** (`Ctrl+Shift+P`).
  2.  Type and run the `Configure Display Language` command.
  3.  Select your desired language (e.g., `zh-cn`).
  4.  If the corresponding language pack is not installed, VS Code will automatically prompt you to install it.
  5.  Restart VS Code for the changes to take effect.
- **Temporary Switch**: You can temporarily specify a language via a command-line argument when launching VS Code:
  `code . --locale=fr`

<!--
这一页内容比较简单，可以快速过。

- **智能推荐**: 提一下，如果你的操作系统是中文环境，首次启动 VS Code 时，它会自动推荐你安装中文语言包，非常智能。
- **动手演示**: 快速演示一遍 `Configure Display Language` 命令的流程，展示如何从列表中选择语言。
- **区分“显示语言”和“编程语言”**: 强调一下，这里的“语言”指的是 VS Code 界面的语言，而不是 Java、Go 等编程语言的支持。编程语言的支持是通过安装不同的扩展（如 Extension Pack for Java）来实现的，这是一个重要的区分，避免初学者混淆。
-->

---

# 3.2 Configure: Custom Layout

- **Dual Side Bars**: Open two sidebars (primary and secondary) at the same time, for example, view the file tree on the left and GitLens or Copilot Chat on the right.
- **Panel Position**: The panel area (Terminal, Problems, etc.) can be moved to the left, right, top, or bottom of the window.
- **Drag and Drop Views**: Almost all views (like Search, Outline) can be dragged to any sidebar or panel area, and even merged into tab groups.
- **Locked Editor Groups**: Lock an editor group (e.g., for the terminal) so that newly opened files always open in other unlocked groups, preventing the terminal from being accidentally covered.

<!--
本页的核心是展示VS Code布局的极致灵活性。

- **动手演示**：
  - **双侧边栏**：打开“大纲”视图，然后把它从主侧边栏拖到窗口右侧，形成第二个侧边栏。这是一个非常实用的功能。
  - **面板位置**：将下方的终端面板移动到窗口右侧，展示如何为编辑器腾出更多的垂直空间。
  - **视图合并**：将“问题”面板拖拽到“终端”面板的标签栏上，让它们成为可以切换的标签页。
  - **锁定编辑器组**：打开一个终端到编辑器区域，然后锁定这个组。接着在另一个编辑器组中打开新文件，学员会看到新文件总是在未锁定的组里打开，而终端始终可见。
- **课外引申**：鼓励学员探索 **View: Reset View Locations** 命令，当他们把布局搞乱时，可以用这个命令一键恢复默认布局。
-->

---

# 3.3 Configure: Keyboard Shortcuts

- **Editing Methods**:
  - **Graphical Editor**: `Ctrl+K Ctrl+S`, provides search, filtering, and conflict detection.
  - **JSON File**: Advanced customization via `keybindings.json`.
- **Keymap Extensions**: A great tool to lower the migration cost! Install with one click to use familiar keybinding schemes from IntelliJ IDEA, Eclipse, Vim, etc.
- **Core Concept: `when` clause**: Makes a shortcut effective only in a specific context. For example, a shortcut can be triggered only during debugging or when the focus is on the terminal.
- **Conflict Resolution**: When a shortcut is bound to multiple commands, the editor will show a conflict, and you need to resolve it based on the `when` clause or personal preference.

<!--
这一页的目标是让学员无痛地从其他编辑器迁移过来，并能定制自己的专属快捷键。

- **Keymap 扩展是关键**：对于从其他IDE（特别是IntelliJ IDEA）转来的Java开发者，这是必须首先介绍的功能。现场演示在扩展市场搜索并安装 "IntelliJ IDEA Keymap"，然后展示一些常用的IDEA快捷键（如 `Ctrl+Alt+L` 格式化代码）已经生效。
- **演示如何修改快捷键**：打开快捷键编辑器 (`Ctrl+K Ctrl+S`)，搜索一个常用命令（比如 "Toggle Line Comment"），然后演示如何点击铅笔图标来修改它的快捷键。
- **解释 `when` 子句**：以 `F5` 键为例，解释它为什么在非调试模式下是“启动调试”，而在调试模式下是“继续”。通过在快捷键编辑器中搜索 `F5`，展示这两个命令不同的 `when` 子句 (`inDebugMode` vs `!inDebugMode`)，让学员理解上下文绑定的概念。
- **课外引申**：鼓励学员下载官方的快捷键参考表 (Keyboard Shortcut Reference)，并尝试将一两个自己最常用的操作绑定到顺手的快捷键上。
-->

---

# 3.4 Configure: Settings

- **Setting Types**:
  - **User Settings**: Global settings stored in the user directory, affecting all VS Code instances.
  - **Workspace Settings**: Project-level settings stored in the project's `.vscode` folder, valid only for the current project and overriding user settings.
- **Access Methods**:
  - **Settings Editor**: `Ctrl+,` (or `Cmd+,`), a graphical interface for easy searching and modification.
  - **JSON File**: `settings.json`, for direct editing, suitable for advanced configuration and team sharing.
- **Priority**: Workspace Settings > User Settings. This means teams can unify code styles, linter rules, etc., through workspace settings.
- **Language-Specific Settings**: You can configure separate settings for specific languages (like Java, Go), such as formatting rules and linter checks.

<!--
这一页是VS Code个性化配置的核心。

- **重点强调用户设置和工作区设置的区别**：
  - **用户设置**：是你个人的偏好，比如字体大小、主题、是否自动保存等。
  - **工作区设置**：是项目级别的配置，例如代码缩进是2个空格还是4个空格，是否启用某个Linter，这些应该被提交到Git仓库，确保团队成员使用统一的开发规范。
- **演示如何访问设置**：
  - 首先演示通过 `Ctrl+,` 打开图形化设置界面，并演示如何搜索设置（例如搜索 `files.autoSave`）。
  - 然后演示通过命令面板 `Preferences: Open User Settings (JSON)` 和 `Preferences: Open Workspace Settings (JSON)` 直接打开 `settings.json` 文件，并解释直接编辑JSON的优势（例如，可以添加注释，方便团队协作）。
- **语言特定设置**：演示如何为 Java 或 Go 配置语言特定设置。例如，可以设置 Java 文件的 `editor.formatOnSave` 为 `true`，而其他文件类型不受影响。这对于后端开发中不同语言的代码风格统一非常重要。
- **课外引申**：可以提及一些常用的设置，例如 `editor.tabSize` (Tab 宽度), `editor.insertSpaces` (使用空格代替Tab), `files.autoSave` (自动保存)。
-->


---

# 3.5 Configure: Settings Sync

- **Core Functionality**: Sync your VS Code configuration across multiple devices, including:
  - Settings
  - Keyboard Shortcuts
  - User Snippets
  - Extensions and their enabled status
  - UI State
- **How to Enable**: Turn on via the **Manage** gear menu or the **Accounts** menu's **Backup and Sync Settings...**.
- **Login**: Supports login with Microsoft or GitHub accounts.
- **Conflict Handling**: When conflicts occur, you can choose to merge, replace local, or resolve manually.
- **Important Note**: Extensions in remote windows (like SSH, Dev Containers, WSL) are not automatically synced.

<!--
这一页对于经常在多台机器（例如台式机、笔记本、远程服务器）之间切换的开发者来说非常重要。

- **强调一致性**：解释 Settings Sync 如何帮助开发者在任何机器上都能获得一致的开发体验，无需重复配置。
- **动手演示**：
  - 演示如何通过左下角的齿轮图标或账户图标开启 Settings Sync。
  - 简单介绍同步的内容，特别是设置、快捷键和扩展。
  - 提及“合并或替换”的选项，并解释其含义。
- **远程窗口的注意事项**：特别强调远程窗口（SSH, WSL, Dev Containers）中的扩展不会自动同步。这意味着如果你在远程环境中安装了扩展，它们不会自动同步到你的本地机器，反之亦然。这是为了保持远程环境的独立性和轻量级。
- **课外引申**：可以提及 Settings Sync 还会备份你的配置数据到云端，即使电脑损坏，也能快速恢复开发环境。
-->


---

# 3.6 Configure: Extension Marketplace

- **Extension Marketplace**: The official source for VS Code extensions, offering a vast number to enhance functionality.
- **Browsing and Installing**: Search, install, and manage extensions via the **Extensions View** (`Ctrl+Shift+X`).
  - You can filter and sort by category, install count, rating, etc.
  - Supports installing pre-release versions.
- **Managing Extensions**: Enable/disable (globally or per workspace), update, uninstall.
  - Extensions can be updated automatically or manually.
- **Security**: The marketplace scans extensions for malware and prompts for trust of third-party publishers.
- **Workspace Recommendations**: Recommend extensions in the project's `.vscode/extensions.json` to facilitate a unified development environment for the team.

<!--
本页是对扩展市场的深入介绍，补充了之前“安装扩展”的内容。

- **强调扩展的丰富性**：再次强调扩展是VS Code强大的原因，并鼓励学员积极探索。
- **演示扩展视图的搜索和筛选功能**：例如，搜索 `@category:"Programming Languages"` 或 `@installed` 来查看已安装的扩展。
- **讲解工作区推荐扩展**：这是一个非常重要的团队协作功能。演示如何创建一个 `.vscode/extensions.json` 文件，并添加一些推荐的扩展ID（例如 Java 和 Go 的扩展）。解释当团队成员打开项目时，VS Code会自动提示安装这些推荐扩展，从而统一团队的开发环境。
- **安全提示**：提醒学员，安装扩展时要注意发布者和安装时的信任提示，确保安装的扩展是可信的。
- **课外引申**：可以提及命令行管理扩展 (`code --install-extension`)，这对于自动化部署或CI/CD环境非常有用。
-->

---

# 3.7 Configure: Themes

- **Theme Types**:
  - **Color Themes**: Change the overall color scheme of the editor and UI, affecting code highlighting.
  - **File Icon Themes**: Change the icons for files and folders in the file explorer.
  - **Product Icon Themes**: Change the icons of the VS Code UI itself (e.g., Activity Bar icons).
- **How to Switch**:
  - **Color Theme**: `Ctrl+K Ctrl+T` (or via Command Palette `Preferences: Color Theme`).
  - **File Icon Theme**: Via Command Palette `Preferences: File Icon Theme`.
  - **Product Icon Theme**: Via Command Palette `Preferences: Product Icon Theme`.
- **Customization**: You can further fine-tune theme colors through settings like `workbench.colorCustomizations`.
- **Auto Switch**: Can automatically switch themes based on the operating system's light/dark mode.

<!--
这一页是关于VS Code的视觉定制，虽然不直接影响功能，但一个舒适的视觉环境能显著提升开发体验。

- **动手演示**：
  - 快速演示如何通过 `Ctrl+K Ctrl+T` 切换不同的颜色主题，让学员直观感受不同主题的风格。
  - 演示如何切换文件图标主题，例如安装一个 Material Icon Theme。
  - 简单提及产品图标主题，展示其对UI图标的影响。
- **强调个性化**：告诉学员，选择一个自己喜欢且不刺眼的主题非常重要，可以减少视觉疲劳。
- **课外引申**：
  - 鼓励学员在扩展市场搜索更多主题，找到最适合自己的。
  - 对于有兴趣的学员，可以提及如何通过 `workbench.colorCustomizations` 在 `settings.json` 中对主题进行更细粒度的定制，例如修改某个特定UI元素的颜色。
  - 提及自动切换主题功能，这对于经常在不同光照环境下工作的开发者很有用。
-->


---

# 3.8 Configure: Profiles

- **Core Concept**: A "profile" is a collection of VS Code settings, extensions, keyboard shortcuts, UI layout, etc., bundled together.
- **Use Cases**:
  - **Multi-language Development**: Create dedicated profiles for different languages like Java and Go to avoid loading unnecessary extensions.
  - **Specific Projects**: Customize configurations for specific projects (e.g., a Spring Boot project).
  - **Demos/Teaching**: Quickly switch to a clean or preset environment for demonstrations.
- **Management**:
  - **Profiles Editor**: A unified place to create, edit, switch, and delete profiles.
  - **Associate with Workspace**: Profiles can be associated with specific folders or workspaces, automatically switching when opened.
  - **Import/Export**: Convenient for sharing with others or migrating between different machines.

<!--
Profiles 是一个非常强大的功能，尤其适合需要处理多种技术栈的后端开发者。

- **强调“隔离”和“定制”**：解释 Profiles 如何帮助开发者保持环境的“纯净”，避免不同项目或语言的配置相互干扰。
- **动手演示**：
  - 打开 Profiles 编辑器（通过左下角的齿轮图标 -> Profiles）。
  - 演示如何创建一个新的 Profile，例如一个“Java Backend”Profile，并选择只包含 Java 相关的扩展和设置。
  - 演示如何切换 Profile，并展示切换后扩展和设置的变化。
  - 提及可以将 Profile 与工作区关联，这样每次打开特定项目时，VS Code 都会自动加载对应的 Profile。
- **分享与协作**：强调导入/导出功能对于团队协作的重要性，可以快速分享统一的开发环境。
- **课外引申**：可以提及“临时 Profile”的用途，例如在测试某个新扩展或排查问题时，创建一个临时 Profile，用完即焚，不影响主环境。
-->



---

# 3.9 Configure: Telemetry

- **Purpose**: VS Code collects telemetry data to improve the product, such as debugging issues, optimizing performance, and prioritizing new features.
- **Data Types**: Mainly includes crash reports, error telemetry, and usage data.
- **Disabling Telemetry**: Controlled via the `telemetry.telemetryLevel` setting:
  - `all`: Collects all data.
  - `off`: **Completely disables all telemetry data collection**.
- **Extension Telemetry**: Extensions may collect data independently and are not controlled by the `telemetry.telemetryLevel` setting. Please consult the extension's documentation.

<!--
这一页是关于隐私和数据收集，对于一些学员来说可能比较敏感，需要清晰地解释。

- **强调透明度**：说明 VS Code 官方对遥测数据的收集是透明的，并且提供了明确的禁用选项。
- **演示如何禁用遥测**：打开设置 (`Ctrl+,`)，搜索 `telemetry.telemetryLevel`，并演示如何将其设置为 `off`。强调这是完全禁用。
- **区分核心与扩展**：特别强调，`telemetry.telemetryLevel` 只控制 VS Code 核心的遥测数据。学员安装的第三方扩展可能会有自己的遥测机制，如果关心这部分，需要单独查阅扩展的文档。
- **隐私声明**：可以提及官方的隐私声明链接，鼓励学员自行查阅。
- **课外引申**：可以简单介绍 `Developer: Show Telemetry` 命令，它可以在输出面板中实时查看 VS Code 正在发送的遥测事件，这对于理解遥测机制很有帮助。
-->

---

# 4.1 Edit code: Basic Editing

- **Multiple Cursors**: `Alt+Click` to add cursors, `Ctrl+D` to select the next match for efficient bulk editing.
- **Column Selection**: `Shift+Alt+Drag` for block selection, useful for handling tabular data or aligning code.
- **Auto Save & Hot Exit**: Configure `files.autoSave` for automatic saving, `files.hotExit` ensures unsaved changes are not lost.
- **Find and Replace**:
  - **In-file**: `Ctrl+F`, supports regex, whole word match, case sensitive.
  - **Global**: `Ctrl+Shift+F`, search and replace across files, supports include/exclude paths.
- **Code Formatting**: `Format Document` (`Shift+Alt+F`) or `Format Selection`, supports format on save.
- **Code Folding**: Fold/unfold code blocks based on structure to improve readability.

<!--
这一页的目标是让学员掌握VS Code最基础也是最常用的编辑功能，这些功能是日常编码效率的基石。

- **多光标演示**: 现场演示 `Alt+Click` 和 `Ctrl+D` 的用法，强调其在重构和批量修改变量名时的效率。这是VS Code的明星功能之一。
- **全局搜索演示**: 演示 `Ctrl+Shift+F`，并展示如何使用包含/排除模式来精确搜索。强调其在大型项目中的重要性，例如快速查找某个API的所有调用点。
- **自动保存**: 强调 `files.autoSave` 的重要性，避免意外数据丢失。建议设置为 `afterDelay`。
- **代码格式化**: 强调 `editor.formatOnSave` 的设置，保持代码风格一致性，这对于团队协作尤为重要。
- **折叠**: 演示如何折叠函数、类、注释块等，让代码结构更清晰，方便快速浏览。
- **课外引申**: 可以提及文件编码、行尾符等设置，以及如何比较文件差异 (`code --diff file1 file2`)。
-->

---

# 4.2 Edit code: IntelliSense

- **Core Features**: Provides smart code completions, parameter info, quick info, and member lists.
- **How it Works**: Powered by a Language Service, based on language semantics and code analysis.
- **Triggering**: Pops up automatically, or can be triggered manually (`Ctrl+Space`).
- **Types**: Includes language server suggestions, snippets, and word-based text completions.
- **Customization**: Can be personalized through settings (`editor.quickSuggestions`, `editor.acceptSuggestionOnEnter`, etc.) and shortcuts.
- **AI Enhancement**: AI tools like GitHub Copilot further enhance the intelligence of code completions and suggestions.

<!--
IntelliSense 是现代IDE的基石，也是VS Code提高开发效率的关键。

- **强调其重要性**：对于Java和Go这类强类型语言，IntelliSense能够极大地减少拼写错误，提高编码速度，并帮助开发者快速了解API。
- **动手演示**：
  - 在一个Java或Go文件中，演示代码自动补全，包括方法、变量、类名等。
  - 演示如何手动触发 (`Ctrl+Space`) 建议。
- **AI的加持**：简单提及 GitHub Copilot 如何通过AI进一步增强 IntelliSense 的能力，提供更智能、更上下文相关的建议。
- **课外引申**：
  - 鼓励学员探索 `editor.quickSuggestions` 和 `editor.acceptSuggestionOnEnter` 等设置，根据自己的习惯调整 IntelliSense 的行为。
  - 提及 IntelliSense 的 CamelCase 过滤功能，例如输入 `cra` 就能快速找到 `createApplication`。
-->

---

# 4.3 Edit code: Code Navigation

- **Quick File Navigation**: `Ctrl+Tab` to quickly switch between recently opened files; `Ctrl+P` to quickly open a file.
- **Breadcrumbs**: The top navigation bar shows the file path and symbol path for easy navigation.
- **Definition & Implementation**:
  - **Go to Definition**: `F12` or `Ctrl+Click`, jumps to the symbol's definition.
  - **Go to Type Definition**: Jumps to the type definition of a variable or expression.
  - **Go to Implementation**: Jumps to the concrete implementation of an interface or abstract method.
- **Symbol Navigation**:
  - **Go to Symbol in File**: `Ctrl+Shift+O`, quickly jump to functions, variables, etc. in the current file.
  - **Go to Symbol in Workspace**: `Ctrl+T`, search for symbols across all files in the workspace.
- **Peek**: `Alt+F12`, view the definition or reference without leaving the current file.

<!--
代码导航是理解和修改大型代码库的关键技能。本页将介绍VS Code提供的强大导航功能。

- **强调效率**：对于后端开发者来说，经常需要在不同的文件、函数、类之间跳转，熟练掌握这些快捷键能极大地提高效率。
- **动手演示**：
  - **Ctrl+P**：演示如何快速打开文件，并结合模糊匹配。
  - **F12 / Ctrl+Click**：在一个Java或Go项目中，演示如何跳转到方法定义、类定义。强调这是最常用的导航方式。
  - **Alt+F12 (Peek Definition)**：演示如何“偷窥”定义，而不用离开当前文件，这在需要快速查看而不打断思路时非常有用。
  - **Ctrl+Shift+O (Go to Symbol in File)**：演示如何快速在当前文件中跳转到某个方法或变量。
  - **Ctrl+T (Go to Symbol in Workspace)**：演示如何跨文件搜索整个工作区中的符号，这对于查找某个接口的所有实现或某个类的所有引用非常有用。
  - **面包屑**：演示如何使用面包屑进行层级导航。
- **课外引申**：
  - 鼓励学员探索 `editor.gotoLocation.multipleDefinitions` 等设置，以自定义跳转行为。
  - 提及 `editor.bracketPairColorization.enabled` 设置，它可以为括号添加颜色，帮助理解代码结构。
-->

---

# 4.4 Edit code: Refactoring

- **Core**: Refactoring is the process of improving the structure of code without changing its external behavior.
- **Supported Operations**:
  - **Extract Method/Variable**: Select code and quickly extract it as a new method or variable.
  - **Rename Symbol**: Rename variables, functions, classes, etc., synchronously in all references.
- **Code Actions**: The light bulb icon that appears in the editor provides quick fixes and refactoring suggestions.
- **Refactor Preview**: Preview all changes before applying a refactor.

<!--
重构是后端开发中保持代码健康、可维护性的重要环节。VS Code提供了强大的重构支持。

- **强调重构的重要性**：解释重构如何帮助改善代码质量，减少技术债务。
- **动手演示**：
  - **提取方法/变量**：在一个Java或Go函数中，选中一段代码，演示如何通过“灯泡”图标或 `Ctrl+.` 快速将其提取为一个新方法或变量。强调命名时的智能提示。
  - **重命名符号**：演示 `F2` 的强大功能，在一个变量名上按 `F2`，然后修改名称，展示所有引用处同步更新的效果。
  - **Code Actions**：演示“灯泡”图标的出现时机，以及如何选择不同的 Code Actions。可以提及 `editor.codeActionsOnSave` 设置，例如配置保存时自动组织导入。
  - **重构预览**：演示在执行复杂重构前，如何通过预览功能查看所有受影响的文件和代码行，确保重构的安全性。
- **课外引申**：
  - 鼓励学员探索更多 Code Actions 的类型，例如“移动文件”、“生成 Getter/Setter”等。
  - 提及一些流行的重构模式，例如 Martin Fowler 的《重构》一书。
-->

---

# 4.5 Edit code: Snippets

- **What are Snippets**: Predefined code templates that allow you to quickly insert commonly used code structures, such as loops, conditionals, function definitions, etc., using simple triggers (prefix).
- **Efficiency Boost**: Reduces repetitive typing, ensures code consistency, and is especially useful for template code common in backend development.
- **Sources**:
  - **Built-in**: Provided by VS Code itself.
  - **Extensions**: Many extensions provide snippets for specific languages or frameworks.
  - **Custom**: The most powerful! You can create your own snippets based on personal or team needs.
- **Custom Snippets**:
  - Create them via `File > Preferences > Configure User Snippets`.
  - Support for placeholders (`$1`, `$2`), default values, variables (`$TM_FILENAME`), and other advanced features.

<!--
Snippets 是提高编码效率的利器，尤其对于后端开发中常见的重复性代码块。

- **强调效率**：Snippets 通过预定义代码模板，极大地减少了重复性输入的工作量，同时也确保了代码的一致性。
- **动手演示**：
  - 演示如何创建一个简单的 Snippet，例如一个 Java 的 `public static void main` 方法的模板，或者一个 Go 的 `func main()` 模板。
  - 演示占位符 (`$1`, `$2`, `$0`) 的用法，以及如何通过 `Tab` 键在占位符之间跳转。
  - 演示 `TM_FILENAME` 等变量的用法，例如在注释中自动插入文件名。
- **团队协作**：提及可以将 Snippets 存储在项目 `.vscode` 文件夹中，以便团队成员共享。
- **课外引申**：
  - 鼓励学员探索 Snippet 的高级语法，例如 `choice` (选择列表) 和 `transform` (变量转换)。
  - 提及如何将 Snippet 绑定到自定义快捷键，实现更快的触发。
-->




---

# 4.6 Edit code: Workspaces

- **What is a Workspace**: A collection of one or more folders opened in VS Code.
- **Single-folder Workspace**: The most common, directly opening a project folder.
- **Multi-root Workspaces**:
  - Defined by a `.code-workspace` file, can contain multiple unrelated project folders.
  - **Scenario**: Microservices architecture, front-end/back-end separation projects, convenient management of all related code in one VS Code window.
- **Workspace Advantages**:
  - **Project-level Configuration**: Independent settings, tasks, debug configurations, does not affect global settings.
  - **UI State Saving**: Remembers opened files, layout, etc.
  - **Extension Enabling/Disabling**: Extensions can be enabled or disabled for specific workspaces.
  - **Team Collaboration**: `.vscode` folder and `.code-workspace` file can be committed to Git to unify the development environment for the team.
- **Workspace Trust**: A security mechanism to ensure safe code execution.

<!--
工作区是VS Code中一个非常重要的概念，尤其对于后端开发者来说，经常会涉及到多模块、多服务的项目。

- **强调“工作区”而非“项目”**：VS Code没有传统IDE中“项目”的概念，而是以“文件夹”为单位。一个工作区可以包含多个文件夹。
- **动手演示多根工作区**：
  - 演示如何通过 `File > Add Folder to Workspace...` 添加多个文件夹到一个工作区。
  - 演示如何保存工作区 (`File > Save Workspace As...`)，生成 `.code-workspace` 文件。
  - 解释 `.code-workspace` 文件中 `folders` 数组的含义，以及如何在其中定义相对路径。
  - 演示工作区设置 (`.vscode/settings.json` 或 `.code-workspace` 文件中的 `settings` 部分) 如何覆盖用户设置，并强调其在团队中统一代码规范的重要性。
- **工作区信任**：简单解释一下 Workspace Trust 的作用，当打开一个新项目时，如果不是自己创建的，会提示是否信任，这是为了安全。
- **课外引申**：
  - 鼓励学员探索如何为多根工作区配置不同的调试启动项和任务。
  - 提及如何利用工作区来管理不同版本的同一个项目，例如 `project-v1.code-workspace` 和 `project-v2.code-workspace`。
-->

---

# 5.1 Build, Debug, Test: Tasks

- **What are Tasks**: A mechanism to automate the running of external tools (like compilers, build tools, test runners) within VS Code.
- **`tasks.json`**: The configuration file for tasks, located in the `.vscode` folder at the workspace root.
- **Core Properties**:
  - `label`: The name of the task.
  - `type`: `shell` (executes shell commands) or `process` (executes processes).
  - `command`: The command to execute.
  - `group`: Task group (like `build`, `test`), for quick running.
  - `presentation`: Controls how the task output is displayed in the terminal.
- **Problem Matchers**:
  - Scans task output and shows errors and warnings in the "Problems" panel and editor.
  - VS Code has built-in problem matchers for various languages (like `$go`, `$tsc`).
- **Compound Tasks**: Chain multiple tasks together using the `dependsOn` property to create complex build workflows.

<!--
任务是VS Code自动化开发流程的核心，对于后端开发尤其重要，因为我们经常需要编译、打包、运行测试。

- **强调自动化**：解释任务如何将命令行操作集成到VS Code中，减少上下文切换，提高效率。
- **动手演示**：
  - **创建自定义任务**：
    - 打开命令面板，搜索 `Tasks: Configure Task`，选择 `Create tasks.json file from template`，然后选择 `Others`。
    - 编写一个简单的 Java 或 Go 编译任务，例如 `javac HelloWorld.java` 或 `go build`。
    - 演示如何运行任务 (`Terminal > Run Task...`)。
  - **问题匹配器**：
    - 在代码中故意引入一个编译错误。
    - 运行编译任务，展示错误如何在“问题”面板中显示，并点击错误跳转到代码行。
    - 解释 `$go` 或 `$tsc` 等内置问题匹配器的作用。
  - **复合任务**：
    - 举例说明微服务场景下，如何用 `dependsOn` 串联多个服务的构建任务。
- **课外引申**：
  - 鼓励学员探索 `tasks.json` 的更多高级配置，例如变量替换 (`${workspaceFolder}`)、平台特定配置 (`windows`, `linux`)。
  - 提及如何将任务绑定到快捷键，实现一键构建或测试。
-->

---

# 5.2 Build, Debug, Test: Debugging

- **Core Debugging Features**:
  - **Breakpoints**: Pause execution at a specific line.
  - **Step Over/Into/Out**: Control the execution flow line by line.
  - **Watch**: Monitor the value of variables and expressions.
  - **Call Stack**: Inspect the function call chain.
  - **Debug Console**: Execute code in the context of the debuggee.
- **`launch.json`**: The configuration file for defining debugging sessions.
- **Zero-configuration Debugging**: For many simple cases (like a single Go file or a Java class with a `main` method), you can start debugging without any configuration (`F5`).
- **Advanced Debugging**:
  - **Conditional Breakpoints**: Break only when a certain condition is met.
  - **Logpoints**: Log a message to the console without pausing execution.
  - **Attach to Process**: Attach the debugger to an already running process.

<!--
调试是解决代码问题不可或缺的工具。VS Code的调试功能非常强大且灵活。

- **强调调试的重要性**：解释调试如何帮助开发者理解代码执行流程，快速定位和解决问题。
- **动手演示**：
  - **设置断点**：在一个Java或Go文件中，点击行号旁边的空白区域设置一个普通断点。
  - **启动调试**：按 `F5` 启动调试会话。展示调试工具栏，并演示“继续”、“单步跳过”、“单步进入”等操作。
  - **查看变量**：在“运行和调试视图”的“变量”部分，展示如何查看变量的值。演示如何将鼠标悬停在代码中的变量上查看其值。
  - **调试控制台**：演示如何在调试控制台中输入表达式并查看结果。
  - **条件断点**：演示如何设置一个条件断点，例如当某个变量达到特定值时才触发。
  - **日志点**：演示如何设置日志点，这在不修改代码的情况下进行日志输出非常有用。
- **`launch.json`**：简单介绍 `launch.json` 的作用，它是定义调试会话的关键。对于Java和Go，通常由对应的扩展自动生成或提供模板。
- **课外引申**：
  - 鼓励学员探索更多调试功能，例如异常断点、函数断点、远程调试等。
  - 提及如何利用 GitHub Copilot 来帮助生成 `launch.json` 配置。
-->

---

# 5.3 Build, Debug, Test: Testing

- **Test Explorer**: A dedicated view in the Activity Bar for discovering, running, and managing tests.
- **Test Framework Integration**: Extensions provide rich integration with popular testing frameworks like JUnit for Java and the built-in `testing` package for Go.
- **Running and Debugging Tests**:
  - Run or debug individual tests, test suites, or all tests directly from the Test Explorer or from CodeLens annotations in the editor.
- **Viewing Test Results**: Test results are displayed directly in the Test Explorer and in the editor with detailed error messages and output.
- **Test Coverage**: Some extensions can display test coverage information, highlighting which lines of code are covered by tests.

<!--
测试是保证代码质量的重要环节。VS Code的测试集成让测试变得更加便捷。

- **强调测试的重要性**：解释测试如何帮助开发者确保代码的正确性，减少Bug。
- **动手演示**：
  - **安装测试扩展**：以 Java 为例，确保安装了 `Test Runner for Java`。对于 Go，Go 扩展本身就包含了测试支持。
  - **发现测试**：打开 Test Explorer，展示它如何自动发现项目中的测试用例。
  - **运行测试**：演示如何点击 Test Explorer 中的“播放”按钮运行所有测试，或点击单个测试旁边的播放按钮运行特定测试。
  - **调试测试**：演示如何设置断点，然后调试一个测试用例，展示调试流程与普通代码调试类似。
  - **测试覆盖率**：如果环境允许，可以简单演示测试覆盖率的显示效果，例如编辑器行号旁边的颜色标记。
- **AI 辅助**：提及 Copilot 在测试方面的帮助，例如生成测试用例的骨架，或者在测试失败时提供修复建议。
- **课外引申**：
  - 鼓励学员探索不同语言的测试框架（如 Java 的 JUnit/TestNG，Go 的 `go test`）。
  - 提及如何将测试任务集成到 `tasks.json` 中，实现自动化测试。
-->

---

# 6.1 GitHub Copilot: Overview

- **Your AI Pair Programmer**: An AI-powered tool that helps you write code faster and with less work.
- **Core Capabilities**:
  - **Code Completion**: Suggests single lines or entire functions as you type.
  - **Code Generation**: Generates code from natural language comments.
  - **Answering Questions**: Provides answers to coding questions directly in the editor.
  - **Explaining and Fixing Code**: Explains complex code snippets and suggests fixes for bugs.
- **Powered by OpenAI Codex**: Trained on a massive dataset of natural language and public source code.
- **Integration**: Deeply integrated into VS Code, available as an extension.

<!--
GitHub Copilot 是近年来最受关注的开发工具之一，它极大地改变了开发者的工作方式。本页将介绍其核心功能。

- **强调“AI 结对编程”**：解释 Copilot 不仅仅是代码补全，更像是一个智能的伙伴，可以帮助你思考、生成代码、甚至解决问题。
- **动手演示**：
  - **代码补全**：在一个 Java 或 Go 文件中，演示 Copilot 如何根据你输入的注释或函数签名，自动生成代码。例如，输入 `// function to calculate factorial`，看它如何生成阶乘函数。
  - **自然语言聊天**：打开 Copilot Chat 视图，演示如何提问（例如“解释这段代码的作用”），或者让它生成测试用例。
  - **智能操作**：简单提及智能操作，例如在代码中出现错误时，Copilot 可能会提供快速修复建议。
- **自主编码**：简单介绍这个概念，但强调这通常需要更深入的配置和理解，可以作为课外引申。
- **课外引申**：
  - 鼓励学员了解 Copilot 的定价模式（通常有免费试用和付费订阅）。
  - 提及 Copilot 可以通过自定义指令来适应你的编码风格和项目规范。
-->

---

# 6.2 GitHub Copilot: Customize Copilot

- **Core**: Customize instructions and prompt files to make Copilot's generated content better align with your coding standards and project requirements.
- **Custom Instructions**:
  - Define general coding guidelines, technology stack preferences, or project requirements.
  - Can be stored in `.github/copilot-instructions.md` file, automatically applied to all chat requests.
  - Examples: naming conventions, error handling approaches, code style, etc.
- **Prompt Files**:
  - Reusable prompt templates for common tasks, such as code generation and code reviews.
  - Markdown format, can include metadata (such as `mode`, `model`, `tools`).
  - Examples: generating specific components, performing security reviews, etc.
- **Advantages**: Avoid repetitive context input, ensure consistency and high quality of AI-generated content.

<!--
本页是关于如何“驯服”Copilot，让它更好地服务于你的开发工作。

- **强调定制的重要性**：解释为什么需要定制 Copilot，例如统一团队的代码风格，或者让它专注于特定领域的代码生成。
- **动手演示**：
  - **自定义指令**：
    - 简单展示 `.github/copilot-instructions.md` 文件的内容，例如定义 PascalCase 命名约定。
    - 演示在 Copilot Chat 中提问时，Copilot 如何自动遵循这些指令。
  - **提示文件**：
    - 简单展示一个 `.prompt.md` 文件的结构，例如一个用于生成 Spring Boot Controller 的模板。
    - 演示如何在 Copilot Chat 中通过 `/` 命令快速调用提示文件。
- **最佳实践**：
  - 建议将自定义指令和提示文件纳入版本控制，以便团队共享和维护。
  - 鼓励学员思考自己的日常工作中，哪些重复性任务可以通过定制 Copilot 来自动化。
- **课外引申**：
  - 提及 Copilot 还可以通过自定义聊天模式和扩展工具来进一步增强。
  - 鼓励学员探索 Copilot 的设置，例如 `github.copilot.chat.codeGeneration.instructions`。
-->

---

# 6.3 GitHub Copilot: Language Models

- **Model Selection**: Copilot provides multiple built-in language models optimized for different tasks (e.g., speed, reasoning capabilities).
- **Bring Your Own Model**:
  - You can use your own API key to connect to models from providers like Anthropic, Azure, Google, OpenAI, etc.
  - **Advantages**: More model choices, experimenting with new models, local computation, more granular control.
- **Switching Models**:
  - **Chat**: Switch through the model selector in the chat input field.
  - **Code Completion**: Switch through `Configure Code Completions...` in the Copilot menu.
- **Considerations**:
  - The bring-your-own-model feature is currently in preview and not applicable to Copilot Business/Enterprise users.
  - Different models may have different capabilities and may not be suitable for all Copilot features.

<!--
这一页是关于 Copilot 的高级定制，特别是如何选择和管理其底层语言模型。

- **强调模型多样性**：解释不同的模型有不同的侧重点，例如有些模型擅长快速生成代码，有些则擅长复杂的逻辑推理。
- **介绍“自带模型”**：
  - 解释为什么开发者可能需要使用自己的 API Key 来接入外部模型，例如为了使用最新的模型，或者为了满足特定的合规性要求。
  - 简单演示如何在 Copilot Chat 中切换模型。
- **注意事项**：强调“自带模型”功能的限制和注意事项，特别是对于企业用户。
- **课外引申**：
  - 鼓励学员关注 AI 领域的发展，了解不同语言模型的特点和优势。
  - 讨论如何根据具体的开发任务选择最合适的语言模型。
-->

---

# 6.4 GitHub Copilot: Tips & Tricks

## Optimize Your Development Experience

- **Choose the Right Copilot Tool**: Select code completion, chat, edit, or Agent mode based on your task.
- **Personalize Copilot**: Use instruction files (`.instructions.md`) to customize Copilot behavior to match team coding standards.
- **Effective Prompt Engineering**: Learn how to write high-quality prompts, provide context, and iteratively optimize.
- **Workspace Indexing**: Utilize workspace indexing (local or remote) to improve Copilot's understanding of the codebase.
- **Choose AI Models**: Select appropriate AI models based on task requirements (fast coding or reasoning).
- **Reusable Prompts**: Create and share prompt files (`.prompt.md`) to enable prompt reuse.

<!--
本Slide将介绍如何最大化利用GitHub Copilot在VS Code中的功能。
1. **选择合适的Copilot工具**: 强调根据不同的开发场景（如快速编码、代码重构、问题解答、高层需求实现）选择最适合的Copilot工具，例如：
    - **代码补全**: 适用于日常编码，提供行内建议。
    - **聊天模式**: 用于头脑风暴、获取代码建议，可选择特定领域参与者。
    - **编辑模式**: 通过自然语言启动代码编辑会话，自动应用大规模代码更改。
    - **Agent模式**: 实现高层需求，Copilot自主调用工具规划和实现代码更改。
2. **个性化Copilot**: 解释如何通过创建`.instructions.md`文件来为Copilot提供额外的上下文，使其生成的代码更符合团队的编码实践、工具使用和项目特定要求。例如，可以指定缩进风格、命名约定、测试框架等。
3. **有效的Prompt工程**: 强调Prompt的质量直接影响Copilot响应的准确性。提供编写有效Prompt的技巧：
    - 从通用到具体：逐步细化需求。
    - 提供示例：通过输入输出示例指导Copilot。
    - 任务分解：将复杂任务拆解为简单子任务。
    - 提供上下文：利用`#codebase`、`#fetch`、`#githubRepo`等工具或直接拖拽文件、文件夹、符号来丰富Prompt的上下文。
    - 保持聊天历史相关性：及时清理不相关的历史记录或开启新会话。
4. **工作区索引**: 解释工作区索引（本地或远程）如何帮助Copilot快速准确地搜索代码库，从而提供更准确的答案。特别是对于大型GitHub仓库，远程索引可以显著提升搜索速度。
5. **选择AI模型**: 介绍Copilot提供不同AI模型，并说明如何根据任务类型（如快速编码任务的GPT-4o、Claude Sonnet 3.5/3.7、Gemini 2.0 Flash，或推理/规划任务的Claude Sonnet 3.7 Thinking、o1、o3-mini）选择最合适的模型。
6. **可复用Prompt**: 介绍如何创建`.prompt.md`文件来保存特定任务的Prompt及其上下文和指令，从而实现Prompt的复用，并可以在团队内共享。
引导学员自学：鼓励学员深入阅读相关文档，特别是关于Prompt工程和个性化设置的部分，尝试不同的Copilot工具和模型，并在实际项目中应用这些技巧。
-->

---

# 6.5 GitHub Copilot: Frequently Asked Questions (FAQ)

## Resolve Your Questions

- **Subscription & Usage**: How to get Copilot subscription, monitor usage, and handle usage limits.
- **General Issues**: How to remove Copilot from VS Code, network and firewall configuration, and rate limiting.
- **Code Completion & Chat**: Enable/disable code completion and chat feature troubleshooting.
- **Troubleshooting & Feedback**: How to provide feedback, view logs, and use Chat Debug view.

<!--
本Slide将概述VS Code中强大的源代码管理（SCM）功能，特别是其对Git的深度集成。
1. **内置Git支持**: 强调VS Code开箱即用地支持Git，无需额外安装插件即可进行基本的版本控制操作。同时提及可以通过扩展市场安装其他SCM提供商的插件。
2. **SCM视图**: 介绍VS Code侧边栏的“源代码管理”视图（SCM视图），它是进行版本控制操作的主要界面。学员可以通过该视图直观地查看文件变更、暂存区状态、合并冲突等。
3. **Git操作**: 详细说明VS Code支持的Git操作，包括：
    - **克隆仓库**: 从远程仓库克隆代码到本地。
    - **初始化仓库**: 将本地文件夹初始化为Git仓库。
    - **提交**: 暂存（stage）和提交（commit）代码变更，并提及如何配置Git用户信息。
    - **分支管理**: 创建、切换分支，以及如何利用`scm.workingSets.enabled`设置在分支切换时保存和恢复编辑器状态。
    - **远程操作**: 拉取（pull）、推送（push）、同步（sync）远程分支，以及如何配置凭据助手和`git.autofetch`设置。
4. **AI辅助**: 突出GitHub Copilot在版本控制中的应用，例如生成提交信息和辅助代码审查，提升开发效率。
5. **可视化工具**: 介绍VS Code提供的多种可视化工具，帮助开发者更好地理解和管理代码变更：
    - **Git blame信息**: 在编辑器中显示代码行是由谁在何时修改的。
    - **3-way合并编辑器**: 交互式地解决合并冲突，支持接受传入、当前或组合更改。
    - **Diff视图**: 直观地比较文件差异，支持行内暂存或回滚。
    - **Timeline视图**: 显示文件的历史事件，如Git提交记录。
6. **多SCM提供商**: 提及VS Code支持同时管理多个源代码管理提供商，例如Git和Azure DevOps Server，并通过“Source Control Repositories”视图进行切换和管理。
引导学员自学：鼓励学员深入学习Git的基本概念和命令，并结合VS Code的SCM功能进行实践。特别是对于合并冲突的解决和Diff视图的使用，可以通过实际操作来加深理解。同时，可以探索VS Code市场中更多的SCM扩展，以满足特定项目或团队的需求。
-->

---

---
layout: center
---

# 7. Source Control

## Version Control: The Core of Code Collaboration

---

# 7.1 Source Control: Overview

## Git Integration and Version Control in VS Code

- **Built-in Git Support**: VS Code natively integrates Git, providing powerful version control features.
- **SCM View**: Intuitively manage code changes, staging, commits, and other operations through the SCM view in the sidebar.
- **Git Operations**: Support for cloning, initializing repositories, committing, branch management, and remote operations (pull, push, sync).
- **AI Assistance**: GitHub Copilot can assist with generating commit messages and code reviews.
- **Visualization Tools**: Provides Git blame information, 3-way merge editor, Diff view, and Timeline view.
- **Multiple SCM Providers**: Support for managing multiple version control systems simultaneously.

<!--
本Slide将概述VS Code中强大的源代码管理（SCM）功能，特别是其对Git的深度集成。
1. **内置Git支持**: 强调VS Code开箱即用地支持Git，无需额外安装插件即可进行基本的版本控制操作。同时提及可以通过扩展市场安装其他SCM提供商的插件。
2. **SCM视图**: 介绍VS Code侧边栏的“源代码管理”视图（SCM视图），它是进行版本控制操作的主要界面。学员可以通过该视图直观地查看文件变更、暂存区状态、合并冲突等。
3. **Git操作**: 详细说明VS Code支持的Git操作，包括：
    - **克隆仓库**: 从远程仓库克隆代码到本地。
    - **初始化仓库**: 将本地文件夹初始化为Git仓库。
    - **提交**: 暂存（stage）和提交（commit）代码变更，并提及如何配置Git用户信息。
    - **分支管理**: 创建、切换分支，以及如何利用`scm.workingSets.enabled`设置在分支切换时保存和恢复编辑器状态。
    - **远程操作**: 拉取（pull）、推送（push）、同步（sync）远程分支，以及如何配置凭据助手和`git.autofetch`设置。
4. **AI辅助**: 突出GitHub Copilot在版本控制中的应用，例如生成提交信息和辅助代码审查，提升开发效率。
5. **可视化工具**: 介绍VS Code提供的多种可视化工具，帮助开发者更好地理解和管理代码变更：
    - **Git blame信息**: 在编辑器中显示代码行是由谁在何时修改的。
    - **3-way合并编辑器**: 交互式地解决合并冲突，支持接受传入、当前或组合更改。
    - **Diff视图**: 直观地比较文件差异，支持行内暂存或回滚。
    - **Timeline视图**: 显示文件的历史事件，如Git提交记录。
    - **多SCM提供商**: 提及VS Code支持同时管理多个源代码管理提供商，例如Git和Azure DevOps Server，并通过“Source Control Repositories”视图进行切换和管理。
引导学员自学：鼓励学员深入学习Git的基本概念和命令，并结合VS Code的SCM功能进行实践。特别是对于合并冲突的解决和Diff视图的使用，可以通过实际操作来加深理解。同时，可以探索VS Code市场中更多的SCM扩展，以满足特定项目或团队的需求。
-->

---


---

# 7.2 Source Control: Git Basics

## Effortlessly Master Git in VS Code

- **Git Environment Setup**: Ensure Git is installed and configure GitHub account in VS Code.
- **Getting Code**: Support for cloning remote repositories, initializing local repositories, publishing to GitHub, and remote work through GitHub Codespaces and Remote Repositories.
- **Managing Code Changes**: Stage, commit, push, and pull changes, with Copilot assistance for generating commit messages and code reviews.
- **Branch Management**: Create, switch, and publish branches, with PR management through GitHub Pull Requests and Issues extension.
- **Integrated Terminal**: Use Git commands in VS Code's built-in terminal, with Git Bash support.

<!--
本Slide将解答关于VS Code中Git和GitHub使用的常见问题，帮助学员解决实际操作中可能遇到的困惑。
1. **Git操作**: 涵盖了日常Git操作中常见的疑问，例如：
    - **撤销提交**: 使用`Git: Undo Last Commit`命令。
    - **重命名本地分支**: 使用`Git: Rename Branch…`命令。
    - **撤销暂存**: 通过SCM视图中的`-`图标或拖拽来取消暂存。
    - **修改最近提交信息**: 使用`Git: Commit Staged (Amend)`命令。
2. **远程仓库问题**: 解释当推送、拉取或同步操作灰显或无法完成时，通常是由于未设置Git origin（需要手动添加远程仓库URL并推送）或凭据管理配置不当（建议设置凭据助手或禁用`git.autofetch`）。
3. **认证与安全**: 讨论Git认证弹窗的出现原因（通常是`git.autofetch`导致，可通过凭据助手解决），以及如何使用Git Credential Manager (GCM) 来处理Azure DevOps组织的多因素认证。同时，会解释Git 2.35.2版本引入的“潜在不安全仓库”警告，以及如何通过`Manage Unsafe Repositories`命令将其标记为安全。
4. **仓库发现**: 解释VS Code如何发现Git仓库，以及为什么有时父文件夹中的Git仓库未被自动发现（这是为了避免混淆和数据丢失），并说明如何通过`git.openRepositoryInParentFolders`设置来调整此行为。
5. **SSH与GitHub Enterprise**: 确认VS Code支持SSH Git认证（对于带密码的SSH密钥，建议从Git Bash启动VS Code）和GitHub Enterprise Server的认证。
引导学员自学：鼓励学员在遇到Git相关问题时，首先查阅VS Code的官方文档和Git的官方文档，学会利用搜索引擎和社区资源解决问题。对于复杂的Git操作，可以尝试在命令行中执行，以便更好地理解其底层原理。
-->

---

---

# Source Control: Frequently Asked Questions (FAQ)

## Resolve Common Confusions in Git & GitHub Usage

- **Git Operations**: How to undo commits, rename branches, unstage changes, and modify recent commit messages.
- **Remote Repository Issues**: Resolve grayed-out or failed push/pull/sync operations, such as unset Git origin or credential management.
- **Authentication & Security**: Handle Git authentication popups, multi-factor authentication (MFA), and potentially unsafe repository warnings.
- **Repository Discovery**: Explain how VS Code discovers Git repositories and why repositories in parent folders may not be discovered, with configuration settings.
- **SSH & GitHub Enterprise**: Support for SSH Git authentication and GitHub Enterprise.

<!--
本Slide将解答关于VS Code中Git和GitHub使用的常见问题，帮助学员解决实际操作中可能遇到的困惑。
1. **Git操作**: 涵盖了日常Git操作中常见的疑问，例如：
    - **撤销提交**: 使用`Git: Undo Last Commit`命令。
    - **重命名本地分支**: 使用`Git: Rename Branch…`命令。
    - **撤销暂存**: 通过SCM视图中的`-`图标或拖拽来取消暂存。
    - **修改最近提交信息**: 使用`Git: Commit Staged (Amend)`命令。
2. **远程仓库问题**: 解释当推送、拉取或同步操作灰显或无法完成时，通常是由于未设置Git origin（需要手动添加远程仓库URL并推送）或凭据管理配置不当（建议设置凭据助手或禁用`git.autofetch`）。
3. **认证与安全**: 讨论Git认证弹窗的出现原因（通常是`git.autofetch`导致，可通过凭据助手解决），以及如何使用Git Credential Manager (GCM) 来处理Azure DevOps组织的多因素认证。同时，会解释Git 2.35.2版本引入的“潜在不安全仓库”警告，以及如何通过`Manage Unsafe Repositories`命令将其标记为安全。
4. **仓库发现**: 解释VS Code如何发现Git仓库，以及为什么有时父文件夹中的Git仓库未被自动发现（这是为了避免混淆和数据丢失），并说明如何通过`git.openRepositoryInParentFolders`设置来调整此行为。
5. **SSH与GitHub Enterprise**: 确认VS Code支持SSH Git认证（对于带密码的SSH密钥，建议从Git Bash启动VS Code）和GitHub Enterprise Server的认证。
引导学员自学：鼓励学员在遇到Git相关问题时，首先查阅VS Code的官方文档和Git的官方文档，学会利用搜索引擎和社区资源解决问题。对于复杂的Git操作，可以尝试在命令行中执行，以便更好地理解其底层原理。
-->


---
layout: center
---

# 8. Terminal

## A Powerful Tool for Command Line Interaction

---

# 8.1 Terminal: Getting Started

## Running Your First Command in VS Code

- **Integrated Terminal**: VS Code has a built-in fully-featured terminal that can run shell commands directly.
- **Multiple Shell Support**: Supports Bash, Zsh, PowerShell, and other shells.
- **Basic Operations**: Open terminal, run commands (like `ls`), interact with command output (click links to open files).
- **Command History**: Quickly navigate and re-run historical commands.
- **Multiple Terminal Management**: Support for opening multiple terminals simultaneously and switching between different shells.
- **Terminal Layout**: Terminals can be dragged to the editor area for flexible layout.

<!--
本Slide将引导学员如何在VS Code中开始使用集成终端，从基本操作到高级管理。
1. **集成终端**: 强调VS Code内置的终端是一个功能齐全的工具，可以直接在编辑器内运行各种Shell命令，如`echo`, `ls`, `git`等，无需切换到外部终端。
2. **多种Shell支持**: 介绍VS Code终端支持多种Shell，如Bash, Zsh, PowerShell等，并会根据操作系统配置自动选择默认Shell。学员可以根据自己的偏好选择和切换Shell。
3. **基本操作**: 详细说明如何开始使用终端：
    - **打开终端**: 通过菜单栏`View > Terminal`或快捷键`kb(workbench.action.terminal.toggleTerminal)`。
    - **运行命令**: 在终端中输入命令并执行，例如`ls`来列出当前目录文件。
    - **与命令输出交互**: 强调终端输出中的文件路径或URL是可点击的链接，可以直接在编辑器中打开文件或在浏览器中打开URL，这对于处理编译错误或日志非常有用。
    - **命令历史**: 介绍如何通过快捷键`kb(workbench.action.terminal.scrollToPreviousCommand)`和`kb(workbench.action.terminal.scrollToNextCommand)`在命令历史中导航，以及如何通过点击图标重新运行之前的命令。
    - **多终端管理**: 解释终端支持同时开启多个实例，每个实例可以使用不同的Shell，方便开发者同时进行不同任务（如一个用于Git命令，一个用于构建脚本）。同时，可以方便地在不同终端之间切换、重命名和关闭。
    - **终端布局**: 提及终端可以被拖拽到编辑器区域，像其他编辑器标签页一样进行布局，甚至可以拖出VS Code窗口成为浮动窗口，提供灵活的工作空间。
引导学员自学：鼓励学员在日常开发中多使用VS Code的集成终端，熟悉各种快捷键和命令。可以尝试配置不同的Shell配置文件，并探索终端的更多高级功能，如任务自动化、自定义快捷键等。
-->

---

# 8.2 Terminal: Fundamentals

## Deep Dive into VS Code Integrated Terminal

- **Opening & Switching**: Multiple ways to open terminal, support for switching between different shells.
- **Terminal Management**: Create, close, group (split) terminals, support for drag-and-drop layout adjustment.
- **Buffer Navigation**: Quick scrolling through terminal output, support for command navigation.
- **Link Detection**: Intelligently recognize file, URL, and folder links, support for extension-contributed link handlers.
- **Copy & Paste**: Follow platform standards, support for selection-based copying and multi-line paste warnings.
- **Mouse Operations**: Right-click behavior configuration, column selection, Alt key cursor movement, mouse event modes.
- **Find & Run**: Find text within terminal, run selected code or current line.
- **Advanced Features**: Terminal maximization, select all, drag-and-drop file paths, task automation for terminal startup, working directory configuration, fixed-size terminals.
- **AI Assistance**: GitHub Copilot applications in terminal, including inline chat and chat participants.

<!--
本Slide将深入探讨VS Code集成终端的各项基础功能和高级特性。
1. **打开与切换**: 再次强调打开终端的多种方式（菜单、命令面板、快捷键），并介绍如何选择和切换不同的Shell配置文件。
2. **终端管理**: 详细说明如何管理多个终端实例，包括：
    - **创建与关闭**: 通过`+`图标、垃圾桶图标或命令来创建和关闭终端。
    - **分组（分屏）**: 如何将终端进行水平或垂直分屏，方便同时查看多个终端输出。
    - **拖拽调整布局**: 终端可以像编辑器标签页一样拖拽到编辑器区域，实现灵活的布局。
3. **缓冲区导航**: 介绍如何在终端缓冲区中进行导航，包括逐行、逐页滚动，以及滚动到顶部或底部。特别提及了Shell集成后的命令导航功能。
4. **链接检测**: 详细说明终端如何智能识别并处理不同类型的链接（URI/URL、文件、文件夹、单词链接），以及扩展如何贡献自定义链接处理器。强调了`Ctrl/Cmd`键点击链接的行为。
5. **复制与粘贴**: 介绍终端的复制粘贴行为，遵循平台标准，并提及`copyOnSelection`设置和多行粘贴警告。
6. **鼠标操作**: 解释鼠标右键在不同平台下的默认行为，以及如何通过`terminal.integrated.rightClickBehavior`设置进行自定义。同时介绍了列选择、Alt键移动光标和鼠标事件模式。
7. **查找与运行**: 介绍终端内置的查找功能，以及如何运行编辑器中选中的文本或当前行到终端。
8. **高级功能**: 简要提及一些高级特性，如终端最大化、全选、拖放文件路径到终端、通过Tasks自动化终端启动、工作目录配置、固定尺寸终端等。
9. **AI辅助**: 突出GitHub Copilot在终端中的应用，包括：
    - **终端行内聊天**: 直接在终端中与Copilot交互，获取Shell命令建议和解释。
    - **终端聊天参与者**: 在Chat视图中使用`@terminal`参与者进行更复杂的终端相关查询。
    - **引用终端上下文**: 在聊天Prompt中引用终端选中内容或最后一条命令。
引导学员自学：鼓励学员深入探索终端的各项设置，根据自己的使用习惯进行个性化配置。特别是对于Shell集成、链接处理和AI辅助功能，可以通过实际操作来体验其便利性。同时，可以查阅VS Code的Tasks文档，学习如何自动化终端操作。
-->

---

# 8.3 Terminal: Terminal Profiles

## Customize Your Shell Environment

- **What are Terminal Profiles**: Platform-specific shell configurations including executable paths, arguments, and custom settings.
- **Configuration & Customization**: Automatically detect and allow customization of existing profiles, or create new profiles.
- **Profile Parameters**: Support for `path`, `source`, `overrideName`, `env`, `icon`, `color`, and other parameters.
- **Default Profile**: Set default profile through `terminal.integrated.defaultProfile.*` setting.
- **Remove Built-in Profiles**: Set profile name to `null` to remove.
- **Task/Debug Dedicated Profiles**: Use `terminal.integrated.automationProfile.<platform>` to configure dedicated shells for tasks and debugging.
- **Shortcut Launch**: Launch specific profiles through keyboard shortcuts.
- **Unsafe Profile Detection**: Warn about shells installed in unsafe paths.
- **Common Shell Configurations**: Provide configuration examples for Cmder, Cygwin, Git Bash, MSYS2, Windows PowerShell, WSL, and other shells.

<!--
本Slide将详细介绍VS Code中终端配置文件的概念、如何配置和管理它们，以及一些常见Shell的配置示例。
1. **什么是终端配置文件**: 解释终端配置文件是平台特定的Shell配置，它包含了Shell的可执行路径、启动参数以及其他自定义设置。VS Code会自动检测一些默认的Shell配置文件。
2. **配置与自定义**: 介绍如何通过`Terminal: Select Default Profile`命令来配置默认配置文件，以及如何基于现有Shell创建新的自定义配置文件。强调配置文件可以通过`settings.json`文件手动编辑。
3. **配置文件参数**: 详细说明配置文件中支持的各种参数：
    - `path`: Shell可执行文件的路径。
    - `source`: 仅Windows可用，用于让VS Code检测PowerShell或Git Bash的安装。
    - `args`: 传递给Shell的参数。
    - `overrideName`: 是否覆盖动态终端标题。
    - `env`: 定义环境变量，可设置为`null`来删除环境变量。
    - `icon`和`color`: 用于自定义终端图标和颜色。
    - 强调这些参数都支持变量解析。
4. **默认配置文件**: 解释如何通过`terminal.integrated.defaultProfile.*`设置来手动指定默认的终端配置文件。
5. **移除内置配置文件**: 介绍如何通过将配置文件名设置为`null`来移除VS Code自动检测到的内置配置文件，使其不再显示在终端下拉列表中。
6. **任务/调试专用配置文件**: 介绍`terminal.integrated.automationProfile.<platform>`设置，允许为任务和调试功能配置一个独立的Shell配置文件，避免与默认配置文件冲突。
7. **快捷键启动**: 演示如何通过自定义键盘快捷键来直接启动特定的终端配置文件，提升工作效率。
8. **不安全配置文件检测**: 解释VS Code会检测安装在不安全路径（如可被其他用户写入的路径）的Shell，并在配置时发出警告，以提高安全性。
9. **常见Shell配置**: 提供了一些常见Shell（如Cmder、Cygwin、Git Bash、MSYS2、Windows PowerShell、WSL）的配置示例，帮助学员快速上手。
引导学员自学：鼓励学员根据自己的开发环境和习惯，尝试自定义终端配置文件。特别是对于经常使用的Shell，可以配置启动参数、环境变量等，以优化开发体验。同时，可以深入了解VS Code的变量引用文档，以便在配置文件中更灵活地使用变量。
-->

---

# 8.4 Terminal: Shell Integration

## Enhance Terminal Intelligence and Interactivity

- **Core Features**: Enhance terminal's understanding of internal shell events, enabling working directory detection, command detection, decoration, and navigation.
- **Installation Methods**: Support for automatic script injection (default) and manual installation, covering multiple shells (bash, fish, pwsh, zsh, Git Bash).
- **Integration Quality**: Provides "None", "Rich", and "Basic" integration quality levels, affecting feature completeness.
- **Command Decoration & Navigation**: Display decorations based on command execution results, support command navigation and output selection.
- **Command Guide & Sticky Scroll**: Hover to display command guide, sticky scroll to pin commands, improving readability.
- **Quick Fix**: Intelligently recognize command output, provide context-relevant quick fix suggestions.
- **Recent Commands & Directories**: Quickly run recent commands, quickly switch to recently accessed directories.
- **Working Directory Detection**: Improve link resolution accuracy, and display current directory in terminal tabs.
- **Enhanced PowerShell Shortcuts**: Resolve PowerShell shortcut compatibility issues in VS Code terminal.
- **Enhanced Accessibility**: Improve terminal accessibility, such as audio prompts when commands fail.
- **IntelliSense (Preview)**: Provide intelligent suggestions for files, folders, commands, and parameters in terminal.
- **Supported Escape Sequences**: Introduce VS Code custom and supported Shell integration escape sequences.

<!--
本Slide将深入讲解VS Code终端的Shell集成功能，以及它如何提升终端的智能性和用户体验。
1. **核心功能**: 解释Shell集成如何让VS Code终端更深入地理解Shell内部的事件，从而实现更高级的功能，如准确的工作目录检测、命令执行状态的识别、命令装饰和导航等。
2. **安装方式**: 介绍Shell集成的两种安装方式：
    - **自动脚本注入**: 默认情况下，VS Code会自动为支持的Shell注入集成脚本。这是最简单的方式。
    - **手动安装**: 对于一些特殊情况（如子Shell、SSH会话、复杂Shell设置），需要手动将集成脚本添加到Shell的初始化文件中。提供了bash、fish、pwsh、zsh、Git Bash的配置示例。
3. **集成质量**: 解释Shell集成有不同的“质量”等级（None, Rich, Basic），这些等级决定了集成功能的完整性。学员可以通过悬停终端标签页来查看当前的集成质量。
4. **命令装饰与导航**: 详细说明Shell集成如何根据命令的退出码在行左侧显示成功或失败的装饰，并在滚动条的概览标尺中显示。这些装饰是可交互的，可以重新运行命令。同时，Shell集成也增强了命令导航功能，使得在命令历史中跳转和选择输出更加可靠。
5. **命令指南与粘性滚动**: 介绍“命令指南”功能，它在命令和输出旁边显示一个垂直条，帮助快速识别命令边界。以及“粘性滚动”功能，它将部分显示的命令“粘”在终端顶部，方便查看长输出所属的命令。
6. **快速修复**: 突出Shell集成的一项智能功能——快速修复。它能扫描命令输出，并根据上下文提供高相关性的操作建议，例如端口占用时建议杀死进程、Git推送失败时建议设置上游等。
7. **最近命令与目录**: 介绍`Terminal: Run Recent Command`和`Terminal: Go to Recent Directory`命令，它们利用Shell集成提供的历史信息，实现快速搜索和执行历史历史命令，以及快速切换最近访问的目录。
8. **工作目录检测**: 解释Shell集成如何准确地告诉VS Code当前Shell的工作目录，这对于终端中链接的解析（如`package.json`）和终端标签页显示当前目录非常重要。
9. **增强的PowerShell快捷键**: 提及Shell集成解决了PowerShell在VS Code终端中一些快捷键（如`Ctrl+Space`）的兼容性问题，使其行为更符合预期。
10. **增强可访问性**: 强调Shell集成如何提升终端的可访问性，例如通过检测到的命令进行导航，以及命令失败时的音频提示。
11. **IntelliSense (预览)**: 介绍终端中的IntelliSense功能，它利用Shell集成提供文件、文件夹、命令和参数的智能提示，极大地提升了命令行输入的效率。
12. **支持的转义序列**: 简要提及VS Code自定义和支持的Shell集成转义序列，这些是实现上述功能的基础。
引导学员自学：鼓励学员尝试手动安装Shell集成，并深入了解其工作原理。可以探索快速修复功能，并尝试自定义快捷键来提升终端操作效率。对于IntelliSense功能，可以尝试在不同Shell中体验其智能提示效果。
-->

---

# 8.5 Terminal: Appearance

## Personalize Your Terminal Interface

- **Text Styling**: Font, font size, letter spacing, line height, font weight, ligatures, etc.
- **Cursor Styling**: Cursor shape, width, blinking behavior.
- **Custom Tabs**: Tab visibility, text content (with variable support), icons, status animations.
- **Visual Hints**: Enable and duration settings for visual bell notifications.
- **Terminal Colors**: ANSI color configuration, minimum contrast settings.
- **Ligatures**: Enable font ligatures, support for font feature settings and fallback ligatures.
- **GPU Acceleration**: WebGL renderer for enhanced performance, support for custom glyphs and blurry width glyph scaling.
- **Custom Prompt**: Recommended tools like Starship and oh-my-posh for beautifying Shell Prompt.

<!--
本Slide将详细介绍VS Code终端的外观定制选项，帮助学员打造个性化的终端界面。
1. **文本样式**: 涵盖了终端文本的各种样式设置，包括字体家族（`fontFamily`）、字体大小（`fontSize`）、字间距（`letterSpacing`）、行高（`lineHeight`）、字重（`fontWeight`、`fontWeightBold`）以及字体连字（`fontLigatures`）等。强调了Powerline和Nerd Fonts的使用，以及VS Code对部分Powerline符号的内置支持。
2. **光标样式**: 介绍了如何自定义终端光标的形状（`cursorStyle`）、宽度（`cursorWidth`）和闪烁行为（`cursorBlinking`），以及非活动光标的样式。
3. **自定义标签页**: 详细说明了终端标签页的各种定制选项，包括：
    - **可见性**: 控制标签页何时显示（`hideCondition`）、是否显示活动终端名称（`showActiveTerminal`）、操作按钮（`showActions`）以及标签页位置（`location`）。
    - **文本内容**: 自定义标签页的标题（`title`）、描述（`description`）和分隔符（`separator`），并列举了可用的变量，如`${cwd}`、`${process}`等。
    - **图标**: 如何通过终端配置文件设置标签页图标，以及默认图标和颜色。
    - **状态动画**: 控制标签页状态图标的动画效果。
4. **视觉提示**: 介绍了当终端响铃时，如何通过`enableBell`和`bellDuration`设置来控制黄色响铃图标的显示和持续时间。
5. **终端颜色**: 解释了终端如何处理ANSI颜色，以及如何通过`workbench.colorCustomizations`设置独立于主题配置颜色。强调了`drawBoldTextInBrightColors`设置和最小对比度（`minimumContrastRatio`）功能，后者旨在解决颜色对比度问题，确保文本可读性。
6. **连字（Ligatures）**: 详细介绍了如何启用字体连字，以及如何通过`fontFeatureSettings`进行更细粒度的控制。提及了回退连字（`fallbackLigatures`）功能，用于手动指定字符序列以形成连字。
7. **GPU加速**: 解释了终端的两种渲染器（WebGL和DOM），以及默认启用的GPU加速如何提升性能。强调了GPU加速下对自定义字形（如Powerline符号、方框绘制字符）和模糊宽度字形缩放的支持，以确保字符显示效果。
8. **自定义Prompt**: 推荐使用Starship和oh-my-posh等工具来美化Shell Prompt，提升终端的视觉吸引力。
引导学员自学：鼓励学员根据自己的审美和使用习惯，尝试调整终端的各种外观设置，打造一个舒适高效的开发环境。特别是对于字体、颜色和Prompt的定制，可以通过实际操作来体验其效果。同时，可以探索更多的第三方工具和主题，进一步美化终端。
-->

---

# 8.6 Terminal: Advanced Features

## Explore More Terminal Possibilities

- **Persistent Sessions**: Support for process reconnection and process recovery, ensuring terminal state is not lost.
- **Terminal Visibility**: Control terminal view hiding behavior at startup.
- **Keyboard Shortcuts & Shell**: Configure which shortcuts are handled by VS Code vs. sent to Shell.
- **Custom Sequence Shortcuts**: Send custom escape sequences through `sendSequence` command.
- **Send Custom Signals**: Use `sendSignal` command to send signals to foreground processes.
- **Confirmation Dialogs**: Configure warning prompts for process exit, child process termination, and non-zero exit codes.
- **Auto Reply**: Automatically send preset inputs to Shell for specific outputs.
- **Tab Width**: Configure display width of tabs in terminal.
- **Unicode & Emoji Support**: Terminal support for Unicode characters and Emojis with considerations.
- **Image Support**: Support for Sixel or iTerm inline image protocols to display images.
- **Process Environment**: Terminal process environment inheritance, `$LANG` variable interaction, and extension contributions to environment.
- **Windows & ConPTY**: Explain Windows terminal ConPTY technology and its characteristics.
- **Remote Development**: Local terminals in remote windows and reducing remote input latency (Local Echo).

<!--
本Slide将深入探讨VS Code终端的各种高级功能和配置选项，帮助学员更灵活地使用终端。
1. **持久会话**: 解释终端如何支持进程重连（重新加载窗口后恢复进程和内容）和进程恢复（重启VS Code后重新启动进程并恢复内容），以及如何配置这些行为。
2. **终端可见性**: 介绍`terminal.integrated.hideOnStartup`和`terminal.integrated.hideOnLastClosed`设置，用于控制终端视图在启动时和最后一个终端关闭时的隐藏行为。
3. **键盘快捷键与Shell**: 详细说明`terminal.integrated.commandsToSkipShell`设置，它决定了哪些VS Code命令的快捷键会“跳过Shell”直接由VS Code处理，以及如何自定义此列表。同时提及了和弦快捷键（Chords）和助记符（Mnemonics）的配置。
4. **自定义序列快捷键**: 介绍`workbench.action.terminal.sendSequence`命令，它允许用户发送自定义的转义序列到终端，实现更精细的控制，例如发送箭头键、回车等。强调了变量替换的支持。
5. **发送自定义信号**: 介绍`workbench.action.terminal.sendSignal`命令，允许向活动终端的前台进程发送任意信号，例如`SIGTERM`来优雅地终止进程。
6. **确认对话框**: 解释如何配置终端在进程退出、终止子进程或非零退出码时是否显示警告对话框，以避免不必要的提示。
7. **自动回复**: 介绍`terminal.integrated.autoReplies`设置，它允许终端在接收到特定输出时自动向Shell发送预设的输入，例如自动回复批处理脚本中的`Terminate batch job (Y/N)`提示。
8. **制表符宽度**: 提及`terminal.integrated.tabStopWidth`设置，用于配置终端中制表符的显示宽度。
9. **Unicode与Emoji支持**: 讨论终端对Unicode字符和Emoji的支持，以及可能存在的兼容性问题和相关配置（如`terminal.integrated.unicodeVersion`）。
10. **图像支持**: 介绍终端对Sixel或iTerm行内图像协议的支持，允许在终端中显示图像，并提及当前的一些限制。
11. **进程环境**: 解释终端进程环境的继承机制（`terminal.integrated.inheritEnv`）、`$LANG`环境变量的交互，以及扩展如何贡献终端环境，并处理环境变化时终端的重新启动。
12. **Windows与ConPTY**: 简要介绍Windows上的ConPTY技术，它是VS Code终端在Windows上实现Unix风格终端的关键，并提及ConPTY的一些特性和注意事项。
13. **远程开发**: 讨论在远程开发场景下终端的特殊功能，例如在远程窗口中启动本地终端，以及降低远程输入延迟（Local Echo）。
引导学员自学：鼓励学员深入探索这些高级功能，特别是那些可以提升工作效率和解决特定问题的设置。例如，可以尝试配置自动回复来简化重复性操作，或者了解ConPTY的工作原理来更好地理解Windows终端的行为。对于远程开发用户，可以尝试Local Echo功能来优化远程体验。
-->


---
layout: center
---

# Languages

## 多语言支持，赋能全栈开发

---

# Languages: 概述

## VS Code的语言支持与扩展

- **广泛的语言支持**: VS Code原生支持JavaScript、TypeScript、CSS、HTML等，并通过扩展市场支持数百种编程语言。
- **语言特性**: 提供语法高亮、括号匹配、智能补全（IntelliSense）、代码导航、调试、重构等。
- **AI增强**: GitHub Copilot提供AI驱动的代码补全和辅助功能。
- **语言模式切换**: 快速切换当前文件的语言模式。
- **语言标识符**: 了解VS Code如何关联语言模式与语言标识符。
- **文件关联**: 通过`files.associations`设置将文件扩展名关联到特定语言。

<!--
本Slide将概述VS Code对各种编程语言的广泛支持，以及如何通过内置功能和扩展来增强开发体验。
1. **广泛的语言支持**: 强调VS Code不仅原生支持前端开发常用的语言（如JavaScript、TypeScript、CSS、HTML），还通过其庞大的扩展市场支持几乎所有主流编程语言，包括后端常用的Java、Go、Python、C#等。鼓励学员通过扩展视图或Marketplace搜索并安装所需语言的扩展。
2. **语言特性**: 介绍VS Code为不同语言提供的核心特性，这些特性极大地提升了开发效率：
    - **语法高亮和括号匹配**: 基础的代码可读性功能。
    - **智能补全（IntelliSense）**: 提供代码建议、参数信息、成员列表等，包括AI驱动的GitHub Copilot。
    - **Linting和修正**: 实时检查代码错误和风格问题，并提供快速修复建议。
    - **代码导航**: 快速跳转到定义、查找所有引用等，帮助理解代码结构。
    - **调试**: 强大的调试功能，支持断点、单步执行、变量查看等。
    - **重构**: 自动化代码重构操作，如重命名、提取方法等。
3. **AI增强**: 突出GitHub Copilot作为AI驱动的代码补全工具，如何帮助开发者更快、更智能地编写代码，并提及Copilot在生成代码、文档和测试方面的能力。
4. **语言模式切换**: 介绍如何通过状态栏的语言指示器或`Change Language Mode`命令快速切换当前文件的语言模式，这对于处理没有标准文件扩展名的文件非常有用。
5. **语言标识符**: 解释VS Code如何使用语言标识符来关联语言模式，并强调标识符通常是小写的编程语言名称，但大小写敏感。学员可以通过`Change Language Mode`下拉列表查看已安装语言及其标识符。
6. **文件关联**: 介绍`files.associations`设置，允许用户将新的文件扩展名或特定文件路径关联到现有的语言标识符，从而为这些文件提供相应的语言支持。
引导学员自学：鼓励学员探索VS Code的扩展市场，寻找适合自己开发语言的优秀扩展。同时，深入了解IntelliSense、调试和重构等高级语言特性，并通过实际项目练习来掌握它们。对于多语言项目，学会如何管理文件关联和语言模式切换，将有助于提升开发效率。
-->

---

# Languages: Java

## VS Code中的Java开发

- **全面的Java支持**: 通过扩展包提供代码补全、重构、Linting、格式化、代码片段等功能。
- **快速启动**: 推荐使用Java Coding Pack或Extension Pack for Java快速搭建开发环境。
- **JDK安装**: 需要安装JDK 1.8或更高版本，并推荐多种JDK来源。
- **项目管理**: 支持轻量级模式和标准模式，理解VS Code工作区与Java项目的关系。
- **编辑增强**: 代码导航、智能补全（包括IntelliCode和Copilot）、代码片段。
- **调试与测试**: 强大的Java调试器和测试运行器，支持高级调试功能和JUnit/TestNG。
- **框架集成**: 深度集成Spring Boot、Tomcat、Jetty等流行框架。

<!--
本Slide将详细介绍VS Code中对Java开发的全面支持，以及如何利用其功能提升Java开发效率。
1. **全面的Java支持**: 强调VS Code通过一系列扩展（特别是Extension Pack for Java）为Java开发者提供了从代码编辑到调试、测试的完整功能，包括代码补全、重构、Linting、格式化和代码片段等。
2. **快速启动**: 推荐学员使用“Java Coding Pack”或“Extension Pack for Java”来快速设置Java开发环境，这些工具包集成了VS Code、JDK和一系列推荐的Java扩展，简化了配置过程。
3. **JDK安装**: 强调Java开发需要安装JDK 1.8或更高版本，并列举了多个推荐的JDK来源（如Amazon Corretto, Azul Zulu等）。同时提及了多JDK版本管理和Java预览功能的使用。
4. **项目管理**: 解释VS Code支持两种Java项目模式：轻量级模式（适用于单个源文件）和标准模式（适用于大型项目）。强调了VS Code工作区与Java项目概念的区别，以及如何通过Maven for Java和Project Manager for Java等扩展来管理Maven、Eclipse和Gradle项目。
5. **编辑增强**: 详细介绍了VS Code为Java代码编辑提供的增强功能：
    - **代码导航**: 支持搜索符号、Peek Definition、Go to Definition等，并提及Spring Boot Tools扩展对Spring Boot项目的增强。
    - **智能补全**: 提供上下文相关的代码补全，包括AI辅助的IntelliCode和GitHub Copilot，提升编码速度和质量。
    - **代码片段**: 内置多种常用Java代码片段（如`sout`、`main`），并通过语言服务器提供实时预览，提高编码效率。
    - **快速修复**: 自动检测代码问题并提供快速修复建议。
    - **重构**: 支持各种代码重构操作。
6. **调试与测试**: 突出VS Code强大的Java调试器（Debugger for Java）和测试运行器（Test Runner for Java），支持断点、表达式求值、条件断点、热代码替换等高级调试功能，以及JUnit和TestNG测试框架。
7. **框架集成**: 深度集成Spring Boot、Tomcat和Jetty等流行框架，通过相应的扩展进一步提升开发体验。
引导学员自学：鼓励学员安装Java扩展包，并尝试在VS Code中创建一个简单的Java项目，体验代码补全、调试和测试功能。可以深入了解Maven或Gradle项目管理，以及Spring Boot等框架的集成，以便在实际项目中应用。
-->

---

# Languages: Go

## VS Code中的Go开发

- **Go扩展**: 提供IntelliSense、代码导航、符号搜索、测试、调试等功能。
- **gopls**: Go语言服务器，提供核心语言特性，支持语义化高亮。
- **智能感知**: 自动补全、悬停信息、签名帮助，提升编码效率。
- **代码导航**: 快速跳转定义、类型定义、引用、调用层级、实现等。
- **构建与诊断**: 检测构建和vet错误，支持Lint工具集成。
- **格式化**: 支持Go文件格式化，可配置保存时自动格式化。
- **测试**: 通过Test UI和CodeLens运行、调试Go测试，支持测试覆盖率。
- **包导入**: 自动组织导入，支持添加缺失的包。
- **重构**: 支持变量、函数等重构操作。
- **调试**: 利用Delve调试器，支持本地/远程调试、表达式求值、Disassembly视图。

<!--
本Slide将介绍VS Code中对Go语言开发的强大支持，以及如何利用Go扩展提升Go开发效率。
1. **Go扩展**: 强调Go扩展为Go开发者提供了丰富的特性，包括IntelliSense、代码导航、符号搜索、测试和调试等，极大地提升了Go语言的开发体验。
2. **gopls**: 解释Go语言服务器`gopls`是Go扩展的核心，它提供了Go语言的智能感知功能，并支持语义化高亮，使得代码更具可读性。
3. **智能感知**: 详细说明Go扩展提供的智能感知功能，包括：
    - **自动补全**: 在输入代码时提供上下文相关的建议，包括当前包、已导入包和未导入包的成员。
    - **悬停信息**: 鼠标悬停在变量、函数或结构体上时，显示其文档、签名等信息。
    - **签名帮助**: 在调用函数时提供函数签名提示，并随着参数输入自动移动提示位置。
4. **代码导航**: 介绍Go扩展提供的多种代码导航功能，如Go to Definition、Go to Type Definition、Peek Definition、Go to References、Show Call Hierarchy、Go to Implementations等，帮助开发者快速理解代码结构和关系。同时提及了文件和测试文件之间的快速切换。
5. **构建与诊断**: 解释`gopls`如何检测构建和vet错误，并在“问题”面板中显示诊断信息。还提到了如何集成额外的Lint工具进行代码检查。
6. **格式化**: 说明Go扩展支持Go文件格式化，可以通过快捷键或命令触发，并可配置保存时自动格式化。强调了`gopls`在格式化中的作用，以及如何配置`gofumpt`风格的格式化。
7. **测试**: 介绍了VS Code的测试UI和CodeLens如何方便地运行、调试Go测试，并支持函数、文件、包或工作区级别的测试。同时提及了测试覆盖率的计算。
8. **包导入**: 解释Go扩展如何自动组织导入，并移除未使用的导入。还介绍了如何通过命令添加缺失的包。
9. **重构**: 简要说明Go扩展支持代码重构功能，如变量重命名、提取函数等。
10. **调试**: 突出Go扩展利用Delve调试器提供的强大调试功能，包括本地和远程调试、使用Delve表达式语法进行数据检查、动态配置更改、Disassembly视图等。
引导学员自学：鼓励学员安装Go扩展，并尝试在VS Code中编写Go代码，体验其智能感知、代码导航和调试功能。可以深入了解`gopls`的配置选项，并尝试集成不同的Lint工具。对于Go测试，可以尝试编写单元测试并使用VS Code的测试UI进行管理。
-->

---

# Java: Getting Started

## 快速开始你的Java之旅

- **设置VS Code**: 推荐使用Java Coding Pack或Extension Pack for Java快速安装所需工具和扩展。
- **JDK安装**: 确保安装JDK 1.8或更高版本，并了解多种JDK来源。
- **创建源代码文件**: 学习如何创建Java文件，并了解Java语言服务器的自动加载。
- **创建Java项目**: 通过`Java: Create Java Project`命令创建项目，支持多种构建工具。
- **编辑源代码**: 利用代码片段、IntelliSense和重构功能提升编码效率。
- **运行与调试**: 设置断点，通过“运行|调试”按钮或快捷键启动调试会话，支持高级调试功能。

<!--
本Slide将引导学员如何在VS Code中快速开始Java开发，从环境设置到编写、运行和调试第一个Java程序。
1. **设置VS Code**: 强调快速设置Java开发环境的重要性。推荐使用“Java Coding Pack”或“Extension Pack for Java”来快速设置Java开发环境，这些工具包集成了VS Code、JDK和一系列推荐的Java扩展，简化了配置过程。
2. **JDK安装**: 强调Java开发需要安装JDK 1.8或更高版本。列举了多个推荐的JDK来源，并提醒学员注意多JDK版本管理和Java预览功能的相关文档。
3. **创建源代码文件**: 介绍两种创建Java文件的方式：
    - **直接创建文件**: 在VS Code中创建`.java`文件，Java语言服务器会自动加载并提供语言支持。强调打开文件所在的文件夹的重要性。
    - **创建Java项目**: 通过`Java: Create Java Project`命令创建完整的Java项目，支持选择构建工具（如Maven）。提及VS Code对Java项目的处理方式与传统IDE（如IntelliJ IDEA）不同，主要依赖扩展来提供项目管理功能。
4. **编辑源代码**: 介绍VS Code为Java代码编辑提供的便利功能，包括：
    - **代码片段**: 利用内置的代码片段（如`sout`、`main`）快速生成常用代码结构。
    - **IntelliSense**: 提供智能代码补全，提升编码速度。
    - **重构**: 支持各种代码重构操作，如重命名、提取方法等。
5. **运行与调试**: 详细说明如何在VS Code中运行和调试Java程序：
    - **设置断点**: 在代码行号旁边点击即可设置断点。
    - **启动调试**: 通过“运行|调试”按钮、快捷键`kb(workbench.action.debug.start)`或CodeLens选项启动调试会话。
    - **调试功能**: 强调调试器支持高级功能，如表达式求值、条件断点和热代码替换（Hot Code Replace）。
引导学员自学：鼓励学员按照教程步骤，亲手在VS Code中编写并运行一个简单的Java“Hello World”程序，体验整个开发流程。可以尝试设置断点，单步调试，并修改代码后使用热代码替换功能。同时，可以探索Java扩展包中包含的其他扩展，了解它们提供的额外功能。
-->

---

# Java: Navigate and Edit

## 导航与编辑Java源代码

- **代码导航**: 利用Outline视图、Projects视图、Call Hierarchy、Type Hierarchy等进行代码导航。
- **符号搜索**: 在工作区或当前文件中快速搜索符号。
- **Peek Definition**: 无需离开当前位置即可查看符号定义。
- **Go to Definition**: 直接跳转到符号定义处。
- **Go to Super Implementation**: 快速查看类实现和方法重写。
- **折叠区域**: 折叠或展开代码片段，优化代码视图。
- **智能选择**: 根据语义信息扩展或收缩选择范围。
- **语义高亮**: 基于Java语言服务提供更精确的代码着色。
- **Spring Boot导航**: 针对Spring Boot项目提供增强导航功能。
- **代码编辑**: IntelliSense智能补全、代码片段、快速修复、重构等。
- **创建新文件**: 支持通过模板创建Java源文件，自动填充类体和包信息。
- **代码片段**: 丰富的Java代码片段和后缀补全功能，提高编码效率。

<!--
本Slide将详细介绍VS Code中Java源代码的导航和编辑功能，帮助学员高效地编写和理解Java代码。
1. **代码导航**: 强调VS Code提供了多种强大的代码导航工具，包括：
    - **Outline视图**: 方便地查看当前文件中的成员结构。
    - **Projects视图**: 提供项目概览。
    - **Call Hierarchy**: 显示函数的调用层级。
    - **Type Hierarchy**: 显示Java对象的继承关系。
    - **Definition Navigation**: 快速跳转到定义处。
    - **Search Types in Workspace**: 在整个工作区搜索类型。
2. **符号搜索**: 介绍如何在工作区（`kb(workbench.action.showAllSymbols)`或`Quick Open` + `#`）和当前文件（`Quick Open` + `@`）中快速搜索符号，并导航到其位置。
3. **Peek Definition**: 解释“Peek Definition”功能，允许在不离开当前编辑位置的情况下，通过弹出窗口快速查看符号的定义。
4. **Go to Definition**: 说明“Go to Definition”功能，可以直接跳转到符号的定义处。
5. **Go to Super Implementation**: 介绍如何通过点击链接快速查看类的实现和方法的重写。
6. **折叠区域**: 演示如何折叠或展开代码片段，以更好地查看源代码结构。
7. **智能选择**: 介绍“智能选择”功能，可以根据光标位置的语义信息智能地扩展或收缩选择范围。
8. **语义高亮**: 解释“语义高亮”如何基于Java语言服务提供更精确的代码着色，提升代码可读性。
9. **Spring Boot导航**: 突出Spring Boot Tools扩展为Spring Boot项目提供的增强导航功能，如快速查找请求映射、Bean、函数和Spring注解。
10. **代码编辑**: 总结VS Code在Java代码编辑方面的优势，包括：
    - **IntelliSense**: 智能代码补全和签名细节，包括AI辅助的IntelliCode。
    - **代码片段**: 丰富的Java代码片段和后缀补全功能，如`sout`、`main`等，并提供预览。
    - **快速修复**: 自动检测代码问题并提供快速修复建议。
    - **重构**: 支持各种代码重构操作。
11. **创建新文件**: 介绍VS Code如何支持在创建Java源文件时应用模板，自动生成类体和包信息。
引导学员自学：鼓励学员在实际编码中多使用这些导航和编辑功能，特别是快捷键，以提高编码效率。可以尝试自定义代码片段，并探索IntelliCode的更多高级用法。对于Spring Boot开发者，可以深入了解Spring Boot Tools扩展提供的特定导航功能。
-->

---

# Java: Refactoring

## Java代码重构与源操作

- **重构**: 提供了多种重构操作，如赋值给变量、匿名类与Lambda表达式转换、增强for循环、提取常量/字段/方法/局部变量、内联常量/局部变量/方法、反转布尔表达式、移动、重命名等。
- **源操作**: 提供了生成构造函数、委托方法、覆盖/实现方法、组织导入、生成Getter/Setter、生成`hashCode()`和`equals()`、生成`toString()`、将修饰符改为final等功能。
- **其他代码操作**: 修复不可访问引用、创建不存在的包等。
- **便捷访问**: 通过灯泡图标或右键菜单的“Source Action...”访问。

<!--
本Slide将详细介绍VS Code中Java代码的重构（Refactoring）和源操作（Source Actions）功能，这些功能可以帮助开发者更高效地修改和优化代码。
1. **重构**: 解释重构的目的是在不改变程序行为的前提下，对代码进行系统性的修改。VS Code为Java提供了丰富的重构选项，包括：
    - **赋值给变量**: 将表达式赋值给局部变量或字段，也可用于将参数赋值给构造函数中未使用的字段。
    - **匿名类与Lambda表达式转换**: 互相转换匿名内部类和Lambda表达式。
    - **增强for循环**: 将传统for循环转换为增强for循环。
    - **提取（Extract）**: 将选中的表达式或语句提取为常量、字段、方法或局部变量，并替换原有代码。
    - **内联（Inline）**: 将常量、局部变量或方法的引用替换为其定义的值或方法体。
    - **反转布尔表达式**: 反转条件中的布尔表达式或局部布尔变量。
    - **移动（Move）**: 移动类到其他包、静态/实例方法到其他类、内部类到新文件，并自动修正所有引用。
    - **重命名（Rename）**: 重命名选中的元素（类、方法、变量等），并自动更新所有引用，支持文件和文件夹的重命名。
    - **类型改变**: 转换`var`类型和解析后的具体类型。
2. **源操作**: 介绍源操作用于生成常用代码结构和修复问题，包括：
    - **生成构造函数**: 为类生成构造函数。
    - **生成委托方法**: 生成委托方法。
    - **覆盖/实现方法**: 方便地覆盖或实现父类/接口的方法。
    - **组织导入**: 清理和组织导入语句，处理模糊导入。
    - **生成Getter/Setter**: 批量生成字段的Getter和Setter方法。
    - **生成`hashCode()`和`equals()`**: 生成默认实现的`hashCode()`和`equals()`方法，支持自定义选项。
    - **生成`toString()`**: 生成`toString()`方法，支持自定义。
    - **将修饰符改为final**: 为变量和参数添加`final`修饰符。
3. **其他代码操作**: 提及其他一些有用的代码操作，如修复不可访问引用、创建不存在的包、创建未解析类型等。
4. **便捷访问**: 强调这些重构和源操作可以通过代码旁边的“灯泡”图标或右键菜单中的“Source Action...”来快速访问。
引导学员自学：鼓励学员在日常编码中积极使用这些重构和源操作功能，特别是那些可以自动化重复性任务的功能。通过实际操作，体验这些功能如何帮助保持代码的整洁性、可读性和可维护性。可以尝试在自己的项目中进行一些重构练习，并观察VS Code如何智能地处理代码变更。
-->

---

# Java: Formatting and Linting

## Java代码格式化与Linting

- **格式化**: 支持Eclipse格式化配置文件，可导入现有配置文件或编辑内置配置文件。
- **SonarLint**: 实时检测代码中的Bug和安全漏洞，提供详细解释和修复建议。
- **Checkstyle**: 使用Checkstyle配置检查代码风格，支持实时Linting和批量检查。
- **便捷访问**: 通过命令或状态栏图标快速访问和配置。

<!--
本Slide将介绍VS Code中Java代码的格式化（Formatting）和Linting功能，帮助学员保持代码风格一致性并发现潜在问题。
1. **格式化**: 解释VS Code通过`Language Support for Java™ by Red Hat`扩展提供Java代码格式化功能。强调其支持导入Eclipse格式化配置文件（`.xml`），这意味着团队可以共享和应用统一的格式化规则。同时，也支持编辑内置的格式化配置文件，并提供实时预览功能。
2. **SonarLint**: 详细介绍`SonarLint`扩展，它是一个实时代码质量工具，能够即时检测代码中的Bug和安全漏洞。强调其特点：
    - **实时分析**: 在编码时即时高亮问题。
    - **详细解释**: 提供问题原因、危害和修复建议，并附带示例。
    - **规则丰富**: 支持500+ Java规则，并提供快速修复。
    - **规则文档**: 提供规则的完整文档，帮助理解为什么会出现问题以及如何修复。
    - **规则管理**: 可以通过“SonarLint Rules”视图启用更多质量和安全规则。
3. **Checkstyle**: 介绍`Checkstyle for Java`扩展，它允许开发者使用现有的Checkstyle配置（如Google或Sun的Check）或自定义配置文件来检查代码风格。强调其特点：
    - **实时Linting**: 在编辑Java文件时实时检查代码格式。
    - **批量检查**: 支持对整个项目进行批量检查。
    - **快速修复**: 提供快速修复建议来解决风格违规。
    - **配置管理**: 可以通过命令或右键菜单设置Checkstyle配置文件，并支持选择Checkstyle版本和添加第三方模块。
引导学员自学：鼓励学员在项目中配置并使用代码格式化工具，确保团队代码风格的一致性。同时，积极使用SonarLint和Checkstyle等Linting工具，培养良好的编码习惯，提高代码质量和安全性。可以尝试自定义Checkstyle规则，以满足特定项目的需求。
-->

---

# Java: Project Management

## Java项目管理与依赖

- **项目视图**: 通过“Java Projects”视图管理项目和依赖，支持层级和平面视图切换。
- **创建与导入项目**: 快速创建新Java项目，或导入现有Maven/Gradle项目。
- **导出JAR**: 支持从项目视图或命令导出JAR文件。
- **配置运行时**: 灵活配置项目使用的JDK版本，支持多JDK环境。
- **配置Classpath**: 为非托管文件夹手动配置Classpath。
- **依赖管理**: 为Maven项目添加依赖，为非托管文件夹管理JAR库。
- **轻量级模式**: 快速启动和编辑源文件，支持与标准模式切换。
- **构建状态**: 实时查看Java语言服务器的构建任务状态。

<!--
本Slide将详细介绍VS Code中Java项目管理和依赖管理的功能，帮助学员高效地组织和维护Java项目。
1. **项目视图**: 解释“Java Projects”视图是管理Java项目的核心界面，它允许用户查看项目结构、依赖关系，并提供了项目管理任务的入口。支持在层级视图和平面视图之间切换。
2. **创建与导入项目**: 介绍如何快速创建新的Java项目（通过“+”按钮或`Java: Create Java Project...`命令），以及如何导入现有的Maven或Gradle项目（通过“Open Folder...”）。强调VS Code会自动检测并导入项目。
3. **导出JAR**: 说明如何从项目视图或通过`Java: Export Jar...`命令将项目导出为JAR文件。
4. **配置运行时**: 详细介绍`java.configuration.runtimes`设置，允许用户灵活配置不同JDK版本及其安装路径，并可以设置默认JDK。同时提及了如何为Maven/Gradle项目和非托管文件夹更改JDK版本。
5. **配置Classpath**: 解释如何为非托管文件夹（没有构建工具的项目）手动配置Classpath，包括添加和移除JAR库，以及通过`java.project.referencedLibraries`设置进行更细粒度的控制（包括、排除、源附件）。
6. **轻量级模式**: 介绍VS Code for Java的“轻量级模式”，它适用于快速编辑源文件，提供基本的语言特性（如代码导航、Outline视图、Javadoc）。强调轻量级模式不解析导入依赖，也不构建项目，因此不支持调试、重构等高级功能。说明了如何通过`java.server.launchMode`设置控制启动模式，以及如何手动在轻量级模式和标准模式之间切换。
7. **构建状态**: 解释如何通过状态栏的语言状态项或通知来实时查看Java语言服务器的构建任务状态，这对于理解项目加载和编译过程非常有帮助。
引导学员自学：鼓励学员在实际项目中尝试使用项目管理功能，特别是多JDK环境的配置和非托管文件夹的依赖管理。可以深入了解 Maven 或 Gradle 的构建脚本，并尝试在不同模式下切换，体验其差异。同时，关注构建状态，以便及时发现和解决项目问题。
-->

---

# Java: Build Tools

## VS Code中的Java构建工具

- **Maven支持**: 通过Maven for Java扩展提供Maven项目探索、命令执行、依赖管理、项目生成等功能。
- **Gradle支持**: 通过Gradle for Java扩展提供Gradle项目导入、任务管理、依赖查看、构建文件编辑等功能。
- **构建服务器**: Gradle Build Server确保构建任务与命令行一致。
- **测试委托**: 支持将测试执行委托给Gradle。
- **其他构建工具**: 提及Bazel等其他构建工具的扩展支持。

<!--
本Slide将介绍VS Code中对Java构建工具的支持，重点关注Maven和Gradle。
1. **Maven支持**: 详细介绍`Maven for Java`扩展，它为Maven项目提供了全面的支持：
    - **项目探索**: 自动扫描`pom.xml`文件，并在侧边栏显示所有Maven项目和模块。
    - **未知类型解析**: 支持搜索Maven Central来解析源代码中的未知类型。
    - **`pom.xml`编辑**: 提供代码片段和自动补全，方便添加Maven依赖。支持生成Effective POM。
    - **命令执行**: 方便地运行Maven目标（goals），支持历史记录和收藏命令。
    - **调试Maven目标**: 直接从VS Code中调试Maven目标。
    - **项目生成**: 通过Maven Archetype生成新项目。
2. **Gradle支持**: 详细介绍`Gradle for Java`扩展，它为Gradle项目提供了增强的开发体验：
    - **Gradle Build Server**: 解释其作用是导入Gradle项目并将构建任务委托给Gradle守护进程，确保构建结果与命令行一致。
    - **可视化界面**: 允许查看和管理Gradle任务和项目依赖，以及直接在VS Code中运行Gradle任务。
    - **Gradle Language Server**: 为Gradle构建文件提供语法高亮、错误报告和自动补全。
    - **测试委托**: 支持将测试执行委托给Gradle。
    - **任务管理**: 在“Gradle Projects”视图中列出所有Gradle项目和任务，支持固定任务和查看最近任务。
    - **依赖查看**: 在“Dependencies”项下查看项目的所有依赖。
    - **守护进程管理**: 在“Gradle Daemons”视图中管理运行中的Gradle守护进程。
    - **构建文件编辑**: 为Gradle构建文件提供语义化高亮、Outline视图、问题检测和自动补全。
3. **其他构建工具**: 提及VS Code也支持其他构建工具，如Bazel，并有相应的扩展。
引导学员自学：鼓励学员根据自己项目使用的构建工具，深入了解相应的VS Code扩展。可以尝试在实际项目中利用这些扩展来管理依赖、执行构建任务和调试。对于Maven和Gradle，可以尝试自定义其构建脚本，并观察VS Code如何提供智能支持。
-->

---

# Java: Run and Debug

## Java应用程序的运行与调试

- **Debugger for Java**: 基于Java Debug Server的轻量级调试器，提供丰富的调试功能。
- **安装与配置**: 通过Extension Pack for Java安装，支持自动生成和自定义`launch.json`配置。
- **启动调试**: 多种方式启动调试会话，包括CodeLens、编辑器菜单和F5快捷键。
- **单文件调试**: 支持调试单个Java文件，无需项目配置。
- **调试会话输入**: 可配置在集成终端或外部终端进行输入。
- **断点**: 支持行断点、条件断点、数据断点、日志点和触发断点。
- **表达式求值**: 在WATCH窗口和Debug Console中评估表达式。
- **热代码替换 (HCR)**: 调试时无需重启JVM即可替换代码，支持手动、自动和禁用模式。
- **步进过滤**: 过滤掉不希望单步调试的类或方法。
- **配置选项**: 丰富的`launch.json`配置选项，用于自定义JVM参数、环境变量等。
- **故障排除**: 常见问题及解决方案。

<!--
本Slide将详细介绍VS Code中Java应用程序的运行和调试功能，帮助学员高效地定位和解决代码问题。
1. **Debugger for Java**: 解释`Debugger for Java`扩展是VS Code中Java调试的核心，它是一个基于Java Debug Server的轻量级调试器，提供了与传统IDE相媲美的调试功能，如启动/附加、断点、异常、暂停与继续、单步执行、变量查看、调用堆栈、线程和调试控制台等。
2. **安装与配置**: 强调通过`Extension Pack for Java`即可安装调试器。说明调试器默认会自动查找主类并生成内存中的启动配置，但用户也可以通过`create a launch.json file`链接来自定义和持久化启动配置，以便更灵活地控制调试行为。
3. **启动调试**: 介绍多种启动调试会话的方式，包括：
    - **CodeLens**: 在`main()`函数旁边的“运行|调试”CodeLens。
    - **编辑器菜单**: 顶部编辑器标题栏的“Run Java”或“Debug Java”菜单。
    - **F5快捷键**: 按下F5键，调试器会自动找到入口点并启动调试。
4. **单文件调试**: 突出VS Code支持调试单个Java文件，即使没有完整的项目配置，这对于快速测试代码片段非常方便。
5. **调试会话输入**: 解释如果程序需要输入，可以通过配置在VS Code的集成终端或外部终端进行输入，解决了默认Debug Console不支持输入的问题。
6. **断点**: 详细介绍调试器支持的各种断点类型：
    - **行断点**: 最基本的断点。
    - **条件断点**: 当表达式为真时才触发。
    - **数据断点**: 当变量值改变时触发（需在调试会话中设置）。
    - **日志点（Logpoints）**: 无需修改代码即可向Debug Console输出信息，不中断执行。
    - **触发断点（Triggered breakpoints）**: 当另一个断点被命中后自动启用。
7. **表达式求值**: 说明如何在“WATCH”窗口和“Debug Console”中评估表达式，方便实时查看变量值和执行代码片段。
8. **热代码替换 (HCR)**: 重点介绍“热代码替换”功能，它允许在不重启JVM的情况下，在调试会话中修改Java代码并立即生效，极大地提升了开发效率。说明了HCR的配置选项（手动、自动、禁用）。
9. **步进过滤**: 解释如何配置步进过滤，跳过不希望单步调试的类或方法，例如JDK内部类，从而专注于自己的代码。
10. **配置选项**: 提及`launch.json`中丰富的配置选项，用于自定义JVM参数、环境变量、命令行缩短等，以满足不同项目的调试需求。
11. **故障排除**: 简要提及文档中提供了常见的调试问题及其解决方案，引导学员在遇到问题时查阅。
引导学员自学：鼓励学员在实际项目中积极使用VS Code的调试功能，特别是条件断点、日志点和热代码替换。通过调试，深入理解程序的执行流程和变量状态。同时，学会自定义`launch.json`配置，以适应不同项目的调试场景。
-->

---

# Java: Testing

## Java代码测试

- **Test Runner for Java**: 轻量级扩展，支持运行和调试Java测试用例。
- **支持框架**: 支持JUnit 4、JUnit 5和TestNG。
- **项目设置**: 介绍如何为Maven、Gradle和非托管文件夹配置测试框架。
- **运行/调试测试**: 通过CodeLens或Testing Explorer快速运行和调试测试用例。
- **Testing Explorer**: 树形视图展示所有测试用例，并可查看测试结果。
- **自定义测试配置**: 通过`java.test.config`设置自定义测试运行参数，如`args`、`classPaths`、`env`、`vmArgs`等。
- **查看测试结果**: 在编辑器装饰和Testing Explorer中查看测试结果，并可跳转到源代码位置。
- **生成测试**: 支持从主源代码或测试源代码生成测试用例骨架。
- **测试导航**: 快速在测试和被测试代码之间跳转。
- **其他测试命令与设置**: 介绍其他测试相关命令和设置。

<!--
本Slide将详细介绍VS Code中Java代码的测试功能，帮助学员高效地编写、运行和管理Java测试用例。
1. **Test Runner for Java**: 解释`Test Runner for Java`扩展是VS Code中Java测试的核心，它是一个轻量级扩展，提供了运行和调试Java测试用例的功能。
2. **支持框架**: 强调该扩展支持主流的Java测试框架，包括JUnit 4、JUnit 5和TestNG。
3. **项目设置**: 详细说明如何为不同类型的Java项目（Maven、Gradle和非托管文件夹）设置和启用测试框架，包括添加必要的依赖JAR包。
4. **运行/调试测试**: 介绍多种运行和调试测试用例的方式，包括：
    - **CodeLens**: 在类和方法定义旁边的绿色播放按钮。
    - **Testing Explorer**: 在测试资源管理器中选择测试用例并运行/调试。
5. **Testing Explorer**: 解释“Testing Explorer”是一个树形视图，展示工作区中所有的测试用例，并允许用户直接从该视图运行/调试测试和查看测试结果。
6. **自定义测试配置**: 详细介绍`java.test.config`设置，允许用户自定义测试运行的各种参数，例如命令行参数（`args`）、额外的Classpath（`classPaths`）、环境变量（`env`）、JVM参数（`vmArgs`）、工作目录（`workingDirectory`）以及测试框架类型（`testKind`）和过滤器（`filters`）。
7. **查看测试结果**: 说明测试运行后，相关的测试项会在编辑器装饰和Testing Explorer中更新状态，并可以点击堆栈跟踪中的链接跳转到源代码位置。
8. **生成测试**: 介绍如何通过“Source Action...”菜单中的“Generate Tests...”功能，从主源代码或测试源代码生成测试用例的骨架，提高测试编写效率。
9. **测试导航**: 解释如何通过“Go to Test”或“Go to Test Subject”命令在测试代码和被测试代码之间快速跳转。
10. **其他测试命令与设置**: 提及VS Code中还有其他测试相关的命令（如“Run Tests in Current File”）和设置，可以通过命令面板和设置编辑器进行探索。
引导学员自学：鼓励学员在实际项目中编写单元测试，并利用VS Code的测试功能进行运行和调试。可以尝试自定义测试配置，以满足特定测试场景的需求。同时，学会利用生成测试功能来快速创建测试用例。
-->

---

# Java: Spring Boot

## VS Code中的Spring Boot开发

- **扩展支持**: 推荐安装Spring Boot Extension Pack，包含Spring Boot Tools、Spring Initializr、Spring Boot Dashboard。
- **项目创建**: 通过Spring Initializr快速生成Maven或Gradle的Spring Boot项目。
- **项目编辑**: 支持在`pom.xml`中添加/移除依赖，提供智能提示。
- **应用开发**: Spring Boot Tools提供丰富的语言支持，如`application.properties`、`application.yml`和`.java`文件的智能补全、导航。
- **运行应用**: 通过Spring Boot Dashboard方便地管理和运行Spring Boot应用。

<!--
本Slide将介绍VS Code中对Spring Boot开发的强大支持，以及如何利用相关扩展提升开发效率。
1. **扩展支持**: 强调VS Code是Spring Boot开发的理想轻量级环境，并推荐安装`Spring Boot Extension Pack`，它集成了`Spring Boot Tools`、`Spring Initializr`和`Spring Boot Dashboard`等核心扩展。
2. **项目创建**: 详细说明如何通过`Spring Initializr`扩展快速生成新的Spring Boot项目，支持选择Maven或Gradle作为构建工具，并引导用户完成项目初始化向导。
3. **项目编辑**: 介绍`Spring Initializr`扩展在项目创建后，如何方便地在`pom.xml`文件中添加或移除Spring Boot的Starter依赖，并提供智能提示功能。
4. **应用开发**: 突出`Spring Boot Tools`扩展在Spring Boot应用开发中的核心作用，它为`application.properties`、`application.yml`和`.java`文件提供了丰富的语言支持，包括：
    - **快速导航**: 快速跳转到Spring元素。
    - **智能补全**: 针对Spring特定组件的智能代码补全。
    - **实时应用信息**: 显示运行中的Spring应用的实时信息和指标。
    - **代码模板**: 提供代码模板以加速开发。
5. **运行应用**: 介绍除了传统的调试启动方式外，还可以通过`Spring Boot Dashboard`扩展方便地查看和管理工作区中所有可用的Spring Boot项目，并快速启动、停止或调试它们。
引导学员自学：鼓励学员安装Spring Boot Extension Pack，并尝试创建一个简单的Spring Boot项目。可以深入了解`application.properties`和`application.yml`的配置，并尝试使用Spring Boot Tools提供的导航和实时信息功能。同时，可以探索如何将Spring Boot应用部署到Azure等云平台。
-->

---

# Java: Extensions

## 扩展你的Java开发体验

- **核心Java开发**: 推荐Extension Pack for Java，包含语言支持、调试器、测试运行器、Maven、项目管理器和IntelliCode。
- **Spring Boot扩展**: 推荐Spring Boot Extension Pack，包含Spring Boot Tools、Spring Initializr Java Support和Spring Boot Dashboard。
- **Gradle支持**: 通过Gradle for Java扩展提供Gradle项目支持。
- **应用服务器**: Community Server Connectors支持Tomcat、Jetty等应用服务器。
- **MicroProfile / Quarkus**: 提供了相应的扩展包支持。
- **其他Java IDE键位映射**: 方便从Eclipse或IntelliJ IDEA迁移的用户。
- **远程开发与容器支持**: 推荐Remote Development、Container Tools、Kubernetes和Live Share等扩展。
- **Azure集成**: Azure Tools Extension Pack、Azure Repos、Azure IoT Toolkit、Azure Resource Manager Tools等。
- **搜索更多扩展**: 通过扩展视图搜索更多Java相关扩展。

<!--
本Slide将介绍VS Code中丰富的Java扩展生态系统，帮助学员根据需求选择合适的扩展来增强开发体验。
1. **核心Java开发**: 强调`Extension Pack for Java`是进行核心Java开发的首选，它包含了Red Hat的Java语言支持、Java调试器、测试运行器、Maven支持、项目管理器和IntelliCode等，提供了全面的基础功能。
2. **Spring Boot扩展**: 推荐`Spring Boot Extension Pack`，它集成了`Spring Boot Tools`、`Spring Initializr Java Support`和`Spring Boot Dashboard`，为Spring Boot开发者提供了从项目创建到开发、运行和管理的完整支持。
3. **Gradle支持**: 提及`Gradle for Java`扩展，为使用Gradle构建工具的Java项目提供支持。
4. **应用服务器**: 介绍`Community Server Connectors`扩展，它支持Tomcat、Jetty等主流应用服务器，方便开发者在VS Code中管理和部署Web应用。
5. **MicroProfile / Quarkus**: 提及了对Eclipse MicroProfile和Quarkus等现代Java框架的扩展支持。
6. **其他Java IDE键位映射**: 介绍了针对从Eclipse或IntelliJ IDEA迁移过来的开发者，提供了相应的键位映射扩展，帮助他们更快地适应VS Code的快捷键。
7. **远程开发与容器支持**: 推荐了一系列在远程开发和容器化场景下非常有用的扩展，包括：
    - **Remote Development**: 允许在容器、远程机器或WSL中进行开发。
    - **Container Tools**: 用于构建Docker镜像和管理镜像仓库。
    - **Kubernetes**: 提供Kubernetes集群管理和清单文件编辑支持。
    - **Live Share**: 用于实时协作编程。
8. **Azure集成**: 介绍了VS Code与Azure云服务的深度集成，包括`Azure Tools Extension Pack`（发现和交互Azure服务）、`Azure Repos`（连接Azure DevOps Server，管理代码仓库）、`Azure IoT Toolkit`（IoT应用开发）和`Azure Resource Manager Tools`（ARM模板编辑）。
9. **搜索更多扩展**: 指导学员如何通过VS Code的扩展视图搜索更多Java相关的扩展，以满足个性化需求。
引导学员自学：鼓励学员根据自己的项目需求和技术栈，探索并安装相应的扩展。特别是对于云原生开发和DevOps实践，可以深入了解Azure集成和容器化相关的扩展。同时，可以尝试贡献自己的扩展，丰富VS Code的Java生态系统。
-->

---

# Java: FAQ

## Java开发常见问题解答

- **开源性**: 大部分Java扩展都是开源的，可在GitHub上找到对应仓库。
- **未来功能**: 持续增加重构和Linting功能，提升性能，并欢迎社区贡献。
- **键位映射**: 支持从其他IDE（如IntelliJ IDEA、Eclipse）导入键位映射。
- **最新进展**: 可通过Java at Microsoft博客和扩展包发布说明获取最新信息。
- **新Java版本支持**: 支持Java 22及更高版本，并提供预览功能配置方法。
- **企业代理**: 配置`java.jdt.ls.vmargs`以支持企业代理环境。
- **Visual Studio支持**: 目前无计划将Java支持扩展到Visual Studio。
- **多语言显示**: 部分扩展支持中文显示，并欢迎贡献其他语言支持。
- **故障排除与贡献**: 提供Java Language Server的故障排除指南和贡献方式。

<!--
本Slide将总结VS Code中Java开发的常见问题，帮助学员解决实际操作中可能遇到的困惑。
1. **开源性**: 强调VS Code中大部分Java扩展都是开源的，鼓励学员通过Marketplace页面找到对应的GitHub仓库，了解其实现细节或参与贡献。
2. **未来功能**: 提及Java扩展团队会根据GitHub issues中的请求和客户反馈来规划未来的功能，包括增加重构、Linting功能和性能改进。鼓励学员积极提供反馈和参与贡献。
3. **键位映射**: 解释VS Code支持通过“Keymap extensions”来匹配其他IDE（如IntelliJ IDEA、Eclipse）的键盘快捷键，方便开发者从其他IDE迁移。
4. **最新进展**: 指导学员通过“Java at Microsoft”博客和“Extension Pack for Java”的发布说明来获取Java支持的最新进展和更新信息。
5. **新Java版本支持**: 强调VS Code已支持Java 22及更高版本，并提供了在Maven和Gradle项目中配置预览功能的方法。同时提醒可能需要清理工作区以使更改生效。
6. **企业代理**: 解释如何在企业代理环境下配置`java.jdt.ls.vmargs`设置，以便Java语言服务器能够正确连接到互联网，下载依赖和源代码。
7. **Visual Studio支持**: 明确表示目前没有计划将Java支持扩展到Visual Studio，因为VS Code专注于提供轻量级、多语言的编辑体验。
8. **多语言显示**: 提及部分Java扩展已支持中文显示，并鼓励社区贡献其他显示语言的支持。
9. **故障排除与贡献**: 引导学员查阅“Java for Visual Studio Code wiki”以获取详细的故障排除指南，并鼓励他们通过GitHub仓库提交Bug报告或功能建议，甚至直接参与代码贡献。
引导学员自学：鼓励学员在遇到问题时，首先查阅FAQ文档，并学会利用VS Code内置的日志和调试工具进行自我排查。同时，积极向社区和官方提供反馈，共同改进Java开发体验。
-->

---
layout: center
---

# Reference

## 深入了解VS Code配置

---

# Reference: Default Keyboard Shortcuts

## VS Code默认键盘快捷键参考

- **查看默认快捷键**: 可通过“Show System Keybindings”或“Open Default Keyboard Shortcuts (JSON)”查看。
- **键盘布局**: 默认以标准美式键盘布局渲染，可配置其他键盘布局。
- **基本编辑**: 剪切、复制、粘贴、删除行、插入行、移动行、复制行、撤销、重做、多光标操作、选择、缩进、行首/尾/文件首/尾跳转、滚动、代码折叠、注释、查找替换等。
- **富语言编辑**: 触发建议、参数提示、格式化文档/选择、跳转定义、查看悬停信息、快速修复、跳转引用、重命名符号、智能选择、修剪尾随空格、更改语言模式等。
- **导航**: 显示所有符号、跳转到行/文件/符号、显示问题、错误/警告导航、显示所有命令、导航编辑器组历史、前进/后退等。
- **编辑器/窗口管理**: 新建/关闭窗口/编辑器/文件夹、循环切换编辑器组、拆分编辑器、焦点切换、移动编辑器/编辑器组等。
- **文件管理**: 新建/打开/保存文件、关闭文件/组、重新打开关闭的编辑器、复制文件路径、在文件管理器中显示、比较文件等。
- **显示**: 全屏、Zen模式、缩放、侧边栏可见性、显示视图（Explorer, Search, SCM, Run, Extensions, Output）、Markdown预览、集成终端切换等。
- **搜索**: 显示搜索、文件内替换、切换大小写敏感/全字匹配/正则表达式、显示搜索详情、焦点切换搜索结果、显示历史搜索词等。
- **搜索编辑器**: 在编辑器中打开结果、焦点搜索编辑器输入、重新搜索、删除文件结果等。
- **首选项**: 打开设置、工作区设置、键盘快捷键、用户代码片段、选择颜色主题、配置显示语言等。
- **调试**: 切换断点、启动/继续/暂停/单步调试等。
- **任务**: 运行构建任务、运行测试任务等。
- **扩展**: 安装/显示已安装/过期/推荐/流行扩展、更新所有扩展等。

<!--
本Slide将详细介绍VS Code的默认键盘快捷键，帮助学员熟悉并高效使用VS Code的各项功能。
1. **查看默认快捷键**: 解释如何通过“Show System Keybindings”命令在键盘快捷键编辑器中查看系统默认快捷键，或者通过“Open Default Keyboard Shortcuts (JSON)”命令查看JSON格式的默认快捷键定义。
2. **键盘布局**: 提醒学员默认快捷键是基于标准美式键盘布局渲染的，并提及可以配置其他键盘布局。
3. **基本编辑**: 列举了大量常用的基本编辑操作快捷键，如剪切/复制/粘贴行、删除/插入/移动/复制行、撤销/重做、多光标操作、选择、缩进、行首/尾/文件首/尾跳转、滚动、代码折叠、行/块注释、查找/替换等。这些是日常编码中频繁使用的功能。
4. **富语言编辑**: 介绍了与语言特性相关的快捷键，如触发建议（IntelliSense）、参数提示、格式化文档/选择、跳转定义、查看悬停信息、快速修复、跳转引用、重命名符号、智能选择、修剪尾随空格、更改语言模式等。这些快捷键能够显著提升编码效率。
5. **导航**: 涵盖了在VS Code中进行文件和符号导航的快捷键，如显示所有符号、跳转到行/文件/符号、显示问题面板、错误/警告导航、显示所有命令、导航编辑器组历史、前进/后退等。这些快捷键有助于快速定位代码和文件。
6. **编辑器/窗口管理**: 介绍了管理编辑器和窗口布局的快捷键，如新建/关闭窗口/编辑器/文件夹、循环切换编辑器组、拆分编辑器、焦点切换、移动编辑器/编辑器组等。这些快捷键有助于优化工作空间。
7. **文件管理**: 列举了文件操作相关的快捷键，如新建/打开/保存文件、关闭文件/组、重新打开关闭的编辑器、复制文件路径、在文件管理器中显示、比较文件等。
8. **显示**: 介绍了控制VS Code界面显示的快捷键，如全屏、Zen模式、缩放、侧边栏可见性、显示各种视图（Explorer, Search, SCM, Run, Extensions, Output）、Markdown预览、集成终端切换等。
9. **搜索**: 涵盖了搜索功能相关的快捷键，如显示搜索、文件内替换、切换大小写敏感/全字匹配/正则表达式、显示搜索详情、焦点切换搜索结果、显示历史搜索词等。
10. **搜索编辑器**: 介绍了搜索编辑器特有的快捷键，如在编辑器中打开结果、焦点搜索编辑器输入、重新搜索、删除文件结果等。
11. **首选项**: 列举了与VS Code配置相关的快捷键，如打开设置、工作区设置、键盘快捷键、用户代码片段、选择颜色主题、配置显示语言等。
12. **调试**: 介绍了调试操作的快捷键，如切换断点、启动/继续/暂停/单步调试等。
13. **任务**: 介绍了任务相关的快捷键，如运行构建任务、运行测试任务等。
14. **扩展**: 介绍了扩展管理相关的快捷键，如安装/显示已安装/过期/推荐/流行扩展、更新所有扩展等。
引导学员自学：鼓励学员花时间熟悉这些默认快捷键，特别是那些与自己日常工作流密切相关的。可以尝试自定义一些不常用的快捷键，或者将其他IDE的快捷键映射到VS Code中。熟练使用快捷键将极大地提升开发效率。
-->

---

# Reference: Default Settings

## VS Code默认设置参考

- **默认设置**: VS Code自带一套默认设置，可通过用户或工作区设置覆盖。
- **查看方式**: 通过“Preferences: Open Default Settings (JSON)”命令查看所有默认设置。

<!--
本Slide将介绍VS Code的默认设置，以及如何查看和理解它们。
1. **默认设置**: 解释VS Code内置了一套默认设置，这些设置可以在用户级别或工作区级别被覆盖，从而实现个性化配置。
2. **查看方式**: 指导学员如何通过命令面板中的“Preferences: Open Default Settings (JSON)”命令来查看所有默认设置的JSON文件。强调这是一个只读文件，用于参考。
引导学员自学：鼓励学员通过设置编辑器（Settings editor）来探索和修改VS Code的设置，而不是直接编辑JSON文件。同时，可以深入了解VS Code的设置优先级（用户设置 > 工作区设置 > 文件夹设置），以便更好地管理自己的开发环境。
-->

---

# Reference: Substitution Variables

## VS Code中的变量替换

- **用途**: 在调试和任务配置文件中支持变量替换，以及部分设置。
- **语法**: 使用`${variableName}`语法进行变量替换。
- **预定义变量**: 提供了多种预定义变量，如`${userHome}`、`${workspaceFolder}`、`${file}`等，涵盖文件路径、工作区信息、行号、选中文本等。
- **环境变量**: 通过`${env:Name}`引用环境变量。
- **配置变量**: 通过`${config:Name}`引用VS Code设置。
- **命令变量**: 通过`${command:commandID}`执行VS Code命令并获取其字符串结果。
- **输入变量**: 通过`${input:variableID}`定义交互式输入，支持`promptString`、`pickString`和`command`类型。
- **变量作用域**: 变量作用域默认为当前文件夹，多根工作区可通过`${workspaceFolder:FolderName}`引用其他根文件夹。
- **替换过程**: 变量替换分两步进行，确保变量之间不相互依赖。

<!--
本Slide将详细介绍VS Code中变量替换的功能，以及如何在调试、任务配置和设置中使用它们。
1. **用途**: 解释变量替换主要用于`launch.json`（调试配置）和`tasks.json`（任务配置）文件，以及一些特定的VS Code设置中，以实现动态配置。
2. **语法**: 说明变量替换的通用语法是`${variableName}`。
3. **预定义变量**: 详细列举并解释了VS Code提供的一系列预定义变量，这些变量可以获取当前用户主目录、工作区路径、文件名、行号、选中文本等信息。通过示例说明了这些变量在不同场景下的具体值。
4. **环境变量**: 介绍如何使用`${env:Name}`语法引用系统环境变量，例如`${env:USERNAME}`。
5. **配置变量**: 解释如何使用`${config:Name}`语法引用VS Code的配置设置，例如`${config:editor.fontSize}`。
6. **命令变量**: 介绍如何使用`${command:commandID}`语法执行VS Code命令，并将其返回的字符串结果作为变量值。强调命令变量必须返回字符串，并举例说明了如何用于选择进程ID。
7. **输入变量**: 重点介绍了输入变量（`${input:variableID}`），它允许在配置中定义交互式输入，从而在运行时向用户请求信息。详细说明了三种输入变量类型：
    - `promptString`: 显示输入框获取字符串。
    - `pickString`: 显示快速选择下拉列表让用户选择。
    - `command`: 运行一个命令来获取输入。
    并提供了Angular CLI的示例，展示了如何组合使用`pickString`和`promptString`来生成命令参数。
8. **变量作用域**: 解释了变量的作用域，默认情况下变量作用于当前文件夹，但在多根工作区中，可以通过`${workspaceFolder:FolderName}`来引用其他根文件夹的路径。
9. **替换过程**: 简要说明变量替换是一个两步过程，确保变量的独立性，避免循环依赖。
引导学员自学：鼓励学员在实际的调试和任务配置中尝试使用各种变量，特别是输入变量，以实现更灵活和交互式的开发流程。可以尝试创建自定义任务，并利用变量来自动化一些重复性操作。同时，可以查阅VS Code的官方文档，了解更多关于变量替换的细节和高级用法。
-->

---
title: Thanks
layout: center
---

# Thanks For Your Attention!