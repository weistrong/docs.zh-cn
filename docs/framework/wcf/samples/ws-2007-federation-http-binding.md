---
description: 了解有关以下内容的详细信息： WS 2007 联合 HTTP 绑定
title: WS 2007 联合 HTTP 绑定
ms.date: 03/30/2017
ms.assetid: 91c1b477-a96e-4bf5-9330-5e9312113371
ms.openlocfilehash: 12363abb1c8c503db8ec4aac9197276c8ec41c58
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715049"
---
# <a name="ws-2007-federation-http-binding"></a><span data-ttu-id="ee9c1-103">WS 2007 联合 HTTP 绑定</span><span class="sxs-lookup"><span data-stu-id="ee9c1-103">WS 2007 Federation HTTP Binding</span></span>

<span data-ttu-id="ee9c1-104">此示例演示 <xref:System.ServiceModel.WS2007FederationHttpBinding> 的用法，它是一个标准绑定，可用来生成支持 1.3 版 WS-Trust 规范的联合方案。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-104">This sample demonstrates the use of <xref:System.ServiceModel.WS2007FederationHttpBinding>, a standard binding that you can use to build federated scenarios that support version 1.3 of the WS-Trust specification.</span></span>

> [!NOTE]
> <span data-ttu-id="ee9c1-105">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-105">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="ee9c1-106">该示例包含基于控制台的客户端程序 (*Client.exe*) 、基于控制台的 security token service *程序 (Securitytokenservice.exe) 和* 基于控制台的服务程序 (*Service.exe*) 。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-106">The sample consists of a console-based client program (*Client.exe*), a console-based security token service program (*Securitytokenservice.exe*), and a console-based service program (*Service.exe*).</span></span> <span data-ttu-id="ee9c1-107">服务实现用来定义“请求/答复”通信模式的协定。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-107">The service implements a contract that defines a request/reply communication pattern.</span></span> <span data-ttu-id="ee9c1-108">该协定由 `ICalculator` 接口定义，此接口公开数学运算（`Add`、`Subtract`、`Multiply` 和 `Divide`）。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-108">The contract is defined by the `ICalculator` interface, which exposes math operations (`Add`, `Subtract`, `Multiply`, and `Divide`).</span></span> <span data-ttu-id="ee9c1-109">客户端从安全令牌服务 (STS) 获取安全令牌，向服务发出同步请求，以进行给定数学运算。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-109">The client obtains a security token from the Security Token Service (STS) and makes synchronous requests to the service for a given math operation.</span></span> <span data-ttu-id="ee9c1-110">服务使用结果进行回复。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-110">The service then replies with the result.</span></span> <span data-ttu-id="ee9c1-111">客户端活动显示在控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-111">Client activity is visible in the console window.</span></span>

<span data-ttu-id="ee9c1-112">此示例使用 `ICalculator` 元素提供 `ws2007FederationHttpBinding` 协定。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-112">The sample makes the `ICalculator` contract available using the `ws2007FederationHttpBinding` element.</span></span> <span data-ttu-id="ee9c1-113">此绑定在客户端上的配置如下所示：</span><span class="sxs-lookup"><span data-stu-id="ee9c1-113">The configuration of this binding on the client is shown in the following code:</span></span>

```xml
<bindings>
  <ws2007FederationHttpBinding>
    <binding name="ServiceFed" >
      <security mode ="Message">
        <message issuedKeyType ="SymmetricKey"
                 issuedTokenType ="http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV1.1" >
          <!-- Endpoint address and binding for Security Token Service -->
          <issuer address ="http://localhost:8000/sts/windows"
                  binding ="ws2007HttpBinding" />
        </message>
      </security>
    </binding>
  </ws2007FederationHttpBinding>
</bindings>
```

<span data-ttu-id="ee9c1-114">在上 [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md) ， `security` 值指定应该使用的安全模式。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-114">On the [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md), the `security` value specifies which security mode should be used.</span></span> <span data-ttu-id="ee9c1-115">在此示例中， `message` 使用了安全，这就是在 [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) 中指定的原因 [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-115">In this sample, `message` security is used, which is why the [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) is specified inside the [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md).</span></span> <span data-ttu-id="ee9c1-116">[\<issuer>](../../configure-apps/file-schema/wcf/issuer.md)内的元素 [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) 为向客户端颁发安全令牌的 STS 指定地址和绑定，以便客户端可以向服务进行身份验证 `ICalculator` 。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-116">The [\<issuer>](../../configure-apps/file-schema/wcf/issuer.md) element inside the [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) specifies the address and binding for the STS that issues a security token to the client so that the client can authenticate to the `ICalculator` service.</span></span>
  
<span data-ttu-id="ee9c1-117">下面的代码演示了如何在服务上配置此绑定：</span><span class="sxs-lookup"><span data-stu-id="ee9c1-117">The configuration of this binding on the service is shown in the following code:</span></span>

```xml
<bindings>
  <ws2007FederationHttpBinding>
    <binding name="ServiceFed" >
      <security mode ="Message">
        <message issuedKeyType ="SymmetricKey"
                 issuedTokenType ="http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV1.1" >
          <!-- Metadata address for Security Token Service -->
          <issuerMetadata address ="http://localhost:8000/sts/mex" >
            <identity>
              <certificateReference storeLocation ="CurrentUser"
                                    storeName="TrustedPeople"
                                    x509FindType ="FindBySubjectDistinguishedName"
                                    findValue ="CN=STS" />
            </identity>
          </issuerMetadata>
        </message>
      </security>
    </binding>
  </ws2007FederationHttpBinding>
</bindings>
```

<span data-ttu-id="ee9c1-118">在上 [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md) ， `security` 值指定应该使用的安全模式。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-118">On the [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md), the `security` value specifies which security mode should be used.</span></span> <span data-ttu-id="ee9c1-119">在此示例中， `message` 使用了安全，这就是在 [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) 中指定的原因 [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-119">In this sample, `message` security is used, which is why the [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) is specified inside the [\<security>](../../configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md).</span></span> <span data-ttu-id="ee9c1-120">[\<issuerMetadata>](../../configure-apps/file-schema/wcf/issuermetadata.md)内的元素 `ws2007FederationHttpBinding` [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) 指定终结点的地址和标识，该终结点可用于检索 STS 的元数据。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-120">The [\<issuerMetadata>](../../configure-apps/file-schema/wcf/issuermetadata.md) element of `ws2007FederationHttpBinding` inside the [\<message>](../../configure-apps/file-schema/wcf/message-element-of-ws2007federationhttpbinding.md) specifies the address and identity for an endpoint that can be used to retrieve metadata for the STS.</span></span>

<span data-ttu-id="ee9c1-121">以下代码显示了服务的行为：</span><span class="sxs-lookup"><span data-stu-id="ee9c1-121">The behavior for the service is shown in the following code:</span></span>

```xml
<behaviors>
  <serviceBehaviors>
    <behavior name ="ServiceBehaviour" >
      <serviceDebug includeExceptionDetailInFaults ="true"/>
      <serviceMetadata httpGetEnabled ="true"/>
      <serviceCredentials>
        <issuedTokenAuthentication>
          <knownCertificates>
            <add storeLocation ="LocalMachine"
                 storeName="TrustedPeople"
                 x509FindType="FindBySubjectDistinguishedName"
                 findValue="CN=STS" />
          </knownCertificates>
        </issuedTokenAuthentication>
        <serviceCertificate storeLocation ="LocalMachine"
                            storeName ="My"
                            x509FindType ="FindBySubjectDistinguishedName"
                            findValue ="CN=localhost"/>
      </serviceCredentials>
    </behavior>
  </serviceBehaviors>
</behaviors>
```
  
<span data-ttu-id="ee9c1-122">[\<issuedTokenAuthentication>](../../configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)> 允许服务在身份验证过程中为其允许客户端提供的令牌指定约束。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-122">The [\<issuedTokenAuthentication>](../../configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)> allows the service to specify constraints on the tokens it allows clients to present during authentication.</span></span> <span data-ttu-id="ee9c1-123">此配置指定该服务接受由主题名称为 CN=STS 的证书签名的令牌。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-123">This configuration specifies that tokens signed by a certificate whose subject name is CN=STS are accepted by the service.</span></span>

<span data-ttu-id="ee9c1-124">STS 使用标准的 <xref:System.ServiceModel.WS2007HttpBinding> 提供单个终结点。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-124">STS makes a single endpoint available using the standard <xref:System.ServiceModel.WS2007HttpBinding>.</span></span> <span data-ttu-id="ee9c1-125">服务响应客户端对令牌的请求。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-125">The service responds to requests from clients for tokens.</span></span> <span data-ttu-id="ee9c1-126">如果客户端使用 Windows 帐户进行身份验证，则服务将颁发一个令牌，该令牌以声明的形式包含客户端的用户名。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-126">If the client is authenticated using a Windows account, the service issues a token that contains the client's user name as a claim.</span></span> <span data-ttu-id="ee9c1-127">在创建令牌的过程中，STS 使用与 CN=STS 证书关联的私钥对令牌进行签名。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-127">As part of creating the token, STS signs the token using the private key associated with the CN=STS certificate.</span></span> <span data-ttu-id="ee9c1-128">另外，它还创建对称密钥并使用与 CN=localhost 证书关联的公钥对该密钥进行加密。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-128">In addition, it creates a symmetric key and encrypts it using the public key associated with the CN=localhost certificate.</span></span> <span data-ttu-id="ee9c1-129">在向客户端返回令牌的过程中，STS 还返回对称密钥。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-129">In returning the token to the client, STS also returns the symmetric key.</span></span> <span data-ttu-id="ee9c1-130">客户端向 `ICalculator` 服务出示所颁发的令牌，并通过使用密钥对消息进行签名来证明客户端知道该对称密钥。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-130">The client presents the issued token to the `ICalculator` service and proves that it knows the symmetric key by signing the message with that key.</span></span>

<span data-ttu-id="ee9c1-131">运行示例时，对安全令牌的请求显示在 STS 控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-131">When you run the sample, the request for the security token is shown in the STS console window.</span></span> <span data-ttu-id="ee9c1-132">操作请求和响应显示在客户端和服务控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-132">The operation's requests and responses are displayed in the client and service console windows.</span></span> <span data-ttu-id="ee9c1-133">在任何一个控制台窗口中按 Enter 可以关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-133">Press ENTER in any of the console windows to shut down the application.</span></span>

```console
Add(100,15.99) = 115.99
Subtract(145,76.54) = 68.46
Multiply(9,81.25) = 731.25
Divide(22,7) = 3.14285714285714
Press <ENTER> to terminate client.
```

<span data-ttu-id="ee9c1-134">此示例附带的 *Setup.bat* 文件允许你使用相关证书来配置服务器和 STS，以运行自承载的应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-134">The *Setup.bat* file included with this sample allows you to configure the server and STS with the relevant certificates to run a self-hosted application.</span></span> <span data-ttu-id="ee9c1-135">该批处理文件在 LocalMachine/TrustedPeople 证书存储区中创建两个证书。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-135">The batch file creates two certificates in the LocalMachine/TrustedPeople certificate store.</span></span> <span data-ttu-id="ee9c1-136">第一个证书的主题名称为 CN=STS，STS 使用该证书对颁发给客户端的安全令牌进行签名。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-136">The first certificate has a subject name of CN=STS and is used by STS to sign the security tokens that it issues to the client.</span></span> <span data-ttu-id="ee9c1-137">第二个证书的主题名称为 CN=localhost，STS 使用该证书，按照服务能够解密的方式对密钥进行加密。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-137">The second certificate has a subject name of CN=localhost and is used by STS to encrypt a key in a way that the service can decrypt.</span></span>

## <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ee9c1-138">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="ee9c1-138">To set up, build, and run the sample</span></span>
  
1. <span data-ttu-id="ee9c1-139">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-139">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="ee9c1-140">使用管理员权限打开 Visual Studio 开发人员命令提示，并运行 Setup.bat 文件创建所需的证书。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-140">Open a Developer Command Prompt for Visual Studio with administrator privileges and run the Setup.bat file to create the required certificates.</span></span>

 <span data-ttu-id="ee9c1-141">此批处理文件使用与 Windows SDK 分发的 *Certmgr.exe* 和 Makecert.exe。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-141">This batch file uses *Certmgr.exe* and Makecert.exe, which are distributed with the Windows SDK.</span></span> <span data-ttu-id="ee9c1-142">但是，必须在 Visual Studio 命令提示符中运行 *Setup.bat* ，才能使脚本能够找到这些工具。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-142">However, you must run *Setup.bat* from within a Visual Studio command prompt to enable the script to find these tools.</span></span>

1. <span data-ttu-id="ee9c1-143">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-143">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

2. <span data-ttu-id="ee9c1-144">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-144">To run the sample in a single- or cross-computer configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span> <span data-ttu-id="ee9c1-145">如果使用的是 Windows Vista，则必须使用提升的权限运行 *Service.exe*、 *Client.exe* 和 *SecurityTokenService.exe* (右键单击文件，然后单击 "以 **管理员身份运行**) "。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-145">If you are using Windows Vista, you must run *Service.exe*, *Client.exe*, and *SecurityTokenService.exe* with elevated privileges (right-click the files and then click **Run as administrator**).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee9c1-146">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="ee9c1-146">The samples may already be installed on your computer.</span></span> <span data-ttu-id="ee9c1-147">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="ee9c1-147">Check for the following (default) directory before continuing:</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="ee9c1-148">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee9c1-148">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ee9c1-149">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="ee9c1-149">This sample is located in the following directory:</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\WS\WS2007FederationHttp`
