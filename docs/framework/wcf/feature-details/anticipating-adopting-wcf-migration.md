---
description: 了解更多相关信息：预见采用 Windows Communication Foundation：简化未来迁移
title: Windows Communication Foundation 使用展望：轻松实现未来的迁移
ms.date: 03/30/2017
ms.assetid: f49664d9-e9e0-425c-a259-93f0a569d01b
ms.openlocfilehash: 6ea81b1dd01ed45ff62fa50c1b17442f88fc05af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643808"
---
# <a name="anticipating-adopting-the-windows-communication-foundation-easing-future-migration"></a><span data-ttu-id="f4ef0-103">Windows Communication Foundation 使用展望：轻松实现未来的迁移</span><span class="sxs-lookup"><span data-stu-id="f4ef0-103">Anticipating Adopting the Windows Communication Foundation: Easing Future Migration</span></span>

<span data-ttu-id="f4ef0-104">若要确保更方便地将新的 ASP.NET 应用程序迁移到 WCF，请遵循上述建议以及下面的建议。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-104">To ensure an easier future migration of new ASP.NET applications to WCF, follow the preceding recommendations as well as the following recommendations.</span></span>  
  
## <a name="protocols"></a><span data-ttu-id="f4ef0-105">协议</span><span class="sxs-lookup"><span data-stu-id="f4ef0-105">Protocols</span></span>  

 <span data-ttu-id="f4ef0-106">禁用 ASP.NET 2.0 对 SOAP 1.2 的支持：</span><span class="sxs-lookup"><span data-stu-id="f4ef0-106">Disable ASP.NET 2.0’s support for SOAP 1.2:</span></span>  
  
```xml  
<configuration>  
     <system.web>  
      <webServices >  
          <protocols>  
           <remove name="HttpSoap12"/>  
          </protocols>
      </webServices>  
     </system.web>
</configuration>  
```  
  
 <span data-ttu-id="f4ef0-107">这样做是可行的，因为 WCF 需要与不同的协议（如 SOAP 1.1 和 SOAP 1.2）一致的消息才能使用不同的终结点。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-107">Doing so is advisable because WCF requires messages conforming to different protocols, like SOAP 1.1 and SOAP 1.2, to go by using different endpoints.</span></span> <span data-ttu-id="f4ef0-108">如果将 ASP.NET 2.0 Web 服务配置为支持 SOAP 1.1 和 SOAP 1.2 （这是默认配置），则不能将它转发到原始地址处的单个 WCF 终结点，该终结点肯定与所有 ASP.NET Web 服务的现有客户端兼容。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-108">If an ASP.NET 2.0 Web service is configured to support both SOAP 1.1 and SOAP 1.2, which is the default configuration, then it cannot be migrated forward to a single WCF endpoint at the original address that would be certainly be compatible with all of the ASP.NET Web service’s existing clients.</span></span> <span data-ttu-id="f4ef0-109">另外，选择 SOAP 1.2 而非 SOAP 1.1 将更加严格地限制服务的客户。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-109">Also choosing SOAP 1.2 instead of 1.1 will more severely restrict the clientele of the service.</span></span>  
  
## <a name="service-development"></a><span data-ttu-id="f4ef0-110">服务开发</span><span class="sxs-lookup"><span data-stu-id="f4ef0-110">Service Development</span></span>  

 <span data-ttu-id="f4ef0-111">WCF 允许您通过将应用 <xref:System.ServiceModel.ServiceContractAttribute> 到接口或类来定义服务协定。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-111">WCF allows you to define service contracts by applying the <xref:System.ServiceModel.ServiceContractAttribute> either to interfaces or to classes.</span></span> <span data-ttu-id="f4ef0-112">建议将此属性应用于接口而不是类，因为这样可以为可由任意数量的类以不同方式实现的协定创建一个定义。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-112">It is recommended to apply the attribute to an interface rather than to a class, because doing so creates a definition of a contract that can be variously implemented by any number of classes.</span></span> <span data-ttu-id="f4ef0-113">ASP.NET 2.0 支持将 <xref:System.Web.Services.WebService> 属性应用到接口和类的选项。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-113">ASP.NET 2.0 supports the option of applying the <xref:System.Web.Services.WebService> attribute to interfaces as well as classes.</span></span> <span data-ttu-id="f4ef0-114">但是，如前所述，ASP.NET 2.0 中存在缺陷，如果将 <xref:System.Web.Services.WebService> 属性应用到接口而不是类，则此属性的 Namespace 参数将不起任何作用。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-114">However, as mentioned already, there is a defect in ASP.NET 2.0, by which the Namespace parameter of the <xref:System.Web.Services.WebService> attribute has no effect when that attribute is applied to an interface rather than a class.</span></span> <span data-ttu-id="f4ef0-115">由于通常建议使用特性的 Namespace 参数从默认值修改服务的命名空间，因此，可以 `http://tempuri.org` <xref:System.Web.Services.WebService> 通过 <xref:System.ServiceModel.ServiceContractAttribute> 将特性应用到接口或类来继续定义 ASP.NET Web 服务。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-115">Since it is generally advisable to modify the namespace of a service from the default value, `http://tempuri.org`, using the Namespace parameter of the <xref:System.Web.Services.WebService> attribute, one should continue defining ASP.NET Web Services by applying the <xref:System.ServiceModel.ServiceContractAttribute> attribute either to interfaces or to classes.</span></span>  
  
- <span data-ttu-id="f4ef0-116">在定义那些接口的方法中尽量少使用代码。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-116">Have as little code as possible in the methods by which those interfaces are defined.</span></span> <span data-ttu-id="f4ef0-117">允许它们将其工作委托给其他类。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-117">Have them delegate their work to other classes.</span></span> <span data-ttu-id="f4ef0-118">新的 WCF 服务类型还可将其实体工作委托给这些类。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-118">New WCF service types could then also delegate their substantive work to those classes.</span></span>  
  
- <span data-ttu-id="f4ef0-119">使用 `MessageName` 的 <xref:System.Web.Services.WebMethodAttribute> 参数为服务的操作提供显式名称。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-119">Provide explicit names for the operations of a service using the `MessageName` parameter of the <xref:System.Web.Services.WebMethodAttribute>.</span></span>  
  
    ```csharp  
    [WebMethod(MessageName="ExplicitName")]  
    string Echo(string input);  
    ```  
  
     <span data-ttu-id="f4ef0-120">这样做很重要，因为 ASP.NET 中的操作的默认名称不同于 WCF 提供的默认名称。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-120">Doing so is important, because the default names for operations in ASP.NET are different from the default names supplied by WCF.</span></span> <span data-ttu-id="f4ef0-121">通过提供显式名称，可以避免依赖默认名称。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-121">By providing explicit names, you avoid relying on the default ones.</span></span>  
  
- <span data-ttu-id="f4ef0-122">不要通过多态方法实现 ASP.NET Web 服务操作，因为 WCF 不支持通过多态方法实现操作。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-122">Do not implement ASP.NET Web service operations with polymorphic methods, because WCF does not support implementing operations with polymorphic methods.</span></span>  
  
- <span data-ttu-id="f4ef0-123">使用 <xref:System.Web.Services.Protocols.SoapDocumentMethodAttribute> 为 SOAPAction HTTP 标头提供显式值，HTTP 请求将通过此标头路由到方法。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-123">Use the <xref:System.Web.Services.Protocols.SoapDocumentMethodAttribute> to provide explicit values for the SOAPAction HTTP headers by which HTTP requests will be routed to methods.</span></span>  
  
    ```csharp  
    [WebMethod]  
    [SoapDocumentMethod(RequestElementName="ExplicitAction")]  
    string Echo(string input);  
    ```  
  
     <span data-ttu-id="f4ef0-124">采用此方法将绕过 ASP.NET 和 WCF 使用的默认 SOAPAction 值。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-124">Taking this approach will circumvent having to rely on the default SOAPAction values used by ASP.NET and WCF being the same.</span></span>  
  
- <span data-ttu-id="f4ef0-125">避免使用 SOAP 扩展。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-125">Avoid using SOAP extensions.</span></span> <span data-ttu-id="f4ef0-126">如果 SOAP 扩展是必需的，则确定是否要将其视为已由 WCF 提供的功能。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-126">If SOAP extensions are required, then determine whether the purpose for which they are being considered is a feature that is already provided by WCF.</span></span> <span data-ttu-id="f4ef0-127">如果确实如此，请重新考虑选择不立即采用 WCF。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-127">If that is indeed the case, then reconsider the choice to not adopt WCF right away.</span></span>  
  
## <a name="state-management"></a><span data-ttu-id="f4ef0-128">状态管理</span><span class="sxs-lookup"><span data-stu-id="f4ef0-128">State Management</span></span>  

 <span data-ttu-id="f4ef0-129">避免必须在服务中保持状态。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-129">Avoid having to maintain state in services.</span></span> <span data-ttu-id="f4ef0-130">维护状态不仅会损害应用程序的可伸缩性，而且 ASP.NET 和 WCF 的状态管理机制也有很大不同，尽管 WCF 在 ASP.NET 兼容模式下支持 ASP.NET 机制。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-130">Not only does maintaining state tend to compromise the scalability of an application, but the state management mechanisms of ASP.NET and WCF are very different, although WCF does support the ASP.NET mechanisms in ASP.NET compatibility mode.</span></span>  
  
## <a name="exception-handling"></a><span data-ttu-id="f4ef0-131">异常处理</span><span class="sxs-lookup"><span data-stu-id="f4ef0-131">Exception Handling</span></span>  

 <span data-ttu-id="f4ef0-132">在设计服务发送和接收的数据类型的结构时，请同时设计表示异常的不同类型的结构，这些异常可能发生在人们希望传送到客户端的服务中。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-132">In designing the structures of the data types to be sent and received by a service, also design structures to represent the various types of exceptions that might occur within a service that one might wish to convey to a client.</span></span>  
  
```csharp  
[Serializable]  
[XmlRoot(Namespace="ExplicitNamespace", IsNullable=true)]  
public partial class AnticipatedException
{
    private string anticipatedExceptionInformationField;  

    public string AnticipatedExceptionInformation
    {  
        get {
            return this.anticipatedExceptionInformationField;  
        }  
        set {  
            this.anticipatedExceptionInformationField = value;  
        }  
    }  
}  
```  
  
 <span data-ttu-id="f4ef0-133">使这些类能够将其自身序列化为 XML：</span><span class="sxs-lookup"><span data-stu-id="f4ef0-133">Give such classes the ability to serialize themselves to XML:</span></span>  
  
```csharp  
public XmlNode ToXML()  
{  
     XmlSerializer serializer = new XmlSerializer(  
      typeof(AnticipatedException));  
     MemoryStream memoryStream = new MemoryStream();  
     XmlTextWriter writer = new XmlTextWriter(  
     memoryStream, UnicodeEncoding.UTF8);  
     serializer.Serialize(writer, this);  
     XmlDocument document = new XmlDocument();  
     document.LoadXml(new string(  
     UnicodeEncoding.UTF8.GetChars(  
     memoryStream.GetBuffer())).Trim());  
    return document.DocumentElement;  
}  
```  
  
 <span data-ttu-id="f4ef0-134">然后，可使用这些类为显式引发的 <xref:System.Web.Services.Protocols.SoapException> 实例提供详细信息：</span><span class="sxs-lookup"><span data-stu-id="f4ef0-134">The classes can then be used to provide the details for explicitly thrown <xref:System.Web.Services.Protocols.SoapException> instances:</span></span>  
  
```csharp  
AnticipatedException exception = new AnticipatedException();  
exception.AnticipatedExceptionInformation = "…";  
throw new SoapException(  
     "Fault occurred",  
     SoapException.ClientFaultCode,  
     Context.Request.Url.AbsoluteUri,  
     exception.ToXML());  
```  
  
 <span data-ttu-id="f4ef0-135">这些异常类将随时与 WCF 类结合使用 <xref:System.ServiceModel.FaultException%601> ，以引发新的 `FaultException<AnticipatedException>(anticipatedException);`</span><span class="sxs-lookup"><span data-stu-id="f4ef0-135">These exception classes will be readily reusable with the WCF <xref:System.ServiceModel.FaultException%601> class to throw a new `FaultException<AnticipatedException>(anticipatedException);`</span></span>  
  
## <a name="security"></a><span data-ttu-id="f4ef0-136">安全</span><span class="sxs-lookup"><span data-stu-id="f4ef0-136">Security</span></span>  

 <span data-ttu-id="f4ef0-137">下面是一些安全建议。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-137">The following are some security recommendations.</span></span>  
  
- <span data-ttu-id="f4ef0-138">避免使用 ASP.NET 2.0 配置文件，因为如果将服务迁移到 WCF，则使用这些配置文件会限制 ASP.NET 集成模式的使用。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-138">Avoid using ASP.NET 2.0 Profiles, as using them would restrict the use of ASP.NET Integration Mode if the service was migrated to WCF.</span></span>  
  
- <span data-ttu-id="f4ef0-139">避免使用 Acl 来控制对服务的访问，因为 ASP.NET Web 服务使用 Internet Information Services (IIS) 支持 Acl，因此 WCF 不支持，因为 ASP.NET Web 服务依赖于 IIS 进行承载，而 WCF 不一定必须承载在 IIS 中。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-139">Avoid using ACLs to control access to services, as ASP.NET Web services supports ACLs using Internet Information Services (IIS), WCF does not—because ASP.NET Web services depend on IIS for hosting, and WCF does not necessarily have to be hosted in IIS.</span></span>  
  
- <span data-ttu-id="f4ef0-140">请务必考虑使用 ASP.NET 2.0 角色提供程序来授权对服务资源的访问。</span><span class="sxs-lookup"><span data-stu-id="f4ef0-140">Do consider using ASP.NET 2.0 Role Providers for authorizing access to the resources of a service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4ef0-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="f4ef0-141">See also</span></span>

- [<span data-ttu-id="f4ef0-142">Windows Communication Foundation 使用展望：轻松实现未来的集成</span><span class="sxs-lookup"><span data-stu-id="f4ef0-142">Anticipating Adopting the Windows Communication Foundation: Easing Future Integration</span></span>](anticipating-adopting-the-wcf-easing-future-integration.md)
