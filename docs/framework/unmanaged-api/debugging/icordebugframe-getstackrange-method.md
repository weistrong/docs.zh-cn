---
description: 了解详细信息： ICorDebugFrame：： GetStackRange 方法
title: ICorDebugFrame::GetStackRange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetStackRange
helpviewer_keywords:
- GetStackRange method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetStackRange method [.NET Framework debugging]
ms.assetid: fab037cb-fda6-40fb-9367-921e435dd5a0
topic_type:
- apiref
ms.openlocfilehash: 1f1278e0c00addc3c14f4e1c8d3ed5aad0381526
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692896"
---
# <a name="icordebugframegetstackrange-method"></a><span data-ttu-id="a75d6-103">ICorDebugFrame::GetStackRange 方法</span><span class="sxs-lookup"><span data-stu-id="a75d6-103">ICorDebugFrame::GetStackRange Method</span></span>

<span data-ttu-id="a75d6-104">获取此堆栈帧的绝对地址范围。</span><span class="sxs-lookup"><span data-stu-id="a75d6-104">Gets the absolute address range of this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a75d6-105">语法</span><span class="sxs-lookup"><span data-stu-id="a75d6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a75d6-106">参数</span><span class="sxs-lookup"><span data-stu-id="a75d6-106">Parameters</span></span>  

 `pStart`  
 <span data-ttu-id="a75d6-107">弄指向的指针 `CORDB_ADDRESS` ，它指定此对象表示的堆栈帧的起始地址 `ICorDebugFrame` 。</span><span class="sxs-lookup"><span data-stu-id="a75d6-107">[out] A pointer to a `CORDB_ADDRESS` that specifies the starting address of the stack frame represented by this `ICorDebugFrame` object.</span></span>  
  
 `pEnd`  
 <span data-ttu-id="a75d6-108">弄指向的指针 `CORDB_ADDRESS` ，它指定此对象表示的堆栈帧的结束地址 `ICorDebugFrame` 。</span><span class="sxs-lookup"><span data-stu-id="a75d6-108">[out] A pointer to a `CORDB_ADDRESS` that specifies the ending address of the stack frame represented by this `ICorDebugFrame` object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a75d6-109">备注</span><span class="sxs-lookup"><span data-stu-id="a75d6-109">Remarks</span></span>  

 <span data-ttu-id="a75d6-110">堆栈的地址范围可用于拼凑将从多个调试引擎中收集的交错堆栈跟踪组合在一起。</span><span class="sxs-lookup"><span data-stu-id="a75d6-110">The address range of the stack is useful for piecing together interleaved stack traces gathered from multiple debugging engines.</span></span> <span data-ttu-id="a75d6-111">数值范围不提供有关堆栈帧内容的信息。</span><span class="sxs-lookup"><span data-stu-id="a75d6-111">The numeric range provides no information about the contents of the stack frame.</span></span> <span data-ttu-id="a75d6-112">它仅用于比较堆栈帧位置。</span><span class="sxs-lookup"><span data-stu-id="a75d6-112">It is meaningful only for comparison of stack frame locations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a75d6-113">要求</span><span class="sxs-lookup"><span data-stu-id="a75d6-113">Requirements</span></span>  

 <span data-ttu-id="a75d6-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a75d6-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a75d6-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a75d6-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a75d6-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a75d6-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a75d6-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a75d6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
