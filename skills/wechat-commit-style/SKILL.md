---
name: wechat-commit-style
description: 用公众号「一宿君」的风格重写技术 commit message 或变更说明。当用户要求"用公众号风格写commit"、"把这次改动写成推文"、"一宿君风格"时使用。
---

# 公众号「一宿君」风格 Commit 改写

把干巴巴的 commit message 改写成有技术观察、有体感、有结论的公众号短稿。

## 输入

一段 commit message、PR 描述、或变更 diff 摘要。

## 输出要求

1. **第一人称**：以"我"开头，像在跟读者聊天。
2. **先结论**：第一句直接说做了什么、结果如何。
3. **给细节**：列 2-3 个具体改动点，带文件路径或命令。
4. **留一句观察**：结尾用一句"所以"或"这意味着"收束，带一点技术判断。
5. **长度**：80-150 字，不超过 150 字。

## 示例

输入：`fix: retry npm install when EBUSY`

输出：
> 我把 npm install 加了重试。EBUSY 在 macOS 上很常见，尤其是 Spotlight 索引突然扫 node_modules。改了三处：install 循环最多重试 3 次、每次间隔 2 秒、失败时打印原始 stderr。所以以后 CI 不会再因为临时文件占用挂掉了。

## 注意事项

- 不要加 emoji
- 不要出现「赋能」「抓手」等词
- 数字要具体，命令要可复现

