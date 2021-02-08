---
description: 了解详细信息： ICorDebug：:D ebugActiveProcess 方法
title: ICorDebug::DebugActiveProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.DebugActiveProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::DebugActiveProcess
helpviewer_keywords:
- DebugActiveProcess method [.NET Framework debugging]
- ICorDebug::DebugActiveProcess method [.NET Framework debugging]
ms.assetid: fdab0ade-7f56-4fa2-b3ef-f7a1d2852bba
topic_type:
- apiref
ms.openlocfilehash: 9c3a212adf962f96fd2c7345fe8b580b6af3b544
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801314"
---
# <a name="icordebugdebugactiveprocess-method"></a><span data-ttu-id="22008-103">ICorDebug::DebugActiveProcess 方法</span><span class="sxs-lookup"><span data-stu-id="22008-103">ICorDebug::DebugActiveProcess Method</span></span>

<span data-ttu-id="22008-104">将调试器附加到现有进程。</span><span class="sxs-lookup"><span data-stu-id="22008-104">Attaches the debugger to an existing process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22008-105">语法</span><span class="sxs-lookup"><span data-stu-id="22008-105">Syntax</span></span>  
  
```cpp  
HRESULT DebugActiveProcess (  
    [in]  DWORD               id,  
    [in]  BOOL                win32Attach,  
    [out] ICorDebugProcess    **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22008-106">参数</span><span class="sxs-lookup"><span data-stu-id="22008-106">Parameters</span></span>  

 `id`  
 <span data-ttu-id="22008-107">中调试器要附加到的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="22008-107">[in] The ID of the process to which the debugger is to be attached.</span></span>  
  
 `win32Attach`  
 <span data-ttu-id="22008-108">中 `true` 如果调试器应该表现为进程的 Win32 调试器并调度非托管回调，则设置为的布尔值; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="22008-108">[in] Boolean value that is set to `true` if the debugger should behave as the Win32 debugger for the process and dispatch the unmanaged callbacks; otherwise, `false`.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="22008-109">弄一个指向 "ICorDebugProcess" 对象地址的指针，该对象表示调试器已附加到的进程。</span><span class="sxs-lookup"><span data-stu-id="22008-109">[out] A pointer to the address of an "ICorDebugProcess" object that represents the process to which the debugger has been attached.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="22008-110">备注</span><span class="sxs-lookup"><span data-stu-id="22008-110">Remarks</span></span>  

 <span data-ttu-id="22008-111">Win9x 和非 x86 平台都不支持互操作调试，如基于 IA-64 和基于 AMD64 的平台。</span><span class="sxs-lookup"><span data-stu-id="22008-111">Interop debugging is not supported on Win9x and non-x86 platforms, such as IA-64-based and AMD64-based platforms.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22008-112">要求</span><span class="sxs-lookup"><span data-stu-id="22008-112">Requirements</span></span>  

 <span data-ttu-id="22008-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22008-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22008-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="22008-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="22008-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22008-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22008-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22008-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22008-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="22008-117">See also</span></span>

- [<span data-ttu-id="22008-118">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="22008-118">ICorDebug Interface</span></span>](icordebug-interface.md)
