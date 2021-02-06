---
description: 了解详细信息： ICorDebugNativeFrame：： GetIP 方法
title: ICorDebugNativeFrame::GetIP 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetIP
helpviewer_keywords:
- GetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
- ICorDebugNativeFrame::GetIP method [.NET Framework debugging]
ms.assetid: 99f693f3-d3b9-4fd8-9d09-b8efd03f7b67
topic_type:
- apiref
ms.openlocfilehash: f36a14c38aa6c3754cf78eca8c657adc76469067
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637828"
---
# <a name="icordebugnativeframegetip-method"></a><span data-ttu-id="7f042-103">ICorDebugNativeFrame::GetIP 方法</span><span class="sxs-lookup"><span data-stu-id="7f042-103">ICorDebugNativeFrame::GetIP Method</span></span>

<span data-ttu-id="7f042-104">获取指令指针当前所设置到的本机代码偏移位置。</span><span class="sxs-lookup"><span data-stu-id="7f042-104">Gets the native code offset location to which the instruction pointer is currently set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f042-105">语法</span><span class="sxs-lookup"><span data-stu-id="7f042-105">Syntax</span></span>  
  
```cpp  
HRESULT GetIP (  
    [out] ULONG32           *pnOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f042-106">参数</span><span class="sxs-lookup"><span data-stu-id="7f042-106">Parameters</span></span>  

 `pnOffset`  
 <span data-ttu-id="7f042-107">弄指向本机代码中的偏移位置的指针。</span><span class="sxs-lookup"><span data-stu-id="7f042-107">[out] A pointer to the offset location in the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7f042-108">备注</span><span class="sxs-lookup"><span data-stu-id="7f042-108">Remarks</span></span>  

 <span data-ttu-id="7f042-109">如果此 "ICorDebugNativeFrame" 表示的堆栈帧处于活动状态，则偏移量是要执行的下一条指令的地址。</span><span class="sxs-lookup"><span data-stu-id="7f042-109">If the stack frame that is represented by this "ICorDebugNativeFrame" is active, the offset is the address of the next instruction to be executed.</span></span> <span data-ttu-id="7f042-110">如果此堆栈帧不处于活动状态，则偏移量是在重新激活堆栈帧时要执行的下一条指令的地址。</span><span class="sxs-lookup"><span data-stu-id="7f042-110">If this stack frame is not active, the offset is the address of the next instruction to be executed when the stack frame is reactivated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f042-111">要求</span><span class="sxs-lookup"><span data-stu-id="7f042-111">Requirements</span></span>  

 <span data-ttu-id="7f042-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f042-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f042-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7f042-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7f042-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7f042-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7f042-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f042-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f042-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f042-116">See also</span></span>
