# Github Commit 提交规范帮助文档

> 以下内容整理自：[约定式提交](https://www.conventionalcommits.org/zh-hans/v1.0.0/)，[提交类型列表](https://github.com/pvdlg/conventional-changelog-metahub#commit-types)。

### 概述

约定式提交规范是一种基于提交信息的轻量级约定。 它提供了一组简单规则来创建清晰的提交历史； 这更有利于编写自动化工具。 通过在提交信息中描述功能、修复和破坏性变更， 使这种惯例与 [SemVer](http://semver.org/) 相互对应。

提交说明的结构如下所示：

```
<Required Type>[optional scope]: <Required Description>
[optional body]
[optional footer(s)]
```

翻译过来：

```
<（必须）类型>[（可选）范围]: <（必须）介绍>
[（可选）主要内容]
[（可选）脚注（也许不止一条）]
```

---

##### 快速跳转：

[Type（类型）](#type提交类型)、[Scope（范围）](#scope范围)、[Description（介绍）](#description介绍)、[Body（主要内容）](#body主要内容)、[Footer(s) （脚注）](#footers 脚注)

---

## Type（提交类型）

| 提交类型   | 含义                                 | 介绍                                                         | 表情 | Tag类型  |
| ---------- | ------------------------------------ | ------------------------------------------------------------ | ---- | -------- |
| `feat`     | Features（功能更新）                 | 更新了新的功能等                                             | ✨    | `minor ` |
| `fix`      | Bug Fixes（漏洞修复）                | 修复Bug、错误等                                              | 🐛    | `patch`  |
| `docs`     | Documentation（文档修改）            | 修改了介绍文档（比如 **`Readme.md`**）等                     | 📚    | `patch ` |
| `style`    | Styles（修饰代码）                   | 修改代码样式（比如 **`你闲着没事干给代码写了注释`**）等      | 💎    | -        |
| `refactor` | Code Refactoring（代码重构）         | 代码重构，但是没有添加任何新功能                             | 📦    | -        |
| `perf`     | Performance Improvements（性能优化） | 性能优化                                                     | 🚀    | `patch`  |
| `test`     | Tests（测试）                        | 新增或修改测试文件                                           | 🚨    | -        |
| `build`    | Builds（构建系统）                   | 影响构建系统或外部依赖项的更改（比如**`gulp`**、**`broccoli`**、**`npm`**） | 🛠    | `patch`  |
| `ci`       | Continuous Integrations（构建配置）  | 对 CI 配置文件和脚本的更改（比如**`Travis`**、**`Circle`**、**`BrowserStack`**、**`SauceLabs`**） | ⚙️    | -        |
| `chore`    | Chores（非重要）                     | 不影响核心代码的更新                                         | ♻️    | -        |
| `revert`   | Reverts（还原）                      | 还原到之前的Commit                                           | 🗑    | -        |



## Scope（范围）

这里制定了当前变更所作用的域。

比如我现在更新了Unity的版本，我在这里就可以写上 `Unity Version Change`。

一般使用括号紧跟在 `Type` 后面。



## Description（介绍）

这里制定了你当前变更的具体信息，一般要求**简洁、明了、概括**，如果有更多的变更信息，可以写在接下来的 ``Body`` 中。

比如我对本次工程优化了性能、更新了联机玩法，我可以写上 `Imporve Performance, Add Multiplay`。



## Body（主要内容）

这里是你的介绍里面的变更信息的补充，一般要求**详细，完整，细节**，如果你没有太多的变更信息可以不写。



## Footers（脚注）

脚注是你这次提交的批注等，常用以下两个：

**`(Co-)authored-by:sb.`**，**`BREAKING CHANGE` **

#### (Co-)authored-by:sb.

这个一般是填写本次commit由sb.编写。

加上**`Co-`**前缀就是表明**本次commit由两个或多个人共同编写**。

比如 `authored-by:BakaShanNei` 或 `Co-authored-by:Desd, BakaShanNei`。

#### BREAKING CHANGE（破坏性变更）

**注意，这个需要全大写**。

以下是破坏性变更的一些提交实例：

### 包含了描述并且脚注中有破坏性变更的提交说明

```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```



### 包含了 `!` 字符以提醒注意破坏性变更的提交说明

```
feat!: send an email to the customer when a product is shipped
```

### 包含了范围和破坏性变更 `!` 的提交說明

```
feat(api)!: send an email to the customer when a product is shipped
```

### 包含了 `!` 和 BREAKING CHANGE 脚注的提交说明

```
chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```
