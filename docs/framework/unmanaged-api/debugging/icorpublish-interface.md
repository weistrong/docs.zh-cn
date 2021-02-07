---
description: 了解详细信息： ICorPublish 接口
title: ICorPublish 接口
ms.date: 03/30/2017
api_name:
- ICorPublish
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish
helpviewer_keywords:
- ICorPublish interface [.NET Framework debugging]
ms.assetid: 87c4fcb2-7703-4a2e-afb6-42973381b960
topic_type:
- apiref
ms.openlocfilehash: 0cec1d3407246989c6b916ca0760e6f556566ce6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721822"
---
# <a name="icorpublish-interface"></a><span data-ttu-id="23714-103">ICorPublish 接口</span><span class="sxs-lookup"><span data-stu-id="23714-103">ICorPublish Interface</span></span>

<span data-ttu-id="23714-104">用作发布有关进程的信息，以及有关这些进程中的应用程序域的信息。</span><span class="sxs-lookup"><span data-stu-id="23714-104">Serves as the general interface for publishing information about processes and information about the application domains in those processes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="23714-105">方法</span><span class="sxs-lookup"><span data-stu-id="23714-105">Methods</span></span>  
  
|<span data-ttu-id="23714-106">方法</span><span class="sxs-lookup"><span data-stu-id="23714-106">Method</span></span>|<span data-ttu-id="23714-107">说明</span><span class="sxs-lookup"><span data-stu-id="23714-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="23714-108">EnumProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="23714-108">EnumProcesses Method</span></span>](icorpublish-enumprocesses-method.md)|<span data-ttu-id="23714-109">获取一个 [ICorPublishProcessEnum](icorpublishprocessenum-interface.md) 实例，它包含在此计算机上运行的托管进程。</span><span class="sxs-lookup"><span data-stu-id="23714-109">Gets an [ICorPublishProcessEnum](icorpublishprocessenum-interface.md) instance that contains the managed processes running on this computer.</span></span>|  
|[<span data-ttu-id="23714-110">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="23714-110">GetProcess Method</span></span>](icorpublish-getprocess-method.md)|<span data-ttu-id="23714-111">获取一个表示具有指定标识符的进程的 [ICorPublishProcess](icorpublishprocess-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="23714-111">Gets an [ICorPublishProcess](icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="23714-112">要求</span><span class="sxs-lookup"><span data-stu-id="23714-112">Requirements</span></span>  

 <span data-ttu-id="23714-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="23714-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="23714-114">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="23714-114">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="23714-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="23714-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="23714-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="23714-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23714-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="23714-117">See also</span></span>

- [<span data-ttu-id="23714-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="23714-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="23714-119">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="23714-119">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
