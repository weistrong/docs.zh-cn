---
description: 了解详细信息： ICorDebugValueBreakpoint：： GetValue 方法
title: ICorDebugValueBreakpoint::GetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint::GetValue
helpviewer_keywords:
- GetValue method, ICorDebugValueBreakpoint interface [.NET Framework debugging]
- ICorDebugValueBreakpoint::GetValue method [.NET Framework debugging]
ms.assetid: 52a73654-bc47-48b6-b2b1-a4456b10140c
topic_type:
- apiref
ms.openlocfilehash: b690ea7a39ac70edd8e3e6be7682bae1e808555d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690166"
---
# <a name="icordebugvaluebreakpointgetvalue-method"></a><span data-ttu-id="1cdc0-103">ICorDebugValueBreakpoint::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="1cdc0-103">ICorDebugValueBreakpoint::GetValue Method</span></span>

<span data-ttu-id="1cdc0-104">获取一个指向 "ICorDebugValue" 对象的接口指针，该对象表示在其上设置断点的对象的值。</span><span class="sxs-lookup"><span data-stu-id="1cdc0-104">Gets an interface pointer to an "ICorDebugValue" object that represents the value of the object on which the breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cdc0-105">语法</span><span class="sxs-lookup"><span data-stu-id="1cdc0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetValue (  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1cdc0-106">参数</span><span class="sxs-lookup"><span data-stu-id="1cdc0-106">Parameters</span></span>  

 `ppValue`  
 <span data-ttu-id="1cdc0-107">弄指向对象地址的指针 `ICorDebugValue` 。</span><span class="sxs-lookup"><span data-stu-id="1cdc0-107">[out] A pointer to the address of an `ICorDebugValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1cdc0-108">要求</span><span class="sxs-lookup"><span data-stu-id="1cdc0-108">Requirements</span></span>  

 <span data-ttu-id="1cdc0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1cdc0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1cdc0-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1cdc0-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1cdc0-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1cdc0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1cdc0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1cdc0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cdc0-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="1cdc0-113">See also</span></span>
