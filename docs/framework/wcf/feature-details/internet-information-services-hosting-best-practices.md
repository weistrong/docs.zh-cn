---
description: 了解详细信息： Internet Information Services 托管最佳实践
title: Internet 信息服务承载最佳实践
ms.date: 03/30/2017
ms.assetid: 0834768e-9665-46bf-86eb-d4b09ab91af5
ms.openlocfilehash: 6a17d28977fba83d50e54672fa8e79979f130c4d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802744"
---
# <a name="internet-information-services-hosting-best-practices"></a><span data-ttu-id="26dc6-103">Internet 信息服务承载最佳实践</span><span class="sxs-lookup"><span data-stu-id="26dc6-103">Internet Information Services Hosting Best Practices</span></span>

<span data-ttu-id="26dc6-104">本主题概述了 Windows Communication Foundation (WCF) 服务中承载的最佳实践。</span><span class="sxs-lookup"><span data-stu-id="26dc6-104">This topic outlines some best practices for hosting Windows Communication Foundation (WCF) services.</span></span>  
  
## <a name="implementing-wcf-services-as-dlls"></a><span data-ttu-id="26dc6-105">将 WCF 服务实现为 DLL</span><span class="sxs-lookup"><span data-stu-id="26dc6-105">Implementing WCF Services as DLLs</span></span>  

 <span data-ttu-id="26dc6-106">如果将 WCF 服务实现为部署到 Web 应用程序的 \bin 目录的 DLL，则可以在 Web 应用程序模型之外重用该服务，例如，在可能未部署 (IIS) Internet Information Services 测试环境中。</span><span class="sxs-lookup"><span data-stu-id="26dc6-106">Implementing a WCF service as a DLL that is deployed to the \bin directory of a Web application allows you reuse the service outside of the Web application model, for example, in a test environment that may not have Internet Information Services (IIS) deployed.</span></span>  
  
## <a name="service-hosts-in-iis-hosted-applications"></a><span data-ttu-id="26dc6-107">承载于 IIS 中的应用程序中的服务主机</span><span class="sxs-lookup"><span data-stu-id="26dc6-107">Service Hosts in IIS-Hosted Applications</span></span>  

 <span data-ttu-id="26dc6-108">不要使用命令式自宿主 Api 来创建新的服务主机，这些主机在 iis 宿主环境中不受本机支持的网络传输上进行侦听 (例如，IIS 6.0 来托管 TCP 服务，因为 IIS 6.0) 在本机上不支持 TCP 通信。</span><span class="sxs-lookup"><span data-stu-id="26dc6-108">Do not use the imperative self-host APIs to create new service hosts that listen on network transports not natively supported by the IIS hosting environment (For example, IIS 6.0 to host TCP services, because TCP communication is not natively supported on IIS 6.0).</span></span> <span data-ttu-id="26dc6-109">不建议使用此方法。</span><span class="sxs-lookup"><span data-stu-id="26dc6-109">This approach is not recommended.</span></span> <span data-ttu-id="26dc6-110">强制创建的服务主机在 IIS 承载环境内是未知的。</span><span class="sxs-lookup"><span data-stu-id="26dc6-110">Service hosts created imperatively are not known within the IIS hosting environment.</span></span> <span data-ttu-id="26dc6-111">很重要的一点是，在 IIS 确定承载应用程序池是否空闲时，它未说明强制创建的服务所进行的处理。</span><span class="sxs-lookup"><span data-stu-id="26dc6-111">The critical point is that processing done by imperatively created services is not accounted for by IIS when it determines whether the hosting application pool is idle.</span></span> <span data-ttu-id="26dc6-112">结果是具有这样强制创建的服务主机的应用程序具有主动处置 IIS 托管进程的 IIS 承载环境。</span><span class="sxs-lookup"><span data-stu-id="26dc6-112">The result is that applications that have such imperatively created service hosts have an IIS hosting environment that aggressively disposes of IIS host processes.</span></span>  
  
## <a name="uris-and-iis-hosted-endpoints"></a><span data-ttu-id="26dc6-113">URI 和承载于 IIS 中的终结点</span><span class="sxs-lookup"><span data-stu-id="26dc6-113">URIs and IIS-Hosted Endpoints</span></span>  

 <span data-ttu-id="26dc6-114">承载于 IIS 中的服务的终结点应该使用相对统一资源标识符 (URI) 而不是绝对地址进行配置。</span><span class="sxs-lookup"><span data-stu-id="26dc6-114">Endpoints for an IIS-hosted service should be configured using relative Uniform Resource Identifiers (URIs), not absolute addresses.</span></span> <span data-ttu-id="26dc6-115">这保证终结点地址在属于承载应用程序的 URI 地址集范围内，并确保像预期的那样发生基于消息的激活。</span><span class="sxs-lookup"><span data-stu-id="26dc6-115">This guarantees that the endpoint address falls within the set of URI addresses that belong to the hosting application and ensures that message-based activation happens as expected.</span></span>  
  
## <a name="state-management-and-process-recycling"></a><span data-ttu-id="26dc6-116">状态管理和进程回收</span><span class="sxs-lookup"><span data-stu-id="26dc6-116">State Management and Process Recycling</span></span>  

 <span data-ttu-id="26dc6-117">为不在内存中维护本地状态的服务优化了 IIS 承载环境。</span><span class="sxs-lookup"><span data-stu-id="26dc6-117">The IIS hosting environment is optimized for services that do not maintain local state in memory.</span></span> <span data-ttu-id="26dc6-118">IIS 回收托管进程以响应各种外部和内部事件，导致仅存储在内存中的任何可变状态丢失。</span><span class="sxs-lookup"><span data-stu-id="26dc6-118">IIS recycles the host process in response to a variety of external and internal events, causing any volatile state stored exclusively in memory to be lost.</span></span> <span data-ttu-id="26dc6-119">寄宿在 IIS 中的服务应该在进程外存储其状态（例如，在数据库中），或者在出现应用程序回收事件时可以轻松重新创建的内存中缓存中存储其状态。</span><span class="sxs-lookup"><span data-stu-id="26dc6-119">Services hosted in IIS should store their state external to the process (for example, in a database) or in an in-memory cache that can easily be re-created if an application recycle event occurs.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="26dc6-120">WCF 用于消息层可靠性和安全性的协议利用可变的内存中状态。</span><span class="sxs-lookup"><span data-stu-id="26dc6-120">The protocols WCF uses for message-layer reliability and security make use of the volatile in-memory state.</span></span> <span data-ttu-id="26dc6-121">WCF 可靠会话和安全会话可能由于应用程序回收而意外终止。</span><span class="sxs-lookup"><span data-stu-id="26dc6-121">WCF reliable sessions and security sessions may terminate unexpectedly due to application recycles.</span></span> <span data-ttu-id="26dc6-122">使用这些协议的 IIS 托管的应用程序应该依赖于 WCF 提供的会话密钥来关联应用层状态 (例如，应用层构造或自定义相关标头) 或为托管应用程序禁用 IIS 进程回收。</span><span class="sxs-lookup"><span data-stu-id="26dc6-122">IIS-hosted applications that make use of these protocols should either depend on something other than the WCF-provided session key for correlating application-layer state (for example, an application-layer construct or custom correlation header) or disable IIS process recycling for the hosted application.</span></span>  
  
## <a name="optimizing-performance-in-middle-tier-scenarios"></a><span data-ttu-id="26dc6-123">在中间层方案中优化性能</span><span class="sxs-lookup"><span data-stu-id="26dc6-123">Optimizing Performance in Middle-Tier Scenarios</span></span>  

 <span data-ttu-id="26dc6-124">若要在 *中间层方案* 中实现最佳性能（一项服务，该服务为响应传入消息而调用其他服务），请一次将 WCF 服务客户端实例化到远程服务，并跨多个传入请求重复使用它。</span><span class="sxs-lookup"><span data-stu-id="26dc6-124">For optimal performance in a *middle-tier scenario*—a service that calls out to other services in response to incoming messages—instantiate the WCF service client to the remote service once and reuse it across multiple incoming requests.</span></span> <span data-ttu-id="26dc6-125">实例化 WCF 服务客户端是一项成本高昂的操作，相对于对预先存在的客户端实例进行服务调用，中间层方案通过跨请求缓存远程客户端来产生明显的性能提升。</span><span class="sxs-lookup"><span data-stu-id="26dc6-125">Instantiating WCF service clients is an expensive operation relative to making a service call on a pre-existing client instance, and middle-tier scenarios produce distinct performance gains by caching remote clients across requests.</span></span> <span data-ttu-id="26dc6-126">WCF 服务客户端是线程安全的，因此不必跨多个线程同步对客户端的访问。</span><span class="sxs-lookup"><span data-stu-id="26dc6-126">WCF service clients are thread-safe, so it is not necessary to synchronize access to a client across multiple threads.</span></span>  
  
 <span data-ttu-id="26dc6-127">中间层方案还通过使用由 `svcutil /a` 选项生成的异步 API 来产生性能提升。</span><span class="sxs-lookup"><span data-stu-id="26dc6-127">Middle-tier scenarios also produce performance gains by using the asynchronous APIs generated by the `svcutil /a` option.</span></span> <span data-ttu-id="26dc6-128">`/a`选项会使 "工作项[元数据实用工具" 工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md)为 `BeginXXX/EndXXX` 每个服务操作生成方法，这允许在后台线程上进行远程服务的可能长时间运行的调用。</span><span class="sxs-lookup"><span data-stu-id="26dc6-128">The `/a` option causes the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to generate `BeginXXX/EndXXX` methods for each service operation, which allows potentially long-running calls to remote services to be made on background threads.</span></span>  
  
## <a name="wcf-in-multi-homed-or-multi-named-scenarios"></a><span data-ttu-id="26dc6-129">多宿主或多名称方案中的 WCF</span><span class="sxs-lookup"><span data-stu-id="26dc6-129">WCF in Multi-Homed or Multi-named scenarios</span></span>  

 <span data-ttu-id="26dc6-130">你可以在 IIS Web 场中部署 WCF 服务，其中一组计算机共享公用外部名称 (例如 `http://www.contoso.com`) ，但由不同的主机名单独寻址 (例如， `http://www.contoso.com` 可能会将流量定向到名为和) 两个不同的计算机 `http://machine1.internal.contoso.com` `http://machine2.internal.contoso.com` 。</span><span class="sxs-lookup"><span data-stu-id="26dc6-130">You can deploy WCF services inside of an IIS Web farm, where a set of computers share a common external name (such as `http://www.contoso.com`) but are individually addressed by different hostnames (for example, `http://www.contoso.com` might direct traffic to two different machines named `http://machine1.internal.contoso.com` and `http://machine2.internal.contoso.com`).</span></span> <span data-ttu-id="26dc6-131">WCF 完全支持此部署方案，但需要对承载 WCF 服务的 IIS 网站进行特殊配置，才能在服务的元数据 (Web Services 描述语言) 中显示正确的 (外部) 主机名。</span><span class="sxs-lookup"><span data-stu-id="26dc6-131">This deployment scenario is fully supported by WCF, but requires special configuration of the IIS Web site hosting WCF services to display the correct (external) hostname in the service's metadata (Web Services Description Language).</span></span>  
  
 <span data-ttu-id="26dc6-132">若要确保服务元数据中出现正确的主机名，WCF 将生成，请将承载 WCF 服务的 IIS 网站的默认标识配置为使用显式主机名。</span><span class="sxs-lookup"><span data-stu-id="26dc6-132">To ensure that the correct hostname appears in the service metadata WCF generates, configure the default identity for the IIS Web site that hosts WCF services to use an explicit hostname.</span></span> <span data-ttu-id="26dc6-133">例如，驻留在场中的计算机 `www.contoso.com` 应使用 \*：80： www .com FOR HTTP 的 IIS 网站绑定，并使用 \* ：443： www .COM for HTTPS。</span><span class="sxs-lookup"><span data-stu-id="26dc6-133">For example, computers that reside inside of the `www.contoso.com` farm should use an IIS site binding of \*:80:www.contoso.com for HTTP and \*:443:www.contoso.com for HTTPS.</span></span>  
  
 <span data-ttu-id="26dc6-134">可以使用 IIS Microsoft 管理控制台 (MMC) 管理单元配置 IIS 网站绑定。</span><span class="sxs-lookup"><span data-stu-id="26dc6-134">You can configure IIS Web site bindings by using the IIS Microsoft Management Console (MMC) snap-in.</span></span>  
  
## <a name="application-pools-running-in-different-user-contexts-overwrite-assemblies-from-other-accounts-in-the-temporary-folder"></a><span data-ttu-id="26dc6-135">在不同用户上下文中运行的应用程序池覆盖来自临时文件夹中其他帐户的程序集</span><span class="sxs-lookup"><span data-stu-id="26dc6-135">Application Pools Running in Different User Contexts Overwrite Assemblies from Other Accounts in the Temporary Folder</span></span>  

 <span data-ttu-id="26dc6-136">若要确保在不同用户上下文中运行的应用程序池无法覆盖临时 ASP.NET files 文件夹中其他帐户的程序集，请对不同的应用程序使用不同的标识和临时文件夹。</span><span class="sxs-lookup"><span data-stu-id="26dc6-136">To ensure that application pools running in different user contexts cannot overwrite assemblies from other accounts in the temporary ASP.NET files folder, use different identities and temporary folders for different applications.</span></span> <span data-ttu-id="26dc6-137">例如，如果具有两个虚拟应用程序 /Application1 和 / Application2，则可以创建两个应用程序池 A 和 B，它们具有不同的标识。</span><span class="sxs-lookup"><span data-stu-id="26dc6-137">For example, if you have two virtual applications /Application1 and / Application2, you can create two Application pools, A and B, with two different identities.</span></span> <span data-ttu-id="26dc6-138">应用程序池 A 可以使用一个用户标识 (user1) 运行，而应用程序池 B 可以使用其他用户标识 (user2) 运行，并将 /Application1 配置为使用 A，将 /Application2 配置为使用 B。</span><span class="sxs-lookup"><span data-stu-id="26dc6-138">Application pool A can run under one user identity (user1) while application pool B can run under another user identity (user2), and configure /Application1 to use A and /Application2 to use B.</span></span>  
  
 <span data-ttu-id="26dc6-139">在 Web.config 中，你可以使用配置临时文件夹 \<system.web/compilation/@tempFolder> 。</span><span class="sxs-lookup"><span data-stu-id="26dc6-139">In Web.config, you can configure the temporary folder using \<system.web/compilation/@tempFolder>.</span></span> <span data-ttu-id="26dc6-140">对于/Application1，可以是 "c:\tempForUser1"，对于 application2，它可以是 "c:\tempForUser2"。</span><span class="sxs-lookup"><span data-stu-id="26dc6-140">For /Application1, it can be "c:\tempForUser1" and for application2 it can be "c:\tempForUser2".</span></span> <span data-ttu-id="26dc6-141">将相应的写入权限授予两个标识的这些文件夹。</span><span class="sxs-lookup"><span data-stu-id="26dc6-141">Grant corresponding write permission to these folders for the two identities.</span></span>  
  
 <span data-ttu-id="26dc6-142">之后，user2 无法更改 /application2 的代码生成文件夹（在 c:\tempForUser1 下）。</span><span class="sxs-lookup"><span data-stu-id="26dc6-142">Then user2 cannot change the code-generation folder for /application2 (under c:\tempForUser1).</span></span>  
  
## <a name="enabling-asynchronous-processing"></a><span data-ttu-id="26dc6-143">启用异步处理</span><span class="sxs-lookup"><span data-stu-id="26dc6-143">Enabling asynchronous processing</span></span>  

 <span data-ttu-id="26dc6-144">默认情况下，会以同步方式处理发送到在 IIS 6.0 和更早版本下承载的 WCF 服务的消息。</span><span class="sxs-lookup"><span data-stu-id="26dc6-144">By default messages sent to a WCF service hosted under IIS 6.0 and earlier are processed in a synchronous manner.</span></span> <span data-ttu-id="26dc6-145">ASP.NET 在 ASP.NET 工作) 线程 (的线程上调用 WCF，并使用其他线程处理请求。</span><span class="sxs-lookup"><span data-stu-id="26dc6-145">ASP.NET calls into WCF on its own thread (the ASP.NET worker thread) and WCF uses another thread to process the request.</span></span> <span data-ttu-id="26dc6-146">WCF 在完成其处理之前会保持 ASP.NET 工作线程。</span><span class="sxs-lookup"><span data-stu-id="26dc6-146">WCF holds onto the ASP.NET worker thread until it completes its processing.</span></span> <span data-ttu-id="26dc6-147">这将导致同步处理请求。</span><span class="sxs-lookup"><span data-stu-id="26dc6-147">This leads to synchronous processing of requests.</span></span> <span data-ttu-id="26dc6-148">异步处理请求可实现更高的可伸缩性，因为它可减少处理请求所需的线程数–在处理请求时，WCF 不会保存到 ASP.NET 线程。</span><span class="sxs-lookup"><span data-stu-id="26dc6-148">Processing requests asynchronously enables greater scalability because it reduces the number of threads required to process a request –WCF does not hold on to the ASP.NET thread while processing the request.</span></span> <span data-ttu-id="26dc6-149">对于运行 IIS 6.0 的计算机，不建议使用异步行为，因为无法限制打开 *服务器 (DOS) 攻击的传入* 请求。</span><span class="sxs-lookup"><span data-stu-id="26dc6-149">Use of asynchronous behavior is not recommended for machines running IIS 6.0 because there is no way to throttle incoming requests that open up the server to *Denial Of Service* (DOS) attacks.</span></span> <span data-ttu-id="26dc6-150">从 IIS 7.0 开始，引入了并发请求限制：`[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ASP.NET\2.0.50727.0]"MaxConcurrentRequestsPerCpu`。</span><span class="sxs-lookup"><span data-stu-id="26dc6-150">Starting with IIS 7.0, a concurrent request throttle has been introduced: `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ASP.NET\2.0.50727.0]"MaxConcurrentRequestsPerCpu`.</span></span> <span data-ttu-id="26dc6-151">借助这一新的限制，可安全地使用异步处理。</span><span class="sxs-lookup"><span data-stu-id="26dc6-151">With this new throttle it is safe to use the asynchronous processing.</span></span>  <span data-ttu-id="26dc6-152">默认情况下，在 IIS 7.0 中会注册异步处理程序和模块。</span><span class="sxs-lookup"><span data-stu-id="26dc6-152">By default in IIS 7.0, the asynchronous handler and module are registered.</span></span> <span data-ttu-id="26dc6-153">如果关闭了此功能，可在应用程序的 Web.config 文件中手动启用对请求的异步处理。</span><span class="sxs-lookup"><span data-stu-id="26dc6-153">If this has been turned off, you can manually enable asynchronous processing of requests in your application's Web.config file.</span></span> <span data-ttu-id="26dc6-154">所使用的设置取决于 `aspNetCompatibilityEnabled` 设置。</span><span class="sxs-lookup"><span data-stu-id="26dc6-154">The settings you use depend on your `aspNetCompatibilityEnabled` setting.</span></span> <span data-ttu-id="26dc6-155">如果已将 `aspNetCompatibilityEnabled` 设置为 `false`，请按照下面的配置代码段所示配置 `System.ServiceModel.Activation.ServiceHttpModule`。</span><span class="sxs-lookup"><span data-stu-id="26dc6-155">If you have `aspNetCompatibilityEnabled` set to `false`, configure the `System.ServiceModel.Activation.ServiceHttpModule` as shown in the following configuration snippet.</span></span>  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="false" />
  </system.serviceModel>  
  <system.webServer>  
    <modules>  
      <remove name="ServiceModel"/>  
      <add name="ServiceModel"
           preCondition="integratedMode,runtimeVersionv2.0"
           type="System.ServiceModel.Activation.ServiceHttpModule, System.ServiceModel,Version=3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>  
    </modules>  
    </system.webServer>  
```  
  
 <span data-ttu-id="26dc6-156">如果已将 `aspNetCompatibilityEnabled` 设置为 `true`，请按照下面的配置代码段所示配置 `System.ServiceModel.Activation.ServiceHttpHandlerFactory`。</span><span class="sxs-lookup"><span data-stu-id="26dc6-156">If you have `aspNetCompatibilityEnabled` set to `true`, configure the `System.ServiceModel.Activation.ServiceHttpHandlerFactory` as shown in the following config snippet.</span></span>  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="true" />
  </system.serviceModel>  
  <system.webServer>  
    <handlers>  
          <clear/>  
          <add name="TestAsyncHttpHandler"
               path="*.svc"
               verb="*"
               type="System.ServiceModel.Activation.ServiceHttpHandlerFactory, System.ServiceModel, Version=3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"
               />  
    </handlers>
  </system.webServer>  
```  
  
## <a name="see-also"></a><span data-ttu-id="26dc6-157">请参阅</span><span class="sxs-lookup"><span data-stu-id="26dc6-157">See also</span></span>

- [<span data-ttu-id="26dc6-158">服务承载示例</span><span class="sxs-lookup"><span data-stu-id="26dc6-158">Service Hosting Samples</span></span>](../samples/hosting.md)
- <span data-ttu-id="26dc6-159">[Windows Server App Fabric 承载功能](/previous-versions/appfabric/ee677189(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="26dc6-159">[Windows Server App Fabric Hosting Features](/previous-versions/appfabric/ee677189(v=azure.10))</span></span>
