---
description: 了解详细信息： ICLRAssemblyReferenceList：： IsStringAssemblyReferenceInList 方法
title: ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyReferenceList.IsStringAssemblyReferenceInList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList
helpviewer_keywords:
- ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList method [.NET Framework hosting]
- IsStringAssemblyReferenceInList method [.NET Framework hosting]
ms.assetid: e6121cc3-2f11-42c7-bdae-47808581ff71
topic_type:
- apiref
ms.openlocfilehash: 667764337fbda22a526e51575faf049efc4b86ca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790030"
---
# <a name="iclrassemblyreferencelistisstringassemblyreferenceinlist-method"></a><span data-ttu-id="ab05d-103">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList 方法</span><span class="sxs-lookup"><span data-stu-id="ab05d-103">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList Method</span></span>

<span data-ttu-id="ab05d-104">获取一个值，该值指示所提供的名称是否与列表中的程序集的名称相匹配。</span><span class="sxs-lookup"><span data-stu-id="ab05d-104">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab05d-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab05d-105">Syntax</span></span>  
  
```cpp  
HRESULT IsStringAssemblyReferenceInList (  
    [in] LPCWSTR pwzAssemblyName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab05d-106">参数</span><span class="sxs-lookup"><span data-stu-id="ab05d-106">Parameters</span></span>  

 `pwzAssemblyName`  
 <span data-ttu-id="ab05d-107">中要搜索的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="ab05d-107">[in] The name of the assembly for which to search.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ab05d-108">返回值</span><span class="sxs-lookup"><span data-stu-id="ab05d-108">Return Value</span></span>  
  
|<span data-ttu-id="ab05d-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ab05d-109">HRESULT</span></span>|<span data-ttu-id="ab05d-110">说明</span><span class="sxs-lookup"><span data-stu-id="ab05d-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ab05d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab05d-111">S_OK</span></span>|<span data-ttu-id="ab05d-112">此字符串将显示在列表中。</span><span class="sxs-lookup"><span data-stu-id="ab05d-112">The string appears in the list.</span></span>|  
|<span data-ttu-id="ab05d-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ab05d-113">S_FALSE</span></span>|<span data-ttu-id="ab05d-114">该字符串未出现在列表中。</span><span class="sxs-lookup"><span data-stu-id="ab05d-114">The string does not appear in the list.</span></span>|  
|<span data-ttu-id="ab05d-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ab05d-115">E_FAIL</span></span>|<span data-ttu-id="ab05d-116">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ab05d-116">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ab05d-117">方法返回 E_FAIL 后，公共语言运行时在进程中将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ab05d-117">After a method returns E_FAIL, the common language runtime is no longer usable within the process.</span></span> <span data-ttu-id="ab05d-118">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ab05d-118">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab05d-119">要求</span><span class="sxs-lookup"><span data-stu-id="ab05d-119">Requirements</span></span>  

 <span data-ttu-id="ab05d-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ab05d-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab05d-121">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ab05d-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ab05d-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ab05d-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ab05d-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab05d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab05d-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab05d-124">See also</span></span>

- [<span data-ttu-id="ab05d-125">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="ab05d-125">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="ab05d-126">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="ab05d-126">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="ab05d-127">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="ab05d-127">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
- [<span data-ttu-id="ab05d-128">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="ab05d-128">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
