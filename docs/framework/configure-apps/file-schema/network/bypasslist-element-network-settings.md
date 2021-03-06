---
title: <bypasslist> 元素（网络设置）
description: <bypasslist>网络设置元素提供了一组正则表达式，用于描述在 .NET Framework 中不使用代理的地址。
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#bypasslist
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist
helpviewer_keywords:
- bypasslist element
- <bypasslist> element
ms.assetid: 124446b7-abb1-4e5e-a492-b64398f268f1
ms.openlocfilehash: 0a03b391c839b7255fdd423a305d474d0e48ad39
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102259351"
---
# <a name="bypasslist-element-network-settings"></a><span data-ttu-id="d3fe3-103">\<bypasslist> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="d3fe3-103">\<bypasslist> Element (Network Settings)</span></span>

<span data-ttu-id="d3fe3-104">提供了一组正则表达式，描述不使用代理的地址。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-104">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<defaultProxy>**](defaultproxy-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<bypasslist>**

## <a name="syntax"></a><span data-ttu-id="d3fe3-105">语法</span><span class="sxs-lookup"><span data-stu-id="d3fe3-105">Syntax</span></span>  
  
```xml  
<bypasslist>
</bypasslist>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d3fe3-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d3fe3-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d3fe3-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d3fe3-108">特性</span><span class="sxs-lookup"><span data-stu-id="d3fe3-108">Attributes</span></span>  

 <span data-ttu-id="d3fe3-109">无。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d3fe3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d3fe3-110">Child Elements</span></span>  
  
|<span data-ttu-id="d3fe3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3fe3-111">**Element**</span></span>|<span data-ttu-id="d3fe3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3fe3-112">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d3fe3-113">add</span><span class="sxs-lookup"><span data-stu-id="d3fe3-113">add</span></span>](add-element-for-bypasslist-network-settings.md)|<span data-ttu-id="d3fe3-114">将 IP 地址或 DNS 名称添加到代理跳过列表。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-114">Adds an IP address or DNS name to the proxy bypass list.</span></span>|  
|[<span data-ttu-id="d3fe3-115">clear</span><span class="sxs-lookup"><span data-stu-id="d3fe3-115">clear</span></span>](clear-element-for-bypasslist-network-settings.md)|<span data-ttu-id="d3fe3-116">清除跳过列表。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-116">Clears the bypass list.</span></span>|  
|[<span data-ttu-id="d3fe3-117">删除</span><span class="sxs-lookup"><span data-stu-id="d3fe3-117">remove</span></span>](remove-element-for-bypasslist-network-settings.md)|<span data-ttu-id="d3fe3-118">从代理跳过列表中删除 IP 地址或 DNS 名称。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-118">Removes an IP address or DNS name from the proxy bypass list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d3fe3-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d3fe3-119">Parent Elements</span></span>  
  
|<span data-ttu-id="d3fe3-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3fe3-120">**Element**</span></span>|<span data-ttu-id="d3fe3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3fe3-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d3fe3-122">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="d3fe3-122">defaultProxy</span></span>](defaultproxy-element-network-settings.md)|<span data-ttu-id="d3fe3-123">配置超文本传输协议 (HTTP) 代理服务器。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-123">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d3fe3-124">备注</span><span class="sxs-lookup"><span data-stu-id="d3fe3-124">Remarks</span></span>  

 <span data-ttu-id="d3fe3-125">绕过列表包含用于描述 <xref:System.Net.WebRequest> 实例直接访问而不是通过代理服务器访问的 uri 的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-125">The bypass list contains regular expressions that describe URIs that <xref:System.Net.WebRequest> instances access directly instead of through the proxy server.</span></span>  
  
 <span data-ttu-id="d3fe3-126">为此元素指定正则表达式时，应格外小心。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-126">You should use caution when specifying a regular expression for this element.</span></span> <span data-ttu-id="d3fe3-127">正则表达式 `[a-z]+\\.contoso\\.com` 匹配 contoso.com 域中的任何主机，但它还匹配 contoso.com.cpandl.com 域中的任何主机。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-127">The regular expression `[a-z]+\\.contoso\\.com` matches any host in the contoso.com domain, but it also matches any host in the contoso.com.cpandl.com domain.</span></span> <span data-ttu-id="d3fe3-128">若要仅匹配 contoso.com 域中的主机，请使用锚 (`$`) ： `[a-z]+\\.contoso\\.com$` 。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-128">To match only a host in the contoso.com domain, use an anchor (`$`): `[a-z]+\\.contoso\\.com$`.</span></span>
  
 <span data-ttu-id="d3fe3-129">有关正则表达式的详细信息，请参阅。[.NET Framework 正则表达式](../../../../standard/base-types/regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-129">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../standard/base-types/regular-expressions.md).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="d3fe3-130">配置文件</span><span class="sxs-lookup"><span data-stu-id="d3fe3-130">Configuration Files</span></span>  

 <span data-ttu-id="d3fe3-131">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-131">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3fe3-132">示例</span><span class="sxs-lookup"><span data-stu-id="d3fe3-132">Example</span></span>  

 <span data-ttu-id="d3fe3-133">下面的示例将两个地址添加到跳过列表。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-133">The following example adds two addresses to the bypass list.</span></span> <span data-ttu-id="d3fe3-134">首先，将跳过 contoso.com 域中所有服务器的代理;第二种方式是跳过其 IP 地址以192.168 开头的所有服务器的代理。</span><span class="sxs-lookup"><span data-stu-id="d3fe3-134">The first bypasses the proxy for all servers in the contoso.com domain; the second bypasses the proxy for all servers whose IP addresses begin with 192.168.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="d3fe3-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3fe3-135">See also</span></span>

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="d3fe3-136">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="d3fe3-136">Network Settings Schema</span></span>](index.md)
