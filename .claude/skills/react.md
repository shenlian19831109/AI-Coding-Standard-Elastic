# React 开发专项规范 (react.md)

本规范作为 `CLAUDE.md` 的扩展，仅在涉及 React 组件、Hooks 或前端状态管理时激活。

## 🛠️ 环境对齐 (Environment Alignment)
1.  **版本感知**：在编写任何 UI 组件前，必须读取 `package.json` 确认以下版本：
    *   React 版本 (v16/17/18)：决定是否使用 `Concurrent` 特性。
    *   UI 库版本 (如 AntD v4 vs v5, MUI v4 vs v5)：严禁混用不同版本的 API。
2.  **依赖最小化**：严禁为了实现简单功能（如：防抖、深拷贝）引入新的 npm 包，优先检查项目内是否有 `utils/` 或已安装 `lodash-es`。

## 🧩 组件编写规范
1.  **增量修改**：修改现有组件时，严禁重构未受影响的逻辑。保持 Diff 干净，方便 Review。
2.  **Hooks 约束**：
    *   `useEffect` 必须明确所有依赖项，严禁使用 `// eslint-disable-line` 绕过检查。
    *   复杂逻辑必须抽离为自定义 Hook (`useWorkFlow`)，保持组件 UI 纯粹。
3.  **状态管理**：遵循项目既有方案（Zustand / Redux / Context）。若无方案，默认使用 `useState` 提升，严禁擅自引入外部状态库。

## 🎨 样式与性能
1.  **样式对齐**：检查项目使用 Tailwind, CSS Modules 还是 Styled-components，严禁混用。
2.  **渲染优化**：在 `Strict` 模式下，大列表渲染必须使用虚拟列表 (Virtual List)，且必须对昂贵的计算使用 `useMemo`。
