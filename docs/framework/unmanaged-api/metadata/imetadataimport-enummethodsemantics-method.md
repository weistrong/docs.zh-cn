---
description: 了解详细信息： IMetaDataImport：： EnumMethodSemantics 方法
title: IMetaDataImport::EnumMethodSemantics 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethodSemantics
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethodSemantics
helpviewer_keywords:
- EnumMethodSemantics method [.NET Framework metadata]
- IMetaDataImport::EnumMethodSemantics method [.NET Framework metadata]
ms.assetid: e7e3c630-9691-46d6-94df-b5593a7bb08a
topic_type:
- apiref
ms.openlocfilehash: 9819afb2d7974e9f705c6ff665d3414eade0ab90
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728244"
---
# <a name="imetadataimportenummethodsemantics-method"></a><span data-ttu-id="21a27-103">IMetaDataImport::EnumMethodSemantics 方法</span><span class="sxs-lookup"><span data-stu-id="21a27-103">IMetaDataImport::EnumMethodSemantics Method</span></span>

<span data-ttu-id="21a27-104">枚举与指定方法相关的属性和属性更改事件。</span><span class="sxs-lookup"><span data-stu-id="21a27-104">Enumerates the properties and the property-change events to which the specified method is related.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21a27-105">语法</span><span class="sxs-lookup"><span data-stu-id="21a27-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMethodSemantics (  
   [in, out] HCORENUM    *phEnum,  
   [in]  mdMethodDef     mb,
   [out] mdToken         rEventProp[],  
   [in]  ULONG           cMax,  
   [out] ULONG           *pcEventProp  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="21a27-106">参数</span><span class="sxs-lookup"><span data-stu-id="21a27-106">Parameters</span></span>  

 `phEnum`  
 <span data-ttu-id="21a27-107">[in，out]指向枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="21a27-107">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="21a27-108">第一次调用此方法时，此值必须为 NULL。</span><span class="sxs-lookup"><span data-stu-id="21a27-108">This must be NULL for the first call of this method.</span></span>  
  
 `mb`  
 <span data-ttu-id="21a27-109">中用于限制枚举范围的 MethodDef 标记。</span><span class="sxs-lookup"><span data-stu-id="21a27-109">[in] A MethodDef token that limits the scope of the enumeration.</span></span>  
  
 `rEventProp`  
 <span data-ttu-id="21a27-110">弄用于存储事件或属性的数组。</span><span class="sxs-lookup"><span data-stu-id="21a27-110">[out] The array used to store the events or properties.</span></span>  
  
 `cMax`  
 <span data-ttu-id="21a27-111">[in] `rEventProp` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="21a27-111">[in] The maximum size of the `rEventProp` array.</span></span>  
  
 `pcEventProp`  
 <span data-ttu-id="21a27-112">弄中返回的事件或属性的数目 `rEventProp` 。</span><span class="sxs-lookup"><span data-stu-id="21a27-112">[out] The number of events or properties returned in `rEventProp`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="21a27-113">返回值</span><span class="sxs-lookup"><span data-stu-id="21a27-113">Return Value</span></span>  
  
|<span data-ttu-id="21a27-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="21a27-114">HRESULT</span></span>|<span data-ttu-id="21a27-115">说明</span><span class="sxs-lookup"><span data-stu-id="21a27-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="21a27-116">`EnumMethodSemantics` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="21a27-116">`EnumMethodSemantics` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="21a27-117">没有要枚举的事件或属性。</span><span class="sxs-lookup"><span data-stu-id="21a27-117">There are no events or properties to enumerate.</span></span> <span data-ttu-id="21a27-118">在这种情况下， `pcEventProp` 为零。</span><span class="sxs-lookup"><span data-stu-id="21a27-118">In that case, `pcEventProp` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="21a27-119">备注</span><span class="sxs-lookup"><span data-stu-id="21a27-119">Remarks</span></span>  

 <span data-ttu-id="21a27-120">很多公共语言运行时类型定义 `Changed` 与其属性相关的属性事件和 `On` *属性* `Changed` 方法。</span><span class="sxs-lookup"><span data-stu-id="21a27-120">Many common language runtime types define *Property*`Changed` events and `On`*Property*`Changed` methods related to their properties.</span></span> <span data-ttu-id="21a27-121">例如， <xref:System.Windows.Forms.Control?displayProperty=nameWithType> 类型定义 <xref:System.Windows.Forms.Control.Font%2A> 属性、 <xref:System.Windows.Forms.Control.FontChanged> 事件和 <xref:System.Windows.Forms.Control.OnFontChanged%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="21a27-121">For example, the <xref:System.Windows.Forms.Control?displayProperty=nameWithType> type defines a <xref:System.Windows.Forms.Control.Font%2A> property, a <xref:System.Windows.Forms.Control.FontChanged> event, and an <xref:System.Windows.Forms.Control.OnFontChanged%2A> method.</span></span> <span data-ttu-id="21a27-122">属性的 set 访问器方法 <xref:System.Windows.Forms.Control.Font%2A> 调用 <xref:System.Windows.Forms.Control.OnFontChanged%2A> 方法，而后者又引发了 <xref:System.Windows.Forms.Control.FontChanged> 事件。</span><span class="sxs-lookup"><span data-stu-id="21a27-122">The set accessor method of the <xref:System.Windows.Forms.Control.Font%2A> property calls <xref:System.Windows.Forms.Control.OnFontChanged%2A> method, which in turn raises the <xref:System.Windows.Forms.Control.FontChanged> event.</span></span> <span data-ttu-id="21a27-123">您将 `EnumMethodSemantics` 使用的 MethodDef 调用 <xref:System.Windows.Forms.Control.OnFontChanged%2A> 来获取对 <xref:System.Windows.Forms.Control.Font%2A> 属性和事件的引用 <xref:System.Windows.Forms.Control.FontChanged> 。</span><span class="sxs-lookup"><span data-stu-id="21a27-123">You would call `EnumMethodSemantics` using the MethodDef for <xref:System.Windows.Forms.Control.OnFontChanged%2A> to get references to the <xref:System.Windows.Forms.Control.Font%2A> property and the <xref:System.Windows.Forms.Control.FontChanged> event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21a27-124">要求</span><span class="sxs-lookup"><span data-stu-id="21a27-124">Requirements</span></span>  

 <span data-ttu-id="21a27-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="21a27-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21a27-126">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="21a27-126">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="21a27-127">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="21a27-127">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="21a27-128">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21a27-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21a27-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="21a27-129">See also</span></span>

- [<span data-ttu-id="21a27-130">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="21a27-130">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="21a27-131">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="21a27-131">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
