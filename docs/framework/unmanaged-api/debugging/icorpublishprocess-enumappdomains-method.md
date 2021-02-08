---
description: 了解详细信息： ICorPublishProcess：： EnumAppDomains 方法
title: ICorPublishProcess::EnumAppDomains 方法
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.EnumAppDomains
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::EnumAppDomains
helpviewer_keywords:
- EnumAppDomains method [.NET Framework debugging]
- ICorPublishProcess::EnumAppDomains method [.NET Framework debugging]
ms.assetid: 7da621fc-e7d0-4c00-9439-5c93619d7414
topic_type:
- apiref
ms.openlocfilehash: c7834b23967ab467c1589ee31929bf346b4b3b8f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794600"
---
# <a name="icorpublishprocessenumappdomains-method"></a><span data-ttu-id="df2dc-103">ICorPublishProcess::EnumAppDomains 方法</span><span class="sxs-lookup"><span data-stu-id="df2dc-103">ICorPublishProcess::EnumAppDomains Method</span></span>

<span data-ttu-id="df2dc-104">获取此 [ICorPublishProcess](icorpublishprocess-interface.md)引用的进程中的应用程序域的枚举器。</span><span class="sxs-lookup"><span data-stu-id="df2dc-104">Gets an enumerator for the application domains in the process that is referenced by this [ICorPublishProcess](icorpublishprocess-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df2dc-105">语法</span><span class="sxs-lookup"><span data-stu-id="df2dc-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumAppDomains (  
    [out] ICorPublishAppDomainEnum   **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="df2dc-106">参数</span><span class="sxs-lookup"><span data-stu-id="df2dc-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="df2dc-107">弄一个指针，指向允许在此进程中通过应用程序域集合进行迭代的 [ICorPublishAppDomainEnum](icorpublishappdomainenum-interface.md) 实例的地址。</span><span class="sxs-lookup"><span data-stu-id="df2dc-107">[out] A pointer to the address of an [ICorPublishAppDomainEnum](icorpublishappdomainenum-interface.md) instance that allows iteration through the collection of application domains in this process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="df2dc-108">备注</span><span class="sxs-lookup"><span data-stu-id="df2dc-108">Remarks</span></span>  

 <span data-ttu-id="df2dc-109">应用程序域的列表基于在调用方法时存在的应用程序域的快照 `EnumAppDomains` 。</span><span class="sxs-lookup"><span data-stu-id="df2dc-109">The list of application domains is based on a snapshot of the application domains that exist when the `EnumAppDomains` method is called.</span></span> <span data-ttu-id="df2dc-110">可以多次调用此方法来创建新的最新列表。</span><span class="sxs-lookup"><span data-stu-id="df2dc-110">This method may be called more than once to create a new up-to-date list.</span></span> <span data-ttu-id="df2dc-111">此方法的后续调用将不会影响现有列表。</span><span class="sxs-lookup"><span data-stu-id="df2dc-111">Existing lists will not be affected by subsequent calls of this method.</span></span>  
  
 <span data-ttu-id="df2dc-112">如果进程已终止， `EnumAppDomains` 则将失败，并且 HRESULT 值为 CORDBG_E_PROCESS_TERMINATED。</span><span class="sxs-lookup"><span data-stu-id="df2dc-112">If the process has been terminated, `EnumAppDomains` will fail with an HRESULT value of CORDBG_E_PROCESS_TERMINATED.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df2dc-113">要求</span><span class="sxs-lookup"><span data-stu-id="df2dc-113">Requirements</span></span>  

 <span data-ttu-id="df2dc-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df2dc-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df2dc-115">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="df2dc-115">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="df2dc-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="df2dc-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="df2dc-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df2dc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df2dc-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="df2dc-118">See also</span></span>

- [<span data-ttu-id="df2dc-119">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="df2dc-119">ICorPublishProcess Interface</span></span>](icorpublishprocess-interface.md)
