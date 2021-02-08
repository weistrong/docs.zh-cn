---
description: 了解详细信息： IMetaDataEmit：： SetRVA 方法
title: IMetaDataEmit::SetRVA 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetRVA
helpviewer_keywords:
- IMetaDataEmit::SetRVA method [.NET Framework metadata]
- SetRVA method [.NET Framework metadata]
ms.assetid: 4d69fb6d-ee35-4318-8224-5eea2bd16818
topic_type:
- apiref
ms.openlocfilehash: 52294250df2b7a677bb4ecb09ea0a97baca595a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771777"
---
# <a name="imetadataemitsetrva-method"></a><span data-ttu-id="6b874-103">IMetaDataEmit::SetRVA 方法</span><span class="sxs-lookup"><span data-stu-id="6b874-103">IMetaDataEmit::SetRVA Method</span></span>

<span data-ttu-id="6b874-104">设置指定方法的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="6b874-104">Sets the relative virtual address of the specified method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b874-105">语法</span><span class="sxs-lookup"><span data-stu-id="6b874-105">Syntax</span></span>  
  
```cpp  
HRESULT SetRVA (  
    [in]  mdMethodDef  md,
    [in]  ULONG        ulRVA
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6b874-106">参数</span><span class="sxs-lookup"><span data-stu-id="6b874-106">Parameters</span></span>  

 `md`  
 <span data-ttu-id="6b874-107">中目标方法或方法实现的标记。</span><span class="sxs-lookup"><span data-stu-id="6b874-107">[in] The token for the target method or method implementation.</span></span>  
  
 `ulRVA`  
 <span data-ttu-id="6b874-108">中代码或数据区域的地址。</span><span class="sxs-lookup"><span data-stu-id="6b874-108">[in] The address of the code or data area.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b874-109">要求</span><span class="sxs-lookup"><span data-stu-id="6b874-109">Requirements</span></span>  

 <span data-ttu-id="6b874-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6b874-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6b874-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="6b874-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6b874-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="6b874-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6b874-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6b874-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b874-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="6b874-114">See also</span></span>

- [<span data-ttu-id="6b874-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="6b874-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="6b874-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="6b874-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
