---
description: 了解详细信息： ICorDebug：： CreateProcess 方法
title: ICorDebug::CreateProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.CreateProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::CreateProcess
helpviewer_keywords:
- ICorDebug::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: b6128694-11ed-46e7-bd4e-49ea1914c46a
topic_type:
- apiref
ms.openlocfilehash: b504b5f7a60fd0fd4a8f8f1c5d8e3c3b8dcfd858
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712111"
---
# <a name="icordebugcreateprocess-method"></a><span data-ttu-id="b211f-103">ICorDebug::CreateProcess 方法</span><span class="sxs-lookup"><span data-stu-id="b211f-103">ICorDebug::CreateProcess Method</span></span>

<span data-ttu-id="b211f-104">在调试器的控制下启动进程及其主线程。</span><span class="sxs-lookup"><span data-stu-id="b211f-104">Launches a process and its primary thread under the control of the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b211f-105">语法</span><span class="sxs-lookup"><span data-stu-id="b211f-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateProcess (  
    [in]  LPCWSTR                     lpApplicationName,  
    [in]  LPWSTR                      lpCommandLine,  
    [in]  LPSECURITY_ATTRIBUTES       lpProcessAttributes,  
    [in]  LPSECURITY_ATTRIBUTES       lpThreadAttributes,  
    [in]  BOOL                        bInheritHandles,  
    [in]  DWORD                       dwCreationFlags,  
    [in]  PVOID                       lpEnvironment,  
    [in]  LPCWSTR                     lpCurrentDirectory,  
    [in]  LPSTARTUPINFOW              lpStartupInfo,  
    [in]  LPPROCESS_INFORMATION       lpProcessInformation,  
    [in]  CorDebugCreateProcessFlags  debuggingFlags,  
    [out] ICorDebugProcess            **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b211f-106">参数</span><span class="sxs-lookup"><span data-stu-id="b211f-106">Parameters</span></span>  

 `lpApplicationName`  
 <span data-ttu-id="b211f-107">中指向以 null 结尾的字符串的指针，该字符串指定由已启动的进程执行的模块。</span><span class="sxs-lookup"><span data-stu-id="b211f-107">[in] Pointer to a null-terminated string that specifies the module to be executed by the launched process.</span></span> <span data-ttu-id="b211f-108">该模块在调用进程的安全上下文中执行。</span><span class="sxs-lookup"><span data-stu-id="b211f-108">The module is executed in the security context of the calling process.</span></span>  
  
 `lpCommandLine`  
 <span data-ttu-id="b211f-109">中指向以 null 结尾的字符串的指针，该字符串指定由已启动的进程执行的命令行。</span><span class="sxs-lookup"><span data-stu-id="b211f-109">[in] Pointer to a null-terminated string that specifies the command line to be executed by the launched process.</span></span> <span data-ttu-id="b211f-110">应用程序名称 (例如，"SomeApp.exe" ) 必须是第一个参数。</span><span class="sxs-lookup"><span data-stu-id="b211f-110">The application name (for example, "SomeApp.exe") must be the first argument.</span></span>  
  
 `lpProcessAttributes`  
 <span data-ttu-id="b211f-111">中指向 Win32 `SECURITY_ATTRIBUTES` 结构的指针，该结构指定进程的安全说明符。</span><span class="sxs-lookup"><span data-stu-id="b211f-111">[in] Pointer to a Win32 `SECURITY_ATTRIBUTES` structure that specifies the security descriptor for the process.</span></span> <span data-ttu-id="b211f-112">如果 `lpProcessAttributes` 为 null，则进程将获取默认安全描述符。</span><span class="sxs-lookup"><span data-stu-id="b211f-112">If `lpProcessAttributes` is null, the process gets a default security descriptor.</span></span>  
  
 `lpThreadAttributes`  
 <span data-ttu-id="b211f-113">中指向 Win32 `SECURITY_ATTRIBUTES` 结构的指针，该结构指定进程的主线程的安全说明符。</span><span class="sxs-lookup"><span data-stu-id="b211f-113">[in] Pointer to a Win32 `SECURITY_ATTRIBUTES` structure that specifies the security descriptor for the primary thread of the process.</span></span> <span data-ttu-id="b211f-114">如果 `lpThreadAttributes` 为 null，则线程将获取默认安全描述符。</span><span class="sxs-lookup"><span data-stu-id="b211f-114">If `lpThreadAttributes` is null, the thread gets a default security descriptor.</span></span>  
  
 `bInheritHandles`  
 <span data-ttu-id="b211f-115">中如果设置为，则 `true` 指示调用进程中的每个可继承句柄由已启动的进程继承，或 `false` 指示不继承句柄。</span><span class="sxs-lookup"><span data-stu-id="b211f-115">[in] Set to `true` to indicate that each inheritable handle in the calling process is inherited by the launched process, or `false` to indicate that the handles are not inherited.</span></span> <span data-ttu-id="b211f-116">继承句柄与原始句柄具有相同的值和访问权限。</span><span class="sxs-lookup"><span data-stu-id="b211f-116">The inherited handles have the same value and access rights as the original handles.</span></span>  
  
 `dwCreationFlags`  
 <span data-ttu-id="b211f-117">中 [Win32 进程创建标志](/windows/win32/procthread/process-creation-flags) 的按位组合，用于控制优先级类和已启动进程的行为。</span><span class="sxs-lookup"><span data-stu-id="b211f-117">[in] A bitwise combination of the [Win32 Process Creation Flags](/windows/win32/procthread/process-creation-flags) that control the priority class and the behavior of the launched process.</span></span>  
  
 `lpEnvironment`  
 <span data-ttu-id="b211f-118">中指向新进程的环境块的指针。</span><span class="sxs-lookup"><span data-stu-id="b211f-118">[in] Pointer to an environment block for the new process.</span></span>  
  
 `lpCurrentDirectory`  
 <span data-ttu-id="b211f-119">中指向以 null 结尾的字符串的指针，该字符串指定进程的当前目录的完整路径。</span><span class="sxs-lookup"><span data-stu-id="b211f-119">[in] Pointer to a null-terminated string that specifies the full path to the current directory for the process.</span></span> <span data-ttu-id="b211f-120">如果此参数为 null，则新进程将与调用进程具有相同的当前驱动器和目录。</span><span class="sxs-lookup"><span data-stu-id="b211f-120">If this parameter is null, the new process will have the same current drive and directory as the calling process.</span></span>  
  
 `lpStartupInfo`  
 <span data-ttu-id="b211f-121">中指向 Win32 `STARTUPINFOW` 结构的指针，该结构指定窗口工作站、桌面、标准句柄和启动进程主窗口的外观。</span><span class="sxs-lookup"><span data-stu-id="b211f-121">[in] Pointer to a Win32 `STARTUPINFOW` structure that specifies the window station, desktop, standard handles, and appearance of the main window for the launched process.</span></span>  
  
 `lpProcessInformation`  
 <span data-ttu-id="b211f-122">中指向 Win32 `PROCESS_INFORMATION` 结构的指针，该结构指定有关要启动的进程的标识信息。</span><span class="sxs-lookup"><span data-stu-id="b211f-122">[in] Pointer to a Win32 `PROCESS_INFORMATION` structure that specifies the identification information about the process to be launched.</span></span>  
  
 `debuggingFlags`  
 <span data-ttu-id="b211f-123">中指定调试选项的 CorDebugCreateProcessFlags 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="b211f-123">[in] A value of the CorDebugCreateProcessFlags enumeration that specifies the debugging options.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="b211f-124">弄指向表示进程的 ICorDebugProcess 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="b211f-124">[out] A pointer to the address of a ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b211f-125">备注</span><span class="sxs-lookup"><span data-stu-id="b211f-125">Remarks</span></span>  

 <span data-ttu-id="b211f-126">此方法的参数与 Win32 方法的参数相同 `CreateProcess` 。</span><span class="sxs-lookup"><span data-stu-id="b211f-126">The parameters of this method are the same as those of the Win32 `CreateProcess` method.</span></span>  
  
 <span data-ttu-id="b211f-127">若要启用非托管混合模式调试，请将设置 `dwCreationFlags` 为 DEBUG_PROCESS &#124; DEBUG_ONLY_THIS_PROCESS。</span><span class="sxs-lookup"><span data-stu-id="b211f-127">To enable unmanaged mixed-mode debugging, set `dwCreationFlags` to DEBUG_PROCESS &#124; DEBUG_ONLY_THIS_PROCESS.</span></span> <span data-ttu-id="b211f-128">如果只想使用托管调试，请不要设置这些标志。</span><span class="sxs-lookup"><span data-stu-id="b211f-128">If you want to use only managed debugging, do not set these flags.</span></span>  
  
 <span data-ttu-id="b211f-129">如果调试器和要调试的进程 (附加的进程) 共享单个控制台，并且如果使用了互操作调试，则附加的进程可以保存控制台锁并在调试事件时停止。</span><span class="sxs-lookup"><span data-stu-id="b211f-129">If the debugger and the process to be debugged (the attached process) share a single console, and if interop debugging is used, it is possible for the attached process to hold console locks and stop at a debug event.</span></span> <span data-ttu-id="b211f-130">然后，调试器会阻止任何使用控制台的尝试。</span><span class="sxs-lookup"><span data-stu-id="b211f-130">The debugger will then block any attempt to use the console.</span></span> <span data-ttu-id="b211f-131">若要避免此问题，请在参数中设置 CREATE_NEW_CONSOLE 标志 `dwCreationFlags` 。</span><span class="sxs-lookup"><span data-stu-id="b211f-131">To avoid this problem, set the CREATE_NEW_CONSOLE flag in the `dwCreationFlags` parameter.</span></span>  
  
 <span data-ttu-id="b211f-132">Win9x 和非 x86 平台（如基于 IA-64 和 AMD64 的平台）不支持互操作调试。</span><span class="sxs-lookup"><span data-stu-id="b211f-132">Interop debugging is not supported on Win9x and non-x86 platforms such as IA-64-based and AMD64-based platforms.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b211f-133">要求</span><span class="sxs-lookup"><span data-stu-id="b211f-133">Requirements</span></span>  

 <span data-ttu-id="b211f-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b211f-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b211f-135">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b211f-135">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b211f-136">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b211f-136">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b211f-137">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b211f-137">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b211f-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="b211f-138">See also</span></span>

- [<span data-ttu-id="b211f-139">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="b211f-139">ICorDebug Interface</span></span>](icordebug-interface.md)
