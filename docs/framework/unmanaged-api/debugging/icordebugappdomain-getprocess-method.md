---
description: 了解详细信息： ICorDebugAppDomain：： GetProcess 方法
title: ICorDebugAppDomain::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebugAppDomain interface [.NET Framework debugging]
- ICorDebugAppDomain::GetProcess method [.NET Framework debugging]
ms.assetid: 9d0b9628-a91c-40d0-b9bc-00b34a396b8f
topic_type:
- apiref
ms.openlocfilehash: a681e58334df5dd7373e49b70c096fa1ff10773f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772401"
---
# <a name="icordebugappdomaingetprocess-method"></a><span data-ttu-id="1dffa-103">ICorDebugAppDomain::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="1dffa-103">ICorDebugAppDomain::GetProcess Method</span></span>

<span data-ttu-id="1dffa-104">获取包含应用程序域的进程。</span><span class="sxs-lookup"><span data-stu-id="1dffa-104">Gets the process containing the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1dffa-105">语法</span><span class="sxs-lookup"><span data-stu-id="1dffa-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1dffa-106">参数</span><span class="sxs-lookup"><span data-stu-id="1dffa-106">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="1dffa-107">弄指向表示进程的 ICorDebugProcess 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="1dffa-107">[out] A pointer to the address of an ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1dffa-108">要求</span><span class="sxs-lookup"><span data-stu-id="1dffa-108">Requirements</span></span>  

 <span data-ttu-id="1dffa-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1dffa-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1dffa-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1dffa-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1dffa-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1dffa-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1dffa-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1dffa-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
