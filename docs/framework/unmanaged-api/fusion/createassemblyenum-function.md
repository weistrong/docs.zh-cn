---
description: 了解详细信息： CreateAssemblyEnum 函数
title: CreateAssemblyEnum 函数
ms.date: 03/30/2017
api_name:
- CreateAssemblyEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyEnum
helpviewer_keywords:
- CreateAssemblyEnum function [.NET Framework fusion]
ms.assetid: 3506df38-6cea-42f6-946e-4287863bcfb3
topic_type:
- apiref
ms.openlocfilehash: 47177fcf0cd9e1b492fa89b9fb80c5cdaaced689
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761133"
---
# <a name="createassemblyenum-function"></a><span data-ttu-id="2be60-103">CreateAssemblyEnum 函数</span><span class="sxs-lookup"><span data-stu-id="2be60-103">CreateAssemblyEnum Function</span></span>

<span data-ttu-id="2be60-104">获取一个指针，该指针指向可使用指定的[IAssemblyName](iassemblyname-interface.md)枚举程序集中的对象的[IAssemblyEnum](iassemblyenum-interface.md)实例。</span><span class="sxs-lookup"><span data-stu-id="2be60-104">Gets a pointer to an [IAssemblyEnum](iassemblyenum-interface.md) instance that can enumerate the objects in the assembly with the specified [IAssemblyName](iassemblyname-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2be60-105">语法</span><span class="sxs-lookup"><span data-stu-id="2be60-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateAssemblyEnum (  
    [out] IAssemblyEnum  **pEnum,  
    [in]  IUnknown       *pUnkReserved,  
    [in]  IAssemblyName  *pName,  
    [in]  DWORD          dwFlags,  
    [in]  LPVOID         pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="2be60-106">参数</span><span class="sxs-lookup"><span data-stu-id="2be60-106">Parameters</span></span>  

 `pEnum`  
 <span data-ttu-id="2be60-107">弄指向包含所请求指针的内存位置的指针 `IAssemblyEnum` 。</span><span class="sxs-lookup"><span data-stu-id="2be60-107">[out] Pointer to a memory location that contains the requested `IAssemblyEnum` pointer.</span></span>  
  
 `pUnkReserved`  
 <span data-ttu-id="2be60-108">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="2be60-108">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="2be60-109">`pUnkReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="2be60-109">`pUnkReserved` must be a null reference.</span></span>  
  
 `pName`  
 <span data-ttu-id="2be60-110">中 `IAssemblyName` 请求的程序集的。</span><span class="sxs-lookup"><span data-stu-id="2be60-110">[in] The `IAssemblyName` of the requested assembly.</span></span> <span data-ttu-id="2be60-111">此名称用于筛选枚举。</span><span class="sxs-lookup"><span data-stu-id="2be60-111">This name is used to filter the enumeration.</span></span> <span data-ttu-id="2be60-112">它可以为 null，以枚举全局程序集缓存中的所有程序集。</span><span class="sxs-lookup"><span data-stu-id="2be60-112">It can be null to enumerate all assemblies in the global assembly cache.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="2be60-113">中用于修改枚举器的行为的标志。</span><span class="sxs-lookup"><span data-stu-id="2be60-113">[in] Flags for modifying the enumerator's behavior.</span></span> <span data-ttu-id="2be60-114">此参数仅包含 [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) 枚举中的一个位。</span><span class="sxs-lookup"><span data-stu-id="2be60-114">This parameter contains exactly one bit from the [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) enumeration.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="2be60-115">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="2be60-115">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="2be60-116">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="2be60-116">`pvReserved` must be a null reference.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2be60-117">备注</span><span class="sxs-lookup"><span data-stu-id="2be60-117">Remarks</span></span>  

 <span data-ttu-id="2be60-118">`dwFlags`参数只包含枚举中的一个位 `ASM_CACHE_FLAGS` 。</span><span class="sxs-lookup"><span data-stu-id="2be60-118">The `dwFlags` parameter contains exactly one bit from the `ASM_CACHE_FLAGS` enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2be60-119">要求</span><span class="sxs-lookup"><span data-stu-id="2be60-119">Requirements</span></span>  

 <span data-ttu-id="2be60-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2be60-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2be60-121">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="2be60-121">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="2be60-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2be60-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2be60-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2be60-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2be60-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="2be60-124">See also</span></span>

- [<span data-ttu-id="2be60-125">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="2be60-125">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
- [<span data-ttu-id="2be60-126">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="2be60-126">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="2be60-127">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="2be60-127">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
