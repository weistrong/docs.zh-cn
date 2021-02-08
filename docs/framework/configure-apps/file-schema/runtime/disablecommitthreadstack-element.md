---
description: 了解详细信息： <disableCommitThreadStack> 元素
title: <disableCommitThreadStack> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/disableCommitThreadStack
- http://schemas.microsoft.com/.NetConfiguration/v2.0#disableCommitThreadStack
helpviewer_keywords:
- <disableCommitThreadStack> element
- disableCommitThreadStack element
ms.assetid: 3559d46a-7640-4c72-9a11-7e980768929e
ms.openlocfilehash: f80a23b12f67b9f3df1ddb010edb735225f6f7a8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787092"
---
# <a name="disablecommitthreadstack-element"></a><span data-ttu-id="6e115-103">\<disableCommitThreadStack> 元素</span><span class="sxs-lookup"><span data-stu-id="6e115-103">\<disableCommitThreadStack> Element</span></span>

<span data-ttu-id="6e115-104">指定在线程启动时是否提交完整线程堆栈。</span><span class="sxs-lookup"><span data-stu-id="6e115-104">Specifies whether the full thread stack is committed when a thread is started.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<disableCommitThreadStack>**  
  
## <a name="syntax"></a><span data-ttu-id="6e115-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e115-105">Syntax</span></span>  
  
```xml  
<disableCommitThreadStack enabled="0|1"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6e115-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6e115-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6e115-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6e115-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6e115-108">特性</span><span class="sxs-lookup"><span data-stu-id="6e115-108">Attributes</span></span>  
  
|<span data-ttu-id="6e115-109">属性</span><span class="sxs-lookup"><span data-stu-id="6e115-109">Attribute</span></span>|<span data-ttu-id="6e115-110">说明</span><span class="sxs-lookup"><span data-stu-id="6e115-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6e115-111">enabled</span><span class="sxs-lookup"><span data-stu-id="6e115-111">enabled</span></span>|<span data-ttu-id="6e115-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="6e115-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="6e115-113">指定是否禁止在线程启动时提交完整线程堆栈（默认行为）。</span><span class="sxs-lookup"><span data-stu-id="6e115-113">Specifies whether committing the full thread stack on thread startup (the default behavior) is disabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="6e115-114">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="6e115-114">enabled Attribute</span></span>  
  
|<span data-ttu-id="6e115-115">值</span><span class="sxs-lookup"><span data-stu-id="6e115-115">Value</span></span>|<span data-ttu-id="6e115-116">说明</span><span class="sxs-lookup"><span data-stu-id="6e115-116">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="6e115-117">0</span><span class="sxs-lookup"><span data-stu-id="6e115-117">0</span></span>|<span data-ttu-id="6e115-118">不禁用公共语言运行时的默认行为（即在线程启动时提交完整线程堆栈）。</span><span class="sxs-lookup"><span data-stu-id="6e115-118">Do not disable the default behavior of the common language runtime, which is to commit the full thread stack when a thread is started.</span></span>|  
|<span data-ttu-id="6e115-119">1</span><span class="sxs-lookup"><span data-stu-id="6e115-119">1</span></span>|<span data-ttu-id="6e115-120">禁用公共语言运行时的默认行为（即在线程启动时提交完整线程堆栈）。</span><span class="sxs-lookup"><span data-stu-id="6e115-120">Disable the default behavior of the common language runtime, which is to commit the full thread stack when a thread is started.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6e115-121">子元素</span><span class="sxs-lookup"><span data-stu-id="6e115-121">Child Elements</span></span>  

 <span data-ttu-id="6e115-122">无。</span><span class="sxs-lookup"><span data-stu-id="6e115-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6e115-123">父元素</span><span class="sxs-lookup"><span data-stu-id="6e115-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6e115-124">元素</span><span class="sxs-lookup"><span data-stu-id="6e115-124">Element</span></span>|<span data-ttu-id="6e115-125">说明</span><span class="sxs-lookup"><span data-stu-id="6e115-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6e115-126">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="6e115-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="6e115-127">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="6e115-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e115-128">备注</span><span class="sxs-lookup"><span data-stu-id="6e115-128">Remarks</span></span>  

 <span data-ttu-id="6e115-129">公共语言运行时的默认行为是在线程启动时提交完整线程堆栈。</span><span class="sxs-lookup"><span data-stu-id="6e115-129">The default behavior of the common language runtime is to commit the full thread stack when a thread is started.</span></span> <span data-ttu-id="6e115-130">当必须在内存有限的服务器上创建大量线程，并且其中大多数线程都使用非常小的堆栈空间时，如果公共语言运行时在线程启动时不立即提交完整线程堆栈，则服务器可能会表现更好。</span><span class="sxs-lookup"><span data-stu-id="6e115-130">If a large number of threads must be created on a server that has limited memory, and most of those threads will use very little stack space, the server might perform better if the common language runtime does not commit the full thread stack immediately when a thread is started.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6e115-131">非托管主机可以使用 `STARTUP_DISABLE_COMMITTHREADSTACK` STARTUP_FLAGS [枚举中的](../../../unmanaged-api/hosting/startup-flags-enumeration.md) 启动标志实现相同结果。</span><span class="sxs-lookup"><span data-stu-id="6e115-131">Unmanaged hosts can use the `STARTUP_DISABLE_COMMITTHREADSTACK` startup flag in the [STARTUP_FLAGS](../../../unmanaged-api/hosting/startup-flags-enumeration.md) enumeration to accomplish the same result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6e115-132">示例</span><span class="sxs-lookup"><span data-stu-id="6e115-132">Example</span></span>  

 <span data-ttu-id="6e115-133">下面的示例演示如何禁用公共语言运行时的默认行为（即在线程启动时提交完整线程堆栈）。</span><span class="sxs-lookup"><span data-stu-id="6e115-133">The following example shows how to disable the default behavior of the common language runtime, which is to commit the full thread stack on thread startup.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <disableCommitThreadStack enabled="1" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6e115-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e115-134">See also</span></span>

- [<span data-ttu-id="6e115-135">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="6e115-135">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="6e115-136">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="6e115-136">Configuration File Schema</span></span>](../index.md)
