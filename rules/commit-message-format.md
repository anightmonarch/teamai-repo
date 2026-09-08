# Commit Message 规范

本仓库所有 commit message 遵循以下格式：

## 格式

```
<type>(<scope>): <subject>

<body>

<footer>
```

## Type

- `feat`：新功能
- `fix`：修复
- `docs`：文档
- `style`：格式
- `refactor`：重构
- `test`：测试
- `chore`：构建/工具

## Scope

使用模块名或目录名，如 `auth`、`api`、`cli`、`publish`。

## Subject

- 祈使句，首字母小写，结尾不加句号
- 不超过 50 字

## 示例

```
feat(publish): add retry for npm install EBUSY

On macOS, Spotlight indexing can temporarily lock node_modules.
Retry up to 3 times with 2s interval.

Closes #123
```

