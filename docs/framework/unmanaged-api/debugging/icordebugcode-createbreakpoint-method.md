---
description: 了解详细信息： ICorDebugCode：： CreateBreakpoint 方法
title: ICorDebugCode::CreateBreakpoint 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.CreateBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::CreateBreakpoint
helpviewer_keywords:
- ICorDebugCode::CreateBreakpoint method [.NET Framework debugging]
- CreateBreakpoint method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 46842618-0fe4-480b-871c-82fba82d23d9
topic_type:
- apiref
ms.openlocfilehash: a9285d59da3e3f34ea303413fca67bc39aff9e32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711370"
---
# <a name="icordebugcodecreatebreakpoint-method"></a><span data-ttu-id="d2a2f-103">ICorDebugCode::CreateBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="d2a2f-103">ICorDebugCode::CreateBreakpoint Method</span></span>

<span data-ttu-id="d2a2f-104">在此代码段中的指定偏移量处创建断点。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-104">Creates a breakpoint in this code segment at the specified offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2a2f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2a2f-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateBreakpoint (  
    [in] ULONG32     offset,  
    [out] ICorDebugFunctionBreakpoint **ppBreakpoint  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2a2f-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2a2f-106">Parameters</span></span>  

 `offset`  
 <span data-ttu-id="d2a2f-107">中创建断点的偏移量。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-107">[in] The offset at which to create the breakpoint.</span></span>  
  
 `ppBreakpoint`  
 <span data-ttu-id="d2a2f-108">弄指向表示断点的 "ICorDebugFunctionBreakpoint" 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-108">[out] A pointer to the address of an "ICorDebugFunctionBreakpoint" object that represents the breakpoint.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d2a2f-109">备注</span><span class="sxs-lookup"><span data-stu-id="d2a2f-109">Remarks</span></span>  

 <span data-ttu-id="d2a2f-110">在断点处于活动状态之前，必须将其添加到进程对象。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-110">Before the breakpoint is active, it must be added to the process object.</span></span>  
  
 <span data-ttu-id="d2a2f-111">如果此代码为 Microsoft 中间语言 (MSIL) 代码，并且存在 (JIT) 编译的本机版本代码，则将在 JIT 编译的代码中应用该断点。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-111">If this code is Microsoft intermediate language (MSIL) code, and there is a just-in-time (JIT)-compiled, native version of the code, the breakpoint will be applied in the JIT-compiled code as well.</span></span> <span data-ttu-id="d2a2f-112">如果稍后对代码进行 JIT 编译，则 (相同。 ) </span><span class="sxs-lookup"><span data-stu-id="d2a2f-112">(The same is true if the code is JIT-compiled later.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2a2f-113">要求</span><span class="sxs-lookup"><span data-stu-id="d2a2f-113">Requirements</span></span>  

 <span data-ttu-id="d2a2f-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a2f-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2a2f-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d2a2f-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d2a2f-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2a2f-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2a2f-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2a2f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
