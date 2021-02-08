---
description: 了解详细信息： ICorDebugMDA：： GetFlags 方法
title: ICorDebugMDA::GetFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetFlags
helpviewer_keywords:
- ICorDebugMDA::GetFlags method [.NET Framework debugging]
- GetFlags method [.NET Framework debugging]
ms.assetid: 87ce7c5b-fd82-453e-bf55-c8a32150b183
topic_type:
- apiref
ms.openlocfilehash: 53476da06252771627d4883ef9056eb7f945e1b8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801164"
---
# <a name="icordebugmdagetflags-method"></a><span data-ttu-id="f20a7-103">ICorDebugMDA::GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="f20a7-103">ICorDebugMDA::GetFlags Method</span></span>

<span data-ttu-id="f20a7-104">获取与托管调试助手关联的标志 (MDA) [ICorDebugMDA](icordebugmda-interface.md)表示。</span><span class="sxs-lookup"><span data-stu-id="f20a7-104">Gets the flags associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f20a7-105">语法</span><span class="sxs-lookup"><span data-stu-id="f20a7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFlags (  
    [in] CorDebugMDAFlags *pFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f20a7-106">参数</span><span class="sxs-lookup"><span data-stu-id="f20a7-106">Parameters</span></span>  

 `pFlags`  
 <span data-ttu-id="f20a7-107">中 [CorDebugMDAFlags](cordebugmdaflags-enumeration.md) 枚举值的按位组合，这些值指定此 MDA 的标志的设置。</span><span class="sxs-lookup"><span data-stu-id="f20a7-107">[in] A bitwise combination of the [CorDebugMDAFlags](cordebugmdaflags-enumeration.md) enumeration values that specify the settings of the flags for this MDA.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f20a7-108">要求</span><span class="sxs-lookup"><span data-stu-id="f20a7-108">Requirements</span></span>  

 <span data-ttu-id="f20a7-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f20a7-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f20a7-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f20a7-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f20a7-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f20a7-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f20a7-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f20a7-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f20a7-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f20a7-113">See also</span></span>

- [<span data-ttu-id="f20a7-114">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="f20a7-114">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="f20a7-115">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="f20a7-115">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
