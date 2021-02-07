---
description: 了解详细信息： ICorDebugChain：： GetStackRange 方法
title: ICorDebugChain::GetStackRange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetStackRange
helpviewer_keywords:
- ICorDebugChain::GetStackRange method [.NET Framework debugging]
- GetStackRange method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 554284e7-3f6c-4d40-8da5-1c9317fbd484
topic_type:
- apiref
ms.openlocfilehash: 066dda06564655350d799dabb54acd622b828172
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694918"
---
# <a name="icordebugchaingetstackrange-method"></a><span data-ttu-id="3ba2e-103">ICorDebugChain::GetStackRange 方法</span><span class="sxs-lookup"><span data-stu-id="3ba2e-103">ICorDebugChain::GetStackRange Method</span></span>

<span data-ttu-id="3ba2e-104">获取此链的堆栈段的地址范围。</span><span class="sxs-lookup"><span data-stu-id="3ba2e-104">Gets the address range of the stack segment for this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ba2e-105">语法</span><span class="sxs-lookup"><span data-stu-id="3ba2e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3ba2e-106">参数</span><span class="sxs-lookup"><span data-stu-id="3ba2e-106">Parameters</span></span>  

 `pStart`  
 <span data-ttu-id="3ba2e-107">弄一个指针，指向作为 `CORDB_ADDRESS` 堆栈段起始地址的值。</span><span class="sxs-lookup"><span data-stu-id="3ba2e-107">[out] A pointer to a `CORDB_ADDRESS` value that is the starting address of the stack segment.</span></span>  
  
 `pEnd`  
 <span data-ttu-id="3ba2e-108">弄一个指针，指向作为 `CORDB_ADDRESS` 堆栈段结束地址的值。</span><span class="sxs-lookup"><span data-stu-id="3ba2e-108">[out] A pointer to a `CORDB_ADDRESS` value that is the ending address of the stack segment.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3ba2e-109">备注</span><span class="sxs-lookup"><span data-stu-id="3ba2e-109">Remarks</span></span>  

 <span data-ttu-id="3ba2e-110">数值范围仅用于比较堆栈帧位置。</span><span class="sxs-lookup"><span data-stu-id="3ba2e-110">The numeric range is meaningful only for comparison of stack frame locations.</span></span> <span data-ttu-id="3ba2e-111">您无法对堆栈上实际存储的内容作出任何假设。</span><span class="sxs-lookup"><span data-stu-id="3ba2e-111">You cannot make any assumptions about what is actually stored on the stack.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ba2e-112">要求</span><span class="sxs-lookup"><span data-stu-id="3ba2e-112">Requirements</span></span>  

 <span data-ttu-id="3ba2e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3ba2e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3ba2e-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3ba2e-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3ba2e-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3ba2e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3ba2e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ba2e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
