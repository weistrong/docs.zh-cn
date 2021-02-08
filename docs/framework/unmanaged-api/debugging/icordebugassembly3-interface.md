---
description: 了解详细信息： ICorDebugAssembly3 接口
title: “ICor调试程序集3”接口
ms.date: 03/30/2017
ms.assetid: 17fc5d76-75a9-4933-83f0-594de7f973f3
ms.openlocfilehash: 3a8cabf41dffa75d82c2b6fde53dff2ede4838e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791499"
---
# <a name="icordebugassembly3-interface"></a><span data-ttu-id="48f26-103">“ICor调试程序集3”接口</span><span class="sxs-lookup"><span data-stu-id="48f26-103">ICorDebugAssembly3 Interface</span></span>

<span data-ttu-id="48f26-104">对 ICorDebugAssembly 接口进行逻辑扩展，从而为容器程序集及其包含的程序集提供支持。</span><span class="sxs-lookup"><span data-stu-id="48f26-104">Logically extends the ICorDebugAssembly interface to provide support for container assemblies and their contained assemblies.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="48f26-105">方法</span><span class="sxs-lookup"><span data-stu-id="48f26-105">Methods</span></span>  
  
|<span data-ttu-id="48f26-106">方法</span><span class="sxs-lookup"><span data-stu-id="48f26-106">Method</span></span>|<span data-ttu-id="48f26-107">说明</span><span class="sxs-lookup"><span data-stu-id="48f26-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="48f26-108">EnumerateContainedAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="48f26-108">EnumerateContainedAssemblies Method</span></span>](icordebugassembly3-enumeratecontainedassemblies-method.md)|<span data-ttu-id="48f26-109">获取该程序集中所包含的程序集的枚举器。</span><span class="sxs-lookup"><span data-stu-id="48f26-109">Gets an enumerator for the assemblies contained in this assembly.</span></span>|  
|[<span data-ttu-id="48f26-110">GetContainerAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="48f26-110">GetContainerAssembly Method</span></span>](icordebugassembly3-getcontainerassembly-method.md)|<span data-ttu-id="48f26-111">返回该 `ICorDebugAssembly3` 对象的容器程序集。</span><span class="sxs-lookup"><span data-stu-id="48f26-111">Returns the container assembly of this `ICorDebugAssembly3` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="48f26-112">备注</span><span class="sxs-lookup"><span data-stu-id="48f26-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="48f26-113">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="48f26-113">The interface is available with .NET Native only.</span></span> <span data-ttu-id="48f26-114">尝试调用 `QueryInterface` 来检索接口指针会为 .NET Native 外部的 ICorDebug 方案返回 `E_NOINTERFACE`。</span><span class="sxs-lookup"><span data-stu-id="48f26-114">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48f26-115">要求</span><span class="sxs-lookup"><span data-stu-id="48f26-115">Requirements</span></span>  

 <span data-ttu-id="48f26-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="48f26-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48f26-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="48f26-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="48f26-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48f26-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="48f26-119">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48f26-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48f26-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="48f26-120">See also</span></span>

- [<span data-ttu-id="48f26-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="48f26-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="48f26-122">调试</span><span class="sxs-lookup"><span data-stu-id="48f26-122">Debugging</span></span>](index.md)
