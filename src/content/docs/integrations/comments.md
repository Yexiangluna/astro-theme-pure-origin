---
title: 评论系统
description: 集成 Waline 评论系统
order: 1
---

# 评论系统

本主题支持 Waline 评论系统。

## 启用 Waline

1. 首先部署 Waline 服务端，参考 [Waline 官方文档](https://waline.js.org/)

2. 在站点配置中启用评论：

```typescript
// site.config.ts
export default {
  comment: {
    waline: {
      serverURL: 'https://your-waline-server.vercel.app',
    }
  }
}
```

## 配置选项

```typescript
waline: {
  serverURL: 'https://...',  // Waline 服务端地址
  lang: 'zh-CN',             // 语言设置
  emoji: [                   // 表情包
    'https://unpkg.com/@waline/emojis@1.2.0/weibo',
  ],
}
```

## 禁用特定文章的评论

在文章 frontmatter 中设置：

```yaml
---
title: 我的文章
comment: false
---
```
