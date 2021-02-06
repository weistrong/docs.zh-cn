---
description: 了解详细信息： ICorDebugThread：： GetProcess 方法
title: ICorDebugThread::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetProcess
helpviewer_keywords:
- ICorDebugThread::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 163816e7-0739-4566-b3df-cd256be8b8a4
topic_type:
- apiref
ms.openlocfilehash: dac5da30b343ebd17c1b1ebdd6d4cfa38b78f0bd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658927"
---
# <a name="icordebugthreadgetprocess-method"></a><span data-ttu-id="7dce5-103">ICorDebugThread::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="7dce5-103">ICorDebugThread::GetProcess Method</span></span>

<span data-ttu-id="7dce5-104">获取一个接口指针，该指针指向此 ICorDebugThread 构成部件的进程。</span><span class="sxs-lookup"><span data-stu-id="7dce5-104">Gets an interface pointer to the process of which this ICorDebugThread forms a part.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7dce5-105">语法</span><span class="sxs-lookup"><span data-stu-id="7dce5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7dce5-106">参数</span><span class="sxs-lookup"><span data-stu-id="7dce5-106">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="7dce5-107">弄指向表示进程的 ICorDebugProcess 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="7dce5-107">[out] A pointer to the address of an ICorDebugProcess interface object that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7dce5-108">要求</span><span class="sxs-lookup"><span data-stu-id="7dce5-108">Requirements</span></span>  

 <span data-ttu-id="7dce5-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7dce5-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7dce5-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7dce5-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7dce5-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7dce5-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7dce5-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7dce5-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
