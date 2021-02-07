---
description: 了解详细信息： ICorDebugModule：： GetProcess 方法
title: ICorDebugModule::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetProcess method [.NET Framework debugging]
ms.assetid: 5e13446c-0271-446c-924a-9072c0e6eeae
topic_type:
- apiref
ms.openlocfilehash: eb8497ac8ec6913fe079d6f5f148d3769bf6633a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691596"
---
# <a name="icordebugmodulegetprocess-method"></a><span data-ttu-id="7d0a7-103">ICorDebugModule::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="7d0a7-103">ICorDebugModule::GetProcess Method</span></span>

<span data-ttu-id="7d0a7-104">获取此模块的包含进程。</span><span class="sxs-lookup"><span data-stu-id="7d0a7-104">Gets the containing process of this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d0a7-105">语法</span><span class="sxs-lookup"><span data-stu-id="7d0a7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [out] ICorDebugProcess **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d0a7-106">参数</span><span class="sxs-lookup"><span data-stu-id="7d0a7-106">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="7d0a7-107">弄指向 ICorDebugProcess 对象的地址的指针，该对象表示包含此模块的进程。</span><span class="sxs-lookup"><span data-stu-id="7d0a7-107">[out] A pointer to the address of an ICorDebugProcess object that represents the process containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d0a7-108">要求</span><span class="sxs-lookup"><span data-stu-id="7d0a7-108">Requirements</span></span>  

 <span data-ttu-id="7d0a7-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7d0a7-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d0a7-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7d0a7-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7d0a7-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7d0a7-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7d0a7-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d0a7-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
