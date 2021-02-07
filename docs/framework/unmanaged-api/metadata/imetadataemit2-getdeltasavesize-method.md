---
description: 了解详细信息： IMetaDataEmit2：： GetDeltaSaveSize 方法
title: IMetaDataEmit2::GetDeltaSaveSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.GetDeltaSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::GetDeltaSaveSize
helpviewer_keywords:
- IMetaDataEmit2::GetDeltaSaveSize method [.NET Framework metadata]
- GetDeltaSaveSize method [.NET Framework metadata]
ms.assetid: 036db5e7-8211-4645-9a34-03d1a89be955
topic_type:
- apiref
ms.openlocfilehash: d7b5eae7f89a5465876083c5cc8021330d3c59de
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745757"
---
# <a name="imetadataemit2getdeltasavesize-method"></a><span data-ttu-id="256bd-103">IMetaDataEmit2::GetDeltaSaveSize 方法</span><span class="sxs-lookup"><span data-stu-id="256bd-103">IMetaDataEmit2::GetDeltaSaveSize Method</span></span>

<span data-ttu-id="256bd-104">获取一个值，该值指示当前的 "编辑并继续" 会话导致的元数据大小的任何更改。</span><span class="sxs-lookup"><span data-stu-id="256bd-104">Gets a value indicating any change in metadata size that results from the current edit-and-continue session.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="256bd-105">语法</span><span class="sxs-lookup"><span data-stu-id="256bd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDeltaSaveSize (  
    [in]  CorSaveSize  fSave,  
    [out] DWORD        *pdwSaveSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="256bd-106">参数</span><span class="sxs-lookup"><span data-stu-id="256bd-106">Parameters</span></span>  

 `fSave`  
 <span data-ttu-id="256bd-107">中 [CorSaveSize](corsavesize-enumeration.md) 值之一，指示所需的精度级别。</span><span class="sxs-lookup"><span data-stu-id="256bd-107">[in] One of the [CorSaveSize](corsavesize-enumeration.md) values, indicating the level of precision desired.</span></span> <span data-ttu-id="256bd-108">对于 .NET Framework 版本2.0，将忽略此参数。</span><span class="sxs-lookup"><span data-stu-id="256bd-108">For the .NET Framework version 2.0, this parameter is ignored.</span></span>  
  
 `pdwSaveSize`  
 <span data-ttu-id="256bd-109">弄元数据的大小更改。</span><span class="sxs-lookup"><span data-stu-id="256bd-109">[out] The change in the size of the metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="256bd-110">要求</span><span class="sxs-lookup"><span data-stu-id="256bd-110">Requirements</span></span>  

 <span data-ttu-id="256bd-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="256bd-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="256bd-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="256bd-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="256bd-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="256bd-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="256bd-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="256bd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="256bd-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="256bd-115">See also</span></span>

- [<span data-ttu-id="256bd-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="256bd-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="256bd-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="256bd-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
