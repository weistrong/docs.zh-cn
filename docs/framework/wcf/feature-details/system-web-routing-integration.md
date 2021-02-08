---
description: 了解详细信息： System.web. 路由集成
title: System.Web.Routing 集成
ms.date: 03/30/2017
ms.assetid: 31fe2a4f-5c47-4e5d-8ee1-84c524609d41
ms.openlocfilehash: 8f396d5a3cad30f5cc67cb0cf44fad76a0bb54c9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793332"
---
# <a name="systemwebrouting-integration"></a><span data-ttu-id="db817-103">System.Web.Routing 集成</span><span class="sxs-lookup"><span data-stu-id="db817-103">System.Web.Routing Integration</span></span>

<span data-ttu-id="db817-104">在 Internet 信息服务 () IIS 中承载 Windows Communication Foundation (WCF) 服务时，会将 .svc 文件放在虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="db817-104">When hosting a Windows Communication Foundation (WCF) service in Internet Information Service (IIS) you place a .svc file in the virtual directory.</span></span> <span data-ttu-id="db817-105">此 .svc 文件指定所用的服务主机工厂以及实现服务的类。</span><span class="sxs-lookup"><span data-stu-id="db817-105">This .svc file specifies the service host factory to use as well as the class that implements the service.</span></span> <span data-ttu-id="db817-106">向服务发出请求时，请在 URI 中指定 .svc 文件，例如： `http://contoso.com/EmployeeServce.svc` 。</span><span class="sxs-lookup"><span data-stu-id="db817-106">When making requests to the service you specify the .svc file in the URI, for example: `http://contoso.com/EmployeeServce.svc`.</span></span> <span data-ttu-id="db817-107">对于编写 REST 服务的程序员，此类型的 URI 并非最佳选择。</span><span class="sxs-lookup"><span data-stu-id="db817-107">For programmers writing REST services, this type of URI is not optimal.</span></span> <span data-ttu-id="db817-108">REST 服务的 URI 指定了特定资源，通常没有任何扩展。</span><span class="sxs-lookup"><span data-stu-id="db817-108">URIs for REST services specify a specific resource and normally do not have any extensions.</span></span> <span data-ttu-id="db817-109"><xref:System.Web.Routing>集成功能允许托管 WCF REST 服务，该服务在没有扩展的情况下响应 uri。</span><span class="sxs-lookup"><span data-stu-id="db817-109">The <xref:System.Web.Routing> integration feature allows you to host a WCF REST service that responds to URIs without an extension.</span></span> <span data-ttu-id="db817-110">有关路由的详细信息，请参阅 [ASP.NET 路由](/previous-versions/aspnet/cc668201(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="db817-110">For more information about routing see [ASP.NET Routing](/previous-versions/aspnet/cc668201(v=vs.100)).</span></span>  
  
## <a name="using-systemwebrouting-integration"></a><span data-ttu-id="db817-111">使用 System.Web.Routing 集成</span><span class="sxs-lookup"><span data-stu-id="db817-111">Using System.Web.Routing Integration</span></span>  

 <span data-ttu-id="db817-112">若要使用 <xref:System.Web.Routing> 集成功能，请使用 <xref:System.ServiceModel.Activation.ServiceRoute> 类创建一个或多个路由，然后将这些路由添加到 Global.asax 文件中的 <xref:System.Web.Routing.RouteTable>。</span><span class="sxs-lookup"><span data-stu-id="db817-112">To use the <xref:System.Web.Routing> integration feature, you use the <xref:System.ServiceModel.Activation.ServiceRoute> class to create one or more routes and add them to the <xref:System.Web.Routing.RouteTable> in a Global.asax file.</span></span> <span data-ttu-id="db817-113">这些路由可指定服务所响应的相对 URI。</span><span class="sxs-lookup"><span data-stu-id="db817-113">These routes specify the relative URIs that the service responds to.</span></span> <span data-ttu-id="db817-114">以下示例演示如何执行此操作。</span><span class="sxs-lookup"><span data-stu-id="db817-114">The following example shows how to do this.</span></span>  
  
```aspx-csharp  
<%@ Application Language="C#" %>  
<%@ Import Namespace="System.Web.Routing" %>  
<%@ Import Namespace="System.ServiceModel.Activation" %>  
<%@ Import Namespace="System.ServiceModel.Web " %>  
  
<script RunAt="server">  
    void Application_Start(object sender, EventArgs e)  
    {  
        RegisterRoutes(RouteTable.Routes);  
    }  
  
    private void RegisterRoutes(RouteCollection routes)  
    {  
        routes.Add(new ServiceRoute("Customers", new WebServiceHostFactory(), typeof(Service)));
   }  
</script>  
```  
  
 <span data-ttu-id="db817-115">这示例将具有以 Customers 开头的相对 URI 的所有请求路由到 `Service` 服务。</span><span class="sxs-lookup"><span data-stu-id="db817-115">This routes all requests with a relative URI that begins with Customers to the `Service` service.</span></span>  
  
 <span data-ttu-id="db817-116">在 Web.config 文件中，必须添加 `System.Web.Routing.UrlRoutingModule` 模块，将 `runAllManagedModulesForAllRequests` 特性设置为 `true`，以及将 `UrlRoutingHandler` 处理程序添加到 `<system.webServer>` 元素，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="db817-116">In your Web.config file you must add the `System.Web.Routing.UrlRoutingModule` module, set the `runAllManagedModulesForAllRequests` attribute to `true`, and add the `UrlRoutingHandler` handler to the `<system.webServer>` element as shown in the following example.</span></span>  
  
```xml  
<system.webServer>  
      <modules runAllManagedModulesForAllRequests="true">  
        <add name="UrlRoutingModule" type="System.Web.Routing.UrlRoutingModule, System.Web, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a" />  
      </modules>  
      <handlers>  
        <add name="UrlRoutingHandler" preCondition="integratedMode" verb="*" path="UrlRouting.axd"/>  
      </handlers>  
    </system.webServer>  
```  
  
 <span data-ttu-id="db817-117">此示例将加载路由所需的模块和处理程序。</span><span class="sxs-lookup"><span data-stu-id="db817-117">This loads a module and handler required for routing.</span></span> <span data-ttu-id="db817-118">有关详细信息，请参阅[路由](routing.md)。</span><span class="sxs-lookup"><span data-stu-id="db817-118">For more information, see [Routing](routing.md).</span></span> <span data-ttu-id="db817-119">另外，还必须在 `aspNetCompatibilityEnabled` 元素中将 `true` 特性设置为 `<serviceHostingEnvironment>`，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="db817-119">You must also set the `aspNetCompatibilityEnabled` attribute to `true` in the `<serviceHostingEnvironment>` element as shown in the following example.</span></span>  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="true"/>  
        <!-- ... -->  
    </system.serviceModel>  
```  
  
 <span data-ttu-id="db817-120">实现该服务的类必须启用 ASP.NET 兼容性需求，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="db817-120">The class that implements the service must enable ASP.NET compatibility requirements as shown in the following example.</span></span>  
  
```csharp
[ServiceContract]  
[AspNetCompatibilityRequirements(RequirementsMode=AspNetCompatibilityRequirementsMode.Allowed)]  
    public class Service  
    {  
        // ...  
    }  
```  
  
## <a name="see-also"></a><span data-ttu-id="db817-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="db817-121">See also</span></span>

- [<span data-ttu-id="db817-122">WCF Web HTTP 编程模型</span><span class="sxs-lookup"><span data-stu-id="db817-122">WCF Web HTTP Programming Model</span></span>](wcf-web-http-programming-model.md)
- <span data-ttu-id="db817-123">[ASP.NET 路由](/previous-versions/aspnet/cc668201(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db817-123">[ASP.NET Routing](/previous-versions/aspnet/cc668201(v=vs.100))</span></span>
