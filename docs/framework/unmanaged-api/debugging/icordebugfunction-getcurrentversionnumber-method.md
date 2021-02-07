---
description: 了解详细信息： ICorDebugFunction：： GetCurrentVersionNumber 方法
title: ICorDebugFunction::GetCurrentVersionNumber 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetCurrentVersionNumber
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetCurrentVersionNumber
helpviewer_keywords:
- GetCurrentVersionNumber method [.NET Framework debugging]
- ICorDebugFunction::GetCurrentVersionNumber method [.NET Framework debugging]
ms.assetid: c3af1575-cbe6-457a-bc08-c53460edcbc8
topic_type:
- apiref
ms.openlocfilehash: ccc96755ac74624a00b806e3f569f39f2d6059f5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692532"
---
# <a name="icordebugfunctiongetcurrentversionnumber-method"></a><span data-ttu-id="42c0c-103">ICorDebugFunction::GetCurrentVersionNumber 方法</span><span class="sxs-lookup"><span data-stu-id="42c0c-103">ICorDebugFunction::GetCurrentVersionNumber Method</span></span>

<span data-ttu-id="42c0c-104">获取对此 ICorDebugFunction 对象所表示的函数进行的最新编辑的版本号。</span><span class="sxs-lookup"><span data-stu-id="42c0c-104">Gets the version number of the latest edit made to the function represented by this ICorDebugFunction object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42c0c-105">语法</span><span class="sxs-lookup"><span data-stu-id="42c0c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentVersionNumber (  
    [out] ULONG32 *pnCurrentVersion  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="42c0c-106">参数</span><span class="sxs-lookup"><span data-stu-id="42c0c-106">Parameters</span></span>  

 `pnCurrentVersion`  
 <span data-ttu-id="42c0c-107">弄指向整数值的指针，该整数值是对此函数进行的最新编辑的版本号。</span><span class="sxs-lookup"><span data-stu-id="42c0c-107">[out] A pointer to an integer value that is the version number of the latest edit made to this function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="42c0c-108">备注</span><span class="sxs-lookup"><span data-stu-id="42c0c-108">Remarks</span></span>  

 <span data-ttu-id="42c0c-109">对此函数进行的最新编辑的版本号可能大于函数本身的版本号。</span><span class="sxs-lookup"><span data-stu-id="42c0c-109">The version number of the latest edit made to this function may be greater than the version number of the function itself.</span></span> <span data-ttu-id="42c0c-110">使用 [ICorDebugFunction2：： GetVersionNumber](icordebugfunction2-getversionnumber-method.md) 方法或 [ICorDebugCode：： GetVersionNumber](icordebugcode-getversionnumber-method.md) 方法检索函数的版本号。</span><span class="sxs-lookup"><span data-stu-id="42c0c-110">Use either the [ICorDebugFunction2::GetVersionNumber](icordebugfunction2-getversionnumber-method.md) method or the [ICorDebugCode::GetVersionNumber](icordebugcode-getversionnumber-method.md) method to retrieve the version number of the function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="42c0c-111">要求</span><span class="sxs-lookup"><span data-stu-id="42c0c-111">Requirements</span></span>  

 <span data-ttu-id="42c0c-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42c0c-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42c0c-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="42c0c-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="42c0c-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="42c0c-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="42c0c-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42c0c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
