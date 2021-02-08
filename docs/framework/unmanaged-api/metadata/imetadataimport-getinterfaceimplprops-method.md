---
description: 了解详细信息： IMetaDataImport：： GetInterfaceImplProps 方法
title: IMetaDataImport::GetInterfaceImplProps 方法
ms.date: 02/25/2019
api_name:
- IMetaDataImport.GetInterfaceImplProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetInterfaceImplProps
helpviewer_keywords:
- IMetaDataImport::GetInterfaceImplProps method [.NET Framework metadata]
- GetInterfaceImpProps method [.NET Framework metadata]
ms.assetid: be3f5985-b1e4-4036-8602-c16e8508d4af
topic_type:
- apiref
ms.openlocfilehash: 6b3c9394bcf37f700c84e1fda0b785dc0c3f4713
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783906"
---
# <a name="imetadataimportgetinterfaceimplprops-method"></a><span data-ttu-id="86b7e-103">IMetaDataImport::GetInterfaceImplProps 方法</span><span class="sxs-lookup"><span data-stu-id="86b7e-103">IMetaDataImport::GetInterfaceImplProps Method</span></span>

<span data-ttu-id="86b7e-104">获取一个指针，该指针指向实现指定方法的的元数据标记 <xref:System.Type> 和声明该方法的接口。</span><span class="sxs-lookup"><span data-stu-id="86b7e-104">Gets a pointer to the metadata tokens for the <xref:System.Type> that implements the specified method, and for the interface that declares that method.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="86b7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="86b7e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetInterfaceImplProps (  
   [in]  mdInterfaceImpl        iiImpl,  
   [out] mdTypeDef              *pClass,  
   [out] mdToken                *ptkIface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86b7e-106">参数</span><span class="sxs-lookup"><span data-stu-id="86b7e-106">Parameters</span></span>  

 `iiImpl`  
 <span data-ttu-id="86b7e-107">中表示要为其返回类和接口标记的方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="86b7e-107">[in] The metadata token representing the method to return the class and interface tokens for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="86b7e-108">弄表示实现方法的类的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="86b7e-108">[out] The metadata token representing the class that implements the method.</span></span>  
  
 `ptkIface`  
 <span data-ttu-id="86b7e-109">弄表示用于定义实现的方法的接口的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="86b7e-109">[out] The metadata token representing the interface that defines the implemented method.</span></span>  

## <a name="remarks"></a><span data-ttu-id="86b7e-110">备注</span><span class="sxs-lookup"><span data-stu-id="86b7e-110">Remarks</span></span>

 <span data-ttu-id="86b7e-111">可以 `iImpl` 通过调用 [EnumInterfaceImpls](imetadataimport-enuminterfaceimpls-method.md) 方法来获取的值。</span><span class="sxs-lookup"><span data-stu-id="86b7e-111">You obtain the value for `iImpl` by calling the [EnumInterfaceImpls](imetadataimport-enuminterfaceimpls-method.md) method.</span></span>

 <span data-ttu-id="86b7e-112">例如，假设某个类的 `mdTypeDef` 标记值为0x02000007，并且它实现了三个类型具有标记的接口：</span><span class="sxs-lookup"><span data-stu-id="86b7e-112">For example, suppose that a class has an `mdTypeDef` token value of 0x02000007 and that it implements three interfaces whose types have tokens:</span></span>

- <span data-ttu-id="86b7e-113">0x02000003 (TypeDef) </span><span class="sxs-lookup"><span data-stu-id="86b7e-113">0x02000003 (TypeDef)</span></span>
- <span data-ttu-id="86b7e-114">0x0100000A (TypeRef) </span><span class="sxs-lookup"><span data-stu-id="86b7e-114">0x0100000A (TypeRef)</span></span>
- <span data-ttu-id="86b7e-115">0x0200001C (TypeDef) </span><span class="sxs-lookup"><span data-stu-id="86b7e-115">0x0200001C (TypeDef)</span></span>

<span data-ttu-id="86b7e-116">从概念上讲，此信息存储到接口实现表中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="86b7e-116">Conceptually, this information is stored into an interface implementation table as:</span></span>

| <span data-ttu-id="86b7e-117">行号</span><span class="sxs-lookup"><span data-stu-id="86b7e-117">Row number</span></span> | <span data-ttu-id="86b7e-118">类标记</span><span class="sxs-lookup"><span data-stu-id="86b7e-118">Class token</span></span> | <span data-ttu-id="86b7e-119">接口令牌</span><span class="sxs-lookup"><span data-stu-id="86b7e-119">Interface token</span></span> |
|------------|-------------|-----------------|
| <span data-ttu-id="86b7e-120">4</span><span class="sxs-lookup"><span data-stu-id="86b7e-120">4</span></span>          |             |                 |
| <span data-ttu-id="86b7e-121">5</span><span class="sxs-lookup"><span data-stu-id="86b7e-121">5</span></span>          | <span data-ttu-id="86b7e-122">02000007</span><span class="sxs-lookup"><span data-stu-id="86b7e-122">02000007</span></span>    | <span data-ttu-id="86b7e-123">02000003</span><span class="sxs-lookup"><span data-stu-id="86b7e-123">02000003</span></span>        |
| <span data-ttu-id="86b7e-124">6</span><span class="sxs-lookup"><span data-stu-id="86b7e-124">6</span></span>          | <span data-ttu-id="86b7e-125">02000007</span><span class="sxs-lookup"><span data-stu-id="86b7e-125">02000007</span></span>    | <span data-ttu-id="86b7e-126">0100000A</span><span class="sxs-lookup"><span data-stu-id="86b7e-126">0100000A</span></span>        |
| <span data-ttu-id="86b7e-127">7</span><span class="sxs-lookup"><span data-stu-id="86b7e-127">7</span></span>          |             |                 |
| <span data-ttu-id="86b7e-128">8</span><span class="sxs-lookup"><span data-stu-id="86b7e-128">8</span></span>          | <span data-ttu-id="86b7e-129">02000007</span><span class="sxs-lookup"><span data-stu-id="86b7e-129">02000007</span></span>    | <span data-ttu-id="86b7e-130">0200001C</span><span class="sxs-lookup"><span data-stu-id="86b7e-130">0200001C</span></span>        |

<span data-ttu-id="86b7e-131">请记住，该令牌是一个4字节的值：</span><span class="sxs-lookup"><span data-stu-id="86b7e-131">Recall, the token is a 4-byte value:</span></span>

- <span data-ttu-id="86b7e-132">下3个字节保存行号或 RID。</span><span class="sxs-lookup"><span data-stu-id="86b7e-132">The lower 3 bytes hold the row number, or RID.</span></span>
- <span data-ttu-id="86b7e-133">上部字节保留标记类型– 0x09 `mdtInterfaceImpl` 。</span><span class="sxs-lookup"><span data-stu-id="86b7e-133">The upper byte holds the token type – 0x09 for `mdtInterfaceImpl`.</span></span>

<span data-ttu-id="86b7e-134">`GetInterfaceImplProps` 返回在参数中提供其标记的行中保存的信息 `iImpl` 。</span><span class="sxs-lookup"><span data-stu-id="86b7e-134">`GetInterfaceImplProps` returns the information held in the row whose token you provide in the `iImpl` argument.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="86b7e-135">要求</span><span class="sxs-lookup"><span data-stu-id="86b7e-135">Requirements</span></span>  

 <span data-ttu-id="86b7e-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="86b7e-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86b7e-137">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="86b7e-137">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="86b7e-138">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="86b7e-138">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="86b7e-139">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86b7e-139">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86b7e-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="86b7e-140">See also</span></span>

- [<span data-ttu-id="86b7e-141">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="86b7e-141">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="86b7e-142">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="86b7e-142">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
