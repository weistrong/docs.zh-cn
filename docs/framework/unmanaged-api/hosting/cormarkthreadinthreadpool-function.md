---
description: 了解详细信息： CorMarkThreadInThreadPool 函数
title: CorMarkThreadInThreadPool 函数
ms.date: 03/30/2017
api_name:
- CorMarkThreadInThreadPool
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CorMarkThreadInThreadPool
helpviewer_keywords:
- CorMarkThreadInThreadPool function [.NET Framework hosting]
ms.assetid: 3f958d41-e82e-4ec3-ae6f-16c7b3b31e3e
topic_type:
- apiref
ms.openlocfilehash: 68d945870075f2f8c06fe76b7a71e2f806078694
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716927"
---
# <a name="cormarkthreadinthreadpool-function"></a><span data-ttu-id="9ebda-103">CorMarkThreadInThreadPool 函数</span><span class="sxs-lookup"><span data-stu-id="9ebda-103">CorMarkThreadInThreadPool Function</span></span>

<span data-ttu-id="9ebda-104">标记当前正在执行的线程池线程以执行托管代码。</span><span class="sxs-lookup"><span data-stu-id="9ebda-104">Marks the currently executing thread-pool thread for the execution of managed code.</span></span> <span data-ttu-id="9ebda-105">从 .NET Framework 版本2.0 开始，此函数不起作用。</span><span class="sxs-lookup"><span data-stu-id="9ebda-105">Starting with the .NET Framework version 2.0, this function has no effect.</span></span> <span data-ttu-id="9ebda-106">这不是必需的，并且可以从代码中删除。</span><span class="sxs-lookup"><span data-stu-id="9ebda-106">It is not required, and can be removed from your code.</span></span> <span data-ttu-id="9ebda-107">此函数在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="9ebda-107">This function is deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ebda-108">语法</span><span class="sxs-lookup"><span data-stu-id="9ebda-108">Syntax</span></span>  
  
```cpp  
void CorMarkThreadInThreadPool ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="9ebda-109">要求</span><span class="sxs-lookup"><span data-stu-id="9ebda-109">Requirements</span></span>  

 <span data-ttu-id="9ebda-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ebda-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9ebda-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9ebda-112">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9ebda-112">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9ebda-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ebda-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ebda-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ebda-114">See also</span></span>

- [<span data-ttu-id="9ebda-115">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="9ebda-115">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
