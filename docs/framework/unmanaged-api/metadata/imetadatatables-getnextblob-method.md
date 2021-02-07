---
description: 了解详细信息： IMetaDataTables：： GetNextBlob 方法
title: IMetaDataTables::GetNextBlob 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextBlob
helpviewer_keywords:
- IMetaDataTables::GetNextBlob method [.NET Framework metadata]
- GetNextBlob method [.NET Framework metadata]
ms.assetid: 017c8ab4-4c09-4754-9935-5b0b49cabecb
topic_type:
- apiref
ms.openlocfilehash: 99126ab5c3891ee09346bb54096a4fce3ca44bc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688125"
---
# <a name="imetadatatablesgetnextblob-method"></a><span data-ttu-id="871eb-103">IMetaDataTables::GetNextBlob 方法</span><span class="sxs-lookup"><span data-stu-id="871eb-103">IMetaDataTables::GetNextBlob Method</span></span>

<span data-ttu-id="871eb-104">获取表中 (BLOB) 的下一个二进制大型对象的索引。</span><span class="sxs-lookup"><span data-stu-id="871eb-104">Gets the index of the next binary large object (BLOB) in the table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="871eb-105">语法</span><span class="sxs-lookup"><span data-stu-id="871eb-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNextBlob (  
    [in]  ULONG   ixBlob,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="871eb-106">参数</span><span class="sxs-lookup"><span data-stu-id="871eb-106">Parameters</span></span>  

 `ixBlob`  
 <span data-ttu-id="871eb-107">中从 Blob 的列中返回的索引。</span><span class="sxs-lookup"><span data-stu-id="871eb-107">[in] The index, as returned from a column of BLOBs.</span></span>  
  
 `pNext`  
 <span data-ttu-id="871eb-108">弄指向下一个 BLOB 的索引的指针。</span><span class="sxs-lookup"><span data-stu-id="871eb-108">[out] A pointer to the index of the next BLOB.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="871eb-109">要求</span><span class="sxs-lookup"><span data-stu-id="871eb-109">Requirements</span></span>  

 <span data-ttu-id="871eb-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="871eb-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="871eb-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="871eb-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="871eb-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="871eb-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="871eb-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="871eb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="871eb-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="871eb-114">See also</span></span>

- [<span data-ttu-id="871eb-115">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="871eb-115">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="871eb-116">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="871eb-116">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
