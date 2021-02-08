---
description: 了解详细信息： <PreferComInsteadOfManagedRemoting> 元素
title: <PreferComInsteadOfManagedRemoting> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- <PreferComInsteadOfManagedRemoting> element
- PreferComInsteadOfManagedRemoting element
ms.assetid: a279a42a-c415-4e79-88cf-64244ebda613
ms.openlocfilehash: b621af9b584d1ea2623ffe5a44f74b5b7bd520e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782268"
---
# <a name="prefercominsteadofmanagedremoting-element"></a><span data-ttu-id="bb376-103">\<PreferComInsteadOfManagedRemoting> 元素</span><span class="sxs-lookup"><span data-stu-id="bb376-103">\<PreferComInsteadOfManagedRemoting> Element</span></span>

<span data-ttu-id="bb376-104">指定运行时是否将对跨应用程序域边界的所有调用使用 COM 互操作而不是远程处理。</span><span class="sxs-lookup"><span data-stu-id="bb376-104">Specifies whether the runtime will use COM interop instead of remoting for all calls across application domain boundaries.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<PreferComInsteadOfManagedRemoting>**  
  
## <a name="syntax"></a><span data-ttu-id="bb376-105">语法</span><span class="sxs-lookup"><span data-stu-id="bb376-105">Syntax</span></span>  
  
```xml  
<PreferComInsteadOfManagedRemoting enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bb376-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bb376-106">Attributes and Elements</span></span>  

 <span data-ttu-id="bb376-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bb376-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bb376-108">特性</span><span class="sxs-lookup"><span data-stu-id="bb376-108">Attributes</span></span>  
  
|<span data-ttu-id="bb376-109">属性</span><span class="sxs-lookup"><span data-stu-id="bb376-109">Attribute</span></span>|<span data-ttu-id="bb376-110">描述</span><span class="sxs-lookup"><span data-stu-id="bb376-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="bb376-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="bb376-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="bb376-112">指示运行时是否将使用 COM 互操作，而不是跨应用程序域边界进行远程处理。</span><span class="sxs-lookup"><span data-stu-id="bb376-112">Indicates whether the runtime will use COM interop instead of remoting across application domain boundaries.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="bb376-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="bb376-113">enabled Attribute</span></span>  
  
|<span data-ttu-id="bb376-114">值</span><span class="sxs-lookup"><span data-stu-id="bb376-114">Value</span></span>|<span data-ttu-id="bb376-115">说明</span><span class="sxs-lookup"><span data-stu-id="bb376-115">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="bb376-116">运行时将跨应用程序域边界使用远程处理。</span><span class="sxs-lookup"><span data-stu-id="bb376-116">The runtime will use remoting across application domain boundaries.</span></span> <span data-ttu-id="bb376-117">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="bb376-117">This is the default.</span></span>|  
|`true`|<span data-ttu-id="bb376-118">运行时将跨应用程序域边界使用 COM 互操作。</span><span class="sxs-lookup"><span data-stu-id="bb376-118">The runtime will use COM interop across application domain boundaries.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bb376-119">子元素</span><span class="sxs-lookup"><span data-stu-id="bb376-119">Child Elements</span></span>  

 <span data-ttu-id="bb376-120">无。</span><span class="sxs-lookup"><span data-stu-id="bb376-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bb376-121">父元素</span><span class="sxs-lookup"><span data-stu-id="bb376-121">Parent Elements</span></span>  
  
|<span data-ttu-id="bb376-122">元素</span><span class="sxs-lookup"><span data-stu-id="bb376-122">Element</span></span>|<span data-ttu-id="bb376-123">说明</span><span class="sxs-lookup"><span data-stu-id="bb376-123">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="bb376-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="bb376-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="bb376-125">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="bb376-125">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bb376-126">备注</span><span class="sxs-lookup"><span data-stu-id="bb376-126">Remarks</span></span>  

 <span data-ttu-id="bb376-127">将 `enabled` 属性设置为时 `true` ，运行时的行为如下所示：</span><span class="sxs-lookup"><span data-stu-id="bb376-127">When you set the `enabled` attribute to `true`, the runtime behaves as follows:</span></span>  
  
- <span data-ttu-id="bb376-128">当[iunknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)接口通过 COM 接口进入域时，运行时不为[IManagedObject](../../../unmanaged-api/hosting/imanagedobject-interface.md)接口调用[iunknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="bb376-128">The runtime does not call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for an [IManagedObject](../../../unmanaged-api/hosting/imanagedobject-interface.md) interface when an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface enters the domain through a COM interface.</span></span> <span data-ttu-id="bb376-129">相反，它会构造一个 [运行时可调用包装](../../../../standard/native-interop/runtime-callable-wrapper.md) 器 (对象周围的 RCW) 。</span><span class="sxs-lookup"><span data-stu-id="bb376-129">Instead, it constructs a [Runtime Callable Wrapper](../../../../standard/native-interop/runtime-callable-wrapper.md) (RCW) around the object.</span></span>  
  
- <span data-ttu-id="bb376-130">运行时在接收到 `QueryInterface` 在此域中创建 (CCW) 的任何[COM 可调用包装](../../../../standard/native-interop/com-callable-wrapper.md)器的[IManagedObject](../../../unmanaged-api/hosting/imanagedobject-interface.md)接口调用时返回 E_NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="bb376-130">The runtime returns E_NOINTERFACE when it receives a `QueryInterface` call for an [IManagedObject](../../../unmanaged-api/hosting/imanagedobject-interface.md) interface for any [COM Callable Wrapper](../../../../standard/native-interop/com-callable-wrapper.md) (CCW) that has been created in this domain.</span></span>  
  
 <span data-ttu-id="bb376-131">这两个行为确保跨应用程序域边界在托管对象之间对 COM 接口进行的所有调用均使用 COM 和 COM 互操作，而不是远程处理。</span><span class="sxs-lookup"><span data-stu-id="bb376-131">These two behaviors ensure that all calls over COM interfaces between managed objects across application domain boundaries use COM and COM interop instead of remoting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb376-132">示例</span><span class="sxs-lookup"><span data-stu-id="bb376-132">Example</span></span>  

 <span data-ttu-id="bb376-133">下面的示例演示如何指定运行时应跨隔离边界使用 COM 互操作：</span><span class="sxs-lookup"><span data-stu-id="bb376-133">The following example shows how to specify that the runtime should use COM interop across isolation boundaries:</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <PreferComInsteadOfManagedRemoting enabled="true"/>  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="bb376-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb376-134">See also</span></span>

- [<span data-ttu-id="bb376-135">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="bb376-135">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="bb376-136">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="bb376-136">Configuration File Schema</span></span>](../index.md)
