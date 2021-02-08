---
description: 了解详细信息： ICorRuntimeHost：： LocksHeldByLogicalThread 方法
title: ICorRuntimeHost::LocksHeldByLogicalThread 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.LocksHeldByLogicalThread
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::LocksHeldByLogicalThread
helpviewer_keywords:
- ICorRuntimeHost::LocksHeldByLogicalThread method [.NET Framework hosting]
- LocksHeldByLogicalThread method [.NET Framework hosting]
ms.assetid: c3601255-d894-4d7c-b1df-c31334551700
topic_type:
- apiref
ms.openlocfilehash: bd64151bdc0c6aa0235192f0fc7f4badd8b0bbd6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789640"
---
# <a name="icorruntimehostlocksheldbylogicalthread-method"></a><span data-ttu-id="42b38-103">ICorRuntimeHost::LocksHeldByLogicalThread 方法</span><span class="sxs-lookup"><span data-stu-id="42b38-103">ICorRuntimeHost::LocksHeldByLogicalThread Method</span></span>

<span data-ttu-id="42b38-104">检索当前线程所持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="42b38-104">Retrieves the number of locks that current thread holds.</span></span>  
  
 <span data-ttu-id="42b38-105">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="42b38-105">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42b38-106">语法</span><span class="sxs-lookup"><span data-stu-id="42b38-106">Syntax</span></span>  
  
```cpp  
HRESULT LocksHeldByLogicalThread(  
    [out] DWORD *pCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="42b38-107">参数</span><span class="sxs-lookup"><span data-stu-id="42b38-107">Parameters</span></span>  

 `pCount`  
 <span data-ttu-id="42b38-108">弄一个指针，指向当前线程所持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="42b38-108">[out] A pointer to the number of locks that the current thread holds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="42b38-109">要求</span><span class="sxs-lookup"><span data-stu-id="42b38-109">Requirements</span></span>  

 <span data-ttu-id="42b38-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42b38-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42b38-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="42b38-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="42b38-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="42b38-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="42b38-113">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="42b38-113">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42b38-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="42b38-114">See also</span></span>

- [<span data-ttu-id="42b38-115">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="42b38-115">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
