---
title: 站点配置
description: 配置你的站点基本信息
order: 2
---

# 站点配置

本主题的配置文件位于 `src/site.config.ts`。

## 基本配置

```typescript
export default {
  // 站点标题
  title: '我的博客',

  // 站点描述
  description: '一个使用 Astro Theme Pure 的博客',

  // 作者信息
  author: '你的名字',

  // 日期格式配置
  dateLocale: 'zh-CN',
}
```

## 导航菜单

在 `header.menu` 中配置导航菜单：

```typescript
header: {
  menu: [
    { title: 'Blog', link: '/blog' },
    { title: 'Docs', link: '/docs' },
    { title: 'Projects', link: '/projects' },
    { title: 'About', link: '/about' },
  ]
}
```

## 社交链接

配置你的社交媒体链接：

```typescript
social: {
  github: 'https://github.com/username',
  twitter: 'https://twitter.com/username',
}
```
