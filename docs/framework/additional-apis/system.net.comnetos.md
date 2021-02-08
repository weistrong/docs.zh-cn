---
description: 了解详细信息： ComNetOS 类
title: 'ComNetOS 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.ComNetOS
- System.Net.ComNetOS.IsWin7orLater
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 7376fe4a5e02818907cb71573451fffb3a3667cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802523"
---
# <a name="comnetos-class"></a>ComNetOS 类

提供有关当前操作系统的信息，如客户端或服务器)  (的版本和安装类型。 此类不能被继承。
  
```csharp  
internal static class ComNetOS
```

> [!WARNING]
> 此类是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此类。

## <a name="iswin7orlater-field"></a>IsWin7orLater 字段

指定操作系统版本是否为 Windows 7 或更高版本。

```csharp
internal static readonly bool IsWin7orLater
```

## <a name="requirements"></a>要求

**命名空间：** <xref:System.Net>

**程序集：** System.dll 中的系统 () 
