# AI Coding Standard - Elastic (V2.0)
## AI 编程弹性约束规范 - 弹性三档版

[English](#english) | [中文](#chinese)

---

<a name="chinese"></a>
## 中文说明

### 🌟 核心理念
这是一个专为 AI 辅助编程（如 Cursor, Claude, GitHub Copilot）设计的工程化约束体系。它通过 **Fast / Balanced / Strict** 三档模式，解决了 AI 编程中常见的“幻觉”、“效率低下”和“代码污染”问题。

### 🔧 快速开始
1. 将 `CLAUDE.md` 放入项目根目录。
2. (可选) 将 `GLOSSARY.md` 放入根目录以统一命名。
3. (可选) 将 `.claude/skills/` 目录下的插件放入对应位置。
4. **激活模式**：在对话开始时对 AI 说：
   - `"使用 fast 模式"`：适合原型开发，不打断，速度快。
   - `"使用 balanced 模式"`：默认推荐，兼顾质量与效率。
   - `"使用 strict 模式"`：适合金融/核心逻辑，强制溯源，零幻觉。

### 📂 目录结构
- `CLAUDE.md`: 核心调度中心。
- `GLOSSARY.md`: 业务术语表模板。
- `.claude/skills/react.md`: React 开发专项插件。
- `.claude/skills/sql.md`: SQL 与数据库安全插件。

---

<a name="english"></a>
## English Instructions

### 🌟 Core Concept
This is an engineering constraint system designed specifically for AI-assisted programming (e.g., Cursor, Claude, GitHub Copilot). It solves common AI programming issues like "hallucinations," "inefficiency," and "code pollution" through three dynamic modes: **Fast / Balanced / Strict**.

### 🔧 Quick Start
1. Place `CLAUDE.md` in your project root.
2. (Optional) Place `GLOSSARY.md` in the root to unify naming.
3. (Optional) Place the plugins from `.claude/skills/` into the corresponding directory.
4. **Activate Mode**: At the start of a conversation, tell the AI:
   - `"Use fast mode"`: Best for MVP/prototyping, no interruptions, high speed.
   - `"Use balanced mode"`: Default recommendation, balances quality and efficiency.
   - `"Use strict mode"`: Best for financial/core logic, mandatory sourcing, zero hallucinations.

### 📂 Directory Structure
- `CLAUDE.md`: Core dispatch center.
- `GLOSSARY.md`: Business glossary template.
- `.claude/skills/react.md`: Specialized plugin for React development.
- `.claude/skills/sql.md`: Specialized plugin for SQL and database security.
