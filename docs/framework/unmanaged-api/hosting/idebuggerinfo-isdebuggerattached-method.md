---
description: 了解详细信息： IDebuggerInfo：： IsDebuggerAttached 方法
title: IDebuggerInfo::IsDebuggerAttached 方法
ms.date: 03/30/2017
api_name:
- IDebuggerInfo.IsDebuggerAttached
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IsDebuggerAttached
helpviewer_keywords:
- IDebuggerInfo::IsDebuggerAttached method [.NET Framework hosting]
- IsDebuggerAttached method, IDebuggerInfo interface [.NET Framework hosting]
ms.assetid: 6e21872f-602f-411a-a423-bff5cdf27000
topic_type:
- apiref
ms.openlocfilehash: a17a7f5f1cef1d0c7025f4051e59767ce09ec421
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709797"
---
# <a name="idebuggerinfoisdebuggerattached-method"></a><span data-ttu-id="5527a-103">IDebuggerInfo::IsDebuggerAttached 方法</span><span class="sxs-lookup"><span data-stu-id="5527a-103">IDebuggerInfo::IsDebuggerAttached Method</span></span>

<span data-ttu-id="5527a-104">获取一个值，该值指示托管调试器是否已附加到此进程。</span><span class="sxs-lookup"><span data-stu-id="5527a-104">Gets a value that indicates whether a managed debugger is attached to this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5527a-105">语法</span><span class="sxs-lookup"><span data-stu-id="5527a-105">Syntax</span></span>  
  
```cpp  
HRESULT IsDebuggerAttached (  
    [out] BOOL *pbAttached  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5527a-106">参数</span><span class="sxs-lookup"><span data-stu-id="5527a-106">Parameters</span></span>  

 `pbAttached`  
 <span data-ttu-id="5527a-107">弄一个指向值的指针， `true` 如果托管调试器附加到进程，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5527a-107">[out] A pointer to a value that is `true` if a managed debugger is attached to the process; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5527a-108">要求</span><span class="sxs-lookup"><span data-stu-id="5527a-108">Requirements</span></span>  

 <span data-ttu-id="5527a-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5527a-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5527a-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5527a-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5527a-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5527a-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5527a-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5527a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5527a-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5527a-113">See also</span></span>

- [<span data-ttu-id="5527a-114">IDebuggerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="5527a-114">IDebuggerInfo Interface</span></span>](idebuggerinfo-interface.md)
