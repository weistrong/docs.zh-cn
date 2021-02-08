---
description: 了解详细信息： s_isDebuggerCheckDisabledForTestPurposes 字段
title: s_isDebuggerCheckDisabledForTestPurposes 字段
ms.date: 03/30/2017
ms.technology: dotnet-wpf
topic_type:
- apiref
api_name:
- System.Windows.Diagnostics.VisualDiagnostics.s_isDebuggerCheckDisabledForTestPurposes
api_location:
- PresentationCore.dll
api_type:
- Assembly
ms.assetid: 9033a513-c255-4f31-b6d7-09b8d8c50e2d
ms.openlocfilehash: a71235c13a7a35872bcf5374be8077bafad5ff9a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802653"
---
# <a name="s_isdebuggercheckdisabledfortestpurposes-field"></a>s_isDebuggerCheckDisabledForTestPurposes 字段

Visual Studio 使用类中的此私有字段 `System.Windows.Diagnostics.VisualDiagnostics` 来确定是否将执行活动调试器的内部检查。

## <a name="syntax"></a>语法

```csharp
private static bool s_isDebuggerCheckDisabledForTestPurposes
```

> [!WARNING]
> 类中的 Api `System.Windows.Diagnostics.VisualDiagnostics` 仅当应用程序在调试器下运行时才可用。 设置 `s_isDebuggerCheckDisabledForTestPurposes` 为 `true` ，以在调试器外部访问 api。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此字段。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Windows.Diagnostics>

**程序集：** PresentationCore.dll 中的 PresentationCore () 

**.NET Framework 版本：** 自4.6 起可用。
