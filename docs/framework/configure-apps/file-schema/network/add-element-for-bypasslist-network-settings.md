---
description: '详细了解： <add> bypasslist 的元素 (网络设置) '
title: bypasslist 的 <add> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
helpviewer_keywords:
- <bypasslist>, add element
- bypasslist, add element
- <add> element, bypasslist
- add element, bypasslist
ms.assetid: a0b86e28-86b4-4497-abe8-d5fd614c7926
ms.openlocfilehash: 6bbd42cdf5d3b9bc31326b619cde96cfac0c755a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698630"
---
# <a name="add-element-for-bypasslist-network-settings"></a><span data-ttu-id="be2f3-103">bypasslist 的 \<add> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="be2f3-103">\<add> Element for bypasslist (Network Settings)</span></span>

<span data-ttu-id="be2f3-104">将 IP 地址或 DNS 名称添加到代理跳过列表。</span><span class="sxs-lookup"><span data-stu-id="be2f3-104">Adds an IP address or DNS name to the proxy bypass list.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[**\<defaultProxy>**](defaultproxy-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<bypasslist>**](bypasslist-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="be2f3-105">语法</span><span class="sxs-lookup"><span data-stu-id="be2f3-105">Syntax</span></span>  
  
```xml  
<add
  address="regular expression"
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="be2f3-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="be2f3-106">Attributes and Elements</span></span>  

 <span data-ttu-id="be2f3-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be2f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="be2f3-108">特性</span><span class="sxs-lookup"><span data-stu-id="be2f3-108">Attributes</span></span>  
  
|<span data-ttu-id="be2f3-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="be2f3-109">**Attribute**</span></span>|<span data-ttu-id="be2f3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="be2f3-110">**Description**</span></span>|  
|-------------------|---------------------|  
|<span data-ttu-id="be2f3-111">**address**</span><span class="sxs-lookup"><span data-stu-id="be2f3-111">**address**</span></span>|<span data-ttu-id="be2f3-112">描述 IP 地址或 DNS 名称的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="be2f3-112">A regular expression describing an IP address or DNS name.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="be2f3-113">子元素</span><span class="sxs-lookup"><span data-stu-id="be2f3-113">Child Elements</span></span>  

 <span data-ttu-id="be2f3-114">无。</span><span class="sxs-lookup"><span data-stu-id="be2f3-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="be2f3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="be2f3-115">Parent Elements</span></span>  
  
|<span data-ttu-id="be2f3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="be2f3-116">**Element**</span></span>|<span data-ttu-id="be2f3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="be2f3-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="be2f3-118">bypasslist</span><span class="sxs-lookup"><span data-stu-id="be2f3-118">bypasslist</span></span>](bypasslist-element-network-settings.md)|<span data-ttu-id="be2f3-119">提供了一组正则表达式，描述不使用代理的地址。</span><span class="sxs-lookup"><span data-stu-id="be2f3-119">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be2f3-120">备注</span><span class="sxs-lookup"><span data-stu-id="be2f3-120">Remarks</span></span>  

 <span data-ttu-id="be2f3-121">`add`元素将描述 IP 地址或 DNS 服务器名称的正则表达式插入绕过代理服务器的地址列表。</span><span class="sxs-lookup"><span data-stu-id="be2f3-121">The `add` element inserts regular expressions describing IP addresses or DNS server names to the list of addresses that bypass a proxy server.</span></span>  
  
 <span data-ttu-id="be2f3-122">特性的值 `address` 应为描述一组 IP 地址或主机名的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="be2f3-122">The value of the `address` attribute should be a regular expression that describes a set of IP addresses or host names.</span></span>  
  
 <span data-ttu-id="be2f3-123">为此元素指定正则表达式时，应格外小心。</span><span class="sxs-lookup"><span data-stu-id="be2f3-123">You should use caution when specifying a regular expression for this element.</span></span> <span data-ttu-id="be2f3-124">正则表达式 "[a-z] + \\ \\ .com" 与 contoso.com 域中的任何主机匹配，但它还匹配 contoso.com.cpandl.com 域中的任何主机。</span><span class="sxs-lookup"><span data-stu-id="be2f3-124">The regular expression "[a-z]+\\.contoso\\.com" matches any host in the contoso.com domain, but it also matches any host in the contoso.com.cpandl.com domain.</span></span> <span data-ttu-id="be2f3-125">若要仅匹配 contoso.com 域中的主机，请使用锚 ( "$" ) ： "[a-z] + \\ \\ .com $"。</span><span class="sxs-lookup"><span data-stu-id="be2f3-125">To match only a host in the contoso.com domain, use an anchor ("$"): "[a-z]+\\.contoso\\.com$".</span></span>  
  
 <span data-ttu-id="be2f3-126">有关正则表达式的详细信息，请参阅。[.NET Framework 正则表达式](../../../../standard/base-types/regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="be2f3-126">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../standard/base-types/regular-expressions.md).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="be2f3-127">配置文件</span><span class="sxs-lookup"><span data-stu-id="be2f3-127">Configuration Files</span></span>  

 <span data-ttu-id="be2f3-128">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="be2f3-128">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="be2f3-129">示例</span><span class="sxs-lookup"><span data-stu-id="be2f3-129">Example</span></span>  

 <span data-ttu-id="be2f3-130">下面的示例将两个地址添加到跳过列表。</span><span class="sxs-lookup"><span data-stu-id="be2f3-130">The following example adds two addresses to the bypass list.</span></span> <span data-ttu-id="be2f3-131">首先，将跳过 contoso.com 域中所有服务器的代理;第二种方式是跳过其 IP 地址以192.168 开头的所有服务器的代理。</span><span class="sxs-lookup"><span data-stu-id="be2f3-131">The first bypasses the proxy for all servers in the contoso.com domain; the second bypasses the proxy for all servers whose IP address begins with 192.168.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
        <add address="[a-z]+\.contoso\.com$" />  
        <add address="192\.168\.\d{1,3}\.\d{1,3}" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="be2f3-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="be2f3-132">See also</span></span>

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="be2f3-133">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="be2f3-133">Network Settings Schema</span></span>](index.md)
