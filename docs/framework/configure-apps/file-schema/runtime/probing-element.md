---
description: 了解详细信息： <probing> 元素
title: <probing> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/probing
- http://schemas.microsoft.com/.NetConfiguration/v2.0#probing
helpviewer_keywords:
- <probing> element
- container tags, <probing> element
- probing element
ms.assetid: 09c80fc9-1ba5-4192-89f7-3a79b2e4b024
ms.openlocfilehash: 404e53f735ce02c2a3d7911216f834d38e309789
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726099"
---
# <a name="probing-element"></a><span data-ttu-id="7c4c6-103">\<probing> 元素</span><span class="sxs-lookup"><span data-stu-id="7c4c6-103">\<probing> Element</span></span>

<span data-ttu-id="7c4c6-104">指定加载程序集时要搜索的公共语言运行时的应用程序基子目录。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-104">Specifies application base subdirectories for the common language runtime to search when loading assemblies.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<assemblyBinding>**](assemblybinding-element-for-runtime.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<probing>**  
  
## <a name="syntax"></a><span data-ttu-id="7c4c6-105">语法</span><span class="sxs-lookup"><span data-stu-id="7c4c6-105">Syntax</span></span>  
  
```xml  
<probing privatePath="paths"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7c4c6-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7c4c6-106">Attributes and Elements</span></span>  

 <span data-ttu-id="7c4c6-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7c4c6-108">特性</span><span class="sxs-lookup"><span data-stu-id="7c4c6-108">Attributes</span></span>  
  
|<span data-ttu-id="7c4c6-109">属性</span><span class="sxs-lookup"><span data-stu-id="7c4c6-109">Attribute</span></span>|<span data-ttu-id="7c4c6-110">描述</span><span class="sxs-lookup"><span data-stu-id="7c4c6-110">Description</span></span>|  
|---------------|-----------------|  
|`privatePath`|<span data-ttu-id="7c4c6-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="7c4c6-112">指定可能包含程序集的应用程序基目录的子目录。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-112">Specifies subdirectories of the application's base directory that might contain assemblies.</span></span> <span data-ttu-id="7c4c6-113">用分号分隔每个子目录。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-113">Delimit each subdirectory with a semicolon.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7c4c6-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7c4c6-114">Child Elements</span></span>  

<span data-ttu-id="7c4c6-115">无。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7c4c6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7c4c6-116">Parent Elements</span></span>  
  
|<span data-ttu-id="7c4c6-117">元素</span><span class="sxs-lookup"><span data-stu-id="7c4c6-117">Element</span></span>|<span data-ttu-id="7c4c6-118">说明</span><span class="sxs-lookup"><span data-stu-id="7c4c6-118">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="7c4c6-119">包含有关程序集版本重定向和程序集位置的信息。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-119">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="7c4c6-120">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="7c4c6-121">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-121">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="7c4c6-122">示例</span><span class="sxs-lookup"><span data-stu-id="7c4c6-122">Example</span></span>  

 <span data-ttu-id="7c4c6-123">下面的示例演示如何指定运行时应搜索程序集的应用程序基子目录。</span><span class="sxs-lookup"><span data-stu-id="7c4c6-123">The following example shows how to specify application base subdirectories the runtime should search for assemblies.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <probing privatePath="bin;bin2\subbin;bin3"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7c4c6-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="7c4c6-124">See also</span></span>

- [<span data-ttu-id="7c4c6-125">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="7c4c6-125">Runtime settings schema</span></span>](index.md)
- [<span data-ttu-id="7c4c6-126">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="7c4c6-126">Configuration file schema</span></span>](../index.md)
- [<span data-ttu-id="7c4c6-127">指定程序集的位置</span><span class="sxs-lookup"><span data-stu-id="7c4c6-127">Specify an assembly's location</span></span>](../../../../standard/assembly/location.md)
- [<span data-ttu-id="7c4c6-128">运行时如何定位程序集</span><span class="sxs-lookup"><span data-stu-id="7c4c6-128">How the runtime locates assemblies</span></span>](../../../deployment/how-the-runtime-locates-assemblies.md)
