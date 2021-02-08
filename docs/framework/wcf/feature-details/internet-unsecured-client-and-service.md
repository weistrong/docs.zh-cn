---
description: 了解更多相关信息： Internet 不安全的客户端和服务
title: 不安全的 Internet 客户端和服务
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 97a10d79-3e7d-4bd1-9a99-fd9807fd70bc
ms.openlocfilehash: 8b402b276c80b2e1c148de0837d8644aad7a2d4a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802770"
---
# <a name="internet-unsecured-client-and-service"></a><span data-ttu-id="64f3e-103">不安全的 Internet 客户端和服务</span><span class="sxs-lookup"><span data-stu-id="64f3e-103">Internet Unsecured Client and Service</span></span>

<span data-ttu-id="64f3e-104">下图显示了一个公共的、不安全的 Windows Communication Foundation (WCF) 客户端和服务的示例：</span><span class="sxs-lookup"><span data-stu-id="64f3e-104">The following illustration shows an example of a public, unsecured Windows Communication Foundation (WCF) client and service:</span></span>  
  
 ![显示不安全的 Internet 方案的屏幕截图](./media/internet-unsecured-client-and-service/public-unsecured-internet.gif)  
  
|<span data-ttu-id="64f3e-106">特征</span><span class="sxs-lookup"><span data-stu-id="64f3e-106">Characteristic</span></span>|<span data-ttu-id="64f3e-107">说明</span><span class="sxs-lookup"><span data-stu-id="64f3e-107">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="64f3e-108">安全模式</span><span class="sxs-lookup"><span data-stu-id="64f3e-108">Security Mode</span></span>|<span data-ttu-id="64f3e-109">无</span><span class="sxs-lookup"><span data-stu-id="64f3e-109">None</span></span>|  
|<span data-ttu-id="64f3e-110">Transport</span><span class="sxs-lookup"><span data-stu-id="64f3e-110">Transport</span></span>|<span data-ttu-id="64f3e-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="64f3e-111">HTTP</span></span>|  
|<span data-ttu-id="64f3e-112">绑定</span><span class="sxs-lookup"><span data-stu-id="64f3e-112">Binding</span></span>|<span data-ttu-id="64f3e-113"><xref:System.ServiceModel.BasicHttpBinding> 在代码中，或 [\<basicHttpBinding>](../../configure-apps/file-schema/wcf/basichttpbinding.md) 配置中的元素。</span><span class="sxs-lookup"><span data-stu-id="64f3e-113"><xref:System.ServiceModel.BasicHttpBinding> in code, or the [\<basicHttpBinding>](../../configure-apps/file-schema/wcf/basichttpbinding.md) element in configuration.</span></span>|  
|<span data-ttu-id="64f3e-114">互操作性</span><span class="sxs-lookup"><span data-stu-id="64f3e-114">Interoperability</span></span>|<span data-ttu-id="64f3e-115">与现有的 Web 服务客户端和服务进行互操作</span><span class="sxs-lookup"><span data-stu-id="64f3e-115">With existing Web service clients and services</span></span>|  
|<span data-ttu-id="64f3e-116">身份验证</span><span class="sxs-lookup"><span data-stu-id="64f3e-116">Authentication</span></span>|<span data-ttu-id="64f3e-117">无</span><span class="sxs-lookup"><span data-stu-id="64f3e-117">None</span></span>|  
|<span data-ttu-id="64f3e-118">完整性</span><span class="sxs-lookup"><span data-stu-id="64f3e-118">Integrity</span></span>|<span data-ttu-id="64f3e-119">无</span><span class="sxs-lookup"><span data-stu-id="64f3e-119">None</span></span>|  
|<span data-ttu-id="64f3e-120">机密性</span><span class="sxs-lookup"><span data-stu-id="64f3e-120">Confidentiality</span></span>|<span data-ttu-id="64f3e-121">无</span><span class="sxs-lookup"><span data-stu-id="64f3e-121">None</span></span>|  
  
## <a name="service"></a><span data-ttu-id="64f3e-122">服务</span><span class="sxs-lookup"><span data-stu-id="64f3e-122">Service</span></span>  

 <span data-ttu-id="64f3e-123">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="64f3e-123">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="64f3e-124">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="64f3e-124">Do one of the following:</span></span>  
  
- <span data-ttu-id="64f3e-125">使用代码（而不使用配置）创建独立服务。</span><span class="sxs-lookup"><span data-stu-id="64f3e-125">Create a stand-alone service using the code with no configuration.</span></span>  
  
- <span data-ttu-id="64f3e-126">使用提供的配置创建服务，但不定义任何终结点。</span><span class="sxs-lookup"><span data-stu-id="64f3e-126">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="64f3e-127">代码</span><span class="sxs-lookup"><span data-stu-id="64f3e-127">Code</span></span>  

 <span data-ttu-id="64f3e-128">下面的代码演示如何创建不安全的终结点。</span><span class="sxs-lookup"><span data-stu-id="64f3e-128">The following code shows how to create an endpoint with no security.</span></span> <span data-ttu-id="64f3e-129">默认情况下，<xref:System.ServiceModel.BasicHttpBinding> 将安全模式设置为 <xref:System.ServiceModel.BasicHttpSecurityMode.None>。</span><span class="sxs-lookup"><span data-stu-id="64f3e-129">By default, the <xref:System.ServiceModel.BasicHttpBinding> has the security mode set to <xref:System.ServiceModel.BasicHttpSecurityMode.None>.</span></span>  
  
 [!code-csharp[C_UnsecuredService#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_unsecuredservice/cs/source.cs#1)]
 [!code-vb[C_UnsecuredService#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_unsecuredservice/vb/source.vb#1)]  
  
### <a name="service-configuration"></a><span data-ttu-id="64f3e-130">服务配置</span><span class="sxs-lookup"><span data-stu-id="64f3e-130">Service Configuration</span></span>  

 <span data-ttu-id="64f3e-131">下面的代码使用配置设置相同的终结点。</span><span class="sxs-lookup"><span data-stu-id="64f3e-131">The following code sets up the same endpoint using configuration.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors />  
    <services>  
      <service behaviorConfiguration="" name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"
                  binding="basicHttpBinding"  
                  bindingConfiguration="Basic_Unsecured"
                  name="BasicHttp_ICalculator"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <basicHttpBinding>  
        <binding name="Basic_Unsecured" />  
      </basicHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="64f3e-132">客户端</span><span class="sxs-lookup"><span data-stu-id="64f3e-132">Client</span></span>  

 <span data-ttu-id="64f3e-133">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="64f3e-133">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="64f3e-134">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="64f3e-134">Do one of the following:</span></span>  
  
- <span data-ttu-id="64f3e-135">使用代码（和客户端代码）创建独立客户端。</span><span class="sxs-lookup"><span data-stu-id="64f3e-135">Create a stand-alone client using the code (and client code).</span></span>  
  
- <span data-ttu-id="64f3e-136">创建不定义任何终结点地址的客户端。</span><span class="sxs-lookup"><span data-stu-id="64f3e-136">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="64f3e-137">而使用将配置名称作为自变量的客户端构造函数。</span><span class="sxs-lookup"><span data-stu-id="64f3e-137">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="64f3e-138">例如：</span><span class="sxs-lookup"><span data-stu-id="64f3e-138">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="64f3e-139">代码</span><span class="sxs-lookup"><span data-stu-id="64f3e-139">Code</span></span>  

 <span data-ttu-id="64f3e-140">下面的代码演示了访问不安全终结点的基本 WCF 客户端。</span><span class="sxs-lookup"><span data-stu-id="64f3e-140">The following code shows a basic WCF client that accesses an unsecured endpoint.</span></span>  
  
 [!code-csharp[C_UnsecuredClient#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_unsecuredclient/cs/source.cs#1)]
 [!code-vb[C_UnsecuredClient#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_unsecuredclient/vb/source.vb#1)]  
  
### <a name="client-configuration"></a><span data-ttu-id="64f3e-141">客户端配置</span><span class="sxs-lookup"><span data-stu-id="64f3e-141">Client Configuration</span></span>  

 <span data-ttu-id="64f3e-142">下面的代码将配置客户端。</span><span class="sxs-lookup"><span data-stu-id="64f3e-142">The following code configures the client.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <basicHttpBinding>  
        <binding name="BasicHttpBinding_ICalculator" >  
          <security mode="None">  
          </security>  
        </binding>  
      </basicHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://localhost/Calculator/Unsecured"  
          binding="basicHttpBinding"
          bindingConfiguration="BasicHttpBinding_ICalculator"  
          contract="ICalculator"
          name="BasicHttpBinding_ICalculator" />  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="64f3e-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="64f3e-143">See also</span></span>

- [<span data-ttu-id="64f3e-144">常用安全方案</span><span class="sxs-lookup"><span data-stu-id="64f3e-144">Common Security Scenarios</span></span>](common-security-scenarios.md)
- [<span data-ttu-id="64f3e-145">安全性概述</span><span class="sxs-lookup"><span data-stu-id="64f3e-145">Security Overview</span></span>](security-overview.md)
- <span data-ttu-id="64f3e-146">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="64f3e-146">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
