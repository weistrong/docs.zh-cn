---
description: 了解详细信息： ICorDebugProcess：： GetThread 方法
title: ICorDebugProcess::GetThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetThread
helpviewer_keywords:
- ICorDebugProcess::GetThread method [.NET Framework debugging]
- GetThread method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: a48261ed-700b-41c9-8cb4-18c526546603
topic_type:
- apiref
ms.openlocfilehash: bd636df50afd3f12901c1b48559c44ac6ad0cb81
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746888"
---
# <a name="icordebugprocessgetthread-method"></a><span data-ttu-id="4bad0-103">ICorDebugProcess::GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="4bad0-103">ICorDebugProcess::GetThread Method</span></span>

<span data-ttu-id="4bad0-104">获取此进程的线程，该线程具有指定操作系统) 线程 ID (操作系统。</span><span class="sxs-lookup"><span data-stu-id="4bad0-104">Gets this process's thread that has the specified operating system (OS) thread ID.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bad0-105">语法</span><span class="sxs-lookup"><span data-stu-id="4bad0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThread(  
    [in] DWORD dwThreadId,  
    [out] ICorDebugThread **ppThread);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4bad0-106">参数</span><span class="sxs-lookup"><span data-stu-id="4bad0-106">Parameters</span></span>  

 `dwThreadId`  
 <span data-ttu-id="4bad0-107">中要检索的线程的 OS 线程 ID。</span><span class="sxs-lookup"><span data-stu-id="4bad0-107">[in] The OS thread ID of the thread to be retrieved.</span></span>  
  
 `ppThread`  
 <span data-ttu-id="4bad0-108">弄指向表示线程的 ICorDebugThread 对象的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="4bad0-108">[out] A pointer to the address of an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4bad0-109">要求</span><span class="sxs-lookup"><span data-stu-id="4bad0-109">Requirements</span></span>  

 <span data-ttu-id="4bad0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4bad0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4bad0-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4bad0-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4bad0-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4bad0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4bad0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4bad0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
