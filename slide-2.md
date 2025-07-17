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