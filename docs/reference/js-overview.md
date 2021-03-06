---
type: doc
layout: reference
category: "Introduction"
title: "在 JavaScript 开发中使用 Kotlin"
---

# Kotlin JavaScript 概述

Kotlin 提供了在 JavaScript 平台上运行的能力. 实现方法是将 Kotlin 代码转换为 JavaScript. 目前的实现针对 ECMAScript 5.1 标准, 但我们计划最终实现 ECMAScript 2015 标准.

当你选择编译目标为 JavaScript 时, 所有的 Kotlin 代码, 包括你的工程内的代码, 以及 Kotlin 自带的标准库的代码, 全部都会转换为 JavaScript.
但是不包括 JDK, 以及你使用到的任何 JVM, 或其他 Java 框架, 或其他库. Kotlin 代码之外的一切文件都会在编译期间被忽略掉.

Kotlin 编译器在编译时会尝试实现以下目标:

* 保证编译输出的 JavaScript 代码在尺寸方面最优化
* 保证编译输出的 JavaScript 代码是易读的
* 实现与现有的模块系统(module system)的互操作性
* 无论是编译到 JavaScript 还是JVM, (最大限度地)保证标准库的功能等同.

## 如何使用

在以下场景中, 你可能会希望将 Kotlin 代码编译为 JavaScript:

* 编写 Kotlin 代码, 用于客户端 JavaScript

    * **与 DOM 元素交互**. Kotlin 提供了一系列静态类型的接口, 可以与文档对象模型(Document Object Model)进行交互, 可以用来创建或修改 DOM 元素.

    * **与图形交互, 比如 WebGL**. 你可以编写 Kotlin 代码, 在 Web 页面中使用 WebGL 来创建图形元素 .

* 编写 Kotlin 代码, 用于服务器端 JavaScript

    * **使用服务器端技术**. 你可以使用 Kotlin 来与服务器端 JavaScript 交互, 比如 Node.js

Kotlin 可以与既有的第三方库和框架共同工作, 比如 jQuery 或 React. 要使用强类型 API 的第三方框架, 你可以使用 [ts2kt](https://github.com/kotlin/ts2kt) 工具, 将 [Definitely Typed](http://definitelytyped.org/) 类型定义库中的 TypeScript 定义转换为 Kotlin. 或者, 你也可以使用 [动态类型(Dynamic Type)](dynamic-type.html) 功能来访问任何没有强类型的框架.

JetBrains 专门针对 React 社区开发了几种工具: [React bindings](https://github.com/JetBrains/kotlin-wrappers), 以及 [Create React Kotlin App](https://github.com/JetBrains/create-react-kotlin-app). 其中, Create React Kotlin App 可以帮助你使用 Kotlin 来创建 React 应用程序, 而不需要编译配置.

Kotlin 兼容于 CommonJS, AMD 以及 UMD, 因此可以直接[与不同的模块系统交互](https://kotlinlang.org/docs/tutorials/javascript/working-with-modules/working-with-modules.html).


## 使用 Kotlin 进行 JavaScript 开发入门

关于如何使用 Kotlin 进行 JavaScript 开发, 请参见以下 [教程](https://kotlinlang.org/docs/tutorials/javascript/kotlin-to-javascript/kotlin-to-javascript.html).
