---
description: 了解详细 <add> 信息： <backupList>
title: <add> 的 <backupList>
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: 9855d93be011b4eaa2890c4d24392fde3b65d05a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804070"
---
# <a name="add-of-backuplist"></a><span data-ttu-id="9a39c-103">\<add> 的 \<backupList></span><span class="sxs-lookup"><span data-stu-id="9a39c-103">\<add> of \<backupList></span></span>

<span data-ttu-id="9a39c-104">表示定义备份终结点元素的配置元素。</span><span class="sxs-lookup"><span data-stu-id="9a39c-104">Represents a configuration element that defines a backup endpoint element.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<backupLists>**](backuplists.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<backupList>**](backuplist.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="9a39c-105">语法</span><span class="sxs-lookup"><span data-stu-id="9a39c-105">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9a39c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9a39c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="9a39c-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a39c-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9a39c-108">特性</span><span class="sxs-lookup"><span data-stu-id="9a39c-108">Attributes</span></span>  
  
|<span data-ttu-id="9a39c-109">属性</span><span class="sxs-lookup"><span data-stu-id="9a39c-109">Attribute</span></span>|<span data-ttu-id="9a39c-110">说明</span><span class="sxs-lookup"><span data-stu-id="9a39c-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9a39c-111">name</span><span class="sxs-lookup"><span data-stu-id="9a39c-111">name</span></span>|<span data-ttu-id="9a39c-112">一个字符串，指定备份终结点的名称。</span><span class="sxs-lookup"><span data-stu-id="9a39c-112">A string that specifies the name of the backup endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9a39c-113">子元素</span><span class="sxs-lookup"><span data-stu-id="9a39c-113">Child Elements</span></span>  

 <span data-ttu-id="9a39c-114">无。</span><span class="sxs-lookup"><span data-stu-id="9a39c-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9a39c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9a39c-115">Parent Elements</span></span>  
  
|<span data-ttu-id="9a39c-116">元素</span><span class="sxs-lookup"><span data-stu-id="9a39c-116">Element</span></span>|<span data-ttu-id="9a39c-117">说明</span><span class="sxs-lookup"><span data-stu-id="9a39c-117">Description</span></span>|  
|-------------|-----------------|  
|[\<routing>](routing.md)|<span data-ttu-id="9a39c-118">包含当无法访问主终结点时路由服务将使用的终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="9a39c-118">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9a39c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a39c-119">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType>
