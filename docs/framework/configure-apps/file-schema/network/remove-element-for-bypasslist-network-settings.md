---
description: '详细了解： <remove> bypasslist 的元素 (网络设置) '
title: bypasslist 的 <remove> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- <bypasslist>, remove element
- remove element, bypasslist
- bypasslist, remove element
- remove element, bypasslist
ms.assetid: 61dcfb4a-e3d9-4abf-a2cd-7d685fe2f64b
ms.openlocfilehash: 48441f1b402b339a1bd2ea069678afb4b1d5f2e1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740283"
---
# <a name="remove-element-for-bypasslist-network-settings"></a><span data-ttu-id="59faa-103">bypasslist 的 \<remove> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="59faa-103">\<remove> Element for bypasslist (Network Settings)</span></span>

<span data-ttu-id="59faa-104">从代理跳过列表中删除 IP 地址或 DNS 名称。</span><span class="sxs-lookup"><span data-stu-id="59faa-104">Removes an IP address or DNS name from the proxy bypass list.</span></span>

[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[**\<defaultProxy>**](defaultproxy-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<bypasslist>**](bypasslist-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**  

## <a name="syntax"></a><span data-ttu-id="59faa-105">语法</span><span class="sxs-lookup"><span data-stu-id="59faa-105">Syntax</span></span>

```xml
<remove
  address="regular expression"
/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="59faa-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="59faa-106">Attributes and Elements</span></span>

<span data-ttu-id="59faa-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="59faa-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="59faa-108">特性</span><span class="sxs-lookup"><span data-stu-id="59faa-108">Attributes</span></span>

|<span data-ttu-id="59faa-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="59faa-109">**Attribute**</span></span>|<span data-ttu-id="59faa-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="59faa-110">**Description**</span></span>|
|-------------------|---------------------|
|`address`|<span data-ttu-id="59faa-111">描述 IP 地址或 DNS 名称的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="59faa-111">A regular expression describing an IP address or DNS name.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="59faa-112">子元素</span><span class="sxs-lookup"><span data-stu-id="59faa-112">Child Elements</span></span>

<span data-ttu-id="59faa-113">无。</span><span class="sxs-lookup"><span data-stu-id="59faa-113">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="59faa-114">父元素</span><span class="sxs-lookup"><span data-stu-id="59faa-114">Parent Elements</span></span>

|<span data-ttu-id="59faa-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="59faa-115">**Element**</span></span>|<span data-ttu-id="59faa-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="59faa-116">**Description**</span></span>|
|-----------------|---------------------|
|[<span data-ttu-id="59faa-117">bypasslist</span><span class="sxs-lookup"><span data-stu-id="59faa-117">bypasslist</span></span>](bypasslist-element-network-settings.md)|<span data-ttu-id="59faa-118">提供了一组正则表达式，描述不使用代理的地址。</span><span class="sxs-lookup"><span data-stu-id="59faa-118">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|

## <a name="remarks"></a><span data-ttu-id="59faa-119">备注</span><span class="sxs-lookup"><span data-stu-id="59faa-119">Remarks</span></span>

<span data-ttu-id="59faa-120">`remove`元素从绕过代理服务器的地址列表中删除描述 IP 地址或 DNS 服务器名称的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="59faa-120">The `remove` element removes regular expressions describing IP addresses or DNS server names from the list of addresses that bypass a proxy server.</span></span> <span data-ttu-id="59faa-121">地址在配置文件中或配置层次结构中的更高级别定义。</span><span class="sxs-lookup"><span data-stu-id="59faa-121">The addresses were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>

<span data-ttu-id="59faa-122">特性的值 `address` 应为描述一组 IP 地址或主机名的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="59faa-122">The value for the `address` attribute should be a regular expression that describes a set of IP addresses or host names.</span></span>

<span data-ttu-id="59faa-123">有关正则表达式的详细信息，请参阅。[.NET Framework 正则表达式](../../../../standard/base-types/regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="59faa-123">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../standard/base-types/regular-expressions.md).</span></span>

## <a name="configuration-files"></a><span data-ttu-id="59faa-124">配置文件</span><span class="sxs-lookup"><span data-stu-id="59faa-124">Configuration Files</span></span>

<span data-ttu-id="59faa-125">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="59faa-125">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>

## <a name="example"></a><span data-ttu-id="59faa-126">示例</span><span class="sxs-lookup"><span data-stu-id="59faa-126">Example</span></span>

<span data-ttu-id="59faa-127">下面的示例删除 adventure-works.com 域的任何先前定义，然后将 contoso.com 域添加到跳过列表。</span><span class="sxs-lookup"><span data-stu-id="59faa-127">The following example removes any previous definition for the adventure-works.com domain, and then adds the contoso.com domain to the bypass list.</span></span>

```xml
<configuration>
  <system.net>
    <defaultProxy>
      <bypasslist>
        <remove address="[a-z]+\.adventure-works\.com$" />
        <add address="[a-z]+\.contoso\.com$" />
      </bypasslist>
    </defaultProxy>
  </system.net>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="59faa-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="59faa-128">See also</span></span>

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="59faa-129">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="59faa-129">Network Settings Schema</span></span>](index.md)
