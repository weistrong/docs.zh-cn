---
description: 了解详细信息： ICLRReferenceAssemblyEnum 接口
title: ICLRReferenceAssemblyEnum 接口
ms.date: 03/30/2017
api_name:
- ICLRReferenceAssemblyEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRReferenceAssemblyEnum
helpviewer_keywords:
- ICLRReferenceAssemblyEnum interface [.NET Framework hosting]
ms.assetid: 8adbf092-c3ba-4bee-b25b-0de6e43a4ce5
topic_type:
- apiref
ms.openlocfilehash: a7e522623c254940a6dbb8d22bf7f2fec76a1072
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688983"
---
# <a name="iclrreferenceassemblyenum-interface"></a><span data-ttu-id="870d7-103">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="870d7-103">ICLRReferenceAssemblyEnum Interface</span></span>

<span data-ttu-id="870d7-104">提供一些方法，这些方法允许主机使用公共语言运行时 (CLR) 内部的程序集标识数据来操作由文件或流引用的程序集，而无需创建或了解这些标识。</span><span class="sxs-lookup"><span data-stu-id="870d7-104">Provides methods that allow the host to manipulate the set of assemblies referenced by a file or stream using assembly identity data that is internal to the common language runtime (CLR), without needing to create or understand those identities.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="870d7-105">方法</span><span class="sxs-lookup"><span data-stu-id="870d7-105">Methods</span></span>  
  
|<span data-ttu-id="870d7-106">方法</span><span class="sxs-lookup"><span data-stu-id="870d7-106">Method</span></span>|<span data-ttu-id="870d7-107">说明</span><span class="sxs-lookup"><span data-stu-id="870d7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="870d7-108">Get 方法</span><span class="sxs-lookup"><span data-stu-id="870d7-108">Get Method</span></span>](iclrreferenceassemblyenum-get-method.md)|<span data-ttu-id="870d7-109">获取所提供索引处的程序集标识。</span><span class="sxs-lookup"><span data-stu-id="870d7-109">Gets the assembly identity at the supplied index.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="870d7-110">要求</span><span class="sxs-lookup"><span data-stu-id="870d7-110">Requirements</span></span>  

 <span data-ttu-id="870d7-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="870d7-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="870d7-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="870d7-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="870d7-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="870d7-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="870d7-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="870d7-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="870d7-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="870d7-115">See also</span></span>

- [<span data-ttu-id="870d7-116">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="870d7-116">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="870d7-117">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="870d7-117">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="870d7-118">承载接口</span><span class="sxs-lookup"><span data-stu-id="870d7-118">Hosting Interfaces</span></span>](hosting-interfaces.md)
