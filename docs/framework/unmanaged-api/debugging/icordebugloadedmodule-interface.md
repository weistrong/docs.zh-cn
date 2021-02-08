---
description: 了解详细信息： ICorDebugLoadedModule 接口
title: ICorDebugLoadedModule 接口
ms.date: 03/30/2017
ms.assetid: 34be6369-2e75-4a95-a538-3b29ac97cf6d
ms.openlocfilehash: 6a1b466a9d2d7781fad7ac2bc8c24f0b2a5c23e0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801223"
---
# <a name="icordebugloadedmodule-interface"></a><span data-ttu-id="e025f-103">ICorDebugLoadedModule 接口</span><span class="sxs-lookup"><span data-stu-id="e025f-103">ICorDebugLoadedModule Interface</span></span>

<span data-ttu-id="e025f-104">提供有关已加载模块的信息。</span><span class="sxs-lookup"><span data-stu-id="e025f-104">Provides information about a loaded module.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e025f-105">方法</span><span class="sxs-lookup"><span data-stu-id="e025f-105">Methods</span></span>  
  
|<span data-ttu-id="e025f-106">方法</span><span class="sxs-lookup"><span data-stu-id="e025f-106">Method</span></span>|<span data-ttu-id="e025f-107">说明</span><span class="sxs-lookup"><span data-stu-id="e025f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e025f-108">GetBaseAddress 方法</span><span class="sxs-lookup"><span data-stu-id="e025f-108">GetBaseAddress Method</span></span>](icordebugloadedmodule-getbaseaddress-method.md)|<span data-ttu-id="e025f-109">获取已加载模块的基址。</span><span class="sxs-lookup"><span data-stu-id="e025f-109">Gets the base address of the loaded module.</span></span>|  
|[<span data-ttu-id="e025f-110">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="e025f-110">GetName Method</span></span>](icordebugloadedmodule-getname-method.md)|<span data-ttu-id="e025f-111">获取加载模块的名称。</span><span class="sxs-lookup"><span data-stu-id="e025f-111">Gets the name of the loaded module.</span></span>|  
|[<span data-ttu-id="e025f-112">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="e025f-112">GetSize Method</span></span>](icordebugloadedmodule-getsize-method.md)|<span data-ttu-id="e025f-113">获取加载模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="e025f-113">Gets the size in bytes of the loaded module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e025f-114">备注</span><span class="sxs-lookup"><span data-stu-id="e025f-114">Remarks</span></span>  

 <span data-ttu-id="e025f-115">`ICorDebugLoadedModule` 接口由调试器实现并且被 CLR 调试接口使用，以便从调试器中获取有关加载的模块的信息。</span><span class="sxs-lookup"><span data-stu-id="e025f-115">The `ICorDebugLoadedModule` interface is implemented by a debugger and is used by the CLR debugging interfaces to get information about the loaded module from the debugger.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e025f-116">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="e025f-116">This interface is available with .NET Native only.</span></span> <span data-ttu-id="e025f-117">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="e025f-117">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e025f-118">要求</span><span class="sxs-lookup"><span data-stu-id="e025f-118">Requirements</span></span>  

 <span data-ttu-id="e025f-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e025f-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e025f-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e025f-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e025f-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e025f-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e025f-122">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e025f-122">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e025f-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="e025f-123">See also</span></span>

- [<span data-ttu-id="e025f-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="e025f-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="e025f-125">调试</span><span class="sxs-lookup"><span data-stu-id="e025f-125">Debugging</span></span>](index.md)
