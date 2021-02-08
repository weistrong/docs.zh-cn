---
description: 了解详细信息： <developmentMode> 元素
title: <developmentMode> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/developmentMode
- http://schemas.microsoft.com/.NetConfiguration/v2.0#developmentMode
helpviewer_keywords:
- developmentMode element
- container tags, <developmentMode> element
- <developmentMode> element
ms.assetid: 60e79a8c-415a-497d-be29-b9d0fd9bdee3
ms.openlocfilehash: 668461d13c8a1767268692804e9783bb6d4b9a56
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787118"
---
# <a name="developmentmode-element"></a><span data-ttu-id="107f2-103">\<developmentMode> 元素</span><span class="sxs-lookup"><span data-stu-id="107f2-103">\<developmentMode> Element</span></span>

<span data-ttu-id="107f2-104">指定运行时是否搜索由 DEVPATH 环境变量指定的目录中的程序集。</span><span class="sxs-lookup"><span data-stu-id="107f2-104">Specifies whether the runtime searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<developmentMode>**  
  
## <a name="syntax"></a><span data-ttu-id="107f2-105">语法</span><span class="sxs-lookup"><span data-stu-id="107f2-105">Syntax</span></span>  
  
```xml  
<developmentMode developerInstallation="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="107f2-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="107f2-106">Attributes and Elements</span></span>  

 <span data-ttu-id="107f2-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="107f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="107f2-108">特性</span><span class="sxs-lookup"><span data-stu-id="107f2-108">Attributes</span></span>  
  
|<span data-ttu-id="107f2-109">属性</span><span class="sxs-lookup"><span data-stu-id="107f2-109">Attribute</span></span>|<span data-ttu-id="107f2-110">说明</span><span class="sxs-lookup"><span data-stu-id="107f2-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="107f2-111">**developerInstallation**</span><span class="sxs-lookup"><span data-stu-id="107f2-111">**developerInstallation**</span></span>|<span data-ttu-id="107f2-112">指定运行时是否搜索由 DEVPATH 环境变量指定的目录中的程序集。</span><span class="sxs-lookup"><span data-stu-id="107f2-112">Specifies whether the runtime searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>|  
  
## <a name="developerinstallation-attribute"></a><span data-ttu-id="107f2-113">developerInstallation 特性</span><span class="sxs-lookup"><span data-stu-id="107f2-113">developerInstallation Attribute</span></span>  
  
|<span data-ttu-id="107f2-114">值</span><span class="sxs-lookup"><span data-stu-id="107f2-114">Value</span></span>|<span data-ttu-id="107f2-115">说明</span><span class="sxs-lookup"><span data-stu-id="107f2-115">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="107f2-116">true</span><span class="sxs-lookup"><span data-stu-id="107f2-116">**true**</span></span>|<span data-ttu-id="107f2-117">在由 DEVPATH 环境变量指定的目录中搜索程序集。</span><span class="sxs-lookup"><span data-stu-id="107f2-117">Searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>|  
|<span data-ttu-id="107f2-118">**false**</span><span class="sxs-lookup"><span data-stu-id="107f2-118">**false**</span></span>|<span data-ttu-id="107f2-119">不搜索由 DEVPATH 环境变量指定的目录中的程序集。</span><span class="sxs-lookup"><span data-stu-id="107f2-119">Does not search for assemblies in directories specified by the DEVPATH environment variable.</span></span> <span data-ttu-id="107f2-120">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="107f2-120">This is the default</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="107f2-121">子元素</span><span class="sxs-lookup"><span data-stu-id="107f2-121">Child Elements</span></span>  

 <span data-ttu-id="107f2-122">无。</span><span class="sxs-lookup"><span data-stu-id="107f2-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="107f2-123">父元素</span><span class="sxs-lookup"><span data-stu-id="107f2-123">Parent Elements</span></span>  
  
|<span data-ttu-id="107f2-124">元素</span><span class="sxs-lookup"><span data-stu-id="107f2-124">Element</span></span>|<span data-ttu-id="107f2-125">说明</span><span class="sxs-lookup"><span data-stu-id="107f2-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="107f2-126">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="107f2-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="107f2-127">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="107f2-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="107f2-128">备注</span><span class="sxs-lookup"><span data-stu-id="107f2-128">Remarks</span></span>  

 <span data-ttu-id="107f2-129">仅在开发时使用此设置。</span><span class="sxs-lookup"><span data-stu-id="107f2-129">Use this setting only at development time.</span></span> <span data-ttu-id="107f2-130">运行时不检查在 DEVPATH 中找到的具有强名称的程序集的版本。</span><span class="sxs-lookup"><span data-stu-id="107f2-130">The runtime does not check the versions on strong-named assemblies found in the DEVPATH.</span></span> <span data-ttu-id="107f2-131">它只使用它找到的第一个程序集。</span><span class="sxs-lookup"><span data-stu-id="107f2-131">It simply uses the first assembly it finds.</span></span>  
  
## <a name="example"></a><span data-ttu-id="107f2-132">示例</span><span class="sxs-lookup"><span data-stu-id="107f2-132">Example</span></span>  

 <span data-ttu-id="107f2-133">下面的示例演示如何使运行时在由 DEVPATH 环境变量指定的目录中搜索程序集。</span><span class="sxs-lookup"><span data-stu-id="107f2-133">The following example shows how to cause the runtime to search for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <developmentMode developerInstallation="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="107f2-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="107f2-134">See also</span></span>

- [<span data-ttu-id="107f2-135">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="107f2-135">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="107f2-136">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="107f2-136">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="107f2-137">如何：使用 DEVPATH 查找程序集</span><span class="sxs-lookup"><span data-stu-id="107f2-137">How to: Locate Assemblies by Using DEVPATH</span></span>](../../how-to-locate-assemblies-by-using-devpath.md)
