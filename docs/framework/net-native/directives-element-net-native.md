---
description: '了解详细信息： <Directives> 元素 ( .NET Native) '
title: <Directives>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 444846f3-48d5-4341-a43e-69f7221389eb
ms.openlocfilehash: 7aa3bf3718f32d55ba8189c65705868c6fb399ae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662905"
---
# <a name="directives-element-net-native"></a><span data-ttu-id="c2030-103">\<Directives>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="c2030-103">\<Directives> Element (.NET Native)</span></span>

<span data-ttu-id="c2030-104">.NET Native 的每个运行时指令文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="c2030-104">The root element in every runtime directives file for .NET Native.</span></span>  
  
 `<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">`
  
## <a name="syntax"></a><span data-ttu-id="c2030-105">语法</span><span class="sxs-lookup"><span data-stu-id="c2030-105">Syntax</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <!-- child elements -->
</Directives>  
```  
  
## <a name="attributes"></a><span data-ttu-id="c2030-106">特性</span><span class="sxs-lookup"><span data-stu-id="c2030-106">Attributes</span></span>  
  
|<span data-ttu-id="c2030-107">属性</span><span class="sxs-lookup"><span data-stu-id="c2030-107">Attribute</span></span>|<span data-ttu-id="c2030-108">说明</span><span class="sxs-lookup"><span data-stu-id="c2030-108">Description</span></span>|  
|---------------|-----------------|  
|`xmlns`|<span data-ttu-id="c2030-109">XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="c2030-109">The XML namespace.</span></span> <span data-ttu-id="c2030-110">其值始终为 `http://schemas.microsoft.com/netfx/2013/01/metadata` 。</span><span class="sxs-lookup"><span data-stu-id="c2030-110">Its value is always `http://schemas.microsoft.com/netfx/2013/01/metadata`.</span></span>|  
  
## <a name="child-elements"></a><span data-ttu-id="c2030-111">子元素</span><span class="sxs-lookup"><span data-stu-id="c2030-111">Child elements</span></span>  
  
|<span data-ttu-id="c2030-112">元素</span><span class="sxs-lookup"><span data-stu-id="c2030-112">Element</span></span>|<span data-ttu-id="c2030-113">说明</span><span class="sxs-lookup"><span data-stu-id="c2030-113">Description</span></span>|  
|-------------|-----------------|  
|[\<Application>](application-element-net-native.md)|<span data-ttu-id="c2030-114">作为应用程序范围内的类型和其元数据可以用于反射的类型成员的容器而服务。</span><span class="sxs-lookup"><span data-stu-id="c2030-114">Serves as a container for application-wide types and type members whose metadata is available for reflection.</span></span>|  
|[\<Library>](library-element-net-native.md)|<span data-ttu-id="c2030-115">定义那些子类型和类型成员在运行时间要求元数据的程序集。</span><span class="sxs-lookup"><span data-stu-id="c2030-115">Defines the assembly whose child types and type members require metadata at run time.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2030-116">备注</span><span class="sxs-lookup"><span data-stu-id="c2030-116">Remarks</span></span>  

 <span data-ttu-id="c2030-117">每个运行时指令文件都可以只包含一个 `<Directives>` 元素。</span><span class="sxs-lookup"><span data-stu-id="c2030-117">Each runtime directives file can contain only one `<Directives>` element.</span></span>  
  
 <span data-ttu-id="c2030-118">`<Directives>`元素可以包含零个或一个 [\<Application>](application-element-net-native.md) 元素，以及零个、一个或多个元素 [\<Library>](library-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="c2030-118">The `<Directives>` element can contain zero or one [\<Application>](application-element-net-native.md) element, and zero, one, or more [\<Library>](library-element-net-native.md) elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2030-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2030-119">See also</span></span>

- [<span data-ttu-id="c2030-120">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="c2030-120">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="c2030-121">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="c2030-121">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
