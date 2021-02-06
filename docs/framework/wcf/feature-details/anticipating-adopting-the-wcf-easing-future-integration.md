---
description: 了解更多相关信息：预测采用 Windows Communication Foundation：简化未来的集成
title: Windows Communication Foundation 使用展望：轻松实现未来的集成
ms.date: 03/30/2017
ms.assetid: 3028bba8-6355-4ee0-9ecd-c56e614cb474
ms.openlocfilehash: 512e35e8a4cd6057c96e96a1474f393c3f006525
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643873"
---
# <a name="anticipating-adopting-the-windows-communication-foundation-easing-future-integration"></a><span data-ttu-id="e08c1-103">Windows Communication Foundation 使用展望：轻松实现未来的集成</span><span class="sxs-lookup"><span data-stu-id="e08c1-103">Anticipating Adopting the Windows Communication Foundation: Easing Future Integration</span></span>

<span data-ttu-id="e08c1-104">如果您今天使用 ASP.NET，并预计将来使用 WCF，则本主题将指导您确保新的 ASP.NET Web 服务与 WCF 应用程序一起正常工作。</span><span class="sxs-lookup"><span data-stu-id="e08c1-104">If you use ASP.NET today, and anticipate using WCF in the future, this topic provides guidance to ensure that new ASP.NET Web services will work well together with WCF applications.</span></span>  
  
## <a name="general-recommendations"></a><span data-ttu-id="e08c1-105">一般性建议</span><span class="sxs-lookup"><span data-stu-id="e08c1-105">General Recommendations</span></span>  

 <span data-ttu-id="e08c1-106">对任何新服务采用 ASP.NET 2.0。</span><span class="sxs-lookup"><span data-stu-id="e08c1-106">Adopt ASP.NET 2.0 for any new services.</span></span> <span data-ttu-id="e08c1-107">这样做将允许新服务访问新版本中的改进和增强。</span><span class="sxs-lookup"><span data-stu-id="e08c1-107">Doing so will provide access to the improvements and enhancements of the new version.</span></span> <span data-ttu-id="e08c1-108">不过，它还允许将 ASP.NET 2.0 组件与同一应用程序中的 WCF 组件一起使用。</span><span class="sxs-lookup"><span data-stu-id="e08c1-108">However, it will also allow for the possibility of using ASP.NET 2.0 components together with WCF components in the same application.</span></span>  
  
## <a name="protocols"></a><span data-ttu-id="e08c1-109">协议</span><span class="sxs-lookup"><span data-stu-id="e08c1-109">Protocols</span></span>  

 <span data-ttu-id="e08c1-110">使用 ASP.NET 2.0 的新工具验证与 WS-I 基本配置文件 1.1 的一致性：</span><span class="sxs-lookup"><span data-stu-id="e08c1-110">Use ASP.NET 2.0’s new facility for validating conformity to the WS-I Basic Profile 1.1:</span></span>  
  
```csharp  
[WebService(Namespace = "http://tempuri.org/")]  
[WebServiceBinding(  
     ConformsTo = WsiProfiles.BasicProfile1_1,  
     EmitConformanceClaims=true)]  
public interface IEcho  
```  
  
 <span data-ttu-id="e08c1-111">符合 WS-I Basic Profile 1.1 的 ASP.NET Web 服务将通过使用 WCF 预定义绑定，与 WCF 客户端进行互操作 <xref:System.ServiceModel.BasicHttpBinding> 。</span><span class="sxs-lookup"><span data-stu-id="e08c1-111">ASP.NET Web services that conform to WS-I Basic Profile 1.1 will be interoperable with WCF clients by using WCF predefined binding, <xref:System.ServiceModel.BasicHttpBinding>.</span></span>  
  
## <a name="service-development"></a><span data-ttu-id="e08c1-112">服务开发</span><span class="sxs-lookup"><span data-stu-id="e08c1-112">Service Development</span></span>  

 <span data-ttu-id="e08c1-113">避免使用 <xref:System.Web.Services.Protocols.SoapDocumentServiceAttribute> 特性依据 SOAP 消息正文元素的完全限定名称将消息路由到方法，而应使用 SOAPAction HTTP 标头。</span><span class="sxs-lookup"><span data-stu-id="e08c1-113">Avoid using the <xref:System.Web.Services.Protocols.SoapDocumentServiceAttribute> attribute to have messages routed to methods based on the fully-qualified name of the body element of the SOAP message rather than the SOAPAction HTTP header.</span></span> <span data-ttu-id="e08c1-114">WCF 使用 SOAPAction HTTP 标头来路由消息。</span><span class="sxs-lookup"><span data-stu-id="e08c1-114">WCF uses the SOAPAction HTTP header for routing messages.</span></span>  
  
## <a name="data-representation"></a><span data-ttu-id="e08c1-115">数据表示形式</span><span class="sxs-lookup"><span data-stu-id="e08c1-115">Data Representation</span></span>  

 <span data-ttu-id="e08c1-116">只要为 XML 显式定义了命名空间，则在默认情况下，<xref:System.Xml.Serialization.XmlSerializer> 将类型序列化为的 XML 与 <xref:System.Runtime.Serialization.DataContractSerializer> 将类型序列化为的 XML 在语义上完全相同。</span><span class="sxs-lookup"><span data-stu-id="e08c1-116">The XML into which <xref:System.Xml.Serialization.XmlSerializer> serializes a type by default is semantically identical to the XML into which the <xref:System.Runtime.Serialization.DataContractSerializer> serializes a type, provided the namespace for the XML is explicitly defined.</span></span> <span data-ttu-id="e08c1-117">定义用于 ASP.NET Web 服务的数据类型时，若要在将来采用 WCF，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="e08c1-117">When defining a data type for use with ASP.NET Web services in anticipation of adopting WCF in the future, do the following:</span></span>  
  
1. <span data-ttu-id="e08c1-118">使用 .NET Framework 类而不是 XML 架构来定义该类型。</span><span class="sxs-lookup"><span data-stu-id="e08c1-118">Define the type using .NET Framework classes rather than XML Schema.</span></span>  
  
2. <span data-ttu-id="e08c1-119">仅将 <xref:System.SerializableAttribute> 和 <xref:System.Xml.Serialization.XmlRootAttribute> 添加到该类，使用后者显式定义类型的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e08c1-119">Add only the <xref:System.SerializableAttribute> and the <xref:System.Xml.Serialization.XmlRootAttribute> to the class, using the latter to explicitly define the namespace for the type.</span></span> <span data-ttu-id="e08c1-120">不要添加 <xref:System.Xml.Serialization> 命名空间中的其他属性来控制如何将 .NET Framework 类转换为 XML。</span><span class="sxs-lookup"><span data-stu-id="e08c1-120">Do no add additional attributes from the <xref:System.Xml.Serialization> namespace to control how the .NET Framework class is to be translated into XML.</span></span>  
  
 <span data-ttu-id="e08c1-121">通过采用此方法，以后可将 .NET 类转换为附加了 <xref:System.Runtime.Serialization.DataContractAttribute> 和 <xref:System.Runtime.Serialization.DataMemberAttribute> 的数据协定，而无需为了传输而对类序列化成的 XML 进行重大更改。</span><span class="sxs-lookup"><span data-stu-id="e08c1-121">By adopting this approach, you should be able to later make the .NET classes into data contracts with the addition of the <xref:System.Runtime.Serialization.DataContractAttribute> and <xref:System.Runtime.Serialization.DataMemberAttribute> without significantly altering the XML into which the classes are serialized for transmission.</span></span> <span data-ttu-id="e08c1-122">ASP.NET Web 服务在消息中使用的类型将能够由 WCF 应用程序作为数据协定进行处理，从而实现了其他好处，从而提高了 WCF 应用程序的性能。</span><span class="sxs-lookup"><span data-stu-id="e08c1-122">The types used in messages by ASP.NET Web services will be able to be processed as data contracts by WCF applications, yielding, amongst other benefits, better performance in WCF applications.</span></span>  
  
## <a name="security"></a><span data-ttu-id="e08c1-123">安全</span><span class="sxs-lookup"><span data-stu-id="e08c1-123">Security</span></span>  

 <span data-ttu-id="e08c1-124">避免使用 Internet Information Services (IIS) 提供的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="e08c1-124">Avoid using the authentication options provided by Internet Information Services (IIS).</span></span> <span data-ttu-id="e08c1-125">WCF 客户端不支持它们。</span><span class="sxs-lookup"><span data-stu-id="e08c1-125">WCF clients do not support them.</span></span> <span data-ttu-id="e08c1-126">如果某个服务需要安全，请使用 WCF 提供的选项，因为这些选项更丰富并且基于标准协议。</span><span class="sxs-lookup"><span data-stu-id="e08c1-126">If a service needs to be secured, use the options provided by WCF, because these options are richer and are based on standard protocols.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e08c1-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="e08c1-127">See also</span></span>

- [<span data-ttu-id="e08c1-128">Windows Communication Foundation 使用展望：轻松实现未来的迁移</span><span class="sxs-lookup"><span data-stu-id="e08c1-128">Anticipating Adopting the Windows Communication Foundation: Easing Future Migration</span></span>](anticipating-adopting-wcf-migration.md)
