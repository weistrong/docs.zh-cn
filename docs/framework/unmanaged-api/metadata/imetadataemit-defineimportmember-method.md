---
description: 了解详细信息： IMetaDataEmit：:D efineImportMember 方法
title: IMetaDataEmit::DefineImportMember 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineImportMember
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineImportMember
helpviewer_keywords:
- DefineImportMember method [.NET Framework metadata]
- IMetaDataEmit::DefineImportMember method [.NET Framework metadata]
ms.assetid: c7dd94c6-335b-46ff-9dfe-505056db5673
topic_type:
- apiref
ms.openlocfilehash: 91c6ea70d38b8d4f73570ed19d86bacca30ebae5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753453"
---
# <a name="imetadataemitdefineimportmember-method"></a><span data-ttu-id="e862c-103">IMetaDataEmit::DefineImportMember 方法</span><span class="sxs-lookup"><span data-stu-id="e862c-103">IMetaDataEmit::DefineImportMember Method</span></span>

<span data-ttu-id="e862c-104">创建对在当前范围外定义的类型或模块的指定成员的引用，并定义该引用的标记。</span><span class="sxs-lookup"><span data-stu-id="e862c-104">Creates a reference to the specified member of a type or module that is defined outside the current scope, and defines a token for that reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e862c-105">语法</span><span class="sxs-lookup"><span data-stu-id="e862c-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineImportMember (
    [in]  IMetaDataAssemblyImport  *pAssemImport,
    [in]  const void               *pbHashValue,
    [in]  ULONG                    cbHashValue,  
    [in]  IMetaDataImport          *pImport,
    [in]  mdToken                  mbMember,
    [in]  IMetaDataAssemblyEmit    *pAssemEmit,
    [in]  mdToken                  tkParent,
    [out] mdMemberRef              *pmr
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e862c-106">参数</span><span class="sxs-lookup"><span data-stu-id="e862c-106">Parameters</span></span>  

 `pAssemImport`  
 <span data-ttu-id="e862c-107">中一个 [IMetaDataAssemblyImport](imetadataassemblyimport-interface.md) 接口，它表示从中导入目标成员的程序集。</span><span class="sxs-lookup"><span data-stu-id="e862c-107">[in] An [IMetaDataAssemblyImport](imetadataassemblyimport-interface.md) interface that represents the assembly from which the target member is imported.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="e862c-108">中一个数组，其中包含由指定的程序集的哈希 `pAssemImport` 。</span><span class="sxs-lookup"><span data-stu-id="e862c-108">[in] An array that contains the hash for the assembly specified by `pAssemImport`.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="e862c-109">[in] `pbHashValue` 数组中的字节数。</span><span class="sxs-lookup"><span data-stu-id="e862c-109">[in] The number of bytes in the `pbHashValue` array.</span></span>  
  
 `pImport`  
 <span data-ttu-id="e862c-110">中一个 [IMetaDataImport](imetadataimport-interface.md) 接口，表示从其导入目标成员的元数据范围。</span><span class="sxs-lookup"><span data-stu-id="e862c-110">[in] An [IMetaDataImport](imetadataimport-interface.md) interface that represents the metadata scope from which the target member is imported.</span></span>  
  
 `mbMember`  
 <span data-ttu-id="e862c-111">中指定目标成员的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e862c-111">[in] The metadata token that specifies the target member.</span></span> <span data-ttu-id="e862c-112">标记可以是 `mdMethodDef` 成员方法的 () ， `mdProperty` (成员属性) ，或 (`mdFieldDef` 标记成员字段的) 。</span><span class="sxs-lookup"><span data-stu-id="e862c-112">The token can be an `mdMethodDef` (for a member method), `mdProperty` (for a member property), or `mdFieldDef` (for a member field) token.</span></span>  
  
 `pAssemEmit`  
 <span data-ttu-id="e862c-113">中一个 [IMetaDataAssemblyEmit](imetadataassemblyemit-interface.md) 接口，该接口表示向其中导入目标成员的程序集。</span><span class="sxs-lookup"><span data-stu-id="e862c-113">[in] An [IMetaDataAssemblyEmit](imetadataassemblyemit-interface.md) interface that represents the assembly into which the target member is imported.</span></span>  
  
 `tkParent`  
 <span data-ttu-id="e862c-114">中 `mdTypeRef` `mdModuleRef` 类型或模块的或标记，分别拥有目标成员。</span><span class="sxs-lookup"><span data-stu-id="e862c-114">[in] The `mdTypeRef` or `mdModuleRef` token for the type or module, respectively, that owns the target member.</span></span>  
  
 `pmr`  
 <span data-ttu-id="e862c-115">弄 `mdMemberRef` 在成员引用的当前范围内定义的标记。</span><span class="sxs-lookup"><span data-stu-id="e862c-115">[out] The `mdMemberRef` token that is defined in the current scope for the member reference.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e862c-116">备注</span><span class="sxs-lookup"><span data-stu-id="e862c-116">Remarks</span></span>  

 <span data-ttu-id="e862c-117">`DefineImportMember`方法查找由指定的成员，该成员 `mbMember` 在指定的另一个范围内定义， `pImport` 并检索其属性。</span><span class="sxs-lookup"><span data-stu-id="e862c-117">The `DefineImportMember` method looks up the member, specified by `mbMember`, that is defined in another scope, specified by `pImport`, and retrieves its properties.</span></span> <span data-ttu-id="e862c-118">它使用此信息调用当前范围中的 [IMetaDataEmit：:D efinememberref](imetadataemit-definememberref-method.md) 方法来创建成员引用。</span><span class="sxs-lookup"><span data-stu-id="e862c-118">It uses this information to call the [IMetaDataEmit::DefineMemberRef](imetadataemit-definememberref-method.md) method in the current scope to create the member reference.</span></span>  
  
 <span data-ttu-id="e862c-119">通常，在使用方法之前， `DefineImportMember` 必须在当前作用域内为目标成员的父类、接口或模块创建类型引用或模块引用。</span><span class="sxs-lookup"><span data-stu-id="e862c-119">Generally, before you use the `DefineImportMember` method, you must create, in the current scope, a type reference or module reference for the target member's parent class, interface, or module.</span></span> <span data-ttu-id="e862c-120">然后，在参数中传递此引用的元数据标记 `tkParent` 。</span><span class="sxs-lookup"><span data-stu-id="e862c-120">The metadata token for this reference is then passed in the `tkParent` argument.</span></span> <span data-ttu-id="e862c-121">如果目标成员的父成员稍后将由编译器或链接器解析，则不需要创建对它的引用。</span><span class="sxs-lookup"><span data-stu-id="e862c-121">You do not need to create a reference to the target member's parent if it will be resolved later by the compiler or linker.</span></span> <span data-ttu-id="e862c-122">总结：</span><span class="sxs-lookup"><span data-stu-id="e862c-122">To summarize:</span></span>  
  
- <span data-ttu-id="e862c-123">如果目标成员是字段或方法，则使用 [IMetaDataEmit：:D efinetyperefbyname](imetadataemit-definetyperefbyname-method.md) 或 [IMetaDataEmit：:D efineimporttype](imetadataemit-defineimporttype-method.md) 方法为成员的父类或父接口创建类型引用（在当前范围内）。</span><span class="sxs-lookup"><span data-stu-id="e862c-123">If the target member is a field or method, use either the [IMetaDataEmit::DefineTypeRefByName](imetadataemit-definetyperefbyname-method.md) or the [IMetaDataEmit::DefineImportType](imetadataemit-defineimporttype-method.md) method to create a type reference, in the current scope, for the member's parent class or parent interface.</span></span>  
  
- <span data-ttu-id="e862c-124">如果目标成员是全局变量或全局函数 (也就是说，不是类或接口的成员) ，请使用 [IMetaDataEmit：:D efinemoduleref](imetadataemit-definemoduleref-method.md) 方法为成员的父模块创建模块引用（在当前范围内）。</span><span class="sxs-lookup"><span data-stu-id="e862c-124">If the target member is a global variable or global function (that is, not a member of a class or interface), use the [IMetaDataEmit::DefineModuleRef](imetadataemit-definemoduleref-method.md) method to create a module reference, in the current scope, for the member's parent module.</span></span>  
  
- <span data-ttu-id="e862c-125">如果目标成员的父项稍后将由编译器或链接器解析，则传入 `mdTokenNil` `tkParent` 。</span><span class="sxs-lookup"><span data-stu-id="e862c-125">If the target member's parent will be resolved later by the compiler or linker, then pass `mdTokenNil` in `tkParent`.</span></span> <span data-ttu-id="e862c-126">这种情况的唯一应用场景是从一个 .obj 文件中导入全局函数或全局变量，该文件最终将链接到当前模块和合并的元数据中。</span><span class="sxs-lookup"><span data-stu-id="e862c-126">The only scenario in which this applies is when a global function or global variable is being imported from a .obj file that will ultimately be linked into the current module and the metadata merged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e862c-127">要求</span><span class="sxs-lookup"><span data-stu-id="e862c-127">Requirements</span></span>  

 <span data-ttu-id="e862c-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e862c-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e862c-129">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e862c-129">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e862c-130">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e862c-130">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e862c-131">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e862c-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e862c-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="e862c-132">See also</span></span>

- [<span data-ttu-id="e862c-133">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="e862c-133">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="e862c-134">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="e862c-134">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
