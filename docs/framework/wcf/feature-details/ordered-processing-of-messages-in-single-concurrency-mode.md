---
description: 了解详细信息：以单并发模式对消息进行有序处理
title: 单并发模式中的有序消息处理
ms.date: 03/30/2017
ms.assetid: a90f5662-a796-46cd-ae33-30a4072838af
ms.openlocfilehash: 2dd876f1831dda8b388108f238810be333e693be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733679"
---
# <a name="ordered-processing-of-messages-in-single-concurrency-mode"></a><span data-ttu-id="1c9a4-103">单并发模式中的有序消息处理</span><span class="sxs-lookup"><span data-stu-id="1c9a4-103">Ordered Processing of Messages in Single Concurrency Mode</span></span>

<span data-ttu-id="1c9a4-104">WCF 不会保证消息的处理顺序，除非基础通道是会话的。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-104">WCF makes no guarantees about the order in which messages are processed, unless the underlying channel is sessionful.</span></span>  <span data-ttu-id="1c9a4-105">例如，使用 MsmqInputChannel 的 WCF 服务（不是会话通道）将无法按顺序处理消息。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-105">For instance, a WCF service that uses MsmqInputChannel, which is not a sessionful channel, will fail to process messages in order.</span></span> <span data-ttu-id="1c9a4-106">在某些情况下，开发人员可能希望按顺序处理行为，但不希望使用会话。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-106">There are some circumstances where a developer may want the in order processing behavior but not want to use sessions.</span></span> <span data-ttu-id="1c9a4-107">本主题介绍在单一并发模式中运行服务时，如何配置这种行为。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-107">This topic describes how to configure this behavior when a service is running in Single Concurrency Mode.</span></span>  
  
## <a name="in-order-message-processing"></a><span data-ttu-id="1c9a4-108">有序消息处理</span><span class="sxs-lookup"><span data-stu-id="1c9a4-108">In-order Message Processing</span></span>  

 <span data-ttu-id="1c9a4-109">名为 <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> 的新特性已添加到 <xref:System.ServiceModel.ServiceBehaviorAttribute>。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-109">A new attribute called <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> has been added to the <xref:System.ServiceModel.ServiceBehaviorAttribute>.</span></span> <span data-ttu-id="1c9a4-110">当 <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> 设置为 true 并且<xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> 设置为 <xref:System.ServiceModel.ConcurrencyMode.Single> 时，将按顺序处理发送到服务的消息。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-110">When <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> is set to true and <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> is set to <xref:System.ServiceModel.ConcurrencyMode.Single> messages sent to the service will be processed in order.</span></span> <span data-ttu-id="1c9a4-111">下面的代码段演示如何设置这些特性。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-111">The following code snippet illustrates how to set these attributes.</span></span>  
  
```csharp
[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single, EnsureOrderedDispatch = true )]  
    class Service : IService  
    {  
         // ...  
    }  
```  
  
 <span data-ttu-id="1c9a4-112">如果 <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> 设置为任何其他值，则引发 <xref:System.InvalidOperationException>。</span><span class="sxs-lookup"><span data-stu-id="1c9a4-112">If <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> is set to any other value, an <xref:System.InvalidOperationException> is thrown.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c9a4-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="1c9a4-113">See also</span></span>

- [<span data-ttu-id="1c9a4-114">会话、实例化和并发</span><span class="sxs-lookup"><span data-stu-id="1c9a4-114">Sessions, Instancing, and Concurrency</span></span>](sessions-instancing-and-concurrency.md)
- [<span data-ttu-id="1c9a4-115">并发</span><span class="sxs-lookup"><span data-stu-id="1c9a4-115">Concurrency</span></span>](../samples/concurrency.md)
