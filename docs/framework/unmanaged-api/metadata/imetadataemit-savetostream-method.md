---
description: 了解详细信息： IMetaDataEmit：： SaveToStream 方法
title: IMetaDataEmit::SaveToStream 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SaveToStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SaveToStream
helpviewer_keywords:
- IMetaDataEmit::SaveToStream method [.NET Framework metadata]
- SaveToStream method [.NET Framework metadata]
ms.assetid: e0290a49-3818-4a43-ad46-3014faa34f97
topic_type:
- apiref
ms.openlocfilehash: 104aa0b0dfcd0f4f9e8b87b4633880f6423f92d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706651"
---
# <a name="imetadataemitsavetostream-method"></a><span data-ttu-id="8249f-103">IMetaDataEmit::SaveToStream 方法</span><span class="sxs-lookup"><span data-stu-id="8249f-103">IMetaDataEmit::SaveToStream Method</span></span>

<span data-ttu-id="8249f-104">将当前范围中的所有元数据保存到指定的 `IStream` 。</span><span class="sxs-lookup"><span data-stu-id="8249f-104">Saves all metadata in the current scope to the specified `IStream`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8249f-105">语法</span><span class="sxs-lookup"><span data-stu-id="8249f-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveToStream (
    [in]  IStream     *pIStream,  
    [in]  DWORD       dwSaveFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8249f-106">参数</span><span class="sxs-lookup"><span data-stu-id="8249f-106">Parameters</span></span>  

 `pIStream`  
 <span data-ttu-id="8249f-107">中要保存到的可写流。</span><span class="sxs-lookup"><span data-stu-id="8249f-107">[in] The writable stream to save to.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="8249f-108">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="8249f-108">[in] Reserved.</span></span> <span data-ttu-id="8249f-109">必须为零。</span><span class="sxs-lookup"><span data-stu-id="8249f-109">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8249f-110">要求</span><span class="sxs-lookup"><span data-stu-id="8249f-110">Requirements</span></span>  

 <span data-ttu-id="8249f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8249f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8249f-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8249f-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8249f-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8249f-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8249f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8249f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8249f-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8249f-115">See also</span></span>

- [<span data-ttu-id="8249f-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8249f-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="8249f-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8249f-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
