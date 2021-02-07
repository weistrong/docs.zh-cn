---
description: 了解更多： Intranet 不安全客户端和服务
title: 不安全的 Intranet 客户端和服务
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f450f5d4-3547-47ec-9320-2809e6a12634
ms.openlocfilehash: a03abc5b8eb0317c4d5d19347b3974d615570069
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704519"
---
# <a name="intranet-unsecured-client-and-service"></a><span data-ttu-id="ac419-103">不安全的 Intranet 客户端和服务</span><span class="sxs-lookup"><span data-stu-id="ac419-103">Intranet Unsecured Client and Service</span></span>

<span data-ttu-id="ac419-104">下图描绘了一个简单的 Windows Communication Foundation (WCF) 服务，该服务开发用于向 WCF 应用程序提供安全的专用网络的信息。</span><span class="sxs-lookup"><span data-stu-id="ac419-104">The following illustration depicts a simple Windows Communication Foundation (WCF) service developed to provide information on a secure private network to a WCF application.</span></span> <span data-ttu-id="ac419-105">安全不是必需的，因为数据重要性较低，网络本来就是安全的，或者是由 WCF 基础结构下面的层提供的。</span><span class="sxs-lookup"><span data-stu-id="ac419-105">Security is not required because the data is of low importance, the network is expected to be inherently secure, or security is provided by a layer below the WCF infrastructure.</span></span>  
  
 ![Intranet 不安全的客户端和服务方案。](./media/intranet-unsecured-client-and-service/unsecured-web-client-service.gif)  
  
|<span data-ttu-id="ac419-107">特征</span><span class="sxs-lookup"><span data-stu-id="ac419-107">Characteristic</span></span>|<span data-ttu-id="ac419-108">说明</span><span class="sxs-lookup"><span data-stu-id="ac419-108">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="ac419-109">安全模式</span><span class="sxs-lookup"><span data-stu-id="ac419-109">Security Mode</span></span>|<span data-ttu-id="ac419-110">无</span><span class="sxs-lookup"><span data-stu-id="ac419-110">None</span></span>|  
|<span data-ttu-id="ac419-111">Transport</span><span class="sxs-lookup"><span data-stu-id="ac419-111">Transport</span></span>|<span data-ttu-id="ac419-112">TCP</span><span class="sxs-lookup"><span data-stu-id="ac419-112">TCP</span></span>|  
|<span data-ttu-id="ac419-113">绑定</span><span class="sxs-lookup"><span data-stu-id="ac419-113">Binding</span></span>|<xref:System.ServiceModel.NetTcpBinding>|  
|<span data-ttu-id="ac419-114">互操作性</span><span class="sxs-lookup"><span data-stu-id="ac419-114">Interoperability</span></span>|<span data-ttu-id="ac419-115">仅 WCF</span><span class="sxs-lookup"><span data-stu-id="ac419-115">WCF only</span></span>|  
|<span data-ttu-id="ac419-116">身份验证</span><span class="sxs-lookup"><span data-stu-id="ac419-116">Authentication</span></span>|<span data-ttu-id="ac419-117">无</span><span class="sxs-lookup"><span data-stu-id="ac419-117">None</span></span>|  
|<span data-ttu-id="ac419-118">完整性</span><span class="sxs-lookup"><span data-stu-id="ac419-118">Integrity</span></span>|<span data-ttu-id="ac419-119">无</span><span class="sxs-lookup"><span data-stu-id="ac419-119">None</span></span>|  
|<span data-ttu-id="ac419-120">机密性</span><span class="sxs-lookup"><span data-stu-id="ac419-120">Confidentiality</span></span>|<span data-ttu-id="ac419-121">无</span><span class="sxs-lookup"><span data-stu-id="ac419-121">None</span></span>|  
  
## <a name="service"></a><span data-ttu-id="ac419-122">服务</span><span class="sxs-lookup"><span data-stu-id="ac419-122">Service</span></span>  

 <span data-ttu-id="ac419-123">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="ac419-123">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="ac419-124">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="ac419-124">Do one of the following:</span></span>  
  
- <span data-ttu-id="ac419-125">使用代码（而不使用配置）创建独立服务。</span><span class="sxs-lookup"><span data-stu-id="ac419-125">Create a stand-alone service using the code with no configuration.</span></span>  
  
- <span data-ttu-id="ac419-126">使用提供的配置创建服务，但不定义任何终结点。</span><span class="sxs-lookup"><span data-stu-id="ac419-126">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="ac419-127">代码</span><span class="sxs-lookup"><span data-stu-id="ac419-127">Code</span></span>  

 <span data-ttu-id="ac419-128">下面的代码演示如何创建不安全的终结点：</span><span class="sxs-lookup"><span data-stu-id="ac419-128">The following code shows how to create an endpoint with no security:</span></span>  
  
 [!code-csharp[C_UnsecuredService#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_unsecuredservice/cs/source.cs#2)]
 [!code-vb[C_UnsecuredService#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_unsecuredservice/vb/source.vb#2)]  
  
### <a name="configuration"></a><span data-ttu-id="ac419-129">Configuration</span><span class="sxs-lookup"><span data-stu-id="ac419-129">Configuration</span></span>  

 <span data-ttu-id="ac419-130">下面的代码使用配置设置相同的终结点：</span><span class="sxs-lookup"><span data-stu-id="ac419-130">The following code sets up the same endpoint using configuration:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors />  
    <services>  
      <service behaviorConfiguration=""
               name="ServiceModel.Calculator">  
        <endpoint address="net.tcp://localhost:8008/Calculator"
                  binding="netTcpBinding"  
                  bindingConfiguration="tcp_Unsecured"
                  name="netTcp_ICalculator"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <netTcpBinding>  
        <binding name="tcp_Unsecured">  
          <security mode="None" />  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="ac419-131">客户端</span><span class="sxs-lookup"><span data-stu-id="ac419-131">Client</span></span>  

 <span data-ttu-id="ac419-132">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="ac419-132">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="ac419-133">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="ac419-133">Do one of the following:</span></span>  
  
- <span data-ttu-id="ac419-134">使用代码（和客户端代码）创建独立客户端。</span><span class="sxs-lookup"><span data-stu-id="ac419-134">Create a stand-alone client using the code (and client code).</span></span>  
  
- <span data-ttu-id="ac419-135">创建不定义任何终结点地址的客户端。</span><span class="sxs-lookup"><span data-stu-id="ac419-135">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="ac419-136">而使用将配置名称作为自变量的客户端构造函数。</span><span class="sxs-lookup"><span data-stu-id="ac419-136">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="ac419-137">例如：</span><span class="sxs-lookup"><span data-stu-id="ac419-137">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="ac419-138">代码</span><span class="sxs-lookup"><span data-stu-id="ac419-138">Code</span></span>  

 <span data-ttu-id="ac419-139">下面的代码演示一个基本 WCF 客户端，它使用 TCP 协议访问不安全的终结点。</span><span class="sxs-lookup"><span data-stu-id="ac419-139">The following code shows a basic WCF client that accesses an unsecured endpoint using the TCP protocol.</span></span>  
  
 [!code-csharp[C_UnsecuredClient#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_unsecuredclient/cs/source.cs#2)]
 [!code-vb[C_UnsecuredClient#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_unsecuredclient/vb/source.vb#2)]  
  
### <a name="configuration"></a><span data-ttu-id="ac419-140">Configuration</span><span class="sxs-lookup"><span data-stu-id="ac419-140">Configuration</span></span>  

 <span data-ttu-id="ac419-141">下面的配置代码应用于客户端：</span><span class="sxs-lookup"><span data-stu-id="ac419-141">The following configuration code applies to the client:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <netTcpBinding>  
        <binding name="NetTcpBinding_ICalculator" >  
          <security mode="None">  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client>  
      <endpoint address="net.tcp://machineName:8008/Calculator "  
                binding="netTcpBinding"
                bindingConfiguration="NetTcpBinding_ICalculator"  
                contract="ICalculator"
                name="NetTcpBinding_ICalculator" />  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ac419-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac419-142">See also</span></span>

- <xref:System.ServiceModel.NetTcpBinding>
- [<span data-ttu-id="ac419-143">安全性概述</span><span class="sxs-lookup"><span data-stu-id="ac419-143">Security Overview</span></span>](security-overview.md)
- <span data-ttu-id="ac419-144">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="ac419-144">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
