---
description: 了解详细信息： <compositeDuplex>
title: <compositeDuplex>
ms.date: 03/30/2017
ms.assetid: 725004d1-ce88-4405-a220-78e89844f81f
ms.openlocfilehash: 0a9ec47027618a5f4fb30b627ccb9ad04c547f48
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782177"
---
# \<compositeDuplex>

<span data-ttu-id="756e6-102">定义绑定元素，客户端在必须公开一个终结点以使服务可以将消息发送回客户端时使用此元素。</span><span class="sxs-lookup"><span data-stu-id="756e6-102">Defines the binding element that is used when the client must expose an endpoint for the service to send messages back to the client.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<compositeDuplex>**  
  
## <a name="syntax"></a><span data-ttu-id="756e6-103">语法</span><span class="sxs-lookup"><span data-stu-id="756e6-103">Syntax</span></span>  
  
```xml  
<compositeDuplex clientBaseAddress="URI" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="756e6-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="756e6-104">Attributes and Elements</span></span>  

 <span data-ttu-id="756e6-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="756e6-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="756e6-106">特性</span><span class="sxs-lookup"><span data-stu-id="756e6-106">Attributes</span></span>  
  
|<span data-ttu-id="756e6-107">属性</span><span class="sxs-lookup"><span data-stu-id="756e6-107">Attribute</span></span>|<span data-ttu-id="756e6-108">说明</span><span class="sxs-lookup"><span data-stu-id="756e6-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="756e6-109">clientBaseAddress</span><span class="sxs-lookup"><span data-stu-id="756e6-109">clientBaseAddress</span></span>|<span data-ttu-id="756e6-110">一个在双工模式下设置反向通道地址的 URI。</span><span class="sxs-lookup"><span data-stu-id="756e6-110">A URI that sets the address of the back channel in duplex mode.</span></span> <span data-ttu-id="756e6-111">服务使用该地址与客户端进行联系和建立连接。</span><span class="sxs-lookup"><span data-stu-id="756e6-111">The service uses this address to make contact and establish a connection with the client.</span></span><br /><br /> <span data-ttu-id="756e6-112">如果未设置此属性，则生成默认地址 " `full qualified name+default port\TemporaryIndigoAddress\guid` "。</span><span class="sxs-lookup"><span data-stu-id="756e6-112">If this attribute is not set, a default address "`full qualified name+default port\TemporaryIndigoAddress\guid`" is generated.</span></span> <span data-ttu-id="756e6-113">默认值为 `null`。</span><span class="sxs-lookup"><span data-stu-id="756e6-113">The default is `null`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="756e6-114">子元素</span><span class="sxs-lookup"><span data-stu-id="756e6-114">Child Elements</span></span>  

 <span data-ttu-id="756e6-115">无</span><span class="sxs-lookup"><span data-stu-id="756e6-115">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="756e6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="756e6-116">Parent Elements</span></span>  
  
|<span data-ttu-id="756e6-117">元素</span><span class="sxs-lookup"><span data-stu-id="756e6-117">Element</span></span>|<span data-ttu-id="756e6-118">说明</span><span class="sxs-lookup"><span data-stu-id="756e6-118">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="756e6-119">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="756e6-119">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="756e6-120">备注</span><span class="sxs-lookup"><span data-stu-id="756e6-120">Remarks</span></span>  

 <span data-ttu-id="756e6-121">此配置元素与本身不允许进行双工通信的传输（例如，HTTP）一起使用。</span><span class="sxs-lookup"><span data-stu-id="756e6-121">This configuration element is used with transports that do not allow duplex communications natively, for example, HTTP.</span></span> <span data-ttu-id="756e6-122">与此相反，TCP 本身允许进行双工通信，并且不要求服务在将消息发送回客户端时使用此绑定元素。</span><span class="sxs-lookup"><span data-stu-id="756e6-122">TCP, by contrast, allows duplex communications natively, and does not require the use of this binding element for the service to send messages back to a client.</span></span>  
  
 <span data-ttu-id="756e6-123">客户端必须公开一个地址，以便服务进行联系和建立连接。</span><span class="sxs-lookup"><span data-stu-id="756e6-123">The client must expose an address for the service to make contact and establish a connection.</span></span> <span data-ttu-id="756e6-124">此客户端地址由 `clientBaseAddress` 属性提供。</span><span class="sxs-lookup"><span data-stu-id="756e6-124">This client address is provided by the `clientBaseAddress` attribute.</span></span> <span data-ttu-id="756e6-125">请注意，如果用户未显式设置 ClientBaseAddress，则 Windows Communication Foundation (WCF) 将自动生成一个 ClientBaseAddress。</span><span class="sxs-lookup"><span data-stu-id="756e6-125">Note that Windows Communication Foundation (WCF) auto-generates a ClientBaseAddress if one is not explicitly set by the user.</span></span>  
  
## <a name="example"></a><span data-ttu-id="756e6-126">示例</span><span class="sxs-lookup"><span data-stu-id="756e6-126">Example</span></span>  
  
```xml  
<compositeDuplex clientBaseAddress="http://www.contoso.com" />
```  
  
## <a name="see-also"></a><span data-ttu-id="756e6-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="756e6-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.CompositeDuplexElement>
- <xref:System.ServiceModel.Channels.CompositeDuplexBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="756e6-128">绑定</span><span class="sxs-lookup"><span data-stu-id="756e6-128">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="756e6-129">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="756e6-129">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="756e6-130">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="756e6-130">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
