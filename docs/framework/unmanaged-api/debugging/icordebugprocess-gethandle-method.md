---
description: 了解详细信息： ICorDebugProcess：： GetHandle 方法
title: ICorDebugProcess::GetHandle 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetHandle
helpviewer_keywords:
- GetHandle method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::GetHandle method [.NET Framework debugging]
ms.assetid: e7d3ecf5-09d2-4d94-abb6-ff3483deebb6
topic_type:
- apiref
ms.openlocfilehash: fbc92be53b30d3c70f85fea36e05c6a5514b0f03
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722115"
---
# <a name="icordebugprocessgethandle-method"></a><span data-ttu-id="63b3e-103">ICorDebugProcess::GetHandle 方法</span><span class="sxs-lookup"><span data-stu-id="63b3e-103">ICorDebugProcess::GetHandle Method</span></span>

<span data-ttu-id="63b3e-104">获取进程的句柄。</span><span class="sxs-lookup"><span data-stu-id="63b3e-104">Gets a handle to the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63b3e-105">语法</span><span class="sxs-lookup"><span data-stu-id="63b3e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHandle([out] HPROCESS *phProcessHandle);  
```  
  
## <a name="parameters"></a><span data-ttu-id="63b3e-106">参数</span><span class="sxs-lookup"><span data-stu-id="63b3e-106">Parameters</span></span>  

 `phProcessHandle`  
 <span data-ttu-id="63b3e-107">弄指向 `HPROCESS` 的指针，它是进程的句柄。</span><span class="sxs-lookup"><span data-stu-id="63b3e-107">[out] A pointer to an `HPROCESS` that is the handle to the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63b3e-108">备注</span><span class="sxs-lookup"><span data-stu-id="63b3e-108">Remarks</span></span>  

 <span data-ttu-id="63b3e-109">检索的句柄由调试接口拥有。</span><span class="sxs-lookup"><span data-stu-id="63b3e-109">The retrieved handle is owned by the debugging interface.</span></span> <span data-ttu-id="63b3e-110">调试器应在使用之前复制句柄。</span><span class="sxs-lookup"><span data-stu-id="63b3e-110">The debugger should duplicate the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63b3e-111">要求</span><span class="sxs-lookup"><span data-stu-id="63b3e-111">Requirements</span></span>  

 <span data-ttu-id="63b3e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="63b3e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63b3e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="63b3e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="63b3e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63b3e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63b3e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63b3e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
