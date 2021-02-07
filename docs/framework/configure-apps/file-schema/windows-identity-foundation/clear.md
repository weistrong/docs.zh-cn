---
description: 了解详细信息： <clear>
title: <clear>
ms.date: 03/30/2017
ms.assetid: 54dcd1d1-038f-4fc8-a3a4-56ba7a1ca0fd
author: BrucePerlerMS
ms.openlocfilehash: 460add2722779a61dacc5c7510ea0a94aaef4a3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664127"
---
# \<clear>

<span data-ttu-id="0ec2a-102">清除当前标记处理程序集合中的所有安全标记处理程序。</span><span class="sxs-lookup"><span data-stu-id="0ec2a-102">Clears all security token handlers from the current token handler collection.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**  
  
## <a name="syntax"></a><span data-ttu-id="0ec2a-103">语法</span><span class="sxs-lookup"><span data-stu-id="0ec2a-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <clear>  
      </clear>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0ec2a-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0ec2a-104">Attributes and Elements</span></span>  

 <span data-ttu-id="0ec2a-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ec2a-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0ec2a-106">特性</span><span class="sxs-lookup"><span data-stu-id="0ec2a-106">Attributes</span></span>  

 <span data-ttu-id="0ec2a-107">无</span><span class="sxs-lookup"><span data-stu-id="0ec2a-107">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0ec2a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="0ec2a-108">Child Elements</span></span>  

 <span data-ttu-id="0ec2a-109">无</span><span class="sxs-lookup"><span data-stu-id="0ec2a-109">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0ec2a-110">父元素</span><span class="sxs-lookup"><span data-stu-id="0ec2a-110">Parent Elements</span></span>  
  
|<span data-ttu-id="0ec2a-111">元素</span><span class="sxs-lookup"><span data-stu-id="0ec2a-111">Element</span></span>|<span data-ttu-id="0ec2a-112">说明</span><span class="sxs-lookup"><span data-stu-id="0ec2a-112">Description</span></span>|  
|-------------|-----------------|  
|[\<securityTokenHandlers>](securitytokenhandlers.md)|<span data-ttu-id="0ec2a-113">指定注册到终结点的安全令牌处理程序的集合。</span><span class="sxs-lookup"><span data-stu-id="0ec2a-113">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|
