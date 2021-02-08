---
description: 了解详细信息： IMetaDataEmit：:D efineTypeDef 方法
title: IMetaDataEmit::DefineTypeDef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineTypeDef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeDef
helpviewer_keywords:
- IMetaDataEmit::DefineTypeDef method [.NET Framework metadata]
- DefineTypeDef method [.NET Framework metadata]
ms.assetid: dd11c485-be95-4b97-9cd8-68679a4fb432
topic_type:
- apiref
ms.openlocfilehash: ca0c74b8c067771e9f45a8c00639d75c9ad08de1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784029"
---
# <a name="imetadataemitdefinetypedef-method"></a><span data-ttu-id="6c0f1-103">IMetaDataEmit::DefineTypeDef 方法</span><span class="sxs-lookup"><span data-stu-id="6c0f1-103">IMetaDataEmit::DefineTypeDef Method</span></span>

<span data-ttu-id="6c0f1-104">创建公共语言运行时类型的类型定义，并获取该类型定义的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-104">Creates a type definition for a common language runtime type, and gets a metadata token for that type definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c0f1-105">语法</span><span class="sxs-lookup"><span data-stu-id="6c0f1-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineTypeDef (
    [in]  LPCWSTR     szTypeDef,
    [in]  DWORD       dwTypeDefFlags,
    [in]  mdToken     tkExtends,
    [in]  mdToken     rtkImplements[],
    [out] mdTypeDef   *ptd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6c0f1-106">参数</span><span class="sxs-lookup"><span data-stu-id="6c0f1-106">Parameters</span></span>  

 `szTypeDef`  
 <span data-ttu-id="6c0f1-107">中Unicode 中类型的名称。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-107">[in] The name of the type in Unicode.</span></span>  
  
 `dwTypeDefFlags`  
 <span data-ttu-id="6c0f1-108">[in] `TypeDef` 属性.</span><span class="sxs-lookup"><span data-stu-id="6c0f1-108">[in] `TypeDef` attributes.</span></span> <span data-ttu-id="6c0f1-109">这是一个值的位掩码 `CoreTypeAttr` 。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-109">This is a bitmask of `CoreTypeAttr` values.</span></span>  
  
 `tkExtends`  
 <span data-ttu-id="6c0f1-110">中基类的标记。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-110">[in] The token of the base class.</span></span> <span data-ttu-id="6c0f1-111">它必须是 `mdTypeDef` 或 `mdTypeRef` 令牌。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-111">It must be either an `mdTypeDef` or an `mdTypeRef` token.</span></span>  
  
 `rtkImplements`  
 <span data-ttu-id="6c0f1-112">中标记的数组，该数组指定此类或接口实现的接口。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-112">[in] An array of tokens specifying the interfaces that this class or interface implements.</span></span>  
  
 `ptd`  
 <span data-ttu-id="6c0f1-113">弄 `mdTypeDef` 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-113">[out] The `mdTypeDef` token assigned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6c0f1-114">备注</span><span class="sxs-lookup"><span data-stu-id="6c0f1-114">Remarks</span></span>  

 <span data-ttu-id="6c0f1-115">中的标志 `dwTypeDefFlags` 指定正在创建的类型是否为常规类型系统引用类型 (类或接口) 或通用类型系统值类型。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-115">A flag in `dwTypeDefFlags` specifies whether the type being created is a common type system reference type (class or interface) or a common type system value type.</span></span>  
  
 <span data-ttu-id="6c0f1-116">根据提供的参数，此方法也可以为 `mdInterfaceImpl` 此类型继承或实现的每个接口创建一条记录。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-116">Depending on the parameters supplied, this method, as a side effect, may also create an `mdInterfaceImpl` record for each interface that is inherited or implemented by this type.</span></span> <span data-ttu-id="6c0f1-117">但是，此方法不会返回这些标记中的任何一个 `mdInterfaceImpl` 。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-117">However, this method does not return any of these `mdInterfaceImpl` tokens.</span></span> <span data-ttu-id="6c0f1-118">如果客户端想要以后添加或修改 `mdInterfaceImpl` 令牌，则必须使用 `IMetaDataImport` 接口对其进行枚举。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-118">If a client wants to later add or modify an `mdInterfaceImpl` token, it must use the `IMetaDataImport` interface to enumerate them.</span></span> <span data-ttu-id="6c0f1-119">如果要使用接口的 COM 语义 `[default]` ，则应该提供默认接口作为中的第一个元素 `rtkImplements` ; 在类上设置的自定义属性将指示类具有默认接口 (默认情况下，始终假定该类是) 的类声明的第一个 `mdInterfaceImpl` 标记。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-119">If you want to use COM semantics of the `[default]` interface, you should supply the default interface as the first element in `rtkImplements`; a custom attribute set on the class will indicate that the class has a default interface (which is always assumed to be the first `mdInterfaceImpl` token declared for the class).</span></span>  
  
 <span data-ttu-id="6c0f1-120">数组的每个元素都 `rtkImplements` 包含一个 `mdTypeDef` 或 `mdTypeRef` 标记。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-120">Each element of the `rtkImplements` array holds an `mdTypeDef` or `mdTypeRef` token.</span></span> <span data-ttu-id="6c0f1-121">数组中的最后一个元素必须是 `mdTokenNil` 。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-121">The last element in the array must be `mdTokenNil`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c0f1-122">要求</span><span class="sxs-lookup"><span data-stu-id="6c0f1-122">Requirements</span></span>  

 <span data-ttu-id="6c0f1-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c0f1-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c0f1-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="6c0f1-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6c0f1-125">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="6c0f1-125">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6c0f1-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c0f1-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c0f1-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c0f1-127">See also</span></span>

- [<span data-ttu-id="6c0f1-128">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="6c0f1-128">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="6c0f1-129">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="6c0f1-129">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
