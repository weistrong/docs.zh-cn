---
description: 了解详细信息： IMetaDataAssemblyEmit：： SetFileProps 方法
title: IMetaDataAssemblyEmit::SetFileProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetFileProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetFileProps
helpviewer_keywords:
- IMetaDataAssemblyEmit::SetFileProps method [.NET Framework metadata]
- SetFileProps method [.NET Framework metadata]
ms.assetid: 85667d38-611c-45a9-938d-930ac7a7b681
topic_type:
- apiref
ms.openlocfilehash: 482aa11b85eaf05d126c4fcc0d5a1aced85002d4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789302"
---
# <a name="imetadataassemblyemitsetfileprops-method"></a><span data-ttu-id="b6f87-103">IMetaDataAssemblyEmit::SetFileProps 方法</span><span class="sxs-lookup"><span data-stu-id="b6f87-103">IMetaDataAssemblyEmit::SetFileProps Method</span></span>

<span data-ttu-id="b6f87-104">修改指定的 `File` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="b6f87-104">Modifies the specified `File` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6f87-105">语法</span><span class="sxs-lookup"><span data-stu-id="b6f87-105">Syntax</span></span>  
  
```cpp  
HRESULT SetFileProps (  
    [in] mdFile        file,  
    [in] const void    *pbHashValue,
    [in] ULONG         cbHashValue,  
    [in] DWORD         dwFileFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b6f87-106">参数</span><span class="sxs-lookup"><span data-stu-id="b6f87-106">Parameters</span></span>  

 `file`  
 <span data-ttu-id="b6f87-107">中 `File` 用于指定要修改的元数据结构的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b6f87-107">[in] The metadata token that specifies the `File` metadata structure to be modified.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="b6f87-108">中指向与该文件关联的哈希数据的指针。</span><span class="sxs-lookup"><span data-stu-id="b6f87-108">[in] A pointer to the hash data associated with the file.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="b6f87-109">中的大小（以字节为单位） `pbHashValue` 。</span><span class="sxs-lookup"><span data-stu-id="b6f87-109">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwFileFlags`  
 <span data-ttu-id="b6f87-110">中 [CorFileFlags](corfileflags-enumeration.md) 值的按位组合，用于指定文件的各种属性。</span><span class="sxs-lookup"><span data-stu-id="b6f87-110">[in] A bitwise combination of [CorFileFlags](corfileflags-enumeration.md) values that specify various attributes of the file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b6f87-111">备注</span><span class="sxs-lookup"><span data-stu-id="b6f87-111">Remarks</span></span>  

 <span data-ttu-id="b6f87-112">若要创建 `File` 元数据结构，请使用 [IMetaDataAssemblyEmit：:D efinefile](imetadataassemblyemit-definefile-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b6f87-112">To create a `File` metadata structure, use the [IMetaDataAssemblyEmit::DefineFile](imetadataassemblyemit-definefile-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6f87-113">要求</span><span class="sxs-lookup"><span data-stu-id="b6f87-113">Requirements</span></span>  

 <span data-ttu-id="b6f87-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b6f87-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6f87-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b6f87-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b6f87-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b6f87-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b6f87-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6f87-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6f87-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="b6f87-118">See also</span></span>

- [<span data-ttu-id="b6f87-119">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="b6f87-119">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
