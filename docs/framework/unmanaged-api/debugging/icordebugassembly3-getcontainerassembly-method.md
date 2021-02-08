---
description: 了解详细信息： ICorDebugAssembly3：： GetContainerAssembly 方法
title: ICorDebugAssembly3::GetContainerAssembly 方法
ms.date: 03/30/2017
ms.assetid: f5fddeb6-b82e-4ebb-b432-849ce8513c77
ms.openlocfilehash: 5a6bc6dfb1c8403137a9444ff1cc4f64e75da65d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791512"
---
# <a name="icordebugassembly3getcontainerassembly-method"></a><span data-ttu-id="cc1ea-103">ICorDebugAssembly3::GetContainerAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="cc1ea-103">ICorDebugAssembly3::GetContainerAssembly Method</span></span>

<span data-ttu-id="cc1ea-104">返回该 `ICorDebugAssembly3` 对象的容器程序集。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-104">Returns the container assembly of this `ICorDebugAssembly3` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc1ea-105">语法</span><span class="sxs-lookup"><span data-stu-id="cc1ea-105">Syntax</span></span>  
  
```cpp  
HRESULT GetContainerAssembly(  
    ICorDebugAssembly **ppAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc1ea-106">参数</span><span class="sxs-lookup"><span data-stu-id="cc1ea-106">Parameters</span></span>  

 `ppAssembly`  
 <span data-ttu-id="cc1ea-107">指向表示容器程序集的 ICorDebugAssembly 对象地址的指针; 如果方法调用失败，则为 **null** 。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-107">A pointer to the address of an ICorDebugAssembly object that represents the container assembly, or **null** if the method call fails.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cc1ea-108">返回值</span><span class="sxs-lookup"><span data-stu-id="cc1ea-108">Return Value</span></span>  

 <span data-ttu-id="cc1ea-109">`S_OK` 如果方法调用成功，则为; 否则为。否则， `S_FALSE` 和 `ppAssembly` 为 **null**。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-109">`S_OK` if the method call succeeds; otherwise, `S_FALSE`, and `ppAssembly` is **null**.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc1ea-110">备注</span><span class="sxs-lookup"><span data-stu-id="cc1ea-110">Remarks</span></span>  

 <span data-ttu-id="cc1ea-111">如果程序集和单独容器程序集内的其他程序集合并，则方法返回容器程序集。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-111">If this assembly has been merged with others inside a single container assembly, this method returns the container assembly.</span></span> <span data-ttu-id="cc1ea-112">有关详细信息和术语，请参阅 [ICorDebugProcess6：： EnableVirtualModuleSplitting](icordebugprocess6-enablevirtualmodulesplitting-method.md) 主题。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-112">For more information and terminology, see the [ICorDebugProcess6::EnableVirtualModuleSplitting](icordebugprocess6-enablevirtualmodulesplitting-method.md) topic.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cc1ea-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc1ea-114">要求</span><span class="sxs-lookup"><span data-stu-id="cc1ea-114">Requirements</span></span>  

 <span data-ttu-id="cc1ea-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc1ea-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cc1ea-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cc1ea-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cc1ea-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cc1ea-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc1ea-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc1ea-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc1ea-119">See also</span></span>

- [<span data-ttu-id="cc1ea-120">“ICor调试程序集3”接口</span><span class="sxs-lookup"><span data-stu-id="cc1ea-120">ICorDebugAssembly3 Interface</span></span>](icordebugassembly3-interface.md)
- [<span data-ttu-id="cc1ea-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="cc1ea-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
