---
description: 了解详细信息： <serviceAuthenticationManager>
title: <serviceAuthenticationManager>
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: ae9c8d7f74b3ad7d0c61a77d20f38f228c695970
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786767"
---
# \<serviceAuthenticationManager>

<span data-ttu-id="88fa5-102">提供一个工作流配置元素，该元素在服务级别建立传输、消息或发起方的有效性。</span><span class="sxs-lookup"><span data-stu-id="88fa5-102">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceAuthenticationManager>**  
  
## <a name="syntax"></a><span data-ttu-id="88fa5-103">语法</span><span class="sxs-lookup"><span data-stu-id="88fa5-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="88fa5-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="88fa5-104">Attributes and Elements</span></span>  

 <span data-ttu-id="88fa5-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="88fa5-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="88fa5-106">特性</span><span class="sxs-lookup"><span data-stu-id="88fa5-106">Attributes</span></span>  
  
|<span data-ttu-id="88fa5-107">属性</span><span class="sxs-lookup"><span data-stu-id="88fa5-107">Attribute</span></span>|<span data-ttu-id="88fa5-108">说明</span><span class="sxs-lookup"><span data-stu-id="88fa5-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="88fa5-109">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="88fa5-109">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="88fa5-110">一个字符串，指定当前行为的身份验证策略类型。</span><span class="sxs-lookup"><span data-stu-id="88fa5-110">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="88fa5-111">子元素</span><span class="sxs-lookup"><span data-stu-id="88fa5-111">Child Elements</span></span>  

 <span data-ttu-id="88fa5-112">无。</span><span class="sxs-lookup"><span data-stu-id="88fa5-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="88fa5-113">父元素</span><span class="sxs-lookup"><span data-stu-id="88fa5-113">Parent Elements</span></span>  
  
|<span data-ttu-id="88fa5-114">元素</span><span class="sxs-lookup"><span data-stu-id="88fa5-114">Element</span></span>|<span data-ttu-id="88fa5-115">说明</span><span class="sxs-lookup"><span data-stu-id="88fa5-115">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="88fa5-116">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="88fa5-116">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="88fa5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="88fa5-117">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
