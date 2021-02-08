---
description: '详细了解： <remove> authenticationModules 的元素 (网络设置) '
title: authenticationModules 的 <remove> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- remove element, authenticationModules
- <authenticationModules>, remove element
- <remove> element, authenticationModules
- authenticationModules, remove element
ms.assetid: abf79949-b05c-465a-b51c-bbeda9a74173
ms.openlocfilehash: 7c97cd20717e6e0945cf77ad6584b319120ec6a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804083"
---
# <a name="remove-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="1ffd1-103">authenticationModules 的 \<remove> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="1ffd1-103">\<remove> Element for authenticationModules (Network Settings)</span></span>

<span data-ttu-id="1ffd1-104">从应用程序中移除身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-104">Removes an authentication module from the application.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<authenticationModules>**](authenticationmodules-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**

## <a name="syntax"></a><span data-ttu-id="1ffd1-105">语法</span><span class="sxs-lookup"><span data-stu-id="1ffd1-105">Syntax</span></span>  
  
```xml  
<remove
   type="authentication module name"
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1ffd1-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1ffd1-106">Attributes and Elements</span></span>  

 <span data-ttu-id="1ffd1-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1ffd1-108">特性</span><span class="sxs-lookup"><span data-stu-id="1ffd1-108">Attributes</span></span>  
  
|<span data-ttu-id="1ffd1-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1ffd1-109">**Attribute**</span></span>|<span data-ttu-id="1ffd1-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ffd1-110">**Description**</span></span>|  
|-------------------|---------------------|  
|<span data-ttu-id="1ffd1-111">type </span><span class="sxs-lookup"><span data-stu-id="1ffd1-111">**type**</span></span>|<span data-ttu-id="1ffd1-112">要删除的身份验证模块的名称。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-112">The name of the authentication module to remove.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1ffd1-113">子元素</span><span class="sxs-lookup"><span data-stu-id="1ffd1-113">Child Elements</span></span>  

 <span data-ttu-id="1ffd1-114">无。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1ffd1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1ffd1-115">Parent Elements</span></span>  
  
|<span data-ttu-id="1ffd1-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ffd1-116">**Element**</span></span>|<span data-ttu-id="1ffd1-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ffd1-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="1ffd1-118">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="1ffd1-118">authenticationModules</span></span>](authenticationmodules-element-network-settings.md)|<span data-ttu-id="1ffd1-119">指定用于对网络请求进行身份验证的模块。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-119">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1ffd1-120">备注</span><span class="sxs-lookup"><span data-stu-id="1ffd1-120">Remarks</span></span>  

 <span data-ttu-id="1ffd1-121">`remove`元素删除之前在配置文件或配置层次结构的较高级别中定义的身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-121">The `remove` element removes authentication modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
 <span data-ttu-id="1ffd1-122">特性的值 `type` 应为有效的类名。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-122">The value for the `type` attribute should be a valid class name.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="1ffd1-123">配置文件</span><span class="sxs-lookup"><span data-stu-id="1ffd1-123">Configuration Files</span></span>  

 <span data-ttu-id="1ffd1-124">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-124">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1ffd1-125">示例</span><span class="sxs-lookup"><span data-stu-id="1ffd1-125">Example</span></span>  

 <span data-ttu-id="1ffd1-126">下面的示例将删除身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="1ffd1-126">The following example removes an authentication module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <remove type="System.Net.NtlmClient" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1ffd1-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="1ffd1-127">See also</span></span>

- <xref:System.Net.IAuthenticationModule>
- <xref:System.Net.AuthenticationManager>
- [<span data-ttu-id="1ffd1-128">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="1ffd1-128">Network Settings Schema</span></span>](index.md)
