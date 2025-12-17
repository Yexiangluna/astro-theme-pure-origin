---
title: 搜索功能
description: 使用 Pagefind 实现全站搜索
order: 2
---

# 搜索功能

本主题集成了 Pagefind 全站搜索功能。

## 构建搜索索引

搜索索引会在构建时自动生成：

```bash
bun build
```

## 搜索配置

Pagefind 默认会索引所有博客文章。你可以通过以下方式排除特定内容：

```html
<div data-pagefind-ignore>
  这段内容不会被索引
</div>
```

## 自定义搜索 UI

搜索组件位于 `packages/pure/components/Search.astro`，你可以根据需要自定义样式。

## 搜索快捷键

- `Ctrl/Cmd + K` - 打开搜索框
- `Esc` - 关闭搜索框
