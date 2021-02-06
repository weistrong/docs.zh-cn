---
description: 了解详细信息：如何：指定通道安全凭据
title: 如何：指定通道安全凭据
ms.date: 03/30/2017
ms.assetid: f8e03f47-9c4f-4dd5-8f85-429e6d876119
ms.openlocfilehash: 18cbb1ea1113e5b31f5adb43556db03d91c618ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643145"
---
# <a name="how-to-specify-channel-security-credentials"></a><span data-ttu-id="311e4-103">如何：指定通道安全凭据</span><span class="sxs-lookup"><span data-stu-id="311e4-103">How to: Specify Channel Security Credentials</span></span>

<span data-ttu-id="311e4-104">Windows Communication Foundation (WCF) 服务标记允许 COM 应用程序调用 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="311e4-104">The Windows Communication Foundation (WCF) Service Moniker allows COM applications to call WCF services.</span></span> <span data-ttu-id="311e4-105">大多数 WCF 服务都要求客户端指定凭据以进行身份验证和授权。</span><span class="sxs-lookup"><span data-stu-id="311e4-105">Most WCF services require the client to specify credentials for authentication and authorization.</span></span> <span data-ttu-id="311e4-106">从 WCF 客户端调用 WCF 服务时，可以在托管代码或应用程序配置文件中指定这些凭据。</span><span class="sxs-lookup"><span data-stu-id="311e4-106">When calling a WCF service from a WCF client, you can specify these credentials in managed code or in an application configuration file.</span></span> <span data-ttu-id="311e4-107">从 COM 应用程序调用 WCF 服务时，可以使用 <xref:System.ServiceModel.ComIntegration.IChannelCredentials> 接口来指定凭据。</span><span class="sxs-lookup"><span data-stu-id="311e4-107">When calling a WCF service from a COM application, you can use the <xref:System.ServiceModel.ComIntegration.IChannelCredentials> interface to specify credentials.</span></span> <span data-ttu-id="311e4-108">本主题将介绍使用 <xref:System.ServiceModel.ComIntegration.IChannelCredentials> 接口指定凭据的各种方法。</span><span class="sxs-lookup"><span data-stu-id="311e4-108">This topic will illustrate various ways to specify credentials using the <xref:System.ServiceModel.ComIntegration.IChannelCredentials> interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="311e4-109"><xref:System.ServiceModel.ComIntegration.IChannelCredentials> 是一种基于 IDispatch 的接口，在 Visual Studio 环境中使用它将无法获取 IntelliSense 功能。</span><span class="sxs-lookup"><span data-stu-id="311e4-109"><xref:System.ServiceModel.ComIntegration.IChannelCredentials> is an IDispatch-based interface and you will not get IntelliSense functionality in the Visual Studio environment.</span></span>  
  
 <span data-ttu-id="311e4-110">本文将使用 [消息安全示例](../samples/message-security-sample.md)中定义的 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="311e4-110">This article will use the WCF service defined in the [Message Security Sample](../samples/message-security-sample.md).</span></span>  
  
### <a name="to-specify-a-client-certificate"></a><span data-ttu-id="311e4-111">指定客户端证书</span><span class="sxs-lookup"><span data-stu-id="311e4-111">To specify a client certificate</span></span>  
  
1. <span data-ttu-id="311e4-112">在消息安全目录中运行 Setup.bat 文件以创建和安装所需的测试证书。</span><span class="sxs-lookup"><span data-stu-id="311e4-112">Run the Setup.bat file in the Message Security directory to create and install the required test certificates.</span></span>  
  
2. <span data-ttu-id="311e4-113">打开消息安全项目。</span><span class="sxs-lookup"><span data-stu-id="311e4-113">Open the Message Security project.</span></span>  
  
3. <span data-ttu-id="311e4-114">添加 `[ServiceBehavior(Namespace="http://Microsoft.ServiceModel.Samples")]` 到 `ICalculator` 接口定义。</span><span class="sxs-lookup"><span data-stu-id="311e4-114">Add `[ServiceBehavior(Namespace="http://Microsoft.ServiceModel.Samples")]` to the `ICalculator` interface definition.</span></span>  
  
4. <span data-ttu-id="311e4-115">将添加 `bindingNamespace="http://Microsoft.ServiceModel.Samples"` 到服务的 App.config 中的终结点标记。</span><span class="sxs-lookup"><span data-stu-id="311e4-115">Add `bindingNamespace="http://Microsoft.ServiceModel.Samples"` to the endpoint tag in the App.config for the service.</span></span>  
  
5. <span data-ttu-id="311e4-116">生成消息安全示例并运行 Service.exe。</span><span class="sxs-lookup"><span data-stu-id="311e4-116">Build the Message Security Sample and run Service.exe.</span></span> <span data-ttu-id="311e4-117">使用 Internet Explorer 并浏览到服务的 URI (`http://localhost:8000/ServiceModelSamples/Service`) ，以确保服务正在运行。</span><span class="sxs-lookup"><span data-stu-id="311e4-117">Use Internet Explorer and browse to the service's URI (`http://localhost:8000/ServiceModelSamples/Service`) to ensure that the service is working.</span></span>  
  
6. <span data-ttu-id="311e4-118">打开 Visual Basic 6.0 并创建一个新的 Standard .exe 文件。</span><span class="sxs-lookup"><span data-stu-id="311e4-118">Open Visual Basic 6.0 and create a new Standard .exe file.</span></span> <span data-ttu-id="311e4-119">在窗体中添加一个按钮并双击该按钮，以将以下代码添加到 Click 处理程序中：</span><span class="sxs-lookup"><span data-stu-id="311e4-119">Add a button to the form and double-click the button to add the following code to the Click handler:</span></span>  
  
    ```vb  
        monString = "service:mexAddress=http://localhost:8000/ServiceModelSamples/Service?wsdl"  
        monString = monString + ", address=http://localhost:8000/ServiceModelSamples/Service"  
        monString = monString + ", contract=ICalculator, contractNamespace=http://Microsoft.ServiceModel.Samples"  
        monString = monString + ", binding=BasicHttpBinding_ICalculator, bindingNamespace=http://Microsoft.ServiceModel.Samples"  
  
        Set monikerProxy = GetObject(monString)  
  
        'Set the Service Certificate.  
     monikerProxy.ChannelCredentials.SetServiceCertificateAuthentication "CurrentUser", "NoCheck", "PeerOrChainTrust"  
    monikerProxy.ChannelCredentials.SetDefaultServiceCertificateFromStore "CurrentUser", "TrustedPeople", "FindBySubjectName", "localhost"  
  
        'Set the Client Certificate.  
        monikerProxy.ChannelCredentials.SetClientCertificateFromStoreByName "CN=client.com", "CurrentUser", "My"  
        MsgBox monikerProxy.Add(3, 4)  
    ```  
  
7. <span data-ttu-id="311e4-120">运行 Visual Basic 应用程序并验证结果。</span><span class="sxs-lookup"><span data-stu-id="311e4-120">Run the Visual Basic application and verify the results.</span></span>  
  
     <span data-ttu-id="311e4-121">Visual Basic 应用程序将显示一个消息框，其中包含调用 Add(3, 4) 的结果。</span><span class="sxs-lookup"><span data-stu-id="311e4-121">The Visual Basic application will display a message box with the result from calling Add(3, 4).</span></span> <span data-ttu-id="311e4-122"><xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetClientCertificateFromFile%28System.String%2CSystem.String%2CSystem.String%29> 或 <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetClientCertificateFromStoreByName%28System.String%2CSystem.String%2CSystem.String%29> 也可以用于代替 <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetClientCertificateFromStore%28System.String%2CSystem.String%2CSystem.String%2CSystem.Object%29> 设置客户端证书：</span><span class="sxs-lookup"><span data-stu-id="311e4-122"><xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetClientCertificateFromFile%28System.String%2CSystem.String%2CSystem.String%29> or <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetClientCertificateFromStoreByName%28System.String%2CSystem.String%2CSystem.String%29> can also be used in place of <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetClientCertificateFromStore%28System.String%2CSystem.String%2CSystem.String%2CSystem.Object%29> to set the Client Certificate:</span></span>  
  
    ```vb  
    monikerProxy.ChannelCredentials.SetClientCertificateFromFile "C:\MyClientCert.pfx", "password", "DefaultKeySet"  
    ```  
  
> [!NOTE]
> <span data-ttu-id="311e4-123">为使此调用生效，客户端证书在运行该客户端的计算机上应该是受信任的。</span><span class="sxs-lookup"><span data-stu-id="311e4-123">For this call to work, the client certificate needs to be trusted on the machine the client is running on.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="311e4-124">如果标记格式不正确，或如果服务不可用，则对 `GetObject` 的调用将返回一个错误，指示“语法无效”。</span><span class="sxs-lookup"><span data-stu-id="311e4-124">If the moniker is malformed or if the service is unavailable, the call to `GetObject` will return an error saying "Invalid Syntax."</span></span> <span data-ttu-id="311e4-125">如果您收到此错误，请确保所使用的标记正确无误且服务可用。</span><span class="sxs-lookup"><span data-stu-id="311e4-125">If you receive this error, make sure the moniker you are using is correct and the service is available.</span></span>  
  
### <a name="to-specify-user-name-and-password"></a><span data-ttu-id="311e4-126">指定用户名和密码</span><span class="sxs-lookup"><span data-stu-id="311e4-126">To specify user name and password</span></span>  
  
1. <span data-ttu-id="311e4-127">修改服务的 App.config 文件以使用 `wsHttpBinding`。</span><span class="sxs-lookup"><span data-stu-id="311e4-127">Modify the Service App.config file to use the `wsHttpBinding`.</span></span> <span data-ttu-id="311e4-128">验证用户名和密码时需要如此：</span><span class="sxs-lookup"><span data-stu-id="311e4-128">This is required for user name and password validation:</span></span>  

2. <span data-ttu-id="311e4-129">将 `clientCredentialType` 设置为 UserName：</span><span class="sxs-lookup"><span data-stu-id="311e4-129">Set the `clientCredentialType` to UserName:</span></span>  

3. <span data-ttu-id="311e4-130">打开 Visual Basic 6.0 并创建一个新的 Standard .exe 文件。</span><span class="sxs-lookup"><span data-stu-id="311e4-130">Open Visual Basic 6.0 and create a new Standard .exe file.</span></span> <span data-ttu-id="311e4-131">在窗体中添加一个按钮并双击该按钮，以将以下代码添加到 Click 处理程序中：</span><span class="sxs-lookup"><span data-stu-id="311e4-131">Add a button to the form and double-click the button to add the following code to the Click handler:</span></span>  
  
    ```vb
    monString = "service:mexAddress=http://localhost:8000/ServiceModelSamples/Service?wsdl"  
    monString = monString + ", address=http://localhost:8000/ServiceModelSamples/Service"  
    monString = monString + ", contract=ICalculator, contractNamespace=http://Microsoft.ServiceModel.Samples"  
    monString = monString + ", binding=WSHttpBinding_ICalculator, bindingNamespace=http://Microsoft.ServiceModel.Samples"  
  
    Set monikerProxy = GetObject(monString)  
  
    monikerProxy.ChannelCredentials.SetServiceCertificateAuthentication "CurrentUser", "NoCheck", "PeerOrChainTrust"  
    monikerProxy.ChannelCredentials.SetUserNameCredential "username", "password"  
  
    MsgBox monikerProxy.Add(3, 4)  
    ```  
  
4. <span data-ttu-id="311e4-132">运行 Visual Basic 应用程序并验证结果。</span><span class="sxs-lookup"><span data-stu-id="311e4-132">Run the Visual Basic application and verify the results.</span></span> <span data-ttu-id="311e4-133">Visual Basic 应用程序将显示一个消息框，其中包含调用 Add(3, 4) 的结果。</span><span class="sxs-lookup"><span data-stu-id="311e4-133">The Visual Basic application will display a message box with the result from calling Add(3, 4).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="311e4-134">在本示例中，服务标记中指定的绑定已更改为 WSHttpBinding_ICalculator。</span><span class="sxs-lookup"><span data-stu-id="311e4-134">The binding specified in the service moniker in this sample has been changed to WSHttpBinding_ICalculator.</span></span> <span data-ttu-id="311e4-135">另外请注意，在调用 <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetUserNameCredential%28System.String%2CSystem.String%29> 时，必须提供有效的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="311e4-135">Also note that you must supply a valid user name and password in the call to <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetUserNameCredential%28System.String%2CSystem.String%29>.</span></span>  
  
### <a name="to-specify-windows-credentials"></a><span data-ttu-id="311e4-136">指定 Windows 凭据</span><span class="sxs-lookup"><span data-stu-id="311e4-136">To specify Windows Credentials</span></span>  
  
1. <span data-ttu-id="311e4-137">在服务的 App.config 文件中将 `clientCredentialType` 设置为 Windows：</span><span class="sxs-lookup"><span data-stu-id="311e4-137">Set `clientCredentialType` to Windows in the Service App.config file:</span></span>  

2. <span data-ttu-id="311e4-138">打开 Visual Basic 6.0 并创建一个新的 Standard .exe 文件。</span><span class="sxs-lookup"><span data-stu-id="311e4-138">Open Visual Basic 6.0 and create a new Standard .exe file.</span></span> <span data-ttu-id="311e4-139">在窗体中添加一个按钮并双击该按钮，以将以下代码添加到 Click 处理程序中：</span><span class="sxs-lookup"><span data-stu-id="311e4-139">Add a button to the form and double-click the button to add the following code to the Click handler:</span></span>  
  
    ```vb
    monString = "service:mexAddress=http://localhost:8000/ServiceModelSamples/Service?wsdl"  
    monString = monString + ", address=http://localhost:8000/ServiceModelSamples/Service"  
    monString = monString + ", contract=ICalculator, contractNamespace=http://Microsoft.ServiceModel.Samples"  
    monString = monString + ", binding=WSHttpBinding_ICalculator, bindingNamespace=http://Microsoft.ServiceModel.Samples"  
    monString = monString + ", upnidentity=domain\userID"  
  
    Set monikerProxy = GetObject(monString)  
     monikerProxy.ChannelCredentials.SetWindowsCredential "domain", "userID", "password", 1, True  
  
    MsgBox monikerProxy.Add(3, 4)  
    ```  
  
3. <span data-ttu-id="311e4-140">运行 Visual Basic 应用程序并验证结果。</span><span class="sxs-lookup"><span data-stu-id="311e4-140">Run the Visual Basic application and verify the results.</span></span> <span data-ttu-id="311e4-141">Visual Basic 应用程序将显示一个消息框，其中包含调用 Add(3, 4) 的结果。</span><span class="sxs-lookup"><span data-stu-id="311e4-141">The Visual Basic application will display a message box with the result from calling Add(3, 4).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="311e4-142">您必须使用有效值替换“domain”、“userID”和“password”。</span><span class="sxs-lookup"><span data-stu-id="311e4-142">You must replace "domain", "userID", and "password" with valid values.</span></span>  
  
### <a name="to-specify-an-issue-token"></a><span data-ttu-id="311e4-143">指定颁发令牌</span><span class="sxs-lookup"><span data-stu-id="311e4-143">To specify an issue token</span></span>  
  
1. <span data-ttu-id="311e4-144">颁发令牌仅用于使用联合安全的应用程序。</span><span class="sxs-lookup"><span data-stu-id="311e4-144">Issue tokens are used only for applications using federated security.</span></span> <span data-ttu-id="311e4-145">有关联合安全的详细信息，请参阅 [联合和颁发的令牌](federation-and-issued-tokens.md) 和 [联合身份验证示例](../samples/federation-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="311e4-145">For more information about federated security, see [Federation and Issued Tokens](federation-and-issued-tokens.md) and [Federation Sample](../samples/federation-sample.md).</span></span>  
  
     <span data-ttu-id="311e4-146">下面的 Visual Basic 代码示例演示如何调用 <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetIssuedToken%28System.String%2CSystem.String%2CSystem.String%29> 方法：</span><span class="sxs-lookup"><span data-stu-id="311e4-146">The following Visual Basic code example illustrates how to call the <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetIssuedToken%28System.String%2CSystem.String%2CSystem.String%29> method:</span></span>  
  
    ```vb
        monString = "service:mexAddress=http://localhost:8000/ServiceModelSamples/Service?wsdl"  
        monString = monString + ", address=http://localhost:8000/SomeService/Service"  
        monString = monString + ", contract=ICalculator, contractNamespace=http://SomeService.Samples"  
        monString = monString + ", binding=WSHttpBinding_ISomeContract, bindingNamespace=http://SomeService.Samples"  
  
        Set monikerProxy = GetObject(monString)  
    monikerProxy.SetIssuedToken("http://somemachine/sts", "bindingType", "binding")  
    ```  
  
     <span data-ttu-id="311e4-147">有关用于此方法的参数的更多信息，请参见 <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetIssuedToken%28System.String%2CSystem.String%2CSystem.String%29>。</span><span class="sxs-lookup"><span data-stu-id="311e4-147">For more information about the parameters for this method, see <xref:System.ServiceModel.ComIntegration.IChannelCredentials.SetIssuedToken%28System.String%2CSystem.String%2CSystem.String%29>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="311e4-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="311e4-148">See also</span></span>

- [<span data-ttu-id="311e4-149">联合</span><span class="sxs-lookup"><span data-stu-id="311e4-149">Federation</span></span>](federation.md)
- [<span data-ttu-id="311e4-150">如何：在联合身份验证服务上配置凭据</span><span class="sxs-lookup"><span data-stu-id="311e4-150">How to: Configure Credentials on a Federation Service</span></span>](how-to-configure-credentials-on-a-federation-service.md)
- [<span data-ttu-id="311e4-151">如何：创建联合客户端</span><span class="sxs-lookup"><span data-stu-id="311e4-151">How to: Create a Federated Client</span></span>](how-to-create-a-federated-client.md)
- [<span data-ttu-id="311e4-152">消息安全</span><span class="sxs-lookup"><span data-stu-id="311e4-152">Message Security</span></span>](message-security-in-wcf.md)
- [<span data-ttu-id="311e4-153">绑定与安全</span><span class="sxs-lookup"><span data-stu-id="311e4-153">Bindings and Security</span></span>](bindings-and-security.md)
