# 深入理解开源许可证（Apache,MIT,GPL,BSD,CC）

## 前言

如果说有什么东西正在为开源世界保驾护航，那就一定不能不提到开源许可证（Open Source License），正是因为这些各不相同的开源许可证的共同支持下，才有了现在这么繁荣的开源软件社区。

但是问题是，这些开源协议太多了（至少有上百种！），即使是主流的几个开源协议，由于其法律文本的晦涩难懂，经常令很多开发者摸不着头脑，不知道他们的软件应当使用什么样的许可协议，或者如何使用这些协议。因此，本文试图通过简单通俗的语言，带领读者了解和区分不同许可证之间的区别。

最后，因为作者知识有限，因此对于本文可能存在的谬误，烦请读者尽数指正，不尽感激！

## 什么是开源许可证？“开源”和“自由”的区别是什么

### 开源许可证

狭义的来讲，根据 [OSI（Open Source Initiative，开放源代码倡议组织）](https://opensource.org/licenses) 的解释，开源许可证（Open source licenses）是指那些符合 [OSD（开源定义，Open Source Definition）](https://opensource.org/osd) 的许可证 —— 简单来说，这些许可证允许软件被自由的使用，修改和分发。

广义来讲，开源许可证是指*一种被用于计算机软件或其他产品的，允许在指定的条款内使用，修改和/或分发其源代码，蓝图或设计的许可证*[^1]。一般来讲，我们说的开源许可证是指广义的开源许可证释义。

通俗来讲的话，开源许可证就是一种允许我们在一定条件内按照我们的需要自由使用和修改软件及其源代码的法律条款，籍此条款，这个软件的作者（可能是一个人，也可能是很多人）可以将这些权利许可给我们，并告知我们一些使用限制。这些条款有时由个人起草，有时由商业公司起草，但最广泛使用的是由非营利组织（例如 [自由软件基金会，FSF](https://fsf.org)）起草的各种开源许可证，通常情况下，作为开发者的我们可以通过按照这些许可证的要求放置许可证条款（有的许可证可能有别的要求，也有可能没有要求）来声明我们**基于这些许可证开源**。

需要注意的是，使用开源许可证并不意味着单纯的限制使用者，对于一些许可证（例如下文将会提到的 GPL 协议），他们也会限制您（开发者）的行为。因此，选择一个合适的许可证是十分重要的。

#### 小提示：开源不等于放弃版权

拥有版权（Copyright）意味着你对你开发的软件及其源代码拥有著作权，所有权和其他法定权利，使用一个开源协议并不意味着放弃版权，它仅意味着**您将您在许可证许可的这部分软件（及其源代码）副本的一部分权利（例如，专利权）让渡给软件使用者和其他开发者，并在可能的情况下放弃一些权利（例如，针对软件破解和修改的起诉权）**，这仅对您使用指定许可证开源的软件（及其源代码）副本有效，也就是说，对于您手上那部分未使用任何开源许可证开源的软件（及其源代码）来说，您仍然拥有包括版权在内的一切权利（无论您手上的那部分和您发布出去的副本是否相同）。

从另一个角度来讲，开源许可证作为法律条款之所以能工作，正是因为您本身拥有一个软件的版权和著作权：如果您不是这些软件的作者，那么开源也就无从谈起（当然，这不意味着您必须对您的程序主张版权）。

### 自由软件许可证

根据 FSF 的解释，“自由软件”是指尊重用户自由和社区的软件。粗略地说，这意味着**用户可以自由运行，复制，分发，研究，更改和改进软件**。[^2] 而自由软件许可证通过法律协议，保障使用者的四大基本自由[^3]。

通常情况下，**自由软件许可证都是（狭义的）开源许可证**。

#### Copyleft 许可证

对于 copyleft 一词的中文翻译有很多种，例如“版权相左”，“版权所无”，“著佐权”，但是无论如何，我们能发现其与 "copyright（版权）"一词恰好相反，这意味着 copyleft 许可证与版权的巨大对立。Copyleft 许可证是自由软件许可证中的一种，它旨在通过一些限制，给予用户更多自由。

虽然我们还没有开始讲述详细的许可证文本，但是你将会发现，由于通常的开源许可证偏向于给予使用者几乎所有权力，这也包含了*闭源的权利*。如何理解？*假设有软件 A，基于某种简单全权许可证开源，这时，一个商业公司看中了这个软件，并基于此软件进行修改得到了软件 B，这时这个商业公司完全可以不向公众发布这个软件 B 的源代码 —— 他有权利这么做，但是，这也就意味着其他开发者失去了对于这个软件 A的“改进版本”（也就是软件 B）的**自由***。Copyleft 许可证通过条款限制，要求**程序的所有修改和扩展版本也是自由的**，为用户争取到了这一自由。

> *专有软件开发商使用版权来剥夺用户的自由；我们使用版权来保证他们的自由。这就是为什么我们颠倒了名称，将“版权”改为“copyleft”。*

当然，仍要提到的是，使用 Copyleft 许可证依然不意味着放弃版权（当然，在本地法律允许的条件下，你可以这么做）。

> *Copyleft 是一种在程序上使用版权的方式。这并不意味着放弃版权；事实上，这样做会使copyleft变得不可能。“copyleft”中的“left”不是对动词“离开”的引用，而只是指向“right”镜像的方向。*

#### 小提示：copyleft 许可证不排斥商业化使用

Copyleft 许可证的诞生虽然是为了抵制商业公司通过闭源的方式妨碍用户修改和访问软件源代码的自由，但是这并不意味着 copyleft 许可证是排斥商业化使用的，事实上，**copyleft 许可证所许可的软件应该允许任何人使用他们，也包括商业公司**。但是，这些商业公司在使用这些 copyleft 软件时，也应当受到这些 copyleft 许可证条款的制约。



了解了开源许可证的概念，接下来，我们将详细介绍一些主流的开源许可证及其与其他许可证之间的区别。

## 主流开源许可证及其区别

一般来讲，我们可以将主流许可协议分为两个部分，copyleft license（copyleft 许可证）和 permissive license（宽松许可证）。相比 copyleft 许可证，宽松许可证对软件的再分发限制更加宽容，即不要求公开源代码。

当我们谈到如何使用这些开源许可证时，事实上，几乎所有主流许可证都会要求你提供这些许可证自身的完整内容到你的项目中 —— 通常情况，我们会创建一个 "LICENSE" 文件，并填入完整的许可证条款。当然，对于不同的许可证，会有额外的要求，这些要求将会在下方被详细提及。

下文中，我们将会着重介绍 copyleft 许可证，并提及这些许可证**与其他许可证的兼容性**，简单来说，如果两个许可证可以被称作是**兼容的**，这就意味着这两个许可证所分别许可的作品可以组合成一个更大的作品（此时，这个更大的作品可能采用一个共同的新许可证，也可能依然以不同区块分别许可）。

### Copyleft 许可证

比较常用且著名的 copyleft 许可证即为由 FSF 组织发布的，以 GPL 为首的一系列自由软件许可证，接下来，我们将着重介绍这些许可证。

在 GPL 系列许可证中，存在一个 "X 或以后版本" 的概念，例如 "GPLv2 或以后版本"。这意味着，当我们声明一个项目基于 "GPLv2" 许可时，我们必须严格按照 GPLv2 协议中对代码使用的要求进行许可；但是，当我们声明其基于 "GPLv2 或以后版本" 许可，当其他人在试图合并他的代码和您的代码时，它们将可以按照更新的 "GPLv3" 协议对代码使用的要求进行许可，即使两个 GPL 协议之间本身并不互相兼容。

##### 小提示：理解“合并/组合代码”

根据 [GNU 组织关于"主程序与其插件何时被视为单个组合程序"的解释](https://www.gnu.org/licenses/gpl-faq.html#GPLPlugins)：

> 这取决于主程序如何调用其插件。如果主程序使用 fork 和 exec 来调用插件，并且它们通过共享复杂的数据结构或相互传递复杂的数据结构来建立亲密的通信，则可以使它们成为一个单一的组合程序。使用简单 fork 和 exec 调用插件且未在它们之间建立密切通信的主程序会导致插件成为单独的程序。
>
> 如果主程序动态链接插件，并且它们相互调用函数并共享数据结构，我们认为它们形成一个单一的组合程序，必须将其视为主程序和插件的扩展。如果主程序动态链接插件，但它们之间的通信仅限于使用某些选项调用插件的“main”函数并等待它返回，则属于临界情况。
>
> 使用共享内存与复杂的数据结构进行通信几乎等同于动态链接。

##### 小提示：理解“明确声明”

有的简单全权许可证因为其许可条款十分短小简单，可能会造成很多模糊 —— 有时候，某些权利并未显式授予您，但实际上您拥有这些权利，例如专利权；反之，有些权利并未显式告知限制，但实际上您不拥有这些权利，例如商标权。如果你的项目十分重要，那么选择一个更加复杂正式的协议可能更好一些（反之，有的小型程序代码可能比协议文本还短，这个时候建议使用一些简单的许可证）。

#### GNU General Public License v3.0

[协议原文](https://www.gnu.org/licenses/gpl-3.0-standalone.html) | [非官方翻译](https://jxself.org/translations/gpl-3.zh.shtml)

GNU 通用公共许可证第三版（简称 GNU GPLv3，或 GPLv3）是截至目前最新版的 GPL 协议，它发布于 `29 June 2007`，他相比上一个版本（GPLv2，接下来会提到）提供了些许宽松，并且规范了一些法律术语，同时为软件提供了一些更加有力的保护。GPLv3 是目前使用最广泛的主流 copyleft 许可证之一。

##### 条款简述

在 GPLv3 协议许可下，您可以：

- 商业化使用（这意味着，您可以出于商业目的使用这些源代码）
- 再分发（这意味着，您可以将源代码副本传输给其他任何人）
- 修改（这意味着，您可以修改源代码）
- 专利使用（这意味着，版权人**明确声明**授予您专利使用权）
- 私人使用（这意味着，您可以出于一切目的私下使用和修改源代码）

唯须遵守以下条款：

- 披露源码（这意味着，分发软件时，您必须提供源代码）
- 协议和版权通知（这意味着，软件中必须包含许可证和版权声明的副本）
- 相同许可证共享（这意味着，如果您修改并再分发软件，您必须使用相同许可证分发；在一定条件下，还可以使用类似或相关的许可证）
- 状态更改说明（如果您更改软件，您应当提供适当的说明）

除此之外，该软件：

- 提供责任限制（版权人声明不对使用者造成的任何损失负责）
- 不提供任何担保（版权人声明不为该软件的品质提供任何担保）

##### 详细介绍

> Tips: 详细介绍是出于对许可证原文的简化或可读性描写，它们不是任何法律条款，也不是协议的一部分，只是作者对该协议的一些解释。

GPLv3 许可证许可任何人使用，修改和分发程序及其源代码，这包括：

- 转发完整副本。同时为每一个副本标明版权声明；保留一切免责声明；提供 GPLv3 协议的完整副本且完整保留所有附加条款（下文会提到）
- 转发修改过的源码版本。但你必须提供醒目的修改声明并为其标注日期；必须使用本协议为整个程序授权，而不是某一个部分；如果该程序包含有交互式用户界面，则必须显示适当的法律声明（例外的情况是，如果这个程序原版有交互式用户界面，但未提供法律声明，则你也无须提供）
- 以非源码形式转发。但你应当通过适当方式，在适当地点，为任何可以获得该程序非源码形式的用户提供其源代码

GPLv3 允许你在 GPLv3 协议之外添加一些附加许可，这些附加许可以在转发程序时被选择性删除，这些可能的附加许可包括：

- 表示不提供品质担保或有超出协议要求的责任。
- 要求在此材料中或在适当的法律声明中保留特定的合理法律声明或创作印记。
- 禁止误传材料的起源，或要求合理标示修改以别于原版。
- 限制以宣传为目的使用该材料的作者或授权人的名号。
- 降低约束以便赋予在商标法下使用商品名、商品标识及服务标识。
- 要求任何转发该材料（或其修改版）并对接收者提供契约性责任许诺的人，保证这种许诺不会给作者或授权人带来连带责任。

除此之外的许可并不被允许和 GPLv3 协议共存，如果你看到软件声明了那些额外的许可，你可以去掉他们。

GPLv3 **明确授予**使用者专利权。

GPLv3 *保护用户的合法权益免受反破解法限制*，这意味着当你转发一个受保护作品时，你将会失去任何限制他人破解该作品的权利。

GPLv3 不允许您将您的程序与私有程序合并。

##### 兼容性

- GPLv3 与 LGPLv2.1，LGPLv3 兼容，这个情况下，整个作品基于 GPLv3 许可；例外的，当该 LGPLv2.1 或 LGPLv3 内容被以类库引用方式与 GPLv3 许可作品合并时，该类库仍可基于 LGPLv2.1 或 LGPLv3 许可；
- GPLv3 与 AGPLv3 兼容，这个情况下，整个作品基于 GPLv3 许可，但应当适用 AGPLv3 中关于网络交互的特别要求（下文会提到）；
- GPLv3 与 MIT License，Apache License 2.0，Unlicense，WTFPL 兼容，这个情况下，整个作品基于 GPLv3 许可；
- GPLv3 与 BSD 3-Clause "New" or "Revised" License（Modified BSD），BSD 2-Clause "Simplified" License（FreeBSD），BSD Zero Clause License 兼容，这个情况下，整个作品基于 GPLv3 许可；
- GPLv3 与 BSD 3-Clause Clear License（Clear BSD） 兼容，但是由于后者明确不授予专利权，因此可能引发某些专利问题，因此不建议与之合并[^4]；
- GPLv3 与 MPL 2.0 兼容，这个情况下，先前由 MPL 2.0 许可的作品部分使用 MPL 2.0 和 GPLv3 双重许可，整个作品基于 GPLv3 许可[^5]；
- GPLv3 与 CC-BY 4.0 兼容，这个情况下，整个作品基于 GPLv3 许可；
- GPLv3 与 CC-BY-SA 4.0 **单向兼容**[^6]，这个情况下，整个作品基于 GPLv3 许可；
- GPLv3 与 CC0 兼容，这个情况下，整个作品基于 GPLv3 许可；
- GPLv3 与 GPLv2 不兼容（但是，GPLv3 与被声明为适用于 "GPLv2 或以后版本" 的 GPLv2 协议兼容，并使整个作品基于 GPLv3 许可）；
- GPLv3 与 BSD 4-Clause "Original" or "Old" License（Original BSD） 不兼容；
- GPLv3 与 CC-BY-NC，CC-BY-ND 不兼容。

##### 如何使用

通常情况下的做法是，在你的源代码根目录中创建一个文本文件（GNU 建议命名为 `COPYING`，通常情况下，也可以使用 `LICENSE`），将 GPLv3 的完整许可证文本复制到该文件中。

可选的，你可以在每个文件的顶部添加模板版权声明，这些版权声明也可以在许可证原文底部找到：

```
    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.
```

如果你的程序拥有交互界面（这里指的是 CLI），你应该通过一种方式输出一个简短的版权声明：

```
    <program>  Copyright (C) <year>  <name of author>
    This program comes with ABSOLUTELY NO WARRANTY; for details type `show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type `show c' for details.
```

如果你的程序使用 GUI 交互界面，则可以将其放在“关于”栏目中。

如果你之上存在雇主或校方，你还应当让他们在必要时为此程序签署放弃版权声明。

##### 小提示：如何理解 GPLv3 中对源代码再分发的要求

有时候很多人会对 GPLv3 中源代码再分发的要求产生误解，认为 GPLv3 就是必须将软件和源代码免费公布给所有人，其实这个观点这是错误的：首先 GPL 不排斥商业化，因此你完全可以付费出售你的软件，但是前提是这些软件中必须附带（或许可在未来一段时间内通过网络提供）这些软件的源代码 —— 此时，你不能限制这些购买了你软件的人修改这些源代码或是将这些源代码免费/付费发布给其他人；同时需要注意的是，使用 GPLv3 协议也不意味着你必须将你的软件和源代码公布给所有人，你可以只向你的付费用户公布它们，或是另一家购买你软件的公司（同样，你依然不能阻止这些人根据协议再分发你的软件及其源代码）。

一个例外是，这个软件如果只在你个人，团队，甚至是公司内部使用，那么这些软件源代码应当适用于私人使用许可，这也就意味着，你无需按照 GPL 的要求将它们公开。

#### GNU General Public License v2.0

[协议原文](https://www.gnu.org/licenses/old-licenses/gpl-2.0-standalone.html) | [非官方翻译](https://jxself.org/translations/gpl-2.zh.shtml)

GNU 通用公共许可证第二版（简称 GNU GPLv2，或 GPLv2）是上一版的 GPL 协议，事实上在大部分情况下，你不应该使用这个协议，而应当使用 GPLv3，但是鉴于一些老的软件仍在使用 GPLv2 授权，在此一并提及，但不作详细介绍。

GPLv2 未向使用者提供明确的专利授权，且未声明保护用户破解软件的权利。同时，GPLv2 不允许提供任何 GPLv2 协议之外的附加许可。

GPLv2 不允许您将您的程序与私有程序合并。

##### 兼容性

- GPLv2 与 LGPLv2.1 兼容，这个情况下，整个作品基于 GPLv2 许可；例外的，当该 LGPLv2.1 内容被以类库引用方式与 GPLv2 许可作品合并时，该类库仍可基于 LGPLv2.1 许可；
- GPLv2 与 MIT License，Unlicense，WTFPL 兼容，这个情况下，整个作品基于 GPLv2 许可；
- GPLv2 与 BSD 3-Clause "New" or "Revised" License（Modified BSD），BSD 2-Clause "Simplified" License（FreeBSD），BSD Zero Clause License 兼容，这个情况下，整个作品基于 GPLv2 许可；
- GPLv2 与 BSD 3-Clause Clear License（Clear BSD） 兼容，但是由于后者明确不授予专利权，因此可能引发某些专利问题，因此不建议与之合并[^4]；
- GPLv2 与 MPL 2.0 兼容，这个情况下，先前由 MPL 2.0 许可的作品部分使用 MPL 2.0 和 GPLv2 双重许可，整个作品基于 GPLv2 许可[^5]；
- GPLv2 与 CC-BY 4.0 兼容，这个情况下，整个作品基于 GPLv2 许可；
- GPLv2 与 CC0 兼容，这个情况下，整个作品基于 GPLv2 许可；
- GPLv2 与 GPLv3 不兼容（但是，被声明为适用于 "GPLv2 或以后版本" 的 GPLv2 协议 与 GPLv3 兼容，并使整个作品基于 GPLv3 许可）；
- GPLv2 与 LGPLv3 不兼容（但是，被声明为适用于 "GPLv2 或以后版本" 的 GPLv2 协议 与 LGPLv3 兼容，并使整个作品基于 GPLv3 许可）；
- GPLv2 与 AGPLv3 不兼容；
- GPLv2 与 Apache License 2.0 不兼容；
- GPLv2 与 BSD 4-Clause "Original" or "Old" License（Original BSD） 不兼容；
- GPLv2 与 CC BY-SA 4.0，CC-BY-NC，CC-BY-ND 不兼容。

#### GNU Lesser General Public License v3.0

[协议原文](https://www.gnu.org/licenses/lgpl-3.0-standalone.html) | [非官方翻译（不推荐）](http://www.thebigfly.com/gnu/lgpl/lgpl-v3.php)

与 GPLv3 这样的"强 copyleft 许可证（strong copyleft license）"相对的，GNU 宽通用公共许可证第三版（简称 GNU LGPLv3，或 LGPLv3）是一种弱 copyleft 许可证（weak copyleft license），常用于各种类库（依赖库），其本质上是在 GPLv3 上增加的额外条款，作为一种例外，LGPLv3 豁免您的软件使用者**在以类库引用（link）的方式使用 LGPL 许可的作品时可以不必开源**。

当然，由于其弱 copyleft 的性质，GNU 组织认为 LGPL 实际上是一种妥协，并建议您[不要在您的下一个库中使用 LGPL](https://www.gnu.org/licenses/why-not-lgpl.html)。

##### 条款简述

在 LGPLv3 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 专利使用
- 私人使用

唯须遵守以下条款：

- 披露源码
- 协议和版权通知
- **有条件的相同许可证共享（见下）**
- 状态更改说明

除此之外，该软件：

- 提供责任限制
- 不提供任何担保

##### 详细介绍

当使用 LGPLv3 许可证时，您实际上同样应当遵循 GPLv3 协议的条款，并辅以以下例外和附加条件：

- 对于以库头文件部分作为目标代码合并时，你可以选择下述两个条款之一对这部分代码进行分发：
  - 在目标代码的每个副本中明确声明库在其中使用，并且该库及其使用受 LGPLv3 许可证的约束；
  - 在目标代码中附上 GNU GPL 和 LGPLv3 许可证文档的副本。
- 对于组合作品，您需要：
  - 在组合作品的每份副本上明确声明，其中使用了该库，并且该库及其使用受 LGPLv3 许可证的约束；
  - 在组合作品中附上 GNU GPL 和 LGPLv3 许可证文档的副本；
  - 对于在执行期间显示版权声明的组合作品，请在这些声明中包括库的版权声明，以及将用户引导至 GNU GPL 副本和 LGPLv3 许可证文档的引用；
  - 执行下列操作之一：
    - 根据 LGPLv3 的条款，通过适当的形式允许用户将应用程序与链接库的修改版本重新组合或重新链接以产生修改后的组合作品，以代表您遵照 GPL 条款中 “以非源码形式转发” 作品。
    - 使用合适的共享库机制与库链接。合适的机制是指在运行时使用用户计算机系统上已经存在的库的副本，并且库的修改版可以正常工作并且与链接版本兼容。
  - 您不得限制您组合作品中该库这部分的修改和逆向调试。

- 通过以上两种情况下发布的合并软件，不受 GPL 对保护用户的合法权益免受反破解法限制的条款保护；
- 如果您试图分发修改版的本软件，且有某个应用程序引用了本软件提供的功能（而不是通过传递命令行参数的方式），那么您必须选择下列操作之一：
  - 根据 LGPLv3 许可证要求，前提是您做出真诚的努力，以确保在应用程序不提供功能或数据的情况下，该软件仍在运行，且执行其目的的任何部分仍然有意义；
  - 使用 GPL 协议授权本软件。
- 如果您试图将本库与另一个不受 LGPLv3 协议许可的库合并，那么您必须选择下列操作之一：
  - 在组合库中附带一份不与任何其他库组合的，基于该库的相同作品的副本，并根据 LGPLv3 许可证的条款分发；
  - 在组合库中给出醒目的通知，说明它的一部分是基于该库的作品，并解释在哪里可以找到相同作品的未组合形式。

##### 兼容性

- LGPLv3 与 GPLv3 兼容，这个情况下，整个作品基于 GPLv3 许可；
- LGPLv3 与 LGPLv2.1 兼容，这个情况下，基于 LGPLv2.1 许可代码须以 GPLv3 许可分发（但是，LGPLv3 与被声明为 "LGPLv2.1 或以后版本" 的 LGPLv2.1 协议，或当该 LGPLv2.1 作品被以类库引用方式与 LGPLv3 许可作品合并时兼容）;
- LGPLv3 与 AGPLv3 兼容，这个情况下，整个作品基于 GPLv3 许可，但应当适用 AGPLv3 中关于网络交互的特别要求（下文会提到）；
- LGPLv3 与 MIT License，Apache License 2.0，Unlicense，WTFPL 兼容，这个情况下，整个作品基于 LGPLv3 许可；例外的，当该 LGPLv3 内容被以类库引用方式与这些许可证许可作品合并时，仅该类库基于 LGPLv3 许可；
- LGPLv3 与 BSD 3-Clause "New" or "Revised" License（Modified BSD），BSD 2-Clause "Simplified" License（FreeBSD），BSD Zero Clause License 兼容，这个情况下，整个作品基于 LGPLv3 许可；例外的，当该 LGPLv3 内容被以类库引用方式与这些许可证许可作品合并时，仅该类库基于 LGPLv3 许可；
- LGPLv3 与 BSD 3-Clause Clear License（Clear BSD） 兼容，但是由于后者明确不授予专利权，因此可能引发某些专利问题，因此不建议与之合并[^4]；
- LGPLv3 与 MPL 2.0 兼容，这个情况下，先前由 MPL 2.0 许可的作品部分使用 MPL 2.0 和 LGPLv3 双重许可，整个作品基于 LGPLv3 许可[^5]；例外的，当该 LGPLv3 内容被以类库引用方式与这些许可证许可作品合并时，仅该类库基于 LGPLv3 许可；
- LGPLv3 与 CC-BY 4.0 兼容，这个情况下，整个作品基于 LGPLv3 许可；例外的，当该 LGPLv3 内容被以类库引用方式与这些许可证许可作品合并时，仅该类库基于 LGPLv3 许可；
- LGPLv3 与 CC-BY-SA 4.0 **单向兼容**[^6]，这个情况下，整个作品基于 LGPLv3 许可；例外的，当该 LGPLv3 内容被以类库引用方式与这些许可证许可作品合并时，仅该类库基于 LGPLv3 许可；
- LGPLv3 与 CC0 兼容，这个情况下，整个作品基于 GPLv3 许可；例外的，当该 LGPLv3 内容被以类库引用方式与这些许可证许可作品合并时，仅该类库基于 LGPLv3 许可；
- LGPLv3 与 GPLv2 不兼容（但是，LGPLv3 与被声明为适用于 "GPLv2 或以后版本" 的 GPLv2 协议兼容，并使整个作品基于 GPLv3 许可）；
- GPLv3 与 BSD 4-Clause "Original" or "Old" License（Original BSD） 不兼容；
- GPLv3 与 CC-BY-NC，CC-BY-ND 不兼容。

##### 如何使用

按照 GPLv3 协议的使用方法应用 GPLv3 协议，然后创建 `COPYING.LESSER` 文件，将 LGPLv3 的完整许可证文本复制到该文件中。（但是有时，我们也通过直接将 [LGPL+GPL](https://www.gnu.org/licenses/lgpl+gpl-3.0.txt) 放入同一个 `LICENSE` 或 `COPYING` 文件中来使用）。然后，您可仿照上文 GPLv3 协议的本部分内容，添加一些可选的附加许可，此处不再赘述。

#### GNU Affero General Public License v3.0

[协议原文](https://www.gnu.org/licenses/agpl-3.0-standalone.html) | [非官方翻译](https://www.chinasona.org/gnu/agpl-3.0-cn.html)

GNU Affero 通用公共许可证第三版（简称 GNU AGPLv3，或 AGPLv3）发布于 `19 November 2007`，作为一种比 GPL 协议更加严格的 copyleft 协议，它催生于一个新的互联网环境 —— 客户端软件逐渐被 Web 浏览器前端+后端软件取代，由于 GPL 协议生效的一个主要要求是 “发布”，但是通过后端向用户提供服务，这部分后端代码并未直接向用户提供，因此按照 GPL 协议无须公开其修改版本。AGPL 就是为了修补这一个漏洞 —— 它要求网络服务器的运营商向该服务器的用户提供运行在那里的修改版本的源代码。因此，只要有人在一个可公开访问的服务器上公开使用一个修改过的版本，公众将能够获得修改过的版本的源代码。

AGPLv3 协议主体基于 GPLv3 协议修改，并加入了远程网络交互和与 GPLv3 兼容的相关内容。在此，我们仅介绍这一部分，对其他主体部分一概省略。

##### 条款简述

在 AGPLv3 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 专利使用
- 私人使用

唯须遵守以下条款：

- 披露源码
- 协议和版权通知
- **网络使用视为分发（这意味着，通过网络与软件交互的用户有权获得其源代码的副本）**
- 相同许可证共享
- 状态更改说明

除此之外，该软件：

- 提供责任限制
- 限制商标使用（这意味着版权人**明确声明**其不授予您商标权）
- 不提供任何担保

##### 详细介绍

除去 GPLv3 协议中对您的类似要求外，您仍需注意以下 AGPLv3 协议中关于网络交互的特别要求：

- 如果您修改本程序，您的修改版本必须在显著位置向所有通过计算机网络远程与本程序交互的用户（如果您的版本支持这种交互）提供机会，从网络服务器上免费提供相应的源码。相应源码应包括根据下段规定纳入 GPLv3 许可证的的任何作品相应源码；
- 您有权将任何受 AGPLv3 协议许可的作品与受 GPLv3 协议许可的作品合并为一个单一作品并分发，本许可证仍保护原作品部分，但合并后的完整作品将受 GPLv3 协议管辖。

##### 兼容性

- AGPLv3 与 LGPLv2.1，LGPLv3 兼容，这个情况下，整个作品基于 AGPLv3 许可；例外的，当该 LGPLv2.1 或 LGPLv3 内容被以类库引用方式与 AGPLv3 许可作品合并时，该类库仍可基于 LGPLv2.1 或 LGPLv3 许可；
- AGPLv3 与 GPLv3 兼容，这个情况下，整个作品基于 GPLv3 许可，但应当适用 AGPLv3 中关于网络交互的特别要求（见上）；
- AGPLv3 与 MIT License，Apache License 2.0，Unlicense，WTFPL 兼容，这个情况下，整个作品基于 AGPLv3 许可
- AGPLv3 与 BSD 3-Clause "New" or "Revised" License（Modified BSD），BSD 2-Clause "Simplified" License（FreeBSD），BSD Zero Clause License 兼容，这个情况下，整个作品基于 AGPLv3 许可；
- AGPLv3 与 BSD 3-Clause Clear License（Clear BSD） 兼容，但是由于后者明确不授予专利权，因此可能引发某些专利问题，因此不建议与之合并[^4]；
- AGPLv3 与 MPL 2.0 兼容，这个情况下，先前由 MPL 2.0 许可的作品部分使用 MPL 2.0 和 AGPLv3 双重许可，整个作品基于 AGPLv3 许可[^5]；
- AGPLv3 与 CC-BY 4.0 兼容，这个情况下，整个作品基于 AGPLv3 许可；
- AGPLv3 与 CC-BY-SA 4.0 **单向兼容**[^6]，这个情况下，整个作品基于 AGPLv3 许可；
- AGPLv3 与 CC0 兼容，这个情况下，整个作品基于 AGPLv3 许可；
- AGPLv3 与 GPLv2 不兼容；
- AGPLv3 与 BSD 4-Clause "Original" or "Old" License（Original BSD） 不兼容；
- AGPLv3 与 CC-BY-NC，CC-BY-ND 不兼容。

##### 如何使用

通常情况下的做法是，在你的源代码根目录中创建一个文本文件（通常情况下，也可以使用 `LICENSE` 或 `LICENSE.txt`），将 AGPLv3 的完整许可证文本复制到该文件中。然后，您可仿照上文 GPLv3 协议的本部分内容，添加一些可选的附加许可，此处不再赘述。

#### Mozilla Public License 2.0

[协议原文](https://www.mozilla.org/en-US/MPL/2.0/)

Mozilla 公共许可证第二版（简称 MPL2.0）是一个弱 copyleft 许可证，但是其条款的特殊性质又使其更像一个宽松许可证（甚至，有人专门创造了词语 `copycenter` 来描述这一类许可证），该许可证虽然要求软件源代码需要使用相同许可证进行分发，但是对于可执行软件和包含本软件的大型作品的协议做出了宽松的要求。

MPL2.0 被设计为兼容 GPL 的：其定义了“次要许可证”的概念：这些许可证包含 GPLv2，LGPLv2.1，AGPLv3 及其所有后续版本。对于在合并作品中使用与这些许可证不兼容的许可证时，MPL2.0 额外允许您根据这些次要许可证分发此类作品，且无须公开源代码。

##### 条款简述

在 MPL2.0 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 专利使用
- 私人使用

唯须遵守以下条款：

- 披露源码
- 协议和版权通知
- **有条件的相同许可证共享（见下）**

除此之外，该软件：

- 提供责任限制
- 限制商标使用
- 不提供任何担保

##### 详细介绍

MPL2.0 许可证许可任何人使用，修改和分发程序及其源代码，额外的：

- 任何贡献者均不会因您选择根据 MPL2.0 的后续版本或根据次要许可证的条款（如果允许）分发本软件而授予额外的授权；
- 所有以源代码形式分发的软件均应遵守 MPL2.0 许可证的条款。您必须告知接收者，软件的源代码形式受 MPL2.0 许可证条款的约束，以及他们如何获取 MPL2.0 许可证的副本。您不得尝试在源代码中更改或限制收件人的权利；
- 以可执行文件形式分发的软件仍应同上述条款提供其源代码形式，且您即可以根据 MPL2.0 许可证，也可以根据其他不同的许可证对该软件的可执行文件形式进行再许可，前提是可执行软件的许可证不试图限制或更改接收者在 MPL2.0 许可证下在软件源代码部分中的权利；
- 如果您打算分发一个合并作品，且该合并作品是该软件和受一个或多个次要许可证管辖的作品的组合，并且该软件与次要许可证不见容，则 MPL2.0 允许您根据此类次要许可证的条款额外分发本软件以便大型作品的开发者可以，根据他们的选择，使用 MPL2.0 或此类次要许可证的条款进一步分发该软件。

##### 兼容性

MPL 2.0 协议理论上兼容所有协议，但当您要合并的许可证与 MPL 2.0 协议中定义的“次要许可证”（见上）不兼容时，您应当再分发源代码时提供一个额外的声明，以证明您使用了不兼容的许可证，这些额外声明也可以在许可证原文底部找到：
```
This Source Code Form is “Incompatible With Secondary Licenses”, as defined by the Mozilla Public License, v. 2.0.
```

##### 如何使用

通常情况下的做法是，在你的源代码根目录中创建一个文本文件（通常情况下，也可以使用 `LICENSE` 或 `LICENSE.txt`），将 MPL2.0 的完整许可证文本复制到该文件中。额外的，Mozilla 基金会建议在每个文件的顶部添加模板版权声明，这些版权声明也可以在许可证原文底部找到：

```
This Source Code Form is subject to the terms of the Mozilla Public License, v. 2.0. If a copy of the MPL was not distributed with this file, You can obtain one at https://mozilla.org/MPL/2.0/.
```

### 宽松许可证

宽松许可证中的宽松并不意味着 LGPL 中的 "宽松"，相反，宽松许可证试图通过给予直接用户更多自由和更少的限制，但这么做却放弃了间接用户的自由。但是不可否认的是，宽松许可证的开源方式因为成功拉拢到了商业公司的支持，成功且有效的推进了开源进程，壮大了开源生态，并使其成为了开源世界的主流许可证类型。

#### MIT License

[协议原文](https://mit-license.org/)

MIT License（GNU 组织称之为 Expat License[^7]）是麻省理工学院提供的一种简单全权许可证，该协议非常短小，同时也十分宽松：除了基本的保留协议文本以外，其只要求下游使用者保留署名。

##### 条款简述

在 MIT License 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 私人使用

唯须遵守以下条款：

- 协议和版权通知

除此之外，该软件：

- 提供责任限制
- 不提供任何担保

##### 如何使用

通常情况下的做法是，在你的源代码根目录中创建一个文本文件（通常情况下，也可以使用 `LICENSE` 或 `LICENSE.txt`），将 MIT License 的完整许可证文本复制到该文件中。将 `[year]` 替换为当前年份，将 `[fullname]` 替换为版权所有者的姓名。

#### Apache License 2.0

[协议原文](https://www.apache.org/licenses/LICENSE-2.0.html)

Apache License 2.0 是由 Apache 基金会发布的一种宽松许可证，其与 MIT License 一样宽松，但是协议条款更加复杂正式。Apache License 2.0 相比 MIT License **明确**提供了专利使用许可，但也**明确**限制了商标使用。

##### 条款简述

在 Apache License 2.0 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 专利使用
- 私人使用

唯须遵守以下条款：

- 协议和版权通知
- 状态更改说明

除此之外，该软件：

- 提供责任限制
- 限制商标使用
- 不提供任何担保

##### 如何使用

通常情况下的做法是，在你的源代码根目录中创建一个文本文件（通常情况下，也可以使用 `LICENSE` 或 `LICENSE.txt`），将 Apache License 2.0 的完整许可证文本复制到该文件中。额外的，Apache 基金会建议在每个文件的顶部添加模板版权声明，这些版权声明也可以在许可证原文底部找到：

```
   Copyright [yyyy] [name of copyright owner]

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

#### BSD Licenses*

BSD License 最初是一种用于授权伯克利软件包（**B**erkeley **S**oftware **D**istribution）的宽松许可证。但由于 BSD License 存在多个变种，且其名称都被称作 `BSD License`，并且这几个变种之间变化并不大，因此将其放在一起介绍。事实上，有五个 BSD 许可证，后来它们被赋予了不同的名字。

##### BSD 4-Clause "Original" or "Old" License（Original BSD）

BSD 四段 "原版" 或 "旧版" 许可证（又称 Original BSD）是最初广为流传的 BSD 许可证，其内容十分简单：

```
BSD 4-Clause License

Copyright (c) [year], [fullname]
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

3. All advertising materials mentioning features or use of this software must
   display the following acknowledgement:
     This product includes software developed by [project].

4. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY COPYRIGHT HOLDER "AS IS" AND ANY EXPRESS OR
IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
EVENT SHALL COPYRIGHT HOLDER BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

和 MIT License 相似，其简单要求使用者在分发源代码和二进制文件时保留协议原文，除此之外，其声明了有关版权人姓名使用的限制和另外一个饱受诟病[^8]的“第三段条款”——要求所有广告材料中必须包含一句“本软件基于 [项目名] 项目开发”。这看起来并没有什么问题，但是当一个软件由多个上游项目组成，而人们将不得不无限拓展这句话的时候，就十分令人懊恼了。事实上，这句额外的要求也导致了 Original BSD 协议与 GPL 不兼容[^8]。

于是后来，一个改进版的 BSD License 产生了。

##### BSD 3-Clause "New" or "Revised" License

BSD 三段 "新的" 或 "修订" 许可证（又称 Modified BSD）与 Original BSD 唯一的区别就是删掉了那个 "令人讨厌的广告条款"：

```
BSD 3-Clause License

Copyright (c) [year], [fullname]

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

正因此，Modified BSD 得以与 GPL 兼容。

你以为这就结束了？不知道是不是因为 Modified BSD 删条款起了一个"坏头"，更多的变种产生了...

##### BSD 3-Clause Clear License

BSD 三段清晰许可证（又称 Clear BSD）基于 Modified BSD 进一步微调了条款，简化了一部分内容，删除了保留所有权利（All rights reserved）提示，并在免责声明部分添加了一个专利条款，**明确声明**其不授予专利权：

```
The Clear BSD License

Copyright (c) [year] [fullname]
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted (subject to the limitations in the disclaimer
below) provided that the following conditions are met:

     * Redistributions of source code must retain the above copyright notice,
     this list of conditions and the following disclaimer.

     * Redistributions in binary form must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

     * Neither the name of the copyright holder nor the names of its
     contributors may be used to endorse or promote products derived from this
     software without specific prior written permission.

NO EXPRESS OR IMPLIED LICENSES TO ANY PARTY'S PATENT RIGHTS ARE GRANTED BY
THIS LICENSE. THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND
CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR
BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER
IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.
```

##### BSD 2-Clause "Simplified" License

BSD 两段 "简化" 许可证（又称 FreeBSD）进一步从 Modified BSD 上删除了有关版权人姓名使用的限制，只留下了源代码和二进制再分发要求：

```
BSD 2-Clause License

Copyright (c) [year], [fullname]

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

有人想，既然已经简化到这个地步了，那干脆不如...

##### BSD Zero Clause License

BSD 零段许可证直接删除了一切要求，允许您无限制的使用软件，甚至不需要保留任何版权和免责声明：

```
BSD Zero Clause License

Copyright (c) [year] [fullname]

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY
AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM
LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR
OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
PERFORMANCE OF THIS SOFTWARE.
```

##### 如何使用

这些 BSD 许可证的使用方法与 MIT 协议的用法完全相同：首先，在你的源代码根目录中创建一个文本文件（通常情况下，也可以使用 `LICENSE` 或 `LICENSE.txt`），将某一个 BSD 许可证的完整许可证文本复制到该文件中，然后，将 `[year]` 替换为当前年份，将 `[fullname]` 替换为版权所有者的姓名。

#### WTFPL

[协议原文](http://www.wtfpl.net/about/)

与其说 WTFPL 是一个正经许可证，不如说他是一个“搞笑许可证”，从其名称“**Do What The Fuck You Want To Public License**”就能看出来。这个协议的内容也很简单：**DO WHAT THE FUCK YOU WANT TO**。

虽然看起来很搞笑，但是其完全兼容 GPL（然而 GNU 建议使用 X11 或 Apache 2.0 协议代替这个模棱两可的协议[^9]）

##### 条款简述

在 WTFPL 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 私人使用

##### 如何使用

通常情况下的做法是，在你的源代码根目录中创建一个文本文件（通常情况下，也可以使用 `LICENSE` 或 `LICENSE.txt`），将 WTFPL 的完整许可证文本复制到该文件中。

### 其他许可证

虽然我们讨论的主要内容是“开源许可证”，但是事实上，这个世界上依然存在为其他劳动作品授权的许可证，有时候（例如当我们想要在一个游戏中合并一个音效或是贴图资源时）我们也不得不考虑这些协议与我们开源协议的兼容性。亦或者，您正在像我一样撰写一篇非常棒的文章，希望将其使用一种协议分发，那么，CC 协议一定是您的首选。

#### Unlicense

[协议原文](https://unlicense.org/)

The Unlicense 声明其将其授权的作品贡献至**[公有领域](https://en.wikipedia.org/wiki/Public_domain)**，这意味着**在法律允许的可能下放弃其包括著作权在内的一切权利**。

##### 条款简述

在 Unlicense 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 私人使用

除此之外，该软件：

- 提供责任限制
- 不提供任何担保

##### 如何使用

在源代码的根目录中创建一个文本文件（通常称为 `UNLICENSE` 或 `UNLICENSE.txt`），并将许可证免责声明的文本复制到该文件中。

#### CC0

[协议原文](https://creativecommons.org/publicdomain/zero/1.0/legalcode) | [概要](https://creativecommons.org/publicdomain/zero/1.0/deed.zh)

Creative Commons Zero v1.0 Universal（知识共享 CC0 1.0 通用）协议是由 Creative Commons（知识共享）组织发布的一种公共领域贡献许可证，其声明*将作品 **贡献** 至公共领域，在法律允许的范围，放弃所有他在全世界范围内基于著作权法对作品享有的权利，包括所有相关权利和邻接权利。*

##### 条款简述

在 CC0 协议许可下，您可以：

- 商业化使用
- 再分发
- 修改
- 私人使用

除此之外，该软件：

- 提供责任限制
- 限制专利使用
- 限制商标使用
- 不提供任何担保

##### 如何使用

我们建议您遵循 [CC0 (creativecommons.org)](https://creativecommons.org/choose/zero/?lang=zh) 网站的指引进行使用，*请注意，**这不是一个注册过程**，知识共享不会存储或保存您输入的任何信息。此工具将指导您完成生成包含嵌入元数据的 HTML 的过程，以便将您的工作标记为在 CC0 下可用。您的作品不会与 CC0 关联，也不会在 CC0 下提供，除非您将其标记为 CC0 发布。*

#### Creative Commons Licenses*

Creative Commons Licenses 是由 Creative Commons（知识共享）组织发布的一系列许可证的统称，*习惯上，我们将这一系列许可证称为 CC 许可证*。

CC 许可证有多个版本和多个变种。3.0 版本是一个早期版本，其特点是以一个未本地化版本（Unlocalized）为起点，针对全球各个国家和地区的当地法律制定了不同的版本（例如 CC BY 3.0 中国大陆 和 CC BY 3.0 美国）；在 4.0 版本中，Creative Commons 使用了一个统一的法律文件来代替先前版本的多个不同的本地化法律文件。在这里，我们主要介绍 CC 4.0 版本许可证。

一般来讲，CC 4.0 版本许可证有以下六个变种：

- **[CC BY 4.0 International](https://creativecommons.org/licenses/by/4.0/deed.zh)**（Attribution 4.0 International，署名 4.0 国际）
- **[CC BY-SA 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/deed.zh)**（Attribution-ShareAlike 4.0 International，署名-相同方式共享 4.0 国际）
- **[CC BY-ND 4.0 International](https://creativecommons.org/licenses/by-nd/4.0/deed.zh)**（Attribution-NoDerivatives 4.0 International，署名-禁止演绎 4.0 国际）
- [**CC BY-NC 4.0 International**](https://creativecommons.org/licenses/by-nc/4.0/deed.zh)（Attribution-NonCommercial 4.0 International，署名-非商业性使用 4.0 国际）
- **[CC BY-NC-SA 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh)**（Attribution-NonCommercial-ShareAlike 4.0 International，署名-非商业性使用-相同方式共享 4.0 国际）
- **[CC BY-NC-ND 4.0 International](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh)**（Attribution-NonCommercial-NoDerivatives 4.0 International，署名-非商业性使用-禁止演绎 4.0 国际）

可以看到，CC 许可证总的来说就是四个主要责任的互换，它们分别是**署名，相同方式共享，禁止演绎和非商业性使用**。

它们分别意味着：

- 署名：您必须给出适当的署名，提供指向本许可协议的链接，同时标明是否（对原始作品）作了修改。您可以用任何合理的方式来署名，但是不得以任何方式暗示许可人为您或您的使用背书。
- 相同方式共享：如果您再混合、转换或者基于本作品进行创作，您必须基于与原先许可协议相同的许可协议分发您贡献的作品。
- 禁止演绎： 如果您再混合、转换、或者基于该作品创作，您不可以分发修改作品。
- 非商业性使用：您不得将本作品用于商业目的。

您可以通过选择性的使用这六个许可证之一，来保护您的作品的相关权利。

##### 如何使用

同样，我们推荐您遵循 [Choose a License (creativecommons.org)](https://creativecommons.org/choose/) 网站的指引选择并使用适合您的 CC 许可证。

## 最后

本文采用 [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) 协议许可使用。

本文部分内容参考自 Creative Commons 组织官网，它们根据 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 协议许可再分发和修改。

本文的撰写参考了多篇文章和文档，在此一并提及并感谢这些文章和文档的帮助，排名不分先后：

- [如何选择开源许可证？ - 阮一峰的网络日志 (ruanyifeng.com)](https://www.ruanyifeng.com/blog/2011/05/how_to_choose_free_software_licenses.html)
- [一文看懂开源许可证丨开源知识科普 | PingCAP](https://pingcap.com/zh/blog/introduction-of-open-source-license)
- [各种开源协议介绍 | 菜鸟教程 (runoob.com)](https://www.runoob.com/w3cnote/open-source-license.html)
- [Frequently Asked Questions about the GNU Licenses - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/gpl-faq.html)
- [Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html)
- [A Quick Guide to GPLv3 - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/quick-guide-gplv3)
- [What is Free Software? - GNU Project - Free Software Foundation](https://www.gnu.org/philosophy/free-sw.html)
- [What is Copyleft? - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/copyleft.html)
- [The Open Source Definition | Open Source Initiative](https://opensource.org/osd)
- [Licenses & Standards | Open Source Initiative](https://opensource.org/licenses)
- [Open-source license - Wikipedia](https://en.wikipedia.org/wiki/Open-source_license)
- [BSD licenses - Wikipedia](https://en.wikipedia.org/wiki/BSD_licenses)
- [Permissive license and copyleft: the possible distinctions - iPleaders](https://blog.ipleaders.in/permissive-license-copyleft-possible-distinctions/)
- [Licenses | Choose a License](https://choosealicense.com/licenses/)
- [Appendix | Choose a License](https://choosealicense.com/appendix/)
- [Difference Between GPLV2 and GPLV3 | Difference Between](http://www.differencebetween.net/technology/software-technology/difference-between-gplv2-and-gplv3/)
- [Frequently Asked Questions - Creative Commons](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software)



[^1]: [Open-source license - Wikipedia](https://en.wikipedia.org/wiki/Open-source_license)

[^2]: [What is Free Software? - GNU Project - Free Software Foundation](https://www.gnu.org/philosophy/free-sw.html)
[^3]: 这四大基本自由是：出于任何目的随心所欲地运行程序的自由；研究程序是如何工作的，并改变它，以便它按照你的意愿进行计算的自由；重新分发副本的自由；将修改后的版本副本分发给他人的自由。
[^4]: [Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html#clearbsd)
[^5]: [Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html#MPL-2.0)
[^6]: [Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html#ccbysa)
[^7]: [Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html#Expat)
[^8]: [Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html#OriginalBSD)
[^9]:[Various Licenses and Comments about Them - GNU Project - Free Software Foundation](https://www.gnu.org/licenses/license-list.html#WTFPL)
