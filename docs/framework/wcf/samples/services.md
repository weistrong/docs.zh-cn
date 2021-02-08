---
description: 了解详细信息：服务
title: 服务示例
ms.date: 03/30/2017
ms.assetid: 462a2218-f8c6-4fb7-95bc-64765459c429
ms.openlocfilehash: 706d42a022a53d8f270b791df78b9b534d0cb2c2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793033"
---
# <a name="services"></a><span data-ttu-id="37ac8-103">服务</span><span class="sxs-lookup"><span data-stu-id="37ac8-103">Services</span></span>

<span data-ttu-id="37ac8-104">本节包含演示 Windows Communication Foundation (WCF) 服务的示例。</span><span class="sxs-lookup"><span data-stu-id="37ac8-104">This section contains samples that demonstrate Windows Communication Foundation (WCF) services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37ac8-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="37ac8-105">In this section</span></span>

- <span data-ttu-id="37ac8-106">[提供](../feature-details/hosting.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-106">[Hosting](../feature-details/hosting.md)</span></span>\
<span data-ttu-id="37ac8-107">演示如何承载 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="37ac8-107">Demonstrates hosting WCF services.</span></span>

- <span data-ttu-id="37ac8-108">[服务互操作性](service-interoperability.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-108">[Service Interoperability](service-interoperability.md)</span></span>\
<span data-ttu-id="37ac8-109">说明 WCF 与其他服务技术之间的交互。</span><span class="sxs-lookup"><span data-stu-id="37ac8-109">Demonstrates interaction between WCF and other service technologies.</span></span>

- <span data-ttu-id="37ac8-110">[行为](behaviors.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-110">[Behaviors](behaviors.md)</span></span>\
<span data-ttu-id="37ac8-111">演示 WCF 服务行为。</span><span class="sxs-lookup"><span data-stu-id="37ac8-111">Demonstrates WCF service behaviors.</span></span>

- <span data-ttu-id="37ac8-112">[服务安全](service-security.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-112">[Service Security](service-security.md)</span></span>\
<span data-ttu-id="37ac8-113">说明 WCF 服务安全性。</span><span class="sxs-lookup"><span data-stu-id="37ac8-113">Demonstrates WCF service security.</span></span>

- <span data-ttu-id="37ac8-114">[WCF 服务的简化配置](simplified-configuration-for-wcf-services.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-114">[Simplified Configuration for WCF Services](simplified-configuration-for-wcf-services.md)</span></span>\
<span data-ttu-id="37ac8-115">演示如何使用 WCF 实现和配置典型的服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="37ac8-115">Demonstrates how to implement and configure a typical service and client using WCF.</span></span>

- <span data-ttu-id="37ac8-116">[标准终结点的用法](usage-of-standard-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-116">[Usage of Standard Endpoints](usage-of-standard-endpoints.md)</span></span>\
<span data-ttu-id="37ac8-117">演示如何在服务配置文件中使用标准终结点。</span><span class="sxs-lookup"><span data-stu-id="37ac8-117">Demonstrates how to use standard endpoints in service configuration files.</span></span>

- <span data-ttu-id="37ac8-118">[扩展保护策略](extended-protection-policy.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-118">[Extended Protection Policy](extended-protection-policy.md)</span></span>\
<span data-ttu-id="37ac8-119">演示扩展保护，这是一种针对中间人 (MITM) 攻击而提供保护的安全计划。</span><span class="sxs-lookup"><span data-stu-id="37ac8-119">Demonstrates Extended Protection, a security initiative for protecting against man-in-the-middle (MITM) attacks.</span></span>

- <span data-ttu-id="37ac8-120">[配置通道工厂](configuration-channel-factory.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-120">[Configuration Channel Factory](configuration-channel-factory.md)</span></span>\
<span data-ttu-id="37ac8-121">演示 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> 的用法。</span><span class="sxs-lookup"><span data-stu-id="37ac8-121">Demonstrates the usage of the <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601>.</span></span>

- <span data-ttu-id="37ac8-122">[寻址](addressing.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-122">[Addressing](addressing.md)</span></span>\
<span data-ttu-id="37ac8-123">演示终结点地址的各个方面和功能。</span><span class="sxs-lookup"><span data-stu-id="37ac8-123">Demonstrates various aspects and features of endpoint addresses.</span></span>

- <span data-ttu-id="37ac8-124">[命令性](imperative.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-124">[Imperative](imperative.md)</span></span>\
<span data-ttu-id="37ac8-125">演示如何使用代码为服务定义 <xref:System.ServiceModel.WSHttpBinding>，而不是在配置中定义 `wsHttpBinding` 绑定。</span><span class="sxs-lookup"><span data-stu-id="37ac8-125">Demonstrates how to define a <xref:System.ServiceModel.WSHttpBinding> for a service using code, instead of defining the `wsHttpBinding` binding in configuration.</span></span>

- <span data-ttu-id="37ac8-126">[多个协定](multiple-contracts.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-126">[Multiple Contracts](multiple-contracts.md)</span></span>\
<span data-ttu-id="37ac8-127">演示如何在一个服务上实现多个协定和如何配置终结点以便与每个实现的协定通信。</span><span class="sxs-lookup"><span data-stu-id="37ac8-127">Demonstrates how to implement more than one contract on a service and how to configure endpoints for communicating with each of the implemented contracts.</span></span>

- <span data-ttu-id="37ac8-128">[多个终结点](multiple-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-128">[Multiple Endpoints](multiple-endpoints.md)</span></span>\
<span data-ttu-id="37ac8-129">演示如何在一个服务上配置多个终结点，以及如何从客户端与每个终结点通信。</span><span class="sxs-lookup"><span data-stu-id="37ac8-129">Demonstrates how to configure multiple endpoints on a service and how to communicate with each endpoint from a client.</span></span>

- <span data-ttu-id="37ac8-130">[单个 ListenUri 上的多个终结点](multiple-endpoints-at-a-single-listenuri.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-130">[Multiple Endpoints at a Single ListenUri](multiple-endpoints-at-a-single-listenuri.md)</span></span>\
<span data-ttu-id="37ac8-131">演示一个在单个 `ListenUri` 中承载多个终结点的服务。</span><span class="sxs-lookup"><span data-stu-id="37ac8-131">Demonstrates a service that hosts multiple endpoints at a single `ListenUri`.</span></span>

- <span data-ttu-id="37ac8-132">[OperationContextScope](operationcontextscope.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-132">[OperationContextScope](operationcontextscope.md)</span></span>\
<span data-ttu-id="37ac8-133">演示如何使用标头在 WCF 调用上发送额外的信息。</span><span class="sxs-lookup"><span data-stu-id="37ac8-133">Demonstrates how to send extra information on a WCF call using headers.</span></span>

- <span data-ttu-id="37ac8-134">[服务说明](service-description.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-134">[Service Description](service-description.md)</span></span>\
<span data-ttu-id="37ac8-135">演示服务如何在运行时检索其服务说明信息。</span><span class="sxs-lookup"><span data-stu-id="37ac8-135">Demonstrates how a service can retrieve its service description information at runtime.</span></span>

- <span data-ttu-id="37ac8-136">[ConcurrencyMode](concurrencymode-reentrant.md)</span><span class="sxs-lookup"><span data-stu-id="37ac8-136">[ConcurrencyMode.Reentrant](concurrencymode-reentrant.md)</span></span>\
<span data-ttu-id="37ac8-137">演示如何在服务实现上使用可重入并发模式。</span><span class="sxs-lookup"><span data-stu-id="37ac8-137">Demonstrates how to use the Reentrant concurrency mode on a service implementation.</span></span>
