---
description: 了解详细信息： <legacyCorruptedStateExceptionsPolicy> 元素
title: <legacyCorruptedStateExceptionsPolicy> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- <legacyCorruptedStateExceptionsPolicy> element
- legacyCorruptedStateExceptionsPolicy element
ms.assetid: e0a55ddc-bfa8-4f3e-ac14-d1fc3330e4bb
ms.openlocfilehash: 34082c0779b09400a875894359cf7cf501173508
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786949"
---
# <a name="legacycorruptedstateexceptionspolicy-element"></a><span data-ttu-id="a4833-103">\<legacyCorruptedStateExceptionsPolicy> 元素</span><span class="sxs-lookup"><span data-stu-id="a4833-103">\<legacyCorruptedStateExceptionsPolicy> Element</span></span>

<span data-ttu-id="a4833-104">指定公共语言运行时是否允许托管代码捕获访问冲突和其他损坏状态异常。</span><span class="sxs-lookup"><span data-stu-id="a4833-104">Specifies whether the common language runtime allows managed code to catch access violations and other corrupted state exceptions.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<legacyCorruptedStateExceptionsPolicy>**  
  
## <a name="syntax"></a><span data-ttu-id="a4833-105">语法</span><span class="sxs-lookup"><span data-stu-id="a4833-105">Syntax</span></span>  
  
```xml  
<legacyCorruptedStateExceptionsPolicy enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a4833-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a4833-106">Attributes and Elements</span></span>  

 <span data-ttu-id="a4833-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a4833-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a4833-108">特性</span><span class="sxs-lookup"><span data-stu-id="a4833-108">Attributes</span></span>  
  
|<span data-ttu-id="a4833-109">属性</span><span class="sxs-lookup"><span data-stu-id="a4833-109">Attribute</span></span>|<span data-ttu-id="a4833-110">描述</span><span class="sxs-lookup"><span data-stu-id="a4833-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="a4833-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="a4833-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="a4833-112">指定应用程序将捕获损坏状态异常故障，例如访问冲突。</span><span class="sxs-lookup"><span data-stu-id="a4833-112">Specifies that the application will catch corrupting state exception failures such as access violations.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="a4833-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="a4833-113">enabled Attribute</span></span>  
  
|<span data-ttu-id="a4833-114">值</span><span class="sxs-lookup"><span data-stu-id="a4833-114">Value</span></span>|<span data-ttu-id="a4833-115">说明</span><span class="sxs-lookup"><span data-stu-id="a4833-115">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="a4833-116">应用程序不会捕获损坏状态异常故障，例如访问冲突。</span><span class="sxs-lookup"><span data-stu-id="a4833-116">The application will not catch corrupting state exception failures such as access violations.</span></span> <span data-ttu-id="a4833-117">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="a4833-117">This is the default.</span></span>|  
|`true`|<span data-ttu-id="a4833-118">应用程序将捕获损坏状态异常故障，例如访问冲突。</span><span class="sxs-lookup"><span data-stu-id="a4833-118">The application will catch corrupting state exception failures such as access violations.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a4833-119">子元素</span><span class="sxs-lookup"><span data-stu-id="a4833-119">Child Elements</span></span>  

 <span data-ttu-id="a4833-120">无。</span><span class="sxs-lookup"><span data-stu-id="a4833-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a4833-121">父元素</span><span class="sxs-lookup"><span data-stu-id="a4833-121">Parent Elements</span></span>  
  
|<span data-ttu-id="a4833-122">元素</span><span class="sxs-lookup"><span data-stu-id="a4833-122">Element</span></span>|<span data-ttu-id="a4833-123">说明</span><span class="sxs-lookup"><span data-stu-id="a4833-123">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="a4833-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="a4833-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="a4833-125">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="a4833-125">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a4833-126">备注</span><span class="sxs-lookup"><span data-stu-id="a4833-126">Remarks</span></span>  

 <span data-ttu-id="a4833-127">在 .NET Framework 版本3.5 及更早版本中，公共语言运行时允许托管代码捕获由损坏的进程状态引发的异常。</span><span class="sxs-lookup"><span data-stu-id="a4833-127">In the .NET Framework version 3.5 and earlier, the common language runtime allowed managed code to catch exceptions that were raised by corrupted process states.</span></span> <span data-ttu-id="a4833-128">访问冲突就是这种类型的异常的一个示例。</span><span class="sxs-lookup"><span data-stu-id="a4833-128">An access violation is an example of this type of exception.</span></span>  
  
 <span data-ttu-id="a4833-129">从 .NET Framework 4 开始，托管代码不再在块中捕获这些类型的异常 `catch` 。</span><span class="sxs-lookup"><span data-stu-id="a4833-129">Starting with the .NET Framework 4, managed code no longer catches these types of exceptions in `catch` blocks.</span></span> <span data-ttu-id="a4833-130">不过，你可以通过两种方式重写此更改并保持对损坏状态异常的处理：</span><span class="sxs-lookup"><span data-stu-id="a4833-130">However, you can override this change and maintain the handling of corrupted state exceptions in two ways:</span></span>  
  
- <span data-ttu-id="a4833-131">将 `<legacyCorruptedStateExceptionsPolicy>` 元素的 `enabled` 属性设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="a4833-131">Set the `<legacyCorruptedStateExceptionsPolicy>` element's `enabled` attribute to `true`.</span></span> <span data-ttu-id="a4833-132">此配置设置将应用 processwide 并影响所有方法。</span><span class="sxs-lookup"><span data-stu-id="a4833-132">This configuration setting is applied processwide and affects all methods.</span></span>  
  
 <span data-ttu-id="a4833-133">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="a4833-133">-or-</span></span>  
  
- <span data-ttu-id="a4833-134">将特性应用于 <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=nameWithType> 包含异常块的方法 `catch` 。</span><span class="sxs-lookup"><span data-stu-id="a4833-134">Apply the <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=nameWithType> attribute to the method that contains the exceptions `catch` block.</span></span>  
  
 <span data-ttu-id="a4833-135">此配置元素仅在 .NET Framework 4 及更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="a4833-135">This configuration element is available only in the .NET Framework 4 and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a4833-136">示例</span><span class="sxs-lookup"><span data-stu-id="a4833-136">Example</span></span>  

 <span data-ttu-id="a4833-137">下面的示例演示如何指定应用程序应恢复到 .NET Framework 4 之前的行为，并捕获所有损坏状态异常错误。</span><span class="sxs-lookup"><span data-stu-id="a4833-137">The following example shows how to specify that the application should revert to the behavior before the .NET Framework 4, and catch all corrupting state exception failures.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <legacyCorruptedStateExceptionsPolicy enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a4833-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4833-138">See also</span></span>

- <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute>
- [<span data-ttu-id="a4833-139">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="a4833-139">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="a4833-140">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="a4833-140">Configuration File Schema</span></span>](../index.md)
