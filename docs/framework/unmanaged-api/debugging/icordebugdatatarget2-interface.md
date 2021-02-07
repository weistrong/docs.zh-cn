---
description: 了解详细信息： ICorDebugDataTarget2 接口
title: “ICor调试数据目标2”接口
ms.date: 03/30/2017
ms.assetid: 13f11388-2f91-48d8-98d6-6a4a63cb5746
ms.openlocfilehash: 13a83ee99f0158f32f466f9ae29af3d917248f95
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710460"
---
# <a name="icordebugdatatarget2-interface"></a><span data-ttu-id="f6b1d-103">“ICor调试数据目标2”接口</span><span class="sxs-lookup"><span data-stu-id="f6b1d-103">ICorDebugDataTarget2 Interface</span></span>

<span data-ttu-id="f6b1d-104">对 [ICorDebugDataTarget](icordebugdatatarget-interface.md)接口进行逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-104">Logically extends the [ICorDebugDataTarget](icordebugdatatarget-interface.md)interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f6b1d-105">方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-105">Methods</span></span>  
  
|<span data-ttu-id="f6b1d-106">方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-106">Method</span></span>|<span data-ttu-id="f6b1d-107">说明</span><span class="sxs-lookup"><span data-stu-id="f6b1d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f6b1d-108">CreateVirtualUnwinder 方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-108">CreateVirtualUnwinder Method</span></span>](icordebugdatatarget2-createvirtualunwinder-method.md)|<span data-ttu-id="f6b1d-109">创建一个从初始上下文（不一定是线程叶）开始展开的新堆栈开卷机。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-109">Creates a new stack unwinder that starts unwinding from an initial context (which isn't necessarily the leaf of a thread).</span></span>|  
|[<span data-ttu-id="f6b1d-110">EnumerateThreadIDs 方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-110">EnumerateThreadIDs Method</span></span>](icordebugdatatarget2-enumeratethreadids-method.md)|<span data-ttu-id="f6b1d-111">返回一组活动线程 ID。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-111">Returns a list of active thread IDs.</span></span>|  
|[<span data-ttu-id="f6b1d-112">GetImageFromPointer 方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-112">GetImageFromPointer Method</span></span>](icordebugdatatarget2-getimagefrompointer-method.md)|<span data-ttu-id="f6b1d-113">返回该模块地址中的模块基址和大小。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-113">Returns the module base address and size from an address in that module.</span></span>|  
|[<span data-ttu-id="f6b1d-114">GetImageLocation 方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-114">GetImageLocation Method</span></span>](icordebugdatatarget2-getimagelocation-method.md)|<span data-ttu-id="f6b1d-115">返回模块基址中的模块路径。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-115">Returns the path of a module from the module's base address.</span></span>|  
|[<span data-ttu-id="f6b1d-116">GetSymbolProviderForImage 方法</span><span class="sxs-lookup"><span data-stu-id="f6b1d-116">GetSymbolProviderForImage Method</span></span>](icordebugdatatarget2-getsymbolproviderforimage-method.md)|<span data-ttu-id="f6b1d-117">返回该模块基址中的模块符号提供程序。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-117">Returns the symbol-provider for a module from the base address of that module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6b1d-118">备注</span><span class="sxs-lookup"><span data-stu-id="f6b1d-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f6b1d-119">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-119">This interface is available with .NET Native only.</span></span> <span data-ttu-id="f6b1d-120">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-120">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6b1d-121">要求</span><span class="sxs-lookup"><span data-stu-id="f6b1d-121">Requirements</span></span>  

 <span data-ttu-id="f6b1d-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b1d-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6b1d-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f6b1d-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f6b1d-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f6b1d-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f6b1d-125">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6b1d-125">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6b1d-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6b1d-126">See also</span></span>

- [<span data-ttu-id="f6b1d-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="f6b1d-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="f6b1d-128">调试</span><span class="sxs-lookup"><span data-stu-id="f6b1d-128">Debugging</span></span>](index.md)
