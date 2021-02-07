---
description: 了解详细信息： ICorDebugProcess：： GetID 方法
title: ICorDebugProcess::GetID 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetID
helpviewer_keywords:
- GetID method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::GetID method [.NET Framework debugging]
ms.assetid: b0ba8453-fa7e-4c14-93e5-335409cd4a47
topic_type:
- apiref
ms.openlocfilehash: 806e73724a88d08235f4a3e751f771abace1ad56
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746979"
---
# <a name="icordebugprocessgetid-method"></a><span data-ttu-id="34de6-103">ICorDebugProcess::GetID 方法</span><span class="sxs-lookup"><span data-stu-id="34de6-103">ICorDebugProcess::GetID Method</span></span>

<span data-ttu-id="34de6-104">获取进程的操作系统 (操作系统) ID。</span><span class="sxs-lookup"><span data-stu-id="34de6-104">Gets the operating system (OS) ID of the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34de6-105">语法</span><span class="sxs-lookup"><span data-stu-id="34de6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetID([out] DWORD *pdwProcessId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="34de6-106">参数</span><span class="sxs-lookup"><span data-stu-id="34de6-106">Parameters</span></span>  

 `pdwProcessId`  
 <span data-ttu-id="34de6-107">弄进程的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="34de6-107">[out] The unique ID of the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34de6-108">要求</span><span class="sxs-lookup"><span data-stu-id="34de6-108">Requirements</span></span>  

 <span data-ttu-id="34de6-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="34de6-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34de6-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="34de6-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="34de6-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="34de6-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="34de6-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34de6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
