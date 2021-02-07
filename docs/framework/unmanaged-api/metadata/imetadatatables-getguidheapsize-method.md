---
description: 了解详细信息： IMetaDataTables：： GetGuidHeapSize 方法
title: IMetaDataTables::GetGuidHeapSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetGuidHeapSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetGuidHeapSize
helpviewer_keywords:
- GetGuidHeapSize method [.NET Framework metadata]
- IMetaDataTables::GetGuidHeapSize method [.NET Framework metadata]
ms.assetid: e875cbee-1ad9-4f1a-bf03-38cdb8ff371a
topic_type:
- apiref
ms.openlocfilehash: bbf2fd7e083c5a0a42ad69ab685b3e1aa8321d68
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688138"
---
# <a name="imetadatatablesgetguidheapsize-method"></a><span data-ttu-id="590cf-103">IMetaDataTables::GetGuidHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="590cf-103">IMetaDataTables::GetGuidHeapSize Method</span></span>

<span data-ttu-id="590cf-104">获取 GUID 堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="590cf-104">Gets the size, in bytes, of the GUID heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="590cf-105">语法</span><span class="sxs-lookup"><span data-stu-id="590cf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetGuidHeapSize (  
    [out] ULONG   *pcbGuids  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="590cf-106">参数</span><span class="sxs-lookup"><span data-stu-id="590cf-106">Parameters</span></span>  

 `pcbGuids`  
 <span data-ttu-id="590cf-107">弄一个指针，指向 GUID 堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="590cf-107">[out] A pointer to the size, in bytes, of the GUID heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="590cf-108">要求</span><span class="sxs-lookup"><span data-stu-id="590cf-108">Requirements</span></span>  

 <span data-ttu-id="590cf-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="590cf-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="590cf-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="590cf-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="590cf-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="590cf-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="590cf-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="590cf-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="590cf-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="590cf-113">See also</span></span>

- [<span data-ttu-id="590cf-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="590cf-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="590cf-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="590cf-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
