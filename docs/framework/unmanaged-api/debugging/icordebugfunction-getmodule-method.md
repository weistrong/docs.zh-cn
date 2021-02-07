---
description: 了解详细信息： ICorDebugFunction：： GetModule 方法
title: ICorDebugFunction::GetModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetModule
helpviewer_keywords:
- ICorDebugFunction::GetModule method [.NET Framework debugging]
- GetModule method, ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: 5031a5d3-2564-412a-9007-e36d4631308a
topic_type:
- apiref
ms.openlocfilehash: 62087cdf0443b2ef495461aab74cfa047b95efca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692454"
---
# <a name="icordebugfunctiongetmodule-method"></a><span data-ttu-id="56f3e-103">ICorDebugFunction::GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="56f3e-103">ICorDebugFunction::GetModule Method</span></span>

<span data-ttu-id="56f3e-104">获取在其中定义此函数的模块。</span><span class="sxs-lookup"><span data-stu-id="56f3e-104">Gets the module in which this function is defined.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56f3e-105">语法</span><span class="sxs-lookup"><span data-stu-id="56f3e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModule (  
    [out] ICorDebugModule **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="56f3e-106">参数</span><span class="sxs-lookup"><span data-stu-id="56f3e-106">Parameters</span></span>  

 `ppModule`  
 <span data-ttu-id="56f3e-107">弄指向 ICorDebugModule 对象的地址的指针，该对象表示在其中定义此函数的模块。</span><span class="sxs-lookup"><span data-stu-id="56f3e-107">[out] A pointer to the address of an ICorDebugModule object that represents the module in which this function is defined.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56f3e-108">要求</span><span class="sxs-lookup"><span data-stu-id="56f3e-108">Requirements</span></span>  

 <span data-ttu-id="56f3e-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="56f3e-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56f3e-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="56f3e-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="56f3e-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="56f3e-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="56f3e-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56f3e-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
