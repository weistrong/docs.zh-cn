---
description: 了解详细信息： <persistableType>
title: <persistableType>
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: eadbb951d751dd88ce974edc8d5b343a1469b758
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683627"
---
# \<persistableType>

<span data-ttu-id="6c424-102">指定所有永久类型。</span><span class="sxs-lookup"><span data-stu-id="6c424-102">Specifies all the persistable types.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<comContracts>**](comcontracts.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<comContract>**](comcontract.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<persistableTypes>**](persistabletypes.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<persistableType>**  
  
## <a name="syntax"></a><span data-ttu-id="6c424-103">语法</span><span class="sxs-lookup"><span data-stu-id="6c424-103">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <persistableTypes>
      <persistableType id="String"
                       name="String">
      </persistableType>
    </persistableTypes>
  </comContract>
</comContracts>
```  
  
## <a name="type"></a><span data-ttu-id="6c424-104">类型</span><span class="sxs-lookup"><span data-stu-id="6c424-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6c424-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6c424-105">Attributes and Elements</span></span>  

 <span data-ttu-id="6c424-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c424-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6c424-107">特性</span><span class="sxs-lookup"><span data-stu-id="6c424-107">Attributes</span></span>  
  
|<span data-ttu-id="6c424-108">属性</span><span class="sxs-lookup"><span data-stu-id="6c424-108">Attribute</span></span>|<span data-ttu-id="6c424-109">说明</span><span class="sxs-lookup"><span data-stu-id="6c424-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6c424-110">id</span><span class="sxs-lookup"><span data-stu-id="6c424-110">id</span></span>|<span data-ttu-id="6c424-111">一个必需的属性，包含一个指定持久类型唯一标识符的字符串。</span><span class="sxs-lookup"><span data-stu-id="6c424-111">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="6c424-112">name</span><span class="sxs-lookup"><span data-stu-id="6c424-112">name</span></span>|<span data-ttu-id="6c424-113">一个可选属性，包含一个指定持久类型名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="6c424-113">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6c424-114">子元素</span><span class="sxs-lookup"><span data-stu-id="6c424-114">Child Elements</span></span>  

 <span data-ttu-id="6c424-115">无</span><span class="sxs-lookup"><span data-stu-id="6c424-115">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6c424-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6c424-116">Parent Elements</span></span>  
  
|<span data-ttu-id="6c424-117">元素</span><span class="sxs-lookup"><span data-stu-id="6c424-117">Element</span></span>|<span data-ttu-id="6c424-118">说明</span><span class="sxs-lookup"><span data-stu-id="6c424-118">Description</span></span>|  
|-------------|-----------------|  
|[\<persistableTypes>](persistabletypes.md)|<span data-ttu-id="6c424-119">一个 `persistableType` 元素集合。</span><span class="sxs-lookup"><span data-stu-id="6c424-119">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6c424-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c424-120">See also</span></span>

- <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>
- [\<comContracts>](comcontracts.md)
- [<span data-ttu-id="6c424-121">与 COM + 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="6c424-121">Integrating with COM+ Applications</span></span>](../../../wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="6c424-122">如何：配置 COM+ 服务设置</span><span class="sxs-lookup"><span data-stu-id="6c424-122">How to: Configure COM+ Service Settings</span></span>](../../../wcf/feature-details/how-to-configure-com-service-settings.md)
