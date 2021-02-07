---
description: 了解详细信息： <claimTypeRequired>
title: <claimTypeRequired>
ms.date: 03/30/2017
ms.assetid: c469d71f-6c77-4a24-97aa-53efa126ceef
author: BrucePerlerMS
ms.openlocfilehash: ba95c56af431a6dd81323751a42ce47160544cc3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664166"
---
# \<claimTypeRequired>

<span data-ttu-id="0ee58-102">指定传入安全令牌所需的声明集。</span><span class="sxs-lookup"><span data-stu-id="0ee58-102">Specifies the set of required claims for incoming security tokens.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<claimTypeRequired>**  
  
## <a name="syntax"></a><span data-ttu-id="0ee58-103">语法</span><span class="sxs-lookup"><span data-stu-id="0ee58-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0ee58-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0ee58-104">Attributes and Elements</span></span>  

 <span data-ttu-id="0ee58-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ee58-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0ee58-106">特性</span><span class="sxs-lookup"><span data-stu-id="0ee58-106">Attributes</span></span>  

 <span data-ttu-id="0ee58-107">无</span><span class="sxs-lookup"><span data-stu-id="0ee58-107">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0ee58-108">子元素</span><span class="sxs-lookup"><span data-stu-id="0ee58-108">Child Elements</span></span>  
  
|<span data-ttu-id="0ee58-109">元素</span><span class="sxs-lookup"><span data-stu-id="0ee58-109">Element</span></span>|<span data-ttu-id="0ee58-110">说明</span><span class="sxs-lookup"><span data-stu-id="0ee58-110">Description</span></span>|  
|-------------|-----------------|  
|[\<claimType>](claimtype.md)|<span data-ttu-id="0ee58-111">为传入安全令牌指定一个可选的或必需的声明。</span><span class="sxs-lookup"><span data-stu-id="0ee58-111">Specifies a single optional or required claim for incoming security tokens.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0ee58-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0ee58-112">Parent Elements</span></span>  
  
|<span data-ttu-id="0ee58-113">元素</span><span class="sxs-lookup"><span data-stu-id="0ee58-113">Element</span></span>|<span data-ttu-id="0ee58-114">说明</span><span class="sxs-lookup"><span data-stu-id="0ee58-114">Description</span></span>|  
|-------------|-----------------|  
|[\<identityConfiguration>](identityconfiguration.md)|<span data-ttu-id="0ee58-115">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="0ee58-115">Specifies service-level identity settings.</span></span>|
