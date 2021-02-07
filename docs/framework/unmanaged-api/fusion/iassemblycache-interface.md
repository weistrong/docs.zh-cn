---
description: 了解详细信息： IAssemblyCache 接口
title: IAssemblyCache 接口
ms.date: 03/30/2017
api_name:
- IAssemblyCache
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache
helpviewer_keywords:
- IAssemblyCache interface [.NET Framework fusion]
ms.assetid: 71ea170f-872d-4fc5-81b6-27da1dec9b19
topic_type:
- apiref
ms.openlocfilehash: 29c042fc101180085a697e02376b91b0e1ffd19f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760922"
---
# <a name="iassemblycache-interface"></a><span data-ttu-id="fa5f6-103">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="fa5f6-103">IAssemblyCache Interface</span></span>

<span data-ttu-id="fa5f6-104">表示用于合成技术的全局程序集缓存。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-104">Represents the global assembly cache for use by the fusion technology.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fa5f6-105">方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-105">Methods</span></span>  
  
|<span data-ttu-id="fa5f6-106">方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-106">Method</span></span>|<span data-ttu-id="fa5f6-107">说明</span><span class="sxs-lookup"><span data-stu-id="fa5f6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fa5f6-108">CreateAssemblyCacheItem 方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-108">CreateAssemblyCacheItem Method</span></span>](iassemblycache-createassemblycacheitem-method.md)|<span data-ttu-id="fa5f6-109">获取对新 [IAssemblyCacheItem](iassemblycacheitem-interface.md)的引用。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-109">Gets a reference to a new [IAssemblyCacheItem](iassemblycacheitem-interface.md).</span></span>|  
|[<span data-ttu-id="fa5f6-110">CreateAssemblyScavenger 方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-110">CreateAssemblyScavenger Method</span></span>](iassemblycache-createassemblyscavenger-method.md)|<span data-ttu-id="fa5f6-111">保留供合成技术内部使用。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-111">Reserved for internal use by the fusion technology.</span></span>|  
|[<span data-ttu-id="fa5f6-112">InstallAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-112">InstallAssembly Method</span></span>](iassemblycache-installassembly-method.md)|<span data-ttu-id="fa5f6-113">在全局程序集缓存中安装指定的程序集。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-113">Installs the specified assembly in the global assembly cache.</span></span>|  
|[<span data-ttu-id="fa5f6-114">QueryAssemblyInfo 方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-114">QueryAssemblyInfo Method</span></span>](iassemblycache-queryassemblyinfo-method.md)|<span data-ttu-id="fa5f6-115">获取有关指定程序集的请求的数据。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-115">Gets the requested data about the specified assembly.</span></span>|  
|[<span data-ttu-id="fa5f6-116">UninstallAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="fa5f6-116">UninstallAssembly Method</span></span>](iassemblycache-uninstallassembly-method.md)|<span data-ttu-id="fa5f6-117">从全局程序集缓存中卸载指定的程序集。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-117">Uninstalls the specified assembly from the global assembly cache.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fa5f6-118">要求</span><span class="sxs-lookup"><span data-stu-id="fa5f6-118">Requirements</span></span>  

 <span data-ttu-id="fa5f6-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa5f6-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa5f6-120">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="fa5f6-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="fa5f6-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa5f6-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa5f6-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa5f6-122">See also</span></span>

- [<span data-ttu-id="fa5f6-123">合成接口</span><span class="sxs-lookup"><span data-stu-id="fa5f6-123">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="fa5f6-124">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="fa5f6-124">Global Assembly Cache</span></span>](../../app-domains/gac.md)
