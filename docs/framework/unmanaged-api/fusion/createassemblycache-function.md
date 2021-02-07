---
description: 了解详细信息： CreateAssemblyCache 函数
title: CreateAssemblyCache 函数
ms.date: 03/30/2017
api_name:
- CreateAssemblyCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyCache
helpviewer_keywords:
- CreateAssemblyCache function [.NET Framework fusion]
ms.assetid: 348c7c8c-8578-46ae-97cf-480d6015c3c6
topic_type:
- apiref
ms.openlocfilehash: 1646e1d33401c557b13ae5c025f53aef48042004
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761153"
---
# <a name="createassemblycache-function"></a><span data-ttu-id="64bff-103">CreateAssemblyCache 函数</span><span class="sxs-lookup"><span data-stu-id="64bff-103">CreateAssemblyCache Function</span></span>

<span data-ttu-id="64bff-104">获取一个指针，该指针指向表示全局程序集缓存的新 [IAssemblyCache](iassemblycache-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="64bff-104">Gets a pointer to a new [IAssemblyCache](iassemblycache-interface.md) instance that represents the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64bff-105">语法</span><span class="sxs-lookup"><span data-stu-id="64bff-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateAssemblyCache (  
    [out] IAssemblyCache  **ppAsmCache,  
    [in]  DWORD           dwReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="64bff-106">参数</span><span class="sxs-lookup"><span data-stu-id="64bff-106">Parameters</span></span>  

 `ppAsmCache`  
 <span data-ttu-id="64bff-107">弄返回的 `IAssemblyCache` 指针。</span><span class="sxs-lookup"><span data-stu-id="64bff-107">[out] The returned `IAssemblyCache` pointer.</span></span>  
  
 `dwReserved`  
 <span data-ttu-id="64bff-108">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="64bff-108">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="64bff-109">`dwReserved` 必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="64bff-109">`dwReserved` must be 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64bff-110">要求</span><span class="sxs-lookup"><span data-stu-id="64bff-110">Requirements</span></span>  

 <span data-ttu-id="64bff-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="64bff-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64bff-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="64bff-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="64bff-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="64bff-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="64bff-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64bff-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64bff-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="64bff-115">See also</span></span>

- [<span data-ttu-id="64bff-116">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="64bff-116">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)
- [<span data-ttu-id="64bff-117">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="64bff-117">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
- [<span data-ttu-id="64bff-118">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="64bff-118">Global Assembly Cache</span></span>](../../app-domains/gac.md)
