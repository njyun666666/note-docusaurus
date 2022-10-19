---
title: 使用ExcelJS將html表格匯出成excel
tags:
  - ExcelJS
  - Excel
  - Angular
---

使用 Angular 12 實作

## 安裝 ExcelJS

官方文件：[https://github.com/exceljs/exceljs](https://github.com/exceljs/exceljs)

1. 使用 npm 安裝

```bash
npm i exceljs
```

2. 在 tsconfig.app.json types 加入 node

```typescript title=tsconfig.app.json
{
  "extends": "./tsconfig.json",
  "compilerOptions": {
    "outDir": "./out-tsc/app",
    // highlight-next-line
    "types": ["node"]
  },
  "files": [
    "src/main.ts",
    "src/polyfills.ts"
  ],
  "include": [
    "src/**/*.d.ts"
  ]
}

```

3. 本次實作在 app.component.ts , 引入 exceljs

```typescript title=src\app\app.component.ts
import { Component } from '@angular/core';
// highlight-next-line
import * as Excel from 'exceljs';
import { saveAs } from 'file-saver';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
```

## 安裝 FileSaver.js

官方文件：[https://github.com/eligrey/FileSaver.js](https://github.com/eligrey/FileSaver.js)

1. 使用 npm 安裝

```bash
npm i file-saver
```

2. 在 app.component.ts 引入

```typescript title=src\app\app.component.ts
import { Component } from '@angular/core';
import * as Excel from 'exceljs';
// highlight-next-line
import { saveAs } from 'file-saver';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
```

## 後續實作請看 Github

[https://github.com/njyun666666/exceljs-demo](https://github.com/njyun666666/exceljs-demo)
