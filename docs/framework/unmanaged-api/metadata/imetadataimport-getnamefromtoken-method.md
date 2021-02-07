---
description: 了解详细信息： IMetaDataImport：： GetNameFromToken 方法
title: IMetaDataImport::GetNameFromToken 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNameFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNameFromToken
helpviewer_keywords:
- GetNameFromToken method [.NET Framework metadata]
- IMetaDataImport::GetNameFromToken method [.NET Framework metadata]
ms.assetid: 32114ecf-8916-4ab2-a201-179c017344f1
topic_type:
- apiref
ms.openlocfilehash: 6195020a2b291a47e908b257896bdba64b0a40d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720847"
---
# <a name="imetadataimportgetnamefromtoken-method"></a><span data-ttu-id="28db3-103">IMetaDataImport::GetNameFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="28db3-103">IMetaDataImport::GetNameFromToken Method</span></span>

<span data-ttu-id="28db3-104">获取指定的元数据标记所引用的对象的 UTF-8 名称。</span><span class="sxs-lookup"><span data-stu-id="28db3-104">Gets the UTF-8 name of the object referenced by the specified metadata token.</span></span> <span data-ttu-id="28db3-105">此方法已过时。</span><span class="sxs-lookup"><span data-stu-id="28db3-105">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28db3-106">语法</span><span class="sxs-lookup"><span data-stu-id="28db3-106">Syntax</span></span>  
  
```cpp  
HRESULT GetNameFromToken (  
   [in] mdToken      tk,  
   [out] MDUTF8CSTR  *pszUtf8NamePtr  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="28db3-107">参数</span><span class="sxs-lookup"><span data-stu-id="28db3-107">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="28db3-108">中表示要为其返回名称的对象的标记。</span><span class="sxs-lookup"><span data-stu-id="28db3-108">[in] The token representing the object to return the name for.</span></span>  
  
 `pszUtf8NamePtr`  
 <span data-ttu-id="28db3-109">弄指向堆中 UTF-8 对象名称的指针。</span><span class="sxs-lookup"><span data-stu-id="28db3-109">[out] A pointer to the UTF-8 object name in the heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="28db3-110">备注</span><span class="sxs-lookup"><span data-stu-id="28db3-110">Remarks</span></span>  

 <span data-ttu-id="28db3-111">`GetNameFromToken` 已过时。</span><span class="sxs-lookup"><span data-stu-id="28db3-111">`GetNameFromToken` is obsolete.</span></span> <span data-ttu-id="28db3-112">作为替代方法，可以调用方法来获取所需的特定类型的标记的属性，例如 `GetFieldProps` 为字段或方法提供 `GetMethodProps` 。</span><span class="sxs-lookup"><span data-stu-id="28db3-112">As an alternative, call a method to get the properties of the particular type of token required, such as `GetFieldProps` for a field or `GetMethodProps` for a method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28db3-113">要求</span><span class="sxs-lookup"><span data-stu-id="28db3-113">Requirements</span></span>  

 <span data-ttu-id="28db3-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28db3-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28db3-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="28db3-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="28db3-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="28db3-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="28db3-117">**.NET Framework 版本：** 1。0</span><span class="sxs-lookup"><span data-stu-id="28db3-117">**.NET Framework Versions:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28db3-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="28db3-118">See also</span></span>

- [<span data-ttu-id="28db3-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="28db3-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="28db3-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="28db3-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
