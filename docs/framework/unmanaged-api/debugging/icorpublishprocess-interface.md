---
description: 了解详细信息： ICorPublishProcess 接口
title: ICorPublishProcess 接口
ms.date: 03/30/2017
api_name:
- ICorPublishProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess
helpviewer_keywords:
- ICorPublishProcess interface [.NET Framework debugging]
ms.assetid: 6d1dc41b-8aa2-4889-bb00-1cbccc00c123
topic_type:
- apiref
ms.openlocfilehash: 8dbc619d33c2c9b625dde852948dff00b5be926e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800859"
---
# <a name="icorpublishprocess-interface"></a><span data-ttu-id="1d0f7-103">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="1d0f7-103">ICorPublishProcess Interface</span></span>

<span data-ttu-id="1d0f7-104">提供用于访问要显示的有关进程的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="1d0f7-104">Provides methods that access information to be displayed about a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1d0f7-105">方法</span><span class="sxs-lookup"><span data-stu-id="1d0f7-105">Methods</span></span>  
  
|<span data-ttu-id="1d0f7-106">方法</span><span class="sxs-lookup"><span data-stu-id="1d0f7-106">Method</span></span>|<span data-ttu-id="1d0f7-107">说明</span><span class="sxs-lookup"><span data-stu-id="1d0f7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1d0f7-108">EnumAppDomains 方法</span><span class="sxs-lookup"><span data-stu-id="1d0f7-108">EnumAppDomains Method</span></span>](icorpublishprocess-enumappdomains-method.md)|<span data-ttu-id="1d0f7-109">获取一个 [ICorPublishAppDomainEnum](icorpublishappdomainenum-interface.md) 实例，其中包含此所引用的进程中的应用程序域 `ICorPublishProcess` 。</span><span class="sxs-lookup"><span data-stu-id="1d0f7-109">Gets an [ICorPublishAppDomainEnum](icorpublishappdomainenum-interface.md) instance that contains the application domains in the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="1d0f7-110">GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="1d0f7-110">GetDisplayName Method</span></span>](icorpublishprocess-getdisplayname-method.md)|<span data-ttu-id="1d0f7-111">获取此引用的进程的可执行文件的完整路径 `ICorPublishProcess` 。</span><span class="sxs-lookup"><span data-stu-id="1d0f7-111">Gets the full path of the executable for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="1d0f7-112">GetProcessID 方法</span><span class="sxs-lookup"><span data-stu-id="1d0f7-112">GetProcessID Method</span></span>](icorpublishprocess-getprocessid-method.md)|<span data-ttu-id="1d0f7-113">获取此引用的进程的操作系统标识符 `ICorPublishProcess` 。</span><span class="sxs-lookup"><span data-stu-id="1d0f7-113">Gets the operating system identifier for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="1d0f7-114">IsManaged 方法</span><span class="sxs-lookup"><span data-stu-id="1d0f7-114">IsManaged Method</span></span>](icorpublishprocess-ismanaged-method.md)|<span data-ttu-id="1d0f7-115">获取一个值，该值指示由此引用的进程是否 `ICorPublishProcess` 已知正在运行托管代码。</span><span class="sxs-lookup"><span data-stu-id="1d0f7-115">Gets a value that indicates whether the process referenced by this `ICorPublishProcess` is known to be running managed code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1d0f7-116">要求</span><span class="sxs-lookup"><span data-stu-id="1d0f7-116">Requirements</span></span>  

 <span data-ttu-id="1d0f7-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1d0f7-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1d0f7-118">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="1d0f7-118">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="1d0f7-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1d0f7-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1d0f7-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1d0f7-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d0f7-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d0f7-121">See also</span></span>

- [<span data-ttu-id="1d0f7-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="1d0f7-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="1d0f7-123">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="1d0f7-123">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
