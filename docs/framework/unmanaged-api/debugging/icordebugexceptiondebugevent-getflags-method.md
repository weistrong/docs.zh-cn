---
description: 了解详细信息： ICorDebugExceptionDebugEvent：： GetFlags 方法
title: ICorDebugExceptionDebugEvent::GetFlags 方法
ms.date: 03/30/2017
ms.assetid: 73225303-8852-487e-9a0e-9f0cb95e99d9
ms.openlocfilehash: 54a6c9b0dff2346ca130f80e72fe06dbb3017f10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693468"
---
# <a name="icordebugexceptiondebugeventgetflags-method"></a><span data-ttu-id="80f1f-103">ICorDebugExceptionDebugEvent::GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="80f1f-103">ICorDebugExceptionDebugEvent::GetFlags Method</span></span>

<span data-ttu-id="80f1f-104">获取指示是否可拦截异常的标志。</span><span class="sxs-lookup"><span data-stu-id="80f1f-104">Gets a flag that indicates whether the exception can be intercepted.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80f1f-105">语法</span><span class="sxs-lookup"><span data-stu-id="80f1f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFlags(  
   [out] CorDebugExceptionFlags *pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="80f1f-106">参数</span><span class="sxs-lookup"><span data-stu-id="80f1f-106">Parameters</span></span>  

 `pdwFlags`  
 <span data-ttu-id="80f1f-107">弄指向 [CorDebugExceptionFlags](cordebugexceptionflags-enumeration.md) 值的指针，该指针指示是否可以截获异常。</span><span class="sxs-lookup"><span data-stu-id="80f1f-107">[out] A pointer to a [CorDebugExceptionFlags](cordebugexceptionflags-enumeration.md) value that indicates whether the exception can be intercepted.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="80f1f-108">备注</span><span class="sxs-lookup"><span data-stu-id="80f1f-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="80f1f-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="80f1f-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="80f1f-110">要求</span><span class="sxs-lookup"><span data-stu-id="80f1f-110">Requirements</span></span>  

 <span data-ttu-id="80f1f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="80f1f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80f1f-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="80f1f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="80f1f-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="80f1f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="80f1f-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80f1f-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80f1f-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="80f1f-115">See also</span></span>

- [<span data-ttu-id="80f1f-116">“ICor调试异常调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="80f1f-116">ICorDebugExceptionDebugEvent Interface</span></span>](icordebugexceptiondebugevent-interface.md)
- [<span data-ttu-id="80f1f-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="80f1f-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
