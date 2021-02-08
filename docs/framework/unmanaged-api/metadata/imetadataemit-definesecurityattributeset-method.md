---
description: 了解详细信息： IMetaDataEmit：:D efineSecurityAttributeSet 方法
title: IMetaDataEmit::DefineSecurityAttributeSet 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineSecurityAttributeSet
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet
helpviewer_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet method [.NET Framework metadata]
- DefineSecurityAttributeSet method [.NET Framework metadata]
ms.assetid: 27064ca2-4186-4433-90a7-3b297785e891
topic_type:
- apiref
ms.openlocfilehash: 3512857ca23d65389b0e150bd24234d272ddd9b6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784049"
---
# <a name="imetadataemitdefinesecurityattributeset-method"></a><span data-ttu-id="c6f41-103">IMetaDataEmit::DefineSecurityAttributeSet 方法</span><span class="sxs-lookup"><span data-stu-id="c6f41-103">IMetaDataEmit::DefineSecurityAttributeSet Method</span></span>

<span data-ttu-id="c6f41-104">创建一组安全权限，以附加到指定标记所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="c6f41-104">Creates a set of security permissions to attach to the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6f41-105">语法</span><span class="sxs-lookup"><span data-stu-id="c6f41-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineSecurityAttributeSet (
    [in]  mdToken       tkObj,
    [in]  COR_SECATTR   rSecAttrs[],
    [in]  ULONG         cSecAttrs,
    [out] ULONG         *pulErrorAttr
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c6f41-106">参数</span><span class="sxs-lookup"><span data-stu-id="c6f41-106">Parameters</span></span>  

 `tkObj`  
 <span data-ttu-id="c6f41-107">中安全信息附加到的令牌。</span><span class="sxs-lookup"><span data-stu-id="c6f41-107">[in] The token to which the security information is attached.</span></span>  
  
 `rSecAttrs`  
 <span data-ttu-id="c6f41-108">中结构的数组 `COR_SECATTR` 。</span><span class="sxs-lookup"><span data-stu-id="c6f41-108">[in] An array of `COR_SECATTR` structures.</span></span>  
  
 `cSecAttrs`  
 <span data-ttu-id="c6f41-109">中中的元素数目 `rSecAttrs` 。</span><span class="sxs-lookup"><span data-stu-id="c6f41-109">[in] The number of elements in `rSecAttrs`.</span></span>  
  
 `pulErrorAttr`  
 <span data-ttu-id="c6f41-110">弄如果该方法失败，则指定 `rSecAttrs` 引起问题的元素在中的索引。</span><span class="sxs-lookup"><span data-stu-id="c6f41-110">[out] If the method fails, specifies the index in `rSecAttrs` of the element that caused the problem.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c6f41-111">要求</span><span class="sxs-lookup"><span data-stu-id="c6f41-111">Requirements</span></span>  

 <span data-ttu-id="c6f41-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c6f41-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c6f41-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c6f41-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c6f41-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c6f41-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c6f41-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c6f41-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6f41-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6f41-116">See also</span></span>

- [<span data-ttu-id="c6f41-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="c6f41-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="c6f41-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="c6f41-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
