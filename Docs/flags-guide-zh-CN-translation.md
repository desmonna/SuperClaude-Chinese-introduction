# 《SuperClaude 旗帜使用指南》🏁

## 🤖 大多数 Flag 会自动激活 - 无需为此担心！

实话实说：你无需死记这些标记。SuperClaude 通常会根据你的操作自动添加有用的标记！

**实际情况是这样的：**

*   你输入 `/analyze auth.js`
*   SuperClaude 检测到这是与安全相关的代码
*   通常添加 `--persona-security` 、 `--focus security` 、 `--validate`
*   您通常无需管理任何标志即可获得专业的安全分析

**何时可能需要手动使用标志？**

*   You want to **override** what SuperClaude picked (rare)
    您想覆盖 SuperClaude 的选择（罕见情况）
*   You're **curious** about specific aspects (`--focus performance`)
    您对某些具体方面感到好奇（ `--focus performance` ）
*   You want to **experiment** with different approaches
    您想尝试不同的方法

**Bottom line**: Just use basic commands and let the auto-activation work. These flags are here when you want them, not because you need them. 🎯
核心建议：只需使用基本命令，让自动激活功能发挥作用。这些标志参数是备用的，并非必需。🎯

* * *

## 🚀 Just Try These (No Flag Knowledge Required)
🚀 直接试试这些（无需了解 Flag 知识）

```bash
# These work great with zero flag knowledge:
/sc:analyze src/                   # 自动选择正确的分析标志
/sc:build                          # 根据您的项目自动优化
/sc:improve messy-code.js          # 自动激活质量和安全标志
/sc:troubleshoot "weird error"     # 自动激活调试和分析标志
```

**See? No flags needed.** Everything below is for when you get curious about what's happening behind the scenes.
看吧？根本不需要任何标志。下面的内容只是在你对幕后运作感到好奇时才会用到。

* * *

A practical guide to SuperClaude's flag system. Flags are like command-line options that change how SuperClaude behaves - think of them as superpowers for your commands.
《SuperClaude 标志系统实用指南》。标志如同命令行选项，能改变 SuperClaude 的行为模式——将它们视为赋予命令的超能力。

## What Are Flags? 🤔
什么是 Flags？🤔

**Flags are modifiers** that change how SuperClaude processes your requests. They come after commands and start with `--`.
标志是修改 SuperClaude 处理请求方式的修饰符。它们位于命令之后，以 `--` 开头。

**Basic syntax** (but you usually don't need to know this):
基本语法（但通常无需了解这些）：

```bash
/sc:command --flag-name
/sc:command --flag-name value  
/sc:analyze src/ --focus security --depth deep
```

**How flags actually work in practice**:
实践中 flags 的实际工作原理：

1.  **Auto-activation** - SuperClaude adds them based on context (this is the main way! 🎯)
    自动激活 - SuperClaude 会根据上下文自动添加（这是主要方式！🎯）
2.  **Manual override** - You can add them explicitly if you want different behavior
    手动覆盖 - 如需不同行为可显式添加

**Why flags exist** (mostly automatic benefits):
为什么存在 flags（主要是自动化的好处）：

*   Get better, more focused results
    获得更优质、更聚焦的结果
*   Auto-enable the right thinking depth
    自动启用正确的思考深度
*   Connect to special capabilities when useful
    在有用时连接特殊功能
*   Optimize for speed or detail based on your task
    根据任务需求优化速度或细节
*   Direct attention to what you're actually working on
    专注于你实际正在处理的工作

**The key point**: SuperClaude handles flag selection intelligently so you don't have to think about it! 🧠
关键点：SuperClaude 会智能处理 flag 选择，您无需为此费心！🧠

## Flag Categories 📂
标志类别 📂

### Planning & Analysis Flags 🧠
规划与分析标志 🧠

These control how deeply SuperClaude thinks about your request.
这些参数控制 SuperClaude 对您请求的思考深度。

#### `--plan`

**What it does**: Shows execution plan before doing anything
功能说明：在执行任何操作前显示执行计划
**When to use**: When you want to see what SuperClaude will do first
何时使用：当你想先看看 SuperClaude 会做什么时
**Example**: `/build --plan` - See build steps before running
示例： `/build --plan` - 运行前查看构建步骤

#### `--think`

**What it does**: Multi-file analysis (~4K tokens)
功能说明：多文件分析（约 4000 个词元）
**When to use**: Complex problems involving several files
何时使用：涉及多个文件的复杂问题
**Auto-activates**: Import chains >5 files, cross-module calls >10 references
自动激活条件：导入链超过 5 个文件，跨模块调用超过 10 次引用
**Example**: `/analyze complex-system/ --think`
示例： `/analyze complex-system/ --think`

#### `--think-hard`

**What it does**: Deep architectural analysis (~10K tokens)
功能：深度架构分析（约 10K tokens）
**When to use**: System-wide problems, architectural decisions
何时使用：系统级问题、架构决策
**Auto-activates**: System refactoring, bottlenecks >3 modules
自动激活：系统重构，瓶颈模块超过 3 个
**Example**: `/improve legacy-system/ --think-hard`
示例： `/improve legacy-system/ --think-hard`

#### `--ultrathink`

**What it does**: Maximum depth analysis (~32K tokens)
功能说明：最大深度分析（约 32K tokens）
**When to use**: Critical system redesign, complex debugging
何时使用：关键系统重构、复杂调试
**Auto-activates**: Legacy modernization, critical vulnerabilities
自动激活：遗留系统现代化改造，关键漏洞
**Example**: `/troubleshoot "entire auth system broken" --ultrathink`
示例： `/troubleshoot "entire auth system broken" --ultrathink`

**💡 Tip**: Start with `--think`, only go deeper if needed. More thinking = slower but more thorough.
💡 提示：从 `--think` 开始，仅在必要时深入。思考越多=速度越慢但更彻底。

* * *

### Efficiency & Control Flags ⚡
效率与控制标志 ⚡

Control output style, safety, and performance.
控制输出样式、安全性和性能。

#### `--uc` / `--ultracompressed`

**What it does**: 60-80% token reduction using symbols
功能说明：通过符号实现 60-80%的令牌精简
**When to use**: Large operations, when context is getting full
何时使用：大型操作，当上下文即将填满时
**Auto-activates**: Context usage >75%, large-scale operations
自动激活条件：上下文使用率>75%，大规模操作
**Example**: `/analyze huge-codebase/ --uc`
示例： `/analyze huge-codebase/ --uc`

#### `--safe-mode`

**What it does**: Maximum validation, conservative execution
功能说明：最大程度验证，保守执行
**When to use**: Production environments, risky operations
何时使用：生产环境、高风险操作
**Auto-activates**: Resource usage >85%, production environment
自动激活条件：资源使用率>85%，生产环境
**Example**: `/improve production-code/ --safe-mode`
示例： `/improve production-code/ --safe-mode`

#### `--validate`

**What it does**: Pre-operation validation and risk assessment
功能说明：操作前验证与风险评估
**When to use**: Want to check before making changes
何时使用：希望在做出更改前进行检查
**Auto-activates**: Risk score >0.7
自动激活：风险评分 >0.7
**Example**: `/cleanup legacy/ --validate`
示例： `/cleanup legacy/ --validate`

#### `--verbose`

**What it does**: Maximum detail and explanation
功能说明：提供最详尽的细节与解释
**When to use**: Learning, debugging, need full context
何时使用：学习、调试、需要完整上下文
**Example**: `/build --verbose` - See every build step
示例： `/build --verbose` - 查看每个构建步骤

#### `--answer-only`

**What it does**: Direct response without task creation
功能：直接响应而不创建任务
**When to use**: Quick questions, don't want workflow automation
何时使用：快速提问，不需要工作流自动化
**Example**: `/explain React hooks --answer-only`
示例： `/explain React hooks --answer-only`

**💡 Tip**: `--uc` is great for big operations. `--safe-mode` for anything important. `--verbose` when you're learning.
💡 提示： `--uc` 适用于大型操作。 `--safe-mode` 用于重要事项。 `--verbose` 适合学习时使用。

* * *

### MCP Server Flags 🔧
MCP 服务器标志 🔧

Enable specialized capabilities through MCP servers.
通过 MCP 服务器启用专业功能。

#### `--c7` / `--context7`

**What it does**: Enables Context7 for official library documentation
功能说明：为官方库文档启用 Context7
**When to use**: Working with frameworks, need official docs
何时使用：使用框架时，需要官方文档
**Auto-activates**: External library imports, framework questions
自动激活：外部库导入、框架问题
**Example**: `/build react-app/ --c7` - Get React best practices
示例： `/build react-app/ --c7` - 获取 React 最佳实践

#### `--seq` / `--sequential`

**What it does**: Enables Sequential for complex multi-step analysis
功能说明：启用 Sequential 功能以支持复杂的多步骤分析
**When to use**: Complex debugging, system design
何时使用：复杂调试、系统设计
**Auto-activates**: Complex debugging, `--think` flags
自动激活：复杂调试， `--think` 标志
**Example**: `/troubleshoot "auth flow broken" --seq`
示例： `/troubleshoot "auth flow broken" --seq`

#### `--magic`

**What it does**: Enables Magic for UI component generation
功能说明：为 UI 组件生成启用 Magic 功能
**When to use**: Creating UI components, design systems
何时使用：创建 UI 组件、设计系统
**Auto-activates**: UI component requests, frontend persona
自动激活：UI 组件请求，前端角色
**Example**: `/build dashboard --magic` - Get modern UI components
示例： `/build dashboard --magic` - 获取现代化 UI 组件

#### `--play` / `--playwright`

**What it does**: Enables Playwright for browser automation and testing
功能说明：启用 Playwright 进行浏览器自动化与测试
**When to use**: E2E testing, performance monitoring
何时使用：端到端测试、性能监控
**Auto-activates**: Test workflows, QA persona
自动激活：测试工作流，QA 角色
**Example**: `/test e2e --play`
示例： `/test e2e --play`

#### `--all-mcp`

**What it does**: Enables all MCP servers simultaneously
功能说明：同时启用所有 MCP 服务器
**When to use**: Complex multi-domain problems
何时使用：复杂的多领域问题
**Auto-activates**: Problem complexity >0.8, multi-domain indicators
自动激活条件：问题复杂度>0.8，多领域指标
**Example**: `/analyze entire-app/ --all-mcp`
示例： `/analyze entire-app/ --all-mcp`

#### `--no-mcp`

**What it does**: Disables all MCP servers, native tools only
功能说明：禁用所有 MCP 服务器，仅保留原生工具
**When to use**: Faster execution, don't need specialized features
何时使用：需要更快执行速度，且不需要特殊功能时
**Example**: `/analyze simple-script.js --no-mcp`
示例： `/analyze simple-script.js --no-mcp`

**💡 Tip**: MCP servers add capabilities but use more tokens. `--c7` for docs, `--seq` for thinking, `--magic` for UI.
💡 提示：MCP 服务器增加了功能但会消耗更多令牌。 `--c7` 用于文档， `--seq` 用于思考， `--magic` 用于用户界面。

* * *

### Advanced Orchestration Flags 🎭
高级编排标志 🎭

For complex operations and workflows.
适用于复杂操作和工作流程。

#### `--delegate [files|folders|auto]`

**What it does**: Enables sub-agent delegation for parallel processing
功能说明：启用子代理委托以实现并行处理
**When to use**: Large codebases, complex analysis
何时使用：大型代码库、复杂分析
**Auto-activates**: >7 directories or >50 files
自动激活条件：超过 7 个目录或 50 个文件
**Options**:
选项：

*   `files` - Delegate individual file analysis
    `files` - 委托单个文件分析
*   `folders` - Delegate directory-level analysis
    `folders` - 委托目录级分析
*   `auto` - Smart delegation strategy
    `auto` - 智能委托策略

**Example**: `/analyze monorepo/ --delegate auto`
示例： `/analyze monorepo/ --delegate auto`

#### `--wave-mode [auto|force|off]`

**What it does**: Multi-stage execution with compound intelligence
功能说明：采用复合智能的多阶段执行
**When to use**: Complex improvements, systematic analysis
何时使用：复杂改进、系统分析
**Auto-activates**: Complexity >0.8 AND files >20 AND operation types >2
自动激活条件：复杂度 >0.8 且 文件数 >20 且 操作类型 >2
**Example**: `/improve legacy-system/ --wave-mode force`
示例： `/improve legacy-system/ --wave-mode force`

#### `--loop`

**What it does**: Iterative improvement mode
功能说明：迭代改进模式
**When to use**: Quality improvement, refinement operations
何时使用：质量改进、优化操作
**Auto-activates**: Polish, refine, enhance keywords
自动激活：优化、完善、增强关键词
**Example**: `/improve messy-code.js --loop`
示例： `/improve messy-code.js --loop`

#### `--concurrency [n]`

**What it does**: Control max concurrent sub-agents (1-15)
功能：控制最大并发子代理数量（1-15）
**When to use**: Controlling resource usage
何时使用：控制资源使用
**Example**: `/analyze --delegate auto --concurrency 3`
示例： `/analyze --delegate auto --concurrency 3`

**💡 Tip**: These are powerful but complex. Start with `--delegate auto` for big projects, `--loop` for improvements.
💡 提示：这些功能强大但复杂。大型项目建议从 `--delegate auto` 开始，改进项目则使用 `--loop` 。

* * *

### Focus & Scope Flags 🎯
专注与范围标志 🎯

Direct SuperClaude's attention to specific areas.
引导 SuperClaude 关注特定领域。

#### `--scope [level]`

**Options**: file, module, project, system
选项：文件、模块、项目、系统
**What it does**: Sets analysis scope
功能说明：设置分析范围
**Example**: `/analyze --scope module auth/`
示例： `/analyze --scope module auth/`

#### `--focus [domain]`

**Options**: performance, security, quality, architecture, accessibility, testing
选项：性能、安全性、质量、架构、无障碍性、测试
**What it does**: Focuses analysis on specific domain
功能说明：专注于特定领域的分析
**Example**: `/analyze --focus security --scope project`
示例： `/analyze --focus security --scope project`

#### Persona Flags
角色标记

**Available personas**: architect, frontend, backend, analyzer, security, mentor, refactorer, performance, qa, devops, scribe
可用角色：架构师、前端开发、后端开发、分析师、安全专家、导师、重构专家、性能优化、质量保证、运维工程师、文档编写员
**What they do**: Activates specialist behavior patterns
它们的作用：激活特定的行为模式
**Example**: `/analyze --persona-security` - Security-focused analysis
示例： `/analyze --persona-security` - 安全导向分析

**💡 Tip**: `--focus` is great for targeted analysis. Personas auto-activate but manual control helps.
💡 提示： `--focus` 非常适合针对性分析。角色会自动激活，但手动控制更有帮助。

* * *

## Common Flag Patterns 🔄
常见标志模式 🔄

### Quick Analysis
快速分析

```bash
/sc:analyze src/ --focus quality          # 快速质量检测
/sc:analyze --uc --focus security         # 快速安全扫描
```

### Deep Investigation
深入调查

```bash
/sc:troubleshoot "bug" --think --seq           # 系统调试
/sc:analyze --think-hard --focus architecture  # 架构分析
```

### Large Project Work
大型项目工作

```bash
/sc:analyze monorepo/ --delegate auto --uc        # 高效的大数据分析
/sc:improve legacy/ --wave-mode auto --safe-mode  # 安全系统改进
```

### Learning & Documentation
学习与文档

```bash
/sc:explain React hooks --c7 --verbose    # 带有文档的详细说明
/sc:document api/ --persona-scribe        # 专业文档
```

### Performance-Focused
性能优先

```bash
/sc:analyze --focus performance --play     # 测试中的性能分析
/sc:build --uc --no-mcp                    # 快速构建，不包含额外功能
```

### Security-Focused
安全导向型

```bash
/sc:analyze --focus security --think --validate  # 彻底的安全分析
/sc:scan --persona-security --safe-mode          # 保守安全扫描
```

## Practical Examples 💡
实用示例 💡

### Before/After: Basic Analysis
前后对比：基础分析

**Before** (basic):
之前（基础版）：

```bash
/sc:analyze auth.js
# → Simple file analysis
```

**After** (with flags):
之后（带标志）：

```bash
/sc:analyze auth.js --focus security --think --c7
# → Security-focused analysis with deep thinking and official docs
# → Much more thorough, finds security patterns, checks against best practices
```

### Before/After: Large Project
之前/之后：大型项目

**Before** (slow):
之前（较慢）：

```bash
/sc:analyze huge-monorepo/
# → Tries to analyze everything at once, may timeout or use too many tokens
```

**After** (efficient):
之后（高效版）：

```bash
/sc:analyze huge-monorepo/ --delegate auto --uc --focus architecture
# → Delegates work to sub-agents, compresses output, focuses on architecture
# → Faster, more focused, better results
```

### Before/After: Improvement Work
改进前后的工作对比

**Before** (risky):
之前（存在风险）：

```bash
/sc:improve legacy-system/
# → May make too many changes, could break things
```

**After** (safe):
之后（安全）：

```bash
/sc:improve legacy-system/ --safe-mode --loop --validate --preview
# → Safe changes only, iterative approach, validates first, shows preview
# → Much safer, progressive improvement
```

## Auto-Activation Examples 🤖
自动激活示例 🤖

SuperClaude usually adds flags based on context. Here's when it tries:
SuperClaude 通常会根据上下文添加标记。以下是它尝试添加的情况：

### Complexity-Based
基于复杂性

```bash
/sc:analyze huge-codebase/
# Auto-adds: --delegate auto --uc
# Why: >50 files detected, context management needed

/sc:troubleshoot "complex system issue"  
# Auto-adds: --think --seq
# Why: Multi-component problem detected
```

### Domain-Based
基于域名的

```bash
/sc:build react-app/
# Auto-adds: --c7 --persona-frontend
# Why: Frontend framework detected

/sc:analyze --focus security
# Auto-adds: --persona-security --validate
# Why: Security focus triggers security specialist
```

### Performance-Based
基于性能的

```bash
# When context usage >75%
/sc:analyze large-project/
# Auto-adds: --uc
# Why: Token optimization needed

# When risk score >0.7
/sc:improve production-code/
# Auto-adds: --safe-mode --validate
# Why: High-risk operation detected
```

## Advanced Usage 🚀
高级用法 🚀

### Complex Flag Combinations
复杂标志组合

**Comprehensive Code Review**:
全面代码审查：

```bash
/sc:review codebase/ --persona-qa --think-hard --focus quality --validate --c7
# → QA specialist + deep thinking + quality focus + validation + docs
```

**Legacy System Modernization**:
遗留系统现代化

```bash
/sc:improve legacy/ --wave-mode force --persona-architect --safe-mode --loop --c7
# → Wave orchestration + architect perspective + safety + iteration + docs
```

**Security Audit**:
安全审计

```bash
/sc:scan --persona-security --ultrathink --focus security --validate --seq
# → Security specialist + maximum thinking + security focus + validation + systematic analysis
```

### Performance Optimization
性能优化

**For Speed**:
为了速度：

```bash
/sc:analyze --no-mcp --uc --scope file
# → Disable extra features, compress output, limit scope
```

**For Thoroughness**:
为了全面性：

```bash
/sc:analyze --all-mcp --think-hard --delegate auto
# → All capabilities, deep thinking, parallel processing
```

### Custom Workflows
自定义工作流

**Bug Investigation Workflow**:
Bug 调查工作流程：

```bash
/sc:troubleshoot "specific error" --seq --think --validate
/sc:analyze affected-files/ --focus quality --persona-analyzer  
/sc:test --play --coverage
```

**Feature Development Workflow**:
功能开发工作流程：

```bash
/sc:design new-feature --persona-architect --c7
/sc:build --magic --persona-frontend --validate
/sc:test --play --coverage
/sc:document --persona-scribe --c7
```

## Quick Reference 📋
快速参考 📋

### Most Useful Flags
最实用的标志

| Flag标志 | Purpose目的 | When to Use何时使用 |
| --- | --- | --- |
| \--think | Deeper analysis深入分析 | Complex problems复杂问题 |
| \--uc | Compress output压缩输出 | Large operations大规模操作 |
| \--safe-mode | Conservative execution保守执行 | Important code重要代码 |
| \--c7 | Official docs官方文档 | Framework work框架工作 |
| \--seq | Systematic analysis系统化分析 | Debugging调试 |
| \--focus security | Security focus安全重点 | Security concerns安全问题 |
| \--delegate auto | Parallel processing并行处理 | Large codebases大型代码库 |
| \--validate | Check before action行动前检查 | Risky operations高风险操作 |

### Flag Combinations That Work Well
搭配效果良好的标志组合

```bash
# Safe improvement
--safe-mode --validate --preview

# Deep analysis  
--think --seq --c7

# Large project
--delegate auto --uc --focus

# Learning
--verbose --c7 --persona-mentor

# Security work
--persona-security --focus security --validate

# Performance work
--persona-performance --focus performance --play
```

### Auto-Activation Triggers
自动激活触发器

*   **\--think**: Complex imports, cross-module calls
    \--思考：复杂的导入、跨模块调用
*   **\--uc**: Context >75%, large operations
    \--uc：上下文>75%，大型操作
*   **\--safe-mode**: Resource usage >85%, production
    \--safe-mode: 资源使用率 >85%，生产环境
*   **\--delegate**: >7 directories or >50 files
    \--delegate: >7 个目录或>50 个文件
*   **\--c7**: Framework imports, documentation requests
    \--c7: 框架导入，文档请求
*   **\--seq**: Debugging keywords, --think flags
    \--seq: 调试关键词，--think 标志
*   **Personas**: Domain-specific keywords and patterns
    角色：领域特定关键词与模式

## Troubleshooting Flag Issues 🚨
排查标志问题 🚨

### Common Problems
常见问题

**"Flags don't seem to work"
"标记似乎不起作用"**

*   Check spelling (common typos: `--ultracompresed`, `--persona-fronted`)
    检查拼写（常见拼写错误： `--ultracompresed` 、 `--persona-fronted` ）
*   Some flags need values: `--scope project`, `--focus security`
    某些标志需要赋值： `--scope project` ， `--focus security`
*   Flag conflicts: `--no-mcp` overrides `--c7`, `--seq`, etc.
    标记冲突： `--no-mcp` 会覆盖 `--c7` 、 `--seq` 等。

**"Operation too slow"
"操作过慢"**

*   Try `--uc` for compression
    尝试使用 `--uc` 进行压缩
*   Use `--no-mcp` to disable extra features
    使用 `--no-mcp` 可禁用额外功能
*   Limit scope: `--scope file` instead of `--scope project`
    限制范围：使用 `--scope file` 而非 `--scope project`

**"Too much output"
"输出过多"**

*   Add `--uc` for compression
    添加 `--uc` 以进行压缩
*   Remove `--verbose` if present
    如果存在则移除 `--verbose`
*   Use `--answer-only` for simple questions
    使用 `--answer-only` 进行简单提问

**"Not thorough enough"
"不够彻底"**

*   Add `--think` or `--think-hard`
    添加 `--think` 或 `--think-hard`
*   Enable relevant MCP servers: `--seq`, `--c7`
    启用相关 MCP 服务器： `--seq` 、 `--c7`
*   Use appropriate persona: `--persona-analyzer`
    使用适当的角色身份： `--persona-analyzer`

**"Changes too risky"
"变更风险过高"**

*   Always use `--safe-mode` for important code
    重要代码始终使用 `--safe-mode`
*   Add `--validate` to check first
    添加 `--validate` 以进行首次检查
*   Use `--preview` to see changes before applying
    使用 `--preview` 可在应用前查看更改

### Flag Conflicts
标记冲突

**These override others**:
这些设置会覆盖其他配置：

*   `--no-mcp` overrides all MCP flags (`--c7`, `--seq`, etc.)
    `--no-mcp` 覆盖所有 MCP 标志（ `--c7` 、 `--seq` 等）
*   `--safe-mode` overrides optimization flags
    `--safe-mode` 覆盖优化标志
*   Last persona flag wins: `--persona-frontend --persona-backend` → backend
    最后生效的角色标志： `--persona-frontend --persona-backend` → 后端

**Precedence order**:
优先级顺序：

1.  Safety flags (`--safe-mode`) beat optimization
    安全标志（ `--safe-mode` ）优先于优化
2.  Explicit flags beat auto-activation
    显式标志优于自动激活
3.  Thinking depth: `--ultrathink` > `--think-hard` > `--think`
    思考深度： `--ultrathink` > `--think-hard` > `--think`
4.  Scope: system > project > module > file
    范围：系统 > 项目 > 模块 > 文件

## Tips for Effective Flag Usage 💡
高效使用标志的小贴士 💡

### Starting Out (The Honest Truth)
入门指南（实话实说）

1.  **Just ignore flags at first** - Auto-activation handles most cases pretty well
    刚开始可以忽略 flags——自动激活功能在大多数情况下都能很好地处理
2.  **Watch what gets auto-activated** - You'll learn by seeing what SuperClaude picks
    观察自动激活的内容 - 通过查看 SuperClaude 的选择来学习
3.  **Use `--help` when curious** - Many commands show what flags are available
    好奇时使用 `--help` - 许多命令会显示可用的标志
4.  **Trust the automation** - SuperClaude usually picks reasonable defaults
    相信自动化 - SuperClaude 通常会选择合理的默认值

### Getting Advanced (If You Want To)
进阶指南（可选）

1.  **Experiment with overrides** - Try `--persona-security` on non-security code for different perspectives
    尝试使用覆盖 - 在非安全代码上试用 `--persona-security` 以获得不同视角
2.  **Learn the useful combos** - `--safe-mode --validate` for important stuff
    学习实用组合键 - `--safe-mode --validate` 用于重要事项
3.  **Understand the performance trade-offs** - Fast (`--uc --no-mcp`) vs thorough (`--think-hard --all-mcp`)
    理解性能权衡 - 快速模式（ `--uc --no-mcp` ）与全面模式（ `--think-hard --all-mcp` ）
4.  **Use flags for learning** - `--verbose` when you want to understand what's happening
    使用标志进行学习 - 当你想了解发生了什么时使用 `--verbose`

### Performance Tips (For Power Users)
性能优化技巧（高级用户指南）

*   **For speed**: `--uc --no-mcp --scope file`
    为了速度： `--uc --no-mcp --scope file`
*   **For thoroughness**: `--think-hard --all-mcp --delegate auto`
    为了全面性： `--think-hard --all-mcp --delegate auto`
*   **For safety**: `--safe-mode --validate --preview`
    为了安全起见： `--safe-mode --validate --preview`
*   **For learning**: `--verbose --c7 --persona-mentor`
    学习用途： `--verbose --c7 --persona-mentor`

* * *

## Final Notes 📝
最后说明 📝

**The real truth about flags** 💯:
关于 flags 的真相 💯：

*   **Auto-activation usually works pretty well** compared to manual flag selection
    相比手动选择标志，自动激活通常效果相当不错
*   **You can ignore most of this guide** and just use basic commands
    你可以忽略本指南的大部分内容，仅使用基本命令即可
*   **Flags are here when you want them** - not because you need them
    当你需要时，旗帜就在这里——而非出于必需
*   **Learning happens naturally** through use, not through studying guides 😊
    通过实践自然学习，而非研读指南 😊

**Don't feel overwhelmed** 🧘‍♂️:
别感到不知所措 🧘‍♂️：

*   SuperClaude tries to work well without flag knowledge
    SuperClaude 力求在无需了解标志的情况下也能良好运作
*   The detailed info above is for curiosity, not necessity
    上述详细信息仅供满足好奇心，并非必需
*   Auto-activation keeps getting smarter based on usage patterns
    自动激活功能会根据使用模式不断变得更加智能
*   You're not missing out by not memorizing flags
    不记住这些标志也不会错过什么

**When you actually need flags**:
当你真正需要 flags 时：

*   Overriding auto-activation (rare)
    覆盖自动激活（罕见情况）
*   Experimenting with different approaches (fun)
    尝试不同的方法（有趣）
*   Optimizing for specific performance needs (advanced)
    针对特定性能需求进行优化（高级）
*   Learning about what happened (educational)
    了解发生了什么（教育意义）

**Start simple, stay simple** 🎯:
从简单开始，保持简单 🎯

*   Use basic commands: `/analyze`, `/build`, `/improve`
    使用基本命令： `/analyze` 、 `/build` 、 `/improve`
*   Let auto-activation handle the complexity
    让自动激活功能处理复杂性问题
*   Add manual flags only when you want to experiment
    仅在需要进行实验时手动添加标志
*   Trust that SuperClaude knows what it's doing
    相信 SuperClaude 知道自己在做什么

* * *

*Remember: Behind all this apparent complexity, SuperClaude is actually simple to use. Just start typing commands! 🚀
记住：尽管看起来复杂，SuperClaude 实际上简单易用。只需开始输入命令即可！🚀*
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNDQzODMyMTEsLTEwNTczMzEwODldfQ
==
-->
