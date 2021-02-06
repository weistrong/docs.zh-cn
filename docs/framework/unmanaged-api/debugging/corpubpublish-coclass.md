---
description: 了解详细信息： CorpubPublish 组件类
title: CorpubPublish Coclass
ms.date: 03/30/2017
api_name:
- CorpubPublish Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorpubPublish
helpviewer_keywords:
- CorpubPublish coclass [.NET Framework debugging]
ms.assetid: 191015da-f54a-4bac-a28a-1de7ab3c3428
topic_type:
- apiref
ms.openlocfilehash: fdf4be6ff2d20391e989998cd0045ed27d602561
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661683"
---
# <a name="corpubpublish-coclass"></a><span data-ttu-id="08186-103">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="08186-103">CorpubPublish Coclass</span></span>

<span data-ttu-id="08186-104">提供用于发布应用程序域和进程相关信息的接口。</span><span class="sxs-lookup"><span data-stu-id="08186-104">Provides interfaces for publishing information about application domains and processes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08186-105">语法</span><span class="sxs-lookup"><span data-stu-id="08186-105">Syntax</span></span>  
  
```cpp  
coclass CorpubPublish {  
    [default] interface ICorPublish;  
    interface           ICorPublishProcess;  
    interface           ICorPublishAppDomain;  
    interface           ICorPublishProcessEnum;  
    interface           ICorPublishAppDomainEnum;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="08186-106">界面</span><span class="sxs-lookup"><span data-stu-id="08186-106">Interfaces</span></span>  
  
|<span data-ttu-id="08186-107">接口</span><span class="sxs-lookup"><span data-stu-id="08186-107">Interface</span></span>|<span data-ttu-id="08186-108">说明</span><span class="sxs-lookup"><span data-stu-id="08186-108">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="08186-109">ICorPublish 接口</span><span class="sxs-lookup"><span data-stu-id="08186-109">ICorPublish Interface</span></span>](icorpublish-interface.md)|<span data-ttu-id="08186-110">提供用于在这些进程中发布有关进程和应用程序域的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="08186-110">Provides methods for publishing information about processes and the application domains in those processes.</span></span>|  
|[<span data-ttu-id="08186-111">ICorPublishAppDomain 接口</span><span class="sxs-lookup"><span data-stu-id="08186-111">ICorPublishAppDomain Interface</span></span>](icorpublishappdomain-interface.md)|<span data-ttu-id="08186-112">表示并提供有关进程中的应用程序域的信息。</span><span class="sxs-lookup"><span data-stu-id="08186-112">Represents, and provides information about, an application domain in a process.</span></span>|  
|[<span data-ttu-id="08186-113">ICorPublishAppDomainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="08186-113">ICorPublishAppDomainEnum Interface</span></span>](icorpublishappdomainenum-interface.md)|<span data-ttu-id="08186-114">提供遍历进程中当前存在的应用程序域集合的方法。</span><span class="sxs-lookup"><span data-stu-id="08186-114">Provides methods that traverse a collection of application domains that currently exist within a process.</span></span>|  
|[<span data-ttu-id="08186-115">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="08186-115">ICorPublishProcess Interface</span></span>](icorpublishprocess-interface.md)|<span data-ttu-id="08186-116">表示在计算机上运行的进程。</span><span class="sxs-lookup"><span data-stu-id="08186-116">Represents a process that is running on a computer.</span></span>|  
|[<span data-ttu-id="08186-117">ICorPublishProcessEnum 接口</span><span class="sxs-lookup"><span data-stu-id="08186-117">ICorPublishProcessEnum Interface</span></span>](icorpublishprocessenum-interface.md)|<span data-ttu-id="08186-118">提供遍历计算机上运行的进程集合的方法。</span><span class="sxs-lookup"><span data-stu-id="08186-118">Provides methods that traverse a collection of processes that are running on a computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08186-119">备注</span><span class="sxs-lookup"><span data-stu-id="08186-119">Remarks</span></span>  

 <span data-ttu-id="08186-120">典型的发布方案涉及到需要调试在应用程序域中的计算机上运行的托管代码的开发人员。</span><span class="sxs-lookup"><span data-stu-id="08186-120">A typical publishing scenario involves a developer who wants to debug managed code that is running on a computer within an application domain.</span></span> <span data-ttu-id="08186-121">宿主环境可能会在一个进程内运行多个应用程序域。</span><span class="sxs-lookup"><span data-stu-id="08186-121">The hosting environment may be running more than one application domain within a process.</span></span> <span data-ttu-id="08186-122">开发人员希望使用图形用户界面或其他一些方法列出计算机上运行的所有进程，并选择特定的进程。</span><span class="sxs-lookup"><span data-stu-id="08186-122">The developer would like to use a graphical user interface or some other means to list all of the processes that are running on the computer, and pick a specific process.</span></span> <span data-ttu-id="08186-123">此列表应包括正在运行托管代码的进程中的所有应用程序域。</span><span class="sxs-lookup"><span data-stu-id="08186-123">The listing should include all of the application domains within processes that are running managed code.</span></span> <span data-ttu-id="08186-124">然后，开发人员可以确定特定的应用程序域，并将调试器附加到该域。</span><span class="sxs-lookup"><span data-stu-id="08186-124">The developer can then identify the specific application domain and attach a debugger to that domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08186-125">要求</span><span class="sxs-lookup"><span data-stu-id="08186-125">Requirements</span></span>  

 <span data-ttu-id="08186-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08186-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08186-127">**标头：** CorPub .idl</span><span class="sxs-lookup"><span data-stu-id="08186-127">**Header:** CorPub.idl</span></span>  
  
 <span data-ttu-id="08186-128">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08186-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08186-129">**.NET Framework 版本：**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08186-129">**.NET Framework Versions:**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08186-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="08186-130">See also</span></span>

- [<span data-ttu-id="08186-131">调试</span><span class="sxs-lookup"><span data-stu-id="08186-131">Debugging</span></span>](index.md)
