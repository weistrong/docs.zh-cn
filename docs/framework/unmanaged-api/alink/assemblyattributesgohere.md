---
description: 了解详细信息： AssemblyAttributesGoHere 类
title: 'AssemblyAttributesGoHere 类 (System.runtime.compilerservices) '
ms.date: 03/30/2017
api_name:
- System.Runtime.CompilerServices.AssemblyAttributesGoHere
api_location:
- mscorlib.dll
api_type:
- Assembly
f1_keywords:
- AssemblyAttributesGoHere
helpviewer_keywords:
- AssemblyAttributesGoHere type
- Alink API, AssemblyAttributesGoHere type
ms.assetid: 7b26fcb6-94f4-4f09-933e-b33efe451f4f
topic_type:
- apiref
ms.openlocfilehash: b95ff377f7fa0ffc85136dd69eb4a32121a50dc2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638582"
---
# <a name="assemblyattributesgohere-class"></a><span data-ttu-id="b5414-103">AssemblyAttributesGoHere 类</span><span class="sxs-lookup"><span data-stu-id="b5414-103">AssemblyAttributesGoHere Class</span></span>

<span data-ttu-id="b5414-104">由 ALink 用作占位符以存储有关自定义特性的信息。</span><span class="sxs-lookup"><span data-stu-id="b5414-104">Used by ALink as a placeholder to store information about custom attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5414-105">语法</span><span class="sxs-lookup"><span data-stu-id="b5414-105">Syntax</span></span>

```csharp
internal sealed class AssemblyAttributesGoHere
```

## <a name="remarks"></a><span data-ttu-id="b5414-106">备注</span><span class="sxs-lookup"><span data-stu-id="b5414-106">Remarks</span></span>

<span data-ttu-id="b5414-107">对此类型的引用可能被嵌入网络模块内，模块的源包含程序集自定义属性。</span><span class="sxs-lookup"><span data-stu-id="b5414-107">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="b5414-108">当从一个或多个包含对这些类型的引用的网络模块生成程序集清单时，ALink 将使用附加到这些引用的信息来发出实际的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="b5414-108">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="b5414-109">因此，此类型永远不会被实例化，而且对它的引用仅用作生成过程的一部分，在最终的程序集中不具有任何用途。</span><span class="sxs-lookup"><span data-stu-id="b5414-109">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>

<span data-ttu-id="b5414-110">对此类型的引用指示与安全性无关且用途单一的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="b5414-110">References to this type indicate custom attributes that are not security related and are not multiple-use.</span></span>

<span data-ttu-id="b5414-111">这些类型在 .NET Framework 中标记为 "internal"，位于 <xref:System.Runtime.CompilerServices> 命名空间中。</span><span class="sxs-lookup"><span data-stu-id="b5414-111">These types are marked "internal" within the .NET Framework and are located in the <xref:System.Runtime.CompilerServices> namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5414-112">要求</span><span class="sxs-lookup"><span data-stu-id="b5414-112">Requirements</span></span>

<span data-ttu-id="b5414-113">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="b5414-113">mscorlib.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="b5414-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5414-114">See also</span></span>

- [<span data-ttu-id="b5414-115">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="b5414-115">AssemblyAttributesGoHereM</span></span>](assemblyattributesgoherem.md)
- [<span data-ttu-id="b5414-116">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="b5414-116">AssemblyAttributesGoHereS</span></span>](assemblyattributesgoheres.md)
- [<span data-ttu-id="b5414-117">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="b5414-117">AssemblyAttributesGoHereSM</span></span>](assemblyattributesgoheresm.md)
