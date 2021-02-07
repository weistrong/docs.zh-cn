---
description: 了解详细信息： ICorDebugProcess：： ModifyLogSwitch 方法
title: ICorDebugProcess::ModifyLogSwitch 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ModifyLogSwitch
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ModifyLogSwitch
helpviewer_keywords:
- ICorDebugProcess::ModifyLogSwitch method [.NET Framework debugging]
- ModifyLogSwitch method [.NET Framework debugging]
ms.assetid: 5fd30875-555e-4e96-877b-5dd266cde7c4
topic_type:
- apiref
ms.openlocfilehash: 3c825d6c6b075139793b54526dca696c8fba35a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746751"
---
# <a name="icordebugprocessmodifylogswitch-method"></a><span data-ttu-id="ec93e-103">ICorDebugProcess::ModifyLogSwitch 方法</span><span class="sxs-lookup"><span data-stu-id="ec93e-103">ICorDebugProcess::ModifyLogSwitch Method</span></span>

<span data-ttu-id="ec93e-104">设置指定的日志开关的严重性级别。</span><span class="sxs-lookup"><span data-stu-id="ec93e-104">Sets the severity level of the specified log switch.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec93e-105">语法</span><span class="sxs-lookup"><span data-stu-id="ec93e-105">Syntax</span></span>  
  
```cpp  
HRESULT ModifyLogSwitch(  
    [in] WCHAR *pLogSwitchName,  
    [in] LONG  lLevel);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec93e-106">参数</span><span class="sxs-lookup"><span data-stu-id="ec93e-106">Parameters</span></span>  

 `pLogSwitchName`  
 <span data-ttu-id="ec93e-107">中指向字符串的指针，该字符串指定日志开关的名称。</span><span class="sxs-lookup"><span data-stu-id="ec93e-107">[in] A pointer to a string that specifies the name of the log switch.</span></span>  
  
 `lLevel`  
 <span data-ttu-id="ec93e-108">中要为指定的日志开关设置的严重性级别。</span><span class="sxs-lookup"><span data-stu-id="ec93e-108">[in] The severity level to be set for the specified log switch.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec93e-109">备注</span><span class="sxs-lookup"><span data-stu-id="ec93e-109">Remarks</span></span>  

 <span data-ttu-id="ec93e-110">此方法仅在 [ICorDebugManagedCallback：： CreateProcess](icordebugmanagedcallback-createprocess-method.md) 回调发生之后有效。</span><span class="sxs-lookup"><span data-stu-id="ec93e-110">This method is valid only after the [ICorDebugManagedCallback::CreateProcess](icordebugmanagedcallback-createprocess-method.md) callback has occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec93e-111">要求</span><span class="sxs-lookup"><span data-stu-id="ec93e-111">Requirements</span></span>  

 <span data-ttu-id="ec93e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ec93e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec93e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ec93e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ec93e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ec93e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ec93e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec93e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
