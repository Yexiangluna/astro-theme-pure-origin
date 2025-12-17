---
title: 自定义组件
description: 创建和使用自定义组件
order: 1
---

# 自定义组件

本主题提供了丰富的组件系统，你可以创建自己的组件。

## 创建自定义组件

在 `src/components/` 目录下创建 `.astro` 文件：

```astro
---
// MyComponent.astro
interface Props {
  title: string
  description?: string
}

const { title, description } = Astro.props
---

<div class="my-component">
  <h3>{title}</h3>
  {description && <p>{description}</p>}
</div>

<style>
  .my-component {
    padding: 1rem;
    border: 1px solid var(--border);
    border-radius: 0.5rem;
  }
</style>
```

## 使用组件

在 MDX 文件中导入并使用：

```mdx
import MyComponent from '@/components/MyComponent.astro'

<MyComponent title="Hello" description="World" />
```

## 内置组件

主题提供了多种内置组件：

- `Button` - 按钮组件
- `Icon` - 图标组件
- `Quote` - 引用组件
- `TOC` - 目录组件
