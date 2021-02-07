---
description: 了解详细信息： ServiceThrottlingBehavior
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: c4cf354c96340b910807bf7904e63a08dc01764b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715439"
---
# <a name="servicethrottlingbehavior"></a><span data-ttu-id="eaa50-103">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="eaa50-103">ServiceThrottlingBehavior</span></span>

<span data-ttu-id="eaa50-104">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="eaa50-104">ServiceThrottlingBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eaa50-105">语法</span><span class="sxs-lookup"><span data-stu-id="eaa50-105">Syntax</span></span>  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="eaa50-106">方法</span><span class="sxs-lookup"><span data-stu-id="eaa50-106">Methods</span></span>  

 <span data-ttu-id="eaa50-107">ServiceThrottlingBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="eaa50-107">The ServiceThrottlingBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="eaa50-108">属性</span><span class="sxs-lookup"><span data-stu-id="eaa50-108">Properties</span></span>  

 <span data-ttu-id="eaa50-109">ServiceThrottlingBehavior 类有以下属性：</span><span class="sxs-lookup"><span data-stu-id="eaa50-109">The ServiceThrottlingBehavior class has the following properties:</span></span>  
  
### <a name="maxconcurrentcalls"></a><span data-ttu-id="eaa50-110">MaxConcurrentCalls</span><span class="sxs-lookup"><span data-stu-id="eaa50-110">MaxConcurrentCalls</span></span>  

 <span data-ttu-id="eaa50-111">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="eaa50-111">Data type: sint32</span></span>  
  
 <span data-ttu-id="eaa50-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="eaa50-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="eaa50-113">ServiceHost 中所有调度程序对象正在积极处理的消息的最大数量。</span><span class="sxs-lookup"><span data-stu-id="eaa50-113">The maximum number of messages actively processing across all dispatcher objects in a ServiceHost.</span></span>  
  
### <a name="maxconcurrentinstances"></a><span data-ttu-id="eaa50-114">MaxConcurrentInstances</span><span class="sxs-lookup"><span data-stu-id="eaa50-114">MaxConcurrentInstances</span></span>  

 <span data-ttu-id="eaa50-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="eaa50-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="eaa50-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="eaa50-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="eaa50-117">一次可执行的服务对象的最大数量。</span><span class="sxs-lookup"><span data-stu-id="eaa50-117">The maximum number of service objects that can execute at one time.</span></span>  
  
### <a name="maxconcurrentsessions"></a><span data-ttu-id="eaa50-118">MaxConcurrentSessions</span><span class="sxs-lookup"><span data-stu-id="eaa50-118">MaxConcurrentSessions</span></span>  

 <span data-ttu-id="eaa50-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="eaa50-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="eaa50-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="eaa50-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="eaa50-121">主机一次可接受的最大会话数。</span><span class="sxs-lookup"><span data-stu-id="eaa50-121">The maximum number of sessions a host can accept at one time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eaa50-122">要求</span><span class="sxs-lookup"><span data-stu-id="eaa50-122">Requirements</span></span>  
  
|<span data-ttu-id="eaa50-123">MOF</span><span class="sxs-lookup"><span data-stu-id="eaa50-123">MOF</span></span>|<span data-ttu-id="eaa50-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="eaa50-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="eaa50-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="eaa50-125">Namespace</span></span>|<span data-ttu-id="eaa50-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="eaa50-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eaa50-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="eaa50-127">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
