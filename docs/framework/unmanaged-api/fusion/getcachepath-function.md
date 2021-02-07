---
description: 了解详细信息： GetCachePath 函数
title: GetCachePath 函数
ms.date: 03/30/2017
api_name:
- GetCachePath
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- GetCachePath
helpviewer_keywords:
- GetCachePath function [.NET Framework fusion]
ms.assetid: d977ad29-6619-42e1-b0be-bc25ea950e80
topic_type:
- apiref
ms.openlocfilehash: 4f5045d4110ca9aae33ef54eb85a2146f855e6c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761028"
---
# <a name="getcachepath-function"></a><span data-ttu-id="81518-103">GetCachePath 函数</span><span class="sxs-lookup"><span data-stu-id="81518-103">GetCachePath Function</span></span>

<span data-ttu-id="81518-104">使用指定的标志获取缓存的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="81518-104">Gets the path to the cached assembly, using the specified flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81518-105">语法</span><span class="sxs-lookup"><span data-stu-id="81518-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCachePath (  
    [in]      ASM_CACHE_FLAGS  dwCacheFlags,  
    [in]      LPWSTR           pwzCachePath,  
    [in, out] PDWORD           pcchPath  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="81518-106">参数</span><span class="sxs-lookup"><span data-stu-id="81518-106">Parameters</span></span>  

 `dwCacheFlags`  
 <span data-ttu-id="81518-107">中一个 [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) 值，该值指示缓存的程序集的源。</span><span class="sxs-lookup"><span data-stu-id="81518-107">[in] An [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) value that indicates the source of the cached assembly.</span></span>  
  
 `pwzCachePath`  
 <span data-ttu-id="81518-108">弄指向路径的返回指针。</span><span class="sxs-lookup"><span data-stu-id="81518-108">[out] The returned pointer to the path.</span></span>  
  
 `pcchPath`  
 <span data-ttu-id="81518-109">[in，out]请求的最大长度 `pwzCachePath` ，返回时为的实际长度 `pwzCachePath` 。</span><span class="sxs-lookup"><span data-stu-id="81518-109">[in, out] The requested maximum length of `pwzCachePath`, and upon return, the actual length of `pwzCachePath`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81518-110">要求</span><span class="sxs-lookup"><span data-stu-id="81518-110">Requirements</span></span>  

 <span data-ttu-id="81518-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="81518-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81518-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="81518-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="81518-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81518-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81518-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="81518-114">See also</span></span>

- [<span data-ttu-id="81518-115">ASM_CACHE_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="81518-115">ASM_CACHE_FLAGS Enumeration</span></span>](asm-cache-flags-enumeration.md)
- [<span data-ttu-id="81518-116">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="81518-116">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
