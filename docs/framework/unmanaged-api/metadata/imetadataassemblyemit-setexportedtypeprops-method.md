---
description: 了解详细信息： IMetaDataAssemblyEmit：： SetExportedTypeProps 方法
title: IMetaDataAssemblyEmit::SetExportedTypeProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetExportedTypeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetExportedTypeProps
helpviewer_keywords:
- SetExportedTypeProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetExportedTypeProps method [.NET Framework metadata]
ms.assetid: 1c090153-fd5f-46c7-9cff-39a78d992c8f
topic_type:
- apiref
ms.openlocfilehash: 61032abd7b049af29c583e9aee126184af3c78f2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678089"
---
# <a name="imetadataassemblyemitsetexportedtypeprops-method"></a><span data-ttu-id="c333b-103">IMetaDataAssemblyEmit::SetExportedTypeProps 方法</span><span class="sxs-lookup"><span data-stu-id="c333b-103">IMetaDataAssemblyEmit::SetExportedTypeProps Method</span></span>

<span data-ttu-id="c333b-104">修改指定的 `ExportedType` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="c333b-104">Modifies the specified `ExportedType` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c333b-105">语法</span><span class="sxs-lookup"><span data-stu-id="c333b-105">Syntax</span></span>  
  
```cpp  
HRESULT SetExportedTypeProps (  
    [in] mdExportedType   ct,
    [in] mdToken          tkImplementation,  
    [in] mdTypeDef        tkTypeDef,  
    [in] DWORD            dwExportedTypeFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c333b-106">参数</span><span class="sxs-lookup"><span data-stu-id="c333b-106">Parameters</span></span>  

 `ct`  
 <span data-ttu-id="c333b-107">中 `ExportedType` 用于指定要修改的元数据结构的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c333b-107">[in] The metadata token that specifies the `ExportedType` metadata structure to be modified.</span></span>  
  
 `tkImplementation`  
 <span data-ttu-id="c333b-108">中类型 `File` 为、或的标记， `AssemblyRef` `ExportedType` 用于指定如何实现此类型。</span><span class="sxs-lookup"><span data-stu-id="c333b-108">[in] The token, of type `File`, `AssemblyRef`, or `ExportedType`, that specifies how this type is implemented.</span></span>  
  
 `tkTypeDef`  
 <span data-ttu-id="c333b-109">中 `TypeDef` 在代码文件中引用的标记。</span><span class="sxs-lookup"><span data-stu-id="c333b-109">[in] The `TypeDef` token referenced in the code file.</span></span>  
  
 `dwExportedTypeFlags`  
 <span data-ttu-id="c333b-110">中值的按位组合，用于指定类型的特性。</span><span class="sxs-lookup"><span data-stu-id="c333b-110">[in] A bitwise combination of values that specify attributes of the type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c333b-111">备注</span><span class="sxs-lookup"><span data-stu-id="c333b-111">Remarks</span></span>  

 <span data-ttu-id="c333b-112">若要创建 `ExportedType` 元数据结构，请使用 [IMetaDataAssemblyEmit：:D efineexportedtype](imetadataassemblyemit-defineexportedtype-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c333b-112">To create an `ExportedType` metadata structure, use the [IMetaDataAssemblyEmit::DefineExportedType](imetadataassemblyemit-defineexportedtype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c333b-113">要求</span><span class="sxs-lookup"><span data-stu-id="c333b-113">Requirements</span></span>  

 <span data-ttu-id="c333b-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c333b-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c333b-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c333b-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c333b-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c333b-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c333b-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c333b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c333b-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="c333b-118">See also</span></span>

- [<span data-ttu-id="c333b-119">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="c333b-119">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
