---
description: 了解详细信息： IMetaDataEmit：： SetModuleProps 方法
title: IMetaDataEmit::SetModuleProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetModuleProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetModuleProps
helpviewer_keywords:
- SetModuleProps method [.NET Framework metadata]
- IMetaDataEmit::SetModuleProps method [.NET Framework metadata]
ms.assetid: b74d7629-5f46-458f-8d67-2456a1e7030c
topic_type:
- apiref
ms.openlocfilehash: 0fc68a3f40871ddbb70cef885789ae7fe8ae0cba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772013"
---
# <a name="imetadataemitsetmoduleprops-method"></a><span data-ttu-id="774db-103">IMetaDataEmit::SetModuleProps 方法</span><span class="sxs-lookup"><span data-stu-id="774db-103">IMetaDataEmit::SetModuleProps Method</span></span>

<span data-ttu-id="774db-104">更新对 [IMetaDataEmit：:D efinemoduleref](imetadataemit-definemoduleref-method.md)之前调用定义的模块的引用。</span><span class="sxs-lookup"><span data-stu-id="774db-104">Updates references to a module defined by a prior call to [IMetaDataEmit::DefineModuleRef](imetadataemit-definemoduleref-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="774db-105">语法</span><span class="sxs-lookup"><span data-stu-id="774db-105">Syntax</span></span>  
  
```cpp  
HRESULT SetModuleProps (
    [in]  LPCWSTR     szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="774db-106">参数</span><span class="sxs-lookup"><span data-stu-id="774db-106">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="774db-107">中Unicode 中的模块名称。</span><span class="sxs-lookup"><span data-stu-id="774db-107">[in] The module name in Unicode.</span></span> <span data-ttu-id="774db-108">这只是文件名，而不是完整路径名称。</span><span class="sxs-lookup"><span data-stu-id="774db-108">This is the file name only and not the full path name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="774db-109">要求</span><span class="sxs-lookup"><span data-stu-id="774db-109">Requirements</span></span>  

 <span data-ttu-id="774db-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="774db-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="774db-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="774db-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="774db-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="774db-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="774db-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="774db-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="774db-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="774db-114">See also</span></span>

- [<span data-ttu-id="774db-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="774db-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="774db-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="774db-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
