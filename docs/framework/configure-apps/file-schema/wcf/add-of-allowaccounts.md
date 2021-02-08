---
description: 了解详细 <add> 信息： <allowAccounts>
title: <add> 的 <allowAccounts>
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 275631c4467a888966e89a2f664b186f989ae101
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782216"
---
# <a name="add-of-allowaccounts"></a><span data-ttu-id="d67f1-103">\<add> 的 \<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="d67f1-103">\<add> of \<allowAccounts></span></span>

<span data-ttu-id="d67f1-104">为承载 WCF 服务且被授予对共享服务的连接访问权限的进程指定用户帐户。</span><span class="sxs-lookup"><span data-stu-id="d67f1-104">Specifies a user account for processes that host WCF services, and are granted connection access to the sharing service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel.activation>**](system-servicemodel-activation.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<net.pipe>**](net-pipe.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<allowAccounts>**](allowaccounts.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="d67f1-105">语法</span><span class="sxs-lookup"><span data-stu-id="d67f1-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d67f1-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d67f1-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d67f1-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d67f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d67f1-108">特性</span><span class="sxs-lookup"><span data-stu-id="d67f1-108">Attributes</span></span>  
  
|<span data-ttu-id="d67f1-109">属性</span><span class="sxs-lookup"><span data-stu-id="d67f1-109">Attribute</span></span>|<span data-ttu-id="d67f1-110">说明</span><span class="sxs-lookup"><span data-stu-id="d67f1-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d67f1-111">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="d67f1-111">securityIdentifier</span></span>|<span data-ttu-id="d67f1-112">一个字符串，指定用于标识用户帐户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="d67f1-112">A string that specifies a unique identifier used to identify a user account.</span></span> <span data-ttu-id="d67f1-113">默认值为 LocalSystem、Administrators、NS、LS 和 IIS_USRS。</span><span class="sxs-lookup"><span data-stu-id="d67f1-113">The default values are LocalSystem, Administrators, NS, LS, and IIS_USRS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d67f1-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d67f1-114">Child Elements</span></span>  

 <span data-ttu-id="d67f1-115">无。</span><span class="sxs-lookup"><span data-stu-id="d67f1-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d67f1-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d67f1-116">Parent Elements</span></span>  
  
|<span data-ttu-id="d67f1-117">元素</span><span class="sxs-lookup"><span data-stu-id="d67f1-117">Element</span></span>|<span data-ttu-id="d67f1-118">说明</span><span class="sxs-lookup"><span data-stu-id="d67f1-118">Description</span></span>|  
|-------------|-----------------|  
|[\<allowAccounts>](allowaccounts.md)|<span data-ttu-id="d67f1-119">一个配置元素的集合，这些元素包含一个 `securityIdentifier` 属性，用于为承载 WCF 服务并被授予对共享服务的连接访问权限的进程指定用户帐户。</span><span class="sxs-lookup"><span data-stu-id="d67f1-119">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d67f1-120">示例</span><span class="sxs-lookup"><span data-stu-id="d67f1-120">Example</span></span>  

 <span data-ttu-id="d67f1-121">下面的配置示例将用户帐户的五个默认标识符添加到此集合中。</span><span class="sxs-lookup"><span data-stu-id="d67f1-121">The following configuration example adds the five default identifiers for user accounts to this collection.</span></span>  
  
```xml  
<allowAccounts>
  <!-- LocalSystem account -->
  <add securityIdentifier="S-1-5-18" />
  <!-- LocalService account -->
  <add securityIdentifier="S-1-5-19" />
  <!-- Administrators account -->
  <add securityIdentifier="S-1-5-20" />
  <!-- Network Service account -->
  <add securityIdentifier="S-1-5-32-544" />
  <!-- IIS_IUSRS account (Vista only) -->
  <add securityIdentifier="S-1-5-32-568" />
</allowAccounts>
```  
  
## <a name="see-also"></a><span data-ttu-id="d67f1-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="d67f1-122">See also</span></span>

- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
