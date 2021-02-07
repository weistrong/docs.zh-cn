---
description: 了解详细信息： <policyImporter>
title: <policyImporter>
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 2103c424aef081b72fa822ed207537195b8fdea9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683510"
---
# \<policyImporter>

<span data-ttu-id="5509f-102">指定一个策略导入程序，用于控制有关绑定的自定义策略断言的导入。</span><span class="sxs-lookup"><span data-stu-id="5509f-102">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<client>**](client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<metadata>**](metadata.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<policyImporters>**](policyimporters.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<policyImporter>**  
  
## <a name="syntax"></a><span data-ttu-id="5509f-103">语法</span><span class="sxs-lookup"><span data-stu-id="5509f-103">Syntax</span></span>  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5509f-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5509f-104">Attributes and Elements</span></span>  

 <span data-ttu-id="5509f-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5509f-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5509f-106">特性</span><span class="sxs-lookup"><span data-stu-id="5509f-106">Attributes</span></span>  
  
|<span data-ttu-id="5509f-107">属性</span><span class="sxs-lookup"><span data-stu-id="5509f-107">Attribute</span></span>|<span data-ttu-id="5509f-108">说明</span><span class="sxs-lookup"><span data-stu-id="5509f-108">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="5509f-109">此元素的类型。</span><span class="sxs-lookup"><span data-stu-id="5509f-109">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5509f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5509f-110">Child Elements</span></span>  

 <span data-ttu-id="5509f-111">无</span><span class="sxs-lookup"><span data-stu-id="5509f-111">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5509f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5509f-112">Parent Elements</span></span>  
  
|<span data-ttu-id="5509f-113">元素</span><span class="sxs-lookup"><span data-stu-id="5509f-113">Element</span></span>|<span data-ttu-id="5509f-114">说明</span><span class="sxs-lookup"><span data-stu-id="5509f-114">Description</span></span>|  
|-------------|-----------------|  
|[\<policyImporters>](policyimporters.md)|<span data-ttu-id="5509f-115">指定用于控制有关绑定的自定义策略断言的导入的所有策略导入程序。</span><span class="sxs-lookup"><span data-stu-id="5509f-115">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5509f-116">备注</span><span class="sxs-lookup"><span data-stu-id="5509f-116">Remarks</span></span>  

 <span data-ttu-id="5509f-117">策略导入程序用于搜索有关绑定功能的自定义策略断言，并附加一个实现断言所需功能的自定义绑定元素。</span><span class="sxs-lookup"><span data-stu-id="5509f-117">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5509f-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="5509f-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.PolicyImporterElement>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Description.MetadataImporter>
- [<span data-ttu-id="5509f-119">WCF 客户端配置</span><span class="sxs-lookup"><span data-stu-id="5509f-119">WCF Client Configuration</span></span>](../../../wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="5509f-120">客户端</span><span class="sxs-lookup"><span data-stu-id="5509f-120">Clients</span></span>](../../../wcf/feature-details/clients.md)
