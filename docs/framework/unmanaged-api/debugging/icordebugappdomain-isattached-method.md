---
description: 了解详细信息： ICorDebugAppDomain：： IsAttached 方法
title: ICorDebugAppDomain::IsAttached 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.IsAttached
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::IsAttached
helpviewer_keywords:
- IsAttached method [.NET Framework debugging]
- ICorDebugAppDomain::IsAttached method [.NET Framework debugging]
ms.assetid: af0c67c7-f53e-47c9-b84b-be50bd04903e
topic_type:
- apiref
ms.openlocfilehash: 79427d08be9ffea253695b67767d68589edf6979
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772375"
---
# <a name="icordebugappdomainisattached-method"></a><span data-ttu-id="9ea44-103">ICorDebugAppDomain::IsAttached 方法</span><span class="sxs-lookup"><span data-stu-id="9ea44-103">ICorDebugAppDomain::IsAttached Method</span></span>

<span data-ttu-id="9ea44-104">获取一个值，该值指示调试器是否已附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="9ea44-104">Gets a value that indicates whether the debugger is attached to the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ea44-105">语法</span><span class="sxs-lookup"><span data-stu-id="9ea44-105">Syntax</span></span>  
  
```cpp  
HRESULT IsAttached (  
    [out] BOOL  *pbAttached  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ea44-106">参数</span><span class="sxs-lookup"><span data-stu-id="9ea44-106">Parameters</span></span>  

 `pbAttached`  
 <span data-ttu-id="9ea44-107">[out] `true` 如果调试器附加到应用程序域，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="9ea44-107">[out] `true` if the debugger is attached to the application domain; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9ea44-108">备注</span><span class="sxs-lookup"><span data-stu-id="9ea44-108">Remarks</span></span>  

 <span data-ttu-id="9ea44-109">在调试器附加到应用程序域之前，不能使用 ICorDebugController 方法。</span><span class="sxs-lookup"><span data-stu-id="9ea44-109">The ICorDebugController methods cannot be used until the debugger attaches to the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ea44-110">要求</span><span class="sxs-lookup"><span data-stu-id="9ea44-110">Requirements</span></span>  

 <span data-ttu-id="9ea44-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea44-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ea44-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ea44-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ea44-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ea44-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ea44-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ea44-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
