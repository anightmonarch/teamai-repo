# Code Review 红线

以下情况必须打回：

1. API 调用没有 timeout
2. 异常被空 catch 吞掉
3. 命名用拼音或缩写（除 id/url/api）
4. 魔法数字，必须抽成常量
5. 新增依赖没有说明理由
