---
title: 截取字串時遇到emoji
---

# 截取字串時遇到 emoji

## 一般字串使用 Substring

```csharp
string str = "今天線上沒買到的朋友別哭哭，8/4還有活動喔!!";
var newStr = str.Substring(0,14);

// highlight-next-line
// newStr = "今天線上沒買到的朋友別哭哭，"
```

## 包含 emoji 的字串使用 Substring

```csharp
string str = "今天線上沒買到的朋友別哭哭😭8/4還有活動喔😍🥰";
var newStr = str.Substring(0,14);

// highlight-next-line
// newStr = "今天線上沒買到的朋友別哭哭\ud83d"
```

## 解法

```csharp
string str = "今天線上沒買到的朋友別哭哭😭8/4還有活動喔😍🥰";
var stringInfo = new System.Globalization.StringInfo(str);
var newStr = stringInfo.SubstringByTextElements(0, 14);

// highlight-next-line
// newStr = "今天線上沒買到的朋友別哭哭😭"
```

## 參考資料

- [StringInfo 類別](https://docs.microsoft.com/zh-tw/dotnet/api/system.globalization.stringinfo?view=net-6.0)
- [StringInfo.SubstringByTextElements 方法](https://docs.microsoft.com/zh-tw/dotnet/api/system.globalization.stringinfo.substringbytextelements?view=net-6.0)
