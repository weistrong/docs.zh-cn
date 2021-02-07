---
description: 了解详细信息： IMetaDataImport：： GetCustomAttributeByName 方法
title: IMetaDataImport::GetCustomAttributeByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetCustomAttributeByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetCustomAttributeByName
helpviewer_keywords:
- IMetaDataImport::GetCustomAttributeByName method [.NET Framework metadata]
- GetCustomAttributeByName method [.NET Framework metadata]
ms.assetid: 909aa530-2e3b-4d0a-a38a-a2750e535d7d
topic_type:
- apiref
ms.openlocfilehash: 1a9ca5f7fe13243c01c5dbcb9f49955e9ce05c26
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745484"
---
# <a name="imetadataimportgetcustomattributebyname-method"></a><span data-ttu-id="72f2f-103">IMetaDataImport::GetCustomAttributeByName 方法</span><span class="sxs-lookup"><span data-stu-id="72f2f-103">IMetaDataImport::GetCustomAttributeByName Method</span></span>

<span data-ttu-id="72f2f-104">获取自定义特性（给定其名称和所有者）。</span><span class="sxs-lookup"><span data-stu-id="72f2f-104">Gets the custom attribute, given its name and owner.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72f2f-105">语法</span><span class="sxs-lookup"><span data-stu-id="72f2f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCustomAttributeByName (  
   [in]  mdToken          tkObj,  
   [in]  LPCWSTR          szName,  
   [out] const void       **ppData,  
   [out] ULONG            *pcbData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72f2f-106">参数</span><span class="sxs-lookup"><span data-stu-id="72f2f-106">Parameters</span></span>  

 `tkObj`  
 <span data-ttu-id="72f2f-107">中一个元数据标记，它表示拥有自定义特性的对象。</span><span class="sxs-lookup"><span data-stu-id="72f2f-107">[in] A metadata token representing the object that owns the custom attribute.</span></span>  
  
 `szName`  
 <span data-ttu-id="72f2f-108">中自定义属性的名称。</span><span class="sxs-lookup"><span data-stu-id="72f2f-108">[in] The name of the custom attribute.</span></span>  
  
 `ppData`  
 <span data-ttu-id="72f2f-109">弄一个指针，它指向作为自定义属性的值的数据数组。</span><span class="sxs-lookup"><span data-stu-id="72f2f-109">[out] A pointer to an array of data that is the value of the custom attribute.</span></span>  
  
 `pcbData`  
 <span data-ttu-id="72f2f-110">弄在 \* 中返回的数据的大小（以字节为单位） `ppData` 。</span><span class="sxs-lookup"><span data-stu-id="72f2f-110">[out] The size in bytes of the data returned in \*`ppData`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="72f2f-111">备注</span><span class="sxs-lookup"><span data-stu-id="72f2f-111">Remarks</span></span>  

 <span data-ttu-id="72f2f-112">为同一个所有者定义多个自定义属性是合法的;它们甚至可能具有相同的名称。</span><span class="sxs-lookup"><span data-stu-id="72f2f-112">It is legal to define multiple custom attributes for the same owner; they may even have the same name.</span></span> <span data-ttu-id="72f2f-113">但是， `GetCustomAttributeByName` 只返回一个实例。</span><span class="sxs-lookup"><span data-stu-id="72f2f-113">However, `GetCustomAttributeByName` returns only one instance.</span></span> <span data-ttu-id="72f2f-114"> (`GetCustomAttributeByName` 返回它遇到的第一个实例。 ) 若要查找自定义属性的所有实例，请调用 [IMetaDataImport：： EnumCustomAttributes](imetadataimport-enumcustomattributes-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="72f2f-114">(`GetCustomAttributeByName` returns the first instance that it encounters.) To find all instances of a custom attribute, call the [IMetaDataImport::EnumCustomAttributes](imetadataimport-enumcustomattributes-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72f2f-115">要求</span><span class="sxs-lookup"><span data-stu-id="72f2f-115">Requirements</span></span>  

 <span data-ttu-id="72f2f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="72f2f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72f2f-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="72f2f-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="72f2f-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="72f2f-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="72f2f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72f2f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72f2f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="72f2f-120">See also</span></span>

- [<span data-ttu-id="72f2f-121">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="72f2f-121">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="72f2f-122">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="72f2f-122">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
