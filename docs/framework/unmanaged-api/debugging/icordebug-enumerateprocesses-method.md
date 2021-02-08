---
description: 了解详细信息： ICorDebug：： EnumerateProcesses 方法
title: ICorDebug::EnumerateProcesses 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.EnumerateProcesses
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- EnumerateProcesses
helpviewer_keywords:
- EnumerateProcesses method [.NET Framework debugging]
- ICorDebug::EnumerateProcesses method [.NET Framework debugging]
ms.assetid: ba25d166-1d28-4f1d-aca2-de298bbca669
topic_type:
- apiref
ms.openlocfilehash: 44ee21a820a1c9f94f1d66c93ff040b504bfcc93
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791577"
---
# <a name="icordebugenumerateprocesses-method"></a><span data-ttu-id="6f9aa-103">ICorDebug::EnumerateProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="6f9aa-103">ICorDebug::EnumerateProcesses Method</span></span>

<span data-ttu-id="6f9aa-104">获取正在调试的进程的枚举器。</span><span class="sxs-lookup"><span data-stu-id="6f9aa-104">Gets an enumerator for the processes that are being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f9aa-105">语法</span><span class="sxs-lookup"><span data-stu-id="6f9aa-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateProcesses (  
    [out] ICorDebugProcessEnum      **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6f9aa-106">参数</span><span class="sxs-lookup"><span data-stu-id="6f9aa-106">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="6f9aa-107">指向 ICorDebugProcessEnum 对象地址的指针，该对象是正在调试的进程的枚举器。</span><span class="sxs-lookup"><span data-stu-id="6f9aa-107">A pointer to the address of an ICorDebugProcessEnum object that is the enumerator for the processes being debugged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f9aa-108">要求</span><span class="sxs-lookup"><span data-stu-id="6f9aa-108">Requirements</span></span>  

 <span data-ttu-id="6f9aa-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6f9aa-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f9aa-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6f9aa-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6f9aa-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6f9aa-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6f9aa-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f9aa-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f9aa-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="6f9aa-113">See also</span></span>

- [<span data-ttu-id="6f9aa-114">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="6f9aa-114">ICorDebug Interface</span></span>](icordebug-interface.md)
