---
description: 了解详细信息： x.509 证书验证程序
title: X.509 证书验证程序
ms.date: 03/30/2017
ms.assetid: 3b042379-02c4-4395-b927-e57c842fd3e0
ms.openlocfilehash: 3fead47cab4d639640f5af755717636ca2e8d01e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726229"
---
# <a name="x509-certificate-validator"></a><span data-ttu-id="4f734-103">X.509 证书验证程序</span><span class="sxs-lookup"><span data-stu-id="4f734-103">X.509 Certificate Validator</span></span>

<span data-ttu-id="4f734-104">此示例演示如何实现自定义 X.509 证书验证程序。</span><span class="sxs-lookup"><span data-stu-id="4f734-104">This sample demonstrates how to implement a custom X.509 Certificate Validator.</span></span> <span data-ttu-id="4f734-105">当内置的 X.509 证书验证模式都不能满足应用程序的要求时，实现自定义证书验证程序很有用。</span><span class="sxs-lookup"><span data-stu-id="4f734-105">This is useful in cases where none of the built-in X.509 Certificate Validation modes is appropriate for the requirements of the application.</span></span> <span data-ttu-id="4f734-106">此示例演示了具有自定义验证程序的服务，该验证程序接受自行颁发的证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-106">This sample shows a service that has a custom validator that accepts self-issued certificates.</span></span> <span data-ttu-id="4f734-107">客户端使用此类证书对服务进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4f734-107">The client uses such a certificate to authenticate to the service.</span></span>

<span data-ttu-id="4f734-108">注意：因为任何人都可以构造自行颁发的证书，所以服务使用的自定义验证程序的安全性低于 ChainTrust X509CertificateValidationMode 提供的默认行为。</span><span class="sxs-lookup"><span data-stu-id="4f734-108">Note: As anyone can construct a self-issued certificate the custom validator used by the service is less secure than the default behavior provided by the ChainTrust X509CertificateValidationMode.</span></span> <span data-ttu-id="4f734-109">在成品代码中使用此验证逻辑之前，应慎重考虑这样做的安全隐患。</span><span class="sxs-lookup"><span data-stu-id="4f734-109">The security implications of this should be carefully considered before using this validation logic in production code.</span></span>

<span data-ttu-id="4f734-110">概括而言，此示例演示：</span><span class="sxs-lookup"><span data-stu-id="4f734-110">In summary this sample demonstrates how:</span></span>

- <span data-ttu-id="4f734-111">如何使用 X.509 证书对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4f734-111">The client can be authenticated using an X.509 certificate.</span></span>

- <span data-ttu-id="4f734-112">服务器如何根据自定义 X509CertificateValidator 验证客户端凭据。</span><span class="sxs-lookup"><span data-stu-id="4f734-112">The server validates the client credentials against a custom X509CertificateValidator.</span></span>

- <span data-ttu-id="4f734-113">如何使用服务器的 X.509 证书对服务器进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4f734-113">The server is authenticated using the server's X.509 certificate.</span></span>

<span data-ttu-id="4f734-114">服务公开一个终结点，以便与使用配置文件 App.config 定义的服务进行通信。终结点由地址、绑定和协定组成。</span><span class="sxs-lookup"><span data-stu-id="4f734-114">The service exposes a single endpoint for communicating with the service, defined using the configuration file App.config. The endpoint consists of an address, a binding, and a contract.</span></span> <span data-ttu-id="4f734-115">绑定配置为使用 `wsHttpBinding` 默认为使用 `WSSecurity` 和客户端证书身份验证的标准。</span><span class="sxs-lookup"><span data-stu-id="4f734-115">The binding is configured with a standard `wsHttpBinding` that defaults to using `WSSecurity` and client certificate authentication.</span></span> <span data-ttu-id="4f734-116">服务行为指定对客户端 X.509 证书进行验证的“自定义”模式以及验证程序类的类型。</span><span class="sxs-lookup"><span data-stu-id="4f734-116">The service behavior specifies the Custom mode for validating client X.509 certificates along with the type of the validator class.</span></span> <span data-ttu-id="4f734-117">该行为还使用 serviceCertificate 元素指定服务器证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-117">The behavior also specifies the server certificate using the serviceCertificate element.</span></span> <span data-ttu-id="4f734-118">服务器证书必须包含与中相同的值 `SubjectName` `findValue` [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="4f734-118">The server certificate has to contain the same value for the `SubjectName` as the `findValue` in the [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md).</span></span>

```xml
  <system.serviceModel>
    <services>
      <service name="Microsoft.ServiceModel.Samples.CalculatorService"
               behaviorConfiguration="CalculatorServiceBehavior">
        <!-- use host/baseAddresses to configure base address -->
        <!-- provided by host -->
        <host>
          <baseAddresses>
            <add baseAddress =
                "http://localhost:8001/servicemodelsamples/service" />
          </baseAddresses>
        </host>
        <!-- use base address specified above, provide one endpoint -->
        <endpoint address="certificate"
               binding="wsHttpBinding"
               bindingConfiguration="Binding"
               contract="Microsoft.ServiceModel.Samples.ICalculator" />
      </service>
    </services>
    <bindings>
      <wsHttpBinding>
        <!-- X509 certificate binding -->
        <binding name="Binding">
          <security mode="Message">
            <message clientCredentialType="Certificate" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
    <behaviors>
      <serviceBehaviors>
        <behavior name="CalculatorServiceBehavior">
          <serviceDebug includeExceptionDetailInFaults ="true"/>
          <serviceCredentials>
            <!-- The serviceCredentials behavior allows one -->
            <!-- to specify authentication constraints on -->
            <!-- client certificates. -->
            <clientCertificate>
              <!-- Setting the certificateValidationMode to -->
              <!-- Custom means that if the custom -->
              <!-- X509CertificateValidator does NOT throw -->
              <!-- an exception, then the provided certificate -->
              <!-- will be trusted without performing any -->
              <!-- validation beyond that performed by the custom -->
              <!-- validator. The security implications of this -->
              <!-- setting should be carefully considered before -->
              <!-- using Custom in production code. -->
              <authentication
                 certificateValidationMode="Custom"
                 customCertificateValidatorType =
"Microsoft.ServiceModel.Samples.CustomX509CertificateValidator, service" />
            </clientCertificate>
            <!-- The serviceCredentials behavior allows one to -->
            <!-- define a service certificate. -->
            <!-- A service certificate is used by a client to -->
            <!-- authenticate the service and provide message -->
            <!-- protection. This configuration references the -->
            <!-- "localhost" certificate installed during the setup -->
            <!-- instructions. -->
            <serviceCertificate findValue="localhost"
                 storeLocation="LocalMachine"
                 storeName="My" x509FindType="FindBySubjectName" />
          </serviceCredentials>
        </behavior>
      </serviceBehaviors>
    </behaviors>
      </system.serviceModel>
```

<span data-ttu-id="4f734-119">客户端终结点配置由配置名称、服务终结点的绝对地址、绑定和协定组成。</span><span class="sxs-lookup"><span data-stu-id="4f734-119">The client endpoint configuration consists of a configuration name, an absolute address for the service endpoint, the binding, and the contract.</span></span> <span data-ttu-id="4f734-120">该客户端绑定是使用适当的模式和消息 `clientCredentialType` 配置的。</span><span class="sxs-lookup"><span data-stu-id="4f734-120">The client binding is configured with the appropriate mode and message `clientCredentialType`.</span></span>

```xml
<system.serviceModel>
    <client>
      <!-- X509 certificate based endpoint -->
      <endpoint name="Certificate"
        address=
        "http://localhost:8001/servicemodelsamples/service/certificate"
                binding="wsHttpBinding"
                bindingConfiguration="Binding"
                behaviorConfiguration="ClientCertificateBehavior"
                contract="Microsoft.ServiceModel.Samples.ICalculator">
      </endpoint>
    </client>
    <bindings>
        <wsHttpBinding>
            <!-- X509 certificate binding -->
            <binding name="Binding">
                <security mode="Message">
                    <message clientCredentialType="Certificate" />
               </security>
            </binding>
       </wsHttpBinding>
    </bindings>
    <behaviors>
      <endpointBehaviors>
        <behavior name="ClientCertificateBehavior">
          <clientCredentials>
            <serviceCertificate>
              <!-- Setting the certificateValidationMode to -->
              <!-- PeerOrChainTrust means that if the certificate -->
              <!-- is in the user's Trusted People store, then it -->
              <!-- is trusted without performing a validation of -->
              <!-- the certificate's issuer chain. -->
              <!-- This setting is used here for convenience so -->
              <!-- that the sample can be run without having to -->
              <!-- have certificates issued by a certification -->
              <!-- authority (CA). This setting is less secure -->
              <!-- than the default, ChainTrust. The security -->
              <!-- implications of this setting should be -->
              <!-- carefully considered before using -->
              <!-- PeerOrChainTrust in production code.-->
              <authentication
                  certificateValidationMode="PeerOrChainTrust" />
            </serviceCertificate>
          </clientCredentials>
        </behavior>
      </endpointBehaviors>
    </behaviors>
  </system.serviceModel>
```

<span data-ttu-id="4f734-121">客户端实现设置要使用的客户端证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-121">The client implementation sets the client certificate to use.</span></span>

```csharp
// Create a client with Certificate endpoint configuration
CalculatorClient client = new CalculatorClient("Certificate");
try
{
    client.ClientCredentials.ClientCertificate.SetCertificate(StoreLocation.CurrentUser, StoreName.My, X509FindType.FindBySubjectName, "test1");

    // Call the Add service operation.
    double value1 = 100.00D;
    double value2 = 15.99D;
    double result = client.Add(value1, value2);
    Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);

    // Call the Subtract service operation.
    value1 = 145.00D;
    value2 = 76.54D;
    result = client.Subtract(value1, value2);
    Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result);

    // Call the Multiply service operation.
    value1 = 9.00D;
    value2 = 81.25D;
    result = client.Multiply(value1, value2);
    Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result);

    // Call the Divide service operation.
    value1 = 22.00D;
    value2 = 7.00D;
    result = client.Divide(value1, value2);
    Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result);
    client.Close();
}
catch (TimeoutException e)
{
    Console.WriteLine("Call timed out : {0}", e.Message);
    client.Abort();
}
catch (CommunicationException e)
{
    Console.WriteLine("Call failed : {0}", e.Message);
    client.Abort();
}
catch (Exception e)
{
    Console.WriteLine("Call failed : {0}", e.Message);
    client.Abort();
}
```

<span data-ttu-id="4f734-122">此示例使用自定义 X509CertificateValidator 来验证证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-122">This sample uses a custom X509CertificateValidator to validate certificates.</span></span> <span data-ttu-id="4f734-123">此示例实现从 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 派生的 CustomX509CertificateValidator。</span><span class="sxs-lookup"><span data-stu-id="4f734-123">The sample implements CustomX509CertificateValidator, derived from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="4f734-124">有关更多信息，请参见有关 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 的文档。</span><span class="sxs-lookup"><span data-stu-id="4f734-124">See documentation about <xref:System.IdentityModel.Selectors.X509CertificateValidator> for more information.</span></span> <span data-ttu-id="4f734-125">这个特定的自定义验证程序示例实现了 Validate 方法，可以接受自行颁发的任何 X.509 证书，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="4f734-125">This particular custom validator sample implements the Validate method to accept any X.509 certificate that is self-issued as shown in the following code.</span></span>

```csharp
public class CustomX509CertificateValidator : X509CertificateValidator
{
  public override void Validate ( X509Certificate2 certificate )
  {
   // Only accept self-issued certificates
   if (certificate.Subject != certificate.Issuer)
     throw new Exception("Certificate is not self-issued");
   }
}
```

 <span data-ttu-id="4f734-126">在服务代码中实现验证程序后，必须通知服务主机关于要使用的验证程序实例的信息。</span><span class="sxs-lookup"><span data-stu-id="4f734-126">Once the validator is implemented in service code, the service host must be informed about the validator instance to use.</span></span> <span data-ttu-id="4f734-127">这是使用以下代码完成的。</span><span class="sxs-lookup"><span data-stu-id="4f734-127">This is done using the following code.</span></span>

```csharp
serviceHost.Credentials.ClientCertificate.Authentication.CertificateValidationMode = X509CertificateValidationMode.Custom;
serviceHost.Credentials.ClientCertificate.Authentication.CustomCertificateValidator = new CustomX509CertificateValidator();
```

 <span data-ttu-id="4f734-128">或者，您可以在如下配置中执行相同的操作。</span><span class="sxs-lookup"><span data-stu-id="4f734-128">Or you can do the same thing in configuration as follows.</span></span>

```xml
<behaviors>
    <serviceBehaviors>
     <behavior name="CalculatorServiceBehavior">
       ...
   <serviceCredentials>
    <!--The serviceCredentials behavior allows one to specify -->
    <!--authentication constraints on client certificates.-->
    <clientCertificate>
    <!-- Setting the certificateValidationMode to Custom means -->
    <!--that if the custom X509CertificateValidator does NOT -->
    <!--throw an exception, then the provided certificate will -->
    <!--be trusted without performing any validation beyond that -->
    <!--performed by the custom validator. The security -->
    <!--implications of this setting should be carefully -->
    <!--considered before using Custom in production code. -->
    <authentication certificateValidationMode="Custom"
       customCertificateValidatorType =
"Microsoft.ServiceModel.Samples. CustomX509CertificateValidator, service" />
   </clientCertificate>
   </serviceCredentials>
   ...
  </behavior>
 </serviceBehaviors>
</behaviors>
```

<span data-ttu-id="4f734-129">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="4f734-129">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="4f734-130">客户端应成功地调用所有方法。</span><span class="sxs-lookup"><span data-stu-id="4f734-130">The client should successfully call all the methods.</span></span> <span data-ttu-id="4f734-131">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="4f734-131">Press ENTER in the client window to shut down the client.</span></span>

## <a name="setup-batch-file"></a><span data-ttu-id="4f734-132">设置批处理文件</span><span class="sxs-lookup"><span data-stu-id="4f734-132">Setup Batch File</span></span>

<span data-ttu-id="4f734-133">通过运行此示例随附的 Setup.bat 批处理文件，可以用相关的证书将服务器配置为运行需要基于服务器证书的安全性的自承载应用程序。</span><span class="sxs-lookup"><span data-stu-id="4f734-133">The Setup.bat batch file included with this sample allows you to configure the server with relevant certificates to run a self-hosted application that requires server certificate-based security.</span></span> <span data-ttu-id="4f734-134">必须修改此批处理文件，以便跨计算机或在非承载情况下工作。</span><span class="sxs-lookup"><span data-stu-id="4f734-134">This batch file must be modified to work across computers or to work in a non-hosted case.</span></span>

<span data-ttu-id="4f734-135">下面提供了批处理文件不同节的简要概述，以便可以修改批处理文件从而在相应的配置中运行：</span><span class="sxs-lookup"><span data-stu-id="4f734-135">The following provides a brief overview of the different sections of the batch files so that they can be modified to run in the appropriate configuration:</span></span>

- <span data-ttu-id="4f734-136">创建服务器证书：</span><span class="sxs-lookup"><span data-stu-id="4f734-136">Creating the server certificate:</span></span>

     <span data-ttu-id="4f734-137">Setup.bat 批处理文件中的以下行创建将要使用的服务器证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-137">The following lines from the Setup.bat batch file create the server certificate to be used.</span></span> <span data-ttu-id="4f734-138">%SERVER_NAME% 变量指定服务器名称。</span><span class="sxs-lookup"><span data-stu-id="4f734-138">The %SERVER_NAME% variable specifies the server name.</span></span> <span data-ttu-id="4f734-139">更改此变量可以指定您自己的服务器名称。</span><span class="sxs-lookup"><span data-stu-id="4f734-139">Change this variable to specify your own server name.</span></span> <span data-ttu-id="4f734-140">默认值为 localhost。</span><span class="sxs-lookup"><span data-stu-id="4f734-140">The default value is localhost.</span></span>

    ```bash
    echo ************
    echo Server cert setup starting
    echo %SERVER_NAME%
    echo ************
    echo making server cert
    echo ************
    makecert.exe -sr LocalMachine -ss MY -a sha1 -n CN=%SERVER_NAME% -sky exchange -pe
    ```

- <span data-ttu-id="4f734-141">将服务器证书安装到客户端的受信任证书存储区中：</span><span class="sxs-lookup"><span data-stu-id="4f734-141">Installing the server certificate into client's trusted certificate store:</span></span>

     <span data-ttu-id="4f734-142">Setup.bat 批处理文件中的以下行将服务器证书复制到客户端的受信任的人的存储区中。</span><span class="sxs-lookup"><span data-stu-id="4f734-142">The following lines in the Setup.bat batch file copy the server certificate into the client trusted people store.</span></span> <span data-ttu-id="4f734-143">因为客户端系统不隐式信任 Makecert.exe 生成的证书，所以需要执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="4f734-143">This step is required since certificates generated by Makecert.exe are not implicitly trusted by the client system.</span></span> <span data-ttu-id="4f734-144">如果您已经拥有一个证书，该证书来源于客户端的受信任根证书（例如由 Microsoft 颁发的证书），则不需要执行使用服务器证书填充客户端证书存储区这一步骤。</span><span class="sxs-lookup"><span data-stu-id="4f734-144">If you already have a certificate that is rooted in a client trusted root certificate—for example, a Microsoft issued certificate—this step of populating the client certificate store with the server certificate is not required.</span></span>

    ```bash
    certmgr.exe -add -r LocalMachine -s My -c -n %SERVER_NAME% -r CurrentUser -s TrustedPeople
    ```

- <span data-ttu-id="4f734-145">创建客户端证书：</span><span class="sxs-lookup"><span data-stu-id="4f734-145">Creating the client certificate:</span></span>

     <span data-ttu-id="4f734-146">Setup.bat 批处理文件中的以下行创建将要使用的客户端证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-146">The following lines from the Setup.bat batch file create the client certificate to be used.</span></span> <span data-ttu-id="4f734-147">%USER_NAME% 变量指定客户端名称。</span><span class="sxs-lookup"><span data-stu-id="4f734-147">The %USER_NAME% variable specifies the client name.</span></span> <span data-ttu-id="4f734-148">此值设置为“test1”，因为这是客户端代码查找的名称。</span><span class="sxs-lookup"><span data-stu-id="4f734-148">This value is set to "test1" because this is the name the client code looks for.</span></span> <span data-ttu-id="4f734-149">如果更改 %USER_NAME% 的值，必须更改 Client.cs 源文件中对应的值并重新生成客户端。</span><span class="sxs-lookup"><span data-stu-id="4f734-149">If you change the value of %USER_NAME% you must change the corresponding value in the Client.cs source file and rebuild the client.</span></span>

     <span data-ttu-id="4f734-150">证书存储在 CurrentUser 存储位置下的 My（个人）存储区中。</span><span class="sxs-lookup"><span data-stu-id="4f734-150">The certificate is stored in My (Personal) store under the CurrentUser store location.</span></span>

    ```bash
    echo ************
    echo Client cert setup starting
    echo %USER_NAME%
    echo ************
    echo making client cert
    echo ************
    makecert.exe -sr CurrentUser -ss MY -a sha1 -n CN=%USER_NAME% -sky exchange -pe
    ```

- <span data-ttu-id="4f734-151">将客户端证书安装到服务器的受信任证书存储区中：</span><span class="sxs-lookup"><span data-stu-id="4f734-151">Installing the client certificate into server's trusted certificate store:</span></span>

     <span data-ttu-id="4f734-152">Setup.bat 批处理文件中的以下行将客户端证书复制到受信任的人的存储区中。</span><span class="sxs-lookup"><span data-stu-id="4f734-152">The following lines in the Setup.bat batch file copy the client certificate into the trusted people store.</span></span> <span data-ttu-id="4f734-153">因为服务器系统不隐式信任 Makecert.exe 生成的证书，所以需要执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="4f734-153">This step is required because certificates generated by Makecert.exe are not implicitly trusted by the server system.</span></span> <span data-ttu-id="4f734-154">如果您已经拥有一个证书，该证书来源于受信任的根证书（例如由 Microsoft 颁发的证书），则不需要执行使用客户端证书填充服务器证书存储区这一步骤。</span><span class="sxs-lookup"><span data-stu-id="4f734-154">If you already have a certificate that is rooted in a trusted root certificate—for example, a Microsoft issued certificate—this step of populating the server certificate store with the client certificate is not required.</span></span>

    ```bash
    certmgr.exe -add -r CurrentUser -s My -c -n %USER_NAME% -r LocalMachine -s TrustedPeople
    ```

#### <a name="to-set-up-and-build-the-sample"></a><span data-ttu-id="4f734-155">设置和生成示例</span><span class="sxs-lookup"><span data-stu-id="4f734-155">To set up and build the sample</span></span>

1. <span data-ttu-id="4f734-156">若要生成解决方案，请按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="4f734-156">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

2. <span data-ttu-id="4f734-157">若要用单一计算机配置或跨计算机配置来运行示例，请按照下列说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="4f734-157">To run the sample in a single- or cross-computer configuration, use the following instructions.</span></span>

#### <a name="to-run-the-sample-on-the-same-computer"></a><span data-ttu-id="4f734-158">在同一计算机上运行示例</span><span class="sxs-lookup"><span data-stu-id="4f734-158">To run the sample on the same computer</span></span>

1. <span data-ttu-id="4f734-159">在使用管理员特权打开的 Visual Studio 2012 命令提示符下，从示例安装文件夹运行 Setup.bat。</span><span class="sxs-lookup"><span data-stu-id="4f734-159">Run Setup.bat from the sample install folder inside a Visual Studio 2012 command prompt opened with administrator privileges.</span></span> <span data-ttu-id="4f734-160">这将安装运行示例所需的所有证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-160">This installs all the certificates required for running the sample.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4f734-161">Setup.bat 批处理文件设计为在 Visual Studio 2012 命令提示符下运行。</span><span class="sxs-lookup"><span data-stu-id="4f734-161">The Setup.bat batch file is designed to be run from a Visual Studio 2012 Command Prompt.</span></span> <span data-ttu-id="4f734-162">在 Visual Studio 2012 命令提示符下设置的 PATH 环境变量指向包含 Setup.bat 脚本所需的可执行文件的目录。</span><span class="sxs-lookup"><span data-stu-id="4f734-162">The PATH environment variable set within the Visual Studio 2012 Command Prompt points to the directory that contains executables required by the Setup.bat script.</span></span>

2. <span data-ttu-id="4f734-163">启动 service\bin 中的 Service.exe。</span><span class="sxs-lookup"><span data-stu-id="4f734-163">Launch Service.exe from service\bin.</span></span>

3. <span data-ttu-id="4f734-164">启动 \client\bin 中的 Client.exe。</span><span class="sxs-lookup"><span data-stu-id="4f734-164">Launch Client.exe from \client\bin.</span></span> <span data-ttu-id="4f734-165">客户端活动将显示在客户端控制台应用程序上。</span><span class="sxs-lookup"><span data-stu-id="4f734-165">Client activity is displayed on the client console application.</span></span>

4. <span data-ttu-id="4f734-166">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="4f734-166">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>

#### <a name="to-run-the-sample-across-computers"></a><span data-ttu-id="4f734-167">跨计算机运行示例</span><span class="sxs-lookup"><span data-stu-id="4f734-167">To run the sample across computers</span></span>

1. <span data-ttu-id="4f734-168">在服务计算机上创建目录。</span><span class="sxs-lookup"><span data-stu-id="4f734-168">Create a directory on the service computer.</span></span>

2. <span data-ttu-id="4f734-169">从 \service\bin 中将服务程序文件复制到服务计算机上的虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4f734-169">Copy the service program files from \service\bin to the virtual directory on the service computer.</span></span> <span data-ttu-id="4f734-170">另外，将 Setup.bat、Cleanup.bat、GetComputerName.vbs 和 ImportClientCert.bat 文件复制到服务计算机上。</span><span class="sxs-lookup"><span data-stu-id="4f734-170">Also copy the Setup.bat, Cleanup.bat, GetComputerName.vbs and ImportClientCert.bat files to the service computer.</span></span>

3. <span data-ttu-id="4f734-171">在客户端计算机上为这些客户端二进制文件创建一个目录。</span><span class="sxs-lookup"><span data-stu-id="4f734-171">Create a directory on the client computer for the client binaries.</span></span>

4. <span data-ttu-id="4f734-172">将客户端程序文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="4f734-172">Copy the client program files to the client directory on the client computer.</span></span> <span data-ttu-id="4f734-173">另外，将 Setup.bat、Cleanup.bat 和 ImportServiceCert.bat 文件复制到客户端上。</span><span class="sxs-lookup"><span data-stu-id="4f734-173">Also copy the Setup.bat, Cleanup.bat, and ImportServiceCert.bat files to the client.</span></span>

5. <span data-ttu-id="4f734-174">在服务器上， `setup.bat service` 在使用管理员特权打开的 Visual Studio 开发人员命令提示中运行。</span><span class="sxs-lookup"><span data-stu-id="4f734-174">On the server, run `setup.bat service` in a Developer Command Prompt for Visual Studio opened with administrator privileges.</span></span> <span data-ttu-id="4f734-175">使用参数运行将使用 `setup.bat` `service` 计算机的完全限定的域名创建一个服务证书，并将服务证书导出到名为的文件。</span><span class="sxs-lookup"><span data-stu-id="4f734-175">Running `setup.bat` with the `service` argument creates a service certificate with the fully-qualified domain name of the computer and exports the service certificate to a file named Service.cer.</span></span>

6. <span data-ttu-id="4f734-176">编辑 Service.exe.config，以反映) 的属性中 (新的证书名称，该名称与 `findValue` [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md) 计算机的完全限定域名相同。</span><span class="sxs-lookup"><span data-stu-id="4f734-176">Edit Service.exe.config to reflect the new certificate name (in the `findValue` attribute in the [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md)) which is the same as the fully-qualified domain name of the computer.</span></span> <span data-ttu-id="4f734-177">还要将元素中的计算机名 \<service> / \<baseAddresses> 从 localhost 更改为服务计算机的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="4f734-177">Also change the computer name in the \<service>/\<baseAddresses> element from localhost to fully qualified name of your service computer.</span></span>

7. <span data-ttu-id="4f734-178">将服务目录中的 Service.cer 文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="4f734-178">Copy the Service.cer file from the service directory to the client directory on the client computer.</span></span>

8. <span data-ttu-id="4f734-179">在客户端上， `setup.bat client` 在使用管理员特权打开的 Visual Studio 开发人员命令提示中运行。</span><span class="sxs-lookup"><span data-stu-id="4f734-179">On the client, run `setup.bat client` in a Developer Command Prompt for Visual Studio opened with administrator privileges.</span></span> <span data-ttu-id="4f734-180">如果使用 `setup.bat` 自变量运行 `client`，则会创建一个名为 client.com 的客户端证书，并将此客户端证书导出到名为 Client.cer 的文件中。</span><span class="sxs-lookup"><span data-stu-id="4f734-180">Running `setup.bat` with the `client` argument creates a client certificate named client.com and exports the client certificate to a file named Client.cer.</span></span>

9. <span data-ttu-id="4f734-181">在客户端计算机上的 Client.exe.config 文件中，更改终结点的地址值，使其与服务的新地址相匹配。</span><span class="sxs-lookup"><span data-stu-id="4f734-181">In the Client.exe.config file on the client computer, change the address value of the endpoint to match the new address of your service.</span></span> <span data-ttu-id="4f734-182">通过用服务器的完全限定域名替换 localhost 来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="4f734-182">Do this by replacing localhost with the fully-qualified domain name of the server.</span></span>

10. <span data-ttu-id="4f734-183">将客户端目录中的 Client.cer 文件复制到服务器上的服务目录中。</span><span class="sxs-lookup"><span data-stu-id="4f734-183">Copy the Client.cer file from the client directory to the service directory on the server.</span></span>

11. <span data-ttu-id="4f734-184">在客户端上，在使用管理员特权打开的 Visual Studio 开发人员命令提示中运行 ImportServiceCert.bat。</span><span class="sxs-lookup"><span data-stu-id="4f734-184">On the client, run ImportServiceCert.bat in a Developer Command Prompt for Visual Studio opened with administrator privileges.</span></span> <span data-ttu-id="4f734-185">这会将 Service.cer 文件中的服务证书导入 CurrentUser – TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="4f734-185">This imports the service certificate from the Service.cer file into the CurrentUser - TrustedPeople store.</span></span>

12. <span data-ttu-id="4f734-186">在服务器上，在使用管理员特权打开的 Visual Studio 开发人员命令提示中运行 ImportClientCert.bat。</span><span class="sxs-lookup"><span data-stu-id="4f734-186">On the server, run ImportClientCert.bat in a Developer Command Prompt for Visual Studio opened with administrator privileges.</span></span> <span data-ttu-id="4f734-187">这会将 Client.cer 文件中的客户端证书导入 LocalMachine - TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="4f734-187">This imports the client certificate from the Client.cer file into the LocalMachine - TrustedPeople store.</span></span>

13. <span data-ttu-id="4f734-188">在服务器计算机上，从命令提示窗口中启动 Service.exe。</span><span class="sxs-lookup"><span data-stu-id="4f734-188">On the server computer, launch Service.exe from the command prompt window.</span></span>

14. <span data-ttu-id="4f734-189">在客户端计算机上，从命令提示窗口中启动 Client.exe。</span><span class="sxs-lookup"><span data-stu-id="4f734-189">On the client computer, launch Client.exe from a command prompt window.</span></span> <span data-ttu-id="4f734-190">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="4f734-190">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>

#### <a name="to-clean-up-after-the-sample"></a><span data-ttu-id="4f734-191">运行示例后进行清理</span><span class="sxs-lookup"><span data-stu-id="4f734-191">To clean up after the sample</span></span>

1. <span data-ttu-id="4f734-192">运行完示例后运行示例文件夹中的 Cleanup.bat。</span><span class="sxs-lookup"><span data-stu-id="4f734-192">Run Cleanup.bat in the samples folder once you have finished running the sample.</span></span> <span data-ttu-id="4f734-193">这将从证书存储区中移除服务器和客户端证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-193">This removes the server and client certificates from the certificate store.</span></span>

> [!NOTE]
> <span data-ttu-id="4f734-194">此脚本不会在跨计算机运行此示例时移除客户端上的服务证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-194">This script does not remove service certificates on a client when running this sample across computers.</span></span> <span data-ttu-id="4f734-195">如果你已运行 Windows Communication Foundation 跨计算机使用证书 (WCF) 示例，请确保清除已安装在 CurrentUser-TrustedPeople 存储中的服务证书。</span><span class="sxs-lookup"><span data-stu-id="4f734-195">If you have run Windows Communication Foundation (WCF) samples that use certificates across computers, be sure to clear the service certificates that have been installed in the CurrentUser - TrustedPeople store.</span></span> <span data-ttu-id="4f734-196">为此，请使用以下命令：`certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>`，例如：`certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`。</span><span class="sxs-lookup"><span data-stu-id="4f734-196">To do this, use the following command: `certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>` For example: `certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`.</span></span>
