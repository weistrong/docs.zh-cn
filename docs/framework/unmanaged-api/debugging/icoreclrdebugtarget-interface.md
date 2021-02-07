---
description: 了解详细信息： ICoreClrDebugTarget 接口
title: ICoreClrDebugTarget 接口
ms.date: 03/30/2017
api_name:
- ICoreClrDebugTarget
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget
helpviewer_keywords:
- remote debugging API [Silverlight]
- ICorClrDebugTarget interface
- Silverlight, remote debugging
ms.assetid: 7cfaee76-e284-4a66-a431-8e33f0f60038
topic_type:
- apiref
ms.openlocfilehash: f0ed4dd75cd1daca6e83617433b29bbaecb1dd36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728751"
---
# <a name="icoreclrdebugtarget-interface"></a><span data-ttu-id="050ac-103">ICoreClrDebugTarget 接口</span><span class="sxs-lookup"><span data-stu-id="050ac-103">ICoreClrDebugTarget Interface</span></span>

<span data-ttu-id="050ac-104">提供一些方法，这些方法控制引用计数、枚举进程，并释放与附加到远程 Macintosh Silverlight 目标的调试器关联的内存。</span><span class="sxs-lookup"><span data-stu-id="050ac-104">Provides methods that control reference counts, enumerate processes, and free the memory associated with a debugger that is attached to a remote Macintosh Silverlight target.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="050ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="050ac-105">Syntax</span></span>  
  
```cpp  
class ICoreClrDebugTarget {  
      HRESULT EnumProcesses (  
          [out] DWORD*                    pcProcs,  
          [out] CoreClrDebugProcInfo**    ppProcs  
      );  
  
      HRESULT EnumRuntimes (  
      [in]  DWORD                      dwInternalProcessID,  
      [out] DWORD*                     pcRuntimes,  
      [out] CoreClrDebugRuntimeInfo**  ppRuntimes  
      );  
  
      void FreeMemory (  
      [in] void*      pMemory  
    );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="050ac-106">方法</span><span class="sxs-lookup"><span data-stu-id="050ac-106">Methods</span></span>  
  
|<span data-ttu-id="050ac-107">方法</span><span class="sxs-lookup"><span data-stu-id="050ac-107">Method</span></span>|<span data-ttu-id="050ac-108">说明</span><span class="sxs-lookup"><span data-stu-id="050ac-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="050ac-109">ICoreClrDebugTarget::EnumProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="050ac-109">ICoreClrDebugTarget::EnumProcesses Method</span></span>](icoreclrdebugtarget-enumprocesses-method.md)|<span data-ttu-id="050ac-110">枚举远程计算机上运行的进程。</span><span class="sxs-lookup"><span data-stu-id="050ac-110">Enumerates the processes that are running on a remote computer.</span></span>|  
|[<span data-ttu-id="050ac-111">ICoreClrDebugTarget::EnumRuntimes 方法</span><span class="sxs-lookup"><span data-stu-id="050ac-111">ICoreClrDebugTarget::EnumRuntimes Method</span></span>](icoreclrdebugtarget-enumruntimes-method.md)|<span data-ttu-id="050ac-112">枚举远程计算机上指定进程中的公共语言运行时 (Clr) 。</span><span class="sxs-lookup"><span data-stu-id="050ac-112">Enumerates the common language runtimes (CLRs) in the specified process on a remote computer.</span></span>|  
|[<span data-ttu-id="050ac-113">ICoreClrDebugTarget::FreeMemory 方法</span><span class="sxs-lookup"><span data-stu-id="050ac-113">ICoreClrDebugTarget::FreeMemory Method</span></span>](icoreclrdebugtarget-freememory-method.md)|<span data-ttu-id="050ac-114">释放此类中枚举方法分配的内存。</span><span class="sxs-lookup"><span data-stu-id="050ac-114">Frees the memory that is allocated by the enumeration methods in this class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="050ac-115">备注</span><span class="sxs-lookup"><span data-stu-id="050ac-115">Remarks</span></span>  

 <span data-ttu-id="050ac-116">目前，此功能仅用于调试在远程 Macintosh 计算机上运行的基于 Silverlight 的应用程序目标。</span><span class="sxs-lookup"><span data-stu-id="050ac-116">Currently, this functionality is supported only for debugging a Silverlight-based application target that is running on a remote Macintosh computer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="050ac-117">要求</span><span class="sxs-lookup"><span data-stu-id="050ac-117">Requirements</span></span>  

 <span data-ttu-id="050ac-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="050ac-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="050ac-119">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="050ac-119">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="050ac-120">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="050ac-120">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="050ac-121">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="050ac-121">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="050ac-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="050ac-122">See also</span></span>

- [<span data-ttu-id="050ac-123">ICorDebugRemoteTarget 接口</span><span class="sxs-lookup"><span data-stu-id="050ac-123">ICorDebugRemoteTarget Interface</span></span>](icordebugremotetarget-interface.md)
- [<span data-ttu-id="050ac-124">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="050ac-124">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="050ac-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="050ac-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
