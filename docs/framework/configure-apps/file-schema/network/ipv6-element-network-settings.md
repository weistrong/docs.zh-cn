---
description: '了解详细信息： <ipv6> 元素 (网络设置) '
title: <ipv6> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/ipv6
- http://schemas.microsoft.com/.NetConfiguration/v2.0#ipv6
helpviewer_keywords:
- <ipv6> element
- ipv6 element
ms.assetid: 10b79aef-327b-4718-a892-e11f55e4d169
ms.openlocfilehash: 667acaebdb290140f67ea36020bb191cd1a44f34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698643"
---
# <a name="ipv6-element-network-settings"></a><span data-ttu-id="2281a-103">\<ipv6> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="2281a-103">\<ipv6> Element (Network Settings)</span></span>

<span data-ttu-id="2281a-104">使 Internet 协议版本 6 (IPv6) 来自类的过时成员的响应 <xref:System.Net.Dns> 。</span><span class="sxs-lookup"><span data-stu-id="2281a-104">Enables Internet Protocol version 6 (IPv6) responses from obsolete members of the <xref:System.Net.Dns> class.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<settings>**](settings-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<ipv6>**

## <a name="syntax"></a><span data-ttu-id="2281a-105">语法</span><span class="sxs-lookup"><span data-stu-id="2281a-105">Syntax</span></span>  
  
```xml  
<ipv6  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2281a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2281a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="2281a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2281a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2281a-108">特性</span><span class="sxs-lookup"><span data-stu-id="2281a-108">Attributes</span></span>  
  
|<span data-ttu-id="2281a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2281a-109">**Attribute**</span></span>|<span data-ttu-id="2281a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2281a-110">**Description**</span></span>|  
|-------------------|---------------------|  
|`enabled`|<span data-ttu-id="2281a-111">指定类的成员是否 <xref:System.Net.Dns> 返回 Internet 协议版本 6 (IPv6) 地址。</span><span class="sxs-lookup"><span data-stu-id="2281a-111">Specifies whether members of the <xref:System.Net.Dns> class return Internet Protocol version 6 (IPv6) addresses.</span></span> <span data-ttu-id="2281a-112">默认值是 `false`。</span><span class="sxs-lookup"><span data-stu-id="2281a-112">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2281a-113">子元素</span><span class="sxs-lookup"><span data-stu-id="2281a-113">Child Elements</span></span>  

 <span data-ttu-id="2281a-114">无。</span><span class="sxs-lookup"><span data-stu-id="2281a-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2281a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2281a-115">Parent Elements</span></span>  
  
|<span data-ttu-id="2281a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2281a-116">**Element**</span></span>|<span data-ttu-id="2281a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2281a-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="2281a-118">设置</span><span class="sxs-lookup"><span data-stu-id="2281a-118">settings</span></span>](settings-element-network-settings.md)|<span data-ttu-id="2281a-119">配置 <xref:System.Net> 命名空间的基本网络选项。</span><span class="sxs-lookup"><span data-stu-id="2281a-119">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2281a-120">备注</span><span class="sxs-lookup"><span data-stu-id="2281a-120">Remarks</span></span>  

 <span data-ttu-id="2281a-121">此设置为类的过时成员启用 IPv6 支持 <xref:System.Net.Dns> ： <xref:System.Net.Dns.BeginGetHostByName%2A> 、 <xref:System.Net.Dns.BeginResolve%2A> 、 <xref:System.Net.Dns.EndGetHostByName%2A> 、、、 <xref:System.Net.Dns.EndResolve%2A> <xref:System.Net.Dns.GetHostByAddress%2A> <xref:System.Net.Dns.GetHostByName%2A> 和 <xref:System.Net.Dns.Resolve%2A> 。</span><span class="sxs-lookup"><span data-stu-id="2281a-121">This setting enables IPv6 support for the obsolete members of the <xref:System.Net.Dns> class: <xref:System.Net.Dns.BeginGetHostByName%2A>, <xref:System.Net.Dns.BeginResolve%2A>, <xref:System.Net.Dns.EndGetHostByName%2A>, <xref:System.Net.Dns.EndResolve%2A>, <xref:System.Net.Dns.GetHostByAddress%2A>, <xref:System.Net.Dns.GetHostByName%2A>, and <xref:System.Net.Dns.Resolve%2A>.</span></span> <span data-ttu-id="2281a-122">对于命名空间的其他成员 <xref:System.Net?displayProperty=nameWithType> ，如果在操作系统中启用了 ipv6，则可能会返回 ipv6 地址。</span><span class="sxs-lookup"><span data-stu-id="2281a-122">For other members of the <xref:System.Net?displayProperty=nameWithType> namespace, IPv6 addresses may be returned if IPv6 is enabled in the operating system.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="2281a-123">配置文件</span><span class="sxs-lookup"><span data-stu-id="2281a-123">Configuration Files</span></span>  

 <span data-ttu-id="2281a-124">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="2281a-124">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2281a-125">示例</span><span class="sxs-lookup"><span data-stu-id="2281a-125">Example</span></span>  

 <span data-ttu-id="2281a-126">下面的示例演示如何为类启用 IPv6 支持 <xref:System.Net.Dns> 。</span><span class="sxs-lookup"><span data-stu-id="2281a-126">The following example shows how to enable IPv6 support for the <xref:System.Net.Dns> class.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <ipv6 enabled="true"/>  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="2281a-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="2281a-127">See also</span></span>

- <xref:System.Net?displayProperty=nameWithType>
- <xref:System.Net.Dns?displayProperty=nameWithType>
- <xref:System.Net.Sockets.Socket.OSSupportsIPv6%2A?displayProperty=nameWithType>
- [<span data-ttu-id="2281a-128">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="2281a-128">Network Settings Schema</span></span>](index.md)
