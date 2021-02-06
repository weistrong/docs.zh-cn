---
description: 了解详细信息： ICorDebugThread2：： GetVolatileOSThreadID 方法
title: ICorDebugThread2::GetVolatileOSThreadID 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetVolatileOSThreadID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetVolatileOSThreadID
helpviewer_keywords:
- GetVolatileOSThreadID method [.NET Framework debugging]
- ICorDebugThread2::GetVolatileOSThreadID method [.NET Framework debugging]
ms.assetid: f0922545-c2cf-40c8-9ef6-ca033563e682
topic_type:
- apiref
ms.openlocfilehash: 2c198577195c9b1e4a3a74fae686e405b22120eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658576"
---
# <a name="icordebugthread2getvolatileosthreadid-method"></a><span data-ttu-id="6d732-103">ICorDebugThread2::GetVolatileOSThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="6d732-103">ICorDebugThread2::GetVolatileOSThreadID Method</span></span>

<span data-ttu-id="6d732-104">获取此 ICorDebugThread2 的操作系统线程标识符。</span><span class="sxs-lookup"><span data-stu-id="6d732-104">Gets the operating system thread identifier for this ICorDebugThread2.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d732-105">语法</span><span class="sxs-lookup"><span data-stu-id="6d732-105">Syntax</span></span>  
  
```cpp  
HRESULT GetVolatileOSThreadID (  
    [out] DWORD    *pdwTid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6d732-106">参数</span><span class="sxs-lookup"><span data-stu-id="6d732-106">Parameters</span></span>  

 `pdwTid`  
 <span data-ttu-id="6d732-107">弄此线程的操作系统线程标识符。</span><span class="sxs-lookup"><span data-stu-id="6d732-107">[out] The operating system thread identifier for this thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d732-108">要求</span><span class="sxs-lookup"><span data-stu-id="6d732-108">Requirements</span></span>  

 <span data-ttu-id="6d732-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6d732-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d732-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6d732-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6d732-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6d732-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6d732-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6d732-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
