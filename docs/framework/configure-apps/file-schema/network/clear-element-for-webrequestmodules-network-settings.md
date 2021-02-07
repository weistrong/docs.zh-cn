---
description: '详细了解： <clear> webRequestModules 的元素 (网络设置) '
title: webRequestModules 的 <clear> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- <clear> element, webRequestModules
- <webRequestModules>, clear element
- webRequestModules, clear element
- clear element, webRequestModules
ms.assetid: 48f38bcb-f30c-4b74-a8f0-1a3caf1aa96f
ms.openlocfilehash: 0782bf9edeafed2d61a368c3f6a8b37ef226c990
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740413"
---
# <a name="clear-element-for-webrequestmodules-network-settings"></a><span data-ttu-id="f78d8-103">webRequestModules 的 \<clear> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="f78d8-103">\<clear> Element for webRequestModules (Network Settings)</span></span>

<span data-ttu-id="f78d8-104">从应用程序中删除所有已注册的 Web 请求模块。</span><span class="sxs-lookup"><span data-stu-id="f78d8-104">Removes all registered Web request modules from the application.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<webRequestModules>**](webrequestmodules-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a><span data-ttu-id="f78d8-105">语法</span><span class="sxs-lookup"><span data-stu-id="f78d8-105">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f78d8-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f78d8-106">Attributes and Elements</span></span>  

 <span data-ttu-id="f78d8-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f78d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f78d8-108">特性</span><span class="sxs-lookup"><span data-stu-id="f78d8-108">Attributes</span></span>  

 <span data-ttu-id="f78d8-109">无。</span><span class="sxs-lookup"><span data-stu-id="f78d8-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f78d8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f78d8-110">Child Elements</span></span>  

 <span data-ttu-id="f78d8-111">无。</span><span class="sxs-lookup"><span data-stu-id="f78d8-111">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f78d8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f78d8-112">Parent Elements</span></span>  
  
|<span data-ttu-id="f78d8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f78d8-113">**Element**</span></span>|<span data-ttu-id="f78d8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f78d8-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="f78d8-115">webRequestModules</span><span class="sxs-lookup"><span data-stu-id="f78d8-115">webRequestModules</span></span>](webrequestmodules-element-network-settings.md)|<span data-ttu-id="f78d8-116">指定用于从网络主机请求信息的模块。</span><span class="sxs-lookup"><span data-stu-id="f78d8-116">Specifies modules to use to request information from network hosts.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f78d8-117">备注</span><span class="sxs-lookup"><span data-stu-id="f78d8-117">Remarks</span></span>  

 <span data-ttu-id="f78d8-118">`clear`元素删除先前在配置文件中或在配置层次结构中的更高级别定义的所有已注册 Web 请求模块。</span><span class="sxs-lookup"><span data-stu-id="f78d8-118">The `clear` element removes all registered Web request modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="f78d8-119">配置文件</span><span class="sxs-lookup"><span data-stu-id="f78d8-119">Configuration Files</span></span>  

 <span data-ttu-id="f78d8-120">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="f78d8-120">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f78d8-121">示例</span><span class="sxs-lookup"><span data-stu-id="f78d8-121">Example</span></span>  

 <span data-ttu-id="f78d8-122">下面的示例将清除所有 Web 请求模块，然后为 HTTP 注册 Web 请求模块。</span><span class="sxs-lookup"><span data-stu-id="f78d8-122">The following example clears all Web request modules and then registers a Web request module for HTTP.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <clear/>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f78d8-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f78d8-123">See also</span></span>

- <xref:System.Net.WebRequest>
- [<span data-ttu-id="f78d8-124">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="f78d8-124">Network Settings Schema</span></span>](index.md)
