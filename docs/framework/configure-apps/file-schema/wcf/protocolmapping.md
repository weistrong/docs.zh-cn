---
description: 了解详细信息： <protocolMapping>
title: <protocolMapping>
ms.date: 03/30/2017
ms.assetid: 5076644b-1f33-4f26-9488-87de9fcda04c
ms.openlocfilehash: defdf3129122212dac9481dc5d8d48a0dfa94d72
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786910"
---
# \<protocolMapping>

<span data-ttu-id="d5176-102">表示一个配置节，用于定义传输协议方案（如 http、net.tcp、net.pipe 等）和 WCF 绑定之间的一组默认协议映射。</span><span class="sxs-lookup"><span data-stu-id="d5176-102">Represents a configuration section for defining a set of default protocol mapping between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and WCF bindings.</span></span> <span data-ttu-id="d5176-103">在运行时创建默认终结点时，Windows Communication Foundation (WCF) 会查看已配置的映射，并决定要将哪个绑定用于特定的地址。</span><span class="sxs-lookup"><span data-stu-id="d5176-103">When creating default endpoints at runtime, Windows Communication Foundation (WCF) looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<protocolMapping>**  
  
## <a name="syntax"></a><span data-ttu-id="d5176-104">语法</span><span class="sxs-lookup"><span data-stu-id="d5176-104">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d5176-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d5176-105">Attributes and Elements</span></span>  

 <span data-ttu-id="d5176-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5176-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d5176-107">特性</span><span class="sxs-lookup"><span data-stu-id="d5176-107">Attributes</span></span>  

 <span data-ttu-id="d5176-108">无。</span><span class="sxs-lookup"><span data-stu-id="d5176-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d5176-109">子元素</span><span class="sxs-lookup"><span data-stu-id="d5176-109">Child Elements</span></span>  
  
|<span data-ttu-id="d5176-110">元素</span><span class="sxs-lookup"><span data-stu-id="d5176-110">Element</span></span>|<span data-ttu-id="d5176-111">说明</span><span class="sxs-lookup"><span data-stu-id="d5176-111">Description</span></span>|  
|-------------|-----------------|  
|[\<filters>](filters-of-routing.md)|<span data-ttu-id="d5176-112">包含传输协议方案（如 http、net.tcp、net.pipe 等）和 WCF 绑定之间的默认协议映射。</span><span class="sxs-lookup"><span data-stu-id="d5176-112">Contains a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a WCF binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d5176-113">父元素</span><span class="sxs-lookup"><span data-stu-id="d5176-113">Parent Elements</span></span>  
  
|<span data-ttu-id="d5176-114">元素</span><span class="sxs-lookup"><span data-stu-id="d5176-114">Element</span></span>|<span data-ttu-id="d5176-115">说明</span><span class="sxs-lookup"><span data-stu-id="d5176-115">Description</span></span>|  
|-------------|-----------------|  
|[\<system.serviceModel>](system-servicemodel.md)|<span data-ttu-id="d5176-116">所有 WCF 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="d5176-116">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d5176-117">示例</span><span class="sxs-lookup"><span data-stu-id="d5176-117">Example</span></span>  

 <span data-ttu-id="d5176-118">下面的配置示例演示 machine.config 文件中的默认协议映射。</span><span class="sxs-lookup"><span data-stu-id="d5176-118">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="d5176-119">您可以通过修改 machine.config 文件在计算机级别重写此默认映射。</span><span class="sxs-lookup"><span data-stu-id="d5176-119">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="d5176-120">或者，如果您只希望在应用程序范围内重写此映射，则可以在应用程序配置文件中重写此节，并为单独的协议方案更改映射。</span><span class="sxs-lookup"><span data-stu-id="d5176-120">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
```xml  
<protocolMapping>
  <add scheme="http"
       binding="basicHttpBinding" />
  <add scheme="net.tcp"
       binding="netTcpBinding" />
  <add scheme="net.pipe"
       binding="netNamedPipeBinding" />
  <add scheme="net.msmq"
       binding="netMsmqBinding" />
</protocolMapping>
```  
  
## <a name="see-also"></a><span data-ttu-id="d5176-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5176-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>
