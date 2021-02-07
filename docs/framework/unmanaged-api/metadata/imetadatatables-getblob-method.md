---
description: 了解详细信息： IMetaDataTables：： GetBlob 方法
title: IMetaDataTables::GetBlob 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetBlob
helpviewer_keywords:
- GetBlob method [.NET Framework metadata]
- IMetaDataTables::GetBlob method [.NET Framework metadata]
ms.assetid: 94667c1c-6d58-4aa7-b74e-530b11e2a276
topic_type:
- apiref
ms.openlocfilehash: 733f94c280283e00b644fe7811d450efbc7e1e7c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688385"
---
# <a name="imetadatatablesgetblob-method"></a><span data-ttu-id="e4ec6-103">IMetaDataTables::GetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="e4ec6-103">IMetaDataTables::GetBlob Method</span></span>

<span data-ttu-id="e4ec6-104">获取一个指针，该指针指向指定列索引 (BLOB) 的二进制大型对象。</span><span class="sxs-lookup"><span data-stu-id="e4ec6-104">Gets a pointer to the binary large object (BLOB) at the specified column index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4ec6-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4ec6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBlob (  
    [in]  ULONG          ixBlob,  
    [out] ULONG          *pcbData,  
    [out] const void     **ppData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4ec6-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4ec6-106">Parameters</span></span>  

 `ixBlob`  
 <span data-ttu-id="e4ec6-107">中要从其获取的内存地址 `ppData` 。</span><span class="sxs-lookup"><span data-stu-id="e4ec6-107">[in] The memory address from which to get `ppData`.</span></span>  
  
 `pcbData`  
 <span data-ttu-id="e4ec6-108">弄一个指针，指向的大小（以字节为单位） `ppData` 。</span><span class="sxs-lookup"><span data-stu-id="e4ec6-108">[out] A pointer to the size, in bytes, of `ppData`.</span></span>  
  
 `ppData`  
 <span data-ttu-id="e4ec6-109">弄指向所检索到的二进制数据的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="e4ec6-109">[out] A pointer to a pointer to the binary data retrieved.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4ec6-110">要求</span><span class="sxs-lookup"><span data-stu-id="e4ec6-110">Requirements</span></span>  

 <span data-ttu-id="e4ec6-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4ec6-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4ec6-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e4ec6-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e4ec6-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e4ec6-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e4ec6-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4ec6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4ec6-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4ec6-115">See also</span></span>

- [<span data-ttu-id="e4ec6-116">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="e4ec6-116">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="e4ec6-117">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="e4ec6-117">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
