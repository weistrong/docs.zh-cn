---
title: 服务网格-适用于 WCF 开发人员的 gRPC
description: 使用服务网格将请求路由并平衡到 Kubernetes 群集中的 gRPC 服务。
ms.date: 12/15/2020
ms.openlocfilehash: a1c72a4facf1c133af912bbee242328653a051b6
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938125"
---
# <a name="service-meshes"></a><span data-ttu-id="acdc3-103">服务网格</span><span class="sxs-lookup"><span data-stu-id="acdc3-103">Service meshes</span></span>

<span data-ttu-id="acdc3-104">服务网格是一种基础结构组件，控制网络中的路由服务请求。</span><span class="sxs-lookup"><span data-stu-id="acdc3-104">A service mesh is an infrastructure component that takes control of routing service requests within a network.</span></span> <span data-ttu-id="acdc3-105">服务网格可以处理 Kubernetes 群集中的各种网络级别问题，其中包括：</span><span class="sxs-lookup"><span data-stu-id="acdc3-105">Service meshes can handle all kinds of network-level concerns within a Kubernetes cluster, including:</span></span>

- <span data-ttu-id="acdc3-106">服务发现</span><span class="sxs-lookup"><span data-stu-id="acdc3-106">Service discovery</span></span>
- <span data-ttu-id="acdc3-107">负载均衡</span><span class="sxs-lookup"><span data-stu-id="acdc3-107">Load balancing</span></span>
- <span data-ttu-id="acdc3-108">容错</span><span class="sxs-lookup"><span data-stu-id="acdc3-108">Fault tolerance</span></span>
- <span data-ttu-id="acdc3-109">加密</span><span class="sxs-lookup"><span data-stu-id="acdc3-109">Encryption</span></span>
- <span data-ttu-id="acdc3-110">监视</span><span class="sxs-lookup"><span data-stu-id="acdc3-110">Monitoring</span></span>

<span data-ttu-id="acdc3-111">Kubernetes 服务网格通过向网格中包含的每个 pod 添加一个名为 *挎斗 proxy* 的额外容器来工作。</span><span class="sxs-lookup"><span data-stu-id="acdc3-111">Kubernetes service meshes work by adding an extra container, called a *sidecar proxy*, to each pod included in the mesh.</span></span> <span data-ttu-id="acdc3-112">代理接管了所有入站和出站网络请求的处理。</span><span class="sxs-lookup"><span data-stu-id="acdc3-112">The proxy takes over handling all inbound and outbound network requests.</span></span> <span data-ttu-id="acdc3-113">然后，你可以将网络的配置和管理与应用程序容器保持分离。</span><span class="sxs-lookup"><span data-stu-id="acdc3-113">You can then keep the configuration and management of networking matters separate from the application containers.</span></span> <span data-ttu-id="acdc3-114">在许多情况下，这种分离不需要对应用程序代码进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="acdc3-114">In many cases, this separation doesn't require any changes to the application code.</span></span>

<span data-ttu-id="acdc3-115">在 [上一章节的示例](kubernetes.md#test-the-application)中，来自 web 应用程序的 gRPC 请求全部路由到 gRPC 服务的单个实例。</span><span class="sxs-lookup"><span data-stu-id="acdc3-115">In the [previous chapter's example](kubernetes.md#test-the-application), the gRPC requests from the web application were all routed to a single instance of the gRPC service.</span></span> <span data-ttu-id="acdc3-116">出现这种情况的原因是，服务的主机名被解析为 IP 地址，并且该 IP 地址缓存在实例的生存期内 `HttpClientHandler` 。</span><span class="sxs-lookup"><span data-stu-id="acdc3-116">This happens because the service's host name is resolved to an IP address, and that IP address is cached for the lifetime of the `HttpClientHandler` instance.</span></span> <span data-ttu-id="acdc3-117">可以通过手动处理 DNS 查找或创建多个客户端来解决此行为。</span><span class="sxs-lookup"><span data-stu-id="acdc3-117">It might be possible to work around this behavior by handling DNS lookups manually or creating multiple clients.</span></span> <span data-ttu-id="acdc3-118">但这种解决方法会使应用程序代码复杂化，无需添加任何业务或客户价值。</span><span class="sxs-lookup"><span data-stu-id="acdc3-118">But this workaround would complicate the application code without adding any business or customer value.</span></span>

<span data-ttu-id="acdc3-119">使用服务网格时，来自应用程序容器的请求将发送到挎斗代理。</span><span class="sxs-lookup"><span data-stu-id="acdc3-119">When you use a service mesh, the requests from the application container are sent to the sidecar proxy.</span></span> <span data-ttu-id="acdc3-120">然后，挎斗代理可以在其他服务的所有实例中智能地分发它们。</span><span class="sxs-lookup"><span data-stu-id="acdc3-120">The sidecar proxy can then distribute them intelligently across all instances of the other service.</span></span> <span data-ttu-id="acdc3-121">网格还可以：</span><span class="sxs-lookup"><span data-stu-id="acdc3-121">The mesh can also:</span></span>

- <span data-ttu-id="acdc3-122">无缝响应服务的单个实例故障。</span><span class="sxs-lookup"><span data-stu-id="acdc3-122">Respond seamlessly to failures of individual instances of a service.</span></span>
- <span data-ttu-id="acdc3-123">处理失败调用或超时的重试语义。</span><span class="sxs-lookup"><span data-stu-id="acdc3-123">Handle retry semantics for failed calls or timeouts.</span></span>
- <span data-ttu-id="acdc3-124">将失败的请求重新路由到备用实例，而不返回到客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="acdc3-124">Reroute failed requests to an alternate instance without returning to the client application.</span></span>

<span data-ttu-id="acdc3-125">以下屏幕截图显示了在 Linkerd service 网格中运行的 StockWeb 应用程序。</span><span class="sxs-lookup"><span data-stu-id="acdc3-125">The following screenshot shows the StockWeb application running with the Linkerd service mesh.</span></span> <span data-ttu-id="acdc3-126">没有对应用程序代码进行任何更改，且未使用 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="acdc3-126">There are no changes to the application code, and the Docker image isn't being used.</span></span> <span data-ttu-id="acdc3-127">所需的唯一更改是将批注添加到部署的 YAML 文件中的 `stockdata` 和 `stockweb` 服务。</span><span class="sxs-lookup"><span data-stu-id="acdc3-127">The only change required was the addition of an annotation to the deployment in the YAML files for the `stockdata` and `stockweb` services.</span></span>

![StockWeb service 网格](media/service-mesh/stockweb-servicemesh-screenshot.png)

<span data-ttu-id="acdc3-129">尽管从 `HttpClient` 应用程序代码中的单个实例开始，但从服务器列中可以看到，来自 StockWeb 应用程序的请求已路由到 StockData 服务的两个副本。</span><span class="sxs-lookup"><span data-stu-id="acdc3-129">You can see from the **Server** column that the requests from the StockWeb application have been routed to both replicas of the StockData service, despite originating from a single `HttpClient` instance in the application code.</span></span> <span data-ttu-id="acdc3-130">事实上，如果你查看代码，你会看到，对 StockData 服务的所有100请求都是使用同一个实例同时进行的 `HttpClient` 。</span><span class="sxs-lookup"><span data-stu-id="acdc3-130">In fact, if you review the code, you'll see that all 100 requests to the StockData service are made simultaneously by using the same `HttpClient` instance.</span></span> <span data-ttu-id="acdc3-131">使用服务网格时，这些请求将在多个服务实例可用的情况下进行平衡。</span><span class="sxs-lookup"><span data-stu-id="acdc3-131">With the service mesh, those requests will be balanced across however many service instances are available.</span></span>

<span data-ttu-id="acdc3-132">服务网格仅适用于群集中的流量。</span><span class="sxs-lookup"><span data-stu-id="acdc3-132">Service meshes apply only to traffic within a cluster.</span></span> <span data-ttu-id="acdc3-133">对于外部客户端，请参阅下一章 " [负载均衡](load-balancing.md)"。</span><span class="sxs-lookup"><span data-stu-id="acdc3-133">For external clients, see the next chapter, [Load Balancing](load-balancing.md).</span></span>

## <a name="service-mesh-options"></a><span data-ttu-id="acdc3-134">服务网格选项</span><span class="sxs-lookup"><span data-stu-id="acdc3-134">Service mesh options</span></span>

<span data-ttu-id="acdc3-135">目前有三种通用服务网格实现可用于 Kubernetes： [Istio](https://istio.io)、 [Linkerd](https://linkerd.io)和 [Consul Connect](https://consul.io/mesh.html)。</span><span class="sxs-lookup"><span data-stu-id="acdc3-135">Three general-purpose service mesh implementations are currently available for use with Kubernetes: [Istio](https://istio.io), [Linkerd](https://linkerd.io), and [Consul Connect](https://consul.io/mesh.html).</span></span> <span data-ttu-id="acdc3-136">所有三个都提供请求路由/代理、通信加密、复原、主机到主机身份验证和流量控制。</span><span class="sxs-lookup"><span data-stu-id="acdc3-136">All three provide request routing/proxying, traffic encryption, resilience, host-to-host authentication, and traffic control.</span></span>

<span data-ttu-id="acdc3-137">选择服务网格取决于多个因素：</span><span class="sxs-lookup"><span data-stu-id="acdc3-137">Choosing a service mesh depends on multiple factors:</span></span>

- <span data-ttu-id="acdc3-138">组织对成本、符合性、付费支持计划等的特定要求。</span><span class="sxs-lookup"><span data-stu-id="acdc3-138">The organization's specific requirements around costs, compliance, paid support plans, and so on.</span></span>
- <span data-ttu-id="acdc3-139">群集的性质、其大小、部署的服务数量和群集网络中的流量。</span><span class="sxs-lookup"><span data-stu-id="acdc3-139">The nature of the cluster, its size, the number of services deployed, and the volume of traffic within the cluster network.</span></span>
- <span data-ttu-id="acdc3-140">轻松部署和管理网格，并将其用于服务。</span><span class="sxs-lookup"><span data-stu-id="acdc3-140">Ease of deploying and managing the mesh and using it with services.</span></span>

## <a name="example-add-linkerd-to-a-deployment"></a><span data-ttu-id="acdc3-141">示例：将 Linkerd 添加到部署</span><span class="sxs-lookup"><span data-stu-id="acdc3-141">Example: Add Linkerd to a deployment</span></span>

<span data-ttu-id="acdc3-142">在此示例中，你将了解如何将 Linkerd service 网格与 [上一节](kubernetes.md)中的 *StockKube* 应用程序一起使用。</span><span class="sxs-lookup"><span data-stu-id="acdc3-142">In this example, you'll learn how to use the Linkerd service mesh with the *StockKube* application from [the previous section](kubernetes.md).</span></span>
<span data-ttu-id="acdc3-143">若要执行此示例，需要 [安装 LINKERD CLI](https://linkerd.io/2/getting-started/#step-1-install-the-cli)。</span><span class="sxs-lookup"><span data-stu-id="acdc3-143">To follow this example, you'll need to [install the Linkerd CLI](https://linkerd.io/2/getting-started/#step-1-install-the-cli).</span></span> <span data-ttu-id="acdc3-144">你可以从列出 GitHub 版本的部分下载 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="acdc3-144">You can download Windows binaries from the section that lists GitHub releases.</span></span> <span data-ttu-id="acdc3-145">请确保使用最新的 *稳定* 版本，而不是边缘版本之一。</span><span class="sxs-lookup"><span data-stu-id="acdc3-145">Be sure to use the most recent *stable* release and not one of the edge releases.</span></span>

<span data-ttu-id="acdc3-146">安装 Linkerd CLI 后，请按照 [入门](https://linkerd.io/2/getting-started/index.html) 说明在 Kubernetes 群集上安装 Linkerd 组件。</span><span class="sxs-lookup"><span data-stu-id="acdc3-146">With the Linkerd CLI installed, follow the [Getting Started](https://linkerd.io/2/getting-started/index.html) instructions to install the Linkerd components on your Kubernetes cluster.</span></span> <span data-ttu-id="acdc3-147">说明非常简单，并且在本地 Kubernetes 实例上安装只需几分钟即可完成。</span><span class="sxs-lookup"><span data-stu-id="acdc3-147">The instructions are straightforward, and the installation should take only a couple of minutes on a local Kubernetes instance.</span></span>

### <a name="add-linkerd-to-kubernetes-deployments"></a><span data-ttu-id="acdc3-148">将 Linkerd 添加到 Kubernetes 部署</span><span class="sxs-lookup"><span data-stu-id="acdc3-148">Add Linkerd to Kubernetes deployments</span></span>

<span data-ttu-id="acdc3-149">Linkerd CLI 提供了一个 `inject` 命令，用于将必要的节和属性添加到 Kubernetes 文件。</span><span class="sxs-lookup"><span data-stu-id="acdc3-149">The Linkerd CLI provides an `inject` command to add the necessary sections and properties to Kubernetes files.</span></span> <span data-ttu-id="acdc3-150">您可以运行该命令并将输出写入到新文件中。</span><span class="sxs-lookup"><span data-stu-id="acdc3-150">You can run the command and write the output to a new file.</span></span>

```console
linkerd inject stockdata.yml > stockdata-with-mesh.yml
linkerd inject stockweb.yml > stockweb-with-mesh.yml
```

<span data-ttu-id="acdc3-151">您可以检查新文件，以查看所做的更改。</span><span class="sxs-lookup"><span data-stu-id="acdc3-151">You can inspect the new files to see what changes have been made.</span></span> <span data-ttu-id="acdc3-152">对于部署对象，添加了元数据批注，告诉 Linkerd 在创建时将挎斗代理容器注入到 pod。</span><span class="sxs-lookup"><span data-stu-id="acdc3-152">For deployment objects, a metadata annotation is added to tell Linkerd to inject a sidecar proxy container into the pod when it's created.</span></span>

<span data-ttu-id="acdc3-153">还可以直接通过管道将命令输出传递 `linkerd inject` 给 `kubectl` 。</span><span class="sxs-lookup"><span data-stu-id="acdc3-153">It's also possible to pipe the output of the `linkerd inject` command to `kubectl` directly.</span></span> <span data-ttu-id="acdc3-154">以下命令将在 PowerShell 或任何 Linux shell 中运行。</span><span class="sxs-lookup"><span data-stu-id="acdc3-154">The following commands will work in PowerShell or any Linux shell.</span></span>

```console
linkerd inject stockdata.yml | kubectl apply -f -
linkerd inject stockweb.yml | kubectl apply -f -
```

### <a name="inspect-services-in-the-linkerd-dashboard"></a><span data-ttu-id="acdc3-155">在 Linkerd 仪表板中检查服务</span><span class="sxs-lookup"><span data-stu-id="acdc3-155">Inspect services in the Linkerd dashboard</span></span>

<span data-ttu-id="acdc3-156">使用 CLI 打开 Linkerd 仪表板 `linkerd` 。</span><span class="sxs-lookup"><span data-stu-id="acdc3-156">Open the Linkerd dashboard by using the `linkerd` CLI.</span></span>

```console
linkerd dashboard
```

<span data-ttu-id="acdc3-157">该仪表板提供有关连接到网格的所有服务的详细信息。</span><span class="sxs-lookup"><span data-stu-id="acdc3-157">The dashboard provides detailed information about all services that are connected to the mesh.</span></span>

![显示 StockKube 应用程序的 Linkerd 仪表板](media/service-mesh/linkerd-screenshot.png)

<span data-ttu-id="acdc3-159">如果按以下示例所示增加 StockData gRPC 服务的副本数，并在浏览器中刷新 StockWeb 页，则应在 **服务器** 列中看到 id 的混合。</span><span class="sxs-lookup"><span data-stu-id="acdc3-159">If you increase the number of replicas of the StockData gRPC service as shown in the following example, and refresh the StockWeb page in the browser, you should see a mix of IDs in the **Server** column.</span></span> <span data-ttu-id="acdc3-160">这种组合表明所有可用实例都为请求提供服务。</span><span class="sxs-lookup"><span data-stu-id="acdc3-160">This mix indicates that all the available instances are serving requests.</span></span>

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: stockdata
  namespace: stocks
spec:
  selector:
    matchLabels:
      run: stockdata
  replicas: 2 # Increase the target number of instances
  template:
    metadata:
      annotations:
        linkerd.io/inject: enabled
      creationTimestamp: null
      labels:
        run: stockdata
    spec:
      containers:
      - name: stockdata
        image: stockdata:1.0.0
        imagePullPolicy: Never
        resources:
          limits:
            cpu: 100m
            memory: 100Mi
        ports:
        - containerPort: 80
```

>[!div class="step-by-step"]
><span data-ttu-id="acdc3-161">[上一页](kubernetes.md)
>[下一页](load-balancing.md)</span><span class="sxs-lookup"><span data-stu-id="acdc3-161">[Previous](kubernetes.md)
[Next](load-balancing.md)</span></span>
