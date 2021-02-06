---
description: 了解详细信息： ICorDebugRegisterSet：： SetThreadContext 方法
title: ICorDebugRegisterSet::SetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.SetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::SetThreadContext
helpviewer_keywords:
- ICorDebugRegisterSet::SetThreadContext method [.NET Framework debugging]
- SetThreadContext method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 73afa930-32cb-4c40-81f8-83e8e6fbe213
topic_type:
- apiref
ms.openlocfilehash: 8d874b1864e85e477260632ad6012dbbf10aefb2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637685"
---
# <a name="icordebugregistersetsetthreadcontext-method"></a><span data-ttu-id="49707-103">ICorDebugRegisterSet::SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="49707-103">ICorDebugRegisterSet::SetThreadContext Method</span></span>

<span data-ttu-id="49707-104">`SetThreadContext` 在 .NET Framework 版本2.0 中未实现。</span><span class="sxs-lookup"><span data-stu-id="49707-104">`SetThreadContext` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="49707-105">请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="49707-105">Do not call this method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="49707-106">使用较高级别的操作 [ICorDebugNativeFrame：： SetIP](icordebugnativeframe-setip-method.md) 设置线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="49707-106">Use the higher-level operation [ICorDebugNativeFrame::SetIP](icordebugnativeframe-setip-method.md) to set the context of a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49707-107">语法</span><span class="sxs-lookup"><span data-stu-id="49707-107">Syntax</span></span>  
  
```cpp  
HRESULT SetThreadContext (  
    [in] ULONG32 contextSize,  
    [in, length_is(contextSize),  
         size_is(contextSize)] BYTE context[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="49707-108">要求</span><span class="sxs-lookup"><span data-stu-id="49707-108">Requirements</span></span>  

 <span data-ttu-id="49707-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49707-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49707-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="49707-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="49707-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="49707-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="49707-112">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="49707-112">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49707-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="49707-113">See also</span></span>

- [<span data-ttu-id="49707-114">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="49707-114">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
- [<span data-ttu-id="49707-115">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="49707-115">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
