---
description: 了解详细信息： <UseSmallInternalThreadStacks> 元素
title: <UseSmallInternalThreadStacks> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- UseSmallInternalThreadStacks element
- <UseSmallInternalThreadStacks> element
ms.assetid: 1e3f6ec0-1cac-4e1c-9c81-17d948ae5874
ms.openlocfilehash: eeb253025b32f862926c7315004b1854b8eef928
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639960"
---
# <a name="usesmallinternalthreadstacks-element"></a><span data-ttu-id="f814b-103">\<UseSmallInternalThreadStacks> 元素</span><span class="sxs-lookup"><span data-stu-id="f814b-103">\<UseSmallInternalThreadStacks> Element</span></span>

<span data-ttu-id="f814b-104">请求公共语言运行时 (CLR) 在创建其内部使用的某些线程时指定显式堆栈大小来减少内存使用，而不是使用这些线程的默认堆栈大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-104">Requests that the common language runtime (CLR) reduce memory use by specifying explicit stack sizes when it creates certain threads that it uses internally, instead of using the default stack size for those threads.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<UseSmallInternalThreadStacks>**  
  
## <a name="syntax"></a><span data-ttu-id="f814b-105">语法</span><span class="sxs-lookup"><span data-stu-id="f814b-105">Syntax</span></span>  
  
```xml  
<UseSmallInternalThreadStacks enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f814b-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f814b-106">Attributes and Elements</span></span>  

 <span data-ttu-id="f814b-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f814b-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f814b-108">特性</span><span class="sxs-lookup"><span data-stu-id="f814b-108">Attributes</span></span>  
  
|<span data-ttu-id="f814b-109">属性</span><span class="sxs-lookup"><span data-stu-id="f814b-109">Attribute</span></span>|<span data-ttu-id="f814b-110">说明</span><span class="sxs-lookup"><span data-stu-id="f814b-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f814b-111">enabled</span><span class="sxs-lookup"><span data-stu-id="f814b-111">enabled</span></span>|<span data-ttu-id="f814b-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="f814b-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="f814b-113">指定是否请求 CLR 在创建其内部使用的某些线程时使用显式堆栈大小而不是默认堆栈大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-113">Specifies whether to request that the CLR use explicit stack sizes instead of the default stack size when it creates certain threads that it uses internally.</span></span> <span data-ttu-id="f814b-114">显式堆栈大小小于默认堆栈大小 1 MB。</span><span class="sxs-lookup"><span data-stu-id="f814b-114">The explicit stack sizes are smaller than the default stack size of 1 MB.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="f814b-115">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="f814b-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="f814b-116">值</span><span class="sxs-lookup"><span data-stu-id="f814b-116">Value</span></span>|<span data-ttu-id="f814b-117">说明</span><span class="sxs-lookup"><span data-stu-id="f814b-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f814b-118">是</span><span class="sxs-lookup"><span data-stu-id="f814b-118">true</span></span>|<span data-ttu-id="f814b-119">请求显式堆栈大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-119">Request explicit stack sizes.</span></span>|  
|<span data-ttu-id="f814b-120">false</span><span class="sxs-lookup"><span data-stu-id="f814b-120">false</span></span>|<span data-ttu-id="f814b-121">使用默认堆栈大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-121">Use the default stack size.</span></span> <span data-ttu-id="f814b-122">这是 .NET Framework 4 的默认值。</span><span class="sxs-lookup"><span data-stu-id="f814b-122">This is the default for the .NET Framework 4.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f814b-123">子元素</span><span class="sxs-lookup"><span data-stu-id="f814b-123">Child Elements</span></span>  

 <span data-ttu-id="f814b-124">无。</span><span class="sxs-lookup"><span data-stu-id="f814b-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f814b-125">父元素</span><span class="sxs-lookup"><span data-stu-id="f814b-125">Parent Elements</span></span>  
  
|<span data-ttu-id="f814b-126">元素</span><span class="sxs-lookup"><span data-stu-id="f814b-126">Element</span></span>|<span data-ttu-id="f814b-127">说明</span><span class="sxs-lookup"><span data-stu-id="f814b-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="f814b-128">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="f814b-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="f814b-129">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="f814b-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f814b-130">备注</span><span class="sxs-lookup"><span data-stu-id="f814b-130">Remarks</span></span>  

 <span data-ttu-id="f814b-131">此配置元素用于请求进程中减少的虚拟内存使用，因为 CLR 用于其内部线程的显式线程大小（如果请求被接受）小于默认大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-131">This configuration element is used to request reduced virtual memory use in a process, because the explicit thread sizes that the CLR uses for its internal threads, if the request is honored, are smaller than the default size.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="f814b-132">此配置元素是对 CLR 的请求，而不是绝对要求。</span><span class="sxs-lookup"><span data-stu-id="f814b-132">This configuration element is a request to the CLR rather than an absolute requirement.</span></span> <span data-ttu-id="f814b-133">在 .NET Framework 4 中，请求仅适用于 x86 体系结构。</span><span class="sxs-lookup"><span data-stu-id="f814b-133">In the .NET Framework 4, the request is honored only for the x86 architecture.</span></span> <span data-ttu-id="f814b-134">在未来版本的 CLR 中，可能会完全忽略此元素，或将其替换为所选内部线程始终使用的显式堆栈大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-134">This element might be ignored completely in future versions of the CLR, or replaced by explicit stack sizes that are always used for selected internal threads.</span></span>  
  
 <span data-ttu-id="f814b-135">如果 CLR 接受请求，则指定此配置元素会在较小的虚拟内存使用情况下提高可靠性，因为较小的堆栈大小可能会导致堆栈溢出。</span><span class="sxs-lookup"><span data-stu-id="f814b-135">Specifying this configuration element trades reliability for smaller virtual memory use if the CLR honors the request, because smaller stack sizes could potentially make stack overflows more likely.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f814b-136">示例</span><span class="sxs-lookup"><span data-stu-id="f814b-136">Example</span></span>  

 <span data-ttu-id="f814b-137">下面的示例演示如何请求 CLR 对其内部使用的某些线程使用显式堆栈大小。</span><span class="sxs-lookup"><span data-stu-id="f814b-137">The following example shows how to request that the CLR use explicit stack sizes for certain threads that it uses internally.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <UseSmallInternalThreadStacks enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f814b-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="f814b-138">See also</span></span>

- [<span data-ttu-id="f814b-139">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="f814b-139">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="f814b-140">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="f814b-140">Configuration File Schema</span></span>](../index.md)
