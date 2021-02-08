---
description: 了解详细信息： <etwEnable> 元素
title: <etwEnable> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- etwEnable element
- <etwEnable> element
ms.assetid: 29dde982-6d8b-4099-8867-ad0d7733f6dc
ms.openlocfilehash: 224784f47d15788ded41a5756e1d179a5a25907b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787040"
---
# <a name="etwenable-element"></a><span data-ttu-id="1b577-103">\<etwEnable> 元素</span><span class="sxs-lookup"><span data-stu-id="1b577-103">\<etwEnable> Element</span></span>

<span data-ttu-id="1b577-104">指定是否为公共语言运行时事件启用 Windows 事件跟踪 (ETW)。</span><span class="sxs-lookup"><span data-stu-id="1b577-104">Specifies whether to enable event tracing for Windows (ETW) for common language runtime events.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<etwEnabled>**  
  
## <a name="syntax"></a><span data-ttu-id="1b577-105">语法</span><span class="sxs-lookup"><span data-stu-id="1b577-105">Syntax</span></span>  
  
```xml  
<etwEnable enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1b577-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1b577-106">Attributes and Elements</span></span>  

 <span data-ttu-id="1b577-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b577-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1b577-108">特性</span><span class="sxs-lookup"><span data-stu-id="1b577-108">Attributes</span></span>  
  
|<span data-ttu-id="1b577-109">属性</span><span class="sxs-lookup"><span data-stu-id="1b577-109">Attribute</span></span>|<span data-ttu-id="1b577-110">说明</span><span class="sxs-lookup"><span data-stu-id="1b577-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1b577-111">enabled</span><span class="sxs-lookup"><span data-stu-id="1b577-111">enabled</span></span>|<span data-ttu-id="1b577-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="1b577-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="1b577-113">指定是否应启用 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-113">Specifies whether ETW should be enabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="1b577-114">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="1b577-114">enabled Attribute</span></span>  
  
|<span data-ttu-id="1b577-115">值</span><span class="sxs-lookup"><span data-stu-id="1b577-115">Value</span></span>|<span data-ttu-id="1b577-116">说明</span><span class="sxs-lookup"><span data-stu-id="1b577-116">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1b577-117">是</span><span class="sxs-lookup"><span data-stu-id="1b577-117">true</span></span>|<span data-ttu-id="1b577-118">启用 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-118">Enable ETW.</span></span> <span data-ttu-id="1b577-119">这是从 Windows Vista 和 Windows Server 2008 操作系统开始的 Windows 版本的默认值。</span><span class="sxs-lookup"><span data-stu-id="1b577-119">This is the default for versions of Windows beginning with the Windows Vista and Windows Server 2008 operating systems.</span></span>|  
|<span data-ttu-id="1b577-120">false</span><span class="sxs-lookup"><span data-stu-id="1b577-120">false</span></span>|<span data-ttu-id="1b577-121">禁用 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-121">Disable ETW.</span></span> <span data-ttu-id="1b577-122">这是早期版本的 Windows 的默认设置。</span><span class="sxs-lookup"><span data-stu-id="1b577-122">This is the default for earlier versions of Windows.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1b577-123">子元素</span><span class="sxs-lookup"><span data-stu-id="1b577-123">Child Elements</span></span>  

 <span data-ttu-id="1b577-124">无。</span><span class="sxs-lookup"><span data-stu-id="1b577-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1b577-125">父元素</span><span class="sxs-lookup"><span data-stu-id="1b577-125">Parent Elements</span></span>  
  
|<span data-ttu-id="1b577-126">元素</span><span class="sxs-lookup"><span data-stu-id="1b577-126">Element</span></span>|<span data-ttu-id="1b577-127">说明</span><span class="sxs-lookup"><span data-stu-id="1b577-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="1b577-128">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="1b577-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="1b577-129">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="1b577-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1b577-130">备注</span><span class="sxs-lookup"><span data-stu-id="1b577-130">Remarks</span></span>  

 <span data-ttu-id="1b577-131">从 Windows Vista 开始，默认情况下启用 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-131">Beginning with Windows Vista, ETW is enabled by default.</span></span> <span data-ttu-id="1b577-132">使用此元素可禁用应用程序的 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-132">Use this element to disable ETW for an application.</span></span> <span data-ttu-id="1b577-133">在早期版本的 Windows 中，使用此元素为应用程序启用 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-133">In earlier versions of Windows, use this element to enable ETW for an application.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1b577-134">可以通过使用注册表设置在服务器上全局启用或禁用 ETW。</span><span class="sxs-lookup"><span data-stu-id="1b577-134">ETW can be enabled or disabled globally on a server by using a registry setting.</span></span> <span data-ttu-id="1b577-135">请参阅 [控制 .NET Framework 日志记录](../../../performance/controlling-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="1b577-135">See [Controlling .NET Framework Logging](../../../performance/controlling-logging.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1b577-136">示例</span><span class="sxs-lookup"><span data-stu-id="1b577-136">Example</span></span>  

 <span data-ttu-id="1b577-137">下面的示例演示如何为应用程序启用 ETW 跟踪。</span><span class="sxs-lookup"><span data-stu-id="1b577-137">The following example shows how to enable ETW tracing for an application.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <etwEnable enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1b577-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="1b577-138">See also</span></span>

- [<span data-ttu-id="1b577-139">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="1b577-139">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="1b577-140">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="1b577-140">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="1b577-141">控制 .NET Framework 日志记录</span><span class="sxs-lookup"><span data-stu-id="1b577-141">Controlling .NET Framework Logging</span></span>](../../../performance/controlling-logging.md)
