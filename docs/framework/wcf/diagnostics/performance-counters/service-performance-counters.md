---
description: 了解详细信息：服务性能计数器
title: 服务性能计数器
ms.date: 03/30/2017
ms.assetid: 4210f549-31f2-4ea7-99bd-69eaffb98ddf
ms.openlocfilehash: 16f6f2548cf7f92b64264ac606423c69e62cd110
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99686032"
---
# <a name="service-performance-counters"></a><span data-ttu-id="c656e-103">服务性能计数器</span><span class="sxs-lookup"><span data-stu-id="c656e-103">Service Performance Counters</span></span>

<span data-ttu-id="c656e-104">服务性能计数器将服务行为作为整体来进行衡量，可用于诊断服务整体性能。</span><span class="sxs-lookup"><span data-stu-id="c656e-104">Service performance counters measure the service behavior as a whole and can be used to diagnose the performance of the whole service.</span></span> <span data-ttu-id="c656e-105">如果使用性能监视器 (Perfmon.exe) 查看，可以在 `ServiceModelService 4.0.0.0` 性能对象下找到服务性能计数器。</span><span class="sxs-lookup"><span data-stu-id="c656e-105">They can be found under the `ServiceModelService 4.0.0.0` performance object when viewing with Performance Monitor (Perfmon.exe).</span></span> <span data-ttu-id="c656e-106">使用以下模式命名计数器实例：</span><span class="sxs-lookup"><span data-stu-id="c656e-106">The instances are named using the following pattern:</span></span>  
  
`ServiceName@ServiceBaseAddress`
  
> [!CAUTION]
> <span data-ttu-id="c656e-107">性能计数器实例的名称长度存在限制。</span><span class="sxs-lookup"><span data-stu-id="c656e-107">There is a limit on the length of a performance counter instance's name.</span></span> <span data-ttu-id="c656e-108">当 Windows Communication Foundation (WCF) 计数器实例名称超出最大长度时，WCF 会将部分实例名称替换为哈希值。</span><span class="sxs-lookup"><span data-stu-id="c656e-108">When a Windows Communication Foundation (WCF) counter instance name exceeds the maximum length, WCF replaces a portion of the instance name with a hash value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c656e-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="c656e-109">See also</span></span>

- [<span data-ttu-id="c656e-110">性能计数器</span><span class="sxs-lookup"><span data-stu-id="c656e-110">Performance Counters</span></span>](index.md)
