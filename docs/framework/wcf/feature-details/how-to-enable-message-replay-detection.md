---
description: 了解详细信息：如何：启用消息重播检测
title: 如何：启用消息重放检测
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF security
- replay detection [WCF]
- WCF, custom bindings
- WCF, security
ms.assetid: 8b847e91-69a3-49e1-9e5f-0c455e50d804
ms.openlocfilehash: 743452195d5bf78360909a22ea81997c2712dd06
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704662"
---
# <a name="how-to-enable-message-replay-detection"></a><span data-ttu-id="3d3fb-103">如何：启用消息重放检测</span><span class="sxs-lookup"><span data-stu-id="3d3fb-103">How to: Enable Message Replay Detection</span></span>

<span data-ttu-id="3d3fb-104">当攻击者复制双方之间的消息流并将该消息流向一方或多方重播时，将发生重播攻击。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-104">A replay attack occurs when an attacker copies a stream of messages between two parties and replays the stream to one or more of the parties.</span></span> <span data-ttu-id="3d3fb-105">除非攻击程度降低，否则受到攻击的计算机会将该流处理为合法消息，从而导致产生大量不良结果，例如某项的冗余排序。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-105">Unless mitigated, the computers subject to the attack will process the stream as legitimate messages, resulting in a range of bad consequences, such as redundant orders of an item.</span></span>  
  
 <span data-ttu-id="3d3fb-106">有关消息重播检测的详细信息，请参阅 [消息重播检测](/previous-versions/msp-n-p/ff649371(v=pandp.10))。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-106">For more information about message replay detection, see [Message Replay Detection](/previous-versions/msp-n-p/ff649371(v=pandp.10)).</span></span>  
  
 <span data-ttu-id="3d3fb-107">下面的过程演示了各种属性，这些属性可用于使用 Windows Communication Foundation (WCF) 控制重播检测。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-107">The following procedure demonstrates various properties that you can use to control replay detection using Windows Communication Foundation (WCF).</span></span>  
  
### <a name="to-control-replay-detection-on-the-client-using-code"></a><span data-ttu-id="3d3fb-108">使用代码在客户端上控制重播检测</span><span class="sxs-lookup"><span data-stu-id="3d3fb-108">To control replay detection on the client using code</span></span>  
  
1. <span data-ttu-id="3d3fb-109">创建要在 <xref:System.ServiceModel.Channels.SecurityBindingElement> 中使用的 <xref:System.ServiceModel.Channels.CustomBinding>。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-109">Create a <xref:System.ServiceModel.Channels.SecurityBindingElement> to use in a <xref:System.ServiceModel.Channels.CustomBinding>.</span></span> <span data-ttu-id="3d3fb-110">有关详细信息，请参阅 [如何：使用 SecurityBindingElement 创建自定义绑定](how-to-create-a-custom-binding-using-the-securitybindingelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-110">For more information, see [How to: Create a Custom Binding Using the SecurityBindingElement](how-to-create-a-custom-binding-using-the-securitybindingelement.md).</span></span> <span data-ttu-id="3d3fb-111">下面的示例使用通过 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 类的 <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateKerberosBindingElement%2A> 创建的 <xref:System.ServiceModel.Channels.SecurityBindingElement>。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-111">The following example uses a <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> created with the <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateKerberosBindingElement%2A> of the <xref:System.ServiceModel.Channels.SecurityBindingElement> class.</span></span>  
  
2. <span data-ttu-id="3d3fb-112">使用 <xref:System.ServiceModel.Channels.SecurityBindingElement.LocalClientSettings%2A> 属性返回对 <xref:System.ServiceModel.Channels.LocalClientSecuritySettings> 类的引用，并根据需要设置任何下列属性：</span><span class="sxs-lookup"><span data-stu-id="3d3fb-112">Use the <xref:System.ServiceModel.Channels.SecurityBindingElement.LocalClientSettings%2A> property to return a reference to the <xref:System.ServiceModel.Channels.LocalClientSecuritySettings> class and set any of the following properties, as appropriate:</span></span>  
  
    1. <span data-ttu-id="3d3fb-113">`DetectReplay`.</span><span class="sxs-lookup"><span data-stu-id="3d3fb-113">`DetectReplay`.</span></span> <span data-ttu-id="3d3fb-114">一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-114">A Boolean value.</span></span> <span data-ttu-id="3d3fb-115">该值控制客户端是否应当检测来自服务器的重播。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-115">This governs whether the client should detect replays from the server.</span></span> <span data-ttu-id="3d3fb-116">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-116">The default is `true`.</span></span>  
  
    2. <span data-ttu-id="3d3fb-117">`MaxClockSkew`.</span><span class="sxs-lookup"><span data-stu-id="3d3fb-117">`MaxClockSkew`.</span></span> <span data-ttu-id="3d3fb-118">一个 <xref:System.TimeSpan> 值。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-118">A <xref:System.TimeSpan> value.</span></span> <span data-ttu-id="3d3fb-119">控制重播机制在客户端和服务器之间可以容忍多大程度的时间偏差。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-119">Governs how much time skew the replay mechanism can tolerate between the client and the server.</span></span> <span data-ttu-id="3d3fb-120">该安全机制检查发送的时间戳，并确定在过去它是否返回过快。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-120">The security mechanism examines the time stamp sent and determines whether it was sent too far back in the past.</span></span> <span data-ttu-id="3d3fb-121">默认为 5 分钟。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-121">The default is 5 minutes.</span></span>  
  
    3. <span data-ttu-id="3d3fb-122">`ReplayWindow`.</span><span class="sxs-lookup"><span data-stu-id="3d3fb-122">`ReplayWindow`.</span></span> <span data-ttu-id="3d3fb-123">一个 `TimeSpan` 值。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-123">A `TimeSpan` value.</span></span> <span data-ttu-id="3d3fb-124">该值控制某消息在由服务器（通过中间方）发送之后、到达客户端之前在网络中存留的时间。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-124">This governs how long a message can live in the network after the server sends it (through intermediaries) before reaching the client.</span></span> <span data-ttu-id="3d3fb-125">客户端跟踪在最后一个 `ReplayWindow` 中发送的消息的签名，以进行重播检测。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-125">The client tracks the signatures of the messages sent within the latest `ReplayWindow` for the purposes of replay detection.</span></span>  
  
    4. <span data-ttu-id="3d3fb-126">`ReplayCacheSize`.</span><span class="sxs-lookup"><span data-stu-id="3d3fb-126">`ReplayCacheSize`.</span></span> <span data-ttu-id="3d3fb-127">一个整数值。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-127">An integer value.</span></span> <span data-ttu-id="3d3fb-128">客户端在缓存中存储消息的签名。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-128">The client stores the signatures of the message in a cache.</span></span> <span data-ttu-id="3d3fb-129">此设置指定缓存中可以存储的签名数目。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-129">This setting specifies how many signatures the cache can store.</span></span> <span data-ttu-id="3d3fb-130">如果最后一个重播窗口中发送的消息数达到缓存限制，则拒绝新消息，直到最旧的缓存签名达到时间限制为止。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-130">If the number of messages sent within the last replay window reaches the cache limit, new messages are rejected until the oldest cached signatures reach the time limit.</span></span> <span data-ttu-id="3d3fb-131">默认值为500000。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-131">The default is 500000.</span></span>  
  
### <a name="to-control-replay-detection-on-the-service-using-code"></a><span data-ttu-id="3d3fb-132">使用代码在服务上控制重播检测</span><span class="sxs-lookup"><span data-stu-id="3d3fb-132">To control replay detection on the service using code</span></span>  
  
1. <span data-ttu-id="3d3fb-133">创建要在 <xref:System.ServiceModel.Channels.SecurityBindingElement> 中使用的 <xref:System.ServiceModel.Channels.CustomBinding>。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-133">Create a <xref:System.ServiceModel.Channels.SecurityBindingElement> to use in a <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
2. <span data-ttu-id="3d3fb-134">使用 <xref:System.ServiceModel.Channels.SecurityBindingElement.LocalServiceSettings%2A> 属性返回对 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings> 类的引用，并按照上面所述设置这些属性。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-134">Use the <xref:System.ServiceModel.Channels.SecurityBindingElement.LocalServiceSettings%2A> property to return a reference to the <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings> class, and set the properties as described previously.</span></span>  
  
### <a name="to-control-replay-detection-in-configuration-for-the-client-or-service"></a><span data-ttu-id="3d3fb-135">在客户端或服务的配置中控制重播检测</span><span class="sxs-lookup"><span data-stu-id="3d3fb-135">To control replay detection in configuration for the client or service</span></span>  
  
1. <span data-ttu-id="3d3fb-136">创建一个 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-136">Create a [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md).</span></span>  
  
2. <span data-ttu-id="3d3fb-137">创建 `<security>` 元素。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-137">Create a `<security>` element.</span></span>  
  
3. <span data-ttu-id="3d3fb-138">创建 [\<localClientSettings>](../../configure-apps/file-schema/wcf/localclientsettings-element.md) 或 [\<localServiceSettings>](../../configure-apps/file-schema/wcf/localservicesettings-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-138">Create a [\<localClientSettings>](../../configure-apps/file-schema/wcf/localclientsettings-element.md) or [\<localServiceSettings>](../../configure-apps/file-schema/wcf/localservicesettings-element.md).</span></span>  
  
4. <span data-ttu-id="3d3fb-139">根据需要，设置下列属性值：`detectReplays`、`maxClockSkew`、`replayWindow` 和 `replayCacheSize`。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-139">Set the following attribute values, as appropriate: `detectReplays`, `maxClockSkew`, `replayWindow`, and `replayCacheSize`.</span></span> <span data-ttu-id="3d3fb-140">下面的示例设置 `<localServiceSettings>` 元素的属性：</span><span class="sxs-lookup"><span data-stu-id="3d3fb-140">The following example sets the attributes of both a `<localServiceSettings>` and a `<localClientSettings>` element:</span></span>  
  
    ```xml  
    <customBinding>  
      <binding name="NewBinding0">  
       <textMessageEncoding />  
        <security>  
         <localClientSettings
          replayCacheSize="800000"
          maxClockSkew="00:03:00"  
          replayWindow="00:03:00" />  
         <localServiceSettings
          replayCacheSize="800000"
          maxClockSkew="00:03:00"  
          replayWindow="00:03:00" />  
        <secureConversationBootstrap />  
       </security>  
      <httpTransport />  
     </binding>  
    </customBinding>  
    ```  
  
## <a name="example"></a><span data-ttu-id="3d3fb-141">示例</span><span class="sxs-lookup"><span data-stu-id="3d3fb-141">Example</span></span>  

 <span data-ttu-id="3d3fb-142">下面的示例使用 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> 方法创建 <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateKerberosBindingElement%2A>，并设置绑定的重播属性。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-142">The following example creates a <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> using the <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateKerberosBindingElement%2A> method, and sets the replay properties of the binding.</span></span>  
  
 [!code-csharp[c_ReplayDetection#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_replaydetection/cs/source.cs#1)]
 [!code-vb[c_ReplayDetection#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_replaydetection/vb/source.vb#1)]  
  
## <a name="scope-of-replay-message-security-only"></a><span data-ttu-id="3d3fb-143">重播范围：仅限消息安全</span><span class="sxs-lookup"><span data-stu-id="3d3fb-143">Scope of Replay: Message Security Only</span></span>  

 <span data-ttu-id="3d3fb-144">请注意，下面的过程仅适用于“消息安全”模式。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-144">Note that the following procedures apply only to Message security mode.</span></span> <span data-ttu-id="3d3fb-145">对于“传输”和“使用消息凭据传输”模式，传输机制将检测重播。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-145">For Transport and Transport with Message Credential modes, the transport mechanisms detect replays.</span></span>  
  
## <a name="secure-conversation-notes"></a><span data-ttu-id="3d3fb-146">安全对话说明</span><span class="sxs-lookup"><span data-stu-id="3d3fb-146">Secure Conversation Notes</span></span>  

 <span data-ttu-id="3d3fb-147">对于启用安全对话的绑定，可以针对应用程序通道和安全对话引导绑定来调整这些设置。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-147">For bindings that enable secure conversations, you can adjust these settings both for the application channel as well as for the secure conversation bootstrap binding.</span></span> <span data-ttu-id="3d3fb-148">例如，可以对应用程序通道关闭重播，但是对建立安全对话的引导通道启用重播。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-148">For example, you can turn off replays for the application channel but enable them for the bootstrap channel that establishes the secure conversation.</span></span>  
  
 <span data-ttu-id="3d3fb-149">如果不使用安全对话会话，则重播检测不保证在服务器场方案中和回收进程时检测重播。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-149">If you do not use secure conversation sessions, replay detection does not guarantee detecting replays in server farm scenarios and when the process is recycled.</span></span> <span data-ttu-id="3d3fb-150">这适用于系统提供的下列绑定：</span><span class="sxs-lookup"><span data-stu-id="3d3fb-150">This applies to the following system-provided bindings:</span></span>  
  
- <span data-ttu-id="3d3fb-151"><xref:System.ServiceModel.BasicHttpBinding>.</span><span class="sxs-lookup"><span data-stu-id="3d3fb-151"><xref:System.ServiceModel.BasicHttpBinding>.</span></span>  
  
- <span data-ttu-id="3d3fb-152"><xref:System.ServiceModel.WSHttpBinding>，其 <xref:System.ServiceModel.NonDualMessageSecurityOverHttp.EstablishSecurityContext%2A> 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-152"><xref:System.ServiceModel.WSHttpBinding> with the <xref:System.ServiceModel.NonDualMessageSecurityOverHttp.EstablishSecurityContext%2A> property set to `false`.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3d3fb-153">编译代码</span><span class="sxs-lookup"><span data-stu-id="3d3fb-153">Compiling the Code</span></span>  
  
- <span data-ttu-id="3d3fb-154">编译该代码需要以下命名空间：</span><span class="sxs-lookup"><span data-stu-id="3d3fb-154">The following namespaces are required to compile the code:</span></span>  
  
- <xref:System>  
  
- <xref:System.ServiceModel>  
  
- <xref:System.ServiceModel.Channels>  
  
## <a name="see-also"></a><span data-ttu-id="3d3fb-155">请参阅</span><span class="sxs-lookup"><span data-stu-id="3d3fb-155">See also</span></span>

- <xref:System.ServiceModel.Channels.LocalClientSecuritySettings>
- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [<span data-ttu-id="3d3fb-156">安全对话和安全会话</span><span class="sxs-lookup"><span data-stu-id="3d3fb-156">Secure Conversations and Secure Sessions</span></span>](secure-conversations-and-secure-sessions.md)
- [\<localClientSettings>](../../configure-apps/file-schema/wcf/localclientsettings-element.md)
- [<span data-ttu-id="3d3fb-157">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="3d3fb-157">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](how-to-create-a-custom-binding-using-the-securitybindingelement.md)
