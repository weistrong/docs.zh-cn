---
description: 了解详细 <transport> 信息： <netNamedPipeBinding>
title: <transport> 的 <netNamedPipeBinding>
ms.date: 03/30/2017
ms.assetid: d9eff52d-4bde-4586-b56a-b0ec24611f8d
ms.openlocfilehash: a54c429bcac192ddc46df7232c33ab98bd1a4c58
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773480"
---
# <a name="transport-of-netnamedpipebinding"></a><span data-ttu-id="8d96a-103">\<transport> 的 \<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="8d96a-103">\<transport> of \<netNamedPipeBinding></span></span>

<span data-ttu-id="8d96a-104">定义命名管道的传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="8d96a-104">Defines the transport security settings for a named pipe.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netNamedPipeBinding>**](netnamedpipebinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-netnamedpipebinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="8d96a-105">语法</span><span class="sxs-lookup"><span data-stu-id="8d96a-105">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>
  <binding>
    <security mode="None/Transport">
      <transport protectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</netNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8d96a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8d96a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8d96a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d96a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8d96a-108">特性</span><span class="sxs-lookup"><span data-stu-id="8d96a-108">Attributes</span></span>  
  
|<span data-ttu-id="8d96a-109">属性</span><span class="sxs-lookup"><span data-stu-id="8d96a-109">Attribute</span></span>|<span data-ttu-id="8d96a-110">说明</span><span class="sxs-lookup"><span data-stu-id="8d96a-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8d96a-111">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="8d96a-111">protectionLevel</span></span>|<span data-ttu-id="8d96a-112">定义命名管道的保护级别。</span><span class="sxs-lookup"><span data-stu-id="8d96a-112">Defines protection level of the named pipe.</span></span> <span data-ttu-id="8d96a-113">消息签名降低了在消息传输过程中第三方对消息进行篡改的风险。</span><span class="sxs-lookup"><span data-stu-id="8d96a-113">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="8d96a-114">加密为传输过程提供了数据级保密功能。</span><span class="sxs-lookup"><span data-stu-id="8d96a-114">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="8d96a-115">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="8d96a-115">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="8d96a-116">-None：无保护。</span><span class="sxs-lookup"><span data-stu-id="8d96a-116">-   None: No protection.</span></span><br /><span data-ttu-id="8d96a-117">-Sign：对消息进行签名。</span><span class="sxs-lookup"><span data-stu-id="8d96a-117">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="8d96a-118">-EncryptAndSign：对消息进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="8d96a-118">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="8d96a-119">默认值为 EncryptAndSign。</span><span class="sxs-lookup"><span data-stu-id="8d96a-119">The default value is EncryptAndSign.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8d96a-120">子元素</span><span class="sxs-lookup"><span data-stu-id="8d96a-120">Child Elements</span></span>  

 <span data-ttu-id="8d96a-121">无</span><span class="sxs-lookup"><span data-stu-id="8d96a-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8d96a-122">父元素</span><span class="sxs-lookup"><span data-stu-id="8d96a-122">Parent Elements</span></span>  
  
|<span data-ttu-id="8d96a-123">元素</span><span class="sxs-lookup"><span data-stu-id="8d96a-123">Element</span></span>|<span data-ttu-id="8d96a-124">说明</span><span class="sxs-lookup"><span data-stu-id="8d96a-124">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-netnamedpipebinding.md)|<span data-ttu-id="8d96a-125">定义绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="8d96a-125">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8d96a-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d96a-126">See also</span></span>

- <xref:System.ServiceModel.NamedPipeTransportSecurity>
- <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement.Transport%2A>
- <xref:System.ServiceModel.NetNamedPipeSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>
- [<span data-ttu-id="8d96a-127">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="8d96a-127">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="8d96a-128">绑定</span><span class="sxs-lookup"><span data-stu-id="8d96a-128">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="8d96a-129">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="8d96a-129">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="8d96a-130">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="8d96a-130">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
