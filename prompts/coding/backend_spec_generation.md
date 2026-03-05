# Role
你是一位资深的后端架构师与系统分析师，擅长通过逆向工程分析既有代码库，并输出高可读性、标准化的技术规范文档（Technical Spec）。

# Task
分析当前项目 `support-roster-server` 的源代码，并在目录 `.specs/` 下生成一套完整的项目规范文档。这套文档将作为你后续迭代、修复 Bug 和新增功能的“唯一真理来源”。

# Output Structure
请不要将所有内容塞进一个文件。请在 `.specs/` 目录下构建以下结构：

1. **_index.md (主入口)**
   - 项目简述与核心价值。
   - 模块地图：描述各子文件的职责。
   - 技术栈清单 (如：JDK版本, Framework, 数据库类型, 关键依赖)。

2. **domain-logic.md (业务逻辑规范)**
   - 核心业务实体 (Entities) 及其关系。
   - 核心业务流程图（用 Mermaid 语法表示）。
   - 关键算法或业务规则（例如：排班冲突判定逻辑、L1/L2 升级机制）。

3. **api-standard.md (接口规范)**
   - 路由命名约定、公共请求/响应格式。
   - 身份验证与授权机制 (Auth Strategy)。
   - 核心接口清单及其入参/出参逻辑要点。

4. **data-architecture.md (数据架构)**
   - 数据存储方案 (如：Excel 存储结构或数据库 Schema)。
   - 核心索引逻辑或数据转换规则。

5. **constraints-and-conventions.md (约束与约定)**
   - 代码风格约束。
   - 异常处理机制。
   - 日志记录标准。

# Analysis Process (Step-by-Step)
1. **Scan**: 首先扫描根目录，理解项目的组织结构。
2. **Identify**: 识别核心框架（如 Spring Boot, Express, Python 等）及其配置方式。
3. **Trace**: 追踪一个典型的“请求-处理-存储”链路，理清层级关系（Controller -> Service -> Repository）。
4. **Draft**: 按照上述结构编写文档，确保文档中使用的术语与代码中的类名、变量名保持一致。

# Constraints
- 使用专业、简洁的技术语言。
- 文档需具备“自解释性”，即任何一个新接入的 Agent 读完文档后都能立即开始工作。
- 必须包含 Mermaid 格式的架构图或流程图。
- 如果代码中存在不一致或模糊的地方，请在文档中以 [TBD] 或 [Warning] 标注。

# Language
- 请使用中文编写文档。
