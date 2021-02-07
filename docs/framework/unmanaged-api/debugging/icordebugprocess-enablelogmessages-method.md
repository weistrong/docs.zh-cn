---
description: 了解详细信息： ICorDebugProcess：： EnableLogMessages 方法
title: ICorDebugProcess::EnableLogMessages 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.EnableLogMessages
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::EnableLogMessages
helpviewer_keywords:
- ICorDebugProcess::EnableLogMessages method [.NET Framework debugging]
- EnableLogMessages method [.NET Framework debugging]
ms.assetid: 14a4e5a3-3eaf-4f53-9dd1-762726963a23
topic_type:
- apiref
ms.openlocfilehash: d44f1a14611493372c7321feaa14329d5d77b01b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753986"
---
# <a name="icordebugprocessenablelogmessages-method"></a><span data-ttu-id="8a52e-103">ICorDebugProcess::EnableLogMessages 方法</span><span class="sxs-lookup"><span data-stu-id="8a52e-103">ICorDebugProcess::EnableLogMessages Method</span></span>

<span data-ttu-id="8a52e-104">启用和禁用向调试器传输日志消息。</span><span class="sxs-lookup"><span data-stu-id="8a52e-104">Enables and disables the transmission of log messages to the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a52e-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a52e-105">Syntax</span></span>  
  
```cpp  
HRESULT EnableLogMessages([in]BOOL fOnOff);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a52e-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a52e-106">Parameters</span></span>  

 `fOnOff`  
 <span data-ttu-id="8a52e-107">[in] `true` 启用日志消息的传输; `false` 禁用传输。</span><span class="sxs-lookup"><span data-stu-id="8a52e-107">[in] `true` enables the transmission of log messages; `false` disables the transmission.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8a52e-108">备注</span><span class="sxs-lookup"><span data-stu-id="8a52e-108">Remarks</span></span>  

 <span data-ttu-id="8a52e-109">此方法仅在 [ICorDebugManagedCallback：： CreateProcess](icordebugmanagedcallback-createprocess-method.md) 回调发生之后有效。</span><span class="sxs-lookup"><span data-stu-id="8a52e-109">This method is valid only after the [ICorDebugManagedCallback::CreateProcess](icordebugmanagedcallback-createprocess-method.md) callback occurs.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a52e-110">要求</span><span class="sxs-lookup"><span data-stu-id="8a52e-110">Requirements</span></span>  

 <span data-ttu-id="8a52e-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a52e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a52e-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8a52e-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8a52e-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a52e-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a52e-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a52e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
