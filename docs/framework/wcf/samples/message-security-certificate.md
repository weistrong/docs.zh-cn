---
description: 了解详细信息：消息安全证书
title: 消息安全证书
ms.date: 03/30/2017
helpviewer_keywords:
- WS Security
ms.assetid: 909333b3-35ec-48f0-baff-9a50161896f6
ms.openlocfilehash: 6ed48466d0b5155a5f14a2ec2eae0d879b7377a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99732431"
---
# <a name="message-security-certificate"></a><span data-ttu-id="a5d9a-103">消息安全证书</span><span class="sxs-lookup"><span data-stu-id="a5d9a-103">Message Security Certificate</span></span>

<span data-ttu-id="a5d9a-104">此示例演示如何实现一个应用程序，该应用程序对客户端使用 WS 安全性和 X.509 v3 证书身份验证，并要求使用服务器的 X.509 v3 证书进行服务器身份验证。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-104">This sample demonstrates how to implement an application that uses WS-Security with X.509 v3 certificate authentication for the client and requires server authentication using the server's X.509 v3 certificate.</span></span> <span data-ttu-id="a5d9a-105">此示例使用默认设置，以便客户端和服务器之间的所有应用程序消息都经过签名和加密。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-105">This sample uses default settings such that all application messages between the client and server are signed and encrypted.</span></span> <span data-ttu-id="a5d9a-106">此示例基于 [WSHttpBinding](wshttpbinding.md) ，由 INTERNET INFORMATION SERVICES (IIS) 中承载的客户端控制台程序和服务库组成。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-106">This sample is based on the [WSHttpBinding](wshttpbinding.md) and consists of a client console program and a service library hosted by Internet Information Services (IIS).</span></span> <span data-ttu-id="a5d9a-107">该服务实现定义“请求-答复”通信模式的协定。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-107">The service implements a contract that defines a request-reply communication pattern.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a5d9a-108">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-108">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="a5d9a-109">此示例演示如何使用配置来控制身份验证，以及如何从安全上下文中获取调用方的标识，如下面的示例代码所述。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-109">The sample demonstrates controlling authentication by using configuration and how to obtain the caller’s identity from the security context, as shown in the following sample code.</span></span>  

```csharp
public class CalculatorService : ICalculator  
{  
    public string GetCallerIdentity()  
    {  
        // The client certificate is not mapped to a Windows identity by default.  
        // ServiceSecurityContext.PrimaryIdentity is populated based on the information  
        // in the certificate that the client used to authenticate itself to the service.  
        return ServiceSecurityContext.Current.PrimaryIdentity.Name;  
    }  
    ...  
}  
```  
  
 <span data-ttu-id="a5d9a-110">服务公开两个终结点，一个用来与使用配置文件 (Web.config) 定义的服务进行通信，另一个用来使用 WS-MetadataExchange 协议来公开服务的 WSDL 文档。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-110">The service exposes one endpoint for communicating with the service and one endpoint for exposing the service's WSDL document using the WS-MetadataExchange protocol, defined by using the configuration file (Web.config).</span></span> <span data-ttu-id="a5d9a-111">终结点由地址、绑定和协定组成。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-111">The endpoint consists of an address, a binding, and a contract.</span></span> <span data-ttu-id="a5d9a-112">绑定是使用标准元素配置的 [\<wsHttpBinding>](../../configure-apps/file-schema/wcf/wshttpbinding.md) ，该元素默认为使用消息安全性。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-112">The binding is configured with a standard [\<wsHttpBinding>](../../configure-apps/file-schema/wcf/wshttpbinding.md) element, which defaults to using message security.</span></span> <span data-ttu-id="a5d9a-113">此示例将 `clientCredentialType` 属性设置为 Certificate 以要求进行客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-113">This sample sets the `clientCredentialType` attribute to Certificate to require client authentication.</span></span>  
  
```xml  
<system.serviceModel>  
    <protocolMapping>  
      <add scheme="http" binding="wsHttpBinding"/>  
    </protocolMapping>  
    <bindings>  
      <wsHttpBinding>  
        <!--   
        This configuration defines the security mode as Message and   
        the clientCredentialType as Certificate.  
        -->  
        <binding>  
          <security mode ="Message">  
            <message clientCredentialType="Certificate" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <!--For debugging purposes set the includeExceptionDetailInFaults attribute to true-->  
    <behaviors>  
      <serviceBehaviors>  
        <behavior>  
          <serviceMetadata httpGetEnabled="True"/>  
          <serviceDebug includeExceptionDetailInFaults="False" />  
          <!--   
        The serviceCredentials behavior allows one to define a service certificate.  
        A service certificate is used by the service to authenticate itself to its clients and to provide message protection.  
        This configuration references the "localhost" certificate installed during the setup instructions.  
        -->  
          <serviceCredentials>  
            <serviceCertificate findValue="localhost" storeLocation="LocalMachine" storeName="My" x509FindType="FindBySubjectName" />  
            <clientCertificate>  
              <!--   
            Setting the certificateValidationMode to PeerOrChainTrust means that if the certificate   
            is in the user's Trusted People store, then it will be trusted without performing a  
            validation of the certificate's issuer chain. This setting is used here for convenience so that the   
            sample can be run without having to have certificates issued by a certification authority (CA).  
            This setting is less secure than the default, ChainTrust. The security implications of this   
            setting should be carefully considered before using PeerOrChainTrust in production code.   
            -->  
              <authentication certificateValidationMode="PeerOrChainTrust" />  
            </clientCertificate>  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
  </system.serviceModel>  
```  
  
 <span data-ttu-id="a5d9a-114">此行为指定在客户端向服务进行身份验证时使用服务凭据。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-114">The behavior specifies the service's credentials that are used when the client authenticates the service.</span></span> <span data-ttu-id="a5d9a-115">服务器证书使用者名称是在元素的属性中指定的 `findValue` [\<serviceCredentials>](../../configure-apps/file-schema/wcf/servicecredentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-115">The server certificate subject name is specified in the `findValue` attribute in the [\<serviceCredentials>](../../configure-apps/file-schema/wcf/servicecredentials.md) element.</span></span>  
  
```xml  
<!--For debugging purposes, set the includeExceptionDetailInFaults attribute to true.-->  
<behaviors>  
      <serviceBehaviors>  
        <behavior>  
          <serviceMetadata httpGetEnabled="True"/>  
          <serviceDebug includeExceptionDetailInFaults="False" />  
          <!--   
        The serviceCredentials behavior allows one to define a service certificate.  
        A service certificate is used by the service to authenticate itself to its clients and to provide message protection.  
        This configuration references the "localhost" certificate installed during the setup instructions.  
        -->  
          <serviceCredentials>  
            <serviceCertificate findValue="localhost" storeLocation="LocalMachine" storeName="My" x509FindType="FindBySubjectName" />  
            <clientCertificate>  
              <!--   
            Setting the certificateValidationMode to PeerOrChainTrust means that if the certificate   
            is in the user's Trusted People store, then it will be trusted without performing a  
            validation of the certificate's issuer chain. This setting is used here for convenience so that the   
            sample can be run without having to have certificates issued by a certification authority (CA).  
            This setting is less secure than the default, ChainTrust. The security implications of this   
            setting should be carefully considered before using PeerOrChainTrust in production code.   
            -->  
              <authentication certificateValidationMode="PeerOrChainTrust" />  
            </clientCertificate>  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
```  
  
 <span data-ttu-id="a5d9a-116">客户端终结点配置由服务终结点的绝对地址、绑定和协定组成。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-116">The client endpoint configuration consists of an absolute address for the service endpoint, the binding, and the contract.</span></span> <span data-ttu-id="a5d9a-117">客户端绑定是用相应的安全模式和身份验证模式配置的。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-117">The client binding is configured with the appropriate security mode and authentication mode.</span></span> <span data-ttu-id="a5d9a-118">在跨计算机方案中运行时，请确保相应地更改服务终结点地址。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-118">When running in a cross-computer scenario, ensure that the service endpoint address is changed accordingly.</span></span>  
  
```xml  
<system.serviceModel>  
    <client>  
      <!-- Use a behavior to configure the client certificate to present to the service. -->  
      <endpoint address="http://localhost/servicemodelsamples/service.svc" binding="wsHttpBinding" bindingConfiguration="Binding1" behaviorConfiguration="ClientCertificateBehavior" contract="Microsoft.Samples.Certificate.ICalculator"/>  
    </client>  
  
    <bindings>  
      <wsHttpBinding>  
        <!--   
        This configuration defines the security mode as Message and   
        the clientCredentialType as Certificate.  
        -->  
        <binding name="Binding1">  
          <security mode="Message">  
            <message clientCredentialType="Certificate"/>  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
...  
</system.serviceModel>  
```  
  
 <span data-ttu-id="a5d9a-119">客户端实现可以通过配置文件或通过代码来设置要使用的证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-119">The client implementation can set the certificate to use, either through the configuration file or through code.</span></span> <span data-ttu-id="a5d9a-120">下面的示例演示如何设置要在配置文件中使用的证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-120">The following sample shows how to set the certificate to use in the configuration file.</span></span>  
  
```xml  
<system.serviceModel>  
  ...  
  
<behaviors>  
      <endpointBehaviors>  
        <behavior name="ClientCertificateBehavior">  
          <!--   
        The clientCredentials behavior allows one to define a certificate to present to a service.  
        A certificate is used by a client to authenticate itself to the service and provide message integrity.  
        This configuration references the "client.com" certificate installed during the setup instructions.  
        -->  
          <clientCredentials>  
            <clientCertificate findValue="client.com" storeLocation="CurrentUser" storeName="My" x509FindType="FindBySubjectName"/>  
            <serviceCertificate>  
              <!--   
            Setting the certificateValidationMode to PeerOrChainTrust means that if the certificate   
            is in the user's Trusted People store, then it will be trusted without performing a  
            validation of the certificate's issuer chain. This setting is used here for convenience so that the   
            sample can be run without having to have certificates issued by a certificate authority (CA).  
            This setting is less secure than the default, ChainTrust. The security implications of this   
            setting should be carefully considered before using PeerOrChainTrust in production code.   
            -->  
              <authentication certificateValidationMode="PeerOrChainTrust"/>  
            </serviceCertificate>  
          </clientCredentials>  
        </behavior>  
      </endpointBehaviors>  
    </behaviors>  
  
</system.serviceModel>  
```  
  
 <span data-ttu-id="a5d9a-121">下面的示例演示如何在程序中调用服务。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-121">The following sample shows how to call the service in your program.</span></span>  

```csharp
// Create a client.  
CalculatorClient client = new CalculatorClient();  
  
// Call the GetCallerIdentity service operation.  
Console.WriteLine(client.GetCallerIdentity());  
...  
//Closing the client gracefully closes the connection and cleans up resources.  
client.Close();  
```
  
 <span data-ttu-id="a5d9a-122">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-122">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="a5d9a-123">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-123">Press ENTER in the client window to shut down the client.</span></span>  
  
```console  
CN=client.com  
Add(100,15.99) = 115.99  
Subtract(145,76.54) = 68.46  
Multiply(9,81.25) = 731.25  
Divide(22,7) = 3.14285714285714  
Press <ENTER> to terminate client.  
```  
  
 <span data-ttu-id="a5d9a-124">通过运行消息安全示例随附的 Setup.bat 批处理文件，可以用相关的证书将客户端和服务器配置为运行承载应用程序，该应用程序需要基于证书的安全性。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-124">The Setup.bat batch file included with the Message Security samples enables you to configure the client and server with relevant certificates to run a hosted application that requires certificate-based security.</span></span> <span data-ttu-id="a5d9a-125">该批处理文件可以在三个模式下运行。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-125">The batch file can be run in three modes.</span></span> <span data-ttu-id="a5d9a-126">若要在单一计算机模式下运行，请在 Visual Studio 的开发人员命令提示中 **setup.bat** 对于服务模式，请键入 **setup.bat 服务**;对于客户端模式类型 **setup.bat 客户端**。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-126">To run in single-computer mode type **setup.bat** in a Developer Command Prompt for Visual Studio ; for service mode type **setup.bat service**; and for client mode type **setup.bat client**.</span></span> <span data-ttu-id="a5d9a-127">在跨计算机运行示例时，可以使用客户端模式和服务器模式。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-127">Use the client and server mode when running the sample across computers.</span></span> <span data-ttu-id="a5d9a-128">有关详细信息，请参见本主题末尾的设置过程。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-128">See the setup procedure at the end of this topic for details.</span></span> <span data-ttu-id="a5d9a-129">下面提供了批处理文件不同节的简要概述，您可以修改这些批处理文件，使其能够在相应的配置中运行：</span><span class="sxs-lookup"><span data-stu-id="a5d9a-129">The following provides a brief overview of the different sections of the batch files so that they can be modified to run in appropriate configuration:</span></span>  
  
- <span data-ttu-id="a5d9a-130">创建客户端证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-130">Creating the client certificate.</span></span>  
  
     <span data-ttu-id="a5d9a-131">批处理文件中的以下行用于创建客户端证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-131">The following line in the batch file creates the client certificate.</span></span> <span data-ttu-id="a5d9a-132">创建的证书的主题名称中会使用指定的客户端名称。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-132">The client name specified is used in the subject name of the certificate created.</span></span> <span data-ttu-id="a5d9a-133">证书存储在 `My` 存储位置下的 `CurrentUser` 存储区中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-133">The certificate is stored in `My` store at the `CurrentUser` store location.</span></span>  
  
    ```bat
    echo ************  
    echo making client cert  
    echo ************  
    makecert.exe -sr CurrentUser -ss MY -a sha1 -n CN=%CLIENT_NAME% -sky exchange -pe  
    ```  
  
- <span data-ttu-id="a5d9a-134">将客户端证书安装到服务器的受信任证书存储区中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-134">Installing the client certificate into the server’s trusted certificate store.</span></span>  
  
     <span data-ttu-id="a5d9a-135">批处理文件中的以下行将客户端证书复制到服务器的 TrustedPeople 存储中，以使服务器能够做出相关的信任或不信任决定。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-135">The following line in the batch file copies the client certificate into the server's TrustedPeople store so that the server can make the relevant trust or no-trust decisions.</span></span> <span data-ttu-id="a5d9a-136">为了使安装在 TrustedPeople 存储中的证书受 Windows Communication Foundation (WCF) 服务信任，必须将客户端证书验证模式设置为 `PeerOrChainTrust` 或 `PeerTrust` 。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-136">In order for a certificate installed in the TrustedPeople store to be trusted by a Windows Communication Foundation (WCF) service, the client certificate validation mode must be set to `PeerOrChainTrust` or `PeerTrust`.</span></span> <span data-ttu-id="a5d9a-137">请参见前面的服务配置示例，了解如何使用配置文件完成此操作。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-137">See the previous service configuration sample to learn how this can be done by using a configuration file.</span></span>  
  
    ```bat
    echo ************  
    echo copying client cert to server's LocalMachine store  
    echo ************  
    certmgr.exe -add -r CurrentUser -s My -c -n %CLIENT_NAME% -r LocalMachine -s TrustedPeople
    ```  
  
- <span data-ttu-id="a5d9a-138">创建服务器证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-138">Creating the server certificate.</span></span>  
  
     <span data-ttu-id="a5d9a-139">Setup.bat 批处理文件中的以下行创建将要使用的服务器证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-139">The following lines from the Setup.bat batch file create the server certificate to be used.</span></span>  
  
    ```bat
    echo ************  
    echo Server cert setup starting  
    echo %SERVER_NAME%  
    echo ************  
    echo making server cert  
    echo ************  
    makecert.exe -sr LocalMachine -ss MY -a sha1 -n CN=%SERVER_NAME% -sky exchange -pe  
    ```  
  
     <span data-ttu-id="a5d9a-140">%SERVER_NAME% 变量指定服务器名称。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-140">The %SERVER_NAME% variable specifies the server name.</span></span> <span data-ttu-id="a5d9a-141">该证书存储在 LocalMachine 存储区中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-141">The certificate is stored in the LocalMachine store.</span></span> <span data-ttu-id="a5d9a-142">如果使用服务 (的参数（如）运行 Setup.bat 批处理文件， **setup.bat 服务**) % SERVER_NAME% 包含计算机的完全限定域名。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-142">If the Setup.bat batch file is run with an argument of service (such as, **setup.bat service**) the %SERVER_NAME% contains the fully-qualified domain name of the computer.</span></span> <span data-ttu-id="a5d9a-143">否则，它默认为 localhost。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-143">Otherwise it defaults to localhost.</span></span>  
  
- <span data-ttu-id="a5d9a-144">将服务器证书安装到客户端的受信任证书存储区中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-144">Installing the server certificate into the client’s trusted certificate store.</span></span>  
  
     <span data-ttu-id="a5d9a-145">以下行将服务器证书复制到客户端的受信任人存储中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-145">The following line copies the server certificate into the client trusted people store.</span></span> <span data-ttu-id="a5d9a-146">因为客户端系统不隐式信任 Makecert.exe 生成的证书，所以需要执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-146">This step is required because certificates generated by Makecert.exe are not implicitly trusted by the client system.</span></span> <span data-ttu-id="a5d9a-147">如果已经拥有一个证书，该证书来源于客户端的受信任根证书（例如由 Microsoft 颁发的证书），则不需要执行使用服务器证书填充客户端证书存储区这一步骤。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-147">If you already have a certificate that is rooted in a client trusted root certificate—for example, a Microsoft-issued certificate—this step of populating the client certificate store with the server certificate is not required.</span></span>  
  
    ```console  
    certmgr.exe -add -r LocalMachine -s My -c -n %SERVER_NAME% -r CurrentUser -s TrustedPeople  
    ```  
  
- <span data-ttu-id="a5d9a-148">授予对证书私钥的权限。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-148">Granting permissions on the certificate's private key.</span></span>  
  
     <span data-ttu-id="a5d9a-149">Setup.bat 文件中的以下行使 ASP.NET 工作进程帐户可以访问存储在 LocalMachine 存储区中的服务器证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-149">The following lines in the Setup.bat file make the server certificate stored in the LocalMachine store accessible to the ASP.NET worker process account.</span></span>  
  
    ```bat
    echo ************  
    echo setting privileges on server certificates  
    echo ************  
    for /F "delims=" %%i in ('"%ProgramFiles%\ServiceModelSampleTools\FindPrivateKey.exe" My LocalMachine -n CN^=%SERVER_NAME% -a') do set PRIVATE_KEY_FILE=%%i  
    set WP_ACCOUNT=NT AUTHORITY\NETWORK SERVICE  
    (ver | findstr /C:"5.1") && set WP_ACCOUNT=%COMPUTERNAME%\ASPNET  
    echo Y|cacls.exe "%PRIVATE_KEY_FILE%" /E /G "%WP_ACCOUNT%":R  
    iisreset  
    ```  
  
    > [!NOTE]
    > <span data-ttu-id="a5d9a-150">如果你使用的是非美国英语版本的 Windows 中，必须编辑 Setup.bat 文件，并将 "NT AUTHORITY\NETWORK SERVICE" 帐户名称替换为你的区域性等效项。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-150">If you are using a non-U.S. English edition of Windows, you must edit the Setup.bat file and replace the "NT AUTHORITY\NETWORK SERVICE" account name with your regional equivalent.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a5d9a-151">该批处理文件中使用的工具位于 C:\Program Files\Microsoft Visual Studio 8\Common7\tools 或 C:\Program Files\Microsoft SDKs\Windows\v6.0\bin 中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-151">The tools used in this batch file are located in either C:\Program Files\Microsoft Visual Studio 8\Common7\tools or C:\Program Files\Microsoft SDKs\Windows\v6.0\bin.</span></span> <span data-ttu-id="a5d9a-152">这两个目录中必须有一个位于系统路径中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-152">One of these directories must be in your system path.</span></span> <span data-ttu-id="a5d9a-153">如果安装了 Visual Studio，则在路径中获取此目录的最简单方法是打开 Visual Studio 的开发人员命令提示。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-153">If you have Visual Studio installed, the easiest way to get this directory in your path is to open the Developer Command Prompt for Visual Studio.</span></span> <span data-ttu-id="a5d9a-154">单击 " **开始**"，然后选择 " **所有程序**"、" **Visual Studio 2012**" 和 " **工具**"。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-154">Click **Start**, and then select **All Programs**, **Visual Studio 2012**, **Tools**.</span></span> <span data-ttu-id="a5d9a-155">此命令提示中已经配置了相应的路径。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-155">This command prompt has the appropriate paths already configured.</span></span> <span data-ttu-id="a5d9a-156">否则，您必须向路径中手动添加相应的目录。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-156">Otherwise you must add the appropriate directory to your path manually.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="a5d9a-157">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-157">The samples may already be installed on your computer.</span></span> <span data-ttu-id="a5d9a-158">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="a5d9a-158">Check for the following (default) directory before continuing:</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="a5d9a-159">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5d9a-159">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="a5d9a-160">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="a5d9a-160">This sample is located in the following directory:</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\WS\MessageSecurity`  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="a5d9a-161">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="a5d9a-161">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="a5d9a-162">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-162">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="a5d9a-163">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-163">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
### <a name="to-run-the-sample-on-the-same-computer"></a><span data-ttu-id="a5d9a-164">在同一计算机上运行示例</span><span class="sxs-lookup"><span data-stu-id="a5d9a-164">To run the sample on the same computer</span></span>  
  
1. <span data-ttu-id="a5d9a-165">使用管理员权限打开 Visual Studio 开发人员命令提示，并从示例安装文件夹中运行 Setup.bat。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-165">Open a Developer Command Prompt for Visual Studio  with administrator privileges and run Setup.bat from the sample install folder.</span></span> <span data-ttu-id="a5d9a-166">这将安装运行示例所需的所有证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-166">This installs all the certificates required for running the sample.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="a5d9a-167">Setup.bat 批处理文件设计为从 Visual Studio 的开发人员命令提示运行。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-167">The Setup.bat batch file is designed to be run from a Developer Command Prompt for Visual Studio.</span></span> <span data-ttu-id="a5d9a-168">这要求路径环境变量指向 SDK 的安装目录。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-168">It requires that the path environment variable point to the directory where the SDK is installed.</span></span> <span data-ttu-id="a5d9a-169">在 Visual Studio (2010) 的开发人员命令提示中自动设置此环境变量。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-169">This environment variable is automatically set within a Developer Command Prompt for Visual Studio (2010).</span></span>  
  
2. <span data-ttu-id="a5d9a-170">通过输入地址来验证使用浏览器访问服务 `http://localhost/servicemodelsamples/service.svc` 。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-170">Verify access to the service using a browser by entering the address `http://localhost/servicemodelsamples/service.svc`.</span></span>  
  
3. <span data-ttu-id="a5d9a-171">启动 \client\bin 中的 Client.exe。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-171">Launch Client.exe from \client\bin.</span></span> <span data-ttu-id="a5d9a-172">客户端活动将显示在客户端控制台应用程序上。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-172">Client activity is displayed on the client console application.</span></span>  
  
4. <span data-ttu-id="a5d9a-173">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-173">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
### <a name="to-run-the-sample-across-computers"></a><span data-ttu-id="a5d9a-174">跨计算机运行示例</span><span class="sxs-lookup"><span data-stu-id="a5d9a-174">To run the sample across computers</span></span>  
  
1. <span data-ttu-id="a5d9a-175">在服务计算机上创建目录。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-175">Create a directory on the service computer.</span></span> <span data-ttu-id="a5d9a-176">使用 Internet Information Services (IIS) 管理工具为此目录创建名为 servicemodelsamples 的虚拟应用程序。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-176">Create a virtual application named servicemodelsamples for this directory by using the Internet Information Services (IIS) management tool.</span></span>  
  
2. <span data-ttu-id="a5d9a-177">将服务程序文件从 \inetpub\wwwroot\servicemodelsamples 复制到服务计算机上的虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-177">Copy the service program files from \inetpub\wwwroot\servicemodelsamples to the virtual directory on the service computer.</span></span> <span data-ttu-id="a5d9a-178">确保复制 \bin 子目录中的文件。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-178">Ensure that you copy the files in the \bin subdirectory.</span></span> <span data-ttu-id="a5d9a-179">另外，将 Setup.bat、Cleanup.bat 和 ImportClientCert.bat 文件复制到服务计算机上。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-179">Also copy the Setup.bat, Cleanup.bat, and ImportClientCert.bat files to the service computer.</span></span>  
  
3. <span data-ttu-id="a5d9a-180">在客户端计算机上为这些客户端二进制文件创建一个目录。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-180">Create a directory on the client computer for the client binaries.</span></span>  
  
4. <span data-ttu-id="a5d9a-181">将客户端程序文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-181">Copy the client program files to the client directory on the client computer.</span></span> <span data-ttu-id="a5d9a-182">另外，将 Setup.bat、Cleanup.bat 和 ImportServiceCert.bat 文件复制到客户端上。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-182">Also copy the Setup.bat, Cleanup.bat, and ImportServiceCert.bat files to the client.</span></span>  
  
5. <span data-ttu-id="a5d9a-183">在服务器上，使用管理员权限在 Visual Studio 开发人员命令提示中运行 **setup.bat 服务** 。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-183">On the server, run **setup.bat service** in a Developer Command Prompt for Visual Studio with administrator privileges.</span></span> <span data-ttu-id="a5d9a-184">使用 **服务** 参数运行 **setup.bat** 将使用计算机的完全限定域名创建服务证书，并将服务证书导出到名为的文件。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-184">Running **setup.bat** with the **service** argument creates a service certificate with the fully-qualified domain name of the computer and exports the service certificate to a file named Service.cer.</span></span>  
  
6. <span data-ttu-id="a5d9a-185">编辑 Web.config，以反映) 的属性中 (新的证书名称，该名称与 `findValue` [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md) 计算机的完全限定域名相同。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-185">Edit Web.config to reflect the new certificate name (in the `findValue` attribute in the [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md)) which is the same as the fully-qualified domain name of the computer.</span></span>  
  
7. <span data-ttu-id="a5d9a-186">将服务目录中的 Service.cer 文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-186">Copy the Service.cer file from the service directory to the client directory on the client computer.</span></span>  
  
8. <span data-ttu-id="a5d9a-187">在客户端上，使用管理员权限在 Visual Studio 的开发人员命令提示中运行 **setup.bat 客户端** 。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-187">On the client, run **setup.bat client** in a Developer Command Prompt for Visual Studio with administrator privileges.</span></span> <span data-ttu-id="a5d9a-188">使用 **客户端** 参数运行 **setup.bat** 会创建一个名为 client.com 的客户端证书，并将客户端证书导出到名为的文件。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-188">Running **setup.bat** with the **client** argument creates a client certificate named client.com and exports the client certificate to a file named Client.cer.</span></span>  
  
9. <span data-ttu-id="a5d9a-189">在客户端计算机上的 Client.exe.config 文件中，更改终结点的地址值，使其与服务的新地址相匹配。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-189">In the Client.exe.config file on the client computer, change the address value of the endpoint to match the new address of your service.</span></span> <span data-ttu-id="a5d9a-190">通过用服务器的完全限定域名替换 localhost 来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-190">Do this by replacing localhost with the fully-qualified domain name of the server.</span></span>  
  
10. <span data-ttu-id="a5d9a-191">将客户端目录中的 Client.cer 文件复制到服务器上的服务目录中。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-191">Copy the Client.cer file from the client directory to the service directory on the server.</span></span>  
  
11. <span data-ttu-id="a5d9a-192">在客户端上，以具有管理权限的 Visual Studio 开发人员命令提示运行 ImportServiceCert.bat。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-192">On the client, run ImportServiceCert.bat in a Developer Command Prompt for Visual Studio with administrative privileges.</span></span> <span data-ttu-id="a5d9a-193">这会将 Service.cer 文件中的服务证书导入 CurrentUser – TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-193">This imports the service certificate from the Service.cer file into the CurrentUser - TrustedPeople store.</span></span>  
  
12. <span data-ttu-id="a5d9a-194">在服务器上，以具有管理权限的 Visual Studio 开发人员命令提示运行 ImportClientCert.bat。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-194">On the server, run ImportClientCert.bat in a Developer Command Prompt for Visual Studio with administrative privileges.</span></span> <span data-ttu-id="a5d9a-195">这会将 Client.cer 文件中的客户端证书导入 LocalMachine - TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-195">This imports the client certificate from the Client.cer file into the LocalMachine - TrustedPeople store.</span></span>  
  
13. <span data-ttu-id="a5d9a-196">在客户端计算机上，从命令提示窗口中启动 Client.exe。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-196">On the client computer, launch Client.exe from a command prompt window.</span></span> <span data-ttu-id="a5d9a-197">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-197">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
### <a name="to-clean-up-after-the-sample"></a><span data-ttu-id="a5d9a-198">运行示例后进行清理</span><span class="sxs-lookup"><span data-stu-id="a5d9a-198">To clean up after the sample</span></span>  
  
- <span data-ttu-id="a5d9a-199">运行完示例后运行示例文件夹中的 Cleanup.bat。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-199">Run Cleanup.bat in the samples folder after you have finished running the sample.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="a5d9a-200">此脚本不会在跨计算机运行此示例时移除客户端上的服务证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-200">This script does not remove service certificates on a client when running this sample across computers.</span></span> <span data-ttu-id="a5d9a-201">如果你已运行 Windows Communication Foundation 跨计算机使用证书 (WCF) 示例，请确保清除已安装在 CurrentUser-TrustedPeople 存储中的服务证书。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-201">If you have run Windows Communication Foundation (WCF) samples that use certificates across computers, be sure to clear the service certificates that have been installed in the CurrentUser - TrustedPeople store.</span></span> <span data-ttu-id="a5d9a-202">为此，请使用以下命令：`certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>`，例如：`certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`。</span><span class="sxs-lookup"><span data-stu-id="a5d9a-202">To do this, use the following command: `certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>` For example: `certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`.</span></span>
