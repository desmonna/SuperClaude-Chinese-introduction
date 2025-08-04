# 《SuperClaude 安装指南》 📦

## 🎯 比看起来更简单！

**实话实说** ：本指南看起来很长是因为我们想涵盖所有细节，但安装过程其实非常简单。大多数人只需一条命令，两分钟就能搞定！

### 第一步：安装包

**选项 A：通过 PyPI 安装（推荐）**

```bash
uv add SuperClaude
```

**选项 B：从源文件**

```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```

### 🔧 UV / UVX 设置指南

SuperClaude v3 也支持通过 [`uv`](https://github.com/astral-sh/uv)（更快速的现代 Python 包管理器）或跨平台使用的 `uvx` 进行安装。

### 🌀 使用 `uv` 安装

确保已安装 `uv`：

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 或按照以下说明操作：[https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

当 `uv` 可用后，你可以这样安装 SuperClaude：

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ 使用 `uvx` 安装（跨平台 CLI）

如果你正在使用 `uvx`，只需运行：

```bash
uvx pip install SuperClaude
```

### ✅ 完成安装

安装完成后，继续按照常规安装程序步骤操作：

```bash
python3 -m SuperClaude install
```

或者使用 bash 风格的 CLI：

```bash
SuperClaude install
```

### 🧠 注意：

*   `uv` 提供了更好的缓存和性能表现。
*   兼容 Python 3.8+ 版本，并能与 SuperClaude 流畅协同工作。

* * *

### ⚠️ 重要提示

**安装 SuperClaude 后。** **您可以使用 `SuperClaude commands` 、 `python3 -m SuperClaude commands` 或者 `python3 SuperClaude commands`**

**刚刚发生了什么？** SuperClaude 已为您自动配置好所需的一切。通常无需复杂的设置、依赖项查找或安装烦恼！🎉

* * *

SuperClaude v3 完整安装指南。但请记住——大多数人其实只需要看完上文的快速入门就够了！😊

## 开始之前 🔍

### 所需配置 💻

SuperClaude 支持 **Windows**、**macOS** 和 **Linux** 系统，以下是所需条件：

**必需**

*   **Python 3.8 或更高版本** \- 该框架使用 Python 编写
*   **Claude CLI** - SuperClaude 增强了 Claude Code 的功能，因此您需要先安装它

**可选（推荐）**

*   **Node.js 16+** - 仅当需要 MCP 服务器集成时才需要
*   **Git** - 助力开发工作流程

### 快速检查 🔍

在安装之前，请确保您已具备以下基本条件：

```bash
# Check Python version (should be 3.8+)
python3 --version

# Check if Claude CLI is installed
claude --version

# Check Node.js (optional, for MCP servers)
node --version
```

如果其中任何一项失败，请参阅下方的[先决条件设置](#prerequisites-setup-%F0%9F%9B%A0%EF%B8%8F)部分。

## 快速开始 🚀

**🏆 "直接让它工作"方法（推荐 90%用户使用）** **选项 A：通过 PyPI 安装（推荐）**

```bash
pip install SuperClaude

# Install with recommended settings  
SuperClaude install --quick

# That's it! 🎉
```

**选项 B：从源文件**

```bash
# Clone the repo
git clone <repository-url>
cd SuperClaude
pip install .

# Install with recommended settings  
SuperClaude install --quick

# That's it! 🎉
```

**⚠️ 重要提示****安装 SuperClaude 后****您可以使用 `SuperClaude commands` 、 `python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

**你刚刚获取的内容：**

*   ✅ 所有16个能自动激活专家的智能指令
*   ✅ 11位专业角色，懂得何时提供帮助
*   ✅ 智能路由，自动为您解析复杂度
*   ✅ 只需约 2 分钟时间和 50MB 左右的磁盘空间

**真的，你已经完成了。** 打开 Claude Code，输入 `/help`，然后见证 SuperClaude 施展它的魔法。

**担心它会做什么？** 先看看：

```bash
SuperClaude install --quick --dry-run
```

## 安装选项 🎯

我们提供三种安装配置方案供您选择：

### 🎯 极简安装

```bash
SuperClaude install --minimal
```

*   **内容** ：仅包含核心框架文件
*   **时间** : ~1 分钟
*   **空间** : ~20MB
*   **适用场景** ：测试、基础功能增强、最小化配置
*   **包含** ：指导 Claude 的核心行为文档

### 🚀 快速安装（推荐）

```bash
SuperClaude install --quick
```

*   **功能** ：核心框架 + 16 条斜杠命令
*   **时间** : ~2 分钟
*   **空间** : ~50MB
*   **适用场景** ：大多数用户，常规开发
*   **包含内容** ：极简版所有功能 + 专用命令如 `/analyze`、`/build`、`/improve`

### 🔧 开发者安装

```bash
SuperClaude install --profile developer
```

*   **功能** ：包含 MCP 服务器集成在内的所有内容
*   **时间** : ~5 分钟
*   **空间占用** : ~100MB
*   **适用场景** ：高级用户、贡献者、复杂工作流
*   **包含** ：完整功能+Context7、顺序模式、Magic 模式、Playwright 服务器

### 🎛️ 交互式装置

```bash
SuperClaude install
```

*   让你自由选择和组合组件
*   显示每个组件的详细功能说明
*   若想掌控安装内容，此方案正合心意

## 分步安装指南 📋

### 前提条件设置 🛠️

**缺少 Python？**

```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS  
brew install python3

# Windows
# Download from https://python.org/downloads/
#or open command prompt or powershell
winget install python
```

**找不到 Claude CLI？**

*   访问 [https://claude.ai/code](https://claude.ai/code) 获取安装说明
*   SuperClaude 增强了 Claude 代码功能，因此您需要先安装它

**缺少 Node.js？（可选）**

```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows  
# Download from https://nodejs.org/
#or open command prompt or powershell
winget install nodejs
```

### 获取 SuperClaude 📥

**选项 1：通过 PyPI 安装（推荐）**

```bash
pip install SuperClaude
```

**选项2：下载最新版本**

```bash
# Download and extract the latest release
# (Replace URL with actual release URL)
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**选项 3：从 Git 克隆**

```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### 运行安装程序 🎬

安装程序非常智能，将引导您完成整个安装过程：

```bash
# See all available options
SuperClaude install --help

# Quick installation (recommended)
SuperClaude install --quick

# Want to see what would happen first?
SuperClaude install --quick --dry-run

# Install everything
SuperClaude install --profile developer

# Quiet installation (minimal output)
SuperClaude install --quick --quiet

# Force installation (skip confirmations)
python3 SuperClaude.py install --quick --force
```

### 安装期间 📱

安装后会发生以下情况：

1.  **系统检查** \- 验证您是否具备所需的依赖项
2.  **目录设置** \- 创建 `~/.claude/` 目录结构
3.  **核心文件** \- 复制框架文档文件
4.  **命令** \- 安装斜杠命令定义（如已选择）
5.  **MCP 服务器** \- 下载并配置 MCP 服务器（如已选择）
6.  **配置** \- 根据您的偏好设置 `settings.json` 文件
7.  **验证** \- 测试所有功能是否正常运作

安装程序会显示进度，并在出现问题时通知您。

## 安装完成后 ✅

### 快速测试 🧪

让我们确认一切是否正常运行：

```bash
# Check if files were installed
ls ~/.claude/

# Should show: CLAUDE.md, COMMANDS.md, settings.json, etc.
```

**使用 Claude 代码测试**

1.  开启 Claude Code
2.  尝试输入 `/help` - 你应该能看到 SuperClaude 命令
3.  尝试 `/analyze --help` - 应显示命令选项

### 安装了哪些内容 📂

SuperClaude 默认安装到 `~/.claude/` 目录下，包含以下内容：

```
~/.claude/
├── CLAUDE.md              # 主框架入口点
├── COMMANDS.md             # 可用的斜杠命令
├── FLAGS.md                # 命令标志和选项
├── PERSONAS.md             # 智能角色系统
├── PRINCIPLES.md           # 开发原则
├── RULES.md                # 操作规则
├── MCP.md                  # MCP服务器集成
├── MODES.md                # 操作模式
├── ORCHESTRATOR.md         # 智能路由
├── settings.json           # 配置文件
└── commands/               # 单个命令定义
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... (13 more)
```

**各文件功能说明：**

*   **CLAUDE.md** - 向 Claude Code 介绍 SuperClaude 并加载其他文件
*   **settings.json** - 配置（MCP 服务器、钩子等）
*   **commands/** - 每个斜杠命令的详细定义

### 入门指南 🎯

尝试以下命令开始使用：

```bash
# In Claude Code, try these:
/sc:help                    # 查看可用命令
/sc:analyze README.md       # 分析一个文档
/sc:build --help           # 查看构建选项
/sc:improve --help         # 查看改进选项
```

**不必担心内容过多难以消化** \- SuperClaude 会循序渐进地增强 Claude 代码功能，您可以根据需要自由选择使用程度。

## 管理您的安装 🛠️

### 更新 📅

保持 SuperClaude 最新状态：

```bash
# Check for updates
SuperClaude update

# Force update (overwrite local changes)
SuperClaude update --force

# Update specific components only
SuperClaude update --components core,commands

# See what would be updated
SuperClaude update --dry-run
```

**何时更新：**

*   当新版 SuperClaude 发布时
*   如果您遇到问题（更新通常包含修复）
*   当新的 MCP 服务器可用时

### 备份 💾

进行重大更改前创建备份

```bash
# Create a backup
SuperClaude backup --create

# List existing backups  
SuperClaude backup --list

# Restore from backup
SuperClaude backup --restore

# Create backup with custom name
SuperClaude backup --create --name "before-update"
```

**何时备份：**

*   在更新 SuperClaude 之前
*   在尝试调整设置之前
*   卸载前
*   如果你进行了大量自定义设置

### 卸载 🗑️

如需移除 SuperClaude：

```bash
# Remove SuperClaude (keeps backups)
SuperClaude uninstall

# Complete removal (removes everything)
SuperClaude uninstall --complete

# See what would be removed
SuperClaude uninstall --dry-run
```

**移除的内容：**

*   `~/.claude/` 目录下的所有文件
*   MCP 服务器配置
*   来自 Claude Code 的 SuperClaude 设置

**保留的内容**

*   您的备份（除非使用 `--complete` 参数）
*   Claude Code本身(SuperClaude不会涉及)
*   您的项目及其他文件

## 故障排除 🔧

### 常见问题 🚨

**"未找到 Python"**

```bash
# Try python instead of python3
python --version

# Or check if it's installed but not in PATH
which python3
```

**"未找到 Claude 命令行工具"**

*   请确保已安装 Claude Code
*   尝试运行 `claude --version` 来验证版本
*   访问 [https://claude.ai/code](https://claude.ai/code) 获取安装帮助

**"权限被拒绝"**

```bash
# Try with explicit Python path
/usr/bin/python3 SuperClaude.py install --quick

# Or check if you need different permissions
ls -la ~/.claude/
```

**"MCP 服务器无法安装"**

*   检查是否已安装 Node.js：`node --version`
*   检查 npm 是否可用：`npm --version`
*   先尝试不安装 MCP：`--minimal` 或 `--quick`

**"安装过程中途失败"**

```bash
# Try with verbose output to see what's happening
SuperClaude install --quick --verbose

# Or try a dry run first
SuperClaude install --quick --dry-run
```

### 平台特定问题 🖥️

**Windows：**

*   如果遇到“command not found”错误，请使用 `python` 而非 `python3`
*   如果遇到权限错误，请以管理员身份运行命令提示符
*   确保 Python 已添加到您的 PATH 环境变量中

**macOS：**

*   您可能需要在“安全与隐私”设置中批准 SuperClaude 的权限
*   如果没有安装 Python 3.8+，请使用 `brew install python3`
*   尝试明确使用 `python3` 而非 `python`

**Linux：**

*   确保已安装 `python3-pip`
*   某些软件包安装可能需要使用 `sudo` 权限
*   确保 `~/.local/bin` 已包含在您的 PATH 环境变量中

### 遇到问题了吗？🤔

**查看我们的故障排除资源：**

*   GitHub Issues: [https://github.com/SuperClaude-Org/SuperClaude_Framework/issues](https://github.com/SuperClaude-Org/SuperClaude_Framework/issues)
*   查找与您问题相似的现有议题
*   如果找不到解决方案，请创建新 issue

**提交问题时，请包含以下内容：**

*   您的操作系统及版本
*   Python 版本（`python3 --version`）
*   Claude CLI 版本（`claude --version`）
*   您运行的确切命令
*   完整的错误信息
*   你期望发生的情况

**获取帮助：**

*   GitHub Discussions 用于一般性问题讨论
*   查看 README.md 获取最新更新
*   查看 ROADMAP.md 文件以确认您的问题是否已被记录

## 高级选项 ⚙️

### 自定义安装目录

```bash
# Install to custom location
SuperClaude install --quick --install-dir /custom/path

# Use environment variable
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### 组件选择

```bash
# See available components
SuperClaude install --list-components

# Install specific components only
SuperClaude install --components core,commands

# Skip certain components
SuperClaude install --quick --skip mcp
```

### 开发环境设置

如果您计划贡献或修改 SuperClaude：

```bash
# Developer installation with all components
SuperClaude install --profile developer

# Install in development mode (symlinks instead of copies)
SuperClaude install --profile developer --dev-mode

# Install with git hooks for development
SuperClaude install --profile developer --dev-hooks
```

## 接下来是什么？🚀

**现在 SuperClaude 已经安装好了（很简单吧？）：**

1.  **立即开始使用** \- 尝试输入 `/analyze some-file.js` 或 `/build` 命令，看看会发生什么 ✨
2.  **学习无需压力** \- SuperClaude 通常能领会您的需求
3.  **自由实验** \- 诸如 `/improve` 和 `/troubleshoot` 这类命令具有很高的容错性
4.  **若感好奇，请阅读指南** \- 当你想了解发生了什么时，请查阅 `Docs/` 目录
5.  **提供反馈** \- 告诉我们哪些功能好用，哪些需要改进

**真正的秘诀** ：SuperClaude 的设计理念是在无需学习大量新知识的情况下增强您现有的工作流程。只需像使用常规 Claude Code 那样使用它，但您会发现它变得智能多了！🎯

**还是觉得不确定？** 只需从 `/help` 和 `/analyze README.md` 开始——你会发现它其实并不复杂。

* * *

## 最后说明 📝

*   **安装仅需 1-5 分钟** 具体时长取决于您的选择
*   **所需磁盘空间：20-100MB**（占用很小！）
*   **与现有工具协同工作** \- 不会干扰您的现有配置
*   **轻松卸载** ，随时改变主意
*   **社区支持** \- 我们认真阅读并回复每个问题
*   ### ⚠️ 重要提示
    

**安装完 SuperClaude 后。** **你可以使用 `SuperClaude commands` 、 `python3 -m SuperClaude commands` 或者 `python3 SuperClaude commands`**

感谢试用 SuperClaude！希望它能为您的工作流程带来更多顺畅体验。🙂

* * *

*最后更新：2024年7月 - 如果本指南有任何错误或不清楚的地方，请告诉我们！*
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTQ5OTczNDc2LC0xNDczMDM5NTE4LC0zOD
U1NDMwMl19
-->
