---
description: 了解详细信息：实例
title: 实例数
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 9cd602164816a419b481ff600a7537593d4f500e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655261"
---
# <a name="instances"></a><span data-ttu-id="26db4-103">实例数</span><span class="sxs-lookup"><span data-stu-id="26db4-103">Instances</span></span>

<span data-ttu-id="26db4-104">计数器名称：Instances（实例数）。</span><span class="sxs-lookup"><span data-stu-id="26db4-104">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="26db4-105">说明</span><span class="sxs-lookup"><span data-stu-id="26db4-105">Description</span></span>  

 <span data-ttu-id="26db4-106">服务当前包含的实例上下文的数量。</span><span class="sxs-lookup"><span data-stu-id="26db4-106">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="26db4-107">在大部分时间里，实例上下文的数量都等于实例数。</span><span class="sxs-lookup"><span data-stu-id="26db4-107">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="26db4-108">但是，下列方案例外。</span><span class="sxs-lookup"><span data-stu-id="26db4-108">However, the following scenarios are exception to this rule.</span></span>  
  
- <span data-ttu-id="26db4-109">服务方法显式调用 <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="26db4-109">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
- <span data-ttu-id="26db4-110">一个 <xref:System.ServiceModel.ReleaseInstanceMode> 被应用于一个 <xref:System.ServiceModel.OperationBehaviorAttribute> 实例。</span><span class="sxs-lookup"><span data-stu-id="26db4-110">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26db4-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="26db4-111">See also</span></span>

- <xref:System.ServiceModel.OperationBehaviorAttribute>
