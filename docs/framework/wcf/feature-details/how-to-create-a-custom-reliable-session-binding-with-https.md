---
description: 了解详细信息：如何：使用 HTTPS 创建自定义可靠会话绑定
title: 如何：使用 HTTPS 创建自定义可靠会话绑定
ms.date: 03/30/2017
ms.assetid: fa772232-da1f-4c66-8c94-e36c0584b549
ms.openlocfilehash: 97e0386c3694552099a623a319f566fa4db2a39b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756170"
---
# <a name="how-to-create-a-custom-reliable-session-binding-with-https"></a><span data-ttu-id="5c5a6-103">如何：使用 HTTPS 创建自定义可靠会话绑定</span><span class="sxs-lookup"><span data-stu-id="5c5a6-103">How to: Create a Custom Reliable Session Binding with HTTPS</span></span>

<span data-ttu-id="5c5a6-104">本主题演示如何对可靠会话使用安全套接字层 (SSL) 传输安全。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-104">This topic demonstrates the use of Secure Sockets Layer (SSL) transport security with reliable sessions.</span></span> <span data-ttu-id="5c5a6-105">若要通过 HTTPS 使用可靠会话，必须创建使用可靠会话和 HTTPS 传输协议的自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-105">To use a reliable session over HTTPS, you must create a custom binding that uses a reliable session and the HTTPS transport.</span></span> <span data-ttu-id="5c5a6-106">可以通过使用代码以强制方式或在配置文件中以声明方式启用可靠会话。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-106">You enable the reliable session either imperatively by using code or declaratively in the configuration file.</span></span> <span data-ttu-id="5c5a6-107">此过程使用客户端和服务配置文件来启用可靠会话和 [**\<httpsTransport>**](../../configure-apps/file-schema/wcf/httpstransport.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-107">This procedure uses the client and service configuration files to enable the reliable session and the [**\<httpsTransport>**](../../configure-apps/file-schema/wcf/httpstransport.md) element.</span></span>

<span data-ttu-id="5c5a6-108">此过程的关键部分是 **\<endpoint>** 配置元素包含一个 `bindingConfiguration` 属性，该属性引用名为的自定义绑定配置 `reliableSessionOverHttps` 。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-108">The key part of this procedure is that the **\<endpoint>** configuration element contain a `bindingConfiguration` attribute that references a custom binding configuration named `reliableSessionOverHttps`.</span></span> <span data-ttu-id="5c5a6-109">[**\<binding>**](../../configure-apps/file-schema/wcf/bindings.md)配置元素引用此名称以指定通过包括和元素来使用可靠会话和 HTTPS 传输 **\<reliableSession>** **\<httpsTransport>** 。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-109">The [**\<binding>**](../../configure-apps/file-schema/wcf/bindings.md) configuration element references this name to specify that a reliable session and the HTTPS transport are used by including **\<reliableSession>** and **\<httpsTransport>** elements.</span></span>

<span data-ttu-id="5c5a6-110">有关此示例的源副本，请参阅 [通过 HTTPS 自定义绑定可靠会话](../samples/custom-binding-reliable-session-over-https.md)。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-110">For the source copy of this example, see [Custom Binding Reliable Session over HTTPS](../samples/custom-binding-reliable-session-over-https.md).</span></span>

### <a name="configure-the-service-with-a-custombinding-to-use-a-reliable-session-with-https"></a><span data-ttu-id="5c5a6-111">使用 CustomBinding 配置服务，以便将可靠会话与 HTTPS 一起使用</span><span class="sxs-lookup"><span data-stu-id="5c5a6-111">Configure the service with a CustomBinding to use a reliable session with HTTPS</span></span>

1. <span data-ttu-id="5c5a6-112">为该类型的服务定义服务协定。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-112">Define a service contract for the type of service.</span></span>

   [!code-csharp[c_HowTo_CreateReliableSessionHTTPS#1121](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/service.cs#1121)]

1. <span data-ttu-id="5c5a6-113">在服务类中实现该服务协定。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-113">Implement the service contract in a service class.</span></span> <span data-ttu-id="5c5a6-114">请注意，在服务的实现内未指定地址或绑定信息。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-114">Note that the address or binding information isn't specified inside the implementation of the service.</span></span> <span data-ttu-id="5c5a6-115">无需编写代码即可从配置文件中检索地址或绑定信息。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-115">You aren't required to write code to retrieve the address or binding information from the configuration file.</span></span>

   [!code-csharp[c_HowTo_CreateReliableSessionHTTPS#1122](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/service.cs#1122)]

1. <span data-ttu-id="5c5a6-116">使用名为 `CalculatorService` 的自定义绑定 `reliableSessionOverHttps` （使用可靠会话和 HTTPS 传输）为配置终结点，从而创建一个Web.config文件。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-116">Create a *Web.config* file to configure an endpoint for the `CalculatorService` with a custom binding named `reliableSessionOverHttps` that uses a reliable session and the HTTPS transport.</span></span>

   [!code-xml[c_HowTo_CreateReliableSessionHTTPS#2111](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/common/web.config#2111)]

1. <span data-ttu-id="5c5a6-117">创建包含以下行的 *服务 .svc* 文件：</span><span class="sxs-lookup"><span data-stu-id="5c5a6-117">Create a *Service.svc* file that contains the line:</span></span>

   `<%@ServiceHost language=c# Service="CalculatorService" %>`

1. <span data-ttu-id="5c5a6-118">将 *服务 .svc* 文件放入 INTERNET INFORMATION SERVICES (IIS) 虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-118">Place the *Service.svc* file in your Internet Information Services (IIS) virtual directory.</span></span>

### <a name="configure-the-client-with-a-custombinding-to-use-a-reliable-session-with-https"></a><span data-ttu-id="5c5a6-119">使用 CustomBinding 配置客户端以使用与 HTTPS 的可靠会话</span><span class="sxs-lookup"><span data-stu-id="5c5a6-119">Configure the client with a CustomBinding to use a reliable session with HTTPS</span></span>

1. <span data-ttu-id="5c5a6-120">使用 "工作的元数据实用工具" 工具，从命令行 [ (*Svcutil.exe*)](../servicemodel-metadata-utility-tool-svcutil-exe.md) ，以便从服务元数据生成代码。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-120">Use the [ServiceModel Metadata Utility Tool (*Svcutil.exe*)](../servicemodel-metadata-utility-tool-svcutil-exe.md) from the command line to generate code from service metadata.</span></span>

   ```console
   Svcutil.exe <Metadata Exchange (MEX) address or HTTP GET address>
   ```

1. <span data-ttu-id="5c5a6-121">生成的客户端包含 `ICalculator` 定义客户端实现必须满足的服务协定的接口。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-121">The client that's generated contains the `ICalculator` interface that defines the service contract that the client implementation must satisfy.</span></span>

   [!code-csharp[C_HowTo_CreateReliableSessionHTTPS#1221](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/client.cs#1221)]

1. <span data-ttu-id="5c5a6-122">生成的客户端应用程序还包含 `ClientCalculator` 的实现。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-122">The generated client application also contains the implementation of the `ClientCalculator`.</span></span> <span data-ttu-id="5c5a6-123">请注意，在服务的实现内未指定地址和绑定信息。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-123">Note that the address and binding information isn't specified inside the implementation of the service.</span></span> <span data-ttu-id="5c5a6-124">不需要编写代码来检索配置文件中的地址和绑定信息。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-124">You aren't required to write code to retrieve the address and binding information from the configuration file.</span></span>

   [!code-csharp[C_HowTo_CreateReliableSessionHTTPS#1222](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/client.cs#1222)]

1. <span data-ttu-id="5c5a6-125">将名为的自定义绑定配置 `reliableSessionOverHttps` 为使用 HTTPS 传输和可靠会话。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-125">Configure a custom binding named `reliableSessionOverHttps` to use the HTTPS transport and reliable sessions.</span></span>

   [!code-xml[C_HowTo_CreateReliableSessionHTTPS#2211](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/common/app.config#2211)]

1. <span data-ttu-id="5c5a6-126">在应用程序中创建 `ClientCalculator` 的实例，然后调用服务操作。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-126">Create an instance of the `ClientCalculator` in an application and then call the service operations.</span></span>

   [!code-csharp[C_HowTo_CreateReliableSessionHTTPS#1223](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/client.cs#1223)]

1. <span data-ttu-id="5c5a6-127">编译并运行客户端。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-127">Compile and run the client.</span></span>  

## <a name="net-framework-security"></a><span data-ttu-id="5c5a6-128">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="5c5a6-128">.NET Framework security</span></span>

<span data-ttu-id="5c5a6-129">由于本示例中使用的证书是使用 *Makecert.exe* 创建的测试证书，因此当你尝试从浏览器访问 HTTPS 地址（例如）时，会出现安全警报 `https://localhost/servicemodelsamples/service.svc` 。</span><span class="sxs-lookup"><span data-stu-id="5c5a6-129">Because the certificate used in this sample is a test certificate created with *Makecert.exe*, a security alert appears when you try to access an HTTPS address, such as `https://localhost/servicemodelsamples/service.svc`, from your browser.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c5a6-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="5c5a6-130">See also</span></span>

- [<span data-ttu-id="5c5a6-131">可靠会话</span><span class="sxs-lookup"><span data-stu-id="5c5a6-131">Reliable Sessions</span></span>](reliable-sessions.md)
