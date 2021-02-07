---
description: '了解详细信息： <settings> 元素 (网络设置) '
title: <settings> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#settings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings
helpviewer_keywords:
- settings element
- <settings> element
ms.assetid: 189ce989-c39b-427d-b004-6b82a668b931
ms.openlocfilehash: e6ed242e68ac9a9e2c20067d66681bbcd51fcc50
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712969"
---
# <a name="settings-element-network-settings"></a><span data-ttu-id="6f480-103">\<settings> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="6f480-103">\<settings> Element (Network Settings)</span></span>

<span data-ttu-id="6f480-104">配置 <xref:System.Net?displayProperty=nameWithType> 命名空间的基本网络选项。</span><span class="sxs-lookup"><span data-stu-id="6f480-104">Configures basic network options for the <xref:System.Net?displayProperty=nameWithType> namespace.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<settings>**

## <a name="syntax"></a><span data-ttu-id="6f480-105">语法</span><span class="sxs-lookup"><span data-stu-id="6f480-105">Syntax</span></span>  
  
```xml  
<settings>  
  <httpListener>...</httpListener>  
  <httpWebRequest>...</httpWebRequest>  
  <ipv6>...</ipv6>  
  <performanceCounters>...</performanceCounters>  
  <servicePointManager>...</servicePointManager>  
  <socket>...</socket>  
  <webProxyScript>...</webProxyScript>  
</settings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6f480-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6f480-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6f480-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f480-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6f480-108">特性</span><span class="sxs-lookup"><span data-stu-id="6f480-108">Attributes</span></span>  

 <span data-ttu-id="6f480-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f480-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6f480-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f480-110">Child Elements</span></span>  
  
|<span data-ttu-id="6f480-111">元素</span><span class="sxs-lookup"><span data-stu-id="6f480-111">Element</span></span>|<span data-ttu-id="6f480-112">说明</span><span class="sxs-lookup"><span data-stu-id="6f480-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6f480-113">httpListener</span><span class="sxs-lookup"><span data-stu-id="6f480-113">httpListener</span></span>](httplistener-element-network-settings.md)|<span data-ttu-id="6f480-114">自定义类使用的参数 <xref:System.Net.HttpListener> 。</span><span class="sxs-lookup"><span data-stu-id="6f480-114">Customizes parameters used by the <xref:System.Net.HttpListener> class.</span></span>|  
|[<span data-ttu-id="6f480-115">httpWebRequest</span><span class="sxs-lookup"><span data-stu-id="6f480-115">httpWebRequest</span></span>](httpwebrequest-element-network-settings.md)|<span data-ttu-id="6f480-116">自定义 Web 请求参数。</span><span class="sxs-lookup"><span data-stu-id="6f480-116">Customizes Web request parameters.</span></span>|  
|[<span data-ttu-id="6f480-117">ipv6</span><span class="sxs-lookup"><span data-stu-id="6f480-117">ipv6</span></span>](ipv6-element-network-settings.md)|<span data-ttu-id="6f480-118">启用 Internet 协议版本 6 (IPv6) 支持。</span><span class="sxs-lookup"><span data-stu-id="6f480-118">Enables Internet Protocol version 6 (IPv6) support.</span></span>|  
|[<span data-ttu-id="6f480-119">\<performanceCounter> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="6f480-119">\<performanceCounter> Element (Network Settings)</span></span>](performancecounter-element-network-settings.md)|<span data-ttu-id="6f480-120">启用网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="6f480-120">Enables network performance counters.</span></span>|  
|[<span data-ttu-id="6f480-121">servicePointManager</span><span class="sxs-lookup"><span data-stu-id="6f480-121">servicePointManager</span></span>](servicepointmanager-element-network-settings.md)|<span data-ttu-id="6f480-122">配置与网络资源的连接。</span><span class="sxs-lookup"><span data-stu-id="6f480-122">Configures connections to network resources.</span></span>|  
|[<span data-ttu-id="6f480-123">片</span><span class="sxs-lookup"><span data-stu-id="6f480-123">socket</span></span>](socket-element-network-settings.md)|<span data-ttu-id="6f480-124">指定套接字操作是否使用完成端口。</span><span class="sxs-lookup"><span data-stu-id="6f480-124">Specifies whether socket operations use completion ports.</span></span>|  
|[<span data-ttu-id="6f480-125">\<webProxyScript> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="6f480-125">\<webProxyScript> Element (Network Settings)</span></span>](webproxyscript-element-network-settings.md)|<span data-ttu-id="6f480-126">配置用于发现 Web 代理的脚本的特征。</span><span class="sxs-lookup"><span data-stu-id="6f480-126">Configures the characteristics of the script used to discover Web proxies.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6f480-127">父元素</span><span class="sxs-lookup"><span data-stu-id="6f480-127">Parent Elements</span></span>  
  
|<span data-ttu-id="6f480-128">元素</span><span class="sxs-lookup"><span data-stu-id="6f480-128">Element</span></span>|<span data-ttu-id="6f480-129">说明</span><span class="sxs-lookup"><span data-stu-id="6f480-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6f480-130">system.net</span><span class="sxs-lookup"><span data-stu-id="6f480-130">system.net</span></span>](system-net-element-network-settings.md)|<span data-ttu-id="6f480-131">包含指定 .NET Framework 如何连接到网络的设置。</span><span class="sxs-lookup"><span data-stu-id="6f480-131">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6f480-132">备注</span><span class="sxs-lookup"><span data-stu-id="6f480-132">Remarks</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="6f480-133">配置文件</span><span class="sxs-lookup"><span data-stu-id="6f480-133">Configuration Files</span></span>  

 <span data-ttu-id="6f480-134">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="6f480-134">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f480-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="6f480-135">See also</span></span>

- <xref:System.Net?displayProperty=nameWithType>
- [<span data-ttu-id="6f480-136">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="6f480-136">Network Settings Schema</span></span>](index.md)
