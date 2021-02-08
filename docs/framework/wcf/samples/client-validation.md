---
description: 了解详细信息：客户端验证
title: 客户端验证
ms.date: 03/30/2017
ms.assetid: f0c1f805-1a81-4d0d-a112-bf5e2e87a631
ms.openlocfilehash: 373ee49bccd8905e0cb9bfebf281abdd183ac506
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778563"
---
# <a name="client-validation"></a><span data-ttu-id="c6e23-103">客户端验证</span><span class="sxs-lookup"><span data-stu-id="c6e23-103">Client Validation</span></span>

<span data-ttu-id="c6e23-104">服务通常发布元数据以启用客户端代理类型的自动生成和配置。</span><span class="sxs-lookup"><span data-stu-id="c6e23-104">Services frequently publish metadata to enable automatic generation and configuration of client proxy types.</span></span> <span data-ttu-id="c6e23-105">如果服务不受信任，客户端应用程序应该验证元数据是否符合客户端应用程序有关安全性、事务、服务协定类型等方面的策略。</span><span class="sxs-lookup"><span data-stu-id="c6e23-105">When the service is not trusted, client applications should validate that the metadata conforms to the client application's policy regarding security, transactions, the type of service contract and so on.</span></span> <span data-ttu-id="c6e23-106">下面的示例演示如何编写一个客户端终结点行为，用于验证服务终结点以确保可以安全地使用该服务终结点。</span><span class="sxs-lookup"><span data-stu-id="c6e23-106">The following sample demonstrates how to write a client endpoint behavior that validates the service endpoint to ensure that service endpoint is safe to use.</span></span>  
  
 <span data-ttu-id="c6e23-107">服务公开四个终结点。</span><span class="sxs-lookup"><span data-stu-id="c6e23-107">The service exposes four service endpoints.</span></span> <span data-ttu-id="c6e23-108">第一个终结点使用 WSDualHttpBinding，第二个终结点使用 NTLM 身份验证，第三个终结点启用事务流，第四个终结点使用基于证书的身份验证。</span><span class="sxs-lookup"><span data-stu-id="c6e23-108">The first endpoint uses the WSDualHttpBinding, the second endpoint uses NTLM authentication, the third endpoint enables transaction flow, and the fourth endpoint uses certificate-based authentication.</span></span>  
  
 <span data-ttu-id="c6e23-109">客户端使用 <xref:System.ServiceModel.Description.MetadataResolver> 类来检索服务的元数据。</span><span class="sxs-lookup"><span data-stu-id="c6e23-109">The client uses the <xref:System.ServiceModel.Description.MetadataResolver> class to retrieve the metadata for the service.</span></span> <span data-ttu-id="c6e23-110">客户端强制实施禁用双工绑定、NTLM 身份验证和使用验证行为的事务流的策略。</span><span class="sxs-lookup"><span data-stu-id="c6e23-110">The client enforces a policy of prohibiting duplex bindings, NTLM authentication, and transaction flow using a validating behavior.</span></span> <span data-ttu-id="c6e23-111">对于 <xref:System.ServiceModel.Description.ServiceEndpoint> 从服务的元数据导入的每个实例，客户端应用程序在 `InternetClientValidatorBehavior` <xref:System.ServiceModel.Description.ServiceEndpoint> 尝试使用 Windows Communication Foundation (WCF) 客户端连接到终结点之前，会向添加一个终结点行为的实例。</span><span class="sxs-lookup"><span data-stu-id="c6e23-111">For each <xref:System.ServiceModel.Description.ServiceEndpoint> instance imported from the service's metadata, the client application adds an instance of the `InternetClientValidatorBehavior` endpoint behavior to the <xref:System.ServiceModel.Description.ServiceEndpoint> before attempting to use a Windows Communication Foundation (WCF) client to connect to the endpoint.</span></span> <span data-ttu-id="c6e23-112">在调用服务上的任何操作之前，会运行该行为的 `Validate` 方法，并通过引发 `InvalidOperationExceptions` 强制实施客户端的策略。</span><span class="sxs-lookup"><span data-stu-id="c6e23-112">The behavior's `Validate` method runs before any operations on the service are called and enforces the client's policy by throwing `InvalidOperationExceptions`.</span></span>  
  
### <a name="to-build-the-sample"></a><span data-ttu-id="c6e23-113">生成示例</span><span class="sxs-lookup"><span data-stu-id="c6e23-113">To build the sample</span></span>  
  
1. <span data-ttu-id="c6e23-114">若要生成解决方案，请按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="c6e23-114">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
### <a name="to-run-the-sample-on-the-same-computer"></a><span data-ttu-id="c6e23-115">在同一计算机上运行示例</span><span class="sxs-lookup"><span data-stu-id="c6e23-115">To run the sample on the same computer</span></span>  
  
1. <span data-ttu-id="c6e23-116">使用管理员权限打开 Visual Studio 开发人员命令提示，并从示例安装文件夹中运行 Setup.bat。</span><span class="sxs-lookup"><span data-stu-id="c6e23-116">Open a Developer Command Prompt for Visual Studio with administrator privileges and run Setup.bat from the sample install folder.</span></span> <span data-ttu-id="c6e23-117">这将安装运行示例所需的所有证书。</span><span class="sxs-lookup"><span data-stu-id="c6e23-117">This installs all the certificates required for running the sample.</span></span>  
  
2. <span data-ttu-id="c6e23-118">从 \service\bin\Debug 运行服务应用程序。</span><span class="sxs-lookup"><span data-stu-id="c6e23-118">Run the service application from \service\bin\Debug.</span></span>  
  
3. <span data-ttu-id="c6e23-119">从 \client\bin\Debug 运行客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="c6e23-119">Run the client application from \client\bin\Debug.</span></span> <span data-ttu-id="c6e23-120">客户端活动将显示在客户端控制台应用程序上。</span><span class="sxs-lookup"><span data-stu-id="c6e23-120">Client activity is displayed on the client console application.</span></span>  
  
4. <span data-ttu-id="c6e23-121">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="c6e23-121">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
5. <span data-ttu-id="c6e23-122">在运行完该示例后运行 Cleanup.bat 移除证书。</span><span class="sxs-lookup"><span data-stu-id="c6e23-122">Remove the certificates by running Cleanup.bat when you have finished with the sample.</span></span> <span data-ttu-id="c6e23-123">其他安全示例使用相同的证书。</span><span class="sxs-lookup"><span data-stu-id="c6e23-123">Other security samples use the same certificates.</span></span>  
  
### <a name="to-run-the-sample-across-computers"></a><span data-ttu-id="c6e23-124">跨计算机运行示例</span><span class="sxs-lookup"><span data-stu-id="c6e23-124">To run the sample across computers</span></span>  
  
1. <span data-ttu-id="c6e23-125">在服务器上，在 Visual Studio 开发人员命令提示中，以管理员权限运行，请键入 `setup.bat service` 。</span><span class="sxs-lookup"><span data-stu-id="c6e23-125">On the server, in a Developer Command Prompt for Visual Studio run with administrator privileges, type `setup.bat service`.</span></span> <span data-ttu-id="c6e23-126">使用参数运行将使用 `setup.bat` `service` 计算机的完全限定的域名创建一个服务证书，并将服务证书导出到名为的文件。</span><span class="sxs-lookup"><span data-stu-id="c6e23-126">Running `setup.bat` with the `service` argument creates a service certificate with the fully-qualified domain name of the computer and exports the service certificate to a file named Service.cer.</span></span>  
  
2. <span data-ttu-id="c6e23-127">在服务器上，编辑 App.config 以反映新证书名称。</span><span class="sxs-lookup"><span data-stu-id="c6e23-127">On the server, edit App.config to reflect the new certificate name.</span></span> <span data-ttu-id="c6e23-128">也就是说，将 `findValue` 元素中的属性更改 [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md) 为计算机的完全限定域名。</span><span class="sxs-lookup"><span data-stu-id="c6e23-128">That is, change the `findValue` attribute in the [\<serviceCertificate>](../../configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md) element to the fully-qualified domain name of the computer.</span></span>  
  
3. <span data-ttu-id="c6e23-129">将服务目录中的 Service.cer 文件复制到客户端计算机上的客户端目录中。</span><span class="sxs-lookup"><span data-stu-id="c6e23-129">Copy the Service.cer file from the service directory to the client directory on the client computer.</span></span>  
  
4. <span data-ttu-id="c6e23-130">在客户端上，使用管理员权限打开 Visual Studio 开发人员命令提示，然后键入 `setup.bat client` 。</span><span class="sxs-lookup"><span data-stu-id="c6e23-130">On the client, open a Developer Command Prompt for Visual Studio with administrator privileges, and type `setup.bat client`.</span></span> <span data-ttu-id="c6e23-131">`setup.bat`使用参数运行将 `client` 创建一个名为 Client.com 的客户端证书，并将客户端证书导出到名为的文件。</span><span class="sxs-lookup"><span data-stu-id="c6e23-131">Running `setup.bat` with the `client` argument creates a client certificate named Client.com and exports the client certificate to a file named Client.cer.</span></span>  
  
5. <span data-ttu-id="c6e23-132">在 client.cs 文件中更改 MEX 终结点的地址值和用于设置默认服务器证书的 `findValue` 以与服务的新地址相匹配。</span><span class="sxs-lookup"><span data-stu-id="c6e23-132">In the client.cs file change the address value of the MEX endpoint and the `findValue` for setting the default server certificate to match the new address of your service.</span></span> <span data-ttu-id="c6e23-133">通过使用服务器的完全限定域名替换 localhost 来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="c6e23-133">You do this by replacing localhost with the fully-qualified domain name of the server.</span></span> <span data-ttu-id="c6e23-134">Rebuild。</span><span class="sxs-lookup"><span data-stu-id="c6e23-134">Rebuild.</span></span>  
  
6. <span data-ttu-id="c6e23-135">将客户端目录中的 Client.cer 文件复制到服务器上的服务目录中。</span><span class="sxs-lookup"><span data-stu-id="c6e23-135">Copy the Client.cer file from the client directory to the service directory on the server.</span></span>  
  
7. <span data-ttu-id="c6e23-136">在客户端上，在使用管理员特权打开的 Visual Studio 开发人员命令提示中运行 ImportServiceCert.bat。</span><span class="sxs-lookup"><span data-stu-id="c6e23-136">On the client, run ImportServiceCert.bat in a Developer Command Prompt for Visual Studio opened with administrator privileges.</span></span> <span data-ttu-id="c6e23-137">这会将 Service.cer 文件中的服务证书导入 CurrentUser – TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="c6e23-137">This imports the service certificate from the Service.cer file into the CurrentUser - TrustedPeople store.</span></span>  
  
8. <span data-ttu-id="c6e23-138">在服务器上，在使用管理员特权打开的 Visual Studio 开发人员命令提示中运行 ImportClientCert.bat。</span><span class="sxs-lookup"><span data-stu-id="c6e23-138">On the server, run ImportClientCert.bat in a Developer Command Prompt for Visual Studio opened with administrator privileges.</span></span> <span data-ttu-id="c6e23-139">这会将 Client.cer 文件中的客户端证书导入 LocalMachine - TrustedPeople 存储区。</span><span class="sxs-lookup"><span data-stu-id="c6e23-139">This imports the client certificate from the Client.cer file into the LocalMachine - TrustedPeople store.</span></span>  
  
9. <span data-ttu-id="c6e23-140">在服务计算机上，在 Visual Studio 中生成服务项目并运行 service.exe。</span><span class="sxs-lookup"><span data-stu-id="c6e23-140">On the service computer, build the service project in Visual Studio and run service.exe.</span></span>  
  
10. <span data-ttu-id="c6e23-141">在客户端计算机上，运行 client.exe。</span><span class="sxs-lookup"><span data-stu-id="c6e23-141">On the client computer, run client.exe.</span></span>  
  
    1. <span data-ttu-id="c6e23-142">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="c6e23-142">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
### <a name="to-clean-up-after-the-sample"></a><span data-ttu-id="c6e23-143">运行示例后进行清理</span><span class="sxs-lookup"><span data-stu-id="c6e23-143">To clean up after the sample</span></span>  
  
- <span data-ttu-id="c6e23-144">运行完示例后运行示例文件夹中的 Cleanup.bat。</span><span class="sxs-lookup"><span data-stu-id="c6e23-144">Run Cleanup.bat in the samples folder once you have finished running the sample.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="c6e23-145">此脚本不会在跨计算机运行此示例时移除客户端上的服务证书。</span><span class="sxs-lookup"><span data-stu-id="c6e23-145">This script does not remove service certificates on a client when running this sample across computers.</span></span> <span data-ttu-id="c6e23-146">如果你已运行跨计算机使用证书的 WCF 示例，请确保清除已安装在 CurrentUser-TrustedPeople 存储中的服务证书。</span><span class="sxs-lookup"><span data-stu-id="c6e23-146">If you have run WCF samples that use certificates across computers, be sure to clear the service certificates that have been installed in the CurrentUser - TrustedPeople store.</span></span> <span data-ttu-id="c6e23-147">为此，请使用以下命令：`certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>. For example: certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`。</span><span class="sxs-lookup"><span data-stu-id="c6e23-147">To do this, use the following command: `certmgr -del -r CurrentUser -s TrustedPeople -c -n <Fully Qualified Server Machine Name>. For example: certmgr -del -r CurrentUser -s TrustedPeople -c -n server1.contoso.com`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6e23-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6e23-148">See also</span></span>

- [<span data-ttu-id="c6e23-149">使用元数据</span><span class="sxs-lookup"><span data-stu-id="c6e23-149">Using Metadata</span></span>](../feature-details/using-metadata.md)
