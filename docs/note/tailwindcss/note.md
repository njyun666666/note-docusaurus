---
sidebar_position: 0
title: Note
tags:
  - Tailwind CSS
---

## Tools

- [Tailwind CSS](https://tailwindcss.com/docs/installation)
- [tailwind-merge](https://github.com/dcastil/tailwind-merge)
- [clsx](https://github.com/lukeed/clsx)

## 新增 cn

使用 cn 來更輕鬆地有條件地添加 Tailwind CSS 類別

```ts title="utils.ts"
import {type ClassValue, clsx} from 'clsx';
import {twMerge} from 'tailwind-merge';

export const cn = (...inputs: ClassValue[]) => {
  return twMerge(clsx(inputs));
};
```
