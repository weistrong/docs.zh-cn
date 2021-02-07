---
description: '详细了解： <add> webRequestModules 的元素 (网络设置) '
title: webRequestModules 的 <add> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
helpviewer_keywords:
- <webRequestModules>, add element
- webRequestModules, add element
- add element, webRequestModules
- <add> element, webRequestModules
ms.assetid: 47ec4adc-f39f-4bcd-8680-1ec21fd26890
ms.openlocfilehash: 1edb63a1e1095bb4b3c3d749fd389ffaad5ddf9a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729885"
---
# <a name="add-element-for-webrequestmodules-network-settings"></a><span data-ttu-id="30db2-103">webRequestModules 的 \<add> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="30db2-103">\<add> Element for webRequestModules (Network Settings)</span></span>

<span data-ttu-id="30db2-104">向应用程序添加自定义 Web 请求模块。</span><span class="sxs-lookup"><span data-stu-id="30db2-104">Adds a custom Web request module to the application.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<webRequestModules>**](webrequestmodules-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**

## <a name="syntax"></a><span data-ttu-id="30db2-105">语法</span><span class="sxs-lookup"><span data-stu-id="30db2-105">Syntax</span></span>  
  
```xml  
<add
  prefix="URI prefix"
  type="type_fullname, assembly_fullname"
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="30db2-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="30db2-106">Attributes and Elements</span></span>  

 <span data-ttu-id="30db2-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="30db2-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="30db2-108">特性</span><span class="sxs-lookup"><span data-stu-id="30db2-108">Attributes</span></span>  
  
|<span data-ttu-id="30db2-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="30db2-109">**Attribute**</span></span>|<span data-ttu-id="30db2-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="30db2-110">**Description**</span></span>|  
|-------------------|---------------------|  
|`prefix`|<span data-ttu-id="30db2-111">此 Web 请求模块处理的请求的 URI 前缀。</span><span class="sxs-lookup"><span data-stu-id="30db2-111">The URI prefix for requests handled by this Web request module.</span></span>|  
|`type`|<span data-ttu-id="30db2-112">完全限定的类型名称 (由) 的 <xref:System.Type.FullName%2A> 属性和程序集名称指示 (由 <xref:System.Reflection.Assembly.FullName%2A> 实现此 Web 请求模块的由逗号分隔的) 属性指示。</span><span class="sxs-lookup"><span data-stu-id="30db2-112">The fully qualified type name (indicated by the <xref:System.Type.FullName%2A> property) and the assembly name (indicated by the <xref:System.Reflection.Assembly.FullName%2A> property), separated by a comma, that implements this Web request module.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="30db2-113">子元素</span><span class="sxs-lookup"><span data-stu-id="30db2-113">Child Elements</span></span>  

 <span data-ttu-id="30db2-114">无。</span><span class="sxs-lookup"><span data-stu-id="30db2-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="30db2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="30db2-115">Parent Elements</span></span>  
  
|<span data-ttu-id="30db2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="30db2-116">**Element**</span></span>|<span data-ttu-id="30db2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="30db2-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="30db2-118">webRequestModules</span><span class="sxs-lookup"><span data-stu-id="30db2-118">webRequestModules</span></span>](webrequestmodules-element-network-settings.md)|<span data-ttu-id="30db2-119">指定用于从网络主机请求信息的模块。</span><span class="sxs-lookup"><span data-stu-id="30db2-119">Specifies modules to use to request information from network hosts.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="30db2-120">备注</span><span class="sxs-lookup"><span data-stu-id="30db2-120">Remarks</span></span>  

 <span data-ttu-id="30db2-121">`prefix`特性定义使用指定 Web 请求模块的 URI 前缀。</span><span class="sxs-lookup"><span data-stu-id="30db2-121">The `prefix` attribute defines the URI prefix that uses the specified Web request module.</span></span> <span data-ttu-id="30db2-122">通常会将 Web 请求模块注册为处理特定协议（如 HTTP 或 FTP），但可以注册它来处理对服务器上特定服务器或路径的请求。</span><span class="sxs-lookup"><span data-stu-id="30db2-122">Web request modules are typically registered to handle a specific protocol, such as HTTP or FTP, but can be registered to handle a request to a specific server or path on a server.</span></span>  
  
 <span data-ttu-id="30db2-123">当 URI 匹配前缀传递到方法时，将创建 Web 请求模块 <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="30db2-123">The Web request module is created when a URI matching prefix is passed to the <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="30db2-124">特性的值 `prefix` 应为有效 URI 的前导字符。</span><span class="sxs-lookup"><span data-stu-id="30db2-124">The value for the `prefix` attribute should be the leading characters of a valid URI.</span></span> <span data-ttu-id="30db2-125">例如，`http` 或 `http://www.contoso.com`。</span><span class="sxs-lookup"><span data-stu-id="30db2-125">For example, `http` or `http://www.contoso.com`.</span></span>
  
 <span data-ttu-id="30db2-126">特性的值 `type` 应为有效的类型名称和相应的程序集名称，用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="30db2-126">The value for the `type` attribute should be a valid type name and corresponding assembly name, separated by a comma.</span></span>
  
## <a name="configuration-files"></a><span data-ttu-id="30db2-127">配置文件</span><span class="sxs-lookup"><span data-stu-id="30db2-127">Configuration Files</span></span>  

 <span data-ttu-id="30db2-128">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="30db2-128">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="30db2-129">示例</span><span class="sxs-lookup"><span data-stu-id="30db2-129">Example</span></span>  

 <span data-ttu-id="30db2-130">下面的示例为 HTTP 注册自定义 Web 请求模块。</span><span class="sxs-lookup"><span data-stu-id="30db2-130">The following example registers a custom Web request module for HTTP.</span></span> <span data-ttu-id="30db2-131">应将版本和 PublicKeyToken 的值替换为指定模块的正确值。</span><span class="sxs-lookup"><span data-stu-id="30db2-131">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="30db2-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="30db2-132">See also</span></span>

- <xref:System.Net.WebRequest>
- [<span data-ttu-id="30db2-133">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="30db2-133">Network Settings Schema</span></span>](index.md)
