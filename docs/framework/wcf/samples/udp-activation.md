---
description: 了解详细信息： UDP 激活
title: UDP 激活
ms.date: 03/30/2017
ms.assetid: 4b0ccd10-0dfb-4603-93f9-f0857c581cb7
ms.openlocfilehash: 8ee5e6363265ddc74d27884ef40354108da17581
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798220"
---
# <a name="udp-activation"></a><span data-ttu-id="786cc-103">UDP 激活</span><span class="sxs-lookup"><span data-stu-id="786cc-103">UDP Activation</span></span>

<span data-ttu-id="786cc-104">此示例基于 [Transport： UDP](transport-udp.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="786cc-104">This sample is based on the [Transport: UDP](transport-udp.md) sample.</span></span> <span data-ttu-id="786cc-105">它扩展了 [传输： UDP](transport-udp.md) 示例，以支持使用) 的 Windows 进程激活服务 (处理激活。</span><span class="sxs-lookup"><span data-stu-id="786cc-105">It extends the [Transport: UDP](transport-udp.md) sample to support process activation using the Windows Process Activation Service (WAS).</span></span>  
  
 <span data-ttu-id="786cc-106">该示例主要由三个部分组成：</span><span class="sxs-lookup"><span data-stu-id="786cc-106">The sample consists of three major pieces:</span></span>  
  
- <span data-ttu-id="786cc-107">UDP 协议激活器，代表要激活的应用程序接收 UDP 消息的独立进程。</span><span class="sxs-lookup"><span data-stu-id="786cc-107">A UDP Protocol Activator, a standalone process that receives UDP messages on behalf of applications that are to be activated.</span></span>  
  
- <span data-ttu-id="786cc-108">使用 UDP 自定义传输发送消息的客户端。</span><span class="sxs-lookup"><span data-stu-id="786cc-108">A client that uses the UDP custom transport to send messages.</span></span>  
  
- <span data-ttu-id="786cc-109">通过 UDP 自定义传输接收消息的服务（承载于 WAS 激活的工作进程中）。</span><span class="sxs-lookup"><span data-stu-id="786cc-109">A service (hosted in a worker process activated by WAS) that receives messages over the UDP custom transport.</span></span>  
  
## <a name="udp-protocol-activator"></a><span data-ttu-id="786cc-110">UDP 协议激活器</span><span class="sxs-lookup"><span data-stu-id="786cc-110">UDP Protocol Activator</span></span>  

 <span data-ttu-id="786cc-111">UDP 协议激活器是 WCF 客户端和 WCF 服务之间的桥梁。</span><span class="sxs-lookup"><span data-stu-id="786cc-111">The UDP Protocol Activator is a bridge between the WCF client and the WCF service.</span></span> <span data-ttu-id="786cc-112">该激活器通过 UDP 协议在传输层提供数据通信。</span><span class="sxs-lookup"><span data-stu-id="786cc-112">It provides data communication through the UDP protocol at the transport layer.</span></span> <span data-ttu-id="786cc-113">它主要有两个功能：</span><span class="sxs-lookup"><span data-stu-id="786cc-113">It has two major functions:</span></span>  
  
- <span data-ttu-id="786cc-114">WAS 侦听器适配器 (LA)，它与 WAS 协作激活进程以响应传入消息。</span><span class="sxs-lookup"><span data-stu-id="786cc-114">WAS Listener Adapter (LA), which collaborates with WAS to activate processes in response to incoming messages.</span></span>  
  
- <span data-ttu-id="786cc-115">UDP 协议侦听器，它代表要激活的应用程序接受 UDP 消息。</span><span class="sxs-lookup"><span data-stu-id="786cc-115">UDP Protocol Listener, which accepts UDP messages on behalf of applications that are to be activated.</span></span>  
  
 <span data-ttu-id="786cc-116">激活器必须作为独立的程序在服务器计算机上运行。</span><span class="sxs-lookup"><span data-stu-id="786cc-116">The activator must be running as a standalone program on the server machine.</span></span> <span data-ttu-id="786cc-117">通常，WAS 侦听器适配器（如 NetTcpActivator 和 NetPipeActivator）在长时间运行的 Windows 服务中实现。</span><span class="sxs-lookup"><span data-stu-id="786cc-117">Normally, WAS listener adapters (such as the NetTcpActivator and the NetPipeActivator) are implemented in long-running Windows services.</span></span> <span data-ttu-id="786cc-118">但是，为了简单明确起见，此示例将协议激活器作为独立的应用程序实现。</span><span class="sxs-lookup"><span data-stu-id="786cc-118">However, for simplicity and clarity, this sample implements the protocol activator as a standalone application.</span></span>  
  
### <a name="was-listener-adapter"></a><span data-ttu-id="786cc-119">WAS 侦听器适配器</span><span class="sxs-lookup"><span data-stu-id="786cc-119">WAS Listener Adapter</span></span>  

 <span data-ttu-id="786cc-120">UDP 的 WAS 侦听器适配器是在 `UdpListenerAdapter` 类中实现的。</span><span class="sxs-lookup"><span data-stu-id="786cc-120">The WAS Listener Adapter for UDP is implemented in the `UdpListenerAdapter` class.</span></span> <span data-ttu-id="786cc-121">该适配器是与 WAS 交互以针对 UDP 协议执行应用程序激活的模块。</span><span class="sxs-lookup"><span data-stu-id="786cc-121">It is the module that interacts with WAS to perform application activation for the UDP protocol.</span></span> <span data-ttu-id="786cc-122">这一过程是通过调用下列 Webhost API 实现的：</span><span class="sxs-lookup"><span data-stu-id="786cc-122">This is achieved by calling the following Webhost APIs:</span></span>  
  
- `WebhostRegisterProtocol`  
  
- `WebhostUnregisterProtocol`  
  
- `WebhostOpenListenerChannelInstance`  
  
- `WebhostCloseAllListenerChannelInstances`  
  
 <span data-ttu-id="786cc-123">最初调用 `WebhostRegisterProtocol` 之后，侦听器适配器将为 applicationHost.config（位于 %windir%\system32\inetsrv）中注册的所有应用程序接收来自 WAS 的回调 `ApplicationCreated`。</span><span class="sxs-lookup"><span data-stu-id="786cc-123">After initially calling `WebhostRegisterProtocol`, the listener adapter receives the callback `ApplicationCreated` from WAS for all of the applications registered in applicationHost.config (located in %windir%\system32\inetsrv).</span></span> <span data-ttu-id="786cc-124">在此示例中，我们仅在启用 UDP 协议（协议 ID 为“net.udp”时）的情况下处理应用程序。</span><span class="sxs-lookup"><span data-stu-id="786cc-124">In this sample, we only handle the applications with the UDP protocol (with the protocol id as "net.udp") enabled.</span></span> <span data-ttu-id="786cc-125">如果其他实现对应用程序的动态配置更改（例如，应用程序从禁用转换为启用）作出响应，这些实现可能会以不同的方式处理上述情况。</span><span class="sxs-lookup"><span data-stu-id="786cc-125">Other implementations may handle this differently if such implementations respond to dynamic configuration changes to the application (for example, an application transition from disabled to enabled).</span></span>  
  
 <span data-ttu-id="786cc-126">当收到回调 `ConfigManagerInitializationCompleted` 时，则表示 WAS 已经完成协议初始化的所有通知。</span><span class="sxs-lookup"><span data-stu-id="786cc-126">When the callback `ConfigManagerInitializationCompleted` is received, it indicates that WAS has finished all of the notifications for the initialization of the protocol.</span></span> <span data-ttu-id="786cc-127">此时，侦听器适配器已准备处理激活请求。</span><span class="sxs-lookup"><span data-stu-id="786cc-127">At this time, the listener adapter is ready to process activation requests.</span></span>  
  
 <span data-ttu-id="786cc-128">当首次传入针对某个应用程序的新请求时，侦听器适配器会将 `WebhostOpenListenerChannelInstance` 调入 WAS，从而启动工作进程（如果尚未启动）。</span><span class="sxs-lookup"><span data-stu-id="786cc-128">When a new request comes in the first time for an application, the listener adapter calls `WebhostOpenListenerChannelInstance` into WAS, which starts the worker process if it is not started yet.</span></span> <span data-ttu-id="786cc-129">然后加载协议处理程序，并可以启动侦听器适配器与虚拟应用程序之间的通信。</span><span class="sxs-lookup"><span data-stu-id="786cc-129">Then the protocol handlers are loaded and the communication between the listener adapter and the virtual application can start.</span></span>  
  
 <span data-ttu-id="786cc-130">侦听器适配器在 "<>" 部分的 "% SystemRoot% \System32\inetsrv\ApplicationHost.config 中注册，如下所示 `listenerAdapters` ：</span><span class="sxs-lookup"><span data-stu-id="786cc-130">The listener adapter is registered in the %SystemRoot%\System32\inetsrv\ApplicationHost.config in the <`listenerAdapters`> section as following:</span></span>  
  
```xml  
<add name="net.udp" identity="S-1-5-21-2127521184-1604012920-1887927527-387045" />  
```  
  
### <a name="protocol-listener"></a><span data-ttu-id="786cc-131">协议侦听器</span><span class="sxs-lookup"><span data-stu-id="786cc-131">Protocol Listener</span></span>  

 <span data-ttu-id="786cc-132">UDP 协议侦听器是协议激活器内部的模块，它代表虚拟应用程序在 UDP 终结点进行侦听。</span><span class="sxs-lookup"><span data-stu-id="786cc-132">The UDP protocol listener is a module inside the protocol activator that listens at a UDP endpoint on behalf of the virtual application.</span></span> <span data-ttu-id="786cc-133">它在 `UdpSocketListener` 类中实现。</span><span class="sxs-lookup"><span data-stu-id="786cc-133">It is implemented in the class `UdpSocketListener`.</span></span> <span data-ttu-id="786cc-134">终结点表示为 `IPEndpoint`，其端口号从站点协议的绑定中提取。</span><span class="sxs-lookup"><span data-stu-id="786cc-134">The endpoint is represented as `IPEndpoint` for which the port number is extracted from the binding of the protocol for the site.</span></span>  
  
### <a name="control-service"></a><span data-ttu-id="786cc-135">控制服务</span><span class="sxs-lookup"><span data-stu-id="786cc-135">Control Service</span></span>  

 <span data-ttu-id="786cc-136">在此示例中，我们使用 WCF 在激活器和 WAS 工作进程之间进行通信。</span><span class="sxs-lookup"><span data-stu-id="786cc-136">In this sample, we use WCF to communicate between the activator and the WAS worker process.</span></span> <span data-ttu-id="786cc-137">驻留在激活器中的服务称为“控制服务”。</span><span class="sxs-lookup"><span data-stu-id="786cc-137">The service that resides in the activator is called the Control Service.</span></span>  
  
## <a name="protocol-handlers"></a><span data-ttu-id="786cc-138">协议处理程序</span><span class="sxs-lookup"><span data-stu-id="786cc-138">Protocol Handlers</span></span>  

 <span data-ttu-id="786cc-139">侦听器适配器调用 `WebhostOpenListenerChannelInstance` 之后，WAS 进程管理器将启动工作进程（如果尚未启动）。</span><span class="sxs-lookup"><span data-stu-id="786cc-139">After the listener adapter calls `WebhostOpenListenerChannelInstance`, the WAS process manager starts the worker process if it is not started.</span></span> <span data-ttu-id="786cc-140">工作进程内部的应用程序管理器随后使用该 `ListenerChannelId` 的请求加载 UDP 进程协议处理程序 (PPH)。</span><span class="sxs-lookup"><span data-stu-id="786cc-140">The application manager inside the worker process then loads the UDP Process Protocol Handler (PPH) with the request for that `ListenerChannelId`.</span></span> <span data-ttu-id="786cc-141">中的 PPH 将调用 `IAdphManager` 。`StartAppDomainProtocolListenerChannel`</span><span class="sxs-lookup"><span data-stu-id="786cc-141">The PPH in turns calls `IAdphManager`.`StartAppDomainProtocolListenerChannel`</span></span> <span data-ttu-id="786cc-142">若要启动 UDP AppDomain 协议处理程序 (ADPH) 。</span><span class="sxs-lookup"><span data-stu-id="786cc-142">to start the UDP AppDomain Protocol Handler (ADPH).</span></span>  
  
## <a name="hostedudptransportconfiguration"></a><span data-ttu-id="786cc-143">HostedUDPTransportConfiguration</span><span class="sxs-lookup"><span data-stu-id="786cc-143">HostedUDPTransportConfiguration</span></span>  

 <span data-ttu-id="786cc-144">该信息按如下方式在 Web.config 中注册：</span><span class="sxs-lookup"><span data-stu-id="786cc-144">The information is registered in the Web.config as follows:</span></span>  
  
```xml  
<serviceHostingEnvironment>  
<add name="net.udp" transportConfigurationType="Microsoft.ServiceModel.Samples.Hosting.HostedUdpTransportConfiguration, UdpActivation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6fa904d2da1848d6" />  
</serviceHostingEnvironment>  
```  
  
## <a name="special-setup-for-this-sample"></a><span data-ttu-id="786cc-145">此示例的特殊设置</span><span class="sxs-lookup"><span data-stu-id="786cc-145">Special Setup for This Sample</span></span>  

 <span data-ttu-id="786cc-146">此示例只能在 Windows Vista、Windows Server 2008 或 Windows 7 上生成和运行。</span><span class="sxs-lookup"><span data-stu-id="786cc-146">This sample can be only built and run on Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="786cc-147">若要运行此示例，必须首先正确设置所有组件。</span><span class="sxs-lookup"><span data-stu-id="786cc-147">To run the sample, you must first get all of the components set up correctly.</span></span> <span data-ttu-id="786cc-148">使用下列步骤安装该示例。</span><span class="sxs-lookup"><span data-stu-id="786cc-148">Use the following steps to install the sample.</span></span>  
  
#### <a name="to-set-up-this-sample"></a><span data-ttu-id="786cc-149">设置此示例</span><span class="sxs-lookup"><span data-stu-id="786cc-149">To set up this sample</span></span>  
  
1. <span data-ttu-id="786cc-150">使用以下命令安装 ASP.NET 4.0。</span><span class="sxs-lookup"><span data-stu-id="786cc-150">Install ASP.NET 4.0 using the following command.</span></span>  
  
    ```console  
    %windir%\Microsoft.NET\Framework\v4.0.XXXXX\aspnet_regiis.exe /i /enable  
    ```  
  
2. <span data-ttu-id="786cc-151">在 Windows Vista 上生成项目。</span><span class="sxs-lookup"><span data-stu-id="786cc-151">Build the project on Windows Vista.</span></span> <span data-ttu-id="786cc-152">编译后，该项目还将在后期生成阶段执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="786cc-152">After compilation, it also performs the following operations in the post-build phase:</span></span>  
  
    - <span data-ttu-id="786cc-153">将 UDP 绑定安装到“默认网站”站点。</span><span class="sxs-lookup"><span data-stu-id="786cc-153">Installs the UDP binding to the site "Default Web Site".</span></span>  
  
    - <span data-ttu-id="786cc-154">创建虚拟应用程序“ServiceModelSamples”，指向物理路径“%SystemDrive%\inetpub\wwwroot\servicemodelsamples”。</span><span class="sxs-lookup"><span data-stu-id="786cc-154">Creates the virtual application "ServiceModelSamples" to point to the physical path: "%SystemDrive%\inetpub\wwwroot\servicemodelsamples".</span></span>  
  
    - <span data-ttu-id="786cc-155">这还为该虚拟应用程序启用“net.udp”协议。</span><span class="sxs-lookup"><span data-stu-id="786cc-155">It also enables "net.udp" protocol for this virtual application.</span></span>  
  
3. <span data-ttu-id="786cc-156">启动用户接口应用程序“WasNetActivator.exe”。</span><span class="sxs-lookup"><span data-stu-id="786cc-156">Start the user interface application "WasNetActivator.exe".</span></span> <span data-ttu-id="786cc-157">单击 " **设置** " 选项卡，选中以下复选框，然后单击 " **安装** " 以安装它们：</span><span class="sxs-lookup"><span data-stu-id="786cc-157">Click the **Setup** tab, check the following check boxes and then click **Install** to install them:</span></span>  
  
    - <span data-ttu-id="786cc-158">UDP 侦听器适配器</span><span class="sxs-lookup"><span data-stu-id="786cc-158">UDP Listener Adapter</span></span>  
  
    - <span data-ttu-id="786cc-159">UDP 协议处理程序</span><span class="sxs-lookup"><span data-stu-id="786cc-159">UDP Protocol Handlers</span></span>  
  
4. <span data-ttu-id="786cc-160">单击用户界面应用程序 "WasNetActivator.exe" 的 " **激活** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="786cc-160">Click the **Activation** tab of the user interface application "WasNetActivator.exe".</span></span> <span data-ttu-id="786cc-161">单击 " **启动** " 按钮以启动侦听器适配器。</span><span class="sxs-lookup"><span data-stu-id="786cc-161">Click the **Start** button to start the listener adapter.</span></span> <span data-ttu-id="786cc-162">现在即可运行程序。</span><span class="sxs-lookup"><span data-stu-id="786cc-162">Now you are ready to run the program.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="786cc-163">完成此示例后，必须运行 Cleanup.bat，从“默认网站”中移除 net.udp 绑定。</span><span class="sxs-lookup"><span data-stu-id="786cc-163">When you are finished with this sample, you must run Cleanup.bat to remove the net.udp binding from the "Default Web Site".</span></span>  
  
## <a name="sample-usage"></a><span data-ttu-id="786cc-164">示例用法</span><span class="sxs-lookup"><span data-stu-id="786cc-164">Sample Usage</span></span>  

 <span data-ttu-id="786cc-165">编译后，生成四个不同的二进制文件：</span><span class="sxs-lookup"><span data-stu-id="786cc-165">After compilation, there are four different binaries generated:</span></span>  
  
- <span data-ttu-id="786cc-166">Client.exe：客户端代码。</span><span class="sxs-lookup"><span data-stu-id="786cc-166">Client.exe: The client code.</span></span> <span data-ttu-id="786cc-167">App.config 编译到客户端配置文件 Client.exe.config 中。</span><span class="sxs-lookup"><span data-stu-id="786cc-167">The App.config is compiled into the client configuration file Client.exe.config.</span></span>  
  
- <span data-ttu-id="786cc-168">UDPActivation.dll：包含所有主要 UDP 实现的库。</span><span class="sxs-lookup"><span data-stu-id="786cc-168">UDPActivation.dll: the library that contains all of the major UDP implementations.</span></span>  
  
- <span data-ttu-id="786cc-169">Service.dll：服务代码。</span><span class="sxs-lookup"><span data-stu-id="786cc-169">Service.dll: The service code.</span></span> <span data-ttu-id="786cc-170">此代码被复制到虚拟应用程序 ServiceModelSamples 的 \bin 目录。</span><span class="sxs-lookup"><span data-stu-id="786cc-170">This is copied to the \bin directory of the virtual application ServiceModelSamples.</span></span> <span data-ttu-id="786cc-171">服务文件为 node.js，并 Web.config 配置文件。编译完成后，会将其复制到以下位置：%Systemdrive%\inetpub\wwwroot\servicemodelsamples。</span><span class="sxs-lookup"><span data-stu-id="786cc-171">The service file is Service.svc and the configuration file is Web.config. After compilation, they are copied to the following location: %SystemDrive%\Inetpub\wwwroot\ServiceModelSamples.</span></span>  
  
- <span data-ttu-id="786cc-172">WasNetActivator：UDP 激活器程序。</span><span class="sxs-lookup"><span data-stu-id="786cc-172">WasNetActivator: The UDP activator program.</span></span>  
  
- <span data-ttu-id="786cc-173">确保所有的必需部分均已正确安装。</span><span class="sxs-lookup"><span data-stu-id="786cc-173">Ensure that all of the required pieces are installed correctly.</span></span> <span data-ttu-id="786cc-174">下列步骤说明如何运行该示例：</span><span class="sxs-lookup"><span data-stu-id="786cc-174">The following steps show how to run the sample:</span></span>  
  
1. <span data-ttu-id="786cc-175">确保已启动下面的 Windows 服务：</span><span class="sxs-lookup"><span data-stu-id="786cc-175">Ensure that the following Windows services have been started:</span></span>  
  
    - <span data-ttu-id="786cc-176">Windows 进程激活服务 (WAS)。</span><span class="sxs-lookup"><span data-stu-id="786cc-176">Windows Process Activation Service (WAS).</span></span>  
  
    - <span data-ttu-id="786cc-177">Internet Information Services (IIS)：W3SVC。</span><span class="sxs-lookup"><span data-stu-id="786cc-177">Internet Information Services (IIS): W3SVC.</span></span>  
  
2. <span data-ttu-id="786cc-178">然后启动激活器 WasNetActivator.exe。</span><span class="sxs-lookup"><span data-stu-id="786cc-178">Then start the activator, WasNetActivator.exe.</span></span> <span data-ttu-id="786cc-179">在 " **激活** " 选项卡下，在下拉列表中选择唯一的协议 " **UDP**"。</span><span class="sxs-lookup"><span data-stu-id="786cc-179">Under the **Activation** tab, the only protocol, **UDP**, is selected in the drop down list.</span></span> <span data-ttu-id="786cc-180">单击 " **启动** " 按钮以启动激活器。</span><span class="sxs-lookup"><span data-stu-id="786cc-180">Click the **Start** button to start the activator.</span></span>  
  
3. <span data-ttu-id="786cc-181">启动激活器后，可以通过在命令窗口中运行 Client.exe 来运行客户端代码。</span><span class="sxs-lookup"><span data-stu-id="786cc-181">Once the activator is started, you can run the client code by running Client.exe from a command window.</span></span> <span data-ttu-id="786cc-182">下面是示例输出：</span><span class="sxs-lookup"><span data-stu-id="786cc-182">The following is the sample output:</span></span>  
  
    ```console  
    Testing Udp Activation.  
    Start the status service.  
    Sending UDP datagrams.  
    Type a word that you want to say to the server: Hello, world!  
        Sending datagram: Hello, world![0]  
        Sending datagram: Hello, world![1]  
        Sending datagram: Hello, world![2]  
        Sending datagram: Hello, world![3]  
        Sending datagram: Hello, world![4]  
    Calling UDP duplex contract (ICalculatorContract).  
        0 + 0 = 0  
        1 + 2 = 3  
        2 + 4 = 6  
        3 + 6 = 9  
        4 + 8 = 12  
    Getting status and dump server traces:  
        Operation 'Hello' is called: Hello, world![0]  
        Operation 'Hello' is called: Hello, world![1]  
        Operation 'Hello' is called: Hello, world![2]  
        Operation 'Hello' is called: Hello, world![3]  
        Operation 'Hello' is called: Hello, world![4]  
        Operation 'Add' is called: 0 + 0  
        Operation 'Add' is called: 1 + 2  
        Operation 'Add' is called: 2 + 4  
        Operation 'Add' is called: 3 + 6  
        Operation 'Add' is called: 4 + 8  
    Press <ENTER> to complete test.  
    ```  
  
> [!IMPORTANT]
> <span data-ttu-id="786cc-183">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="786cc-183">The samples may already be installed on your machine.</span></span> <span data-ttu-id="786cc-184">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="786cc-184">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="786cc-185">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="786cc-185">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="786cc-186">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="786cc-186">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Extensibility\Transport\UdpActivation`  
