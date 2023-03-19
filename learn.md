refer: https://remix.run/docs/en/1.14.3/tutorials/blog#md-pulling-from-a-data-source


如果遇到 `error: Environment variable not found: DATABASE_URL.` 的报错，参考 https://github.com/remix-run/remix/issues/5341#issuecomment-1412835063。
全局安装 `pnpm add -g dotenv-cli` 然后修改 dev 命令：

```js
  "dev": "dotenv -e .env.example run-p dev:*",
```

如果执行 `npx prisma db push` 遇到报错 `error: Environment variable not found: DATABASE_URL.`，参考 https://github.com/remix-run/remix/issues/5341#issuecomment-1417448614，就拷贝 .env.example 得到 .env 文件，再执行 `npx prisma db push`。
