---
description: 了解详细信息： <windowsStreamSecurity>
title: <windowsStreamSecurity>
ms.date: 03/30/2017
ms.assetid: 926bea29-90c7-4a26-9cf0-fb4aa44f6f70
ms.openlocfilehash: c623dc23ca67d0341b66a2a4d97de564be77dcc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682392"
---
# \<windowsStreamSecurity>

<span data-ttu-id="1d78b-102">指定自定义绑定的 Windows 流安全设置。</span><span class="sxs-lookup"><span data-stu-id="1d78b-102">Specify Windows stream security settings of the custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<windowsStreamSecurity>**  
  
## <a name="syntax"></a><span data-ttu-id="1d78b-103">语法</span><span class="sxs-lookup"><span data-stu-id="1d78b-103">Syntax</span></span>  
  
```xml  
<windowsStreamSecurity protectionLevel="None/Sign/EncryptAndSign" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1d78b-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1d78b-104">Attributes and Elements</span></span>  

 <span data-ttu-id="1d78b-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d78b-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1d78b-106">特性</span><span class="sxs-lookup"><span data-stu-id="1d78b-106">Attributes</span></span>  
  
|<span data-ttu-id="1d78b-107">属性</span><span class="sxs-lookup"><span data-stu-id="1d78b-107">Attribute</span></span>|<span data-ttu-id="1d78b-108">说明</span><span class="sxs-lookup"><span data-stu-id="1d78b-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1d78b-109">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="1d78b-109">protectionLevel</span></span>|<span data-ttu-id="1d78b-110">定义消息级安全性。</span><span class="sxs-lookup"><span data-stu-id="1d78b-110">Defines message-level security.</span></span> <span data-ttu-id="1d78b-111">消息签名降低了在消息传输过程中第三方对消息进行篡改的风险。</span><span class="sxs-lookup"><span data-stu-id="1d78b-111">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="1d78b-112">加密为传输过程提供了数据级保密功能。</span><span class="sxs-lookup"><span data-stu-id="1d78b-112">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="1d78b-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="1d78b-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="1d78b-114">-None：无保护。</span><span class="sxs-lookup"><span data-stu-id="1d78b-114">-   None: No protection.</span></span><br /><span data-ttu-id="1d78b-115">-Sign：对消息进行签名。</span><span class="sxs-lookup"><span data-stu-id="1d78b-115">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="1d78b-116">-EncryptAndSign：对消息进行签名和加密。</span><span class="sxs-lookup"><span data-stu-id="1d78b-116">-   EncryptAndSign: Messages are signed and encrypted.</span></span><br /><br /> <span data-ttu-id="1d78b-117">默认值为 EncryptAndSign。</span><span class="sxs-lookup"><span data-stu-id="1d78b-117">The default is EncryptAndSign.</span></span><br /><br /> <span data-ttu-id="1d78b-118">此属性的类型为 <xref:System.Net.Security.ProtectionLevel>。</span><span class="sxs-lookup"><span data-stu-id="1d78b-118">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1d78b-119">子元素</span><span class="sxs-lookup"><span data-stu-id="1d78b-119">Child Elements</span></span>  

 <span data-ttu-id="1d78b-120">无</span><span class="sxs-lookup"><span data-stu-id="1d78b-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1d78b-121">父元素</span><span class="sxs-lookup"><span data-stu-id="1d78b-121">Parent Elements</span></span>  
  
|<span data-ttu-id="1d78b-122">元素</span><span class="sxs-lookup"><span data-stu-id="1d78b-122">Element</span></span>|<span data-ttu-id="1d78b-123">说明</span><span class="sxs-lookup"><span data-stu-id="1d78b-123">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="1d78b-124">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="1d78b-124">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1d78b-125">备注</span><span class="sxs-lookup"><span data-stu-id="1d78b-125">Remarks</span></span>  

 <span data-ttu-id="1d78b-126">使用面向流协议（如 TCP 和命名管道）的传输支持基于流的传输升级。</span><span class="sxs-lookup"><span data-stu-id="1d78b-126">Transports that use a stream-oriented protocol such as TCP and named pipes support stream-based transport upgrades.</span></span> <span data-ttu-id="1d78b-127">特别是 WCF 提供了安全升级。</span><span class="sxs-lookup"><span data-stu-id="1d78b-127">Specifically, WCF provides security upgrades.</span></span> <span data-ttu-id="1d78b-128">此传输安全的配置由此配置元素以及 [\<sslStreamSecurity>](sslstreamsecurity.md) 可配置并添加到自定义绑定中的进行封装</span><span class="sxs-lookup"><span data-stu-id="1d78b-128">The configuration of this transport security is encapsulated by this configuration element  as well as by [\<sslStreamSecurity>](sslstreamsecurity.md), which can be configured and added to a custom binding</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d78b-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d78b-129">See also</span></span>

- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Configuration.WindowsStreamSecurityElement>
- <xref:System.ServiceModel.Channels.WindowsStreamSecurityBindingElement>
- [<span data-ttu-id="1d78b-130">绑定</span><span class="sxs-lookup"><span data-stu-id="1d78b-130">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="1d78b-131">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="1d78b-131">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="1d78b-132">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="1d78b-132">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
