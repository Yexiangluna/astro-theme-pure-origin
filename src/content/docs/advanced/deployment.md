---
title: 部署指南
description: 部署你的博客到各种平台
order: 2
---

# 部署指南

本主题支持部署到多种平台。

## Vercel (推荐)

1. 将代码推送到 GitHub
2. 在 Vercel 导入项目
3. 使用默认配置即可

或使用 CLI：

```bash
npx vercel
```

## Netlify

```bash
# 安装 Netlify 适配器
bun add @astrojs/netlify
```

修改 `astro.config.ts`：

```typescript
import netlify from '@astrojs/netlify'

export default defineConfig({
  adapter: netlify(),
})
```

## GitHub Pages

1. 设置 `base` 路径（如果部署到子路径）
2. 配置 GitHub Actions workflow

```yaml
# .github/workflows/deploy.yml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: oven-sh/setup-bun@v1
      - run: bun install
      - run: bun build
      - uses: actions/upload-pages-artifact@v2
        with:
          path: ./dist
```

## 自托管

使用 Node.js 适配器进行服务端渲染：

```bash
bun add @astrojs/node
```

```typescript
import node from '@astrojs/node'

export default defineConfig({
  adapter: node({ mode: 'standalone' }),
  output: 'server',
})
```
