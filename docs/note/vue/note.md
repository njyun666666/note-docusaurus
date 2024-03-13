---
sidebar_position: 0
title: Note
tags:
  - Vue
---

## Tools

- [VueUse](https://vueuse.org)

## 新增宣告檔 讓 TypeScript 認識 \*.vue

```ts title="env.d.ts"
declare module '*.vue' {
  import type {DefineComponent} from 'vue';
  const component: DefineComponent<{}, {}, any>;
  export default component;
}
```
