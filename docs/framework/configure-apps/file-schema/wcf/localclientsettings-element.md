---
description: 了解详细信息： <localClientSettings> 元素
title: <localClientSettings> 元素
ms.date: 03/30/2017
ms.assetid: 4680ace5-f4e1-4fcb-b9d8-a4a4af5cd7ae
ms.openlocfilehash: 6393a460b5a58ab9bf7933df8643df3530da5f14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802211"
---
# <a name="localclientsettings-element"></a><span data-ttu-id="d88ad-103">\<localClientSettings> 元素</span><span class="sxs-lookup"><span data-stu-id="d88ad-103">\<localClientSettings> element</span></span>

<span data-ttu-id="d88ad-104">指定此绑定的本地客户端安全设置。</span><span class="sxs-lookup"><span data-stu-id="d88ad-104">Specifies the security settings of a local client for this binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<localClientSettings>**  
  
## <a name="syntax"></a><span data-ttu-id="d88ad-105">语法</span><span class="sxs-lookup"><span data-stu-id="d88ad-105">Syntax</span></span>  
  
```xml  
<security>
   <localClientSettings cacheCookies="Boolean"
                        cookieRenewalThresholdPercentage="Integer"
                        detectReplays="Boolean"
                        maxClockSkew="TimeSpan"
                        maxCookieCachingTime="TimeSpan"
                        reconnectTransportOnFailure="Boolean"
                        replayCacheSize="Integer"
                        replayWindow="TimeSpan"
                        sessionKeyRenewalInterval="TimeSpan"
                        sessionKeyRolloverInterval="TimeSpan"
                        timestampValidityDuration="TimeSpan" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d88ad-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d88ad-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d88ad-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d88ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d88ad-108">特性</span><span class="sxs-lookup"><span data-stu-id="d88ad-108">Attributes</span></span>  
  
|<span data-ttu-id="d88ad-109">属性</span><span class="sxs-lookup"><span data-stu-id="d88ad-109">Attribute</span></span>|<span data-ttu-id="d88ad-110">说明</span><span class="sxs-lookup"><span data-stu-id="d88ad-110">Description</span></span>|  
|---------------|-----------------|  
|`cacheCookies`|<span data-ttu-id="d88ad-111">一个布尔值，指定是否启用 Cookie 缓存。</span><span class="sxs-lookup"><span data-stu-id="d88ad-111">A Boolean value that specifies whether cookie caching is enabled.</span></span> <span data-ttu-id="d88ad-112">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="d88ad-112">The default is `false`.</span></span>|  
|`cookieRenewalThresholdPercentage`|<span data-ttu-id="d88ad-113">一个整数，指定可续订的最大 Cookie 百分比。</span><span class="sxs-lookup"><span data-stu-id="d88ad-113">An integer that specifies the maximum percentage of cookies that can be renewed.</span></span> <span data-ttu-id="d88ad-114">该值应介于 0 至 100 之间（包括这两个数）。</span><span class="sxs-lookup"><span data-stu-id="d88ad-114">This value should be between 0 and 100 inclusively.</span></span> <span data-ttu-id="d88ad-115">默认值为 90。</span><span class="sxs-lookup"><span data-stu-id="d88ad-115">The default is 90.</span></span>|  
|`detectReplays`|<span data-ttu-id="d88ad-116">一个布尔值，指定是否自动检测和处理针对通道的重放攻击。</span><span class="sxs-lookup"><span data-stu-id="d88ad-116">A Boolean value that specifies whether replay attacks against the channel are detected and dealt with automatically.</span></span> <span data-ttu-id="d88ad-117">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="d88ad-117">The default is `false`.</span></span>|  
|`maxClockSkew`|<span data-ttu-id="d88ad-118">一个 <xref:System.TimeSpan>，指定通信双方的系统时钟之间的最大时间差异。</span><span class="sxs-lookup"><span data-stu-id="d88ad-118">A <xref:System.TimeSpan> that specifies the maximum time difference between the system clocks of the two communicating parties.</span></span> <span data-ttu-id="d88ad-119">默认值为“00:05:00”。</span><span class="sxs-lookup"><span data-stu-id="d88ad-119">The default value is "00:05:00".</span></span><br /><br /> <span data-ttu-id="d88ad-120">当此值被设置为默认值时，接收方所接受的消息的发送时间时间戳最多可比消息接收时间晚或早 5 分钟。</span><span class="sxs-lookup"><span data-stu-id="d88ad-120">When this value is set to the default, the receiver accepts messages with send-time time stamps up to 5 minutes later or earlier than the time the message was received.</span></span> <span data-ttu-id="d88ad-121">未通过发送时间测试的消息会被拒绝。</span><span class="sxs-lookup"><span data-stu-id="d88ad-121">Messages that do not pass the send-time test are rejected.</span></span> <span data-ttu-id="d88ad-122">此设置与 `replayWindow` 属性结合使用。</span><span class="sxs-lookup"><span data-stu-id="d88ad-122">This setting is used in conjunction with the `replayWindow` attribute.</span></span>|  
|`maxCookieCachingTime`|<span data-ttu-id="d88ad-123">一个 <xref:System.TimeSpan>，指定 Cookie 的最长生存期。</span><span class="sxs-lookup"><span data-stu-id="d88ad-123">A <xref:System.TimeSpan> that specifies the maximum lifetime of cookies.</span></span> <span data-ttu-id="d88ad-124">默认值为“10675199.02:48:05.4775807”。</span><span class="sxs-lookup"><span data-stu-id="d88ad-124">The default value is "10675199.02:48:05.4775807".</span></span>|  
|`reconnectTransportOnFailure`|<span data-ttu-id="d88ad-125">一个布尔值，指定使用 WS-ReliableMessaging 的连接是否将在传输失败后尝试重新连接。</span><span class="sxs-lookup"><span data-stu-id="d88ad-125">A Boolean value that specifies whether connections using WS-Reliable messaging will attempt to reconnect after transport failures.</span></span> <span data-ttu-id="d88ad-126">默认值为 `true`，表示将进行无限次重新连接尝试。</span><span class="sxs-lookup"><span data-stu-id="d88ad-126">The default is `true`, which means that infinite attempts to reconnect are attempted.</span></span> <span data-ttu-id="d88ad-127">非活动超时能够打断此循环；非活动超时在无法重新连接通道时使其引发异常。</span><span class="sxs-lookup"><span data-stu-id="d88ad-127">The cycle is broken by the inactivity time-out, which causes the channel to throw an exception when it cannot be reconnected.</span></span>|  
|`replayCacheSize`|<span data-ttu-id="d88ad-128">一个正整数，指定用于重播检测的缓存 Nonce 的数目。</span><span class="sxs-lookup"><span data-stu-id="d88ad-128">A positive integer that specifies the number of cached nonces used for replay detection.</span></span> <span data-ttu-id="d88ad-129">如果超出此限制，则会移除最旧的 Nonce，并且为新消息创建一个新的 Nonce。</span><span class="sxs-lookup"><span data-stu-id="d88ad-129">If this limit is exceeded, the oldest nonce is removed and a new nonce is created for the new message.</span></span> <span data-ttu-id="d88ad-130">默认值为 500000。</span><span class="sxs-lookup"><span data-stu-id="d88ad-130">The default value is 500000.</span></span>|  
|`replayWindow`|<span data-ttu-id="d88ad-131">一个 <xref:System.TimeSpan>，指定单个消息 Nonce 有效的持续时间。</span><span class="sxs-lookup"><span data-stu-id="d88ad-131">A <xref:System.TimeSpan> that specifies the duration in which individual message nonces are valid.</span></span><br /><br /> <span data-ttu-id="d88ad-132">在此持续时间之后，如果发送的消息与之前发送的消息具有相同的 Nonce，则该消息将被拒绝。</span><span class="sxs-lookup"><span data-stu-id="d88ad-132">After this duration, a message sent with the same nonce as the one sent before will not be accepted.</span></span> <span data-ttu-id="d88ad-133">此属性与 `maxClockSkew` 属性结合使用，以防止遭受重放攻击。</span><span class="sxs-lookup"><span data-stu-id="d88ad-133">This attribute is used in conjunction with the `maxClockSkew` attribute to prevent replay attacks.</span></span> <span data-ttu-id="d88ad-134">攻击者可以在其重放时间窗口过期之后重放消息。</span><span class="sxs-lookup"><span data-stu-id="d88ad-134">An attacker could replay a message after its replay window has expired.</span></span> <span data-ttu-id="d88ad-135">但是，该消息将无法通过 `maxClockSkew` 测试；如果消息的发送时间时间戳比消息接收时间晚或早指定的时间，则该测试会拒绝消息。</span><span class="sxs-lookup"><span data-stu-id="d88ad-135">This message, however, would fail the `maxClockSkew` test which rejects messages with send-time timestamps up to a specified time later or earlier than the time the message was received.</span></span>|  
|`sessionKeyRenewalInterval`|<span data-ttu-id="d88ad-136">一个 <xref:System.TimeSpan>，指定一段持续时间，发起方在此段时间之后将续订安全会话的密钥。</span><span class="sxs-lookup"><span data-stu-id="d88ad-136">A <xref:System.TimeSpan> that specifies the duration after which the initiator will renew the key for the security session.</span></span> <span data-ttu-id="d88ad-137">默认值为“10:00:00”。</span><span class="sxs-lookup"><span data-stu-id="d88ad-137">The default is "10:00:00".</span></span>|  
|`sessionKeyRolloverInterval`|<span data-ttu-id="d88ad-138">一个 <xref:System.TimeSpan>，指定在密钥续订期间，上一个会话密钥对于传入消息有效的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="d88ad-138">A <xref:System.TimeSpan> that specifies the time interval a previous session key is valid on incoming messages during a key renewal.</span></span> <span data-ttu-id="d88ad-139">默认值为“00:05:00”。</span><span class="sxs-lookup"><span data-stu-id="d88ad-139">The default is "00:05:00".</span></span><br /><br /> <span data-ttu-id="d88ad-140">在密钥续订期间，客户端和服务器必须总是使用最新的可用密钥来发送消息。</span><span class="sxs-lookup"><span data-stu-id="d88ad-140">During key renewal, the client and server must always send messages using the most current available key.</span></span> <span data-ttu-id="d88ad-141">在延期时间到期前，双方都可以接受以上一个会话密钥加密的传入消息。</span><span class="sxs-lookup"><span data-stu-id="d88ad-141">Both parties will accept incoming messages secured with the previous session key until the rollover time expires.</span></span>|  
|`timestampValidityDuration`|<span data-ttu-id="d88ad-142">一个值为正的 <xref:System.TimeSpan>，指定时间戳有效的持续时间。</span><span class="sxs-lookup"><span data-stu-id="d88ad-142">A positive <xref:System.TimeSpan> that specifies the duration in which a time stamp is valid.</span></span> <span data-ttu-id="d88ad-143">默认值为“00:15:00”。</span><span class="sxs-lookup"><span data-stu-id="d88ad-143">The default is "00:15:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d88ad-144">子元素</span><span class="sxs-lookup"><span data-stu-id="d88ad-144">Child Elements</span></span>  

 <span data-ttu-id="d88ad-145">无</span><span class="sxs-lookup"><span data-stu-id="d88ad-145">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d88ad-146">父元素</span><span class="sxs-lookup"><span data-stu-id="d88ad-146">Parent Elements</span></span>  
  
|<span data-ttu-id="d88ad-147">元素</span><span class="sxs-lookup"><span data-stu-id="d88ad-147">Element</span></span>|<span data-ttu-id="d88ad-148">说明</span><span class="sxs-lookup"><span data-stu-id="d88ad-148">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-custombinding.md)|<span data-ttu-id="d88ad-149">指定自定义绑定的安全选项。</span><span class="sxs-lookup"><span data-stu-id="d88ad-149">Specifies the security options for a custom binding.</span></span>|  
|[\<secureConversationBootstrap>](secureconversationbootstrap.md)|<span data-ttu-id="d88ad-150">指定用于启动安全对话服务的默认值。</span><span class="sxs-lookup"><span data-stu-id="d88ad-150">Specifies the default values used for initiating a secure conversation service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d88ad-151">备注</span><span class="sxs-lookup"><span data-stu-id="d88ad-151">Remarks</span></span>  

 <span data-ttu-id="d88ad-152">这些设置不是从服务的安全策略派生而来的，从这个意义上说，它们是本地的。</span><span class="sxs-lookup"><span data-stu-id="d88ad-152">The settings are local in the sense that they are not settings derived from the security policy of the service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d88ad-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="d88ad-153">See also</span></span>

- <xref:System.ServiceModel.Configuration.LocalClientSecuritySettingsElement>
- <xref:System.ServiceModel.Configuration.SecurityElementBase.LocalClientSettings%2A>
- <xref:System.ServiceModel.Channels.SecurityBindingElement.LocalClientSettings%2A>
- <xref:System.ServiceModel.Channels.LocalClientSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="d88ad-154">绑定</span><span class="sxs-lookup"><span data-stu-id="d88ad-154">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="d88ad-155">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="d88ad-155">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="d88ad-156">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="d88ad-156">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="d88ad-157">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="d88ad-157">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="d88ad-158">自定义绑定安全性</span><span class="sxs-lookup"><span data-stu-id="d88ad-158">Custom Binding Security</span></span>](../../../wcf/samples/custom-binding-security.md)
