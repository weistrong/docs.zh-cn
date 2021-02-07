---
description: '详细了解： <clear> authenticationModules 的元素 (网络设置) '
title: authenticationModules 的 <clear> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- clear element, authenticationModules
- <authenticationModules>, clear element
- <clear> element, authenticationModules
- authenticationModules, clear element
ms.assetid: dc522c45-4a80-4831-8955-f7b68a47edfd
ms.openlocfilehash: ccfc9f53ef53268cdb1155673fc47a862a63419c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698565"
---
# <a name="clear-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="64875-103">authenticationModules 的 \<clear> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="64875-103">\<clear> Element for authenticationModules (Network Settings)</span></span>

<span data-ttu-id="64875-104">清除应用程序中的所有身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="64875-104">Clears all authentication modules from the application.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<authenticationModules>**](authenticationmodules-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a><span data-ttu-id="64875-105">语法</span><span class="sxs-lookup"><span data-stu-id="64875-105">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="64875-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="64875-106">Attributes and Elements</span></span>  

 <span data-ttu-id="64875-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64875-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="64875-108">特性</span><span class="sxs-lookup"><span data-stu-id="64875-108">Attributes</span></span>  

 <span data-ttu-id="64875-109">无。</span><span class="sxs-lookup"><span data-stu-id="64875-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="64875-110">子元素</span><span class="sxs-lookup"><span data-stu-id="64875-110">Child Elements</span></span>  

 <span data-ttu-id="64875-111">无。</span><span class="sxs-lookup"><span data-stu-id="64875-111">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="64875-112">父元素</span><span class="sxs-lookup"><span data-stu-id="64875-112">Parent Elements</span></span>  
  
|<span data-ttu-id="64875-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="64875-113">**Element**</span></span>|<span data-ttu-id="64875-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="64875-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="64875-115">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="64875-115">authenticationModules</span></span>](authenticationmodules-element-network-settings.md)|<span data-ttu-id="64875-116">指定用于对网络请求进行身份验证的模块。</span><span class="sxs-lookup"><span data-stu-id="64875-116">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64875-117">备注</span><span class="sxs-lookup"><span data-stu-id="64875-117">Remarks</span></span>  

 <span data-ttu-id="64875-118">`clear`元素删除之前在配置文件或配置层次结构的较高级别中定义的所有身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="64875-118">The `clear` element removes all authentication modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="64875-119">配置文件</span><span class="sxs-lookup"><span data-stu-id="64875-119">Configuration Files</span></span>  

 <span data-ttu-id="64875-120">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="64875-120">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="64875-121">示例</span><span class="sxs-lookup"><span data-stu-id="64875-121">Example</span></span>  

 <span data-ttu-id="64875-122">下面的示例删除所有配置的身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="64875-122">The following example removes all configured authentication modules.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <clear/>  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="64875-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="64875-123">See also</span></span>

- <xref:System.Net.IAuthenticationModule>
- <xref:System.Net.AuthenticationManager>
- [<span data-ttu-id="64875-124">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="64875-124">Network Settings Schema</span></span>](index.md)
