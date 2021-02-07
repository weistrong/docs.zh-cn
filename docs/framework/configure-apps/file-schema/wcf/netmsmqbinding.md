---
description: 了解详细信息： <netMsmqBinding>
title: <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: a68b44d7-7799-43a3-9e63-f07c782810a6
ms.openlocfilehash: 2d0e475065b1ed34df895fc289567d678489fbbf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683952"
---
# \<netMsmqBinding>

<span data-ttu-id="bc054-102">定义适用于跨计算机通信的排队绑定。</span><span class="sxs-lookup"><span data-stu-id="bc054-102">Defines a queued binding suitable for cross-machine communication.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<netMsmqBinding>**  
  
## <a name="syntax"></a><span data-ttu-id="bc054-103">语法</span><span class="sxs-lookup"><span data-stu-id="bc054-103">Syntax</span></span>  
  
```xml  
<netMsmqBinding>
  <binding closeTimeout="TimeSpan"
           customDeadLetterQueue="Uri"
           deadLetterQueue="Uri"
           durable="Boolean"
           exactlyOnce="Boolean"
           maxBufferPoolSize="Integer"
           maxReceivedMessageSize="Integer"
           maxRetryCycles="Integer"
           name="String"
           openTimeout="TimeSpan"
           poisonMessageHandling="Disabled/EnabledIfSupported"
           queueTransferProtocol="Native/Srmp/SrmpSecure"
           receiveErrorHandling="Drop/Fault/Move/Reject"
           receiveTimeout="TimeSpan"
           receiveRetryCount="Integer"
           rejectAfterLastRetry="Boolean"
           retryCycleDelay="TimeSpan"
           sendTimeout="TimeSpan"
           timeToLive="TimeSpan"
           useActiveDirectory="Boolean"
           useMsmqTracing="Boolean"
           useSourceJournal="Boolean">
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="None/Windows/UserName/Certificate/InfoCard" />
      <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
                 msmqEncryptionAlgorithm="RC4Stream/AES"
                 msmqProtectionLevel="None/Sign/EncryptAndSign"
                 msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    </security>
    <readerQuotas maxArrayLength="Integer"
                  maxBytesPerRead="Integer"
                  maxDepth="Integer"
                  maxNameTableCharCount="Integer"
                  maxStringContentLength="Integer" />
  </binding>
</netMsmqBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bc054-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bc054-104">Attributes and Elements</span></span>  

 <span data-ttu-id="bc054-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc054-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bc054-106">特性</span><span class="sxs-lookup"><span data-stu-id="bc054-106">Attributes</span></span>  
  
|<span data-ttu-id="bc054-107">属性</span><span class="sxs-lookup"><span data-stu-id="bc054-107">Attribute</span></span>|<span data-ttu-id="bc054-108">说明</span><span class="sxs-lookup"><span data-stu-id="bc054-108">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="bc054-109">一个 <xref:System.TimeSpan> 值，指定为完成关闭操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bc054-109">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="bc054-110">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="bc054-110">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="bc054-111">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="bc054-111">The default is 00:01:00.</span></span>|  
|`customDeadLetterQueue`|<span data-ttu-id="bc054-112">一个 URI，包含每个应用程序的死信队列（该队列用于放置已过期的消息或者放置传输或传递失败的消息）的位置。</span><span class="sxs-lookup"><span data-stu-id="bc054-112">A URI that contains the location of the per-application dead letter queue, where messages that have expired or that have failed transfer or delivery are placed.</span></span><br /><br /> <span data-ttu-id="bc054-113">死信队列是发送应用程序的队列管理器中的一个队列，用于放置传递失败的过期消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-113">The dead letter queue is a queue on the queue manager of the sending application for expired messages that have failed to be delivered.</span></span><br /><br /> <span data-ttu-id="bc054-114"><xref:System.ServiceModel.MsmqBindingBase.CustomDeadLetterQueue%2A> 指定的 URI 必须使用 net.msmq 方案。</span><span class="sxs-lookup"><span data-stu-id="bc054-114">The URI that is specified by <xref:System.ServiceModel.MsmqBindingBase.CustomDeadLetterQueue%2A> must use the net.msmq scheme.</span></span>|  
|`deadLetterQueue`|<span data-ttu-id="bc054-115">一个 <xref:System.ServiceModel.MsmqBindingBase.DeadLetterQueue%2A> 值，该值指定所用死信队列（如果有）的类型。</span><span class="sxs-lookup"><span data-stu-id="bc054-115">A <xref:System.ServiceModel.MsmqBindingBase.DeadLetterQueue%2A> value specifying which type of dead-letter queue to use, if any.</span></span><br /><br /> <span data-ttu-id="bc054-116">死信队列是无法传递到应用程序的消息所要传输到的位置。</span><span class="sxs-lookup"><span data-stu-id="bc054-116">A dead-letter queue is the place where messages that have failed to be delivered to the application will be transferred.</span></span><br /><br /> <span data-ttu-id="bc054-117">对于需要 `exactlyOnce` 保证（即，`exactlyOnce` 属性设置为 `true`）的消息，此属性默认为 MSMQ 中系统级事务性死信队列。</span><span class="sxs-lookup"><span data-stu-id="bc054-117">For messages that require `exactlyOnce` assurance (that is, the `exactlyOnce` attribute is set to `true`), this attribute defaults to the system-wide transactional dead-letter queue in MSMQ.</span></span><br /><br /> <span data-ttu-id="bc054-118">对于不需要保证的消息，此属性默认为 `null`。</span><span class="sxs-lookup"><span data-stu-id="bc054-118">For messages that require no assurances, this attribute defaults to `null`.</span></span>|  
|`durable`|<span data-ttu-id="bc054-119">一个布尔值，指示消息在队列中是持久的还是可变的。</span><span class="sxs-lookup"><span data-stu-id="bc054-119">A Boolean value that indicates whether the message is durable or volatile in the queue.</span></span> <span data-ttu-id="bc054-120">持久消息能够在队列管理器崩溃后保留下来，而可变消息则不能。</span><span class="sxs-lookup"><span data-stu-id="bc054-120">A durable message survives a queue manager crash, while a volatile message does not.</span></span> <span data-ttu-id="bc054-121">当应用程序需要较低的延迟并且可以容忍偶尔丢失消息时，可变消息是有用的。</span><span class="sxs-lookup"><span data-stu-id="bc054-121">Volatile messages are useful when applications require lower latency and can tolerate occasional lost messages.</span></span> <span data-ttu-id="bc054-122">如果 `exactlyOnce` 属性设置为 `true`，则消息必须为持久的消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-122">If the `exactlyOnce` attribute is set to `true`, the messages must be durable.</span></span> <span data-ttu-id="bc054-123">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="bc054-123">The default is `true`.</span></span>|  
|`exactlyOnce`|<span data-ttu-id="bc054-124">一个布尔值，指示是否只传递一次此绑定所处理的每个消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-124">A Boolean value that indicates whether each message processed by this binding is delivered only once.</span></span> <span data-ttu-id="bc054-125">然后，将通知发送方有关传递失败的信息。</span><span class="sxs-lookup"><span data-stu-id="bc054-125">The sender will then be notified of delivery failures.</span></span> <span data-ttu-id="bc054-126">如果 `durable` 为 `false`，则将忽略此属性并且传输消息，而不会提供传递保证。</span><span class="sxs-lookup"><span data-stu-id="bc054-126">When `durable` is `false`, this attribute is ignored and messages are transferred without delivery assurance.</span></span> <span data-ttu-id="bc054-127">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="bc054-127">The default is `true`.</span></span> <span data-ttu-id="bc054-128">有关详细信息，请参阅 <xref:System.ServiceModel.MsmqBindingBase.ExactlyOnce%2A>。</span><span class="sxs-lookup"><span data-stu-id="bc054-128">For more information, see <xref:System.ServiceModel.MsmqBindingBase.ExactlyOnce%2A>.</span></span>|  
|`maxBufferPoolSize`|<span data-ttu-id="bc054-129">一个整数，指定此绑定的最大缓冲池大小。</span><span class="sxs-lookup"><span data-stu-id="bc054-129">An integer that specifies the maximum buffer pool size for this binding.</span></span> <span data-ttu-id="bc054-130">默认值为 8。</span><span class="sxs-lookup"><span data-stu-id="bc054-130">The default is 8.</span></span>|  
|`maxReceivedMessageSize`|<span data-ttu-id="bc054-131">一个正整数，定义此绑定所处理的最大消息大小（以字节为单位），其中包括标头。</span><span class="sxs-lookup"><span data-stu-id="bc054-131">A positive integer that defines the maximum message size, in bytes, including headers, that is processed by this binding.</span></span> <span data-ttu-id="bc054-132">如果消息超出此限制，则发送方将收到 SOAP 错误。</span><span class="sxs-lookup"><span data-stu-id="bc054-132">The sender of a message exceeding this limit will receive a SOAP fault.</span></span> <span data-ttu-id="bc054-133">接收方将删除该消息，并在跟踪日志中创建事件项。</span><span class="sxs-lookup"><span data-stu-id="bc054-133">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="bc054-134">默认值为 65536。</span><span class="sxs-lookup"><span data-stu-id="bc054-134">The default is 65536.</span></span> <span data-ttu-id="bc054-135">对消息大小进行的此限制旨在降低遭受拒绝服务 (DoS) 攻击的可能性。</span><span class="sxs-lookup"><span data-stu-id="bc054-135">This bound on message size is intended to limit exposure to Denial of Service (DoS) attacks.</span></span>|  
|`maxRetryCycles`|<span data-ttu-id="bc054-136">一个整数，指示病毒消息检测功能所使用的重试周期数。</span><span class="sxs-lookup"><span data-stu-id="bc054-136">An integer that indicates the number of retry cycles used by the poison-message detection feature.</span></span> <span data-ttu-id="bc054-137">如果所有周期的所有传递尝试均失败，则消息将变为病毒消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-137">A message becomes a poison message when it fails all delivery attempts of all cycles.</span></span> <span data-ttu-id="bc054-138">默认值为 3。</span><span class="sxs-lookup"><span data-stu-id="bc054-138">The default is 3.</span></span> <span data-ttu-id="bc054-139">有关详细信息，请参阅 <xref:System.ServiceModel.MsmqBindingBase.MaxRetryCycles%2A>。</span><span class="sxs-lookup"><span data-stu-id="bc054-139">For more information, see <xref:System.ServiceModel.MsmqBindingBase.MaxRetryCycles%2A>.</span></span>|  
|`name`|<span data-ttu-id="bc054-140">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="bc054-140">Required attribute.</span></span> <span data-ttu-id="bc054-141">一个包含绑定的配置名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="bc054-141">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="bc054-142">因为此值用作绑定的标识，所以它应该是唯一的。</span><span class="sxs-lookup"><span data-stu-id="bc054-142">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="bc054-143">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="bc054-143">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="bc054-144">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="bc054-144">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="bc054-145">一个 <xref:System.TimeSpan> 值，指定为完成打开操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bc054-145">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="bc054-146">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="bc054-146">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="bc054-147">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="bc054-147">The default is 00:01:00.</span></span>|  
|`QueueTransferProtocol`|<span data-ttu-id="bc054-148">一个有效的 <xref:System.ServiceModel.QueueTransferProtocol> 值，指定此绑定所使用的排队通信通道传输。</span><span class="sxs-lookup"><span data-stu-id="bc054-148">A valid <xref:System.ServiceModel.QueueTransferProtocol> value that specifies the queued communication channel transport that this binding uses.</span></span> <span data-ttu-id="bc054-149">在使用 SOAP 可靠消息协议时，MSMQ 不支持 Active Directory 寻址。</span><span class="sxs-lookup"><span data-stu-id="bc054-149">MSMQ does not support Active Directory addressing when using SOAP Reliable Messaging Protocol.</span></span> <span data-ttu-id="bc054-150">因此， `Srmp` `Srmps` 当 `useActiveDirectory` 特性设置为时，不应将此特性设置为或 `true` 。</span><span class="sxs-lookup"><span data-stu-id="bc054-150">Therefore, you should not set this attribute to `Srmp` or `Srmps` when the `useActiveDirectory` attribute is set to `true`.</span></span>|  
|`receiveErrorHandling`|<span data-ttu-id="bc054-151">一个 <xref:System.ServiceModel.ReceiveErrorHandling> 值，指定如何处理病毒消息和不可调度的消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-151">A <xref:System.ServiceModel.ReceiveErrorHandling> value that specifies how poison and nondispatchable messages are handled.</span></span>|  
|`receiveRetryCount`|<span data-ttu-id="bc054-152">一个整数，指定队列管理器在将消息传输到重试队列前可尝试发送该消息的最大次数。</span><span class="sxs-lookup"><span data-stu-id="bc054-152">An integer that specifies the maximum number of times the queue manager should attempt to send a message before transferring it to the retry queue.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="bc054-153">一个 <xref:System.TimeSpan> 值，指定为完成接收操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bc054-153">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="bc054-154">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="bc054-154">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="bc054-155">默认值为 00:10:00。</span><span class="sxs-lookup"><span data-stu-id="bc054-155">The default is 00:10:00.</span></span>|  
|`retryCycleDelay`|<span data-ttu-id="bc054-156">一个 TimeSpan 值，指定尝试传递无法立即传递的消息时，各个重试周期之间的时间延迟。</span><span class="sxs-lookup"><span data-stu-id="bc054-156">A TimeSpan value that specifies the time delay between retry cycles when attempting to deliver a message that could not be delivered immediately.</span></span> <span data-ttu-id="bc054-157">该值只定义最小等待时间，因为实际等待时间可能较长。</span><span class="sxs-lookup"><span data-stu-id="bc054-157">The value defines only the minimum wait time because actual wait time can be longer.</span></span> <span data-ttu-id="bc054-158">默认值为 00:10:00。</span><span class="sxs-lookup"><span data-stu-id="bc054-158">The default value is 00:10:00.</span></span> <span data-ttu-id="bc054-159">有关详细信息，请参阅 <xref:System.ServiceModel.MsmqBindingBase.RetryCycleDelay%2A>。</span><span class="sxs-lookup"><span data-stu-id="bc054-159">For more information, see <xref:System.ServiceModel.MsmqBindingBase.RetryCycleDelay%2A>.</span></span>|  
|`sendTimeout`|<span data-ttu-id="bc054-160">一个 <xref:System.TimeSpan> 值，指定为完成发送操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bc054-160">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="bc054-161">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="bc054-161">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="bc054-162">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="bc054-162">The default is 00:01:00.</span></span>|  
|`timeToLive`|<span data-ttu-id="bc054-163">一个 TimeSpan 值，指定在消息过期并放入死信队列之前消息保持有效的持续时间。</span><span class="sxs-lookup"><span data-stu-id="bc054-163">A TimeSpan value that specifies how long the messages are valid before they are expired and put into the dead-letter queue.</span></span> <span data-ttu-id="bc054-164">默认值为 1.00:00:00。</span><span class="sxs-lookup"><span data-stu-id="bc054-164">The default is 1.00:00:00.</span></span><br /><br /> <span data-ttu-id="bc054-165">设置此属性可以确保具有时效性的消息不会在由接收应用程序进行处理之前过时。</span><span class="sxs-lookup"><span data-stu-id="bc054-165">This attribute is set to ensure that time-sensitive messages do not become stale before they are processed by the receiving applications.</span></span> <span data-ttu-id="bc054-166">如果队列中的消息在指定时间间隔内未被接收应用程序进行处理，则称该消息为过时消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-166">A message in a queue that is not consumed by the receiving application within the time interval specified is said to be expired.</span></span> <span data-ttu-id="bc054-167">过时消息被发送到称为“死信队列”的特殊队列中。</span><span class="sxs-lookup"><span data-stu-id="bc054-167">Expired messages are sent to special queue called the dead letter queue.</span></span> <span data-ttu-id="bc054-168">死信队列的位置通过 `DeadLetterQueue` 属性进行设置，或基于保证设置为适当的默认值。</span><span class="sxs-lookup"><span data-stu-id="bc054-168">The location of the dead letter queue is set with the `DeadLetterQueue` attribute or to the appropriate default, based on assurances.</span></span>|  
|`usingActiveDirectory`|<span data-ttu-id="bc054-169">一个布尔值，指定是否应该使用 Active Directory 转换队列地址。</span><span class="sxs-lookup"><span data-stu-id="bc054-169">A Boolean value that specifies if queue addresses should be converted using Active Directory.</span></span><br /><br /> <span data-ttu-id="bc054-170">MSMQ 队列地址可由路径名或直接格式名组成。</span><span class="sxs-lookup"><span data-stu-id="bc054-170">MSMQ queue addresses can consist of path names or direct format names.</span></span> <span data-ttu-id="bc054-171">对于直接格式名，MSMQ 会使用 DNS、NetBIOS 或 IP 解析计算机名称。</span><span class="sxs-lookup"><span data-stu-id="bc054-171">With a direct format name, MSMQ resolves the computer name using DNS, NetBIOS or IP.</span></span> <span data-ttu-id="bc054-172">对于路径名，MSMQ 会使用 Active Directory 解析计算机名称。</span><span class="sxs-lookup"><span data-stu-id="bc054-172">With a path name, MSMQ resolves the computer name using Active Directory.</span></span><br /><br /> <span data-ttu-id="bc054-173">默认情况下，Windows Communication Foundation (WCF) 排队传输会将消息队列的 URI 转换为直接格式名。</span><span class="sxs-lookup"><span data-stu-id="bc054-173">By default, Windows Communication Foundation (WCF) queued transport converts the URI of a message queue to a direct format name.</span></span> <span data-ttu-id="bc054-174">通过将 `UseActiveDirectory` 属性设置为 True，应用程序可以指定排队传输应使用 Active Directory 而不是 DNS、NetBIOS 或 IP 来解析计算机名称。</span><span class="sxs-lookup"><span data-stu-id="bc054-174">By setting the `UseActiveDirectory` property to true, an application can specify that the queued transport should resolve the computer name using Active Directory rather than DNS, NetBIOS, or IP.</span></span>|  
|`useMsmqTracing`|<span data-ttu-id="bc054-175">一个布尔值，指定是否应跟踪由此绑定处理的消息。</span><span class="sxs-lookup"><span data-stu-id="bc054-175">A Boolean value that specifies whether messages processed by this binding should be traced.</span></span> <span data-ttu-id="bc054-176">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="bc054-176">The default is `false`.</span></span> <span data-ttu-id="bc054-177">如果启用了跟踪，则每当消息离开或到达消息队列计算机时，都会创建报告消息并将其发送到报告队列。</span><span class="sxs-lookup"><span data-stu-id="bc054-177">When tracing is enabled, report messages are created and sent to the report queue each time the message leaves or arrives at a Message Queuing computer.</span></span>|  
|`useSourceJournal`|<span data-ttu-id="bc054-178">一个布尔值，指定是否应将由此绑定处理的消息的副本存储在源日志中。</span><span class="sxs-lookup"><span data-stu-id="bc054-178">A Boolean value that specifies copies of messages processed by this binding should be stored in the source journal.</span></span> <span data-ttu-id="bc054-179">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="bc054-179">The default is `false`.</span></span><br /><br /> <span data-ttu-id="bc054-180">如果排队应用程序要保留已离开计算机传出队列的消息的记录，则可以将这些消息复制到日志队列。</span><span class="sxs-lookup"><span data-stu-id="bc054-180">Queued applications that want to keep a record of messages that have left the computer's outgoing queue can copy the messages to a journal queue.</span></span> <span data-ttu-id="bc054-181">在消息离开传出队列，并且接收到目标计算机已接收该消息的确认后，该消息的副本就会保留在发送计算机的系统日志队列中。</span><span class="sxs-lookup"><span data-stu-id="bc054-181">Once a message leaves the outgoing queue and an acknowledgment is received that the message was received on the destination computer, a copy of the message is kept in the sending computer's system journal queue.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bc054-182">子元素</span><span class="sxs-lookup"><span data-stu-id="bc054-182">Child Elements</span></span>  
  
|<span data-ttu-id="bc054-183">元素</span><span class="sxs-lookup"><span data-stu-id="bc054-183">Element</span></span>|<span data-ttu-id="bc054-184">说明</span><span class="sxs-lookup"><span data-stu-id="bc054-184">Description</span></span>|  
|-------------|-----------------|  
|[\<readerQuotas>](/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="bc054-185">定义可由采用此绑定配置的终结点进行处理的 SOAP 消息的复杂性约束。</span><span class="sxs-lookup"><span data-stu-id="bc054-185">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="bc054-186">此元素的类型为 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>。</span><span class="sxs-lookup"><span data-stu-id="bc054-186">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
|[\<security>](security-of-netmsmqbinding.md)|<span data-ttu-id="bc054-187">定义绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="bc054-187">Defines the security settings for the binding.</span></span> <span data-ttu-id="bc054-188">此元素的类型为 <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="bc054-188">This element is of type <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bc054-189">父元素</span><span class="sxs-lookup"><span data-stu-id="bc054-189">Parent Elements</span></span>  
  
|<span data-ttu-id="bc054-190">元素</span><span class="sxs-lookup"><span data-stu-id="bc054-190">Element</span></span>|<span data-ttu-id="bc054-191">说明</span><span class="sxs-lookup"><span data-stu-id="bc054-191">Description</span></span>|  
|-------------|-----------------|  
|[\<bindings>](bindings.md)|<span data-ttu-id="bc054-192">此元素包含标准绑定和自定义绑定的集合。</span><span class="sxs-lookup"><span data-stu-id="bc054-192">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bc054-193">备注</span><span class="sxs-lookup"><span data-stu-id="bc054-193">Remarks</span></span>  

 <span data-ttu-id="bc054-194">`netMsmqBinding` 绑定通过利用 Microsoft 消息队列 (MSMQ) 作为传输来提供队列支持，并且为松耦合应用程序、故障隔离、负载均衡和断开连接的操作提供支持。</span><span class="sxs-lookup"><span data-stu-id="bc054-194">The `netMsmqBinding` binding provides support for queuing by leveraging Microsoft Message Queuing (MSMQ) as a transport and enables support for loosely coupled applications, failure isolation, load leveling and disconnected operations.</span></span> <span data-ttu-id="bc054-195">有关这些功能的讨论，请参阅 [WCF 中的队列](../../../wcf/feature-details/queues-in-wcf.md)。</span><span class="sxs-lookup"><span data-stu-id="bc054-195">For a discussion of these features, see [Queues in WCF](../../../wcf/feature-details/queues-in-wcf.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc054-196">示例</span><span class="sxs-lookup"><span data-stu-id="bc054-196">Example</span></span>  
  
```xml  
<configuration>
  <system.ServiceModel>
    <bindings>
      <netMsmqBinding>
        <binding closeTimeout="00:00:10"
                 openTimeout="00:00:20"
                 receiveTimeout="00:00:30"
                 sendTimeout="00:00:40"
                 deadLetterQueue="net.msmq://localhost/blah"
                 durable="true"
                 exactlyOnce="true"
                 maxReceivedMessageSize="1000"
                 maxRetries="11"
                 maxRetryCycles="12"
                 poisonMessageHandling="Disabled"
                 rejectAfterLastRetry="false"
                 retryCycleDelay="00:05:55"
                 timeToLive="00:11:11"
                 sourceJournal="true"
                 useMsmqTracing="true"
                 useActiveDirectory="true">
          <security>
            <message clientCredentialType="Windows" />
          </security>
        </binding>
      </netMsmqBinding>
    </bindings>
  </system.ServiceModel>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="bc054-197">请参阅</span><span class="sxs-lookup"><span data-stu-id="bc054-197">See also</span></span>

- <xref:System.ServiceModel.NetMsmqBinding>
- <xref:System.ServiceModel.Configuration.NetMsmqBindingElement>
- [\<binding>](bindings.md)
- [<span data-ttu-id="bc054-198">绑定</span><span class="sxs-lookup"><span data-stu-id="bc054-198">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="bc054-199">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="bc054-199">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="bc054-200">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="bc054-200">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="bc054-201">WCF 中的队列</span><span class="sxs-lookup"><span data-stu-id="bc054-201">Queues in WCF</span></span>](../../../wcf/feature-details/queues-in-wcf.md)
