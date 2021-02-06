---
description: 了解详细信息： <client>
title: <client>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.ServiceModel/client
- http://schemas.microsoft.com/.NetConfiguration/v2.0#client
ms.assetid: bf0f7031-76c8-4e7e-a6c6-9ad9119134be
ms.openlocfilehash: 9765460602738f49963ea521b3f00ed7c63cc568
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638855"
---
# \<client>

<span data-ttu-id="f32d4-102">`client` 元素定义客户端可以连接的终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="f32d4-102">The `client` element defines a list of endpoints that a client can connect to.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<client>**

## <a name="syntax"></a><span data-ttu-id="f32d4-103">语法</span><span class="sxs-lookup"><span data-stu-id="f32d4-103">Syntax</span></span>

```xml
<system.serviceModel>
  <client>
    <endpoint>
    </endpoint>
    <metadata>
    </metadata>
  </client>
</system.serviceModel>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f32d4-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f32d4-104">Attributes and Elements</span></span>

 <span data-ttu-id="f32d4-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f32d4-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="f32d4-106">特性</span><span class="sxs-lookup"><span data-stu-id="f32d4-106">Attributes</span></span>

 <span data-ttu-id="f32d4-107">无</span><span class="sxs-lookup"><span data-stu-id="f32d4-107">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="f32d4-108">子元素</span><span class="sxs-lookup"><span data-stu-id="f32d4-108">Child Elements</span></span>

|<span data-ttu-id="f32d4-109">元素</span><span class="sxs-lookup"><span data-stu-id="f32d4-109">Element</span></span>|<span data-ttu-id="f32d4-110">说明</span><span class="sxs-lookup"><span data-stu-id="f32d4-110">Description</span></span>|
|-------------|-----------------|
|[\<endpoint>](endpoint-of-client.md)|<span data-ttu-id="f32d4-111">包含终结点元素的集合，这些元素指定此客户端可以连接到的终结点。</span><span class="sxs-lookup"><span data-stu-id="f32d4-111">Contains a collection of endpoint elements that specify the endpoints that this client can connect to.</span></span>|
|[\<metadata>](metadata.md)|<span data-ttu-id="f32d4-112">包含用于处理元数据的设置。</span><span class="sxs-lookup"><span data-stu-id="f32d4-112">Contains settings for processing metadata.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="f32d4-113">父元素</span><span class="sxs-lookup"><span data-stu-id="f32d4-113">Parent Elements</span></span>

|<span data-ttu-id="f32d4-114">元素</span><span class="sxs-lookup"><span data-stu-id="f32d4-114">Element</span></span>|<span data-ttu-id="f32d4-115">说明</span><span class="sxs-lookup"><span data-stu-id="f32d4-115">Description</span></span>|
|-------------|-----------------|
|[\<system.serviceModel>](system-servicemodel.md)|<span data-ttu-id="f32d4-116">所有 Windows Communication Foundation (WCF) 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="f32d4-116">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f32d4-117">备注</span><span class="sxs-lookup"><span data-stu-id="f32d4-117">Remarks</span></span>

 <span data-ttu-id="f32d4-118">`client` 节定义客户端可以连接的终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="f32d4-118">The `client` section defines a list of endpoints that a client can connect to.</span></span> <span data-ttu-id="f32d4-119">客户端节中列出的每个终结点都定义了它自己的绑定、行为和协定。</span><span class="sxs-lookup"><span data-stu-id="f32d4-119">Each endpoint listed in the client section defines its own binding, behavior, and contract.</span></span> <span data-ttu-id="f32d4-120">它由 `name` 和 `contract` 属性共同进行唯一标识。</span><span class="sxs-lookup"><span data-stu-id="f32d4-120">It is uniquely identified by the combination of the `name` and `contract` attributes.</span></span> <span data-ttu-id="f32d4-121">客户端代码指定要连接到该客户端实现的服务终结点的 `name`。</span><span class="sxs-lookup"><span data-stu-id="f32d4-121">The client code specifies the `name` to connect to an endpoint for the service that the client implements.</span></span> <span data-ttu-id="f32d4-122">如果省略 `name` 属性，则该终结点将作为其实现的协定的默认终结点。</span><span class="sxs-lookup"><span data-stu-id="f32d4-122">If the `name` attribute is omitted, the endpoint acts as the default endpoint for the contract it implements.</span></span>

 <span data-ttu-id="f32d4-123">此外，本节还指定了用于处理元数据的设置。</span><span class="sxs-lookup"><span data-stu-id="f32d4-123">In addition, this section also specifies settings for processing metadata.</span></span>

## <a name="example"></a><span data-ttu-id="f32d4-124">示例</span><span class="sxs-lookup"><span data-stu-id="f32d4-124">Example</span></span>

```xml
<client>
  <endpoint address="/HelloWorld/"
            bindingConfiguration="usingDefaults"
            name="MyBinding"
            binding="customBinding"
            contract="HelloWorld">
    <addressProperties actingAs="http://www.microsoft.com/TestActor"
                       identityData="BasicReadWrite"
                       identityType="Spn"
                       isAddressPrivate="false">
  </endpoint>
</client>
```

## <a name="see-also"></a><span data-ttu-id="f32d4-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="f32d4-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientSection>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- [<span data-ttu-id="f32d4-126">WCF 客户端配置</span><span class="sxs-lookup"><span data-stu-id="f32d4-126">WCF Client Configuration</span></span>](../../../wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="f32d4-127">客户端</span><span class="sxs-lookup"><span data-stu-id="f32d4-127">Clients</span></span>](../../../wcf/feature-details/clients.md)
