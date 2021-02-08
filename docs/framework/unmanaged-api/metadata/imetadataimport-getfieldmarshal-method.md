---
description: 了解详细信息： IMetaDataImport：： GetFieldMarshal 方法
title: IMetaDataImport::GetFieldMarshal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetFieldMarshal
helpviewer_keywords:
- GetFieldMarshal method [.NET Framework metadata]
- IMetaDataImport::GetFieldMarshal method [.NET Framework metadata]
ms.assetid: 4e2d88c6-8a3a-4fbe-900b-b4f4c06bf6bf
topic_type:
- apiref
ms.openlocfilehash: d6ca1f80a8b9bae4d9c02466042300bc3662f7c3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803511"
---
# <a name="imetadataimportgetfieldmarshal-method"></a><span data-ttu-id="0d904-103">IMetaDataImport::GetFieldMarshal 方法</span><span class="sxs-lookup"><span data-stu-id="0d904-103">IMetaDataImport::GetFieldMarshal Method</span></span>

<span data-ttu-id="0d904-104">获取一个指针，该指针指向由指定的字段元数据标记表示的字段的本机非托管类型。</span><span class="sxs-lookup"><span data-stu-id="0d904-104">Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d904-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d904-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFieldMarshal (  
   [in]  mdToken             tk,
   [out] PCCOR_SIGNATURE     *ppvNativeType,  
   [out] ULONG               *pcbNativeType
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d904-106">参数</span><span class="sxs-lookup"><span data-stu-id="0d904-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="0d904-107">中表示要为其获取互操作封送处理信息的字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="0d904-107">[in] The metadata token that represents the field to get interop marshaling information for.</span></span>  
  
 `ppvNativeType`  
 <span data-ttu-id="0d904-108">弄指向字段本地类型的元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="0d904-108">[out] A pointer to the metadata signature of the field's native type.</span></span>  
  
 `pcbNativeType`  
 <span data-ttu-id="0d904-109">弄的大小（以字节为单位） `ppvNativeType` 。</span><span class="sxs-lookup"><span data-stu-id="0d904-109">[out] The size in bytes of `ppvNativeType`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d904-110">要求</span><span class="sxs-lookup"><span data-stu-id="0d904-110">Requirements</span></span>  

 <span data-ttu-id="0d904-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0d904-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d904-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0d904-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0d904-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0d904-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0d904-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d904-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d904-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="0d904-115">See also</span></span>

- [<span data-ttu-id="0d904-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="0d904-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="0d904-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="0d904-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
