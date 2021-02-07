---
description: 了解详细信息： IAssemblyName 接口
title: IAssemblyName 接口
ms.date: 03/30/2017
api_name:
- IAssemblyName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName
helpviewer_keywords:
- IAssemblyName interface [.NET Framework fusion]
ms.assetid: f7f8e605-6b67-4151-936f-f04ecd671d90
topic_type:
- apiref
ms.openlocfilehash: fb5949572adc533bab5ed26ee969267f430f36ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760701"
---
# <a name="iassemblyname-interface"></a><span data-ttu-id="14cae-103">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="14cae-103">IAssemblyName Interface</span></span>

<span data-ttu-id="14cae-104">提供用于描述和处理程序集的唯一标识的方法。</span><span class="sxs-lookup"><span data-stu-id="14cae-104">Provides methods for describing and working with an assembly's unique identity.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="14cae-105">方法</span><span class="sxs-lookup"><span data-stu-id="14cae-105">Methods</span></span>  
  
|<span data-ttu-id="14cae-106">方法</span><span class="sxs-lookup"><span data-stu-id="14cae-106">Method</span></span>|<span data-ttu-id="14cae-107">说明</span><span class="sxs-lookup"><span data-stu-id="14cae-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="14cae-108">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-108">Clone Method</span></span>](iassemblyname-clone-method.md)|<span data-ttu-id="14cae-109">创建此对象的浅表副本 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="14cae-109">Creates a shallow copy of this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="14cae-110">Finalize 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-110">Finalize Method</span></span>](iassemblyname-finalize-method.md)|<span data-ttu-id="14cae-111">允许此 `IAssemblyName` 对象在调用其析构函数之前释放资源并执行其他清理操作。</span><span class="sxs-lookup"><span data-stu-id="14cae-111">Allows this `IAssemblyName` object to release resources and perform other cleanup operations before its destructor is called.</span></span>|  
|[<span data-ttu-id="14cae-112">GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-112">GetDisplayName Method</span></span>](iassemblyname-getdisplayname-method.md)|<span data-ttu-id="14cae-113">获取此对象引用的程序集的可读名称 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="14cae-113">Gets the human-readable name of the assembly referenced by this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="14cae-114">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-114">GetName Method</span></span>](iassemblyname-getname-method.md)|<span data-ttu-id="14cae-115">获取此对象引用的程序集的简单、未加密名称 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="14cae-115">Gets the simple, unencrypted name of the assembly referenced by this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="14cae-116">GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-116">GetProperty Method</span></span>](iassemblyname-getproperty-method.md)|<span data-ttu-id="14cae-117">获取一个指针，该指针指向由指定的引用的属性 `PropertyId` 。</span><span class="sxs-lookup"><span data-stu-id="14cae-117">Gets a pointer to the property referenced by the specified `PropertyId`.</span></span>|  
|[<span data-ttu-id="14cae-118">GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-118">GetVersion Method</span></span>](iassemblyname-getversion-method.md)|<span data-ttu-id="14cae-119">获取此对象引用的程序集的版本信息 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="14cae-119">Gets the version information for the assembly referenced by this `IAssemblyName` object.</span></span>|  
|[<span data-ttu-id="14cae-120">IsEqual 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-120">IsEqual Method</span></span>](iassemblyname-isequal-method.md)|<span data-ttu-id="14cae-121">`IAssemblyName` `IAssemblyName` 根据指定的比较标志，确定指定的对象是否与此相等。</span><span class="sxs-lookup"><span data-stu-id="14cae-121">Determines whether a specified `IAssemblyName` object is equal to this `IAssemblyName`, based on the specified comparison flags.</span></span>|  
|[<span data-ttu-id="14cae-122">SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="14cae-122">SetProperty Method</span></span>](iassemblyname-setproperty-method.md)|<span data-ttu-id="14cae-123">设置由指定的引用的属性的值 `PropertyId` 。</span><span class="sxs-lookup"><span data-stu-id="14cae-123">Sets the value of the property referenced by the specified `PropertyId`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="14cae-124">要求</span><span class="sxs-lookup"><span data-stu-id="14cae-124">Requirements</span></span>  

 <span data-ttu-id="14cae-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="14cae-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="14cae-126">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="14cae-126">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="14cae-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="14cae-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="14cae-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="14cae-128">See also</span></span>

- [<span data-ttu-id="14cae-129">合成接口</span><span class="sxs-lookup"><span data-stu-id="14cae-129">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="14cae-130">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="14cae-130">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
