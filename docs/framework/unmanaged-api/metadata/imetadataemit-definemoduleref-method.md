---
description: 了解详细信息： IMetaDataEmit：:D efineModuleRef 方法
title: IMetaDataEmit::DefineModuleRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineModuleRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineModuleRef
helpviewer_keywords:
- DefineModuleRef method [.NET Framework metadata]
- IMetaDataEmit::DefineModuleRef method [.NET Framework metadata]
ms.assetid: f2833594-d90b-4a71-9a53-34b12470c64a
topic_type:
- apiref
ms.openlocfilehash: b5af5e458f749d2315612bbe9419f037331f8c46
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753388"
---
# <a name="imetadataemitdefinemoduleref-method"></a><span data-ttu-id="4c116-103">IMetaDataEmit::DefineModuleRef 方法</span><span class="sxs-lookup"><span data-stu-id="4c116-103">IMetaDataEmit::DefineModuleRef Method</span></span>

<span data-ttu-id="4c116-104">创建具有指定名称的模块的元数据签名。</span><span class="sxs-lookup"><span data-stu-id="4c116-104">Creates the metadata signature for a module with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c116-105">语法</span><span class="sxs-lookup"><span data-stu-id="4c116-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineModuleRef (
    [in]  LPCWSTR           szName,
    [out] mdModuleRef       *pmur
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4c116-106">参数</span><span class="sxs-lookup"><span data-stu-id="4c116-106">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="4c116-107">中其他元数据文件（通常为 DLL）的名称。</span><span class="sxs-lookup"><span data-stu-id="4c116-107">[in] The name of the other metadata file, typically a DLL.</span></span> <span data-ttu-id="4c116-108">这只是文件名。</span><span class="sxs-lookup"><span data-stu-id="4c116-108">This is the file name only.</span></span> <span data-ttu-id="4c116-109">不要使用完整路径名称。</span><span class="sxs-lookup"><span data-stu-id="4c116-109">Do not use a full path name.</span></span>  
  
 `pmur`  
 <span data-ttu-id="4c116-110">弄已分配的 `mdModuleRef` 标记。</span><span class="sxs-lookup"><span data-stu-id="4c116-110">[out] The assigned `mdModuleRef` token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4c116-111">要求</span><span class="sxs-lookup"><span data-stu-id="4c116-111">Requirements</span></span>  

 <span data-ttu-id="4c116-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4c116-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c116-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="4c116-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4c116-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="4c116-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4c116-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c116-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c116-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="4c116-116">See also</span></span>

- [<span data-ttu-id="4c116-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="4c116-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="4c116-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="4c116-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
