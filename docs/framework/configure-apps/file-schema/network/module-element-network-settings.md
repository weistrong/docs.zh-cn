---
description: '了解详细信息： <module> 元素 (网络设置) '
title: <module> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#module
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/module
helpviewer_keywords:
- module element
- <module> element
ms.assetid: 10318725-9666-4d65-ab61-b94c64e59f13
ms.openlocfilehash: d498b79ae6046367bc81add5ea387e178ab6c29d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652830"
---
# <a name="module-element-network-settings"></a><span data-ttu-id="82a1e-103">\<module> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="82a1e-103">\<module> Element (Network Settings)</span></span>

<span data-ttu-id="82a1e-104">向应用程序添加新的代理模块。</span><span class="sxs-lookup"><span data-stu-id="82a1e-104">Adds a new proxy module to the application.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<defaultProxy>**](defaultproxy-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<module>**

## <a name="syntax"></a><span data-ttu-id="82a1e-105">语法</span><span class="sxs-lookup"><span data-stu-id="82a1e-105">Syntax</span></span>  
  
```xml  
<module
  type="type_fullname, assembly_fullname"
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="82a1e-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="82a1e-106">Attributes and Elements</span></span>  

 <span data-ttu-id="82a1e-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82a1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="82a1e-108">特性</span><span class="sxs-lookup"><span data-stu-id="82a1e-108">Attributes</span></span>  
  
|<span data-ttu-id="82a1e-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="82a1e-109">**Attribute**</span></span>|<span data-ttu-id="82a1e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="82a1e-110">**Description**</span></span>|  
|-------------------|---------------------|  
|`type`|<span data-ttu-id="82a1e-111">完全限定的类型名称 (由) 的 <xref:System.Type.FullName%2A> 属性和程序集名称指示 (由 <xref:System.Reflection.Assembly.FullName%2A> 实现代理的由逗号分隔的属性) 。</span><span class="sxs-lookup"><span data-stu-id="82a1e-111">The fully qualified type name (indicated by the <xref:System.Type.FullName%2A> property) and the assembly name (indicated by the <xref:System.Reflection.Assembly.FullName%2A> property), separated by a comma, that implements the proxy.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="82a1e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="82a1e-112">Child Elements</span></span>  

 <span data-ttu-id="82a1e-113">无。</span><span class="sxs-lookup"><span data-stu-id="82a1e-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="82a1e-114">父元素</span><span class="sxs-lookup"><span data-stu-id="82a1e-114">Parent Elements</span></span>  
  
|<span data-ttu-id="82a1e-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="82a1e-115">**Element**</span></span>|<span data-ttu-id="82a1e-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="82a1e-116">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="82a1e-117">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="82a1e-117">defaultProxy</span></span>](defaultproxy-element-network-settings.md)|<span data-ttu-id="82a1e-118">配置超文本传输协议 (HTTP) 代理服务器。</span><span class="sxs-lookup"><span data-stu-id="82a1e-118">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="82a1e-119">备注</span><span class="sxs-lookup"><span data-stu-id="82a1e-119">Remarks</span></span>  

 <span data-ttu-id="82a1e-120">`module`元素注册用于实现接口的代理类 <xref:System.Net.IWebProxy> 。</span><span class="sxs-lookup"><span data-stu-id="82a1e-120">The `module` element registers proxy classes that implement the <xref:System.Net.IWebProxy> interface.</span></span> <span data-ttu-id="82a1e-121">在注册代理类之后，该 `module` 可用于通过所支持的代理请求信息。</span><span class="sxs-lookup"><span data-stu-id="82a1e-121">After registering the proxy class, `module` can be used to request information through the supported proxy.</span></span>  
  
 <span data-ttu-id="82a1e-122">该属性的值 `type` 应为模块的类名称及其对应的动态链接库的名称 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="82a1e-122">The value for the `type` attribute should be the class name of the module and the name of its corresponding Dynamic Link Library (DLL).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="82a1e-123">配置文件</span><span class="sxs-lookup"><span data-stu-id="82a1e-123">Configuration Files</span></span>  

 <span data-ttu-id="82a1e-124">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="82a1e-124">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="82a1e-125">示例</span><span class="sxs-lookup"><span data-stu-id="82a1e-125">Example</span></span>  

 <span data-ttu-id="82a1e-126">下面的示例注册自定义代理类。</span><span class="sxs-lookup"><span data-stu-id="82a1e-126">The following example registers a custom proxy class.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <module  
        type="Test.CustomWebProxy, TestProxy, Version=2.0.3600.0, Culture=neutral, PublicKeyToken=b23a5c561934e385"  
      />  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="82a1e-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="82a1e-127">See also</span></span>

- <xref:System.Net.IWebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="82a1e-128">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="82a1e-128">Network Settings Schema</span></span>](index.md)
