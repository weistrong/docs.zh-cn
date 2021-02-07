---
description: 了解详细信息： ICorDebugDebugEvent：： GetEventKind 方法
title: ICorDebugDebugEvent::GetEventKind 方法
ms.date: 03/30/2017
ms.assetid: c37aaceb-c948-46bd-a943-08be4cbb76f4
ms.openlocfilehash: 9e15eb82195fae8aa3797ea47cb04d0bb407d2ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764315"
---
# <a name="icordebugdebugeventgeteventkind-method"></a><span data-ttu-id="6f47f-103">ICorDebugDebugEvent::GetEventKind 方法</span><span class="sxs-lookup"><span data-stu-id="6f47f-103">ICorDebugDebugEvent::GetEventKind Method</span></span>

<span data-ttu-id="6f47f-104">指出该 `ICorDebugDebugEvent` 对象代表的事件类型。</span><span class="sxs-lookup"><span data-stu-id="6f47f-104">Indicates what kind of event this `ICorDebugDebugEvent` object represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f47f-105">语法</span><span class="sxs-lookup"><span data-stu-id="6f47f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetEventKind(  
    [out]CorDebugDebugEventKind *pDebugEventKind  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6f47f-106">参数</span><span class="sxs-lookup"><span data-stu-id="6f47f-106">Parameters</span></span>  

 <span data-ttu-id="6f47f-107">p调试事件类型</span><span class="sxs-lookup"><span data-stu-id="6f47f-107">pDebugEventKind</span></span>  
 <span data-ttu-id="6f47f-108">指向指示事件类型的 [CorDebugDebugEventKind](cordebugdebugeventkind-enumeration.md) 枚举成员的指针。</span><span class="sxs-lookup"><span data-stu-id="6f47f-108">A pointer to a [CorDebugDebugEventKind](cordebugdebugeventkind-enumeration.md) enumeration member that indicates the type of event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6f47f-109">备注</span><span class="sxs-lookup"><span data-stu-id="6f47f-109">Remarks</span></span>  

 <span data-ttu-id="6f47f-110">基于 `pDebugEventKind` 值，可调用 `QueryInterface` 以获取包含其他数据的精确度更高的调试事件接口。</span><span class="sxs-lookup"><span data-stu-id="6f47f-110">Based on the value of `pDebugEventKind`, you can call `QueryInterface` to get a more precise debug event interface that has additional data.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6f47f-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="6f47f-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f47f-112">要求</span><span class="sxs-lookup"><span data-stu-id="6f47f-112">Requirements</span></span>  

 <span data-ttu-id="6f47f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6f47f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f47f-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6f47f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6f47f-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6f47f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6f47f-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f47f-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f47f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="6f47f-117">See also</span></span>

- [<span data-ttu-id="6f47f-118">“ICor调试调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="6f47f-118">ICorDebugDebugEvent Interface</span></span>](icordebugdebugevent-interface.md)
- [<span data-ttu-id="6f47f-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="6f47f-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
