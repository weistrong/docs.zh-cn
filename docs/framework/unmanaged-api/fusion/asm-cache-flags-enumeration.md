---
description: 了解详细信息： ASM_CACHE_FLAGS 枚举
title: ASM_CACHE_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- ASM_CACHE_FLAGS
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- ASM_CACHE_FLAGS
helpviewer_keywords:
- ASM_CACHE_FLAGS enumeration [.NET Framework fusion]
ms.assetid: 82e9a7da-321b-48b8-b239-52eaffda6be8
topic_type:
- apiref
ms.openlocfilehash: 866f61d2960074495ed036e3a8e89ebceec74e87
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761429"
---
# <a name="asm_cache_flags-enumeration"></a><span data-ttu-id="ce614-103">ASM_CACHE_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="ce614-103">ASM_CACHE_FLAGS Enumeration</span></span>

<span data-ttu-id="ce614-104">指示由全局程序集缓存中的 [IAssemblyCacheItem](iassemblycacheitem-interface.md) 表示的程序集的源。</span><span class="sxs-lookup"><span data-stu-id="ce614-104">Indicates the source of an assembly that is represented by [IAssemblyCacheItem](iassemblycacheitem-interface.md) in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce614-105">语法</span><span class="sxs-lookup"><span data-stu-id="ce614-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    ASM_CACHE_ZAP       = 0x01,  
    ASM_CACHE_GAC       = 0x02,  
    ASM_CACHE_DOWNLOAD  = 0x04,  
    ASM_CACHE_ROOT      = 0x08,  
    ASM_CACHE_ROOT_EX   = 0x80  
} ASM_CACHE_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="ce614-106">成员</span><span class="sxs-lookup"><span data-stu-id="ce614-106">Members</span></span>  
  
|<span data-ttu-id="ce614-107">成员</span><span class="sxs-lookup"><span data-stu-id="ce614-107">Member</span></span>|<span data-ttu-id="ce614-108">说明</span><span class="sxs-lookup"><span data-stu-id="ce614-108">Description</span></span>|  
|------------|-----------------|  
|`ASM_CACHE_ZAP`|<span data-ttu-id="ce614-109">使用 Ngen.exe 枚举预编译的程序集的缓存。</span><span class="sxs-lookup"><span data-stu-id="ce614-109">Enumerates the cache of precompiled assemblies by using Ngen.exe.</span></span>|  
|`ASM_CACHE_GAC`|<span data-ttu-id="ce614-110">枚举全局程序集缓存。</span><span class="sxs-lookup"><span data-stu-id="ce614-110">Enumerates the global assembly cache.</span></span>|  
|`ASM_CACHE_DOWNLOAD`|<span data-ttu-id="ce614-111">枚举已按需下载或已进行卷影复制的程序集。</span><span class="sxs-lookup"><span data-stu-id="ce614-111">Enumerates the assemblies that have been downloaded on demand or that have been shadow-copied.</span></span>|  
|`ASM_CACHE_ROOT`|<span data-ttu-id="ce614-112">指示 [GetCachePath](getcachepath-function.md) 函数应返回公共语言运行时 (CLR) 版本2.0 的全局程序集缓存的路径。</span><span class="sxs-lookup"><span data-stu-id="ce614-112">Indicates that the [GetCachePath](getcachepath-function.md) function should return the path to the global assembly cache for the common language runtime (CLR) version 2.0.</span></span> <span data-ttu-id="ce614-113">仅在对 [GetCachePath](getcachepath-function.md)的调用上下文中有意义。</span><span class="sxs-lookup"><span data-stu-id="ce614-113">Meaningful only in the context of a call to [GetCachePath](getcachepath-function.md).</span></span>|  
|`ASM_CACHE_ROOT_EX`|<span data-ttu-id="ce614-114">指示 [GetCachePath](getcachepath-function.md) 函数应返回 CLR 版本4的全局程序集缓存的路径。</span><span class="sxs-lookup"><span data-stu-id="ce614-114">Indicates that the [GetCachePath](getcachepath-function.md) function should return the path to the global assembly cache for CLR version 4.</span></span> <span data-ttu-id="ce614-115">仅在对 [GetCachePath](getcachepath-function.md)的调用上下文中有意义。</span><span class="sxs-lookup"><span data-stu-id="ce614-115">Meaningful only in the context of a call to [GetCachePath](getcachepath-function.md).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ce614-116">要求</span><span class="sxs-lookup"><span data-stu-id="ce614-116">Requirements</span></span>  

 <span data-ttu-id="ce614-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ce614-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce614-118">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="ce614-118">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="ce614-119">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ce614-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ce614-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce614-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce614-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="ce614-121">See also</span></span>

- [<span data-ttu-id="ce614-122">GetCachePath 函数</span><span class="sxs-lookup"><span data-stu-id="ce614-122">GetCachePath Function</span></span>](getcachepath-function.md)
- [<span data-ttu-id="ce614-123">IAssemblyCacheItem 接口</span><span class="sxs-lookup"><span data-stu-id="ce614-123">IAssemblyCacheItem Interface</span></span>](iassemblycacheitem-interface.md)
- [<span data-ttu-id="ce614-124">合成枚举</span><span class="sxs-lookup"><span data-stu-id="ce614-124">Fusion Enumerations</span></span>](fusion-enumerations.md)
