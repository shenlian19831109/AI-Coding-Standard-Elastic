# SQL 与数据库专项规范 (sql.md)

本规范作为 `CLAUDE.md` 的扩展，仅在涉及数据库查询、Schema 变更或 ORM 操作时激活。

## 🛡️ 安全红线 (Security First)
1.  **参数化查询**：严禁任何形式的字符串拼接 SQL。无论在何种模式下，必须使用 `?` 或命名参数。
2.  **权限最小化**：严禁生成带有 `DROP`, `TRUNCATE` 或 `GRANT` 的语句，除非用户在 `Strict` 模式下明确授权。

## 🚀 性能与索引 (Performance)
1.  **索引感知**：在编写 `WHERE`, `JOIN`, `ORDER BY` 子句前，必须确认相关字段是否有索引。若不确定，必须询问用户或读取 `SHOW CREATE TABLE`。
2.  **大表保护**：
    *   严禁对百万级以上的表执行 `SELECT *`。
    *   所有查询必须带有 `LIMIT`，除非是明确的小表配置项。
3.  **N+1 预防**：在编写 ORM 代码（如 Prisma, TypeORM, SQLAlchemy）时，必须使用 `include` 或 `join` 预加载关联数据，严禁在循环中触发查询。

## 📂 变更规范 (Migrations)
1.  **非破坏性变更**：优先使用 `ADD COLUMN` 而非 `RENAME COLUMN`，确保代码回滚时数据库依然可用。
2.  **迁移脚本**：所有 Schema 变更必须提供独立的 `.sql` 迁移文件或 ORM Migration 脚本，并包含 `Up` 和 `Down` 逻辑。
