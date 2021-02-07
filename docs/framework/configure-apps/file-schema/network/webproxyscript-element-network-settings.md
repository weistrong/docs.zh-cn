---
description: '了解详细信息： <webProxyScript> 元素 (网络设置) '
title: <webProxyScript> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#webProxyScript
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/webProxyScript
helpviewer_keywords:
- <webProxyScript> element
- webProxyScript element
ms.assetid: a13c26db-6218-4af3-9696-38f24b23bfac
ms.openlocfilehash: 1627b6650582202f3f1a4c1fdebf2d183e4a894b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740101"
---
# <a name="webproxyscript-element-network-settings"></a><span data-ttu-id="c1410-103">\<webProxyScript> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="c1410-103">\<webProxyScript> Element (Network Settings)</span></span>

<span data-ttu-id="c1410-104">配置用于发现 Web 代理的脚本的特征。</span><span class="sxs-lookup"><span data-stu-id="c1410-104">Configures the characteristics of the script used to discover Web proxies.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<settings>**](settings-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<webProxyScript>**

## <a name="syntax"></a><span data-ttu-id="c1410-105">语法</span><span class="sxs-lookup"><span data-stu-id="c1410-105">Syntax</span></span>  
  
```xml  
<webProxyScript  
  downloadTimeout="hh:mm:ss"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c1410-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c1410-106">Attributes and Elements</span></span>  

 <span data-ttu-id="c1410-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1410-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c1410-108">特性</span><span class="sxs-lookup"><span data-stu-id="c1410-108">Attributes</span></span>  
  
|<span data-ttu-id="c1410-109">属性</span><span class="sxs-lookup"><span data-stu-id="c1410-109">Attribute</span></span>|<span data-ttu-id="c1410-110">说明</span><span class="sxs-lookup"><span data-stu-id="c1410-110">Description</span></span>|  
|---------------|-----------------|  
|`downloadTimeout`|<span data-ttu-id="c1410-111">指定下载脚本的最长时间，以小时、分钟和秒为单位。</span><span class="sxs-lookup"><span data-stu-id="c1410-111">Specifies the maximum time to download the script in hours, minutes, and seconds.</span></span> <span data-ttu-id="c1410-112">默认值为一分钟。</span><span class="sxs-lookup"><span data-stu-id="c1410-112">The default value is one minute.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c1410-113">子元素</span><span class="sxs-lookup"><span data-stu-id="c1410-113">Child Elements</span></span>  

 <span data-ttu-id="c1410-114">无。</span><span class="sxs-lookup"><span data-stu-id="c1410-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c1410-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c1410-115">Parent Elements</span></span>  
  
|<span data-ttu-id="c1410-116">元素</span><span class="sxs-lookup"><span data-stu-id="c1410-116">Element</span></span>|<span data-ttu-id="c1410-117">说明</span><span class="sxs-lookup"><span data-stu-id="c1410-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c1410-118">设置</span><span class="sxs-lookup"><span data-stu-id="c1410-118">settings</span></span>](settings-element-network-settings.md)|<span data-ttu-id="c1410-119">配置 <xref:System.Net> 命名空间的基本网络选项。</span><span class="sxs-lookup"><span data-stu-id="c1410-119">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c1410-120">备注</span><span class="sxs-lookup"><span data-stu-id="c1410-120">Remarks</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="c1410-121">配置文件</span><span class="sxs-lookup"><span data-stu-id="c1410-121">Configuration Files</span></span>  

 <span data-ttu-id="c1410-122">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="c1410-122">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1410-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1410-123">See also</span></span>

- [<span data-ttu-id="c1410-124">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="c1410-124">Network Settings Schema</span></span>](index.md)
