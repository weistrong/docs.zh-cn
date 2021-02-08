---
description: 了解详细信息： <transactedBatching>
title: <transactedBatching>
ms.date: 03/30/2017
ms.assetid: 2f790a0d-8f03-4b86-81b5-ce1bc1a6c575
ms.openlocfilehash: 9a57226c3a2f2b026c69324e37b00e87fd3dd693
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773688"
---
# \<transactedBatching>

<span data-ttu-id="9f2e2-102">指定接收操作是否支持事务批处理。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-102">Specifies whether transaction batching is supported for receive operations.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transactedBatching>**  

## <a name="syntax"></a><span data-ttu-id="9f2e2-103">语法</span><span class="sxs-lookup"><span data-stu-id="9f2e2-103">Syntax</span></span>

```xml
<transactedBatching maxBatchSize="Integer" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9f2e2-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9f2e2-104">Attributes and Elements</span></span>

<span data-ttu-id="9f2e2-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="9f2e2-106">特性</span><span class="sxs-lookup"><span data-stu-id="9f2e2-106">Attributes</span></span>

|<span data-ttu-id="9f2e2-107">属性</span><span class="sxs-lookup"><span data-stu-id="9f2e2-107">Attribute</span></span>|<span data-ttu-id="9f2e2-108">说明</span><span class="sxs-lookup"><span data-stu-id="9f2e2-108">Description</span></span>|
|---------------|-----------------|
|`maxBatchSize`|<span data-ttu-id="9f2e2-109">一个整数，指定可一起成批归入到一个事务中的最大接收操作数。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-109">An integer that specifies the maximum number of receive operations that can be batched together in one transaction.</span></span> <span data-ttu-id="9f2e2-110">默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-110">The default is 0.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="9f2e2-111">子元素</span><span class="sxs-lookup"><span data-stu-id="9f2e2-111">Child Elements</span></span>

<span data-ttu-id="9f2e2-112">无。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-112">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="9f2e2-113">父元素</span><span class="sxs-lookup"><span data-stu-id="9f2e2-113">Parent Elements</span></span>

|<span data-ttu-id="9f2e2-114">元素</span><span class="sxs-lookup"><span data-stu-id="9f2e2-114">Element</span></span>|<span data-ttu-id="9f2e2-115">说明</span><span class="sxs-lookup"><span data-stu-id="9f2e2-115">Description</span></span>|
|-------------|-----------------|
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="9f2e2-116">指定终结点行为。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-116">Specifies an endpoint behavior.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9f2e2-117">备注</span><span class="sxs-lookup"><span data-stu-id="9f2e2-117">Remarks</span></span>

<span data-ttu-id="9f2e2-118">采用事务批处理配置的传输尝试将若干接收操作成批归入到一个事务中。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-118">A transport that is configured with transaction batching attempts to batch several receive operations into one transaction.</span></span> <span data-ttu-id="9f2e2-119">这样做可以避免因创建事务以及在每个接收操作中提交事务所产生的相对较高的成本。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-119">By doing so, the relatively high cost of creating a transaction and committing it in every receive operation is avoided.</span></span>

## <a name="example"></a><span data-ttu-id="9f2e2-120">示例</span><span class="sxs-lookup"><span data-stu-id="9f2e2-120">Example</span></span>

<span data-ttu-id="9f2e2-121">下面的示例演示如何将事务处理批处理行为添加到配置文件中的服务。</span><span class="sxs-lookup"><span data-stu-id="9f2e2-121">The following example shows how to add the transacted batching behavior to a service in a configuration file.</span></span>

```xml
<system.serviceModel>
  <services>
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <host>
        <baseAddresses>
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service" />
        </baseAddresses>
      </host>
      <!-- Define NetMsmqEndpoint -->
      <endpoint address="net.msmq://localhost/private/ServiceModelSamples"
                binding="netMsmqBinding"
                contract="Microsoft.ServiceModel.Samples.IQueueCalculator" />
      <!-- the mex endpoint is exposed at http://localhost:8000/ServiceModelSamples/service/mex -->
      <endpoint address="mex"
                binding="mexHttpBinding"
                contract="IMetadataExchange" />
    </service>
  </services>
  <behaviors>
    <endpointBehaviors>
      <behavior name="endpointBehavior">
        <transactedBatching maxBatchSize="10" />
      </behavior>
    </endpointBehaviors>
    <serviceBehaviors>
      <behavior name="CalculatorServiceBehavior">
        <serviceMetadata httpGetEnabled="true" />
      </behavior>
    </serviceBehaviors>
  </behaviors>
</system.serviceModel>
```

## <a name="see-also"></a><span data-ttu-id="9f2e2-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f2e2-122">See also</span></span>

- <xref:System.ServiceModel.Configuration.TransactedBatchingElement>
- <xref:System.ServiceModel.Description.TransactedBatchingBehavior>
