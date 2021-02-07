---
description: 了解详细信息： <claimType>
title: <claimType>
ms.date: 03/30/2017
ms.assetid: d17b5831-9a2c-45c4-b0d1-68f48e72e861
author: BrucePerlerMS
ms.openlocfilehash: 55fd32edc7fb810742c3cf678b434675aebba00e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664218"
---
# \<claimType>

<span data-ttu-id="d9662-102">为传入安全令牌指定一个可选的或必需的声明。</span><span class="sxs-lookup"><span data-stu-id="d9662-102">Specifies a single optional or required claim for incoming security tokens.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<claimTypeRequired>**](claimtyperequired.md)\  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<claimType>**  
  
## <a name="syntax"></a><span data-ttu-id="d9662-103">语法</span><span class="sxs-lookup"><span data-stu-id="d9662-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
      <claimType type=URI optional=xs:boolean >  
      </claimType>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d9662-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d9662-104">Attributes and Elements</span></span>  

 <span data-ttu-id="d9662-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9662-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d9662-106">特性</span><span class="sxs-lookup"><span data-stu-id="d9662-106">Attributes</span></span>  
  
|<span data-ttu-id="d9662-107">属性</span><span class="sxs-lookup"><span data-stu-id="d9662-107">Attribute</span></span>|<span data-ttu-id="d9662-108">说明</span><span class="sxs-lookup"><span data-stu-id="d9662-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d9662-109">type</span><span class="sxs-lookup"><span data-stu-id="d9662-109">type</span></span>|<span data-ttu-id="d9662-110">声明类型。</span><span class="sxs-lookup"><span data-stu-id="d9662-110">The claim type.</span></span> <span data-ttu-id="d9662-111">通常为 URI。</span><span class="sxs-lookup"><span data-stu-id="d9662-111">Typically a URI.</span></span> <span data-ttu-id="d9662-112">必需。</span><span class="sxs-lookup"><span data-stu-id="d9662-112">Required.</span></span>|  
|<span data-ttu-id="d9662-113">可选</span><span class="sxs-lookup"><span data-stu-id="d9662-113">optional</span></span>|<span data-ttu-id="d9662-114">指定声明类型是否为可选的布尔值。</span><span class="sxs-lookup"><span data-stu-id="d9662-114">A boolean value that specifies whether the claim type is optional.</span></span> <span data-ttu-id="d9662-115">可选。</span><span class="sxs-lookup"><span data-stu-id="d9662-115">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d9662-116">子元素</span><span class="sxs-lookup"><span data-stu-id="d9662-116">Child Elements</span></span>  

 <span data-ttu-id="d9662-117">无</span><span class="sxs-lookup"><span data-stu-id="d9662-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d9662-118">父元素</span><span class="sxs-lookup"><span data-stu-id="d9662-118">Parent Elements</span></span>  
  
|<span data-ttu-id="d9662-119">元素</span><span class="sxs-lookup"><span data-stu-id="d9662-119">Element</span></span>|<span data-ttu-id="d9662-120">说明</span><span class="sxs-lookup"><span data-stu-id="d9662-120">Description</span></span>|  
|-------------|-----------------|  
|[\<claimTypeRequired>](claimtyperequired.md)|<span data-ttu-id="d9662-121">指定传入安全令牌所需的声明集。</span><span class="sxs-lookup"><span data-stu-id="d9662-121">Specifies the set of required claims for incoming security tokens.</span></span>|
