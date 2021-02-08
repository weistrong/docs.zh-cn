---
description: 了解详细信息： ICorDebugVirtualUnwinder：： Next 方法
title: ICorDebugVirtualUnwinder::Next 方法
ms.date: 03/30/2017
ms.assetid: 790e0426-e5cd-49fd-a792-f8c8635d72fe
ms.openlocfilehash: b509e8e4fb24c66764999e67ba7e36299ce7f570
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790511"
---
# <a name="icordebugvirtualunwindernext-method"></a><span data-ttu-id="46cfe-103">ICorDebugVirtualUnwinder::Next 方法</span><span class="sxs-lookup"><span data-stu-id="46cfe-103">ICorDebugVirtualUnwinder::Next Method</span></span>

<span data-ttu-id="46cfe-104">前进到调用方的上下文。</span><span class="sxs-lookup"><span data-stu-id="46cfe-104">Advances to the caller's context.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46cfe-105">语法</span><span class="sxs-lookup"><span data-stu-id="46cfe-105">Syntax</span></span>  
  
```cpp  
HRESULT Next();  
```  
  
## <a name="parameters"></a><span data-ttu-id="46cfe-106">参数</span><span class="sxs-lookup"><span data-stu-id="46cfe-106">Parameters</span></span>  

 <span data-ttu-id="46cfe-107">无。</span><span class="sxs-lookup"><span data-stu-id="46cfe-107">None.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="46cfe-108">返回值</span><span class="sxs-lookup"><span data-stu-id="46cfe-108">Return Value</span></span>  

 <span data-ttu-id="46cfe-109">如果成功展开，则为 `S_OK`如果因帧不够而无法完全展开，则为 `CORDBG_S_AT_END_OF_STACK`。</span><span class="sxs-lookup"><span data-stu-id="46cfe-109">`S_OK` if the unwind occurred successfully, or `CORDBG_S_AT_END_OF_STACK` if the unwind cannot be completed because there are no more frames.</span></span>  
  
 <span data-ttu-id="46cfe-110">如果返回失败的 HRESULT，则 ICorDebug API 将返回 `CORDBG_E_DATA_TARGET_ERROR`。</span><span class="sxs-lookup"><span data-stu-id="46cfe-110">If a failing HRESULT is returned, ICorDebug APIs will return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="46cfe-111">备注</span><span class="sxs-lookup"><span data-stu-id="46cfe-111">Remarks</span></span>  

 <span data-ttu-id="46cfe-112">堆栈查看器应确保向前推进，以便最后 `Next` 的调用将返回失败的 HRESULT 或 `CORDBG_S_AT_END_OF_STACK`。</span><span class="sxs-lookup"><span data-stu-id="46cfe-112">The stack walker should ensure that it makes forward progress, so that eventually a call to `Next` will return a failing HRESULT or `CORDBG_S_AT_END_OF_STACK`.</span></span> <span data-ttu-id="46cfe-113">`S_OK`无限期返回可能导致无限循环。</span><span class="sxs-lookup"><span data-stu-id="46cfe-113">Returning `S_OK` indefinitely may cause an infinite loop.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="46cfe-114">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="46cfe-114">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46cfe-115">要求</span><span class="sxs-lookup"><span data-stu-id="46cfe-115">Requirements</span></span>  

 <span data-ttu-id="46cfe-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46cfe-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46cfe-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46cfe-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46cfe-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46cfe-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46cfe-119">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46cfe-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46cfe-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="46cfe-120">See also</span></span>

- [<span data-ttu-id="46cfe-121">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="46cfe-121">ICorDebugMemoryBuffer Interface</span></span>](icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="46cfe-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="46cfe-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
