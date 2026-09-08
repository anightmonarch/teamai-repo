# 经验：npm install EBUSY 重试策略

## 场景

在 macOS 上运行 npm install 时，经常遇到 EBUSY 错误，原因是 Spotlight 索引正在扫描 node_modules。

## 解决方案

在 CI 脚本中增加重试逻辑：

```bash
for i in 1 2 3; do
  npm install && break
  echo "Retry $i..."
  sleep 2
done
```

## 效果

CI 失败率从 15% 降到 0.3%。

## 标签

troubleshooting, npm, macos, ci

