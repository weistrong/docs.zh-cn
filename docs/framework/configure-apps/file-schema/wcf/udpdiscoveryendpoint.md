---
description: 了解详细信息： <udpDiscoveryEndpoint>
title: <udpDiscoveryEndpoint>
ms.date: 03/30/2017
ms.assetid: 1f485329-2771-43bc-88de-df8f2faa3bb7
ms.openlocfilehash: 9863b4bc768b9c1cca933d001f0db596ce502fa0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749228"
---
# \<udpDiscoveryEndpoint>

<span data-ttu-id="86e31-102">此配置元素定义一个通过 UDP 多播绑定为发现操作预先配置的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="86e31-102">This configuration element defines a standard endpoint that is pre-configured for discovery operations over a UDP multicast binding.</span></span> <span data-ttu-id="86e31-103">此终结点具有固定协定并支持两个 WS-Discovery 协议版本。</span><span class="sxs-lookup"><span data-stu-id="86e31-103">This endpoint has a fixed contract and supports two WS-Discovery protocol versions.</span></span> <span data-ttu-id="86e31-104">此外，根据 WS-Discovery 规范（WS-Discovery 2005 年 4 月版或 WS-Discovery 1.1 版）中的规定，它还具有固定 UDP 绑定和默认地址。</span><span class="sxs-lookup"><span data-stu-id="86e31-104">In addition, it has a fixed UDP binding and a default address as specified in the WS-Discovery specifications (WS-Discovery April 2005 or WS-Discovery V1.1).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<standardEndpoints>**](standardendpoints.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<udpDiscoveryEndpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="86e31-105">语法</span><span class="sxs-lookup"><span data-stu-id="86e31-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint discoveryMode="Adhoc/Managed"
                        discoveryVersion="WSDiscovery11/WSDiscoveryApril2005"
                        maxResponseDelay="Timespan"
                        multicastAddress="Uri"
                        name="String" />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="86e31-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="86e31-106">Attributes and Elements</span></span>  

 <span data-ttu-id="86e31-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="86e31-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="86e31-108">特性</span><span class="sxs-lookup"><span data-stu-id="86e31-108">Attributes</span></span>  
  
|<span data-ttu-id="86e31-109">属性</span><span class="sxs-lookup"><span data-stu-id="86e31-109">Attribute</span></span>|<span data-ttu-id="86e31-110">说明</span><span class="sxs-lookup"><span data-stu-id="86e31-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="86e31-111">discoveryMode</span><span class="sxs-lookup"><span data-stu-id="86e31-111">discoveryMode</span></span>|<span data-ttu-id="86e31-112">一个字符串，指定发现协议的模式。</span><span class="sxs-lookup"><span data-stu-id="86e31-112">A string that specifies the mode of discovery protocol.</span></span> <span data-ttu-id="86e31-113">有效值为 "即席" 和 "Managed"。</span><span class="sxs-lookup"><span data-stu-id="86e31-113">Valid values are "Adhoc" and "Managed".</span></span> <span data-ttu-id="86e31-114">在托管模式下，协议依靠发现代理，此代理用作可检测服务的存储库。</span><span class="sxs-lookup"><span data-stu-id="86e31-114">In managed mode the protocol relies on a Discovery Proxy, which acts as a repository of Discoverable services.</span></span> <span data-ttu-id="86e31-115">即席模式要求协议使用 UDP 多播机制查找可用的服务。</span><span class="sxs-lookup"><span data-stu-id="86e31-115">Adhoc mode requires the protocol to use UDP multicast mechanism to find available services.</span></span> <span data-ttu-id="86e31-116">此值的类型为 <xref:System.ServiceModel.Discovery.ServiceDiscoveryMode>。</span><span class="sxs-lookup"><span data-stu-id="86e31-116">This value is of type <xref:System.ServiceModel.Discovery.ServiceDiscoveryMode>.</span></span>|  
|<span data-ttu-id="86e31-117">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="86e31-117">discoveryVersion</span></span>|<span data-ttu-id="86e31-118">一个字符串，指定两个 WS-Discovery 协议版本中的其中一个版本。</span><span class="sxs-lookup"><span data-stu-id="86e31-118">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="86e31-119">有效值为 WSDiscovery11 和 WSDiscoveryApril2005。</span><span class="sxs-lookup"><span data-stu-id="86e31-119">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="86e31-120">此值的类型为 <xref:System.ServiceModel.Discovery.DiscoveryVersion>。</span><span class="sxs-lookup"><span data-stu-id="86e31-120">This value is of type <xref:System.ServiceModel.Discovery.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="86e31-121">maxResponseDelay</span><span class="sxs-lookup"><span data-stu-id="86e31-121">maxResponseDelay</span></span>|<span data-ttu-id="86e31-122">一个 Timespan 值，指定 Discovery 协议在发送 Probe Match、Resolve Match 这类消息之前等待的最大延迟值。</span><span class="sxs-lookup"><span data-stu-id="86e31-122">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending certain messages such as Probe Match or Resolve Match.</span></span><br /><br /> <span data-ttu-id="86e31-123">如果同时发送所有 ProbeMatch，则可能发生网络风暴。</span><span class="sxs-lookup"><span data-stu-id="86e31-123">If all ProbeMatches are sent at the same time, a network storm may result.</span></span> <span data-ttu-id="86e31-124">若要防止发生这种情况，可在发送 ProbeMatch 时在各 ProbeMatch 之间应用随机延迟。</span><span class="sxs-lookup"><span data-stu-id="86e31-124">To prevent this from occurring, ProbeMatches are sent with a random delay between each ProbeMatch.</span></span> <span data-ttu-id="86e31-125">随机延迟的范围是从 0 到此特性所设置的值之间。</span><span class="sxs-lookup"><span data-stu-id="86e31-125">The random delay is in the range of 0 to the value set by this attribute.</span></span> <span data-ttu-id="86e31-126">如果将此特性设置为 0，则在不使用任何延迟的紧凑循环中发送 ProbeMatch 消息。</span><span class="sxs-lookup"><span data-stu-id="86e31-126">If this attribute is set to 0, then the ProbeMatches messages are sent in a tight loop without any delay.</span></span> <span data-ttu-id="86e31-127">否则，在发送 ProbeMatch 消息时将应用一定的随机延迟，以使发送所有 ProbeMatch 消息所用的总时间不会超过 maxResponseDelay。</span><span class="sxs-lookup"><span data-stu-id="86e31-127">Otherwise, the ProbeMatches messages are sent with some random delay such that the total time taken to send all ProbeMatches messages does not exceed the maxResponseDelay.</span></span> <span data-ttu-id="86e31-128">此值只与服务相关，不可用于客户端。</span><span class="sxs-lookup"><span data-stu-id="86e31-128">This value is only relevant for services, it is not used by clients.</span></span>|  
|<span data-ttu-id="86e31-129">multicastAddress</span><span class="sxs-lookup"><span data-stu-id="86e31-129">multicastAddress</span></span>|<span data-ttu-id="86e31-130">一个 URI，指定用于发送和接收发现消息的多播地址。</span><span class="sxs-lookup"><span data-stu-id="86e31-130">A Uri that specifies a multicast address to use for sending and receiving the discovery messages.</span></span> <span data-ttu-id="86e31-131">默认值是符合协议规范的多播地址。</span><span class="sxs-lookup"><span data-stu-id="86e31-131">The default value is the multicast address as conformant to the protocol specification.</span></span>|  
|`name`|<span data-ttu-id="86e31-132">一个字符串，指定标准终结点的配置的名称。</span><span class="sxs-lookup"><span data-stu-id="86e31-132">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="86e31-133">此名称在服务终结点的 `endpointConfiguration` 特性中用于将标准终结点链接到其配置。</span><span class="sxs-lookup"><span data-stu-id="86e31-133">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="86e31-134">子元素</span><span class="sxs-lookup"><span data-stu-id="86e31-134">Child Elements</span></span>  
  
|<span data-ttu-id="86e31-135">元素</span><span class="sxs-lookup"><span data-stu-id="86e31-135">Element</span></span>|<span data-ttu-id="86e31-136">说明</span><span class="sxs-lookup"><span data-stu-id="86e31-136">Description</span></span>|  
|-------------|-----------------|  
|[\<udpTransportSettings>](udptransportsettings.md)|<span data-ttu-id="86e31-137">一个设置集合，用于为 UDP 终结点配置 UDP 传输。</span><span class="sxs-lookup"><span data-stu-id="86e31-137">A collection of settings that allow you to configure UDP transport for the UDP endpoint.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="86e31-138">父元素</span><span class="sxs-lookup"><span data-stu-id="86e31-138">Parent Elements</span></span>  
  
|<span data-ttu-id="86e31-139">元素</span><span class="sxs-lookup"><span data-stu-id="86e31-139">Element</span></span>|<span data-ttu-id="86e31-140">说明</span><span class="sxs-lookup"><span data-stu-id="86e31-140">Description</span></span>|  
|-------------|-----------------|  
|[\<standardEndpoints>](standardendpoints.md)|<span data-ttu-id="86e31-141">具有一个或多个固定属性（地址、绑定和协定）的预定义终结点的标准终结点集合。</span><span class="sxs-lookup"><span data-stu-id="86e31-141">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="86e31-142">示例</span><span class="sxs-lookup"><span data-stu-id="86e31-142">Example</span></span>  

 <span data-ttu-id="86e31-143">下面的示例演示通过 UDP 多播传输侦听发现消息的服务。</span><span class="sxs-lookup"><span data-stu-id="86e31-143">The following example demonstrates a service listening for discovery messages over a UDP multicast transport.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService" />
    <endpoint name="DiscoveryEndpoint"
              kind="udpDiscoveryEndpoint" />
  </service>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint name="DiscoveryEndpoint"
                        version="WSDiscoveryApril2005" />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</services>
```  
  
## <a name="see-also"></a><span data-ttu-id="86e31-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="86e31-144">See also</span></span>

- <xref:System.ServiceModel.Discovery.DiscoveryEndpoint>
