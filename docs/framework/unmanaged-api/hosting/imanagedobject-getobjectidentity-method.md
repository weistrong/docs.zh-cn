---
description: 了解详细信息： IManagedObject：： GetObjectIdentity 方法
title: IManagedObject::GetObjectIdentity 方法
ms.date: 03/30/2017
api_name:
- IManagedObject.GetObjectIdentity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetObjectIdentity
helpviewer_keywords:
- GetObjectIdentity method [.NET Framework hosting]
- IManagedObject::GetObjectIdentity method [.NET Framework hosting]
ms.assetid: b862ff3e-e480-4cdf-84e2-e1013334a467
topic_type:
- apiref
ms.openlocfilehash: 8929819bbf490680b5f3f1f47b9f3b8e830d57ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671160"
---
# <a name="imanagedobjectgetobjectidentity-method"></a><span data-ttu-id="37734-103">IManagedObject::GetObjectIdentity 方法</span><span class="sxs-lookup"><span data-stu-id="37734-103">IManagedObject::GetObjectIdentity Method</span></span>

<span data-ttu-id="37734-104">获取此托管对象的标识。</span><span class="sxs-lookup"><span data-stu-id="37734-104">Gets the identity of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37734-105">语法</span><span class="sxs-lookup"><span data-stu-id="37734-105">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectIdentity (  
    [out] BSTR*   pBSTRGUID,  
    [out] int*    AppDomainID,  
    [out] CCW_PTR pCCW  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="37734-106">参数</span><span class="sxs-lookup"><span data-stu-id="37734-106">Parameters</span></span>  

 `pBSTRGUID`  
 <span data-ttu-id="37734-107">弄指向对象所在的进程的 GUID 的指针。</span><span class="sxs-lookup"><span data-stu-id="37734-107">[out] A pointer to the GUID of the process in which the object resides.</span></span>  
  
 `AppDomainID`  
 <span data-ttu-id="37734-108">弄指向对象的应用程序域的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="37734-108">[out] A pointer to the ID of the object's application domain.</span></span>  
  
 `pCCW`  
 <span data-ttu-id="37734-109">弄指向 COM 经典 v 表中对象索引的指针。</span><span class="sxs-lookup"><span data-stu-id="37734-109">[out] A pointer to object's index in the COM classic v-table.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="37734-110">备注</span><span class="sxs-lookup"><span data-stu-id="37734-110">Remarks</span></span>  

 <span data-ttu-id="37734-111">托管对象的标识包括进程 GUID、应用程序域 ID 以及 COM 经典 v 表中对象的索引。</span><span class="sxs-lookup"><span data-stu-id="37734-111">The identity of a managed object includes process GUID, application domain ID, and the object's index in the COM classic v-table.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="37734-112">要求</span><span class="sxs-lookup"><span data-stu-id="37734-112">Requirements</span></span>  

 <span data-ttu-id="37734-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="37734-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="37734-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="37734-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="37734-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="37734-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="37734-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37734-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37734-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="37734-117">See also</span></span>

- [<span data-ttu-id="37734-118">IManagedObject 接口</span><span class="sxs-lookup"><span data-stu-id="37734-118">IManagedObject Interface</span></span>](imanagedobject-interface.md)
