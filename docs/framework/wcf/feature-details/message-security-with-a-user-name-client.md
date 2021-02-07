---
description: 了解详细信息：使用用户名客户端的消息安全性
title: 用户名客户端的消息安全
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 36335cb9-76b8-4443-92c7-44f081eabb21
ms.openlocfilehash: 4502635df3b52ba069c19fca7a73cc9395dd105d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756105"
---
# <a name="message-security-with-a-user-name-client"></a><span data-ttu-id="d3cbf-103">用户名客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="d3cbf-103">Message Security with a User Name Client</span></span>

<span data-ttu-id="d3cbf-104">下图显示了使用消息级安全性来保护 Windows Communication Foundation (WCF) 服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-104">The following illustration shows an Windows Communication Foundation (WCF) service and client secured using message-level security.</span></span> <span data-ttu-id="d3cbf-105">服务使用 X.509 证书进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-105">The service is authenticated with an X.509 certificate.</span></span> <span data-ttu-id="d3cbf-106">客户端使用用户名和密码进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-106">The client authenticates using a user name and password.</span></span>  
  
 <span data-ttu-id="d3cbf-107">有关示例应用程序，请参阅 [消息安全用户名](../samples/message-security-user-name.md)。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-107">For a sample application, see [Message Security User Name](../samples/message-security-user-name.md).</span></span>  
  
 <span data-ttu-id="d3cbf-108">![使用用户名身份验证的消息安全](media/1fb10a61-7e1d-42f5-b1af-195bfee5b3c6.gif "1fb10a61-7e1d-42f5-b1af-195bfee5b3c6")</span><span class="sxs-lookup"><span data-stu-id="d3cbf-108">![Message security using username authentication](media/1fb10a61-7e1d-42f5-b1af-195bfee5b3c6.gif "1fb10a61-7e1d-42f5-b1af-195bfee5b3c6")</span></span>  
  
|<span data-ttu-id="d3cbf-109">特征</span><span class="sxs-lookup"><span data-stu-id="d3cbf-109">Characteristic</span></span>|<span data-ttu-id="d3cbf-110">说明</span><span class="sxs-lookup"><span data-stu-id="d3cbf-110">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="d3cbf-111">安全模式</span><span class="sxs-lookup"><span data-stu-id="d3cbf-111">Security Mode</span></span>|<span data-ttu-id="d3cbf-112">消息</span><span class="sxs-lookup"><span data-stu-id="d3cbf-112">Message</span></span>|  
|<span data-ttu-id="d3cbf-113">互操作性</span><span class="sxs-lookup"><span data-stu-id="d3cbf-113">Interoperability</span></span>|<span data-ttu-id="d3cbf-114">仅 Windows Communication Foundation (WCF) </span><span class="sxs-lookup"><span data-stu-id="d3cbf-114">Windows Communication Foundation (WCF) only</span></span>|  
|<span data-ttu-id="d3cbf-115">身份验证（服务器）</span><span class="sxs-lookup"><span data-stu-id="d3cbf-115">Authentication (Server)</span></span>|<span data-ttu-id="d3cbf-116">初始协商需要服务器身份验证</span><span class="sxs-lookup"><span data-stu-id="d3cbf-116">Initial negotiation requires server authentication</span></span>|  
|<span data-ttu-id="d3cbf-117">身份验证（客户端）</span><span class="sxs-lookup"><span data-stu-id="d3cbf-117">Authentication (Client)</span></span>|<span data-ttu-id="d3cbf-118">用户名/密码</span><span class="sxs-lookup"><span data-stu-id="d3cbf-118">User name/password</span></span>|  
|<span data-ttu-id="d3cbf-119">完整性</span><span class="sxs-lookup"><span data-stu-id="d3cbf-119">Integrity</span></span>|<span data-ttu-id="d3cbf-120">是，使用共享安全上下文</span><span class="sxs-lookup"><span data-stu-id="d3cbf-120">Yes, using shared security context</span></span>|  
|<span data-ttu-id="d3cbf-121">机密性</span><span class="sxs-lookup"><span data-stu-id="d3cbf-121">Confidentiality</span></span>|<span data-ttu-id="d3cbf-122">是，使用共享安全上下文</span><span class="sxs-lookup"><span data-stu-id="d3cbf-122">Yes, using shared security context</span></span>|  
|<span data-ttu-id="d3cbf-123">Transport</span><span class="sxs-lookup"><span data-stu-id="d3cbf-123">Transport</span></span>|<span data-ttu-id="d3cbf-124">HTTP</span><span class="sxs-lookup"><span data-stu-id="d3cbf-124">HTTP</span></span>|  
|<span data-ttu-id="d3cbf-125">绑定</span><span class="sxs-lookup"><span data-stu-id="d3cbf-125">Binding</span></span>|<xref:System.ServiceModel.WSHttpBinding>|  
  
## <a name="service"></a><span data-ttu-id="d3cbf-126">服务</span><span class="sxs-lookup"><span data-stu-id="d3cbf-126">Service</span></span>  

 <span data-ttu-id="d3cbf-127">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-127">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="d3cbf-128">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="d3cbf-128">Do one of the following:</span></span>  
  
- <span data-ttu-id="d3cbf-129">使用代码（而不使用配置）创建独立服务。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-129">Create a stand-alone service using the code with no configuration.</span></span>  
  
- <span data-ttu-id="d3cbf-130">使用提供的配置创建服务，但不定义任何终结点。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-130">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="d3cbf-131">代码</span><span class="sxs-lookup"><span data-stu-id="d3cbf-131">Code</span></span>  

 <span data-ttu-id="d3cbf-132">下面的代码演示如何创建使用消息安全的服务终结点。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-132">The following code shows how to create a service endpoint that uses message security.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#9)]
 [!code-vb[C_SecurityScenarios#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#9)]  
  
### <a name="configuration"></a><span data-ttu-id="d3cbf-133">Configuration</span><span class="sxs-lookup"><span data-stu-id="d3cbf-133">Configuration</span></span>  

 <span data-ttu-id="d3cbf-134">以下配置可代替代码使用：</span><span class="sxs-lookup"><span data-stu-id="d3cbf-134">The following configuration can be used instead of the code:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="ServiceCredentialsBehavior">  
          <serviceCredentials>  
            <serviceCertificate findValue="Contoso.com"
                                storeLocation="LocalMachine"  
                                storeName="My"
                                x509FindType="FindBySubjectName" />  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service behaviorConfiguration="ServiceCredentialsBehavior"  
               name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"  
                  binding="wsHttpBinding"  
                  bindingConfiguration="MessageAndUserName"  
                  name="SecuredByTransportEndpoint"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="MessageAndUserName">  
          <security mode="Message">
            <message clientCredentialType="UserName" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="d3cbf-135">客户端</span><span class="sxs-lookup"><span data-stu-id="d3cbf-135">Client</span></span>  
  
### <a name="code"></a><span data-ttu-id="d3cbf-136">代码</span><span class="sxs-lookup"><span data-stu-id="d3cbf-136">Code</span></span>  

 <span data-ttu-id="d3cbf-137">下面的代码创建客户端。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-137">The following code creates the client.</span></span> <span data-ttu-id="d3cbf-138">绑定设置为消息模式安全，客户端凭据类型设置为 `UserName`。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-138">The binding is to message mode security, and the client credential type is set to `UserName`.</span></span> <span data-ttu-id="d3cbf-139">用户名和密码只能使用代码指定（不可配置）。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-139">The user name and password can only be specified using code (it is not configurable).</span></span> <span data-ttu-id="d3cbf-140">返回用户名和密码的代码未在此处显示，因为这必须在应用程序级完成。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-140">The code to return the user name and password is not shown here because it must be done at the application level.</span></span> <span data-ttu-id="d3cbf-141">例如，使用 Windows 窗体对话框查询用户以获得这些数据。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-141">For example, use a Windows Forms dialog box to query the user for the data.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#16](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#16)]
 [!code-vb[C_SecurityScenarios#16](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#16)]  
  
### <a name="configuration"></a><span data-ttu-id="d3cbf-142">Configuration</span><span class="sxs-lookup"><span data-stu-id="d3cbf-142">Configuration</span></span>  

 <span data-ttu-id="d3cbf-143">下面的代码将配置客户端。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-143">The following code configures the client.</span></span> <span data-ttu-id="d3cbf-144">绑定设置为消息模式安全，客户端凭据类型设置为 `UserName`。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-144">The binding is to message mode security, and the client credential type is set to `UserName`.</span></span> <span data-ttu-id="d3cbf-145">用户名和密码只能使用代码指定（不可配置）。</span><span class="sxs-lookup"><span data-stu-id="d3cbf-145">The user name and password can only be specified using code (it is not configurable).</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="UserName" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://machineName/Calculator"
                binding="wsHttpBinding"  
                bindingConfiguration="WSHttpBinding_ICalculator"
                contract="ICalculator"  
                name="WSHttpBinding_ICalculator">  
        <identity>  
          <dns value ="Contoso.com" />  
        </identity>  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d3cbf-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3cbf-146">See also</span></span>

- [<span data-ttu-id="d3cbf-147">安全性概述</span><span class="sxs-lookup"><span data-stu-id="d3cbf-147">Security Overview</span></span>](security-overview.md)
- [<span data-ttu-id="d3cbf-148">用户名消息安全</span><span class="sxs-lookup"><span data-stu-id="d3cbf-148">Message Security User Name</span></span>](../samples/message-security-user-name.md)
- [<span data-ttu-id="d3cbf-149">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="d3cbf-149">Service Identity and Authentication</span></span>](service-identity-and-authentication.md)
- [\<identity>](../../configure-apps/file-schema/wcf/identity.md)
- <span data-ttu-id="d3cbf-150">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="d3cbf-150">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
