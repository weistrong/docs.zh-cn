---
description: 了解详细信息： ICorDebugProcess：： EnumerateAppDomains 方法
title: ICorDebugProcess::EnumerateAppDomains 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.EnumerateAppDomains
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::EnumerateAppDomains
helpviewer_keywords:
- ICorDebugProcess::EnumerateAppDomains method [.NET Framework debugging]
- EnumerateAppDomains method [.NET Framework debugging]
ms.assetid: d508981f-e2b2-445b-a649-69951c22702d
topic_type:
- apiref
ms.openlocfilehash: d212fafe7ae1355ba69e07b88c3b96119371fe43
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691518"
---
# <a name="icordebugprocessenumerateappdomains-method"></a><span data-ttu-id="3fbb4-103">ICorDebugProcess::EnumerateAppDomains 方法</span><span class="sxs-lookup"><span data-stu-id="3fbb4-103">ICorDebugProcess::EnumerateAppDomains Method</span></span>

<span data-ttu-id="3fbb4-104">枚举此进程中的所有应用程序域。</span><span class="sxs-lookup"><span data-stu-id="3fbb4-104">Enumerates all the application domains in this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fbb4-105">语法</span><span class="sxs-lookup"><span data-stu-id="3fbb4-105">Syntax</span></span>  
  
``` cpp
HRESULT EnumerateAppDomains(  
    [out] ICorDebugAppDomainEnum **ppAppDomains);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3fbb4-106">参数</span><span class="sxs-lookup"><span data-stu-id="3fbb4-106">Parameters</span></span>  

 `ppAppDomains`  
 <span data-ttu-id="3fbb4-107">弄一个指针，指向 [ICorDebugAppDomainEnum](icordebugappdomainenum-interface.md) 的地址，该地址是此进程中的应用程序域的枚举器。</span><span class="sxs-lookup"><span data-stu-id="3fbb4-107">[out] A pointer to the address of an [ICorDebugAppDomainEnum](icordebugappdomainenum-interface.md) that is an enumerator for the application domains in this process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3fbb4-108">备注</span><span class="sxs-lookup"><span data-stu-id="3fbb4-108">Remarks</span></span>  

 <span data-ttu-id="3fbb4-109">此方法可在 [ICorDebugManagedCallback：： CreateProcess](icordebugmanagedcallback-createprocess-method.md) 回调之前使用。</span><span class="sxs-lookup"><span data-stu-id="3fbb4-109">This method can be used before the [ICorDebugManagedCallback::CreateProcess](icordebugmanagedcallback-createprocess-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fbb4-110">要求</span><span class="sxs-lookup"><span data-stu-id="3fbb4-110">Requirements</span></span>  

 <span data-ttu-id="3fbb4-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3fbb4-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fbb4-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3fbb4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3fbb4-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3fbb4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3fbb4-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fbb4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
