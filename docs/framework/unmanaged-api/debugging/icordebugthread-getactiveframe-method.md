---
description: 了解详细信息： ICorDebugThread：： GetActiveFrame 方法
title: ICorDebugThread::GetActiveFrame 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetActiveFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetActiveFrame
helpviewer_keywords:
- ICorDebugThread::GetActiveFrame method [.NET Framework debugging]
- GetActiveFrame method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 8d6d3a1a-fef6-4f2f-a22c-3bdd30d70e07
topic_type:
- apiref
ms.openlocfilehash: 3b15aad39503dfec9ac8f98f839ee1a6b16b3f90
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659252"
---
# <a name="icordebugthreadgetactiveframe-method"></a><span data-ttu-id="3601f-103">ICorDebugThread::GetActiveFrame 方法</span><span class="sxs-lookup"><span data-stu-id="3601f-103">ICorDebugThread::GetActiveFrame Method</span></span>

<span data-ttu-id="3601f-104">获取一个接口指针，该指针指向此 ICorDebugThread 对象上的活动 (最新) 帧。</span><span class="sxs-lookup"><span data-stu-id="3601f-104">Gets an interface pointer to the active (most recent) frame on this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3601f-105">语法</span><span class="sxs-lookup"><span data-stu-id="3601f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3601f-106">参数</span><span class="sxs-lookup"><span data-stu-id="3601f-106">Parameters</span></span>  

 `ppFrame`  
 <span data-ttu-id="3601f-107">弄指向表示帧的 ICorDebugFrame 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="3601f-107">[out] A pointer to the address of an ICorDebugFrame interface object that represents a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3601f-108">备注</span><span class="sxs-lookup"><span data-stu-id="3601f-108">Remarks</span></span>  

 <span data-ttu-id="3601f-109">`ppFrame`如果当前没有活动帧，则参数为 null。</span><span class="sxs-lookup"><span data-stu-id="3601f-109">The `ppFrame` parameter is null if no frame is currently active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3601f-110">要求</span><span class="sxs-lookup"><span data-stu-id="3601f-110">Requirements</span></span>  

 <span data-ttu-id="3601f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3601f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3601f-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3601f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3601f-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3601f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3601f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3601f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
