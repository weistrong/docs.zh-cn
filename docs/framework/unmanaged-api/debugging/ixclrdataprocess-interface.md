---
description: 了解详细信息： IXCLRDataProcess 接口
title: IXCLRDataProcess 接口
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess Interface
helpviewer.keywords:
- IXCLRDataProcess Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: b611491e5c9a5957c07a305a3f395b67ad208649
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800638"
---
# <a name="ixclrdataprocess-interface"></a><span data-ttu-id="e658e-103">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="e658e-103">IXCLRDataProcess Interface</span></span>

<span data-ttu-id="e658e-104">提供用于查询有关进程的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="e658e-104">Provides methods for querying information about a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="e658e-105">方法</span><span class="sxs-lookup"><span data-stu-id="e658e-105">Methods</span></span>

| <span data-ttu-id="e658e-106">方法</span><span class="sxs-lookup"><span data-stu-id="e658e-106">Method</span></span>                                                                                                                                               | <span data-ttu-id="e658e-107">说明</span><span class="sxs-lookup"><span data-stu-id="e658e-107">Description</span></span>                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="e658e-108">GetRuntimeNameByAddress</span><span class="sxs-lookup"><span data-stu-id="e658e-108">GetRuntimeNameByAddress</span></span>](ixclrdataprocess-getruntimenamebyaddress-method.md)                     | <span data-ttu-id="e658e-109">获取给定地址的名称。</span><span class="sxs-lookup"><span data-stu-id="e658e-109">Gets a name for the given address.</span></span>                                                               |
| [<span data-ttu-id="e658e-110">GetAppDomainByUniqueId</span><span class="sxs-lookup"><span data-stu-id="e658e-110">GetAppDomainByUniqueId</span></span>](ixclrdataprocess-getappdomainbyuniqueid-method.md)                       | <span data-ttu-id="e658e-111">`AppDomain`按其唯一 id 在进程中获取。</span><span class="sxs-lookup"><span data-stu-id="e658e-111">Gets an `AppDomain` in a process by its unique id.</span></span>                                              |
| [<span data-ttu-id="e658e-112">StartEnumModules</span><span class="sxs-lookup"><span data-stu-id="e658e-112">StartEnumModules</span></span>](ixclrdataprocess-startenummodules-method.md)                                   | <span data-ttu-id="e658e-113">提供枚举进程的模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="e658e-113">Provides a handle to enumerate the modules of a process.</span></span>                                        |
| [<span data-ttu-id="e658e-114">EnumModule</span><span class="sxs-lookup"><span data-stu-id="e658e-114">EnumModule</span></span>](ixclrdataprocess-enummodule-method.md)                                               | <span data-ttu-id="e658e-115">枚举此进程的模块。</span><span class="sxs-lookup"><span data-stu-id="e658e-115">Enumerates the modules of this process.</span></span>                                                         |
| [<span data-ttu-id="e658e-116">EndEnumModules</span><span class="sxs-lookup"><span data-stu-id="e658e-116">EndEnumModules</span></span>](ixclrdataprocess-endenummodules-method.md)                                       | <span data-ttu-id="e658e-117">释放模块枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="e658e-117">Releases the resources used by internal iterators used during module enumeration.</span></span>               |
| [<span data-ttu-id="e658e-118">StartEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="e658e-118">StartEnumMethodInstancesByAddress</span></span>](ixclrdataprocess-startenummethodinstancesbyaddress-method.md) | <span data-ttu-id="e658e-119">提供用于枚举 `AppDomain` 从给定地址开始的方法实例的句柄。</span><span class="sxs-lookup"><span data-stu-id="e658e-119">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span> |
| [<span data-ttu-id="e658e-120">EnumMethodInstanceByAddress</span><span class="sxs-lookup"><span data-stu-id="e658e-120">EnumMethodInstanceByAddress</span></span>](ixclrdataprocess-enummethodinstancebyaddress-method.md)             | <span data-ttu-id="e658e-121">枚举此进程的方法实例（从地址偏移量开始）。</span><span class="sxs-lookup"><span data-stu-id="e658e-121">Enumerates the method instances of this process starting at an address offset.</span></span>                  |
| [<span data-ttu-id="e658e-122">EndEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="e658e-122">EndEnumMethodInstancesByAddress</span></span>](ixclrdataprocess-endenummethodinstancesbyaddress-method.md)     | <span data-ttu-id="e658e-123">释放实例枚举期间使用的内部迭代器所使用的资源。</span><span class="sxs-lookup"><span data-stu-id="e658e-123">Releases the resources used by internal iterators used during instance enumeration.</span></span>             |

## <a name="remarks"></a><span data-ttu-id="e658e-124">备注</span><span class="sxs-lookup"><span data-stu-id="e658e-124">Remarks</span></span>

<span data-ttu-id="e658e-125">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="e658e-125">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="e658e-126">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="e658e-126">However, it's a COM interface that derives from `IUnknown` with GUID `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="e658e-127">要求</span><span class="sxs-lookup"><span data-stu-id="e658e-127">Requirements</span></span>

<span data-ttu-id="e658e-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e658e-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>
<span data-ttu-id="e658e-129">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="e658e-129">**Header:** None</span></span>  
<span data-ttu-id="e658e-130">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="e658e-130">**Library:** None</span></span>  
<span data-ttu-id="e658e-131">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e658e-131">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="e658e-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="e658e-132">See also</span></span>

- [<span data-ttu-id="e658e-133">调试</span><span class="sxs-lookup"><span data-stu-id="e658e-133">Debugging</span></span>](index.md)
- [<span data-ttu-id="e658e-134">调试接口</span><span class="sxs-lookup"><span data-stu-id="e658e-134">Debugging Interfaces</span></span>](debugging-interfaces.md)
