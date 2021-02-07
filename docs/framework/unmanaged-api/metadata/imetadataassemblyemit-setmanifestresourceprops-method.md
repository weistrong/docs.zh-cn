---
description: 了解详细信息： IMetaDataAssemblyEmit：： SetManifestResourceProps 方法
title: IMetaDataAssemblyEmit::SetManifestResourceProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetManifestResourceProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetManifestResourceProps
helpviewer_keywords:
- SetManifestResourceProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetManifestResourceProps method [.NET Framework metadata]
ms.assetid: ef77efd1-849c-4e51-ba92-7ee3d2bf0339
topic_type:
- apiref
ms.openlocfilehash: 0d5022c4acc562f9e77cec4ba080815db410862b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721016"
---
# <a name="imetadataassemblyemitsetmanifestresourceprops-method"></a><span data-ttu-id="9e4a4-103">IMetaDataAssemblyEmit::SetManifestResourceProps 方法</span><span class="sxs-lookup"><span data-stu-id="9e4a4-103">IMetaDataAssemblyEmit::SetManifestResourceProps Method</span></span>

<span data-ttu-id="9e4a4-104">修改指定的 `ManifestResource` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-104">Modifies the specified `ManifestResource` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e4a4-105">语法</span><span class="sxs-lookup"><span data-stu-id="9e4a4-105">Syntax</span></span>  
  
```cpp  
HRESULT SetManifestResourceProps (  
    [in] mdManifestResource  mr,  
    [in] mdToken             tkImplementation,
    [in] DWORD               dwOffset,  
    [in] DWORD               dwResourceFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9e4a4-106">参数</span><span class="sxs-lookup"><span data-stu-id="9e4a4-106">Parameters</span></span>  

 `mr`  
 <span data-ttu-id="9e4a4-107">中 `ManifestResource` 用于指定要修改的元数据结构的标记。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-107">[in] The token that specifies the `ManifestResource` metadata structure to be modified.</span></span>  
  
 `tkImplementation`  
 <span data-ttu-id="9e4a4-108">中 `File` `AssemblyRef` 映射到资源提供程序的标记，类型为或。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-108">[in] The token, of type `File` or `AssemblyRef`, that maps to the resource provider.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="9e4a4-109">中文件中资源的起始位置的偏移量。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-109">[in] The offset to the beginning of the resource within the file.</span></span>  
  
 `dwResourceFlags`  
 <span data-ttu-id="9e4a4-110">中指定资源特性的标志值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-110">[in] A bitwise combination of flag values that specify the attributes of the resource.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9e4a4-111">备注</span><span class="sxs-lookup"><span data-stu-id="9e4a4-111">Remarks</span></span>  

 <span data-ttu-id="9e4a4-112">若要创建 `ManifestResource` 元数据结构，请使用 [IMetaDataAssemblyEmit：:D efinemanifestresource](imetadataassemblyemit-definemanifestresource-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-112">To create a `ManifestResource` metadata structure, use the [IMetaDataAssemblyEmit::DefineManifestResource](imetadataassemblyemit-definemanifestresource-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9e4a4-113">要求</span><span class="sxs-lookup"><span data-stu-id="9e4a4-113">Requirements</span></span>  

 <span data-ttu-id="9e4a4-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9e4a4-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9e4a4-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9e4a4-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9e4a4-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9e4a4-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9e4a4-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9e4a4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e4a4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="9e4a4-118">See also</span></span>

- [<span data-ttu-id="9e4a4-119">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="9e4a4-119">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
