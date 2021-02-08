---
description: 了解详细信息： WCF Web HTTP 错误处理
title: WCF Web HTTP 错误处理
ms.date: 03/30/2017
ms.assetid: 02891563-0fce-4c32-84dc-d794b1a5c040
ms.openlocfilehash: 88483c249bc1b6b866517ca10b348c0885fc34fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779473"
---
# <a name="wcf-web-http-error-handling"></a><span data-ttu-id="b7f8f-103">WCF Web HTTP 错误处理</span><span class="sxs-lookup"><span data-stu-id="b7f8f-103">WCF Web HTTP Error Handling</span></span>

<span data-ttu-id="b7f8f-104">Windows Communication Foundation (WCF) Web HTTP 错误处理使你能够从 WCF Web HTTP 服务返回错误，该服务指定 HTTP 状态代码，并使用与操作 (的格式相同的格式（例如，XML 或 JSON) ）返回错误详细信息。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-104">Windows Communication Foundation (WCF) Web HTTP error handling enables you to return errors from WCF Web HTTP services that specify an HTTP status code and return error details using the same format as the operation (for example, XML or JSON).</span></span>  
  
## <a name="wcf-web-http-error-handling"></a><span data-ttu-id="b7f8f-105">WCF Web HTTP 错误处理</span><span class="sxs-lookup"><span data-stu-id="b7f8f-105">WCF Web HTTP Error Handling</span></span>  

 <span data-ttu-id="b7f8f-106"><xref:System.ServiceModel.Web.WebFaultException> 类定义可用于指定 HTTP 状态代码的构造函数。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-106">The <xref:System.ServiceModel.Web.WebFaultException> class defines a constructor that allows you to specify an HTTP status code.</span></span> <span data-ttu-id="b7f8f-107">随后会将此状态代码返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-107">This status code is then returned to the client.</span></span> <span data-ttu-id="b7f8f-108"><xref:System.ServiceModel.Web.WebFaultException> 类的泛型版本 <xref:System.ServiceModel.Web.WebFaultException%601> 可用于返回用户定义的类型，该类型中包含有关所出现错误的信息。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-108">A generic version of the <xref:System.ServiceModel.Web.WebFaultException> class, <xref:System.ServiceModel.Web.WebFaultException%601> enables you to return a user-defined type that contains information about the error that occurred.</span></span> <span data-ttu-id="b7f8f-109">将使用由操作指定的格式序列化此自定义对象，并将它返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-109">This custom object is serialized using the format specified by the operation and returned to the client.</span></span> <span data-ttu-id="b7f8f-110">下面的示例演示如何返回 HTTP 状态代码。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-110">The following example shows how to return an HTTP status code.</span></span>  
  
```csharp
public string Operation1()
{
    // Operation logic  
   // ...
   throw new WebFaultException(HttpStatusCode.Forbidden);
}  
```  
  
 <span data-ttu-id="b7f8f-111">下面的示例演示如何在用户定义的类型中返回 HTTP 状态代码和额外信息。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-111">The following example shows how to return an HTTP status code and extra information in a user-defined type.</span></span> <span data-ttu-id="b7f8f-112">`MyErrorDetail` 是用户定义的类型，其中包含有关所出现错误的额外信息。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-112">`MyErrorDetail` is a user-defined type that contains extra information about the error that occurred.</span></span>  
  
```csharp
public string Operation2()
{
   // Operation logic  
   // ...
   MyErrorDetail detail = new MyErrorDetail()
   {  
      Message = "Error Message",  
      ErrorCode = 123,  
   }  
   throw new WebFaultException<MyErrorDetail>(detail, HttpStatusCode.Forbidden);  
}  
```  
  
 <span data-ttu-id="b7f8f-113">上述代码返回 HTTP 响应，其中包括禁止状态代码以及包含 `MyErrorDetails` 对象实例的正文。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-113">The preceding code returns an HTTP response with the forbidden status code and a body that contains an instance of the `MyErrorDetails` object.</span></span> <span data-ttu-id="b7f8f-114">`MyErrorDetails` 对象的格式由以下内容确定：</span><span class="sxs-lookup"><span data-stu-id="b7f8f-114">The format of the `MyErrorDetails` object is determined by:</span></span>  
  
- <span data-ttu-id="b7f8f-115">服务操作指定的 `ResponseFormat` 或 <xref:System.ServiceModel.Web.WebGetAttribute> 特性的 <xref:System.ServiceModel.Web.WebInvokeAttribute> 参数值。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-115">The value of the `ResponseFormat` parameter of the <xref:System.ServiceModel.Web.WebGetAttribute> or <xref:System.ServiceModel.Web.WebInvokeAttribute> attribute specified on the service operation.</span></span>  
  
- <span data-ttu-id="b7f8f-116"><xref:System.ServiceModel.Description.WebHttpBehavior.AutomaticFormatSelectionEnabled%2A> 的值。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-116">The value of <xref:System.ServiceModel.Description.WebHttpBehavior.AutomaticFormatSelectionEnabled%2A>.</span></span>  
  
- <span data-ttu-id="b7f8f-117">通过访问 <xref:System.ServiceModel.Web.OutgoingWebResponseContext.Format%2A> 得到的 <xref:System.ServiceModel.Web.OutgoingWebResponseContext> 属性值。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-117">The value of the <xref:System.ServiceModel.Web.OutgoingWebResponseContext.Format%2A> property by accessing the <xref:System.ServiceModel.Web.OutgoingWebResponseContext>.</span></span>  
  
 <span data-ttu-id="b7f8f-118">有关这些值如何影响操作格式的详细信息，请参阅 [WCF WEB HTTP 格式设置](wcf-web-http-formatting.md)。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-118">For more information about how these values affect the formatting of the operation, see [WCF Web HTTP Formatting](wcf-web-http-formatting.md).</span></span>  
  
 <span data-ttu-id="b7f8f-119"><xref:System.ServiceModel.Web.WebFaultException> 是一个 <xref:System.ServiceModel.FaultException>，因此可用作公开 SOAP 终结点和 Web HTTP 终结点的服务的错误异常编程模型。</span><span class="sxs-lookup"><span data-stu-id="b7f8f-119"><xref:System.ServiceModel.Web.WebFaultException> is a <xref:System.ServiceModel.FaultException> and therefore can be used as the fault exception programming model for services that expose SOAP endpoints as well as web HTTP endpoints.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7f8f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7f8f-120">See also</span></span>

- [<span data-ttu-id="b7f8f-121">WCF Web HTTP 编程模型</span><span class="sxs-lookup"><span data-stu-id="b7f8f-121">WCF Web HTTP Programming Model</span></span>](wcf-web-http-programming-model.md)
- [<span data-ttu-id="b7f8f-122">WCF Web HTTP 格式设置</span><span class="sxs-lookup"><span data-stu-id="b7f8f-122">WCF Web HTTP Formatting</span></span>](wcf-web-http-formatting.md)
- [<span data-ttu-id="b7f8f-123">定义和指定错误</span><span class="sxs-lookup"><span data-stu-id="b7f8f-123">Defining and Specifying Faults</span></span>](../defining-and-specifying-faults.md)
- [<span data-ttu-id="b7f8f-124">处理异常和错误</span><span class="sxs-lookup"><span data-stu-id="b7f8f-124">Handling Exceptions and Faults</span></span>](../extending/handling-exceptions-and-faults.md)
- [<span data-ttu-id="b7f8f-125">发送和接收错误</span><span class="sxs-lookup"><span data-stu-id="b7f8f-125">Sending and Receiving Faults</span></span>](../sending-and-receiving-faults.md)
