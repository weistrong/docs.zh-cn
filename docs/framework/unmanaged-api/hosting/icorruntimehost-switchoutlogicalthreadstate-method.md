---
description: 了解详细信息： ICorRuntimeHost：： SwitchOutLogicalThreadState 方法
title: ICorRuntimeHost::SwitchOutLogicalThreadState 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.SwitchOutLogicalThreadState
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::SwitchOutLogicalThreadState
helpviewer_keywords:
- ICorRuntimeHost::SwitchOutLogicalThreadState method [.NET Framework hosting]
- SwitchOutLogicalThreadState method [.NET Framework hosting]
ms.assetid: e1968f0b-2675-4dc2-8507-46164e1df154
topic_type:
- apiref
ms.openlocfilehash: b4190ebe6b2c260f85afd8dd17127d0c63dca6c8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799442"
---
# <a name="icorruntimehostswitchoutlogicalthreadstate-method"></a><span data-ttu-id="d6483-103">ICorRuntimeHost::SwitchOutLogicalThreadState 方法</span><span class="sxs-lookup"><span data-stu-id="d6483-103">ICorRuntimeHost::SwitchOutLogicalThreadState Method</span></span>

<span data-ttu-id="d6483-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="d6483-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6483-105">语法</span><span class="sxs-lookup"><span data-stu-id="d6483-105">Syntax</span></span>  
  
```cpp  
HRESULT SwitchOutLogicalThreadState(  
    [out] DWORD **pFiberCookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d6483-106">参数</span><span class="sxs-lookup"><span data-stu-id="d6483-106">Parameters</span></span>  

 `pFiberCookie`  
 <span data-ttu-id="d6483-107">弄指示要交换的纤程的 Cookie。</span><span class="sxs-lookup"><span data-stu-id="d6483-107">[out] Cookie that indicates the fiber being switched out.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d6483-108">要求</span><span class="sxs-lookup"><span data-stu-id="d6483-108">Requirements</span></span>  

 <span data-ttu-id="d6483-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d6483-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6483-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d6483-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d6483-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d6483-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d6483-112">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="d6483-112">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6483-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6483-113">See also</span></span>

- [<span data-ttu-id="d6483-114">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="d6483-114">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
