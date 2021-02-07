---
description: 了解详细信息： IMetaDataImport：： CountEnum 方法
title: IMetaDataImport::CountEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.CountEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CountEnum
helpviewer_keywords:
- CountEnum method [.NET Framework metadata]
- IMetaDataImport::CountEnum method [.NET Framework metadata]
ms.assetid: d1de53ad-9435-4b5f-9df7-07f21210e5b5
topic_type:
- apiref
ms.openlocfilehash: c579ef7ce440e3552ab28572fc6c96ad12d66400
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677686"
---
# <a name="imetadataimportcountenum-method"></a><span data-ttu-id="a9a7d-103">IMetaDataImport::CountEnum 方法</span><span class="sxs-lookup"><span data-stu-id="a9a7d-103">IMetaDataImport::CountEnum Method</span></span>

<span data-ttu-id="a9a7d-104">获取由指定枚举器检索的枚举中的元素数目。</span><span class="sxs-lookup"><span data-stu-id="a9a7d-104">Gets the number of elements in the enumeration that was retrieved by the specified enumerator.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9a7d-105">语法</span><span class="sxs-lookup"><span data-stu-id="a9a7d-105">Syntax</span></span>  
  
```cpp  
HRESULT CountEnum (  
   [in]  HCORENUM    hEnum,
   [out] ULONG       *pulCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9a7d-106">参数</span><span class="sxs-lookup"><span data-stu-id="a9a7d-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="a9a7d-107">中枚举器的句柄。</span><span class="sxs-lookup"><span data-stu-id="a9a7d-107">[in] The handle for the enumerator.</span></span>  
  
 `pulCount`  
 <span data-ttu-id="a9a7d-108">弄枚举的元素的数目。</span><span class="sxs-lookup"><span data-stu-id="a9a7d-108">[out] The number of elements enumerated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9a7d-109">备注</span><span class="sxs-lookup"><span data-stu-id="a9a7d-109">Remarks</span></span>  

 <span data-ttu-id="a9a7d-110">指定的句柄 `hEnum` 是从以前的 `Enum` *名称* 调用获取的 (例如， [IMetaDataImport：： EnumTypeDefs](imetadataimport-enumtypedefs-method.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a9a7d-110">The handle specified by `hEnum` is obtained from a previous `Enum`*Name* call (for example, [IMetaDataImport::EnumTypeDefs](imetadataimport-enumtypedefs-method.md)).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9a7d-111">要求</span><span class="sxs-lookup"><span data-stu-id="a9a7d-111">Requirements</span></span>  

 <span data-ttu-id="a9a7d-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9a7d-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9a7d-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a9a7d-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a9a7d-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a9a7d-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a9a7d-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9a7d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9a7d-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9a7d-116">See also</span></span>

- [<span data-ttu-id="a9a7d-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="a9a7d-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="a9a7d-118">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="a9a7d-118">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
