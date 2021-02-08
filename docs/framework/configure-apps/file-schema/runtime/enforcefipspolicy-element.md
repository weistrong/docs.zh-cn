---
description: 了解详细信息： <enforceFIPSPolicy> 元素
title: <enforceFIPSPolicy> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- enforceFIPSPolicy element
- FIPS
- <enforceFIPSPolicy> element
- Federal Information Processing Standards (FIPS)
ms.assetid: c35509c4-35cf-43c0-bb47-75e4208aa24e
ms.openlocfilehash: d445570db634867a15b6d97d4e20186bd0641c2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787066"
---
# <a name="enforcefipspolicy-element"></a><span data-ttu-id="6b4f7-103">\<enforceFIPSPolicy> 元素</span><span class="sxs-lookup"><span data-stu-id="6b4f7-103">\<enforceFIPSPolicy> Element</span></span>

<span data-ttu-id="6b4f7-104">指定是否强制执行以下计算机配置要求：加密算法必须符合美国联邦信息处理标准 (FIPS)。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-104">Specifies whether to enforce a computer configuration requirement that cryptographic algorithms must comply with the Federal Information Processing Standards (FIPS).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<enforceFIPSPolicy>**  
  
## <a name="syntax"></a><span data-ttu-id="6b4f7-105">语法</span><span class="sxs-lookup"><span data-stu-id="6b4f7-105">Syntax</span></span>  
  
```xml  
<enforceFIPSPolicy enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6b4f7-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6b4f7-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6b4f7-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6b4f7-108">特性</span><span class="sxs-lookup"><span data-stu-id="6b4f7-108">Attributes</span></span>  
  
|<span data-ttu-id="6b4f7-109">属性</span><span class="sxs-lookup"><span data-stu-id="6b4f7-109">Attribute</span></span>|<span data-ttu-id="6b4f7-110">说明</span><span class="sxs-lookup"><span data-stu-id="6b4f7-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6b4f7-111">enabled</span><span class="sxs-lookup"><span data-stu-id="6b4f7-111">enabled</span></span>|<span data-ttu-id="6b4f7-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="6b4f7-113">指定是否允许强制执行计算机配置要求，要求加密算法必须符合 FIPS。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-113">Specifies whether to enable the enforcement of a computer configuration requirement that cryptographic algorithms must be compliant with FIPS.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="6b4f7-114">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="6b4f7-114">enabled Attribute</span></span>  
  
|<span data-ttu-id="6b4f7-115">值</span><span class="sxs-lookup"><span data-stu-id="6b4f7-115">Value</span></span>|<span data-ttu-id="6b4f7-116">说明</span><span class="sxs-lookup"><span data-stu-id="6b4f7-116">Description</span></span>|  
|-----------|-----------------|  
|`true`|<span data-ttu-id="6b4f7-117">如果你的计算机配置为要求加密算法符合 FIPS 标准，则强制实施此要求。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-117">If your computer is configured to require cryptographic algorithms to be FIPS compliant, that requirement is enforced.</span></span> <span data-ttu-id="6b4f7-118">如果某个类实现了不符合 FIPS 的算法，则该类的构造函数或方法将在 `Create` 该计算机上运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-118">If a class implements an algorithm that is not compliant with FIPS, the constructors or `Create` methods for that class throw exceptions when they are run on that computer.</span></span> <span data-ttu-id="6b4f7-119">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-119">This is the default.</span></span>|  
|`false`|<span data-ttu-id="6b4f7-120">无论计算机配置如何，应用程序使用的加密算法都无需符合 FIPS。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-120">Cryptographic algorithms that are used by the application are not required to be compliant with FIPS, regardless of computer configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6b4f7-121">子元素</span><span class="sxs-lookup"><span data-stu-id="6b4f7-121">Child Elements</span></span>  

 <span data-ttu-id="6b4f7-122">无。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6b4f7-123">父元素</span><span class="sxs-lookup"><span data-stu-id="6b4f7-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6b4f7-124">元素</span><span class="sxs-lookup"><span data-stu-id="6b4f7-124">Element</span></span>|<span data-ttu-id="6b4f7-125">说明</span><span class="sxs-lookup"><span data-stu-id="6b4f7-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6b4f7-126">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="6b4f7-127">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6b4f7-128">备注</span><span class="sxs-lookup"><span data-stu-id="6b4f7-128">Remarks</span></span>  

 <span data-ttu-id="6b4f7-129">从 .NET Framework 2.0 开始，实现加密算法的类的创建由计算机的配置控制。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-129">Starting with the .NET Framework 2.0, the creation of classes that implement cryptographic algorithms is controlled by the configuration of the computer.</span></span> <span data-ttu-id="6b4f7-130">如果计算机配置为要求算法符合 FIPS，并且类实现了不符合 FIPS 的算法，则创建该类的实例的任何尝试都将引发异常。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-130">If the computer is configured to require algorithms to be compliant with FIPS, and a class implements an algorithm that is not compliant with FIPS, any attempt to create an instance of that class throws an exception.</span></span> <span data-ttu-id="6b4f7-131">构造函数引发 <xref:System.InvalidOperationException> 异常，并且 `Create` 方法引发异常，并出现 <xref:System.Reflection.TargetInvocationException> 内部 <xref:System.InvalidOperationException> 异常。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-131">Constructors throw an <xref:System.InvalidOperationException> exception, and `Create` methods throw a <xref:System.Reflection.TargetInvocationException> exception with an inner <xref:System.InvalidOperationException> exception.</span></span>  
  
 <span data-ttu-id="6b4f7-132">如果你的应用程序运行在其配置要求符合 FIPS 的计算机上，并且你的应用程序使用不符合 FIPS 的算法，则可以使用配置文件中的此元素来阻止公共语言运行时 (CLR) 强制执行 FIPS 相容性。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-132">If your application runs on computers whose configurations require compliance with FIPS, and your application uses an algorithm that is not compliant with FIPS, you can use this element in your configuration file to prevent the common language runtime (CLR) from enforcing FIPS compliance.</span></span> <span data-ttu-id="6b4f7-133">此元素是在 .NET Framework 2.0 Service Pack 1 中引入的。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-133">This element was introduced in the .NET Framework 2.0 Service Pack 1.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b4f7-134">示例</span><span class="sxs-lookup"><span data-stu-id="6b4f7-134">Example</span></span>  

 <span data-ttu-id="6b4f7-135">下面的示例演示如何阻止 CLR 强制实施 FIPS 相容性。</span><span class="sxs-lookup"><span data-stu-id="6b4f7-135">The following example shows how to prevent the CLR from enforcing FIPS compliance.</span></span>  
  
```xml  
<configuration>  
    <runtime>  
        <enforceFIPSPolicy enabled="false"/>  
    </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6b4f7-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="6b4f7-136">See also</span></span>

- [<span data-ttu-id="6b4f7-137">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="6b4f7-137">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="6b4f7-138">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="6b4f7-138">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="6b4f7-139">加密模型</span><span class="sxs-lookup"><span data-stu-id="6b4f7-139">Cryptography Model</span></span>](../../../../standard/security/cryptography-model.md)
