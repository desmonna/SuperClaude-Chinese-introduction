# 《SuperClaude角色指南》🎭

## 🎭 角色自动激活 - 无需手动选择！

**简单的事实** ：你不需要选择角色或记住他们的功能。SuperClaude 通常会自动为每种情况引入合适的专家！

**实际情况是这样的：**

*   你输入 `/analyze auth.js` → 安全专家通常会立即介入 🛡️
*   你负责 React 组件开发 → 前端专家通常会接手 🎨
*   你调试性能问题 → 性能优化器通常能帮上忙 ⚡
*   你编写文档 → 专业作者通常能帮上忙 ✍️

**就像拥有一支聪明的团队** ，他们知道何时介入提供帮助，而无需你来安排谁该做什么。

**手动控制随时可用** （例如专门要求对前端代码进行安全审查），但大多数时候你可以直接...让它自动工作。🪄

* * *

## 🚀 直接试试这些（无需了解角色设定）

```bash
# These automatically activate the right experts:
/sc:analyze payment-system/        # → 安全 + 后端专家自动激活
/sc:build react-app/               # → 前端专家接管
/sc:improve slow-queries.sql       # → 性能优化器介入
/sc:troubleshoot "auth failing"    # → 调试专家加安全专家协调
```

**看出规律了吗？** 你只需专注想做的事，SuperClaude 会帮你匹配最佳协助者。以下内容供你了解团队成员时参考。

* * *

将 SuperClaude 角色视为一支随时待命的专家团队。每个角色都具备独特的专业知识、工作重点和视角，能针对不同类型的任务为您提供专业支持。

## 什么是角色（Personas）？🤔

**角色扮演是 AI 专家** ，旨在根据不同工作类型调整 SuperClaude 的行为模式。您将获得相关领域专家的专业级协助，而非通用回复。

**它们在实际中如何运作：**

*   **自动激活** \- SuperClaude 通常会尝试选择有用的专家（大多数情况下效果相当不错！）
*   **智能检测** \- 自动识别安全工作、前端任务、性能问题等
*   **无缝切换** \- 同一对话中可根据需求随时切换不同专家参与
*   **团队协作** \- 多位专家常需协同处理复杂任务
*   **支持手动覆盖** \- 当需要不同视角时，您可以通过 `--persona-name` 参数显式选择

**这为何重要：**

*   无需知晓该请教哪位专家，即可经常获得专业级的建议
*   通常能做出更符合实际工作需求的决策
*   基于任务提供更专注且相关的响应
*   访问可在需要时激活的专用工作流程

**最棒的部分** ：你只需专注于自己的事情，通常在你需要时就会有专家伸出援手。🎯

## SuperClaude 团队 👥

### 技术专家 🔧

#### 🏗️ `architect` - 系统设计专家

**他们的职责** ：长期架构规划、系统设计、可扩展性决策

**优先级** : 长期可维护性 > 可扩展性 > 性能 > 快速修复

**自动激活时机** ：

*   关键词："架构"，"设计"，"可扩展性"，"系统结构"
*   涉及多个模块的复杂系统修改
*   规划大型功能或系统变更

**适用于** :

*   规划新系统或主要功能
*   架构审查与优化改进
*   技术债务评估
*   设计模式推荐
*   可扩展性规划

**示例工作流程** :

```bash
/sc:design microservices-migration --persona-architect
/sc:analyze --focus architecture large-system/
/sc:estimate "redesign auth system" --persona-architect
```

**他们的优先事项** :

*   可维护、易理解的代码
*   低耦合，高内聚
*   面向未来的设计决策
*   关注点清晰分离

* * *

#### 🎨 `frontend` - 用户界面/用户体验与无障碍专家

**他们的工作领域** ：用户体验、无障碍访问、前端性能优化、设计系统

**优先级** : 用户需求 > 可访问性 > 性能 > 技术优雅性

**自动激活时机** ：

*   关键词："组件"、"响应式"、"无障碍"、"用户界面"、"用户体验"
*   前端开发工作
*   用户界面相关任务

**适用于** :

*   构建 UI 组件
*   无障碍合规性（WCAG 2.1 AA 级）
*   前端性能优化
*   设计系统工作
*   用户体验改进

**它们强制执行的性能预算** ：

*   加载时间：3G 网络下<3秒，WiFi下<1秒
*   初始包大小：<500KB，总大小：<2MB
*   无障碍性：目标符合 WCAG 标准

**示例工作流程** ：

```bash
/sc:build dashboard --persona-frontend
/sc:improve --focus accessibility components/
/sc:analyze --persona-frontend --focus performance
```

**他们的优先事项** :

*   直观易用的用户界面
*   为所有用户提供无障碍访问
*   移动端/3G 网络下的实际性能表现
*   干净、可维护的 CSS/JS

* * *

#### ⚙️ `backend` - API 与基础设施专家

**工作内容** ：服务器端开发、API 接口、数据库、可靠性工程

**优先级** : 可靠性 > 安全性 > 性能 > 功能 > 便捷性

**当它们自动激活时** ：

*   关键词："API"、"数据库"、"服务"、"服务器"、"可靠性"
*   后端开发工作
*   基础设施或数据相关任务

**适用于** :

*   API 设计与实现
*   数据库架构与优化
*   安全实现
*   可靠性与错误处理
*   后端性能调优

**它们强制实施的可靠性预算** ：

*   正常运行时间：99.9%（每年停机8.7小时）
*   错误率：关键操作<0.1%
*   API 响应时间：<200毫秒
*   关键服务恢复时间：<5分钟

**示例工作流程** ：

```bash
/sc:design user-api --persona-backend
/sc:analyze --focus security api/
/sc:improve --persona-backend database-layer/
```

**他们的优先事项** ：

*   坚如磐石的可靠性与持续运行时间
*   默认安全（零信任）
*   数据完整性与一致性
*   优雅的错误处理

* * *

#### 🛡️ `security` - 威胁建模与漏洞专家

**工作内容** ：安全分析、威胁建模、漏洞评估、合规审查

**优先级** : 安全性 > 合规性 > 可靠性 > 性能 > 便捷性

**自动激活时机** ：

*   关键词："安全"、"漏洞"、"认证"、"合规"
*   安全扫描或评估工作
*   身份验证/授权任务

**适用于** :

*   安全审计与漏洞扫描
*   威胁建模与风险评估
*   安全编码实践
*   合规要求（OWASP 等）
*   认证与授权系统

**威胁评估等级** ：

*   重要：需立即采取行动
*   高优先级：24小时内修复
*   中：7天内修复
*   低：30天内修复

**示例工作流** :

```bash
/sc:scan --persona-security --focus security
/sc:analyze auth-system/ --persona-security
/sc:improve --focus security --persona-security
```

**他们的优先事项** :

*   默认安全机制，故障自动防护
*   零信任架构原则
*   纵深防御策略
*   清晰的安全文档

* * *

#### ⚡ `performance` - 性能优化与瓶颈分析专家

**他们的工作内容** ：性能优化、瓶颈识别、指标分析

**优先级** : 先测量 > 优化关键路径 > 用户体验 > 避免过早优化

**当它们自动激活时** ：

*   关键词："性能"，"优化"，"速度"，"瓶颈"
*   性能分析或优化工作
*   当提及速度/效率时

**适用于** :

*   性能瓶颈识别
*   基于指标验证的代码优化
*   数据库查询优化
*   前端性能优化
*   负载测试与容量规划

**他们跟踪的性能预算** ：

*   API 响应时间：<500毫秒
*   数据库查询：<100毫秒
*   初始包大小：<500KB
*   内存占用：移动端<100MB，桌面端<500MB

**示例工作流程** ：

```bash
/sc:analyze --focus performance --persona-performance
/sc:improve --type performance slow-endpoints/
/sc:test --benchmark --persona-performance
```

**他们的优先事项** :

*   测量驱动优化
*   真实用户体验提升
*   关键路径性能
*   系统性优化方法论

### 流程与质量专家 ✨

#### 🔍 `analyzer` - 根因调查专家

**工作内容** ：系统性调试、根源分析、基于证据的调查

**优先级** : 证据 > 系统方法 > 全面性 > 速度

**自动激活时机** ：

*   关键词："分析"、"调查"、"调试"、"根本原因"
*   调试或故障排除会话
*   复杂问题排查

**适用于** :

*   调试复杂问题
*   根本原因分析
*   系统调研
*   基于实证的问题解决
*   理解陌生的代码库

**调查方法** ：

1.  结论先行前需收集证据
2.  数据中的模式识别
3.  假设检验与验证
4.  通过测试确认根本原因

**示例工作流程** ：

```bash
/sc:troubleshoot "auth randomly fails" --persona-analyzer
/sc:analyze --persona-analyzer mysterious-bug/
/sc:explain --detailed "why is this slow" --persona-analyzer
```

**他们的优先事项** ：

*   基于证据的结论
*   系统化调查方法
*   解决方案之前先进行全面分析
*   可复现的研究结果

* * *

#### 🧪 `qa` - 质量保证与测试专家

**他们的职责** ：测试策略制定、质量门禁控制、边缘案例检测、风险评估

**优先级** : 预防 > 检测 > 纠正 > 全面覆盖

**自动激活时机** ：

*   关键词："测试"、"质量"、"验证"、"覆盖率"
*   测试或质量保障工作
*   提到的质量门禁或边缘情况

**适用于** :

*   测试策略与规划
*   质量保证流程
*   边缘情况识别
*   基于风险的测试
*   测试自动化

**质量风险评估** ：

*   用户旅程的关键路径分析
*   故障影响评估
*   缺陷概率评估
*   恢复难度评估

**示例工作流程** ：

```bash
/sc:test --persona-qa comprehensive-suite
/sc:analyze --focus quality --persona-qa
/sc:review --persona-qa critical-features/
```

**他们的优先事项** :

*   预防缺陷胜于发现缺陷
*   全面的测试覆盖
*   基于风险的测试优先级
*   品质融入流程

* * *

#### 🔄 `refactorer` - 代码质量与清理专家

**他们的工作内容** ：代码质量提升、技术债务管理、整洁代码实践

**优先级** ：简洁性 > 可维护性 > 可读性 > 性能 > 巧妙性

**自动激活时机** ：

*   关键词："重构"、"清理"、"质量"、"技术债务"
*   代码改进或清理工作
*   可维护性问题

**适用于** :

*   代码重构与清理
*   技术债务削减
*   代码质量改进
*   设计模式应用
*   遗留代码现代化改造

**他们追踪的代码质量指标** ：

*   圈复杂度
*   代码可读性评分
*   技术债务比率
*   测试覆盖率

**示例工作流程** ：

```bash
/sc:improve --type quality --persona-refactorer
/sc:cleanup legacy-module/ --persona-refactorer
/sc:analyze --focus maintainability --persona-refactorer
```

**他们的优先事项** ：

*   简洁易读的解决方案
*   一致的样式与规范
*   可维护的代码结构
*   技术债务管理

* * *

#### 🚀 `devops` - 基础设施与部署专家

**他们的工作内容** ：基础设施自动化、部署、监控、可靠性工程

**优先级** : 自动化 > 可观测性 > 可靠性 > 可扩展性 > 手动流程

**自动激活时机** ：

*   关键词："部署"、"基础设施"、"持续集成/持续交付"、"监控"
*   部署或基础设施工作
*   DevOps 或自动化任务

**适用于** :

*   部署自动化与持续集成/持续交付
*   基础设施即代码
*   监控与告警设置
*   性能监控
*   容器与云基础设施

**基础设施自动化优先级** ：

*   零停机部署
*   自动回滚功能
*   基础设施即代码
*   全面监控

**示例工作流程** :

```bash
/sc:deploy production --persona-devops
/sc:analyze infrastructure/ --persona-devops
/sc:improve deployment-pipeline --persona-devops
```

**他们的优先事项** :

*   自动化优于手动流程
*   全面可观测性
*   可靠、可重复的部署
*   基础设施即代码实践

### 知识与交流 📚

#### 👨‍🏫 `mentor` - 教育指导专家

**他们的工作内容** ：教学、知识传递、教育讲解、促进学习

**优先级** ：理解 > 知识传递 > 教学 > 任务完成

**自动激活时机** ：

*   关键词："解释"、"学习"、"理解"、"教授"
*   教育或知识传递任务
*   分步指导请求

**适用于** :

*   学习新技术
*   理解复杂概念
*   代码解释与逐步讲解
*   最佳实践指南
*   团队知识共享

**学习优化方法** ：

*   技能水平评估
*   渐进式复杂度构建
*   学习风格适配
*   知识留存强化

**示例工作流程** ：

```bash
/sc:explain React hooks --persona-mentor
/sc:document --type guide --persona-mentor
/sc:analyze complex-algorithm.js --persona-mentor
```

**他们优先考虑的事项** ：

*   清晰易懂的解释
*   完整的概念理解
*   引人入胜的学习体验
*   实用技能培养

* * *

#### ✍️ `scribe` - 专业文档专家

**他们的工作** ：专业写作、文档编写、本地化、文化交流

**优先级** : 清晰性 > 受众需求 > 文化敏感性 > 完整性 > 简洁性

**自动激活时机** ：

*   关键词："文档", "编写", "指南", "README"
*   文档编写或写作任务
*   专业沟通需求

**适用于** :

*   技术文档
*   用户指南与教程
*   README 文件和维基
*   API 文档
*   专业沟通

**语言支持** : 英语（默认）、西班牙语、法语、德语、日语、中文、葡萄牙语、意大利语、俄语、韩语

**内容类型** ：技术文档、用户指南、API 文档、提交信息、PR 描述

**示例工作流程** ：

```bash
/sc:document api/ --persona-scribe
/sc:git commit --persona-scribe
/sc:explain --persona-scribe=es complex-feature
```

**他们的优先事项** ：

*   清晰专业的沟通
*   适合目标受众的语言
*   文化敏感性与适应性
*   高标准写作

## 当每个人格闪耀时 ⭐

### 开发阶段映射

**规划与设计阶段** ：

*   🏗️ `architect` - 系统设计与架构规划
*   🎨 `前端` \- 用户界面/用户体验设计
*   ✍️ `scribe` - 需求文档与规范说明

**实施阶段** ：

*   🎨 `前端` \- 用户界面组件开发
*   ⚙️ `backend` - API 与服务实现
*   🛡️ `security` - 安全实现与加固

\*\*测试与质量阶段\*\*

*   🧪 `qa` - 测试策略与质量保障
*   ⚡ `performance` - 性能测试与优化
*   🔍 `analyzer` - 故障排查与根因分析

**维护与改进阶段**

*   🔄 `refactorer` - 代码清理与重构
*   ⚡ `performance` - 性能优化
*   👨‍🏫 `mentor` - 知识传承与文档编写

**部署与运维阶段** ：

*   🚀 `devops` - 部署自动化与基础设施
*   🛡️ `security` - 安全监控与合规
*   ✍️ `scribe` - 操作文档与运行手册

### 问题类型映射

**"我的代码运行很慢"** → ⚡ `性能优化` **"出问题了但找不到原因"** → 🔍 `问题分析` **"需要设计新系统"** → 🏗️ `架构设计` **"界面太难看了"** → 🎨 `前端美化` **"这样安全吗？"** → 🛡️ `安全检查` **"代码太乱了"** → 🔄 `代码重构` **"需要更好的测试"** → 🧪 `质量保障` **"部署总是失败"** → 🚀 `运维支持` **"这个我看不懂"** → 👨‍🏫 `导师指导` **"需要文档"** → ✍️ `文档编写`

## 角色组合 🤝

角色之间通常会自动协作。以下是常见的协作模式：

### 设计与实现

```bash
/sc:design user-dashboard
# 自动激活：🏗️建筑师（系统设计）+ 🎨前端（UI设计）
```

### 安全审查

```bash
/sc:analyze --focus security api/
# 自动激活：🛡️ 安全（主要）+ ⚙️ 后端（API 专业知识）
```

### 性能优化

```bash
/sc:improve --focus performance slow-app/
# 自动激活：⚡性能（主要）+ 🎨前端（如果为UI）或⚙️后端（如果为API）
```

### 质量提升

```bash
/sc:improve --focus quality legacy-code/
# 自动激活：🔄 重构器（主要）+ 🧪 质量保证（测试）+ 🏗️ 架构师（设计）
```

### 文档与学习

```bash
/sc:document complex-feature --type guide
# 自动激活：✍️ 笔记员（写作）+ 👨‍🏫 导师（教育方法）
```

## 实用示例 💡

### 前/后：通用型与角色定制型

**之前** （通用）：

```bash
/sc:analyze auth.js
# → 基本分析，通用建议
```

**之后** （安全角色）：

```bash
/sc:analyze auth.js --persona-security
# → 以安全为重点分析
# → 威害建模视角
# → OWASP合规性检查
# → 漏洞模式检测
```

### 自动激活实战

**前端工作检测** ：

```bash
/sc:build react-components/
# 自动激活：🎨前端
# → 以UI为中心的构建优化
# → 无障碍检查
# → 性能预算
# → 捆绑包大小分析
```

**复杂调试** ：

```bash
/sc:troubleshoot "payment processing randomly fails"
# 自动激活：🔍 分析器
# → 系统调查方法
# → 证据收集方法
# → 模式分析
# → 根本原因识别
```

### 手动覆盖示例

**强制安全视角** ：

```bash
/sc:analyze react-app/ --persona-security
# 尽管它是前端代码，但从安全角度进行分析
# → 跨站脚本漏洞检测
# → 身份验证流程分析
# → 数据泄露风险
```

**获取关于小改动的架构建议** ：

```bash
/sc:improve small-utility.js --persona-architect
# 将架构思维应用于小型代码
# → 设计模式的可能
# → 未来的可扩展性
# → 耦合分析
```

## 高级用法 🚀

### 手动角色控制

**何时需要覆盖自动激活** ：

*   你希望从不同角度看待同一个问题
*   自动激活功能为您的特定需求选择了错误的角色
*   你正在学习，并想了解不同专家如何解决问题

**如何覆盖** ：

```bash
# 明确的角色选择
/sc:analyze frontend-code/ --persona-security  # 前端代码安全分析
/sc:improve backend-api/ --persona-performance # 后端性能优化

# 多角色标志（最后一个标志生效）
/sc:analyze --persona-frontend --persona-security # 使用安全专家的角色
```

### 角色特定标志与设置

**安全角色 + 验证** ：

```bash
/sc:analyze --persona-security --focus security --validate
# → 最高安全重点与验证
```

**性能角色 + 基准测试** ：

```bash
/sc:test --persona-performance --benchmark --focus performance
# → 以性能为导向的基于指标的测试
```

**导师角色 + 详细说明**

```bash
/sc:explain complex-concept --persona-mentor --verbose
# → 带有详细说明的教育解释
```

### 跨领域专业知识

**当你需要多角度思考时** ：

```bash
# 使用不同角色进行顺序分析
/sc:analyze --persona-security api/auth.js
/sc:analyze --persona-performance api/auth.js  
/sc:analyze --persona-refactorer api/auth.js

# 或者让SuperClaude自动协调
/sc:analyze --focus quality api/auth.js
# 自动协同：安全性 + 性能 + 重构器洞察
```

## 常见角色工作流程 💼

### 🏗️ 架构工作流

```bash
# 系统设计
/sc:design microservices-architecture --persona-architect
/sc:estimate "migrate monolith to microservices" --persona-architect

# 架构评估
/sc:analyze --focus architecture --persona-architect large-system/
/sc:review --persona-architect critical-components/
```

### 🎨 前端工作流

```bash
# 组件开发
/sc:build dashboard-components/ --persona-frontend
/sc:improve --focus accessibility --persona-frontend ui/

# 性能优化
/sc:analyze --focus performance --persona-frontend bundle/
/sc:test --persona-frontend --focus performance
```

### ⚙️ 后端工作流

```bash
# API开发
/sc:design rest-api --persona-backend
/sc:build api-endpoints/ --persona-backend

# 可靠性提升
/sc:improve --focus reliability --persona-backend services/
/sc:analyze --persona-backend --focus security api/
```

### 🛡️ 安全防护工作流

```bash
# 安全评估
/sc:scan --persona-security --focus security entire-app/
/sc:analyze --persona-security auth-flow/

# 漏洞修复
/sc:improve --focus security --persona-security vulnerable-code/
/sc:review --persona-security --focus security critical-paths/
```

### 🔍 分析器工作流

```bash
# Bug深入分析
/sc:troubleshoot "intermittent failures" --persona-analyzer
/sc:analyze --persona-analyzer --focus debugging problem-area/

# 系统理解
/sc:explain --persona-analyzer complex-system/
/sc:load --persona-analyzer unfamiliar-codebase/
```

## 快速参考 📋

### 角色速查表

| 角色 | 最适合 | 自动激活于 | 手动标记 |
| --- | --- | --- | --- |
| 🏗️ 架构师 | 系统设计与架构 | "架构", "设计", "可扩展性" | \--persona-architect |
| 🎨 前端 | 用户界面/用户体验，无障碍设计 | "组件", "响应式", "用户界面" | \--persona-frontend |
| ⚙️ 后端 | API、数据库、可靠性 | "API"、"数据库"、"服务" | \--persona-backend |
| 🛡️ 安全 | 安全性与合规性 | "安全", "漏洞", "认证" | \--persona-security |
| ⚡ 性能 | 优化，提速 | "性能", "优化", "缓慢" | \--persona-performance |
| 🔍 分析器 | 调试、排查 | "分析", "调试", "调查" | \--persona-analyzer |
| 🧪 质量保证 | 测试，质量 | "测试", "质量", "验证" | \--persona-qa |
| 🔄 重构者 | 代码清理、重构 | "重构", "清理", "质量" | \--persona-refactorer |
| 🚀 运维开发 | 部署与基础设施 | "部署", "基础设施", "持续集成/持续交付" | \--persona-devops |
| 导师 | 学习、讲解 | "解释"、"学习"、"理解" | \--persona-mentor |
| ✍️ 抄写员 | 文档编写 | "文档", "编写", "指南" | \--persona-scribe |

### 最实用的组合

**注重安全的开发** ：

```bash
--persona-security --focus security --validate
```

**性能优化** ：

```bash
--persona-performance --focus performance --benchmark
```

\*\*学习与理解\*\*：

```bash
--persona-mentor --verbose --explain
```

**质量提升** ：

```bash
--persona-refactorer --focus quality --safe-mode
```

**专业文档** ：

```bash
--persona-scribe --type guide --detailed
```

### 自动激活触发器

**强力触发词** （通常效果显著）：

*   "安全审计" → 🛡️ 安全
*   "UI 组件" → 🎨 前端
*   "API 设计" → ⚙️ 后端
*   "系统架构" → 🏗️ 架构
*   "调试问题" → 🔍 分析器

**适度触发** （通常有效）：

*   "提升性能" → ⚡ 性能优化
*   "编写测试" → 🧪 质量保证
*   "清理代码" → 🔄 重构
*   "部署问题" → 🚀 开发运维

**上下文相关触发器** （因情况而异）：

*   "记录此内容" → ✍️ 记录员 或 👨‍🏫 导师（视受众而定）
*   "分析此内容" → 🔍 分析员、🏗️ 架构师或领域专家（视内容而定）

## 排查角色问题 🚨

### 常见问题

**"错误角色已激活"**

*   使用明确的人物角色标识：`--persona-security`
*   检查您的关键词是否触发了自动激活
*   尝试在请求中使用更具体的语言

**"Persona 似乎不起作用"**

*   验证角色名称拼写：`--persona-frontend` 而非 `--persona-fronted`
*   某些角色更适合搭配特定指令使用
*   尝试结合相关标志： `--focus security --persona-security`

**"想要多角度观点"**

*   手动以不同身份运行相同命令
*   使用更广泛的专注标志：`--focus quality`（激活多个人格）
*   让 SuperClaude 自动协调处理复杂请求

**"角色设定过于专注"**

*   尝试一个更通用的角色设定
*   使用导师角色进行更广泛的解释
*   结合 `--verbose` 参数可获取更多上下文信息

### 何时需要覆盖自动激活

**覆盖时机** ：

*   自动激活选择了错误的专家
*   你想从不同的角度学习
*   突破传统领域界限
*   需要针对边缘案例的专业知识

**如何有效进行覆盖** ：

```bash  
# 强制特定视角
/sc:analyze frontend-code/ --persona-security  # 前端安全视角

# 结合多个视角
/sc:analyze api/ --persona-security
/sc:analyze api/ --persona-performance  # 以不同视角分别运行

# Use general analysis
/sc:analyze --no-persona  # 禁用角色自动激活
```

## 有效使用角色设定的技巧 💡

### 入门指南（真诚版）

1.  **一开始完全忽略角色设定** \- 自动激活功能会处理一切
2.  **常规使用基本命令** \- `/analyze`、`/build`、`/improve` 无需角色知识即可完美运行
3.  **注意观察变化** \- 你会自然地看到不同类型的专业技能显现出来
4.  **信任自动化** \- SuperClaude 选择的专家通常比人工挑选的更优秀

### 进阶指南（可选）

1.  **尝试手动覆盖** \- 在前端代码中使用 `--persona-security` 参数来获取不同视角
2.  **了解团队成员** \- 当你感到好奇时，可以阅读个人角色介绍
3.  **观察角色组合** \- 了解多位专家如何协作解决复杂问题
4.  **用于学习** \- 向不同角色提出相同问题，观察不同的解决思路

### 最佳实践（保持简洁）

*   **先让自动激活功能发挥作用** \- 仅在需要不同视角时进行覆盖
*   **不必想太多** \- 合适的专家总会在需要时出现
*   **用于实验探索** \- 针对同一问题尝试不同角色设定以促进学习
*   **信任智能** \- 自动激活功能通过学习模式持续优化

* * *

## 最后说明 📝

**关于用户画像的真相** 💯：

*   **自动激活通常比自己挑选专家效果更好**
*   **你可以完全忽略这份指南** ，仍然经常获得有用的专家帮助
*   **角色存在的意义是帮助你** ——而非制造需要管理的复杂性
*   **学习自然发生**于实际使用中，而非通过研究角色描述 😊

**不必被团队压垮** 🧘‍♂️：

*   你无需了解每个角色的具体职责
*   SuperClaude 通常在专家选择方面处理得相当合理
*   上述详细描述仅供满足好奇心，并非必需
*   让自动激活功能运行并不会让你错过任何东西

**何时可能需要手动选择角色** ：

*   **好奇心** \- "安全专家会如何看待这段前端代码？"
*   **学习** \- "不同领域的专家会如何解决这个问题？"
*   **实验性功能** \- "让我从性能角度审视这个问题"
*   **覆盖** \- "我想就这个小工具函数获得架构方面的建议"

**保持简洁** 🎯:

*   使用常规命令如 `/analyze some-code/`
*   让合适的专家自动现身
*   手动角色控制功能随需启用，而非必需之选
*   专注工作本身，而非分心于管理协助者

* * *

*在拥有 11 位专家的表面复杂背后，SuperClaude 力求操作简便。只需开始编码，专业助手通常会在需要时及时出现！🚀*
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY0NjQyNjQ1NywxNTE3NDIwMl19
-->
