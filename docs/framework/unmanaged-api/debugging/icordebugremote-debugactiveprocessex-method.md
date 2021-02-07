---
description: 了解详细信息： ICorDebugRemote：:D ebugActiveProcessEx 方法
title: ICorDebugRemote::DebugActiveProcessEx 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRemote.DebugActiveProcessEx
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget::DebugActiveProcessEx
helpviewer_keywords:
- ICorDebugRemote::DebugActiveProcessEx method [.NET Framework debugging]
- DebugActiveProcessEx method, ICorDebugRemote interface [.NET Framework debugging]
ms.assetid: b0df5c5d-9a2e-47bf-894c-6f8a9fe24a1f
topic_type:
- apiref
ms.openlocfilehash: ccbde152e59146bd852a5a0a2f991d10333fa9d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717896"
---
# <a name="icordebugremotedebugactiveprocessex-method"></a><span data-ttu-id="d60d2-103">ICorDebugRemote::DebugActiveProcessEx 方法</span><span class="sxs-lookup"><span data-stu-id="d60d2-103">ICorDebugRemote::DebugActiveProcessEx Method</span></span>

<span data-ttu-id="d60d2-104">在调试器下的远程计算机上启动进程。</span><span class="sxs-lookup"><span data-stu-id="d60d2-104">Launches a process on a remote machine under the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d60d2-105">语法</span><span class="sxs-lookup"><span data-stu-id="d60d2-105">Syntax</span></span>  
  
```cpp  
HRESULT DebugActiveProcessEx (  
    [in]  ICorDebugRemoteTarget *   pRemoteTarget,  
    [in]  DWORD                     dwProcessId,  
    [in]  BOOL                      fWin32Attach,  
    [out] ICorDebugProcess **       ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d60d2-106">参数</span><span class="sxs-lookup"><span data-stu-id="d60d2-106">Parameters</span></span>  

 `pRemoteTarget`  
 <span data-ttu-id="d60d2-107">中指向 [ICorDebugRemoteTarget 接口](icordebugremotetarget-interface.md)的指针。</span><span class="sxs-lookup"><span data-stu-id="d60d2-107">[in] Pointer to an [ICorDebugRemoteTarget Interface](icordebugremotetarget-interface.md).</span></span> <span data-ttu-id="d60d2-108">此参数用于确定正在运行进程的计算机。</span><span class="sxs-lookup"><span data-stu-id="d60d2-108">This parameter is used to determine the machine on which the process is running.</span></span>  
  
 `id`  
 <span data-ttu-id="d60d2-109">中调试器要附加到的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="d60d2-109">[in] The ID of the process to which the debugger is to be attached.</span></span>  
  
 `win32Attach`  
 <span data-ttu-id="d60d2-110">[in] `true` 如果调试器应该表现为进程的 Win32 调试器并调度非托管回调，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="d60d2-110">[in] `true` if the debugger should behave as the Win32 debugger for the process and dispatch the unmanaged callbacks; otherwise, `false`.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="d60d2-111">弄一个指向 "ICorDebugProcess" 对象地址的指针，该对象表示调试器已附加到的进程。</span><span class="sxs-lookup"><span data-stu-id="d60d2-111">[out] A pointer to the address of an "ICorDebugProcess" object that represents the process to which the debugger has been attached.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d60d2-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d60d2-112">Return Value</span></span>  

 <span data-ttu-id="d60d2-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d60d2-113">S_OK</span></span>  
 <span data-ttu-id="d60d2-114">已成功附加到远程计算机上的进程。</span><span class="sxs-lookup"><span data-stu-id="d60d2-114">Successfully attached to the process on the remote machine.</span></span>  
  
 <span data-ttu-id="d60d2-115">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="d60d2-115">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="d60d2-116">无法附加到远程计算机上的进程。</span><span class="sxs-lookup"><span data-stu-id="d60d2-116">Unable to attach to the process on the remote machine.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d60d2-117">备注</span><span class="sxs-lookup"><span data-stu-id="d60d2-117">Remarks</span></span>  

 <span data-ttu-id="d60d2-118">Silverlight 中不支持混合模式调试。</span><span class="sxs-lookup"><span data-stu-id="d60d2-118">Mixed-mode debugging is not supported in Silverlight.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d60d2-119">要求</span><span class="sxs-lookup"><span data-stu-id="d60d2-119">Requirements</span></span>  

 <span data-ttu-id="d60d2-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d60d2-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d60d2-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d60d2-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d60d2-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d60d2-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d60d2-123">**.NET Framework 版本：** 4.5、4、3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="d60d2-123">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d60d2-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="d60d2-124">See also</span></span>

- [<span data-ttu-id="d60d2-125">ICorDebugRemote 接口</span><span class="sxs-lookup"><span data-stu-id="d60d2-125">ICorDebugRemote Interface</span></span>](icordebugremote-interface.md)
- [<span data-ttu-id="d60d2-126">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="d60d2-126">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="d60d2-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="d60d2-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
