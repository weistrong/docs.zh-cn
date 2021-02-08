---
description: 了解详细信息： ICorDebugAppDomain：： EnumerateBreakpoints 方法
title: ICorDebugAppDomain::EnumerateBreakpoints 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateBreakpoints
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateBreakpoints
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateBreakpoints method [.NET Framework debugging]
- EnumerateBreakpoints method [.NET Framework debugging]
ms.assetid: 206069c5-25cb-4794-9d69-67c5aa7ed0af
topic_type:
- apiref
ms.openlocfilehash: 4bd9857b9c662bc76c7c9481f306b20e823e446f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772454"
---
# <a name="icordebugappdomainenumeratebreakpoints-method"></a><span data-ttu-id="8cff5-103">ICorDebugAppDomain::EnumerateBreakpoints 方法</span><span class="sxs-lookup"><span data-stu-id="8cff5-103">ICorDebugAppDomain::EnumerateBreakpoints Method</span></span>

<span data-ttu-id="8cff5-104">获取应用程序域中所有活动断点的枚举器。</span><span class="sxs-lookup"><span data-stu-id="8cff5-104">Gets an enumerator for all active breakpoints in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cff5-105">语法</span><span class="sxs-lookup"><span data-stu-id="8cff5-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateBreakpoints (  
    [out] ICorDebugBreakpointEnum   **ppBreakpoints  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8cff5-106">参数</span><span class="sxs-lookup"><span data-stu-id="8cff5-106">Parameters</span></span>  

 `ppBreakpoints`  
 <span data-ttu-id="8cff5-107">弄指向 ICorDebugBreakpointEnum 对象地址的指针，该对象是应用程序域中所有活动断点的枚举器。</span><span class="sxs-lookup"><span data-stu-id="8cff5-107">[out] A pointer to the address of an ICorDebugBreakpointEnum object that is the enumerator for all active breakpoints in the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8cff5-108">备注</span><span class="sxs-lookup"><span data-stu-id="8cff5-108">Remarks</span></span>  

 <span data-ttu-id="8cff5-109">枚举器包含所有类型的断点，包括函数断点和数据断点。</span><span class="sxs-lookup"><span data-stu-id="8cff5-109">The enumerator includes all types of breakpoints, including function breakpoints and data breakpoints.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8cff5-110">要求</span><span class="sxs-lookup"><span data-stu-id="8cff5-110">Requirements</span></span>  

 <span data-ttu-id="8cff5-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8cff5-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8cff5-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8cff5-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8cff5-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8cff5-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8cff5-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8cff5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
