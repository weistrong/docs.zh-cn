---
description: 了解详细信息： ICorDebugILFrame：： CanSetIP 方法
title: ICorDebugILFrame::CanSetIP 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.CanSetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::CanSetIP
helpviewer_keywords:
- CanSetIP method, ICorDebugILFrame interface [.NET Framework debugging]
- ICorDebugILFrame::CanSetIP method [.NET Framework debugging]
ms.assetid: 16caf02f-c71e-486c-90b0-f0e54357d8f0
topic_type:
- apiref
ms.openlocfilehash: d6ba0d073e8807ac6173f7f3e3982fe1d3eb4e01
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791434"
---
# <a name="icordebugilframecansetip-method"></a><span data-ttu-id="20286-103">ICorDebugILFrame::CanSetIP 方法</span><span class="sxs-lookup"><span data-stu-id="20286-103">ICorDebugILFrame::CanSetIP Method</span></span>

<span data-ttu-id="20286-104">获取 HRESULT，它指示是否可以安全地将指令指针设置为 Microsoft 中间语言 (MSIL) 代码中的指定偏移位置。</span><span class="sxs-lookup"><span data-stu-id="20286-104">Gets an HRESULT that indicates whether it is safe to set the instruction pointer to the specified offset location in Microsoft Intermediate Language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20286-105">语法</span><span class="sxs-lookup"><span data-stu-id="20286-105">Syntax</span></span>  
  
```cpp  
HRESULT CanSetIP (  
    [in] ULONG32   nOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="20286-106">参数</span><span class="sxs-lookup"><span data-stu-id="20286-106">Parameters</span></span>  

 `nOffset`  
 <span data-ttu-id="20286-107">中指令指针所需的设置。</span><span class="sxs-lookup"><span data-stu-id="20286-107">[in] The desired setting for the instruction pointer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="20286-108">备注</span><span class="sxs-lookup"><span data-stu-id="20286-108">Remarks</span></span>  

 <span data-ttu-id="20286-109">在 `CanSetIP` 调用 [ICorDebugILFrame：： SetIP](icordebugilframe-setip-method.md) 方法之前，请使用方法。</span><span class="sxs-lookup"><span data-stu-id="20286-109">Use the `CanSetIP` method before calling the [ICorDebugILFrame::SetIP](icordebugilframe-setip-method.md) method.</span></span> <span data-ttu-id="20286-110">如果 `CanSetIP` 返回除 S_OK 以外的任何 HRESULT，则仍可调用 `ICorDebugILFrame::SetIP` ，但是无法保证调试器将继续安全且正确地执行正在调试的代码。</span><span class="sxs-lookup"><span data-stu-id="20286-110">If `CanSetIP` returns any HRESULT other than S_OK, you can still invoke `ICorDebugILFrame::SetIP`, but there is no guarantee that the debugger will continue the safe and correct execution of the code being debugged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20286-111">要求</span><span class="sxs-lookup"><span data-stu-id="20286-111">Requirements</span></span>  

 <span data-ttu-id="20286-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20286-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20286-113">**标头：** Cordebug.idl、Cordebug.idl、h</span><span class="sxs-lookup"><span data-stu-id="20286-113">**Header:** CorDebug.idl, CorDebug,h</span></span>  
  
 <span data-ttu-id="20286-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="20286-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="20286-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20286-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
