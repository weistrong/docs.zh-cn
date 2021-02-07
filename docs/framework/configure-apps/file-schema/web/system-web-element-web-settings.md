---
description: '了解详细信息： <system.web> 元素 (Web 设置) '
title: <system.web> 元素（网络设置）
ms.date: 03/30/2017
helpviewer_keywords:
- Web.config configuration file [ASP.NET]
- system.Web element
- <system.Web> element
- ASP.NET configuration system
- configuration files [ASP.NET]
ms.assetid: 24c4cf4f-ad32-42b2-b040-8e4549e2855e
ms.openlocfilehash: 2adcd3eba1eb6d67bcb4dc82243cd70d31d64fe9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681898"
---
# <a name="systemweb-element-web-settings"></a><span data-ttu-id="1c624-103">\<system.web> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="1c624-103">\<system.web> Element (Web Settings)</span></span>

<span data-ttu-id="1c624-104">包含有关 ASP.NET 承载层如何管理进程范围的行为的信息。</span><span class="sxs-lookup"><span data-stu-id="1c624-104">Contains information about how the ASP.NET hosting layer manages process-wide behavior.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;**\<system.web>**  
  
## <a name="syntax"></a><span data-ttu-id="1c624-105">语法</span><span class="sxs-lookup"><span data-stu-id="1c624-105">Syntax</span></span>  
  
```xml  
<system.web>  
</system.web>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1c624-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1c624-106">Attributes and Elements</span></span>  

<span data-ttu-id="1c624-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1c624-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1c624-108">特性</span><span class="sxs-lookup"><span data-stu-id="1c624-108">Attributes</span></span>  

<span data-ttu-id="1c624-109">无。</span><span class="sxs-lookup"><span data-stu-id="1c624-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1c624-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1c624-110">Child Elements</span></span>  
  
|<span data-ttu-id="1c624-111">元素</span><span class="sxs-lookup"><span data-stu-id="1c624-111">Element</span></span>|<span data-ttu-id="1c624-112">说明</span><span class="sxs-lookup"><span data-stu-id="1c624-112">Description</span></span>|  
|-------------|-----------------|  
|[\<applicationPool>](applicationpool-element-web-settings.md)|<span data-ttu-id="1c624-113">指定 aspnet.config 文件中的 IIS 应用程序池的配置设置。</span><span class="sxs-lookup"><span data-stu-id="1c624-113">Specifies configuration settings for IIS application pools in an aspnet.config file.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1c624-114">父元素</span><span class="sxs-lookup"><span data-stu-id="1c624-114">Parent Elements</span></span>  
  
|<span data-ttu-id="1c624-115">元素</span><span class="sxs-lookup"><span data-stu-id="1c624-115">Element</span></span>|<span data-ttu-id="1c624-116">说明</span><span class="sxs-lookup"><span data-stu-id="1c624-116">Description</span></span>|  
|-------------|-----------------|  
|[\<configuration>](../configuration-element.md)|<span data-ttu-id="1c624-117">指定公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="1c624-117">Specifies the root element in every configuration file that is used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1c624-118">备注</span><span class="sxs-lookup"><span data-stu-id="1c624-118">Remarks</span></span>  

<span data-ttu-id="1c624-119">`system.web`元素及其子 `applicationPool` 元素已添加到 .NET FRAMEWORK 3.5 SP1 中的 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="1c624-119">The `system.web` element and its child `applicationPool` element were added to the .NET Framework as of .NET Framework 3.5 SP1.</span></span> <span data-ttu-id="1c624-120">在集成模式下运行 IIS 7.0 或更高版本时，此元素组合可让你配置 ASP.NET 管理线程的方式，以及在 ASP.NET 托管在 IIS 应用程序池中时，如何将请求排队。</span><span class="sxs-lookup"><span data-stu-id="1c624-120">When you run IIS 7.0 or later versions in Integrated mode, this element combination lets you configure how ASP.NET manages threads and how it queues requests when ASP.NET is hosted in an IIS application pool.</span></span> <span data-ttu-id="1c624-121">如果在经典或 ISAPI 模式下运行 IIS 7.0 或更高版本，则将忽略这些设置。</span><span class="sxs-lookup"><span data-stu-id="1c624-121">If you run IIS 7.0 or later versions in Classic or ISAPI mode, these settings are ignored.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1c624-122">示例</span><span class="sxs-lookup"><span data-stu-id="1c624-122">Example</span></span>  

<span data-ttu-id="1c624-123">下面的示例演示当 ASP.NET 托管在 IIS 应用程序池中时，如何在 aspnet.config 文件中配置 ASP.NET 进程范围内的行为。</span><span class="sxs-lookup"><span data-stu-id="1c624-123">The following example shows how to configure ASP.NET process-wide behavior in the aspnet.config file when ASP.NET is hosted in an IIS application pool.</span></span> <span data-ttu-id="1c624-124">该示例假设 IIS 在集成模式下运行，并且该应用程序正在使用 .NET Framework 3.5 SP1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="1c624-124">The example assumes that IIS is running in Integrated mode and that the application is using the .NET Framework 3.5 SP1 or a later version.</span></span> <span data-ttu-id="1c624-125">此行为不会在早于 .NET Framework 3.5 SP1 的 .NET Framework 版本中发生。</span><span class="sxs-lookup"><span data-stu-id="1c624-125">This behavior does not occur in versions of the .NET Framework earlier than the .NET Framework 3.5 SP1.</span></span> <span data-ttu-id="1c624-126">示例中的值为默认值。</span><span class="sxs-lookup"><span data-stu-id="1c624-126">The values in the example are the default values.</span></span>  
  
```xml  
<configuration>  
  <system.web>  
    <applicationPool
        maxConcurrentRequestsPerCPU="5000"
        maxConcurrentThreadsPerCPU="0"
        requestQueueLimit="5000" />  
  </system.web>  
</configuration>  
```  
  
## <a name="element-information"></a><span data-ttu-id="1c624-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="1c624-127">Element Information</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="1c624-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="1c624-128">Namespace</span></span>||  
|<span data-ttu-id="1c624-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="1c624-129">Schema Name</span></span>||  
|<span data-ttu-id="1c624-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="1c624-130">Validation File</span></span>||  
|<span data-ttu-id="1c624-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="1c624-131">Can be Empty</span></span>||  
  
## <a name="see-also"></a><span data-ttu-id="1c624-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="1c624-132">See also</span></span>

- [<span data-ttu-id="1c624-133">\<applicationPool> 元素 (Web 设置) </span><span class="sxs-lookup"><span data-stu-id="1c624-133">\<applicationPool> Element (Web Settings)</span></span>](applicationpool-element-web-settings.md)
