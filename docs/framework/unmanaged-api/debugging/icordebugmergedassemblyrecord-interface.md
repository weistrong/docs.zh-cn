---
description: 了解详细信息： ICorDebugMergedAssemblyRecord 接口
title: ICorDebugMergedAssemblyRecord 接口
ms.date: 03/30/2017
ms.assetid: fe280b11-9479-4e34-a07c-0d1ea8088422
ms.openlocfilehash: e64c0ee30a8e8956dd336a30e6c81962c75f04e9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650282"
---
# <a name="icordebugmergedassemblyrecord-interface"></a><span data-ttu-id="085c7-103">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="085c7-103">ICorDebugMergedAssemblyRecord Interface</span></span>

<span data-ttu-id="085c7-104">提供有关合并的程序集的信息。</span><span class="sxs-lookup"><span data-stu-id="085c7-104">Provides information about a merged assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="085c7-105">方法</span><span class="sxs-lookup"><span data-stu-id="085c7-105">Methods</span></span>  
  
|<span data-ttu-id="085c7-106">方法</span><span class="sxs-lookup"><span data-stu-id="085c7-106">Method</span></span>|<span data-ttu-id="085c7-107">说明</span><span class="sxs-lookup"><span data-stu-id="085c7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="085c7-108">GetCulture 方法</span><span class="sxs-lookup"><span data-stu-id="085c7-108">GetCulture Method</span></span>](icordebugmergedassemblyrecord-getculture-method.md)|<span data-ttu-id="085c7-109">获取程序集的区域性名称字符串。</span><span class="sxs-lookup"><span data-stu-id="085c7-109">Gets the culture name string of the assembly.</span></span>|  
|[<span data-ttu-id="085c7-110">GetIndex 方法</span><span class="sxs-lookup"><span data-stu-id="085c7-110">GetIndex Method</span></span>](icordebugmergedassemblyrecord-getindex-method.md)|<span data-ttu-id="085c7-111">获取程序集的前缀索引。</span><span class="sxs-lookup"><span data-stu-id="085c7-111">Gets the assembly's prefix index.</span></span>|  
|[<span data-ttu-id="085c7-112">GetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="085c7-112">GetPublicKey Method</span></span>](icordebugmergedassemblyrecord-getpublickey-method.md)|<span data-ttu-id="085c7-113">获取程序集的公钥。</span><span class="sxs-lookup"><span data-stu-id="085c7-113">Gets the assembly's public key.</span></span>|  
|[<span data-ttu-id="085c7-114">GetPublicKeyToken 方法</span><span class="sxs-lookup"><span data-stu-id="085c7-114">GetPublicKeyToken Method</span></span>](icordebugmergedassemblyrecord-getpublickeytoken-method.md)|<span data-ttu-id="085c7-115">获取程序集的公钥标记。</span><span class="sxs-lookup"><span data-stu-id="085c7-115">Gets the assembly's public key token.</span></span>|  
|[<span data-ttu-id="085c7-116">GetSimpleName 方法</span><span class="sxs-lookup"><span data-stu-id="085c7-116">GetSimpleName Method</span></span>](icordebugmergedassemblyrecord-getsimplename-method.md)|<span data-ttu-id="085c7-117">获取程序集的简单名。</span><span class="sxs-lookup"><span data-stu-id="085c7-117">Gets the simple name of the assembly.</span></span>|  
|[<span data-ttu-id="085c7-118">GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="085c7-118">GetVersion Method</span></span>](icordebugmergedassemblyrecord-getversion-method.md)|<span data-ttu-id="085c7-119">获取程序集的版本信息。</span><span class="sxs-lookup"><span data-stu-id="085c7-119">Gets the assembly's version information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="085c7-120">备注</span><span class="sxs-lookup"><span data-stu-id="085c7-120">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="085c7-121">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="085c7-121">This interface is available with .NET Native only.</span></span> <span data-ttu-id="085c7-122">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="085c7-122">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="085c7-123">要求</span><span class="sxs-lookup"><span data-stu-id="085c7-123">Requirements</span></span>  

 <span data-ttu-id="085c7-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="085c7-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="085c7-125">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="085c7-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="085c7-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="085c7-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="085c7-127">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="085c7-127">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="085c7-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="085c7-128">See also</span></span>

- [<span data-ttu-id="085c7-129">调试接口</span><span class="sxs-lookup"><span data-stu-id="085c7-129">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="085c7-130">调试</span><span class="sxs-lookup"><span data-stu-id="085c7-130">Debugging</span></span>](index.md)
