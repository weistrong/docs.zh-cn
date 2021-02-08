---
description: 了解详细信息： IXCLRDataMethodDefinition 接口
title: IXCLRDataMethodDefinition 接口
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition Interface
helpviewer.keywords:
- IXCLRDataMethodDefinition Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: d73246b42a0bfb982c87b04d5490e945f7caa745
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790342"
---
# <a name="ixclrdatamethoddefinition-interface"></a><span data-ttu-id="0a81c-103">IXCLRDataMethodDefinition 接口</span><span class="sxs-lookup"><span data-stu-id="0a81c-103">IXCLRDataMethodDefinition Interface</span></span>

<span data-ttu-id="0a81c-104">提供用于查询有关方法定义的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="0a81c-104">Provides methods for querying information about a method definition.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="0a81c-105">方法</span><span class="sxs-lookup"><span data-stu-id="0a81c-105">Methods</span></span>

<span data-ttu-id="0a81c-106">以下方法是接口中的一些可用方法。</span><span class="sxs-lookup"><span data-stu-id="0a81c-106">The following methods are some of the methods available in the interface.</span></span>

| <span data-ttu-id="0a81c-107">方法</span><span class="sxs-lookup"><span data-stu-id="0a81c-107">Method</span></span>                                                                                                                          | <span data-ttu-id="0a81c-108">说明</span><span class="sxs-lookup"><span data-stu-id="0a81c-108">Description</span></span>                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="0a81c-109">StartEnumInstances</span><span class="sxs-lookup"><span data-stu-id="0a81c-109">StartEnumInstances</span></span>](ixclrdatamethoddefinition-startenuminstances-method.md) | <span data-ttu-id="0a81c-110">为给定的的方法实例枚举提供句柄 `IXCLRDataAppDomain` 。</span><span class="sxs-lookup"><span data-stu-id="0a81c-110">Provides a handle for the enumeration of method instances for a given `IXCLRDataAppDomain`.</span></span> |
| [<span data-ttu-id="0a81c-111">EnumInstance</span><span class="sxs-lookup"><span data-stu-id="0a81c-111">EnumInstance</span></span>](ixclrdatamethoddefinition-enuminstance-method.md)             | <span data-ttu-id="0a81c-112">枚举此方法定义的实例。</span><span class="sxs-lookup"><span data-stu-id="0a81c-112">Enumerates the instances of this method definition.</span></span>                                         |
| [<span data-ttu-id="0a81c-113">EndEnumInstances</span><span class="sxs-lookup"><span data-stu-id="0a81c-113">EndEnumInstances</span></span>](ixclrdatamethoddefinition-endenuminstances-method.md)     | <span data-ttu-id="0a81c-114">释放实例枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="0a81c-114">Releases the resources used by internal iterators used during instance enumeration.</span></span>         |

## <a name="remarks"></a><span data-ttu-id="0a81c-115">备注</span><span class="sxs-lookup"><span data-stu-id="0a81c-115">Remarks</span></span>

<span data-ttu-id="0a81c-116">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="0a81c-116">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="0a81c-117">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `AAF60008-FB2C-420b-8FB1-42D244A54A97` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="0a81c-117">However, it's a COM interface that derives from `IUnknown` with GUID `AAF60008-FB2C-420b-8FB1-42D244A54A97` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a81c-118">要求</span><span class="sxs-lookup"><span data-stu-id="0a81c-118">Requirements</span></span>

<span data-ttu-id="0a81c-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0a81c-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="0a81c-120">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="0a81c-120">**Header:** None</span></span>  
<span data-ttu-id="0a81c-121">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="0a81c-121">**Library:** None</span></span>  
<span data-ttu-id="0a81c-122">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0a81c-122">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="0a81c-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="0a81c-123">See also</span></span>

- [<span data-ttu-id="0a81c-124">调试</span><span class="sxs-lookup"><span data-stu-id="0a81c-124">Debugging</span></span>](index.md)
- [<span data-ttu-id="0a81c-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="0a81c-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
