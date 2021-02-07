---
description: 了解详细信息： ICorDebugAssembly：： GetProcess 方法
title: ICorDebugAssembly::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::GetProcess
helpviewer_keywords:
- ICorDebugAssembly::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: ea52be06-0a16-4f57-afca-4287d72e76c4
topic_type:
- apiref
ms.openlocfilehash: b121d7f892f6e2e2aa76290d4aee51767c72e9fc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754142"
---
# <a name="icordebugassemblygetprocess-method"></a><span data-ttu-id="96cad-103">ICorDebugAssembly::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="96cad-103">ICorDebugAssembly::GetProcess Method</span></span>

<span data-ttu-id="96cad-104">获取一个接口指针，该指针指向运行此 ICorDebugAssembly 实例的进程。</span><span class="sxs-lookup"><span data-stu-id="96cad-104">Gets an interface pointer to the process in which this ICorDebugAssembly instance is running.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96cad-105">语法</span><span class="sxs-lookup"><span data-stu-id="96cad-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [out] ICorDebugProcess **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="96cad-106">参数</span><span class="sxs-lookup"><span data-stu-id="96cad-106">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="96cad-107">弄指向表示进程的 ICorDebugProcess 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="96cad-107">[out] A pointer to an ICorDebugProcess interface that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96cad-108">要求</span><span class="sxs-lookup"><span data-stu-id="96cad-108">Requirements</span></span>  

 <span data-ttu-id="96cad-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="96cad-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96cad-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="96cad-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="96cad-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="96cad-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="96cad-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96cad-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
