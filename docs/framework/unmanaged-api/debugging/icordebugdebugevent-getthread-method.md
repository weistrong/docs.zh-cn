---
description: 了解详细信息： ICorDebugDebugEvent：： GetThread 方法
title: ICorDebugDebugEvent::GetThread Method
ms.date: 03/30/2017
ms.assetid: 4f2e9a2c-8369-4a07-a881-ad5422626353
ms.openlocfilehash: 1d476603572f31882f481d414e483c6712f1b5fc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710395"
---
# <a name="icordebugdebugeventgetthread-method"></a><span data-ttu-id="3bfbf-103">ICorDebugDebugEvent::GetThread Method</span><span class="sxs-lookup"><span data-stu-id="3bfbf-103">ICorDebugDebugEvent::GetThread Method</span></span>

<span data-ttu-id="3bfbf-104">获取发生事件的线程。</span><span class="sxs-lookup"><span data-stu-id="3bfbf-104">Gets the thread on which the event occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3bfbf-105">语法</span><span class="sxs-lookup"><span data-stu-id="3bfbf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThread(  
        [out]ICorDebugThread **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3bfbf-106">参数</span><span class="sxs-lookup"><span data-stu-id="3bfbf-106">Parameters</span></span>  

 <span data-ttu-id="3bfbf-107">ppThread</span><span class="sxs-lookup"><span data-stu-id="3bfbf-107">ppThread</span></span>  
 <span data-ttu-id="3bfbf-108">[输出] 指针指向代表事件发生线程的 ICorDebugThread 对象的地址。</span><span class="sxs-lookup"><span data-stu-id="3bfbf-108">[out] A pointer to the address of an ICorDebugThread object that represents the thread on which the event occurred.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3bfbf-109">备注</span><span class="sxs-lookup"><span data-stu-id="3bfbf-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3bfbf-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="3bfbf-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3bfbf-111">要求</span><span class="sxs-lookup"><span data-stu-id="3bfbf-111">Requirements</span></span>  

 <span data-ttu-id="3bfbf-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfbf-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3bfbf-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3bfbf-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3bfbf-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3bfbf-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3bfbf-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3bfbf-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3bfbf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="3bfbf-116">See also</span></span>

- [<span data-ttu-id="3bfbf-117">“ICor调试调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="3bfbf-117">ICorDebugDebugEvent Interface</span></span>](icordebugdebugevent-interface.md)
- [<span data-ttu-id="3bfbf-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="3bfbf-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
