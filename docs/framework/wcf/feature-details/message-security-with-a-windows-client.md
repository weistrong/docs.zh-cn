---
description: 了解详细信息： Windows 客户端的消息安全性
title: Windows 客户端的消息安全
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 01e7d0b8-10f9-45c3-a4c5-53d44dc61eb8
ms.openlocfilehash: 97d415f68b4374ab2b18360347d7753f6be51313
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756092"
---
# <a name="message-security-with-a-windows-client"></a><span data-ttu-id="01122-103">Windows 客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="01122-103">Message Security with a Windows Client</span></span>

<span data-ttu-id="01122-104">此方案显示 Windows Communication Foundation (WCF) 客户端和服务器安全模式保护的服务器。</span><span class="sxs-lookup"><span data-stu-id="01122-104">This scenario shows a Windows Communication Foundation (WCF) client and server secured by message security mode.</span></span> <span data-ttu-id="01122-105">客户端和服务使用 Windows 凭据进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="01122-105">The client and service are authenticated using Windows credentials.</span></span>  
  
 <span data-ttu-id="01122-106">![Windows 客户端的消息安全性](media/1c8618d4-0005-4022-beb6-32fd087a8c3c.gif "1c8618d4-0005-4022-beb6-32fd087a8c3c")</span><span class="sxs-lookup"><span data-stu-id="01122-106">![Message security with a Windows client](media/1c8618d4-0005-4022-beb6-32fd087a8c3c.gif "1c8618d4-0005-4022-beb6-32fd087a8c3c")</span></span>  
  
|<span data-ttu-id="01122-107">特征</span><span class="sxs-lookup"><span data-stu-id="01122-107">Characteristic</span></span>|<span data-ttu-id="01122-108">说明</span><span class="sxs-lookup"><span data-stu-id="01122-108">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="01122-109">安全模式</span><span class="sxs-lookup"><span data-stu-id="01122-109">Security Mode</span></span>|<span data-ttu-id="01122-110">消息</span><span class="sxs-lookup"><span data-stu-id="01122-110">Message</span></span>|  
|<span data-ttu-id="01122-111">互操作性</span><span class="sxs-lookup"><span data-stu-id="01122-111">Interoperability</span></span>|<span data-ttu-id="01122-112">仅 WCF</span><span class="sxs-lookup"><span data-stu-id="01122-112">WCF Only</span></span>|  
|<span data-ttu-id="01122-113">身份验证（服务器）</span><span class="sxs-lookup"><span data-stu-id="01122-113">Authentication (Server)</span></span>|<span data-ttu-id="01122-114">服务器和客户端的相互身份验证</span><span class="sxs-lookup"><span data-stu-id="01122-114">Mutual authentication of the server and client</span></span>|  
|<span data-ttu-id="01122-115">身份验证（客户端）</span><span class="sxs-lookup"><span data-stu-id="01122-115">Authentication (Client)</span></span>|<span data-ttu-id="01122-116">服务器和客户端的相互身份验证</span><span class="sxs-lookup"><span data-stu-id="01122-116">Mutual authentication of the server and client</span></span>|  
|<span data-ttu-id="01122-117">完整性</span><span class="sxs-lookup"><span data-stu-id="01122-117">Integrity</span></span>|<span data-ttu-id="01122-118">是，使用共享安全上下文</span><span class="sxs-lookup"><span data-stu-id="01122-118">Yes, using shared security context</span></span>|  
|<span data-ttu-id="01122-119">机密性</span><span class="sxs-lookup"><span data-stu-id="01122-119">Confidentiality</span></span>|<span data-ttu-id="01122-120">是，使用共享安全上下文</span><span class="sxs-lookup"><span data-stu-id="01122-120">Yes, using shared security context</span></span>|  
|<span data-ttu-id="01122-121">Transport</span><span class="sxs-lookup"><span data-stu-id="01122-121">Transport</span></span>|<span data-ttu-id="01122-122">NET.TCP</span><span class="sxs-lookup"><span data-stu-id="01122-122">NET.TCP</span></span>|  
|<span data-ttu-id="01122-123">绑定</span><span class="sxs-lookup"><span data-stu-id="01122-123">Binding</span></span>|<xref:System.ServiceModel.NetTcpBinding>|  
  
## <a name="service"></a><span data-ttu-id="01122-124">服务</span><span class="sxs-lookup"><span data-stu-id="01122-124">Service</span></span>  

 <span data-ttu-id="01122-125">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="01122-125">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="01122-126">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="01122-126">Do one of the following:</span></span>  
  
- <span data-ttu-id="01122-127">使用代码（而不使用配置）创建独立服务。</span><span class="sxs-lookup"><span data-stu-id="01122-127">Create a stand-alone service using the code with no configuration.</span></span>  
  
- <span data-ttu-id="01122-128">使用提供的配置创建服务，但不定义任何终结点。</span><span class="sxs-lookup"><span data-stu-id="01122-128">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="01122-129">代码</span><span class="sxs-lookup"><span data-stu-id="01122-129">Code</span></span>  

 <span data-ttu-id="01122-130">下面的代码演示如何创建一个使用消息安全来建立 Windows 计算机安全上下文的服务终结点。</span><span class="sxs-lookup"><span data-stu-id="01122-130">The following code shows how to create a service endpoint that uses message security to establish a secure context with a Windows machine.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#11)]
 [!code-vb[C_SecurityScenarios#11](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#11)]  
  
### <a name="configuration"></a><span data-ttu-id="01122-131">Configuration</span><span class="sxs-lookup"><span data-stu-id="01122-131">Configuration</span></span>  

 <span data-ttu-id="01122-132">下面的配置可代替代码用于设置服务：</span><span class="sxs-lookup"><span data-stu-id="01122-132">The following configuration can be used instead of the code to set up the service:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <services>  
      <service behaviorConfiguration=""  
               name="ServiceModel.Calculator">  
        <endpoint address="net.tcp://localhost:8008/Calculator"  
                  binding="netTcpBinding"  
                  bindingConfiguration="Windows"  
                  name="WindowsOverMessage"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <netTcpBinding>  
        <binding name="Windows">  
          <security mode="Message">  
            <message clientCredentialType="Windows" />  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="01122-133">客户端</span><span class="sxs-lookup"><span data-stu-id="01122-133">Client</span></span>  

 <span data-ttu-id="01122-134">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="01122-134">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="01122-135">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="01122-135">Do one of the following:</span></span>  
  
- <span data-ttu-id="01122-136">使用代码（和客户端代码）创建独立客户端。</span><span class="sxs-lookup"><span data-stu-id="01122-136">Create a stand-alone client using the code (and client code).</span></span>  
  
- <span data-ttu-id="01122-137">创建不定义任何终结点地址的客户端。</span><span class="sxs-lookup"><span data-stu-id="01122-137">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="01122-138">而使用将配置名称作为自变量的客户端构造函数。</span><span class="sxs-lookup"><span data-stu-id="01122-138">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="01122-139">例如：</span><span class="sxs-lookup"><span data-stu-id="01122-139">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="01122-140">代码</span><span class="sxs-lookup"><span data-stu-id="01122-140">Code</span></span>  

 <span data-ttu-id="01122-141">下面的代码创建客户端。</span><span class="sxs-lookup"><span data-stu-id="01122-141">The following code creates a client.</span></span> <span data-ttu-id="01122-142">绑定设置为 Message 安全模式，客户端凭据类型设置为 `Windows`。</span><span class="sxs-lookup"><span data-stu-id="01122-142">The binding is to Message mode security, and the client credential type is set to `Windows`.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#18](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#18)]
 [!code-vb[C_SecurityScenarios#18](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#18)]  
  
### <a name="configuration"></a><span data-ttu-id="01122-143">Configuration</span><span class="sxs-lookup"><span data-stu-id="01122-143">Configuration</span></span>  

 <span data-ttu-id="01122-144">下面的配置用于设置客户端属性。</span><span class="sxs-lookup"><span data-stu-id="01122-144">The following configuration is used to set the client properties.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <netTcpBinding>  
        <binding name="NetTcpBinding_ICalculator" >  
         <security mode="Message">  
            <message clientCredentialType="Windows" />  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client>  
      <endpoint address="net.tcp://machineName:8008/Calculator"
                binding="netTcpBinding"  
                bindingConfiguration="NetTcpBinding_ICalculator"  
                contract="ICalculator"  
                name="NetTcpBinding_ICalculator">
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="01122-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="01122-145">See also</span></span>

- [<span data-ttu-id="01122-146">安全性概述</span><span class="sxs-lookup"><span data-stu-id="01122-146">Security Overview</span></span>](security-overview.md)
- <span data-ttu-id="01122-147">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="01122-147">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
