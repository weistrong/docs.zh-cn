---
description: 了解详细信息： IMetaDataImport：： CloseEnum 方法
title: IMetaDataImport::CloseEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CloseEnum
helpviewer_keywords:
- IMetaDataImport::CloseEnum method [.NET Framework metadata]
- CloseEnum method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 727819d5-1dab-4ebb-ac25-950b4111dc72
topic_type:
- apiref
ms.openlocfilehash: b18b484cab0d9f4c0ecea21da78535c9a872bb1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677738"
---
# <a name="imetadataimportcloseenum-method"></a><span data-ttu-id="5e2bf-103">IMetaDataImport::CloseEnum 方法</span><span class="sxs-lookup"><span data-stu-id="5e2bf-103">IMetaDataImport::CloseEnum Method</span></span>

<span data-ttu-id="5e2bf-104">关闭由指定句柄标识的枚举器。</span><span class="sxs-lookup"><span data-stu-id="5e2bf-104">Closes the enumerator that is identified by the specified handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e2bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="5e2bf-105">Syntax</span></span>  
  
```cpp  
void CloseEnum (  
   [in] HCORENUM hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5e2bf-106">参数</span><span class="sxs-lookup"><span data-stu-id="5e2bf-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="5e2bf-107">中要关闭的枚举器的句柄。</span><span class="sxs-lookup"><span data-stu-id="5e2bf-107">[in] The handle for the enumerator to close.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5e2bf-108">备注</span><span class="sxs-lookup"><span data-stu-id="5e2bf-108">Remarks</span></span>  

 <span data-ttu-id="5e2bf-109">指定的句柄 `hEnum` 是从以前的 `Enum` *名称* 调用获取的 (例如， [IMetaDataImport：： EnumTypeDefs](imetadataimport-enumtypedefs-method.md)) 。</span><span class="sxs-lookup"><span data-stu-id="5e2bf-109">The handle specified by `hEnum` is obtained from a previous `Enum`*Name* call (for example, [IMetaDataImport::EnumTypeDefs](imetadataimport-enumtypedefs-method.md)).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e2bf-110">要求</span><span class="sxs-lookup"><span data-stu-id="5e2bf-110">Requirements</span></span>  

 <span data-ttu-id="5e2bf-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5e2bf-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e2bf-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5e2bf-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5e2bf-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5e2bf-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5e2bf-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e2bf-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e2bf-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="5e2bf-115">See also</span></span>

- [<span data-ttu-id="5e2bf-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="5e2bf-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="5e2bf-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="5e2bf-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
