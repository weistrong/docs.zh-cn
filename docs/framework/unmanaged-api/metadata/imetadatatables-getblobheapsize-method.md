---
description: 了解详细信息： IMetaDataTables：： GetBlobHeapSize 方法
title: IMetaDataTables::GetBlobHeapSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetBlobHeapSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetBlobHeapSize
helpviewer_keywords:
- GetBlobHeapSize method [.NET Framework metadata]
- IMetaDataTables::GetBlobHeapSize method [.NET Framework metadata]
ms.assetid: 6330a9ee-8cd5-4299-86f1-b4de2c701a0d
topic_type:
- apiref
ms.openlocfilehash: f6d5c7aeb5e1cc1f307d53d8f3e3cc99daa72311
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688307"
---
# <a name="imetadatatablesgetblobheapsize-method"></a><span data-ttu-id="5e4f5-103">IMetaDataTables::GetBlobHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="5e4f5-103">IMetaDataTables::GetBlobHeapSize Method</span></span>

<span data-ttu-id="5e4f5-104">获取 (BLOB) 堆的二进制大型对象的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5e4f5-104">Gets the size, in bytes, of the binary large object (BLOB) heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e4f5-105">语法</span><span class="sxs-lookup"><span data-stu-id="5e4f5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBlobHeapSize (  
    [out] ULONG     *pcbBlobs  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="5e4f5-106">参数</span><span class="sxs-lookup"><span data-stu-id="5e4f5-106">Parameters</span></span>  

 `pcbBlobs`  
 <span data-ttu-id="5e4f5-107">弄一个指针，指向 BLOB 堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5e4f5-107">[out] A pointer to the size, in bytes, of the BLOB heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e4f5-108">要求</span><span class="sxs-lookup"><span data-stu-id="5e4f5-108">Requirements</span></span>  

 <span data-ttu-id="5e4f5-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5e4f5-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e4f5-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5e4f5-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5e4f5-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5e4f5-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5e4f5-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e4f5-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e4f5-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5e4f5-113">See also</span></span>

- [<span data-ttu-id="5e4f5-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="5e4f5-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="5e4f5-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="5e4f5-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
