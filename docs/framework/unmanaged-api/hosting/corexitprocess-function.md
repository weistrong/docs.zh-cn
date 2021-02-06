---
description: 了解详细信息： CorExitProcess 函数
title: CorExitProcess 函数
ms.date: 03/30/2017
api_name:
- CorExitProcess
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CorExitProcess
helpviewer_keywords:
- CorExitProcess function [.NET Framework hosting]
ms.assetid: a5cab4c6-990e-47f3-8798-cf422b791015
topic_type:
- apiref
ms.openlocfilehash: 68d33dec76387e103a34e99c529a4e7aff7535b4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649580"
---
# <a name="corexitprocess-function"></a><span data-ttu-id="54ab3-103">CorExitProcess 函数</span><span class="sxs-lookup"><span data-stu-id="54ab3-103">CorExitProcess Function</span></span>

<span data-ttu-id="54ab3-104">关闭当前的非托管进程。</span><span class="sxs-lookup"><span data-stu-id="54ab3-104">Shuts down the current unmanaged process.</span></span>  
  
 <span data-ttu-id="54ab3-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="54ab3-105">This function has been deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="54ab3-106">改为使用 [ICLRMetaHost：： ExitProcess](iclrmetahost-exitprocess-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="54ab3-106">Use the [ICLRMetaHost::ExitProcess](iclrmetahost-exitprocess-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54ab3-107">语法</span><span class="sxs-lookup"><span data-stu-id="54ab3-107">Syntax</span></span>  
  
```cpp  
void STDMETHODCALLTYPE CorExitProcess (
  int  exitCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="54ab3-108">参数</span><span class="sxs-lookup"><span data-stu-id="54ab3-108">Parameters</span></span>  

 `exitCode`  
 <span data-ttu-id="54ab3-109">一个整数，指定进程退出代码。</span><span class="sxs-lookup"><span data-stu-id="54ab3-109">An integer that specifies the process exit code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="54ab3-110">备注</span><span class="sxs-lookup"><span data-stu-id="54ab3-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="54ab3-111">从 .NET Framework 4 开始， `CorExitProcess` 退出进程中的每个已启动的运行时，而不只是旧 api 所绑定到的运行时。</span><span class="sxs-lookup"><span data-stu-id="54ab3-111">Beginning with the .NET Framework 4, `CorExitProcess` exits every started runtime in the process, not just the runtime to which the legacy APIs have been bound.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="54ab3-112">要求</span><span class="sxs-lookup"><span data-stu-id="54ab3-112">Requirements</span></span>  

 <span data-ttu-id="54ab3-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="54ab3-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54ab3-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="54ab3-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="54ab3-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="54ab3-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="54ab3-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54ab3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54ab3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="54ab3-117">See also</span></span>

- [<span data-ttu-id="54ab3-118">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="54ab3-118">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
