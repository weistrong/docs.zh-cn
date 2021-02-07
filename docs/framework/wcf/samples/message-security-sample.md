---
description: 了解详细信息：消息安全示例
title: 消息安全示例
ms.date: 03/30/2017
ms.assetid: 82444166-6288-493a-85d4-85f43f134d19
ms.openlocfilehash: adec9df3b2a3b5ba022ec2123a8d90d85869246b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752296"
---
# <a name="message-security-sample"></a><span data-ttu-id="54fce-103">消息安全示例</span><span class="sxs-lookup"><span data-stu-id="54fce-103">Message Security Sample</span></span>

<span data-ttu-id="54fce-104">此示例演示如何实现使用 `basicHttpBinding` 和消息安全性的应用程序。</span><span class="sxs-lookup"><span data-stu-id="54fce-104">This sample demonstrates how to implement an application that uses the `basicHttpBinding` and message security.</span></span> <span data-ttu-id="54fce-105">此示例基于实现计算器服务的 [入门](getting-started-sample.md) 。</span><span class="sxs-lookup"><span data-stu-id="54fce-105">This sample is based on the [Getting Started](getting-started-sample.md) that implements a calculator service.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="54fce-106">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="54fce-106">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="54fce-107">`basicHttpBinding` 的安全模式可以设置为下列值：`Message`、`Transport`、`TransportWithMessageCredential`、`TransportCredentialOnly` 和 `None`。</span><span class="sxs-lookup"><span data-stu-id="54fce-107">The security mode of `basicHttpBinding` can be set to the following values: `Message`, `Transport`, `TransportWithMessageCredential`, `TransportCredentialOnly` and `None`.</span></span> <span data-ttu-id="54fce-108">在下面的示例服务 App.config 文件中，终结点定义将指定 `basicHttpBinding` 并引用名为 `Binding1` 的绑定配置，如下面的示例配置中所示：</span><span class="sxs-lookup"><span data-stu-id="54fce-108">In the following sample service App.config file, the endpoint definition specifies the `basicHttpBinding` and references a binding configuration named `Binding1`, as shown in the following sample configuration:</span></span>  
  
```xml  
<system.serviceModel>  
  <services>  
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"  
             behaviorConfiguration="CalculatorServiceBehavior">  
     <!-- This endpoint is exposed at the base address provided by -->  
     <!-- host: http://localhost:8000/ServiceModelSamples/service.-->  
     <endpoint address=""  
               binding="basicHttpBinding"  
               bindingConfiguration="Binding1"
               contract="Microsoft.ServiceModel.Samples.ICalculator" />  
    </service>  
  </services>  
  ...  
</system.serviceModel>  
```  
  
 <span data-ttu-id="54fce-109">绑定配置将的 `mode` 属性设置 [\<security>](../../configure-apps/file-schema/wcf/security-of-basichttpbinding.md) 为 `Message` ，并将的属性设置为， `clientCredentialType` [\<message>](../../configure-apps/file-schema/wcf/message-of-basichttpbinding.md) `Certificate` 如下面的示例配置所示：</span><span class="sxs-lookup"><span data-stu-id="54fce-109">The binding configuration sets the `mode` attribute of the [\<security>](../../configure-apps/file-schema/wcf/security-of-basichttpbinding.md) to `Message` and sets the `clientCredentialType` attribute of the [\<message>](../../configure-apps/file-schema/wcf/message-of-basichttpbinding.md) to `Certificate` as shown in the following sample configuration:</span></span>  
  
```xml  
<bindings>  
  <basicHttpBinding>  
    <!--   
        This configuration defines the SecurityMode as Message and   
        the clientCredentialType as Certificate.  
        -->  
    <binding name="Binding1" >  
      <security mode = "Message">  
        <message clientCredentialType="Certificate"/>  
      </security>  
    </binding>  
  </basicHttpBinding>  
</bindings>  
```  
  
 <span data-ttu-id="54fce-110">服务用于向客户端验证自己身份的证书是在配置文件的 behaviors 节中 `serviceCredentials` 元素的下面设置的。</span><span class="sxs-lookup"><span data-stu-id="54fce-110">The certificate that the service uses to authenticate itself to the client is set in the behaviors section of the configuration file under the `serviceCredentials` element.</span></span> <span data-ttu-id="54fce-111">应用于证书（客户端使用该证书向服务验证自己的身份）的验证模式也是在 behaviors 节中 `clientCertificate` 元素的下面设置的。</span><span class="sxs-lookup"><span data-stu-id="54fce-111">The validation mode that applies to the certificate that the client uses to authenticate itself to the service is also set in the behaviors section under the `clientCertificate` element.</span></span>  
  
```xml  
<!--For debugging purposes, set the includeExceptionDetailInFaults attribute to true.-->  
<behaviors>  
  <serviceBehaviors>  
    <behavior name="CalculatorServiceBehavior">  
      <serviceMetadata httpGetEnabled="True"/>  
      <serviceDebug includeExceptionDetailInFaults="False" />  
      <!--The serviceCredentials behavior allows one to define a -->  
      <!--service certificate. A service certificate is used by a -->  
      <!--client to authenticate the service and provide message -->  
      <!-- protection. This configuration references the "localhost"-->  
      <!--certificate installed during the setup instructions. -->  
      <serviceCredentials>  
        <serviceCertificate findValue="localhost"  
               storeLocation="LocalMachine"
               storeName="My" x509FindType="FindBySubjectName" />  
        <clientCertificate>  
          <!-- Setting the certificateValidationMode to -->  
          <!-- PeerOrChainTrust means that if the certificate -->  
          <!--is in the user's Trusted People store, then it is -->  
          <!-- trusted without performing a validation of the -->  
          <!-- certificate's issuer chain. This setting is used -->  
          <!-- here for convenience so that the sample can be run -->  
          <!-- without having to have certificates issued by a -->  
          <!-- certification authority (CA). -->  
          <!-- This setting is less secure than the default, -->  
          <!-- ChainTrust. The security implications of this -->  
          <!-- setting should be carefully considered before using -->  
          <!-- PeerOrChainTrust in production code. -->  
          <authentication
                       certificateValidationMode="PeerOrChainTrust" />  
        </clientCertificate>  
      </serviceCredentials>  
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
 <span data-ttu-id="54fce-112">在客户端配置文件中指定同样的绑定和安全详细信息。</span><span class="sxs-lookup"><span data-stu-id="54fce-112">The same binding and security details are specified in the client configuration file.</span></span>  
  
 <span data-ttu-id="54fce-113">通过使用下面的代码，可以使调用方的标识显示在服务控制台窗口中：</span><span class="sxs-lookup"><span data-stu-id="54fce-113">The identity of the caller is displayed in the service console window by using the following code:</span></span>  

```csharp
Console.WriteLine("Called by {0}", ServiceSecurityContext.Current.PrimaryIdentity.Name);  
```

 <span data-ttu-id="54fce-114">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="54fce-114">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="54fce-115">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="54fce-115">Press ENTER in the client window to shut down the client.</span></span>  
  
```console
Add(100,15.99) = 115.99  
Subtract(145,76.54) = 68.46  
Multiply(9,81.25) = 731.25  
Divide(22,7) = 3.14285714285714  
Press <ENTER> to terminate client.  
```  
  
### <a name="to-set-up-and-build-the-sample"></a><span data-ttu-id="54fce-116">设置和生成示例</span><span class="sxs-lookup"><span data-stu-id="54fce-116">To set up and build the sample</span></span>  
  
1. <span data-ttu-id="54fce-117">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="54fce-117">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="54fce-118">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="54fce-118">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
### <a name="to-run-the-sample-on-the-same-machine"></a><span data-ttu-id="54fce-119">在同一计算机上运行示例</span><span class="sxs-lookup"><span data-stu-id="54fce-119">To run the sample on the same machine</span></span>  
  
1. <span data-ttu-id="54fce-120">运行示例安装文件夹中的 Setup.bat。</span><span class="sxs-lookup"><span data-stu-id="54fce-120">Run Setup.bat from the sample install folder.</span></span> <span data-ttu-id="54fce-121">这将安装运行示例所需的所有证书。</span><span class="sxs-lookup"><span data-stu-id="54fce-121">This installs all the certificates required for running the sample.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="54fce-122">Setup.bat 批处理文件设计为通过 Windows SDK 命令提示运行。</span><span class="sxs-lookup"><span data-stu-id="54fce-122">The Setup.bat batch file is designed to be run from a Windows SDK Command Prompt.</span></span> <span data-ttu-id="54fce-123">这要求 MSSDK 环境变量指向 SDK 的安装目录。</span><span class="sxs-lookup"><span data-stu-id="54fce-123">It requires that the MSSDK environment variable point to the directory where the SDK is installed.</span></span> <span data-ttu-id="54fce-124">将在 Windows SDK 命令提示中自动设置此环境变量。</span><span class="sxs-lookup"><span data-stu-id="54fce-124">This environment variable is automatically set within a Windows SDK Command Prompt.</span></span>  
  
2. <span data-ttu-id="54fce-125">从 \service\bin 运行服务应用程序。</span><span class="sxs-lookup"><span data-stu-id="54fce-125">Run the service application from \service\bin.</span></span>  
  
3. <span data-ttu-id="54fce-126">从 \client\bin 运行客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="54fce-126">Run the client application from \client\bin.</span></span> <span data-ttu-id="54fce-127">客户端活动将显示在客户端控制台应用程序上。</span><span class="sxs-lookup"><span data-stu-id="54fce-127">Client activity is displayed on the client console application.</span></span>  
  
4. <span data-ttu-id="54fce-128">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="54fce-128">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
5. <span data-ttu-id="54fce-129">在运行完该示例后运行 Cleanup.bat 移除证书。</span><span class="sxs-lookup"><span data-stu-id="54fce-129">Remove the certificates by running Cleanup.bat when you have finished with the sample.</span></span> <span data-ttu-id="54fce-130">其他安全示例使用相同的证书。</span><span class="sxs-lookup"><span data-stu-id="54fce-130">Other security samples use the same certificates.</span></span>  
  
### <a name="to-run-the-sample-across-machines"></a><span data-ttu-id="54fce-131">跨计算机运行示例</span><span class="sxs-lookup"><span data-stu-id="54fce-131">To run the sample across machines</span></span>  
  
1. <span data-ttu-id="54fce-132">在服务计算机上为服务二进制文件创建一个目录。</span><span class="sxs-lookup"><span data-stu-id="54fce-132">Create a directory on the service machine for the service binaries.</span></span>  
  
2. <span data-ttu-id="54fce-133">将服务程序文件复制到服务器上的服务目录中。</span><span class="sxs-lookup"><span data-stu-id="54fce-133">Copy the service program files to the service directory on the server.</span></span> <span data-ttu-id="54fce-134">另外，将 Setup.bat、Cleanup.bat 和 ImportClientCert.bat 文件复制到服务器上。</span><span class="sxs-lookup"><span data-stu-id="54fce-134">Also copy the Setup.bat, Cleanup.bat, and ImportClientCert.bat files to the server.</span></span>  
  
3. <span data-ttu-id="54fce-135">在客户端计算机上为这些客户端二进制文件创建一个目录。</span><span class="sxs-lookup"><span data-stu-id="54fce-135">Create a directory on the client machine for the client binaries.</span></span>  
  
4. <span data-ttu-id="54fce-136">将客户端程序文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="54fce-136">Copy the client program files to the client directory on the client machine.</span></span> <span data-ttu-id="54fce-137">另外，将 Setup.bat、Cleanup.bat 和 ImportServiceCert.bat 文件复制到客户端上。</span><span class="sxs-lookup"><span data-stu-id="54fce-137">Also copy the Setup.bat, Cleanup.bat, and ImportServiceCert.bat files to the client.</span></span>  
  
5. <span data-ttu-id="54fce-138">在服务器上运行 `setup.bat service`。</span><span class="sxs-lookup"><span data-stu-id="54fce-138">On the server, run `setup.bat service`.</span></span> <span data-ttu-id="54fce-139">`setup.bat`使用参数运行将 `service` 使用计算机的完全限定的域名创建一个服务证书，并将服务证书导出到名为 .cer 的文件中。</span><span class="sxs-lookup"><span data-stu-id="54fce-139">Running `setup.bat` with the `service` argument creates a service certificate with the fully-qualified domain name of the machine and exports the service certificate to a file named Service.cer.</span></span>  
  
6. <span data-ttu-id="54fce-140">编辑 Service.exe.config，以反映元素) 的属性中 (新的证书名称，该名称与 `findValue` [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md) 计算机的完全限定域名相同。</span><span class="sxs-lookup"><span data-stu-id="54fce-140">Edit Service.exe.config to reflect the new certificate name (in the `findValue` attribute in the [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md) element) which is the same as the fully-qualified domain name of the machine.</span></span> <span data-ttu-id="54fce-141">还要更改基址的值以指定一个完全限定的计算机名（而不是 localhost）。`.`</span><span class="sxs-lookup"><span data-stu-id="54fce-141">Also change the value of the base address to specify a fully-qualified machine name instead of localhost`.`</span></span>  
  
7. <span data-ttu-id="54fce-142">将服务目录中的 Service.cer 文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="54fce-142">Copy the Service.cer file from the service directory to the client directory on the client machine.</span></span>  
  
8. <span data-ttu-id="54fce-143">在客户端上，运行 `setup.bat client`。</span><span class="sxs-lookup"><span data-stu-id="54fce-143">On the client, run `setup.bat client`.</span></span> <span data-ttu-id="54fce-144">如果使用 `setup.bat` 自变量运行 `client`，则会创建一个名为 client.com 的客户端证书，并将此客户端证书导出到名为 Client.cer 的文件中。</span><span class="sxs-lookup"><span data-stu-id="54fce-144">Running `setup.bat` with the `client` argument creates a client certificate named client.com and exports the client certificate to a file named Client.cer.</span></span>  
  
9. <span data-ttu-id="54fce-145">在客户端计算机上的 Client.exe.config 文件中，更改终结点的地址值，使其与服务的新地址相匹配。</span><span class="sxs-lookup"><span data-stu-id="54fce-145">In the Client.exe.config file on the client machine, change the address value of the endpoint to match the new address of your service.</span></span> <span data-ttu-id="54fce-146">通过使用服务器的完全限定域名替换 localhost 来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="54fce-146">You do this by replacing localhost with the fully-qualified domain name of the server.</span></span> <span data-ttu-id="54fce-147">还将 `findValue` 的属性更改 [\<defaultCertificate>](../../configure-apps/file-schema/wcf/defaultcertificate-element.md) 为新的服务证书名称，该名称是服务器的完全限定域名。</span><span class="sxs-lookup"><span data-stu-id="54fce-147">Also change the `findValue` attribute of the [\<defaultCertificate>](../../configure-apps/file-schema/wcf/defaultcertificate-element.md) to the new service certificate name which is the fully-qualified domain name of the server.</span></span>  
  
10. <span data-ttu-id="54fce-148">将客户端目录中的 Client.cer 文件复制到服务器上的服务目录中。</span><span class="sxs-lookup"><span data-stu-id="54fce-148">Copy the Client.cer file from the client directory to the service directory on the server.</span></span>  
  
11. <span data-ttu-id="54fce-149">在客户端上，运行 ImportServiceCert.bat。</span><span class="sxs-lookup"><span data-stu-id="54fce-149">On the client, run ImportServiceCert.bat.</span></span> <span data-ttu-id="54fce-150">这会将 Service.cer 文件中的服务证书导入 CurrentUser – TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="54fce-150">This imports the service certificate from the Service.cer file into the CurrentUser - TrustedPeople store.</span></span>  
  
12. <span data-ttu-id="54fce-151">在服务器上，运行 ImportClientCert.bat，这会将 Client.cer 文件中的客户端证书导入 LocalMachine - TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="54fce-151">On the server, run ImportClientCert.bat, This imports the client certificate from the Client.cer file into the LocalMachine - TrustedPeople store.</span></span>  
  
13. <span data-ttu-id="54fce-152">在服务计算机上，在命令提示符下运行 Service.exe。</span><span class="sxs-lookup"><span data-stu-id="54fce-152">On the service machine, run Service.exe from a command prompt.</span></span>  
  
14. <span data-ttu-id="54fce-153">在客户端计算机上，从命令提示符窗口中启动 Client.exe。</span><span class="sxs-lookup"><span data-stu-id="54fce-153">On the client machine, launch Client.exe from a command prompt window.</span></span>  
  
    1. <span data-ttu-id="54fce-154">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="54fce-154">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
### <a name="to-clean-up-after-the-sample"></a><span data-ttu-id="54fce-155">运行示例后进行清理</span><span class="sxs-lookup"><span data-stu-id="54fce-155">To clean up after the sample</span></span>  
  
- <span data-ttu-id="54fce-156">运行完示例后运行示例文件夹中的 Cleanup.bat。</span><span class="sxs-lookup"><span data-stu-id="54fce-156">Run Cleanup.bat in the samples folder once you have finished running the sample.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="54fce-157">此脚本不会在跨计算机运行此示例时移除客户端上的服务证书。</span><span class="sxs-lookup"><span data-stu-id="54fce-157">This script does not remove service certificates on a client when running this sample across machines.</span></span> <span data-ttu-id="54fce-158">如果已运行 Windows Communication Foundation 跨计算机使用证书 (WCF) 示例，请确保清除已安装在 CurrentUser-TrustedPeople 存储中的服务证书。</span><span class="sxs-lookup"><span data-stu-id="54fce-158">If you have run Windows Communication Foundation (WCF) samples that use certificates across machines, be sure to clear the service certificates that have been installed in the CurrentUser - TrustedPeople store.</span></span> <span data-ttu-id="54fce-159">为此，请使用以下命令：`certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>`，例如：`certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`。</span><span class="sxs-lookup"><span data-stu-id="54fce-159">To do this, use the following command: `certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>` For example: `certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="54fce-160">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="54fce-160">The samples may already be installed on your machine.</span></span> <span data-ttu-id="54fce-161">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="54fce-161">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="54fce-162">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54fce-162">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="54fce-163">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="54fce-163">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Basic\MessageSecurity`
