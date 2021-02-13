---
title: 中断性变更：一些 API 引发 ArgumentNullException
description: 了解 .NET 6.0 中的以下中断性变更：一些 API 现在会验证参数并引发 ArgumentNullException。
ms.date: 01/29/2021
ms.openlocfilehash: f9d7dc8bb57ed8dc5b4ff41bda9b3bde7db7b880
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804147"
---
# <a name="some-apis-throw-argumentnullexception"></a>一些 API 引发 ArgumentNullException

如果通过 `null` 输入参数进行调用，一些 API 现在会验证输入参数并引发 <xref:System.ArgumentNullException>，而此前会引发 <xref:System.NullReferenceException>。

## <a name="change-description"></a>更改描述

在以前的 .NET 版本中，在通过值为 `null` 的参数进行调用时，受影响的 API 会引发 <xref:System.NullReferenceException>。

从 .NET 6.0 开始，在通过值为 `null` 的参数进行调用时，受影响的 API 会引发 <xref:System.ArgumentNullException>。

## <a name="reason-for-change"></a>更改原因

引发 <xref:System.ArgumentNullException> 符合 .NET 运行时行为。 它提供了更好的调试体验，清晰地传达了是哪个参数引起的异常。

## <a name="version-introduced"></a>引入的版本

.NET 6.0

## <a name="recommended-action"></a>建议的操作

- 审查代码并在必要时更新，以防止向受影响的 API 传递 `null` 输入参数。
- 如果你的代码处理了 <xref:System.NullReferenceException>，请替换或增加一个 <xref:System.ArgumentNullException> 的处理程序。

## <a name="affected-apis"></a>受影响的 API

下表列出了受影响的属性：

| properties | 版本已更改 |
|-|-|-|-|
| <xref:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)?displayProperty=fullName> | 预览版 1 |

<!--

### Affected APIs

- `P:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)`

### Category

Windows Forms

-->
