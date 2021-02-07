---
description: 了解详细信息： <customCookieHandler>
title: <customCookieHandler>
ms.date: 03/30/2017
ms.assetid: a03b153d-5ec6-4915-9031-6f0c3fd348be
author: BrucePerlerMS
ms.openlocfilehash: 6b433769c429ed4149efb324d7c4b216d6042705
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664075"
---
# \<customCookieHandler>

<span data-ttu-id="3b0f9-102">设置自定义 cookie 处理程序类型。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-102">Sets the custom cookie handler type.</span></span> <span data-ttu-id="3b0f9-103">仅当 `mode` 元素的属性 `<cookieHandler>` 为 "Custom" 时，此元素才能存在。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-103">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Custom".</span></span> <span data-ttu-id="3b0f9-104">自定义类型必须派生自 <xref:System.IdentityModel.Services.CookieHandler> 类。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-104">The custom type must be derived from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel.services>**](system-identitymodel-services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<federationConfiguration>**](federationconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<cookieHandler>**](cookiehandler.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<customCookieHandler>**  
  
## <a name="syntax"></a><span data-ttu-id="3b0f9-105">语法</span><span class="sxs-lookup"><span data-stu-id="3b0f9-105">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Custom">  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" >  
      </customCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3b0f9-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="3b0f9-106">Attributes and Elements</span></span>  

 <span data-ttu-id="3b0f9-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3b0f9-108">特性</span><span class="sxs-lookup"><span data-stu-id="3b0f9-108">Attributes</span></span>  
  
|<span data-ttu-id="3b0f9-109">属性</span><span class="sxs-lookup"><span data-stu-id="3b0f9-109">Attribute</span></span>|<span data-ttu-id="3b0f9-110">说明</span><span class="sxs-lookup"><span data-stu-id="3b0f9-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3b0f9-111">type</span><span class="sxs-lookup"><span data-stu-id="3b0f9-111">type</span></span>|<span data-ttu-id="3b0f9-112">指定从类派生的自定义类型 <xref:System.IdentityModel.Services.CookieHandler> 。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-112">Specifies a custom type that derives from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span> <span data-ttu-id="3b0f9-113">有关如何指定属性的详细信息 `type` ，请参阅 [自定义类型引用](../windows-workflow-foundation/index.md)。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-113">For more information about how to specify the `type` attribute, see [Custom Type References](../windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3b0f9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="3b0f9-114">Child Elements</span></span>  

 <span data-ttu-id="3b0f9-115">无</span><span class="sxs-lookup"><span data-stu-id="3b0f9-115">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3b0f9-116">父元素</span><span class="sxs-lookup"><span data-stu-id="3b0f9-116">Parent Elements</span></span>  
  
|<span data-ttu-id="3b0f9-117">元素</span><span class="sxs-lookup"><span data-stu-id="3b0f9-117">Element</span></span>|<span data-ttu-id="3b0f9-118">说明</span><span class="sxs-lookup"><span data-stu-id="3b0f9-118">Description</span></span>|  
|-------------|-----------------|  
|[\<cookieHandler>](cookiehandler.md)|<span data-ttu-id="3b0f9-119">配置用于 <xref:System.IdentityModel.Services.CookieHandler> <xref:System.IdentityModel.Services.SessionAuthenticationModule> 读取和写入 cookie 的。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-119">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3b0f9-120">备注</span><span class="sxs-lookup"><span data-stu-id="3b0f9-120">Remarks</span></span>  

 <span data-ttu-id="3b0f9-121">如果通过将元素的属性设置为 "Custom" 来指定自定义 cookie 处理程序 `mode` `<cookieHandler>` ，则必须通过包含 `<customCookieHandler>` 引用 cookie 处理程序类型的子元素来指定自定义 cookie 处理程序的类型。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-121">When you specify a custom cookie handler by setting the `mode` attribute of the `<cookieHandler>` element to "Custom", you must specify the type of the custom cookie handler by including a `<customCookieHandler>` child element that references the cookie handler type.</span></span> <span data-ttu-id="3b0f9-122">当 `mode` 特性设置为 "分块" 或 "Default" 时，不能指定此元素。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-122">This element cannot be specified when the `mode` attribute is set to "Chunked" or "Default".</span></span> <span data-ttu-id="3b0f9-123">自定义 cookie 处理程序必须派生自 <xref:System.IdentityModel.Services.CookieHandler> 类。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-123">Custom cookie handlers must derive from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="3b0f9-124">`<customCookieHandler>`元素由 <xref:System.IdentityModel.Configuration.CustomTypeElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-124">The `<customCookieHandler>` element is represented by the <xref:System.IdentityModel.Configuration.CustomTypeElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3b0f9-125">示例</span><span class="sxs-lookup"><span data-stu-id="3b0f9-125">Example</span></span>  

 <span data-ttu-id="3b0f9-126">下面的示例将 SAM 配置为使用类型的自定义 cookie 处理程序 `MyNamespace.MyCustomCookieHandler` 。</span><span class="sxs-lookup"><span data-stu-id="3b0f9-126">The following example configures the SAM to use a custom cookie handler of type `MyNamespace.MyCustomCookieHandler`.</span></span>  
  
```xml  
<cookieHandler mode="Custom">  
    <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3b0f9-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b0f9-127">See also</span></span>

- <xref:System.IdentityModel.Services.CookieHandler>
