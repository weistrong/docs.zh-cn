---
description: 了解详细信息： WCF 错误处理
title: WCF 错误处理
ms.date: 03/30/2017
ms.assetid: 1e4b1e0f-9598-449d-9d73-90bda62305b8
ms.openlocfilehash: 57f2c5078e0f73ff57eec79041cb7a2b2d42b498
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668170"
---
# <a name="wcf-error-handling"></a><span data-ttu-id="a9880-103">WCF 错误处理</span><span class="sxs-lookup"><span data-stu-id="a9880-103">WCF Error Handling</span></span>

<span data-ttu-id="a9880-104">WCF 应用程序遇到的错误属于下列三组中的一组：</span><span class="sxs-lookup"><span data-stu-id="a9880-104">The errors encountered by a WCF application belong to one of three groups:</span></span>  
  
1. <span data-ttu-id="a9880-105">通信错误</span><span class="sxs-lookup"><span data-stu-id="a9880-105">Communication Errors</span></span>  
  
2. <span data-ttu-id="a9880-106">代理/通道错误</span><span class="sxs-lookup"><span data-stu-id="a9880-106">Proxy/Channel Errors</span></span>  
  
3. <span data-ttu-id="a9880-107">应用程序错误</span><span class="sxs-lookup"><span data-stu-id="a9880-107">Application Errors</span></span>  
  
 <span data-ttu-id="a9880-108">网络不可用、客户端使用错误地址或服务主机未侦听传入消息时，会发生通信错误。</span><span class="sxs-lookup"><span data-stu-id="a9880-108">Communication errors occur when a network is unavailable, a client uses an incorrect address, or the service host is not listening for incoming messages.</span></span> <span data-ttu-id="a9880-109">这种类型的错误将作为 <xref:System.ServiceModel.CommunicationException> 或 <xref:System.ServiceModel.CommunicationException> 派生的类返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="a9880-109">Errors of this type are returned to the client as <xref:System.ServiceModel.CommunicationException> or <xref:System.ServiceModel.CommunicationException>-derived classes.</span></span>  
  
 <span data-ttu-id="a9880-110">代理/通道错误是通道或代理自身内部发生的错误。</span><span class="sxs-lookup"><span data-stu-id="a9880-110">Proxy/Channel errors are errors that occur within the channel or proxy itself.</span></span> <span data-ttu-id="a9880-111">这种类型的错误包括：尝试使用已关闭的代理或通道，客户端和服务之间存在协定不匹配，或者客户端凭据被服务拒绝。</span><span class="sxs-lookup"><span data-stu-id="a9880-111">Errors of this type include: attempting to use a proxy or channel that has been closed, a contract mismatch exists between the client and service, or the client’s credentials are rejected by the service.</span></span> <span data-ttu-id="a9880-112">此类别中存在许多不同类型的错误，错误太多，恕不在此列出。</span><span class="sxs-lookup"><span data-stu-id="a9880-112">There are many different types of errors in this category, too many to list here.</span></span> <span data-ttu-id="a9880-113">这种类型的错误将按原样返回到客户端（不对异常对象执行任何转换）。</span><span class="sxs-lookup"><span data-stu-id="a9880-113">Errors of this type are returned to the client as-is (no transformation is performed on the exception objects).</span></span>  
  
 <span data-ttu-id="a9880-114">执行服务操作过程中发生应用程序错误。</span><span class="sxs-lookup"><span data-stu-id="a9880-114">Application errors occur during the execution of a service operation.</span></span> <span data-ttu-id="a9880-115">这种类型的错误将作为 <xref:System.ServiceModel.FaultException> 或 <xref:System.ServiceModel.FaultException%601> 发送到客户端。</span><span class="sxs-lookup"><span data-stu-id="a9880-115">Errors of this kind are sent to the client as <xref:System.ServiceModel.FaultException> or <xref:System.ServiceModel.FaultException%601>.</span></span>  
  
 <span data-ttu-id="a9880-116">通过以下一种或多种方法执行 WCF 中的错误处理：</span><span class="sxs-lookup"><span data-stu-id="a9880-116">Error handling in WCF is performed by one or more of the following:</span></span>  
  
- <span data-ttu-id="a9880-117">直接处理引发的异常。</span><span class="sxs-lookup"><span data-stu-id="a9880-117">Directly handling the exception thrown.</span></span> <span data-ttu-id="a9880-118">只能针对通信错误以及代理/通道错误执行此操作。</span><span class="sxs-lookup"><span data-stu-id="a9880-118">This is only done for communication and proxy/channel errors.</span></span>  
  
- <span data-ttu-id="a9880-119">使用错误协定</span><span class="sxs-lookup"><span data-stu-id="a9880-119">Using fault contracts</span></span>  
  
- <span data-ttu-id="a9880-120">实现 <xref:System.ServiceModel.Dispatcher.IErrorHandler> 接口</span><span class="sxs-lookup"><span data-stu-id="a9880-120">Implementing the <xref:System.ServiceModel.Dispatcher.IErrorHandler> interface</span></span>  
  
- <span data-ttu-id="a9880-121">处理 <xref:System.ServiceModel.ServiceHost> 事件</span><span class="sxs-lookup"><span data-stu-id="a9880-121">Handling <xref:System.ServiceModel.ServiceHost> events</span></span>  
  
## <a name="fault-contracts"></a><span data-ttu-id="a9880-122">错误协定</span><span class="sxs-lookup"><span data-stu-id="a9880-122">Fault Contracts</span></span>  

 <span data-ttu-id="a9880-123">利用错误协定，您可以独立于平台的方式定义服务操作期间会发生的错误。</span><span class="sxs-lookup"><span data-stu-id="a9880-123">Fault contracts allow you to define the errors that can occur during service operation in a platform independent way.</span></span> <span data-ttu-id="a9880-124">默认情况下，所有从服务操作内引发的异常都将作为 <xref:System.ServiceModel.FaultException> 对象返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="a9880-124">By default all exceptions thrown from within a service operation will be returned to the client as a <xref:System.ServiceModel.FaultException> object.</span></span> <span data-ttu-id="a9880-125"><xref:System.ServiceModel.FaultException> 对象将包含很少的信息。</span><span class="sxs-lookup"><span data-stu-id="a9880-125">The <xref:System.ServiceModel.FaultException> object will contain very little information.</span></span> <span data-ttu-id="a9880-126">通过定义错误协定并作为 <xref:System.ServiceModel.FaultException%601> 返回错误，可以控制发送到客户端的信息。</span><span class="sxs-lookup"><span data-stu-id="a9880-126">You can control the information sent to the client by defining a fault contract and returning the error as a <xref:System.ServiceModel.FaultException%601>.</span></span> <span data-ttu-id="a9880-127">有关详细信息，请参阅 [在协定和服务中指定和处理错误](specifying-and-handling-faults-in-contracts-and-services.md)。</span><span class="sxs-lookup"><span data-stu-id="a9880-127">For more information, see [Specifying and Handling Faults in Contracts and Services](specifying-and-handling-faults-in-contracts-and-services.md).</span></span>  
  
## <a name="ierrorhandler"></a><span data-ttu-id="a9880-128">IErrorHandler</span><span class="sxs-lookup"><span data-stu-id="a9880-128">IErrorHandler</span></span>  

 <span data-ttu-id="a9880-129">利用 <xref:System.ServiceModel.Dispatcher.IErrorHandler> 接口，您可以对 WCF 应用程序响应错误的方式进行更多的控制。</span><span class="sxs-lookup"><span data-stu-id="a9880-129">The <xref:System.ServiceModel.Dispatcher.IErrorHandler> interface allows you more control over how your WCF application responds to errors.</span></span>  <span data-ttu-id="a9880-130">您可以完全控制返回到客户端的故障消息，还可以执行自定义错误处理，例如日志记录。</span><span class="sxs-lookup"><span data-stu-id="a9880-130">It gives you full control over the fault message that is returned to the client and allows you to perform custom error processing such as logging.</span></span>  <span data-ttu-id="a9880-131">有关 <xref:System.ServiceModel.Dispatcher.IErrorHandler> 和[扩展对错误处理和报告的控制](./samples/extending-control-over-error-handling-and-reporting.md)的详细信息</span><span class="sxs-lookup"><span data-stu-id="a9880-131">For more information about <xref:System.ServiceModel.Dispatcher.IErrorHandler> and [Extending Control Over Error Handling and Reporting](./samples/extending-control-over-error-handling-and-reporting.md)</span></span>  
  
## <a name="servicehost-events"></a><span data-ttu-id="a9880-132">ServiceHost 事件</span><span class="sxs-lookup"><span data-stu-id="a9880-132">ServiceHost Events</span></span>  

 <span data-ttu-id="a9880-133"><xref:System.ServiceModel.ServiceHost> 类承载服务，并定义处理错误可能需要的几个事件。</span><span class="sxs-lookup"><span data-stu-id="a9880-133">The <xref:System.ServiceModel.ServiceHost> class hosts services and defines several events that may be needed for handling errors.</span></span> <span data-ttu-id="a9880-134">例如：</span><span class="sxs-lookup"><span data-stu-id="a9880-134">For example:</span></span>  
  
1. <xref:System.ServiceModel.Channels.CommunicationObject.Faulted>
  
2. <xref:System.ServiceModel.ServiceHostBase.UnknownMessageReceived>
  
 <span data-ttu-id="a9880-135">有关详细信息，请参阅 <xref:System.ServiceModel.ServiceHost></span><span class="sxs-lookup"><span data-stu-id="a9880-135">For more information, see <xref:System.ServiceModel.ServiceHost></span></span>
