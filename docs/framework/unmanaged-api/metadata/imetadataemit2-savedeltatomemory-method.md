---
description: 了解详细信息： IMetaDataEmit2：： SaveDeltaToMemory 方法
title: IMetaDataEmit2::SaveDeltaToMemory 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDeltaToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDeltaToMemory
helpviewer_keywords:
- SaveDeltaToMemory method [.NET Framework metadata]
- IMetaDataEmit2::SaveDeltaToMemory method [.NET Framework metadata]
ms.assetid: e2146726-0084-4c9e-a2d2-e8d461b13b21
topic_type:
- apiref
ms.openlocfilehash: 3ef01889df6dede85947508ca08635c95d655666
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771751"
---
# <a name="imetadataemit2savedeltatomemory-method"></a><span data-ttu-id="2d035-103">IMetaDataEmit2::SaveDeltaToMemory 方法</span><span class="sxs-lookup"><span data-stu-id="2d035-103">IMetaDataEmit2::SaveDeltaToMemory Method</span></span>

<span data-ttu-id="2d035-104">将当前的 "编辑并继续" 会话中的更改保存到内存。</span><span class="sxs-lookup"><span data-stu-id="2d035-104">Saves changes from the current edit-and-continue session to memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d035-105">语法</span><span class="sxs-lookup"><span data-stu-id="2d035-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveDeltaToMemory (  
    [out] void        *pbData,
    [in]  ULONG       cbData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d035-106">参数</span><span class="sxs-lookup"><span data-stu-id="2d035-106">Parameters</span></span>  

 `pbData`  
 <span data-ttu-id="2d035-107">弄开始写入元数据增量的地址。</span><span class="sxs-lookup"><span data-stu-id="2d035-107">[out] The address at which to begin writing the metadata delta.</span></span>  
  
 `cbData`  
 <span data-ttu-id="2d035-108">中更改的大小。</span><span class="sxs-lookup"><span data-stu-id="2d035-108">[in] The size of the changes.</span></span> <span data-ttu-id="2d035-109">使用 [IMetaDataEmit2：： GetDeltaSaveSize](imetadataemit2-getdeltasavesize-method.md) 确定大小。</span><span class="sxs-lookup"><span data-stu-id="2d035-109">Use [IMetaDataEmit2::GetDeltaSaveSize](imetadataemit2-getdeltasavesize-method.md) to determine the size.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d035-110">要求</span><span class="sxs-lookup"><span data-stu-id="2d035-110">Requirements</span></span>  

 <span data-ttu-id="2d035-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d035-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d035-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="2d035-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2d035-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="2d035-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2d035-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d035-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d035-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d035-115">See also</span></span>

- [<span data-ttu-id="2d035-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="2d035-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="2d035-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="2d035-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
