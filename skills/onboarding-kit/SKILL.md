---
name: onboarding-kit
description: 新人入职指南。当用户问"我们团队的 commit 规范"、"deploy 流程"、"项目怎么跑起来"时使用。
---

# 团队 Onboarding Kit

## Commit 规范
- type(scope): subject，type 用 feat/fix/docs/chore
- subject 不超过 50 字，祈使句

## 项目启动
- 本地开发: pnpm install && pnpm dev
- 测试: pnpm test
- 部署: 合并到 main 后自动走 GitHub Actions

## 常用路径
- API 文档: docs/api.md
- 环境变量模板: .env.example
