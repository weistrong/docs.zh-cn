---
description: 了解详细信息： IMetaDataEmit：： SetClassLayout 方法
title: IMetaDataEmit::SetClassLayout 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetClassLayout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetClassLayout
helpviewer_keywords:
- IMetaDataEmit::SetClassLayout method [.NET Framework metadata]
- SetClassLayout method [.NET Framework metadata]
ms.assetid: 2576c449-388d-4434-a0e1-9f53991e11b6
topic_type:
- apiref
ms.openlocfilehash: e0ce8e93137b9a32a13ca86ead539385523fa8a3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706599"
---
# <a name="imetadataemitsetclasslayout-method"></a><span data-ttu-id="42c6d-103">IMetaDataEmit::SetClassLayout 方法</span><span class="sxs-lookup"><span data-stu-id="42c6d-103">IMetaDataEmit::SetClassLayout Method</span></span>

<span data-ttu-id="42c6d-104">完成先前对 [DefineTypeDef 方法](imetadataemit-definetypedef-method.md)的调用所定义的类的字段布局。</span><span class="sxs-lookup"><span data-stu-id="42c6d-104">Completes the layout of fields for a class that has been defined by a prior call to [DefineTypeDef Method](imetadataemit-definetypedef-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42c6d-105">语法</span><span class="sxs-lookup"><span data-stu-id="42c6d-105">Syntax</span></span>  
  
```cpp  
HRESULT SetClassLayout (  
    [in]  mdTypeDef           td,
    [in]  DWORD               dwPackSize,
    [in]  COR_FIELD_OFFSET    rFieldOffsets[],
    [in]  ULONG               ulClassSize
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="42c6d-106">参数</span><span class="sxs-lookup"><span data-stu-id="42c6d-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="42c6d-107">中一个 `mdTypeDef` 标记，该标记指定要布局的类。</span><span class="sxs-lookup"><span data-stu-id="42c6d-107">[in] An `mdTypeDef` token that specifies the class to be laid out.</span></span>  
  
 `dwPackSize`  
 <span data-ttu-id="42c6d-108">中封装大小为1、2、4、8或16字节。</span><span class="sxs-lookup"><span data-stu-id="42c6d-108">[in] The packing size: 1, 2, 4, 8 or 16 bytes.</span></span> <span data-ttu-id="42c6d-109">包装大小是相邻字段之间的字节数。</span><span class="sxs-lookup"><span data-stu-id="42c6d-109">The packing size is the number of bytes between adjacent fields.</span></span>  
  
 `rFieldOffsets`  
 <span data-ttu-id="42c6d-110">中 [COR_FIELD_OFFSET](cor-field-offset-structure.md) 结构的数组，其中每个结构都指定了类的字段和字段在类中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="42c6d-110">[in] An array of [COR_FIELD_OFFSET](cor-field-offset-structure.md) structures, each of which specifies a field of the class and the field's offset within the class.</span></span> <span data-ttu-id="42c6d-111">用终止数组 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="42c6d-111">Terminate the array with `mdTokenNil`.</span></span>  
  
 `ulClassSize`  
 <span data-ttu-id="42c6d-112">中类的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="42c6d-112">[in] The size, in bytes, of the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="42c6d-113">备注</span><span class="sxs-lookup"><span data-stu-id="42c6d-113">Remarks</span></span>  

 <span data-ttu-id="42c6d-114">该类最初是通过以下方式定义的：调用 [IMetaDataEmit：:D efinetypedef](imetadataemit-definetypedef-method.md) 方法，并为类的字段指定三种布局之一：自动、顺序或显式。</span><span class="sxs-lookup"><span data-stu-id="42c6d-114">The class is initially defined by calling the [IMetaDataEmit::DefineTypeDef](imetadataemit-definetypedef-method.md) method, and specifying one of three layouts for the fields of the class: automatic, sequential, or explicit.</span></span> <span data-ttu-id="42c6d-115">通常，您将使用自动布局，并让运行时选择对字段进行布局的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="42c6d-115">Normally, you would use automatic layout and let the runtime choose the best way to lay out the fields.</span></span>  
  
 <span data-ttu-id="42c6d-116">不过，您可能希望根据非托管代码使用的排列方式来排列字段。</span><span class="sxs-lookup"><span data-stu-id="42c6d-116">However, you might want the fields laid out according to the arrangement that unmanaged code uses.</span></span> <span data-ttu-id="42c6d-117">在这种情况下，请选择 "顺序" 或 "显式布局" 并调用 `SetClassLayout` 来完成字段的布局：</span><span class="sxs-lookup"><span data-stu-id="42c6d-117">In this case, choose either sequential or explicit layout and call `SetClassLayout` to complete the layout of the fields:</span></span>  
  
- <span data-ttu-id="42c6d-118">顺序布局：指定包装大小。</span><span class="sxs-lookup"><span data-stu-id="42c6d-118">Sequential layout: Specify the packing size.</span></span> <span data-ttu-id="42c6d-119">字段根据其自然大小或包装大小对齐，以较小的字段偏移量为准。</span><span class="sxs-lookup"><span data-stu-id="42c6d-119">A field is aligned according to either its natural size or the packing size, whichever results in the smaller offset of the field.</span></span> <span data-ttu-id="42c6d-120">将 `rFieldOffsets` 和设置 `ulClassSize` 为零。</span><span class="sxs-lookup"><span data-stu-id="42c6d-120">Set `rFieldOffsets` and `ulClassSize` to zero.</span></span>  
  
- <span data-ttu-id="42c6d-121">显式布局：指定每个字段的偏移量，或指定类大小和包装大小。</span><span class="sxs-lookup"><span data-stu-id="42c6d-121">Explicit layout: Either specify the offset of each field or specify the class size and the packing size.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="42c6d-122">要求</span><span class="sxs-lookup"><span data-stu-id="42c6d-122">Requirements</span></span>  

 <span data-ttu-id="42c6d-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="42c6d-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42c6d-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="42c6d-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="42c6d-125">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="42c6d-125">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="42c6d-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42c6d-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42c6d-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="42c6d-127">See also</span></span>

- [<span data-ttu-id="42c6d-128">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="42c6d-128">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="42c6d-129">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="42c6d-129">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
