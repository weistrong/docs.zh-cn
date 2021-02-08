---
description: 了解详细信息： CorGenericParamAttr 枚举
title: CorGenericParamAttr 枚举
ms.date: 03/30/2017
api_name:
- CorGenericParamAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorGenericParamAttr
helpviewer_keywords:
- CorGenericParamAttr enumeration [.NET Framework metadata]
ms.assetid: 36c76266-71d8-48dc-bd89-54943fa659c1
topic_type:
- apiref
ms.openlocfilehash: 8fe8cb20834ecbc5477bbe8b01bf77d6b1af0eea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784452"
---
# <a name="corgenericparamattr-enumeration"></a><span data-ttu-id="6a197-103">CorGenericParamAttr 枚举</span><span class="sxs-lookup"><span data-stu-id="6a197-103">CorGenericParamAttr Enumeration</span></span>

<span data-ttu-id="6a197-104">包含描述 <xref:System.Type> 泛型类型参数的值，这些值在对 [IMetaDataEmit2：:D efinegenericparam](imetadataemit2-definegenericparam-method.md)的调用中使用。</span><span class="sxs-lookup"><span data-stu-id="6a197-104">Contains values that describe the <xref:System.Type> parameters for generic types, as used in calls to [IMetaDataEmit2::DefineGenericParam](imetadataemit2-definegenericparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a197-105">语法</span><span class="sxs-lookup"><span data-stu-id="6a197-105">Syntax</span></span>  
  
```cpp  
typedef enum CorGenericParamAttr {  
  
    gpVarianceMask                     =   0x0003,  
    gpNonVariant                       =   0x0000,
    gpCovariant                        =   0x0001,  
    gpContravariant                    =   0x0002,  
  
    gpSpecialConstraintMask            =   0x001C,  
    gpNoSpecialConstraint              =   0x0000,  
    gpReferenceTypeConstraint          =   0x0004,
    gpNotNullableValueTypeConstraint   =   0x0008,  
    gpDefaultConstructorConstraint     =   0x0010  
  
} CorGenericParamAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="6a197-106">成员</span><span class="sxs-lookup"><span data-stu-id="6a197-106">Members</span></span>  
  
|<span data-ttu-id="6a197-107">成员</span><span class="sxs-lookup"><span data-stu-id="6a197-107">Member</span></span>|<span data-ttu-id="6a197-108">说明</span><span class="sxs-lookup"><span data-stu-id="6a197-108">Description</span></span>|  
|------------|-----------------|  
|`gpVarianceMask`|<span data-ttu-id="6a197-109">参数变体仅适用于接口和委托的泛型参数。</span><span class="sxs-lookup"><span data-stu-id="6a197-109">Parameter variance applies only to generic parameters for interfaces and delegates.</span></span>|  
|`gpNonVariant`|<span data-ttu-id="6a197-110">指示缺少方差。</span><span class="sxs-lookup"><span data-stu-id="6a197-110">Indicates the absence of variance.</span></span>|  
|`gpCovariant`|<span data-ttu-id="6a197-111">指示协方差。</span><span class="sxs-lookup"><span data-stu-id="6a197-111">Indicates covariance.</span></span>|  
|`gpContravariant`|<span data-ttu-id="6a197-112">指示逆变。</span><span class="sxs-lookup"><span data-stu-id="6a197-112">Indicates contravariance.</span></span>|  
|`gpSpecialConstraintMask`|<span data-ttu-id="6a197-113">特殊约束可应用于任何 <xref:System.Type> 参数。</span><span class="sxs-lookup"><span data-stu-id="6a197-113">Special constraints can apply to any <xref:System.Type> parameter.</span></span>|  
|`gpNoSpecialConstraint`|<span data-ttu-id="6a197-114">指示没有约束适用于 <xref:System.Type> 参数。</span><span class="sxs-lookup"><span data-stu-id="6a197-114">Indicates that no constraint applies to the <xref:System.Type> parameter.</span></span>|  
|`gpReferenceTypeConstraint`|<span data-ttu-id="6a197-115">指示 <xref:System.Type> 参数必须为引用类型。</span><span class="sxs-lookup"><span data-stu-id="6a197-115">Indicates that the <xref:System.Type> parameter must be a reference type.</span></span>|  
|`gpNotNullableValueTypeConstraint`|<span data-ttu-id="6a197-116">指示 <xref:System.Type> 参数必须是不能为 null 值的值类型。</span><span class="sxs-lookup"><span data-stu-id="6a197-116">Indicates that the <xref:System.Type> parameter must be a value type that cannot be a null value.</span></span>|  
|`gpDefaultConstructorConstraint`|<span data-ttu-id="6a197-117">指示 <xref:System.Type> 参数必须包含不带任何参数的默认公共构造函数。</span><span class="sxs-lookup"><span data-stu-id="6a197-117">Indicates that the <xref:System.Type> parameter must have a default public constructor that takes no parameters.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6a197-118">要求</span><span class="sxs-lookup"><span data-stu-id="6a197-118">Requirements</span></span>  

 <span data-ttu-id="6a197-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6a197-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a197-120">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="6a197-120">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="6a197-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a197-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a197-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="6a197-122">See also</span></span>

- [<span data-ttu-id="6a197-123">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="6a197-123">Metadata Enumerations</span></span>](metadata-enumerations.md)
