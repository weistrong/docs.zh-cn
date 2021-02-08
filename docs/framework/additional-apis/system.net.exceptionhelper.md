---
description: 了解详细信息： ExceptionHelper 类
title: 'ExceptionHelper 类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.ExceptionHelper
- System.Net.ExceptionHelper.WebPermissionUnrestricted
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: d1411eae985b45903ceca2ef2d3ff772b643bd52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804122"
---
# <a name="exceptionhelper-class"></a><span data-ttu-id="3eb08-103">ExceptionHelper 类</span><span class="sxs-lookup"><span data-stu-id="3eb08-103">ExceptionHelper class</span></span>

<span data-ttu-id="3eb08-104">提供具有标准化错误消息的异常。</span><span class="sxs-lookup"><span data-stu-id="3eb08-104">Provides exceptions with standardized error messages.</span></span> <span data-ttu-id="3eb08-105">此类不能被继承。</span><span class="sxs-lookup"><span data-stu-id="3eb08-105">This class cannot be inherited.</span></span>

```csharp
internal static class ExceptionHelper
```

> [!WARNING]
> <span data-ttu-id="3eb08-106">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="3eb08-106">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="3eb08-107">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="3eb08-107">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="webpermissionunrestricted-field"></a><span data-ttu-id="3eb08-108">WebPermissionUnrestricted 字段</span><span class="sxs-lookup"><span data-stu-id="3eb08-108">WebPermissionUnrestricted field</span></span>

<span data-ttu-id="3eb08-109">指定应用程序可以连接到 internet 资源。</span><span class="sxs-lookup"><span data-stu-id="3eb08-109">Specifies that the app can connect to internet resources.</span></span>

```csharp
internal static readonly WebPermission WebPermissionUnrestricted
```

## <a name="requirements"></a><span data-ttu-id="3eb08-110">要求</span><span class="sxs-lookup"><span data-stu-id="3eb08-110">Requirements</span></span>

<span data-ttu-id="3eb08-111">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="3eb08-111">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="3eb08-112">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="3eb08-112">**Assembly:** System (in System.dll)</span></span>
