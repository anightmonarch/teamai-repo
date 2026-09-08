# 线上 502 排查：NODE_ENV 没配

## 症状
生产环境所有接口返回 502，本地正常。

## 排查过程
看 pm2 日志发现 `process.env.NODE_ENV` 是 undefined，导致代码走了本地配置，连了本地数据库。

## 根因
Dockerfile 里 `ENV NODE_ENV=production` 被后面的 `FROM` 覆盖了。

## 解法
把 ENV 挪到最后一个 FROM 之后。以后所有环境问题先查环境变量。

## 标签
troubleshooting, prod, env, 502
