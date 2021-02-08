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
# <a name="comnetos-class"></a><span data-ttu-id="c67cc-103">ComNetOS 类</span><span class="sxs-lookup"><span data-stu-id="c67cc-103">ComNetOS class</span></span>

<span data-ttu-id="c67cc-104">提供有关当前操作系统的信息，如客户端或服务器)  (的版本和安装类型。</span><span class="sxs-lookup"><span data-stu-id="c67cc-104">Provides information about the current operating system, such as its version and installation type (client or server).</span></span> <span data-ttu-id="c67cc-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="c67cc-105">This class cannot be inherited.</span></span>
  
```csharp  
internal static class ComNetOS
```

> [!WARNING]
> <span data-ttu-id="c67cc-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="c67cc-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="c67cc-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="c67cc-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="iswin7orlater-field"></a><span data-ttu-id="c67cc-108">IsWin7orLater 字段</span><span class="sxs-lookup"><span data-stu-id="c67cc-108">IsWin7orLater field</span></span>

<span data-ttu-id="c67cc-109">指定操作系统版本是否为 Windows 7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="c67cc-109">Specifies whether the operating system version is Windows 7 or later.</span></span>

```csharp
internal static readonly bool IsWin7orLater
```

## <a name="requirements"></a><span data-ttu-id="c67cc-110">要求</span><span class="sxs-lookup"><span data-stu-id="c67cc-110">Requirements</span></span>

<span data-ttu-id="c67cc-111">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="c67cc-111">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="c67cc-112">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="c67cc-112">**Assembly:** System (in System.dll)</span></span>
