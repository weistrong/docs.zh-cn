---
description: 了解详细信息： <transactionFlow>
title: <transactionFlow>
ms.date: 03/30/2017
ms.assetid: 8c7b4c5b-ace3-4fe3-89ff-7b13c9aacd13
ms.openlocfilehash: 8a853beaec1837606ecb96156b8ec9381fa3e07a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773545"
---
# \<transactionFlow>

<span data-ttu-id="a0316-102">指定自定义绑定的事务流支持。</span><span class="sxs-lookup"><span data-stu-id="a0316-102">Specifies transaction flow support for the custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transactionFlow>**  
  
## <a name="syntax"></a><span data-ttu-id="a0316-103">语法</span><span class="sxs-lookup"><span data-stu-id="a0316-103">Syntax</span></span>  
  
```xml  
<transactionFlow transactionProtocol="OleTransactions/WSAtomicTransactionOctober2004" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a0316-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a0316-104">Attributes and Elements</span></span>  

 <span data-ttu-id="a0316-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0316-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a0316-106">特性</span><span class="sxs-lookup"><span data-stu-id="a0316-106">Attributes</span></span>  
  
|<span data-ttu-id="a0316-107">属性</span><span class="sxs-lookup"><span data-stu-id="a0316-107">Attribute</span></span>|<span data-ttu-id="a0316-108">说明</span><span class="sxs-lookup"><span data-stu-id="a0316-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a0316-109">transactionProtocol</span><span class="sxs-lookup"><span data-stu-id="a0316-109">transactionProtocol</span></span>|<span data-ttu-id="a0316-110">指定要使用的事务处理协议。</span><span class="sxs-lookup"><span data-stu-id="a0316-110">Specifies the transaction protocol to be used.</span></span> <span data-ttu-id="a0316-111">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="a0316-111">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a0316-112">-OleTransactions</span><span class="sxs-lookup"><span data-stu-id="a0316-112">-   OleTransactions</span></span><br /><span data-ttu-id="a0316-113">-WSAtomicTransactionOctober2004</span><span class="sxs-lookup"><span data-stu-id="a0316-113">-   WSAtomicTransactionOctober2004</span></span><br /><br /> <span data-ttu-id="a0316-114">默认值为 OleTransactions。</span><span class="sxs-lookup"><span data-stu-id="a0316-114">The default is OleTransactions.</span></span><br /><br /> <span data-ttu-id="a0316-115">此属性的类型为 <xref:System.ServiceModel.TransactionProtocol>。</span><span class="sxs-lookup"><span data-stu-id="a0316-115">This attribute is of type <xref:System.ServiceModel.TransactionProtocol>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a0316-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a0316-116">Child Elements</span></span>  

 <span data-ttu-id="a0316-117">无。</span><span class="sxs-lookup"><span data-stu-id="a0316-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a0316-118">父元素</span><span class="sxs-lookup"><span data-stu-id="a0316-118">Parent Elements</span></span>  
  
|<span data-ttu-id="a0316-119">元素</span><span class="sxs-lookup"><span data-stu-id="a0316-119">Element</span></span>|<span data-ttu-id="a0316-120">说明</span><span class="sxs-lookup"><span data-stu-id="a0316-120">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="a0316-121">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="a0316-121">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a0316-122">备注</span><span class="sxs-lookup"><span data-stu-id="a0316-122">Remarks</span></span>  

 <span data-ttu-id="a0316-123">此元素允许你在终结点绑定设置中启用或禁用传入事务流，并允许指定传入事务所需的协议格式。</span><span class="sxs-lookup"><span data-stu-id="a0316-123">This element allows you to enable or disable incoming transaction flow in an endpoint’s binding settings, as well as to specify the desired protocol format for incoming transactions.</span></span> <span data-ttu-id="a0316-124">有关使用此配置元素的详细信息，请参阅配置 [配置](../../../wcf/feature-details/servicemodel-transaction-configuration.md) 和 [启用事务流](../../../wcf/feature-details/enabling-transaction-flow.md)。</span><span class="sxs-lookup"><span data-stu-id="a0316-124">For more information on using this configuration element, see [ServiceModel Transaction Configuration](../../../wcf/feature-details/servicemodel-transaction-configuration.md) and [Enabling Transaction Flow](../../../wcf/feature-details/enabling-transaction-flow.md).</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="a0316-125">使用 `OleTransactions` 协议在终结点之间对事务进行流处理时，如果目标终结点尝试使用任何 `OleTransactions` 之外的协议进行流处理，则可能丢失事务超时。</span><span class="sxs-lookup"><span data-stu-id="a0316-125">When using the `OleTransactions` protocol to flow transactions from endpoint to endpoint, the transaction timeout can be lost if the destination endpoint attempts to flow again using any protocol other than `OleTransactions`.</span></span> <span data-ttu-id="a0316-126">这可能导致 OleTransactions 跃点后面的所有下级节点的超时时间比预期延迟。</span><span class="sxs-lookup"><span data-stu-id="a0316-126">This can cause all down-level nodes after the OleTransactions hop to timeout later than expected.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0316-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0316-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.TransactionFlowElement>
- <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="a0316-128">ServiceModel 事务配置</span><span class="sxs-lookup"><span data-stu-id="a0316-128">ServiceModel Transaction Configuration</span></span>](../../../wcf/feature-details/servicemodel-transaction-configuration.md)
- [<span data-ttu-id="a0316-129">启用事务流</span><span class="sxs-lookup"><span data-stu-id="a0316-129">Enabling Transaction Flow</span></span>](../../../wcf/feature-details/enabling-transaction-flow.md)
- [<span data-ttu-id="a0316-130">绑定</span><span class="sxs-lookup"><span data-stu-id="a0316-130">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="a0316-131">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="a0316-131">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="a0316-132">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="a0316-132">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
