---
description: 了解详细信息： IMetaDataEmit：:D efinePinvokeMap 方法
title: IMetaDataEmit::DefinePinvokeMap 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefinePinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefinePinvokeMap
helpviewer_keywords:
- DefinePinvokeMap method [.NET Framework metadata]
- IMetaDataEmit::DefinePinvokeMap method [.NET Framework metadata]
ms.assetid: 03abf921-5154-4070-88fa-10b7092901fb
topic_type:
- apiref
ms.openlocfilehash: 7b0477ca603241e773a67f335da579daa2ed3d30
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784062"
---
# <a name="imetadataemitdefinepinvokemap-method"></a><span data-ttu-id="5dae4-103">IMetaDataEmit::DefinePinvokeMap 方法</span><span class="sxs-lookup"><span data-stu-id="5dae4-103">IMetaDataEmit::DefinePinvokeMap Method</span></span>

<span data-ttu-id="5dae4-104">设置指定的标记所引用的方法的 PInvoke 签名功能。</span><span class="sxs-lookup"><span data-stu-id="5dae4-104">Sets features of the PInvoke signature of the method referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5dae4-105">语法</span><span class="sxs-lookup"><span data-stu-id="5dae4-105">Syntax</span></span>  
  
```cpp  
HRESULT DefinePinvokeMap (
    [in]  mdToken            tk,
    [in]  DWORD              dwMappingFlags,
    [in]  LPCWSTR            szImportName,
    [in]  mdModuleRef        mrImportDLL
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5dae4-106">参数</span><span class="sxs-lookup"><span data-stu-id="5dae4-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="5dae4-107">中目标方法的标记。</span><span class="sxs-lookup"><span data-stu-id="5dae4-107">[in] The token for the target method.</span></span>  
  
 `dwMappingFlags`  
 <span data-ttu-id="5dae4-108">中PInvoke 用来执行映射的标志。</span><span class="sxs-lookup"><span data-stu-id="5dae4-108">[in] Flags used by PInvoke to do the mapping.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="5dae4-109">中非托管 DLL 中目标导出方法的名称。</span><span class="sxs-lookup"><span data-stu-id="5dae4-109">[in] The name of the target export method in an unmanaged DLL.</span></span>  
  
 `mrImportDLL`  
 <span data-ttu-id="5dae4-110">中目标本机 DLL 的标记。</span><span class="sxs-lookup"><span data-stu-id="5dae4-110">[in] The token for the target native DLL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5dae4-111">要求</span><span class="sxs-lookup"><span data-stu-id="5dae4-111">Requirements</span></span>  

 <span data-ttu-id="5dae4-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5dae4-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5dae4-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5dae4-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5dae4-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5dae4-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5dae4-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5dae4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5dae4-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="5dae4-116">See also</span></span>

- [<span data-ttu-id="5dae4-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="5dae4-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="5dae4-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="5dae4-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
