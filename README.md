# SuperClaude v3 🚀

[![Website Preview](https://img.shields.io/badge/Visit-Website-blue?logo=google-chrome)](https://superclaude-org.github.io/SuperClaude_Website/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![PyPI version](https://img.shields.io/pypi/v/SuperClaude.svg)](https://pypi.org/project/SuperClaude/) [![Version](https://img.shields.io/badge/version-3.0.0-blue.svg)](https://github.com/SuperClaude-Org/SuperClaude_Framework) [![GitHub issues](https://img.shields.io/github/issues/SuperClaude-Org/SuperClaude_Framework)](https://github.com/SuperClaude-Org/SuperClaude_Framework/issues) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/SuperClaude-Org/SuperClaude_Framework/blob/master/CONTRIBUTING.md) [![Contributors](https://img.shields.io/github/contributors/SuperClaude-Org/SuperClaude_Framework)](https://github.com/SuperClaude-Org/SuperClaude_Framework/graphs/contributors) [![Website](https://img.shields.io/website?url=https://superclaude-org.github.io/SuperClaude_Website/)](https://superclaude-org.github.io/SuperClaude_Website/)

一个扩展 Claude Code 功能的框架，包含专用命令、角色设定及 MCP 服务器集成。

**📢 状态** ：初始版本，刚刚结束测试阶段！随着我们持续改进，可能会出现一些错误。

## 说明文档导航
**[详细安装指南](Docs/installation-guide-zh-CN-translation.md)|[命令指南](Docs/commands-guide-zh-CN-translation.md)|[Flags指南](Docs/flags-guide-zh-CN-translation.md)|[角色指南](Docs/personas-guide-zh-CN-translation.md)|[用户指南](Docs/superclaude-user-guide-zh-CN-translation.md)**

## SuperClaude 是什么？🤔

SuperClaude 致力于通过以下改进，让 Claude Code 更高效地辅助开发工作：

*   🛠️ **16 个专用命令** 用于常见开发任务（部分效果更佳！）
*   🎭 **智能角色** 通常能为不同领域挑选合适的专家
*   🔧 **MCP 服务器集成** 适用于文档、UI 组件和浏览器自动化
*   📋 **任务管理** 致力于追踪进度
*   ⚡ **令牌优化** 助力长对话处理

这是我们为优化开发工作流所构建的工具。虽然目前还不够完善，但正在不断改进！😊

## 当前状态 📊

✅ **进展顺利：**

*   安装套件（完全重写）
*   核心框架附带9份文档文件
*   16个用于各种开发任务的斜杠命令
*   MCP 服务器集成（Context7、Sequential、Magic、Playwright）
*   统一命令行安装工具，轻松完成配置

⚠️ **已知问题：**

*   这是初始版本，预计会存在一些缺陷
*   部分功能可能尚未完善
*   文档仍在完善中
*   钩子系统已被移除（将在 v4 版本中回归）

## 主要特性 ✨

### 命令 🛠️

我们专注于16个最常用任务的核心命令：

**开发** : `/sc:implement`, `/sc:build`, `/sc:design`
**分析** : `/sc:analyze`, `/sc:troubleshoot`, `/sc:explain`
**质量** : `/sc:improve`, `/sc:test`, `/sc:cleanup`
**其他** : `/sc:document`, `/sc:git`, `/sc:estimate`, `/sc:task`, `/sc:index`, `/sc:load`, `/sc:spawn`

### 智能角色 🎭

试图在相关时介入的 AI 专家

*   🏗️ **架构师** \- 系统设计与架构相关事务
*   🎨 **前端** \- 用户界面/用户体验与无障碍设计
*   ⚙️ **后端** \- 接口与基础设施
*   🔍 **分析器** \- 调试与问题排查工具
*   🛡️ **安全** \- 安全问题和漏洞
*   ✍️ **scribe** - 文档与写作
*   *...以及其他5位专家*

*（它们并非总能完美选择，但通常都能做对！）*

### MCP 集成工具 🔧

在需要时连接的外部工具：

*   **Context7** - 抓取官方库文档和模式
*   **顺序思考** \- 助力解决复杂多步骤的思考问题
*   **魔法** \- 生成现代化 UI 组件
*   **Playwright** - 浏览器自动化与测试工具

*（只要连接正常，这些设备用起来相当顺手！🤞）*

## ⚠️ 从 v2 升级？重要提示！

如果你是从 SuperClaude v2 迁移过来的，需要先进行清理：

1.  如果可用，请使用其卸载程序**卸载 v2 版本**
2.  **手动清理** \- 如果存在则删除：
    *   `SuperClaude/`
    *   `~/.claude/shared/`
    *   `~/.claude/commands/`
    *   `~/.claude/CLAUDE.md`
3.  **然后继续**按照下面的 v3 版本进行安装

这是因为 v3 版本采用了不同的结构，旧文件可能会引发冲突。

### 🔄 **v2 用户的重要变更**

**`/build` 命令已变更！** 在 v2 版本中，`/build` 用于功能实现。而在 v3 版本中：

*   `/sc:build` = 仅编译/打包
*   `/sc:implement` = 功能实现（新功能！）

**迁移指南** ：将 `v2 /build myFeature` 替换为 `v3 /sc:implement myFeature`

## 安装 📦

SuperClaude 的安装分为**两个步骤** ：

1.  首先安装 Python 包
2.  然后运行安装程序以设置 Claude Code 集成

### 第一步：安装包

**选项 A：通过 PyPI 安装（推荐）**

```bash
uv add SuperClaude
```

**选项 B：从源代码**

```bash
git clone https://github.com/SuperClaude-Org/SuperClaude_Framework.git
cd SuperClaude_Framework
uv sync
```

### 🔧 UV/UVX 设置指南

SuperClaude v3 还支持通过 [`uv`](https://github.com/astral-sh/uv)（更快速的现代 Python 包管理器）或跨平台使用的 `uvx` 进行安装。

### 🌀 使用 `uv` 安装

确保已安装 `uv`：

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 或按照以下说明操作：[https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

当 `uv` 可用时，你可以这样安装 SuperClaude：

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ 使用 `uvx` 安装（跨平台命令行工具）

如果使用 `uvx`，只需运行：

```bash
uvx pip install SuperClaude
```

### ✅ 安装完成

安装完成后，继续执行常规安装程序步骤：

```bash
python3 -m SuperClaude install
```

或者使用 bash 风格的命令行界面：

```bash
SuperClaude install
```

### 🧠 注意：

*   `uv` 提供了更优的缓存和性能表现。
*   兼容 Python 3.8+版本，与 SuperClaude 无缝协作。

* * *

**缺少 Python？** 请先安装 Python 3.7+版本：

```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS  
brew install python3

# Windows
# Download from https://python.org/downloads/
```

### 第二步：运行安装程序

安装完成后，运行 SuperClaude 安装程序来配置 Claude Code（可使用任意一种方法）：

### ⚠️ 重要提示

**安装 SuperClaude 后。** **您可以使用 `SuperClaude 命令` 、 `python3 -m SuperClaude commands` 或 `python3 SuperClaude 命令`**

```bash
# Quick setup (recommended for most users)
python3 SuperClaude install

# Interactive selection (choose components)
python3 SuperClaude install --interactive

# Minimal install (just core framework)
python3 SuperClaude install --minimal

# Developer setup (everything included)
python3 SuperClaude install --profile developer

# See all available options
python3 SuperClaude install --help
```

### 或 Python 模块化用法

```bash
# Quick setup (recommended for most users)
python3 -m SuperClaude install

# Interactive selection (choose components)
python3 -m SuperClaude install --interactive

# Minimal install (just core framework)
python3 -m SuperClaude install --minimal

# Developer setup (everything included)
python3 -m SuperClaude install --profile developer

# See all available options
python3 -m SuperClaude install --help
```

### 简单的 bash 命令用法

```bash
# Quick setup (recommended for most users)
SuperClaude install

# Interactive selection (choose components)
SuperClaude install --interactive

# Minimal install (just core framework)
SuperClaude install --minimal

# Developer setup (everything included)
SuperClaude install --profile developer

# See all available options
SuperClaude install --help
```

**搞定啦！🎉** 安装程序已自动处理所有事项：框架文件、MCP 服务器及 Claude Code 配置。

## 工作原理 🔄

SuperClaude 致力于通过以下方式增强 Claude 代码：

1.  **框架文件** \- 安装在 `~/.claude/` 目录下的文档，用于指导 Claude 的响应方式
2.  **斜杠命令** \- 16 个专为不同开发任务设计的命令
3.  **MCP 服务器** \- 提供额外功能的外部服务（当它们正常工作时！）
4.  **智能路由** \- 根据您的操作自动匹配最合适的工具和专家

大多数情况下它与 Claude Code 现有功能配合良好。🤝

## v4 版本即将带来什么 🔮

我们希望在下个版本中完成以下改进：

*   **钩子系统** \- 事件驱动功能（已在 v3 版本移除，正在尝试重新设计）
*   **MCP 套件** \- 更多外部工具集成
*   **更优性能** \- 致力于提升运行速度并减少程序错误
*   **更多角色** \- 或许还需要几位领域专家
*   **跨 CLI 支持** \- 可能兼容其他 AI 编程助手

*（不过时间表可不敢保证——我们还在摸索 v3 版本呢！😅）*

## 配置 ⚙️

安装完成后，您可以通过编辑以下文件来自定义 SuperClaude：

*   `~/.claude/settings.json` - 主配置文件
*   `~/.claude/*.md` - 框架行为文件

大多数用户可能无需更改任何设置——通常开箱即用就能良好运行。🎛️

## 文档 📖

想了解更多？查看我们的指南：

*   📚 [**用户指南**](https://github.com/SuperClaude-Org/SuperClaude_Framework/blob/master/Docs/superclaude-user-guide.md) \- 完整概述与入门指南
*   🛠️ [**指令指南**](https://github.com/SuperClaude-Org/SuperClaude_Framework/blob/master/Docs/commands-guide.md) \- 详解全部 16 个斜杠命令
*   🏳️ [**旗帜指南**](https://github.com/SuperClaude-Org/SuperClaude_Framework/blob/master/Docs/flags-guide.md) \- 命令标志与选项
*   🎭 [**角色指南**](https://github.com/SuperClaude-Org/SuperClaude_Framework/blob/master/Docs/personas-guide.md) \- 了解角色系统
*   📦 [**安装指南**](https://github.com/SuperClaude-Org/SuperClaude_Framework/blob/master/Docs/installation-guide.md) \- 详细安装说明

这些指南比本 README 包含更多细节，且会持续更新。

## 贡献指南 🤝

我们欢迎贡献！需要帮助的领域包括：

*   🐛 **错误报告** \- 告诉我们哪里出了问题
*   📝 **文档** \- 帮助我们更好地解释内容
*   🧪 **测试** \- 为不同配置提供更全面的测试覆盖
*   💡 **创意** \- 新功能或改进建议

代码库主要由 Python 代码和文档文件组成，结构清晰明了。

## 项目结构 📁

```
SuperClaude/
├── setup.py               # pypi setup file
├── SuperClaude/           # Framework files  
│   ├── Core/              # Behavior documentation (COMMANDS.md, FLAGS.md, etc.)
│   ├── Commands/          # 16 slash command definitions
│   └── Settings/          # Configuration files
├── setup/                 # Installation system
└── profiles/              # Installation profiles (quick, minimal, developer)
```

## 架构说明 🏗️

v3 架构聚焦于：

*   **简洁** \- 去除了无价值的复杂性
*   **可靠性** \- 更优的安装体验与更少的破坏性变更
*   **模块化** \- 只选用你需要的组件
*   **性能** \- 通过智能缓存实现更快速的操作

我们从 v2 版本中学到了很多，并尝试解决主要痛点。

## 常见问题 🙋

**问：为何移除了 hooks 系统？**
A：它变得复杂且漏洞百出。我们正在为 v4 版本进行彻底重新设计。

**问：这能与其他 AI 助手一起使用吗？**
A: 目前仅支持 Claude Code，但 v4 版本将具备更广泛的兼容性。

**问：这个足够稳定可以日常使用吗？**
A: 基础功能运行良好，但由于是新发布的版本，难免会有些小问题。用来做实验应该没问题！🧪

## SuperClaude 贡献者

[![Contributors](https://contrib.rocks/image?repo=SuperClaude-Org/SuperClaude_Framework)](https://github.com/SuperClaude-Org/SuperClaude_Framework/graphs/contributors)

## 许可证

MIT - [详见 LICENSE 文件](https://opensource.org/licenses/MIT)

## Star History

   [![Star History Chart](https://api.star-history.com/svg?repos=SuperClaude-Org/SuperClaude_Framework&type=Date)](https://www.star-history.com/#SuperClaude-Org/SuperClaude_Framework&Date)\---

*由厌倦了千篇一律回复的开发者们打造。希望您觉得有用！🙂*

* * *
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcwMTgxMDMyNywyODgzOTM2MTYsLTE0MD
ExMDQwMzJdfQ==
-->
