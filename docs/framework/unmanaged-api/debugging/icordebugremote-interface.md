---
description: 了解详细信息： ICorDebugRemote 接口
title: ICorDebugRemote 接口
ms.date: 03/30/2017
api_name:
- ICorDebugRemote
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemote
helpviewer_keywords:
- ICorDebugRemote interface [.NET Framework debugging]
ms.assetid: 53d073c6-fa02-40d2-82e1-b9452bb6abaa
topic_type:
- apiref
ms.openlocfilehash: 4c9d92800c68155216a077180ea0b613c67423dd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790667"
---
# <a name="icordebugremote-interface"></a><span data-ttu-id="affe7-103">ICorDebugRemote 接口</span><span class="sxs-lookup"><span data-stu-id="affe7-103">ICorDebugRemote Interface</span></span>

<span data-ttu-id="affe7-104">提供启动托管调试器或将其附加到远程目标进程的能力。</span><span class="sxs-lookup"><span data-stu-id="affe7-104">Provides the ability to launch or attach a managed debugger to a remote target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="affe7-105">语法</span><span class="sxs-lookup"><span data-stu-id="affe7-105">Syntax</span></span>  
  
```cpp  
interface ICorDebugRemote : IUnknown  
{  
    HRESULT CreateProcessEx  
      (  
      [in] ICorDebugRemoteTarget *     pRemoteTarget,  
      [in] LPCWSTR                     lpApplicationName,  
      [in] LPWSTR                      lpCommandLine,  
      [in] LPSECURITY_ATTRIBUTES       lpProcessAttributes,  
      [in] LPSECURITY_ATTRIBUTES       lpThreadAttributes,  
      [in] BOOL                        bInheritHandles,  
      [in] DWORD                       dwCreationFlags,  
      [in] PVOID                       lpEnvironment,  
      [in] LPCWSTR                     lpCurrentDirectory,  
      [in] LPSTARTUPINFOW              lpStartupInfo,  
      [in] LPPROCESS_INFORMATION       lpProcessInformation,  
      [in] CorDebugCreateProcessFlags  debuggingFlags,  
      [out] ICorDebugProcess **        ppProcess  
      );  
  
    HRESULT DebugActiveProcessEx  
      (  
      [in] ICorDebugRemoteTarget *   pRemoteTarget,  
      [in] DWORD                     dwProcessId,  
      [in] BOOL                      fWin32Attach,  
      [out] ICorDebugProcess **      ppProcess  
      );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="affe7-106">方法</span><span class="sxs-lookup"><span data-stu-id="affe7-106">Methods</span></span>  
  
|<span data-ttu-id="affe7-107">方法</span><span class="sxs-lookup"><span data-stu-id="affe7-107">Method</span></span>|<span data-ttu-id="affe7-108">说明</span><span class="sxs-lookup"><span data-stu-id="affe7-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="affe7-109">ICorDebugRemote::CreateProcessEx 方法</span><span class="sxs-lookup"><span data-stu-id="affe7-109">ICorDebugRemote::CreateProcessEx Method</span></span>](icordebugremote-createprocessex-method.md)|<span data-ttu-id="affe7-110">在远程计算机上创建用于托管调试的进程。</span><span class="sxs-lookup"><span data-stu-id="affe7-110">Creates a process on a remote machine for managed debugging.</span></span>|  
|[<span data-ttu-id="affe7-111">ICorDebugRemote::DebugActiveProcessEx 方法</span><span class="sxs-lookup"><span data-stu-id="affe7-111">ICorDebugRemote::DebugActiveProcessEx Method</span></span>](icordebugremote-debugactiveprocessex-method.md)|<span data-ttu-id="affe7-112">在调试器下的远程计算机上启动进程。</span><span class="sxs-lookup"><span data-stu-id="affe7-112">Launches a process on a remote machine under the debugger.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="affe7-113">备注</span><span class="sxs-lookup"><span data-stu-id="affe7-113">Remarks</span></span>  

 <span data-ttu-id="affe7-114">目前，此功能仅用于调试在远程 Macintosh 计算机上运行的基于 Silverlight 的应用程序目标。</span><span class="sxs-lookup"><span data-stu-id="affe7-114">Currently, this functionality is supported only for debugging a Silverlight-based application target that is running on a remote Macintosh machine.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="affe7-115">要求</span><span class="sxs-lookup"><span data-stu-id="affe7-115">Requirements</span></span>  

 <span data-ttu-id="affe7-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="affe7-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="affe7-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="affe7-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="affe7-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="affe7-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="affe7-119">**.NET Framework 版本：** 4.5、4、3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="affe7-119">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="affe7-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="affe7-120">See also</span></span>

- [<span data-ttu-id="affe7-121">ICorDebugRemoteTarget 接口</span><span class="sxs-lookup"><span data-stu-id="affe7-121">ICorDebugRemoteTarget Interface</span></span>](icordebugremotetarget-interface.md)
- [<span data-ttu-id="affe7-122">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="affe7-122">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="affe7-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="affe7-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
