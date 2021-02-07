---
description: '详细了解： <clear> bypasslist 的元素 (网络设置) '
title: bypasslist 的 <clear> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- clear element, bypasslist
- <clear> element, bypasslist
- <bypasslist>, clear element
- bypasslist, clear element
ms.assetid: 301584ca-a914-4100-b180-3b288d3b099e
ms.openlocfilehash: 4ddb66c837c55391a19826c44c6df7a3e88c8e0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729884"
---
# <a name="clear-element-for-bypasslist-network-settings"></a><span data-ttu-id="5010f-103">bypasslist 的 \<clear> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="5010f-103">\<clear> Element for bypasslist (Network Settings)</span></span>

<span data-ttu-id="5010f-104">清除代理跳过列表。</span><span class="sxs-lookup"><span data-stu-id="5010f-104">Clears the proxy bypass list.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<defaultProxy>**](defaultproxy-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<bypasslist>**](bypasslist-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a><span data-ttu-id="5010f-105">语法</span><span class="sxs-lookup"><span data-stu-id="5010f-105">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5010f-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5010f-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5010f-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5010f-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5010f-108">特性</span><span class="sxs-lookup"><span data-stu-id="5010f-108">Attributes</span></span>  

 <span data-ttu-id="5010f-109">无。</span><span class="sxs-lookup"><span data-stu-id="5010f-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="5010f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5010f-110">Child Elements</span></span>  

 <span data-ttu-id="5010f-111">无。</span><span class="sxs-lookup"><span data-stu-id="5010f-111">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5010f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5010f-112">Parent Elements</span></span>  
  
|<span data-ttu-id="5010f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5010f-113">**Element**</span></span>|<span data-ttu-id="5010f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5010f-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="5010f-115">bypasslist</span><span class="sxs-lookup"><span data-stu-id="5010f-115">bypasslist</span></span>](bypasslist-element-network-settings.md)|<span data-ttu-id="5010f-116">提供了一组正则表达式，描述不使用代理的地址。</span><span class="sxs-lookup"><span data-stu-id="5010f-116">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5010f-117">备注</span><span class="sxs-lookup"><span data-stu-id="5010f-117">Remarks</span></span>  

 <span data-ttu-id="5010f-118">`clear`元素清除跳过列表中的所有条目。</span><span class="sxs-lookup"><span data-stu-id="5010f-118">The `clear` element clears all entries from the bypass list.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="5010f-119">配置文件</span><span class="sxs-lookup"><span data-stu-id="5010f-119">Configuration Files</span></span>  

 <span data-ttu-id="5010f-120">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="5010f-120">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5010f-121">示例</span><span class="sxs-lookup"><span data-stu-id="5010f-121">Example</span></span>  

 <span data-ttu-id="5010f-122">下面的示例清除了跳过列表，并将两个地址添加到了跳过列表。</span><span class="sxs-lookup"><span data-stu-id="5010f-122">The following example clears the bypass list and then adds two addresses to the bypass list.</span></span> <span data-ttu-id="5010f-123">首先，将跳过 contoso.com 域中所有服务器的代理;第二种方式是跳过其 IP 地址以192.168 开头的所有服务器的代理。</span><span class="sxs-lookup"><span data-stu-id="5010f-123">The first bypasses the proxy for all servers in the contoso.com domain; the second bypasses the proxy for all servers whose IP address begins with 192.168.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
         <clear/>  
        <add address="[a-z]+\.contoso\.com$" />  
        <add address="192\.168\.\d{1,3}\.\d{1,3}" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="5010f-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="5010f-124">See also</span></span>

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="5010f-125">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="5010f-125">Network Settings Schema</span></span>](index.md)
