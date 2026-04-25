# 项目术语表 (GLOSSARY.md)

本文件定义了项目中的核心业务术语及其对应的代码命名，AI 在 **Balanced** 和 **Strict** 模式下必须严格遵守。

## 核心实体 (Entities)

| 业务术语 | 代码命名 (Preferred) | 禁用命名 (Forbidden) | 说明 |
| :--- | :--- | :--- | :--- |
| 用户 ID | `user_id` | `uid`, `userId` | 统一使用下划线风格 |
| 订单状态 | `order_status` | `state`, `status` | |
| 支付金额 | `amount_cents` | `price`, `money` | 统一以“分”为单位 |

## 动作/方法 (Actions)

| 业务动作 | 命名惯例 | 示例 |
| :--- | :--- | :--- |
| 获取列表 | `get_{entity}_list` | `get_user_list` |
| 创建实体 | `create_{entity}` | `create_order` |
| 逻辑删除 | `soft_delete_{entity}` | `soft_delete_comment` |

## 状态枚举 (Enums)

*   **Order Status**: `PENDING`, `PAID`, `SHIPPED`, `COMPLETED`, `CANCELLED`
*   **User Role**: `ADMIN`, `EDITOR`, `VIEWER`
