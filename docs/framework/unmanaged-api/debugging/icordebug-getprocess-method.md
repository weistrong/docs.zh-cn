---
description: 了解详细信息： ICorDebug：： GetProcess 方法
title: ICorDebug::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::GetProcess method [.NET Framework debugging]
ms.assetid: 10a40ba0-1b65-4721-bd11-cf12d57b280d
topic_type:
- apiref
ms.openlocfilehash: a24bb0ec645a337b1202b954c165a76bcf8fad9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801301"
---
# <a name="icordebuggetprocess-method"></a><span data-ttu-id="c8b7f-103">ICorDebug::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="c8b7f-103">ICorDebug::GetProcess Method</span></span>

<span data-ttu-id="c8b7f-104">获取指向指定进程的 "ICorDebugProcess" 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="c8b7f-104">Gets a pointer to the "ICorDebugProcess" instance for the specified process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8b7f-105">语法</span><span class="sxs-lookup"><span data-stu-id="c8b7f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [in] DWORD               dwProcessId,  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c8b7f-106">参数</span><span class="sxs-lookup"><span data-stu-id="c8b7f-106">Parameters</span></span>  

 `dwProcessId`  
 <span data-ttu-id="c8b7f-107">中进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="c8b7f-107">[in] The ID of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="c8b7f-108">弄指向指定进程的实例地址的指针 `ICorDebugProcess` 。</span><span class="sxs-lookup"><span data-stu-id="c8b7f-108">[out] A pointer to the address of a `ICorDebugProcess` instance for the specified process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8b7f-109">要求</span><span class="sxs-lookup"><span data-stu-id="c8b7f-109">Requirements</span></span>  

 <span data-ttu-id="c8b7f-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c8b7f-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8b7f-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c8b7f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c8b7f-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c8b7f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c8b7f-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8b7f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8b7f-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c8b7f-114">See also</span></span>

- [<span data-ttu-id="c8b7f-115">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="c8b7f-115">ICorDebug Interface</span></span>](icordebug-interface.md)
