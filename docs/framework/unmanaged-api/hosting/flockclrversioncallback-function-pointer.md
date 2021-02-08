---
description: 了解详细信息： FLockClrVersionCallback 函数指针
title: FLockClrVersionCallback 函数指针
ms.date: 03/30/2017
api_name:
- FLockClrVersionCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FLockClrVersionCallback
helpviewer_keywords:
- FLockClrVersionCallback function pointer [.NET Framework hosting]
ms.assetid: 98a4762d-9ad2-45bd-9d03-39064a028b44
topic_type:
- apiref
ms.openlocfilehash: 3506cd30ab2a9e5a06b03f5010c9870280a38378
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785375"
---
# <a name="flockclrversioncallback-function-pointer"></a><span data-ttu-id="dfa74-103">FLockClrVersionCallback 函数指针</span><span class="sxs-lookup"><span data-stu-id="dfa74-103">FLockClrVersionCallback Function Pointer</span></span>

<span data-ttu-id="dfa74-104">指向公共语言运行时 (CLR) 调用以指示初始化已启动或已完成的函数。</span><span class="sxs-lookup"><span data-stu-id="dfa74-104">Points to a function that the common language runtime (CLR) calls to indicate that initialization has either started or completed.</span></span>  
  
 <span data-ttu-id="dfa74-105">此函数指针在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="dfa74-105">This function pointer has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfa74-106">语法</span><span class="sxs-lookup"><span data-stu-id="dfa74-106">Syntax</span></span>  
  
```cpp  
typedef HRESULT (__stdcall *FLockClrVersionCallback) ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="dfa74-107">备注</span><span class="sxs-lookup"><span data-stu-id="dfa74-107">Remarks</span></span>  

 <span data-ttu-id="dfa74-108">此函数由主机实现。</span><span class="sxs-lookup"><span data-stu-id="dfa74-108">This function is implemented by the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfa74-109">要求</span><span class="sxs-lookup"><span data-stu-id="dfa74-109">Requirements</span></span>  

 <span data-ttu-id="dfa74-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dfa74-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dfa74-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="dfa74-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dfa74-112">**库：** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="dfa74-112">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="dfa74-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dfa74-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfa74-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="dfa74-114">See also</span></span>

- [<span data-ttu-id="dfa74-115">LockClrVersion 函数</span><span class="sxs-lookup"><span data-stu-id="dfa74-115">LockClrVersion Function</span></span>](lockclrversion-function.md)
- [<span data-ttu-id="dfa74-116">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="dfa74-116">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
