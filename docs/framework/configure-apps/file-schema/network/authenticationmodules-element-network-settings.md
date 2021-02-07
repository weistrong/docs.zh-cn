---
description: '了解详细信息： <authenticationModules> 元素 (网络设置) '
title: <authenticationModules> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#authenticationModules
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules
helpviewer_keywords:
- authenticationModules element
- <authenticationModules> element
ms.assetid: 10fcfaad-82ef-4692-871a-0aec9dfbe75e
ms.openlocfilehash: 2c2dc3c6a3d8fc064bb24c3d86a4441c269e43f0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698604"
---
# <a name="authenticationmodules-element-network-settings"></a><span data-ttu-id="da2e8-103">\<authenticationModules> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="da2e8-103">\<authenticationModules> Element (Network Settings)</span></span>

<span data-ttu-id="da2e8-104">指定用于对网络请求进行身份验证的模块。</span><span class="sxs-lookup"><span data-stu-id="da2e8-104">Specifies modules used to authenticate network requests.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<authenticationModules>**

## <a name="syntax"></a><span data-ttu-id="da2e8-105">语法</span><span class="sxs-lookup"><span data-stu-id="da2e8-105">Syntax</span></span>  
  
```xml  
<authenticationModules>
</authenticationModules>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="da2e8-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="da2e8-106">Attributes and Elements</span></span>  

 <span data-ttu-id="da2e8-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da2e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="da2e8-108">特性</span><span class="sxs-lookup"><span data-stu-id="da2e8-108">Attributes</span></span>  

 <span data-ttu-id="da2e8-109">无。</span><span class="sxs-lookup"><span data-stu-id="da2e8-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="da2e8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="da2e8-110">Child Elements</span></span>  
  
|<span data-ttu-id="da2e8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="da2e8-111">**Element**</span></span>|<span data-ttu-id="da2e8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="da2e8-112">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="da2e8-113">add</span><span class="sxs-lookup"><span data-stu-id="da2e8-113">add</span></span>](add-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="da2e8-114">向应用程序添加身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="da2e8-114">Adds an authentication module to the application.</span></span>|  
|[<span data-ttu-id="da2e8-115">clear</span><span class="sxs-lookup"><span data-stu-id="da2e8-115">clear</span></span>](clear-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="da2e8-116">清除应用程序中的所有身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="da2e8-116">Clears all authentication modules from the application.</span></span>|  
|[<span data-ttu-id="da2e8-117">删除</span><span class="sxs-lookup"><span data-stu-id="da2e8-117">remove</span></span>](remove-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="da2e8-118">从应用程序中移除身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="da2e8-118">Removes an authentication module from the application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="da2e8-119">父元素</span><span class="sxs-lookup"><span data-stu-id="da2e8-119">Parent Elements</span></span>  
  
|<span data-ttu-id="da2e8-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="da2e8-120">**Element**</span></span>|<span data-ttu-id="da2e8-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="da2e8-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="da2e8-122">system.net</span><span class="sxs-lookup"><span data-stu-id="da2e8-122">system.net</span></span>](system-net-element-network-settings.md)|<span data-ttu-id="da2e8-123">包含指定 .NET Framework 如何连接到网络的设置。</span><span class="sxs-lookup"><span data-stu-id="da2e8-123">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="da2e8-124">备注</span><span class="sxs-lookup"><span data-stu-id="da2e8-124">Remarks</span></span>  

 <span data-ttu-id="da2e8-125">`authenticationModule`元素指定对服务器执行身份验证过程的身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="da2e8-125">The `authenticationModule` element specifies the authentication modules that conduct the authentication process with a server.</span></span> <span data-ttu-id="da2e8-126">身份验证模块必须实现 <xref:System.Net.IAuthenticationModule> 接口。</span><span class="sxs-lookup"><span data-stu-id="da2e8-126">An authentication module must implement the <xref:System.Net.IAuthenticationModule> interface.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="da2e8-127">配置文件</span><span class="sxs-lookup"><span data-stu-id="da2e8-127">Configuration Files</span></span>  

 <span data-ttu-id="da2e8-128">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="da2e8-128">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="da2e8-129">示例</span><span class="sxs-lookup"><span data-stu-id="da2e8-129">Example</span></span>  

 <span data-ttu-id="da2e8-130">下面的示例启用了身份验证模块。</span><span class="sxs-lookup"><span data-stu-id="da2e8-130">The following example enables an authentication module.</span></span> <span data-ttu-id="da2e8-131">应将版本和 PublicKeyToken 的值替换为指定模块的正确值。</span><span class="sxs-lookup"><span data-stu-id="da2e8-131">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <add type="System.Net.DigestClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="da2e8-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="da2e8-132">See also</span></span>

- <xref:System.Net.IAuthenticationModule>
- <xref:System.Net.AuthenticationManager>
- [<span data-ttu-id="da2e8-133">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="da2e8-133">Network Settings Schema</span></span>](index.md)
