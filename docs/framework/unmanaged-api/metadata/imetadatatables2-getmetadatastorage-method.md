---
description: 了解详细信息： IMetaDataTables2：： GetMetaDataStorage 方法
title: IMetaDataTables2::GetMetaDataStorage 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables2.GetMetaDataStorage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables2::GetMetaDataStorage
helpviewer_keywords:
- GetMetaDataStorage method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStorage method [.NET Framework metadata]
ms.assetid: 667a6d1e-753d-4ea2-8fd8-a8337d1bb9cd
topic_type:
- apiref
ms.openlocfilehash: df6bbc69be05986dc6d4f143cec7ec09a2d78ee5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799237"
---
# <a name="imetadatatables2getmetadatastorage-method"></a><span data-ttu-id="0a608-103">IMetaDataTables2::GetMetaDataStorage 方法</span><span class="sxs-lookup"><span data-stu-id="0a608-103">IMetaDataTables2::GetMetaDataStorage Method</span></span>

<span data-ttu-id="0a608-104">获取指定节中存储的元数据的大小和内容。</span><span class="sxs-lookup"><span data-stu-id="0a608-104">Gets the size and contents of the metadata stored in the specified section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a608-105">语法</span><span class="sxs-lookup"><span data-stu-id="0a608-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaDataStorage (  
   [in, out] const void   **ppvMd,  
   [out] ULONG   *pcbMd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a608-106">参数</span><span class="sxs-lookup"><span data-stu-id="0a608-106">Parameters</span></span>  

 `ppvMd`  
 <span data-ttu-id="0a608-107">[in，out]指向元数据部分的指针。</span><span class="sxs-lookup"><span data-stu-id="0a608-107">[in, out] A pointer to a metadata section.</span></span>  
  
 `pcbMd`  
 <span data-ttu-id="0a608-108">弄元数据流的大小。</span><span class="sxs-lookup"><span data-stu-id="0a608-108">[out] The size of the metadata stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a608-109">要求</span><span class="sxs-lookup"><span data-stu-id="0a608-109">Requirements</span></span>  

 <span data-ttu-id="0a608-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0a608-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a608-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0a608-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0a608-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0a608-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0a608-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0a608-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a608-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="0a608-114">See also</span></span>

- [<span data-ttu-id="0a608-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="0a608-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
- [<span data-ttu-id="0a608-116">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="0a608-116">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
