---
description: 了解详细信息： ICorConfiguration：： AddDebuggerSpecialThread 方法
title: ICorConfiguration::AddDebuggerSpecialThread 方法
ms.date: 03/30/2017
api_name:
- ICorConfiguration.AddDebuggerSpecialThread
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AddDebuggerSpecialThread
helpviewer_keywords:
- AddDebuggerSpecialThread method [.NET Framework hosting]
- ICorConfiguration::AddDebuggerSpecialThread method [.NET Framework hosting]
ms.assetid: 1f1e3239-438e-4be9-a3bb-7d0722d3a76d
topic_type:
- apiref
ms.openlocfilehash: b6904c2e4d5c265244ac096e0d64c2fc7f5d1be5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636697"
---
# <a name="icorconfigurationadddebuggerspecialthread-method"></a><span data-ttu-id="cd0ad-103">ICorConfiguration::AddDebuggerSpecialThread 方法</span><span class="sxs-lookup"><span data-stu-id="cd0ad-103">ICorConfiguration::AddDebuggerSpecialThread Method</span></span>

<span data-ttu-id="cd0ad-104">向调试服务指示当调试器在托管或非托管调试方案中停止应用程序时，应允许特定线程继续执行。</span><span class="sxs-lookup"><span data-stu-id="cd0ad-104">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd0ad-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd0ad-105">Syntax</span></span>  
  
```cpp  
HRESULT AddDebuggerSpecialThread (  
    [in] DWORD dwSpecialThreadId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd0ad-106">参数</span><span class="sxs-lookup"><span data-stu-id="cd0ad-106">Parameters</span></span>  

 `dwSpecialThreadId`  
 <span data-ttu-id="cd0ad-107">中应该允许继续执行的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="cd0ad-107">[in] The ID of the thread that should be allowed to continue executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cd0ad-108">备注</span><span class="sxs-lookup"><span data-stu-id="cd0ad-108">Remarks</span></span>  

 <span data-ttu-id="cd0ad-109">不允许指定的线程运行托管代码或以任何方式进入运行时。</span><span class="sxs-lookup"><span data-stu-id="cd0ad-109">The specified thread will not be allowed to run managed code or enter the runtime in any way.</span></span> <span data-ttu-id="cd0ad-110">此类线程的一个示例就是支持旧版脚本调试器的进程内线程。</span><span class="sxs-lookup"><span data-stu-id="cd0ad-110">An example of such a thread would be an in-process thread to support legacy script debuggers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd0ad-111">要求</span><span class="sxs-lookup"><span data-stu-id="cd0ad-111">Requirements</span></span>  

 <span data-ttu-id="cd0ad-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0ad-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd0ad-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cd0ad-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cd0ad-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cd0ad-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cd0ad-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd0ad-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd0ad-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd0ad-116">See also</span></span>

- [<span data-ttu-id="cd0ad-117">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="cd0ad-117">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)
