---
description: 了解详细信息： ICorDebugProcess：： ThreadForFiberCookie 方法
title: ICorDebugProcess::ThreadForFiberCookie 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ThreadForFiberCookie
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ThreadForFiberCookie
helpviewer_keywords:
- ICorDebugProcess::ThreadForFiberCookie method [.NET Framework debugging]
- ThreadForFiberCookie method [.NET Framework debugging]
ms.assetid: afe4e97f-bffc-47e1-adad-d6e842487f35
topic_type:
- apiref
ms.openlocfilehash: e3618d08f0b5212dbc8502194926c9ae0c97744b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650191"
---
# <a name="icordebugprocessthreadforfibercookie-method"></a><span data-ttu-id="d872a-103">ICorDebugProcess::ThreadForFiberCookie 方法</span><span class="sxs-lookup"><span data-stu-id="d872a-103">ICorDebugProcess::ThreadForFiberCookie Method</span></span>

<span data-ttu-id="d872a-104">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="d872a-104">This method is not implemented.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d872a-105">语法</span><span class="sxs-lookup"><span data-stu-id="d872a-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadForFiberCookie (  
    [in] DWORD fiberCookie,  
    [out] ICorDebugThread **ppThread  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="d872a-106">要求</span><span class="sxs-lookup"><span data-stu-id="d872a-106">Requirements</span></span>  

 <span data-ttu-id="d872a-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d872a-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d872a-108">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d872a-108">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d872a-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d872a-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d872a-110">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d872a-110">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
