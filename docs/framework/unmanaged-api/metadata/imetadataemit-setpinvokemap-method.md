---
description: 了解详细信息： IMetaDataEmit：： SetPinvokeMap 方法
title: IMetaDataEmit::SetPinvokeMap 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPinvokeMap
helpviewer_keywords:
- IMetaDataEmit::SetPinvokeMap method [.NET Framework metadata]
- SetPinvokeMap method [.NET Framework metadata]
ms.assetid: c6bfd574-1da3-4ba7-82f2-46ca5efcbaba
topic_type:
- apiref
ms.openlocfilehash: e50f06385b599a99454da0a9b971b00806d3140a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771842"
---
# <a name="imetadataemitsetpinvokemap-method"></a><span data-ttu-id="45b07-103">IMetaDataEmit::SetPinvokeMap 方法</span><span class="sxs-lookup"><span data-stu-id="45b07-103">IMetaDataEmit::SetPinvokeMap Method</span></span>

<span data-ttu-id="45b07-104">设置或更改方法的 PInvoke 签名的功能，由之前调用 [IMetaDataEmit：:D efinepinvokemap](imetadataemit-definepinvokemap-method.md)定义。</span><span class="sxs-lookup"><span data-stu-id="45b07-104">Sets or changes features of a method's PInvoke signature, as defined by a prior call to [IMetaDataEmit::DefinePinvokeMap](imetadataemit-definepinvokemap-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45b07-105">语法</span><span class="sxs-lookup"><span data-stu-id="45b07-105">Syntax</span></span>  
  
```cpp  
HRESULT SetPinvokeMap (
    [in]  mdToken      tk,
    [in]  DWORD        dwMappingFlags,  
    [in]  LPCWSTR      szImportName,
    [in]  mdModuleRef  mrImportDLL
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="45b07-106">参数</span><span class="sxs-lookup"><span data-stu-id="45b07-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="45b07-107">中 `mdToken` 应用映射信息的。</span><span class="sxs-lookup"><span data-stu-id="45b07-107">[in] The `mdToken` to which mapping information applies.</span></span>  
  
 `dwMappingFlags`  
 <span data-ttu-id="45b07-108">中PInvoke 用来执行映射的标志。</span><span class="sxs-lookup"><span data-stu-id="45b07-108">[in] Flags used by PInvoke to do the mapping.</span></span> <span data-ttu-id="45b07-109">这是一个值的位掩码 `CorPinvokeMap` 。</span><span class="sxs-lookup"><span data-stu-id="45b07-109">This is a bitmask of `CorPinvokeMap` values.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="45b07-110">中本机 DLL 中目标导出的名称。</span><span class="sxs-lookup"><span data-stu-id="45b07-110">[in] The name of the target export in the native DLL.</span></span>  
  
 `mrImportDLL`  
 <span data-ttu-id="45b07-111">中 `mdModuleRef` 目标非托管 DLL 的标记。</span><span class="sxs-lookup"><span data-stu-id="45b07-111">[in] The `mdModuleRef` token for the target unmanaged DLL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45b07-112">要求</span><span class="sxs-lookup"><span data-stu-id="45b07-112">Requirements</span></span>  

 <span data-ttu-id="45b07-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="45b07-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45b07-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="45b07-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="45b07-115">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="45b07-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="45b07-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45b07-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45b07-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="45b07-117">See also</span></span>

- [<span data-ttu-id="45b07-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="45b07-118">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="45b07-119">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="45b07-119">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
