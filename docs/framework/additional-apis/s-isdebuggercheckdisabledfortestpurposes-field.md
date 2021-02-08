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
# <a name="s_isdebuggercheckdisabledfortestpurposes-field"></a><span data-ttu-id="f1aa9-103">s_isDebuggerCheckDisabledForTestPurposes 字段</span><span class="sxs-lookup"><span data-stu-id="f1aa9-103">s_isDebuggerCheckDisabledForTestPurposes Field</span></span>

<span data-ttu-id="f1aa9-104">Visual Studio 使用类中的此私有字段 `System.Windows.Diagnostics.VisualDiagnostics` 来确定是否将执行活动调试器的内部检查。</span><span class="sxs-lookup"><span data-stu-id="f1aa9-104">This private field in the `System.Windows.Diagnostics.VisualDiagnostics` class is used by Visual Studio to determine whether an internal check for an active debugger will be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1aa9-105">语法</span><span class="sxs-lookup"><span data-stu-id="f1aa9-105">Syntax</span></span>

```csharp
private static bool s_isDebuggerCheckDisabledForTestPurposes
```

> [!WARNING]
> <span data-ttu-id="f1aa9-106">类中的 Api `System.Windows.Diagnostics.VisualDiagnostics` 仅当应用程序在调试器下运行时才可用。</span><span class="sxs-lookup"><span data-stu-id="f1aa9-106">APIs in the `System.Windows.Diagnostics.VisualDiagnostics` class are only available when an application is running under a debugger.</span></span> <span data-ttu-id="f1aa9-107">设置 `s_isDebuggerCheckDisabledForTestPurposes` 为 `true` ，以在调试器外部访问 api。</span><span class="sxs-lookup"><span data-stu-id="f1aa9-107">Set `s_isDebuggerCheckDisabledForTestPurposes` to `true` to access the APIs outside of a debugger.</span></span>
>
> <span data-ttu-id="f1aa9-108">在任何情况下，Microsoft 不支持在生产应用程序中使用此字段。</span><span class="sxs-lookup"><span data-stu-id="f1aa9-108">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1aa9-109">要求</span><span class="sxs-lookup"><span data-stu-id="f1aa9-109">Requirements</span></span>

<span data-ttu-id="f1aa9-110">**命名空间：** <xref:System.Windows.Diagnostics></span><span class="sxs-lookup"><span data-stu-id="f1aa9-110">**Namespace:** <xref:System.Windows.Diagnostics></span></span>

<span data-ttu-id="f1aa9-111">**程序集：** PresentationCore.dll 中的 PresentationCore () </span><span class="sxs-lookup"><span data-stu-id="f1aa9-111">**Assembly:** PresentationCore (in PresentationCore.dll)</span></span>

<span data-ttu-id="f1aa9-112">**.NET Framework 版本：** 自4.6 起可用。</span><span class="sxs-lookup"><span data-stu-id="f1aa9-112">**.NET Framework versions:** Available since 4.6.</span></span>
