# 《SuperClaude 命令指南》🛠️

## 💡 别想太多 - SuperClaude 来帮你

**关于这 17 条命令的真相** ：你无需死记硬背。只需从 `/sc:analyze` 或 `/sc:implement` 开始尝试，看看会发生什么！

**通常的工作流程是这样的：**

*   在 Claude Code 中输入 `/` → 查看可用命令
*   使用基本命令如 `/sc:analyze`、`/sc:build`、`/sc:improve`
*   **SuperClaude 会针对不同情况尝试选择有用的工具和专家**
*   随着你逐渐熟悉，更多命令会变得实用

**自动激活功能相当巧妙** 🪄 - SuperClaude 会尝试检测您想要执行的操作，并自动激活相关专家（安全专家、性能优化师等），无需您手动管理。通常效果很好！😊

* * *

## 快速“试试这些”清单 🚀

**从这里开始** （无需阅读）：

```bash
/sc:help                    # 查看可用功能
/sc:analyze src/            # 尝试智能分析您的代码 
/sc:workflow feature-100-prd.md  # 根据产品需求文档生成逐步实现的工作流程
/sc:implement user-auth     # 创建功能与组件（取代v2的/build命令）
/sc:build                   # 尝试智能构建项目
/sc:improve messy-file.js   # 尝试清理代码
/sc:troubleshoot "error"    # 尝试协助解决问题
```

**说实话，这些已经足够入门了。** 下面的内容是为您好奇还有哪些其他工具可用时准备的。🛠️

* * *

《SuperClaude 斜杠命令实用指南》 涵盖全部 16 个 SuperClaude 斜杠命令的实战指南。我们将如实说明哪些功能表现优异，哪些尚待完善。

## 快速参考 📋

*（其实你完全不需要死记硬背——挑对你有用的就行）*

| 命令 | 目的 | 自动激活 | 最适合 |
| --- | --- | --- | --- |
| /sc:analyze | 智能代码分析 | 安全/性能专家 | 查找问题，理解代码库 |
| /sc:build | 智能建筑 | 前端/后端专家 | 编译、打包、部署准备 |
| /sc:implement | 功能实现 | 特定领域专家 | 创建功能、组件、API、服务 |
| /sc:improve | 自动代码清理 | 质量专家 | 重构、优化、质量修复 |
| /sc:troubleshoot | 问题排查 | 调试专家 | 调试，问题排查 |
| /sc:test | 智能测试 | 质量保证专家 | 运行测试，覆盖率分析 |
| /sc:document | 自动生成文档 | 写作专家 | README 文件、代码注释、指南 |
| /sc:git | 增强版 Git 工作流 | DevOps 专家 | 智能提交，分支管理 |
| /sc:design | 系统设计帮助 | 架构专家 | 架构规划，API 设计 |
| /sc:explain | 学习助手 | 教学专家 | 学习概念，理解代码 |
| /sc:cleanup | 债务减免 | 重构专家 | 删除无用代码，整理文件 |
| /sc:load | 理解上下文 | 分析专家 | 项目分析，代码库理解 |
| /sc:estimate | 智能估算 | 规划专家 | 时间/精力规划，复杂度分析 |
| /sc:spawn | 复杂工作流 | 编排系统 | 多步骤操作，工作流自动化 |
| /sc:task | 项目管理 | 规划系统 | 长期功能规划，任务跟踪 |
| /sc:workflow | 实施规划 | 工作流系统 | 根据 PRD 创建分步工作流程 |
| /sc:index | 命令导航 | 帮助系统 | 寻找适合您任务的命令 |

**专业提示** ：只需尝试那些听起来有用的功能。SuperClaude 通常会针对每种情况自动激活最有帮助的专家和工具！🎯

## 开发命令 🔨

### `/workflow` - 实现工作流生成器 🗺️

**功能说明** ：分析产品需求文档和功能需求，生成详细的逐步实施工作流程。

**实用功能** ：将您的产品需求文档（PRD）分解为结构化的实施计划，提供专家指导、依赖关系映射和任务编排！🎯

**何时使用** ：

*   从产品需求文档或规范开始新功能开发
*   需要一个清晰的实施路线图
*   需要专家指导实施策略
*   规划具有多重依赖关系的复杂功能

**神奇之处** ：根据您的功能需求自动激活相应的专家角色（架构师、安全专家、前端、后端）和 MCP 服务器（Context7 用于模式识别，Sequential 用于复杂分析）。

**示例** ：

```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "user authentication system" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**你将获得** ：

*   **路线图格式** ：分阶段实施计划（含时间表）
*   **任务格式** ：按史诗、用户故事和可执行任务进行组织
*   **详细格式** ：分步说明（含时间预估）
*   **风险评估** ：潜在问题及应对策略
*   **依赖关系映射** ：内部与外部依赖项
*   **专家指导** ：特定领域的最佳实践与模式

### `/implement` - 功能实现

**功能说明** ：通过智能专家激活机制实现功能、组件及系统能力的部署。

**实用功能** ：SuperClaude 会根据您正在实现的内容自动激活合适的专家（前端、后端、安全）和工具！🎯

**何时使用** ：

*   创建新功能或组件（替代 v2 版本的 `/build` 功能）
*   实现 API、服务或模块
*   使用现代框架构建 UI 组件
*   开发业务逻辑与集成

**基本语法** ：

```bash
/sc:implement user authentication system      # 完成功能实现
/sc:implement --type component LoginForm      # 创建特定组件
/sc:implement --type api user-management      # 构建API端点
/sc:implement --framework react dashboard     # 框架相关实现
```

**实用参数** ：

*   `--type component|api|service|feature|module` - 实现类型
*   `--framework react|vue|express|django|etc` - 目标框架
*   `--safe` - 保守的实现方式
*   `--iterative` - 通过验证逐步开发
*   `--with-tests` - 包含测试实现
*   `--documentation` - 在生成代码的同时生成文档

**实际示例** :

```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

\*\*自动激活模式\*\*：

*   **前端** ：UI 组件、React/Vue/Angular → 前端角色 + Magic MCP
*   **后端** ：API、服务、数据库 → 后端角色 + Context7
*   **安全** ：认证、支付、敏感数据 → 安全角色 + 验证
*   **复杂功能** ：多步骤实现 → 顺序 MCP + 架构师角色

**注意事项** :

*   指定 `--type` 参数以获得更精确的结果（组件 vs 服务 vs 功能）
*   使用特定技术栈时，请使用 `--framework` 参数
*   尝试在生产代码中使用 `--safe` 或在复杂功能中使用 `--iterative`
*   注意：这替代了 v2 版本中实际代码实现的 `/build` 命令

* * *

### `/build` - 项目构建

**功能说明** ：智能构建、编译和打包项目，具备错误处理能力。

**简单方法** ：只需输入 `/sc:build`，SuperClaude 就会尝试识别您的构建系统！🎯

**何时使用** ：

*   你需要编译/打包你的项目（试试执行 `/sc:build` 命令）
*   构建过程失败，需要帮助调试
*   设置构建优化（它会尝试检测您所需的内容）
*   部署准备

**基本语法** ：

```bash
/sc:build                          # 构建当前项目
/sc:build --type prod              # 构建生产环境
/sc:build --clean                  # 清理构建（移除旧产物）
/sc:build --optimize               # 启用优化选项
/sc:build src/                     # 构建指定目录
```

**实用参数** ：

*   `--type dev|prod|test` - 构建类型
*   `--clean` - 构建前清理
*   `--optimize` - 启用构建优化
*   `--verbose` - 显示详细的构建输出

**实际示例** :

```bash
/sc:build --type prod --optimize   # 生产环境构建，启用优化
/sc:build --clean --verbose        # 清理构建，输出详细信息
/sc:build src/components           # 仅构建 components 文件夹
```

**注意事项** :

*   与常见构建工具（如 npm、webpack 等）配合使用效果最佳
*   可能难以应对高度自定义的构建配置
*   检查您的构建工具是否在 PATH 环境变量中

* * *

### `/design` - 系统与组件设计

**功能说明** ：创建系统架构、API 设计和组件规范。

**何时使用** ：

*   规划新功能或系统
*   需要 API 或数据库设计
*   创建组件架构
*   记录系统关系

**基本语法** ：

```bash
/sc:design user-auth-system        # 设计一个用户认证系统
/sc:design --type api auth         # 仅设计API部分
/sc:design --format spec payment   # 创建正式规范
```

**实用参数** ：

*   `--type architecture|api|component|database` - 设计重点
*   `--format diagram|spec|code` - 输出格式
*   `--iterative` - 通过迭代优化设计

**实际示例** :

```bash
/sc:design --type api user-management    # 设计用户管理API
/sc:design --format spec chat-system     # 创建聊天系统规范
/sc:design --type database ecommerce     # 设计电子商务数据库架构
```

**注意事项** :

*   更偏向概念性而非代码生成
*   输出质量取决于您对需求的描述清晰程度
*   适用于规划阶段，而非实现细节

## 分析命令 🔍

### `/analyze` - 代码分析

**功能说明** ：全面分析代码质量、安全性、性能及架构设计。

**实用功能** ：SuperClaude 能自动识别您需要的分析类型，通常都会匹配最合适的专家！🔍

**何时使用** ：

*   理解陌生的代码库（只需指向任意文件夹）
*   查找安全漏洞（通常由安全专家介入）
*   性能瓶颈排查（通常需要性能专家协助）
*   代码质量评估（通常由质量专家负责）

**基本语法** ：

```bash
/sc:analyze src/                   # 分析src目录下的所有内容
/sc:analyze --focus security       # 专注于安全问题的分析
/sc:analyze --depth deep app.js    # 对特定的文件进行深度分析
```

**实用参数** ：

*   `--focus quality|security|performance|architecture` - 分析重点
*   `--depth quick|deep` - 分析深度选项
*   `--format text|json|report` - 输出格式

**实际示例** :

```bash
/sc:analyze --focus security --depth deep     # 进行深度安全分析
/sc:analyze --focus performance src/api/      # 进行API性能分析
/sc:analyze --format report .                 # 生成分析报告
```

**注意事项** :

*   在大规模代码库上可能需要较长时间
*   安全分析相当不错，性能分析则参差不齐
*   最适合常见语言（如 JS、Python 等）

* * *

### `/troubleshoot` - 问题排查

**功能说明** ：系统化调试与问题排查。

**何时使用** ：

*   出了问题，但你不确定原因
*   需要系统化的调试方法
*   错误信息令人困惑
*   性能问题排查

**基本语法** ：

```bash
/sc:troubleshoot "login not working"     # 调查登录问题
/sc:troubleshoot --logs error.log        # 分析错误日志
/sc:troubleshoot performance             # 性能故障排除
```

**实用参数** ：

*   `--logs <file>` - 包含日志文件分析
*   `--systematic` - 采用结构化调试方法
*   `--focus network|database|frontend` - 重点区域

**实际示例** :

```bash
/sc:troubleshoot "API returning 500" --logs server.log
/sc:troubleshoot --focus database "slow queries"
/sc:troubleshoot "build failing" --systematic
```

**注意事项** ：

*   配合具体的错误描述效果更佳
*   尽可能包含相关的错误信息和日志
*   可以先从显而易见的建议开始（这通常效果不错！）

* * *

### `/explain` - 教学解释

**功能说明** ：以教学方式解释代码、概念和技术。

**何时使用** ：

*   学习新技术或模式
*   理解复杂代码
*   需要为团队成员提供清晰的说明
*   记录复杂概念

**基本语法** ：

```bash
/sc:explain async/await               # 解释 async/await 概念
/sc:explain --code src/utils.js       # 解释特定代码文件
/sc:explain --beginner React hooks    # 入门友好说明
```

**实用参数** ：

*   `--beginner` - 提供更简单的解释
*   `--advanced` - 技术深度
*   `--code <file>` - 解释特定代码
*   `--examples` - 包含实用示例

**实际示例** :

```bash
/sc:explain --beginner "what is REST API"
/sc:explain --code src/auth.js --advanced
/sc:explain --examples "React context patterns"
```

**注意事项** :

*   适用于广为人知的概念，可能在处理非常小众的主题时表现欠佳
*   比起模糊的"解释这个代码库"，提出具体问题效果更好
*   包含关于您经验水平的背景信息

## 质量命令 ✨

### `/improve` - 代码优化

**功能说明** ：系统性提升代码质量、性能及可维护性。

**何时使用** ：

*   重构混乱的代码
*   性能优化
*   遵循最佳实践
*   现代化旧代码

**基本语法** ：

```bash
/sc:improve src/legacy/            # 改进旧代码
/sc:improve --type performance     # 专注于性能
/sc:improve --safe src/utils.js    # 仅进行安全、低风险的改进
```

**实用参数** ：

*   `--type quality|performance|maintainability|style` - 改进重点
*   `--safe` - 仅应用低风险变更
*   `--preview` - 显示将会进行的更改而不实际执行

**实际示例** :

```bash
/sc:improve --type performance --safe src/api/
/sc:improve --preview src/components/LegacyComponent.js
/sc:improve --type style . --safe
```

**注意事项** :

*   始终先使用 `--preview` 查看将要进行的更改
*   `--safe` 是你的好帮手——可防止高风险的重构操作
*   最适合处理较小的文件/模块而非整个代码库

* * *

### `/cleanup` - 技术债务清理

**功能** ：移除无用代码、未使用的导入语句，并整理文件结构。

**何时使用** ：

*   代码库感觉杂乱无章
*   大量未使用的导入/变量
*   文件组织混乱
*   重大重构之前

**基本语法** :

```bash
/sc:cleanup src/                   # 清理src目录
/sc:cleanup --dead-code            # 专注于删除死代码
/sc:cleanup --imports package.js   # 清理特定文件中的导入
```

**实用参数** :

*   `--dead-code` - 移除未使用的代码
*   `--imports` - 清理导入语句
*   `--files` - 重组文件结构
*   `--safe` - 仅执行保守清理

**实际示例** :

```bash
/sc:cleanup --dead-code --safe src/utils/
/sc:cleanup --imports src/components/
/sc:cleanup --files . --safe
```

**注意事项** :

*   可能较为激进 - 务必仔细审查变更
*   可能无法捕获所有无用代码（特别是动态导入）
*   最好针对较小的部分而非整个项目运行

* * *

### `/test` - 测试与质量保障

**功能** ：运行测试、生成覆盖率报告并维护测试质量。

**何时使用** ：

*   运行测试套件
*   检查测试覆盖率
*   生成测试报告
*   设置持续测试

**基本语法** ：

```bash
/sc:test                           # 运行所有测试
/sc:test --type unit               # 只运行单元测试
/sc:test --coverage                # 生成覆盖率报告
/sc:test --watch src/              # 开发模式下的监控模式
```

**实用参数** ：

*   `--type unit|integration|e2e|all` - 测试类型
*   `--coverage` - 生成覆盖率报告
*   `--watch` - 以监听模式运行测试
*   `--fix` - 尝试自动修复失败的测试

**实际示例** :

```bash
/sc:test --type unit --coverage
/sc:test --watch src/components/
/sc:test --type e2e --fix
```

**注意事项** :

*   需要你的测试框架正确配置
*   覆盖率报告依赖于您现有的测试设置
*   `--fix` 是实验性功能 - 请检查它所做的更改

## 文档命令 📝

### `/document` - 专注文档

**功能说明** ：为特定组件、函数或功能创建文档。

**何时使用** ：

*   需要 README 文件
*   编写 API 文档
*   添加代码注释
*   创建用户指南

**基本语法** ：

```bash
/sc:document src/api/auth.js       # 文档化认证模块
/sc:document --type api            # API文档化
/sc:document --style brief README  # 简化README文档
```

**实用参数** ：

*   `--type inline|external|api|guide` - 文档类型
*   `--style brief|detailed` - 详细程度
*   `--template` - 使用特定文档模板

**实际示例** :

```bash
/sc:document --type api src/controllers/
/sc:document --style detailed --type guide user-onboarding
/sc:document --type inline src/utils/helpers.js
```

**注意事项** :

*   针对特定文件/功能的效果优于整个项目
*   代码质量取决于代码结构的优劣
*   可能需要稍作编辑以匹配您项目的文档风格

## 项目管理命令 📊

### `/estimate` - 项目评估

**功能说明** ：评估开发任务的时间、工作量和复杂度。

**何时使用** ：

*   规划新功能
*   冲刺计划
*   理解项目复杂性
*   资源分配

**基本语法** ：

```bash
/sc:estimate "add user authentication"    # 评估认证功能
/sc:estimate --detailed shopping-cart     # 详细分解
/sc:estimate --complexity user-dashboard  # 复杂性分析
```

**实用参数** :

*   `--detailed` - 任务的详细分解
*   `--complexity` - 关注技术复杂性
*   `--team-size <n>` - 在估算时考虑团队规模

**实际示例** :

```bash
/sc:estimate --detailed "implement payment system"
/sc:estimate --complexity --team-size 3 "migrate to microservices"
/sc:estimate "add real-time chat" --detailed
```

**注意事项** :

*   估算仅供参考——作为起点而非绝对标准
*   配合清晰明确的功能描述效果更佳
*   考虑团队对技术栈的熟悉程度

* * *

### `/task` - 长期项目管理

**功能说明** ：管理复杂的多会话开发任务与功能。

**何时使用** ：

*   规划需要数日/数周完成的功能
*   分解大型项目
*   跨会话跟踪进度
*   协调团队工作

**基本语法** ：

```bash
/sc:task create "implement user dashboard"  # 创建新任务
/sc:task status                            	# 检查任务状态
/sc:task breakdown "payment integration"    # 分解为子任务
```

**实用参数** ：

*   `create` - 创建新的长期任务
*   `status` - 查看当前任务状态
*   `breakdown` - 将大型任务分解为多个小任务
*   `--priority high|medium|low` - 设置任务优先级

**实际示例** :

```bash
/sc:task create "migrate from REST to GraphQL" --priority high
/sc:task breakdown "e-commerce checkout flow"
/sc:task status
```

**注意事项** :

*   仍在实验阶段 - 跨会话持久性尚不稳定 😅
*   更适合规划而非实际项目管理
*   在明确需求时效果最佳

* * *

### `/spawn` - 复杂操作编排

**功能说明** ：协调复杂的多步骤操作和工作流程。

**何时使用** ：

*   涉及多个工具/系统的操作
*   协调并行工作流
*   复杂的部署流程
*   多阶段数据处理

**基本语法** ：

```bash
/sc:spawn deploy-pipeline          # 协调部署
/sc:spawn --parallel migrate-data  # 并行数据迁移
/sc:spawn setup-dev-environment    # 复杂环境设置
```

**实用参数** :

*   `--parallel` - 在可能的情况下并行运行操作
*   `--sequential` - 强制顺序执行
*   `--monitor` - 监控操作进度

**实际示例** :

```bash
/sc:spawn --parallel "test and deploy to staging"
/sc:spawn setup-ci-cd --monitor
/sc:spawn --sequential database-migration
```

**注意事项** :

*   最复杂的命令 - 预期会有些粗糙之处
*   更适合定义明确的工作流程，而非临时性操作
*   可能需要多次迭代才能正确完成

## 版本控制命令 🔄

### `/git` - 增强版 Git 操作

**功能说明** ：通过智能提交消息和工作流优化实现 Git 操作。

**何时使用** ：

*   提交更清晰的提交信息
*   分支管理
*   复杂的 Git 工作流
*   Git 故障排除

**基本语法** ：

```bash
/sc:git commit                     # 智能提交并自动生成消息
/sc:git --smart-commit add .       # 使用智能消息添加和提交
/sc:git branch feature/new-auth    # 创建并切换到新分支
```

**实用参数** :

*   `--smart-commit` - 生成智能化的提交信息
*   `--branch-strategy` - 应用分支命名规范
*   `--interactive` - 交互模式，用于复杂操作

**实际示例** :

```bash
/sc:git --smart-commit "fixed login bug"
/sc:git branch feature/user-dashboard --branch-strategy
/sc:git merge develop --interactive
```

**注意事项** :

*   智能提交信息相当不错，但仍需审查它们
*   假设您遵循常见的 git 工作流程
*   不会修正不良的 git 习惯——只是让它们更容易执行

## 实用命令 🔧

### `/index` - 命令导航

**功能** ：帮助您找到适合任务的正确命令。

**何时使用** ：

*   不确定该使用哪个命令
*   探索可用命令
*   了解命令功能

**基本语法** ：

```bash
/sc:index                          # 列出所有命令
/sc:index testing                  # 查找与测试相关的命令
/sc:index --category analysis      # 分析类别中的命令
```

**实用参数** ：

*   `--category <cat>` - 按命令类别筛选
*   `--search <term>` - 搜索命令描述

**实际示例** :

```bash
/sc:index --search "performance"
/sc:index --category quality
/sc:index git
```

**注意事项** :

*   简单却有助于探索发现
*   比试图记住全部16条命令更好

* * *

### `/load` - 项目上下文加载

**功能说明** ：加载并分析项目上下文以获得更深入的理解。

**何时使用** ：

*   开始接触陌生项目
*   需要了解项目结构
*   在进行重大更改之前
*   新成员入职指南

**基本语法** ：

```bash
/sc:load                           # 加载当前项目上下文
/sc:load src/                      # 加载特定项目上下文
/sc:load --deep                    # 深度分析项目结构
```

**实用参数** ：

*   `--deep` - 全面项目分析
*   `--focus <area>` - 聚焦特定项目区域
*   `--summary` - 生成项目摘要

**实际示例** :

```bash
/sc:load --deep --summary
/sc:load src/components/ --focus architecture
/sc:load . --focus dependencies
```

**注意事项** :

*   在大型项目上可能需要较长时间
*   在项目初期比开发过程中更有用
*   有助于快速上手，但不能替代完善的文档

## 命令提示与模式 💡

### 高效标志组合

```bash
# Safe improvement workflow
/sc:improve --preview src/component.js    # 查看更改内容
/sc:improve --safe src/component.js       # 仅应用安全更改
# Comprehensive analysis
/sc:analyze --focus security --depth deep
/sc:test --coverage
/sc:document --type api

# Smart git workflow
/sc:git add .
/sc:git --smart-commit --branch-strategy

# Project understanding workflow
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:document --type guide
```

### 常见工作流程

**新项目入门指南** ：

```bash
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:test --coverage
/sc:document README
```

\*\*Bug 调查\*\*：

```bash
/sc:troubleshoot "specific error message" --logs
/sc:analyze --focus security
/sc:test --type unit affected-component
```

\*\*代码质量提升\*\*：

```bash
/sc:analyze --focus quality
/sc:improve --preview src/
/sc:cleanup --safe
/sc:test --coverage
```

\*\*预部署检查清单\*\*：

```bash
/sc:test --type all --coverage
/sc:analyze --focus security
/sc:build --type prod --optimize
/sc:git --smart-commit
```

### 排查命令问题

**命令未按预期工作？**

*   尝试添加 `--help` 查看所有选项
*   使用可用的 `--preview` 或 `--safe` 标志
*   从较小范围开始（单个文件而非整个项目）

**分析耗时过长？**

*   使用 `--focus` 来缩小范围
*   尝试使用 `--depth quick` 而非深度分析
*   先分析较小的目录

**构建/测试命令失败？**

*   确保您的工具已添加到 PATH 环境变量中
*   检查配置文件是否位于预期位置
*   先尝试直接运行底层命令

**不确定该使用哪个命令？**

*   使用 `/index` 浏览可用命令
*   查看上方的快速参考表
*   先尝试最具体的命令，再尝试更通用的命令

* * *

## 最后说明 📝

**关于这些命令的真实情况** 💯：

*   **直接尝试** \- 你无需先学习本指南
*   **从基础开始** \- `/analyze`、`/build`、`/improve` 满足大多数需求
*   **让自动激活功能发挥作用** \- SuperClaude 通常会选择有用的专家
*   **自由实验** \- 使用 `--preview` 参数可预先查看操作结果

**尚不完善：**

*   复杂的编排（spawn、task）可能有点不稳定
*   某些分析很大程度上取决于您的项目配置
*   某些命令的错误处理可以更完善

**不断进步：**

*   我们根据用户反馈持续优化命令功能
*   较新的命令（如 analyze、improve）通常表现更佳
*   自动激活功能持续变得更智能

**不必死记硬背** 🧘‍♂️

*   SuperClaude 的设计理念是通过实际使用来探索发现
*   输入 `/` 查看可用命令
*   使用 `--help` 时，命令会提示它们能执行哪些操作
*   智能路由处理了大部分复杂性

**需要帮助？** 遇到问题请查看 GitHub issues 或创建新 issue！🚀

* * *

*快乐编码！请记住——你可以跳过本指南的大部分内容，在实践中学习。🎯*
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5ODE2NzU0NDAsLTE5NjI0NzE2ODUsMj
c1Nzc4NzMzXX0=
-->
