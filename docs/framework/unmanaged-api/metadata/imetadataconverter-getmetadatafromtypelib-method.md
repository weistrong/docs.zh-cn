---
description: 了解详细信息： IMetaDataConverter：： GetMetaDataFromTypeLib 方法
title: IMetaDataConverter::GetMetaDataFromTypeLib 方法
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetMetaDataFromTypeLib
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetMetaDataFromTypeLib
helpviewer_keywords:
- IMetaDataConverter::GetMetaDataFromTypeLib method [.NET Framework metadata]
- GetMetaDataFromTypeLib method [.NET Framework metadata]
ms.assetid: 97dc3a56-adfa-431f-889e-06a35ac84d51
topic_type:
- apiref
ms.openlocfilehash: d1ed5feb9f42ea0f8dc802c4dad527be5d2ed25f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789276"
---
# <a name="imetadataconvertergetmetadatafromtypelib-method"></a><span data-ttu-id="7d564-103">IMetaDataConverter::GetMetaDataFromTypeLib 方法</span><span class="sxs-lookup"><span data-stu-id="7d564-103">IMetaDataConverter::GetMetaDataFromTypeLib Method</span></span>

<span data-ttu-id="7d564-104">获取一个接口指针，该指针指向表示由指定的实例表示的类型库的元数据签名的 [IMetaDataImport](imetadataimport-interface.md) 实例 `ITypeLib` 。</span><span class="sxs-lookup"><span data-stu-id="7d564-104">Gets an interface pointer to an [IMetaDataImport](imetadataimport-interface.md) instance that represents the metadata signature of the type library represented by the specified `ITypeLib` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d564-105">语法</span><span class="sxs-lookup"><span data-stu-id="7d564-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaDataFromTypeLib (  
    [in]  ITypeLib        *pITL,
    [out] IMetaDataImport **ppMDI  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d564-106">参数</span><span class="sxs-lookup"><span data-stu-id="7d564-106">Parameters</span></span>  

 `pITL`  
 <span data-ttu-id="7d564-107">中一个指针，指向 `ITypeLib` 表示类型库的对象。</span><span class="sxs-lookup"><span data-stu-id="7d564-107">[in] Pointer to an `ITypeLib` object that represents the type library.</span></span>  
  
 `ppMDI`  
 <span data-ttu-id="7d564-108">弄指向一个位置的指针，该位置接收 `IMetaDataImport` 表示元数据签名的实例的地址。</span><span class="sxs-lookup"><span data-stu-id="7d564-108">[out] Pointer to a location that receives the address of the `IMetaDataImport` instance that represents the metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d564-109">要求</span><span class="sxs-lookup"><span data-stu-id="7d564-109">Requirements</span></span>  

 <span data-ttu-id="7d564-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7d564-110">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d564-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="7d564-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7d564-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="7d564-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7d564-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d564-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d564-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="7d564-114">See also</span></span>

- [<span data-ttu-id="7d564-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="7d564-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="7d564-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="7d564-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
