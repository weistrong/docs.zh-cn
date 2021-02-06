---
description: 了解详细信息： IMetaDataEmit：： SetFieldRVA 方法
title: IMetaDataEmit::SetFieldRVA 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldRVA
helpviewer_keywords:
- IMetaDataEmit::SetFieldRVA method [.NET Framework metadata]
- SetFieldRVA method [.NET Framework metadata]
ms.assetid: 6dc37f9d-87ee-4cb3-9216-ced600184ce8
topic_type:
- apiref
ms.openlocfilehash: 5d78880b892dc948337aa1ec1a471a5d380f1e2f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657926"
---
# <a name="imetadataemitsetfieldrva-method"></a><span data-ttu-id="f0762-103">IMetaDataEmit::SetFieldRVA 方法</span><span class="sxs-lookup"><span data-stu-id="f0762-103">IMetaDataEmit::SetFieldRVA Method</span></span>

<span data-ttu-id="f0762-104">为指定的标记所引用的字段的相对虚拟地址设置全局变量值。</span><span class="sxs-lookup"><span data-stu-id="f0762-104">Sets a global variable value for the relative virtual address of the field referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0762-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0762-105">Syntax</span></span>  
  
```cpp  
HRESULT SetFieldRVA (
    [in]  mdFieldDef  fd,
    [in]  ULONG       ulRVA
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0762-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0762-106">Parameters</span></span>  

 `fd`  
 <span data-ttu-id="f0762-107">中目标字段的标记。</span><span class="sxs-lookup"><span data-stu-id="f0762-107">[in] The token for the target field.</span></span>  
  
 `ulRVA`  
 <span data-ttu-id="f0762-108">中代码或数据区域的地址。</span><span class="sxs-lookup"><span data-stu-id="f0762-108">[in] The address of a code or data area.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0762-109">要求</span><span class="sxs-lookup"><span data-stu-id="f0762-109">Requirements</span></span>  

 <span data-ttu-id="f0762-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0762-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0762-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f0762-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f0762-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f0762-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f0762-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0762-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0762-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0762-114">See also</span></span>

- [<span data-ttu-id="f0762-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="f0762-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="f0762-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="f0762-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
