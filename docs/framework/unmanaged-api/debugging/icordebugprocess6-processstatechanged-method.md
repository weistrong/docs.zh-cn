---
description: 了解详细信息： ICorDebugProcess6：:P rocessStateChanged 方法
title: ICorDebugProcess6::ProcessStateChanged 方法
ms.date: 03/30/2017
ms.assetid: fb6d30d9-54f3-462b-8ebf-ce0440791ad5
ms.openlocfilehash: 8060c29598adf5d4bbe7bffb4cd6611ee19a2669
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691362"
---
# <a name="icordebugprocess6processstatechanged-method"></a><span data-ttu-id="b4db3-103">ICorDebugProcess6::ProcessStateChanged 方法</span><span class="sxs-lookup"><span data-stu-id="b4db3-103">ICorDebugProcess6::ProcessStateChanged Method</span></span>

<span data-ttu-id="b4db3-104">通知 [ICorDebug](icordebug-interface.md) 进程正在运行。</span><span class="sxs-lookup"><span data-stu-id="b4db3-104">Notifies [ICorDebug](icordebug-interface.md) that the process is running.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4db3-105">语法</span><span class="sxs-lookup"><span data-stu-id="b4db3-105">Syntax</span></span>  
  
```cpp  
HRESULT ProcessStateChanged(   [in] CorDebugStateChange change);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b4db3-106">参数</span><span class="sxs-lookup"><span data-stu-id="b4db3-106">Parameters</span></span>  

 `change`  
 <span data-ttu-id="b4db3-107">中 [ProcessStateChanged](icordebugprocess6-processstatechanged-method.md) 枚举的成员</span><span class="sxs-lookup"><span data-stu-id="b4db3-107">[in] A member of the [ProcessStateChanged](icordebugprocess6-processstatechanged-method.md) enumeration</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b4db3-108">备注</span><span class="sxs-lookup"><span data-stu-id="b4db3-108">Remarks</span></span>  

 <span data-ttu-id="b4db3-109">调试器调用此方法来通知 [ICorDebug](icordebug-interface.md) 进程正在运行。</span><span class="sxs-lookup"><span data-stu-id="b4db3-109">The debugger calls this method to notify [ICorDebug](icordebug-interface.md) that the process is running.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b4db3-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="b4db3-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4db3-111">要求</span><span class="sxs-lookup"><span data-stu-id="b4db3-111">Requirements</span></span>  

 <span data-ttu-id="b4db3-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b4db3-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4db3-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b4db3-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b4db3-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b4db3-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b4db3-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4db3-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4db3-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="b4db3-116">See also</span></span>

- [<span data-ttu-id="b4db3-117">“ICor调试进程6”接口</span><span class="sxs-lookup"><span data-stu-id="b4db3-117">ICorDebugProcess6 Interface</span></span>](icordebugprocess6-interface.md)
- [<span data-ttu-id="b4db3-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="b4db3-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
