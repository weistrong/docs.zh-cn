---
description: 了解详细信息： IAssemblyCacheItem 接口
title: IAssemblyCacheItem 接口
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem
helpviewer_keywords:
- IAssemblyCacheItem interface [.NET Framework fusion]
ms.assetid: ccc9387a-9f44-4f4f-bf8f-0ea6d2afa21b
topic_type:
- apiref
ms.openlocfilehash: 2dcb721f6b65ecca93262f9af2ba355d94bb774d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760844"
---
# <a name="iassemblycacheitem-interface"></a><span data-ttu-id="b8ab7-103">IAssemblyCacheItem 接口</span><span class="sxs-lookup"><span data-stu-id="b8ab7-103">IAssemblyCacheItem Interface</span></span>

<span data-ttu-id="b8ab7-104">表示全局程序集缓存中的单个程序集。</span><span class="sxs-lookup"><span data-stu-id="b8ab7-104">Represents a single assembly in the global assembly cache.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b8ab7-105">方法</span><span class="sxs-lookup"><span data-stu-id="b8ab7-105">Methods</span></span>  
  
|<span data-ttu-id="b8ab7-106">方法</span><span class="sxs-lookup"><span data-stu-id="b8ab7-106">Method</span></span>|<span data-ttu-id="b8ab7-107">说明</span><span class="sxs-lookup"><span data-stu-id="b8ab7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b8ab7-108">AbortItem 方法</span><span class="sxs-lookup"><span data-stu-id="b8ab7-108">AbortItem Method</span></span>](iassemblycacheitem-abortitem-method.md)|<span data-ttu-id="b8ab7-109">允许全局程序集缓存中的程序集在发布前执行清除操作。</span><span class="sxs-lookup"><span data-stu-id="b8ab7-109">Allows the assembly in the global assembly cache to perform cleanup operations before it is released.</span></span>|  
|[<span data-ttu-id="b8ab7-110">Commit 方法</span><span class="sxs-lookup"><span data-stu-id="b8ab7-110">Commit Method</span></span>](iassemblycacheitem-commit-method.md)|<span data-ttu-id="b8ab7-111">将缓存的程序集引用提交到内存。</span><span class="sxs-lookup"><span data-stu-id="b8ab7-111">Commits the cached assembly reference to memory.</span></span>|  
|[<span data-ttu-id="b8ab7-112">CreateStream 方法</span><span class="sxs-lookup"><span data-stu-id="b8ab7-112">CreateStream Method</span></span>](iassemblycacheitem-createstream-method.md)|<span data-ttu-id="b8ab7-113">创建具有指定名称和格式的流。</span><span class="sxs-lookup"><span data-stu-id="b8ab7-113">Creates a stream with the specified name and format.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b8ab7-114">要求</span><span class="sxs-lookup"><span data-stu-id="b8ab7-114">Requirements</span></span>  

 <span data-ttu-id="b8ab7-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8ab7-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8ab7-116">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="b8ab7-116">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="b8ab7-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8ab7-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8ab7-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8ab7-118">See also</span></span>

- [<span data-ttu-id="b8ab7-119">合成接口</span><span class="sxs-lookup"><span data-stu-id="b8ab7-119">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="b8ab7-120">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="b8ab7-120">Global Assembly Cache</span></span>](../../app-domains/gac.md)
- [<span data-ttu-id="b8ab7-121">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="b8ab7-121">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)
