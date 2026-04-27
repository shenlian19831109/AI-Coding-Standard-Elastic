# AI Coding Standard - Elastic (V2.0)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/shenlian19831109/AI-Coding-Standard-Elastic?style=social)](https://github.com/shenlian19831109/AI-Coding-Standard-Elastic/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/shenlian19831109/AI-Coding-Standard-Elastic?style=social)](https://github.com/shenlian19831109/AI-Coding-Standard-Elastic/network/members)

## AI 编程弹性约束规范 - 弹性三档版

[English](#english) | [中文](#chinese)

---

<a name="chinese"></a>
## 中文说明

### 🌟 核心理念

这是一个专为 AI 辅助编程（如 Cursor, Claude, GitHub Copilot）设计的工程化约束体系。它通过 **Fast / Balanced / Strict** 三档模式，解决了 AI 编程中常见的“幻觉”、“效率低下”和“代码污染”问题。该规范旨在帮助开发者在追求效率的同时，确保代码质量和安全性，实现 AI 编程的弹性与可控。

### 💡 为什么选择弹性约束？

传统的 AI 编程方式往往在效率和质量之间难以取舍：
- **过松的约束**：导致 AI 容易产生“幻觉”，生成低质量或不安全的代码，增加后期维护成本。
- **过严的约束**：限制了 AI 的创造力和速度，使得原型开发效率低下，失去了 AI 辅助的优势。

**AI 编程弹性约束规范**通过提供多档模式，让开发者可以根据项目阶段和代码敏感度，灵活调整 AI 的行为，实现效率与质量的最佳平衡。

### 🔧 快速开始

1.  将 `CLAUDE.md` 放入您的项目根目录。
2.  (可选) 将 `GLOSSARY.md` 放入根目录以统一项目中的业务术语和命名规范。
3.  (可选) 将 `.claude/skills/` 目录下的专项插件（如 `react.md`, `sql.md`）放入对应位置，以获得特定领域的 AI 编程优化。
4.  **激活模式**：在与 AI 对话开始时，明确告知 AI 您希望使用的模式：
    -   `"使用 fast 模式"`：适合原型开发、快速迭代和非核心功能。AI 将以最快速度响应，减少不必要的打断和冗余检查。
    -   `"使用 balanced 模式"`：默认推荐模式，兼顾代码质量与开发效率。AI 会进行适度的代码审查、安全检查和命名一致性提醒。
    -   `"使用 strict 模式"`：适合金融、安全或核心逻辑等高敏感度代码。AI 将强制进行溯源检查、避免幻觉，并执行严格的代码安全审计。

**示例 Prompt (使用 balanced 模式):**

```
请使用 balanced 模式，为我生成一个 React 组件，用于展示用户列表，并包含搜索和分页功能。
```

**预期效果:**

AI 将在 `balanced` 模式下，为您生成一个结构清晰、命名规范、并包含基本错误处理和安全考量的 React 用户列表组件。它会主动避免常见的编程错误，并提供高质量的代码建议。

### 📂 目录结构

-   `CLAUDE.md`: 核心调度中心，定义了弹性约束的逻辑和模式切换规则。
-   `GLOSSARY.md`: 业务术语表模板，用于统一项目中的命名和概念。
-   `.claude/skills/react.md`: React 开发专项插件，针对 React 生态提供优化。
-   `.claude/skills/sql.md`: SQL 与数据库安全插件，专注于 SQL 语句的安全性和性能优化。

---

<a name="english"></a>
## English Instructions

### 🌟 Core Concept

This is an engineering constraint system designed specifically for AI-assisted programming (e.g., Cursor, Claude, GitHub Copilot). It solves common AI programming issues like "hallucinations," "inefficiency," and "code pollution" through three dynamic modes: **Fast / Balanced / Strict**. This standard aims to help developers ensure code quality and security while pursuing efficiency, achieving flexibility and control in AI programming.

### 💡 Why Elastic Constraints?

Traditional AI programming often struggles to balance efficiency and quality:
-   **Loose Constraints**: AI tends to "hallucinate," generating low-quality or insecure code, increasing maintenance costs。
-   **Strict Constraints**: Limits AI creativity and speed, making prototyping inefficient and losing the advantages of AI assistance.

The **AI Coding Standard - Elastic** provides multi-tiered modes, allowing developers to flexibly adjust AI behavior based on project phase and code sensitivity, achieving the optimal balance between efficiency and quality.

### 🔧 Quick Start

1.  Place `CLAUDE.md` in your project root.
2.  (Optional) Place `GLOSSARY.md` in the root to unify naming conventions and business terminology.
3.  (Optional) Place specialized plugins from `.claude/skills/` (e.g., `react.md`, `sql.md`) into the corresponding directory for domain-specific AI programming optimization.
4.  **Activate Mode**: At the start of a conversation with the AI, explicitly state the mode you wish to use:
    -   `"Use fast mode"`: Ideal for prototyping, rapid iteration, and non-core functionalities. The AI will respond at maximum speed, minimizing interruptions and redundant checks.
    -   `"Use balanced mode"`: The default recommended mode, balancing code quality and development efficiency. The AI will perform moderate code reviews, security checks, and naming consistency reminders.
    -   `"Use strict mode"`: Best for highly sensitive code such as financial systems or core logic. The AI will enforce traceability, prevent hallucinations, and conduct rigorous code security audits.

**Example Prompt (using balanced mode):**

```
Please use balanced mode to generate a React component for displaying a user list, including search and pagination functionalities.
```

**Expected Outcome:**

Your AI assistant, operating in `balanced` mode, will generate a well-structured, consistently named React user list component that includes basic error handling and security considerations. It will proactively avoid common programming pitfalls and provide high-quality code suggestions.

### 📂 Directory Structure

-   `CLAUDE.md`: The core dispatch center, defining the logic for elastic constraints and mode switching rules.
-   `GLOSSARY.md`: A business glossary template, used to standardize naming and concepts within the project.
-   `.claude/skills/react.md`: A specialized plugin for React development, providing optimizations tailored to the React ecosystem.
-   `.claude/skills/sql.md`: A plugin for SQL and database security, focusing on the security and performance optimization of SQL statements.

## 🤝 Contributing

We welcome contributions to enhance the AI Coding Standard - Elastic! Whether it\"s improving existing guidelines, adding new plugins, or refining the mode definitions, your input is valuable. Please refer to our [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to get involved.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=shenlian19831109/AI-Coding-Standard-Elastic&type=Date)](https://star-history.com/#shenlian19831109/AI-Coding-Standard-Elastic&Date)
