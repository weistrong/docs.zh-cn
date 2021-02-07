---
description: 了解详细信息： WCF Web HTTP 编程模型
title: WCF Web HTTP 编程模型
ms.date: 03/30/2017
helpviewer_keywords:
- web services programming model [WCF]
- POX
- REST
ms.assetid: 2312a8d3-b66e-4623-ba42-978434300c7f
ms.openlocfilehash: f439e69e0e0c041f49e7fc5e64637337880e8459
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752582"
---
# <a name="wcf-web-http-programming-model"></a><span data-ttu-id="c3390-103">WCF Web HTTP 编程模型</span><span class="sxs-lookup"><span data-stu-id="c3390-103">WCF Web HTTP Programming Model</span></span>

<span data-ttu-id="c3390-104">Windows Communication Foundation (WCF) Web HTTP 编程模型，开发人员可以向非 SOAP 终结点公开 WCF 服务操作。</span><span class="sxs-lookup"><span data-stu-id="c3390-104">The Windows Communication Foundation (WCF) Web HTTP Programming Model allows developers to expose WCF service operations to non-SOAP endpoints.</span></span> <span data-ttu-id="c3390-105">本节中的主题详细研究此功能。</span><span class="sxs-lookup"><span data-stu-id="c3390-105">The topics in this section examine the feature in detail.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c3390-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="c3390-106">In This Section</span></span>  

 [<span data-ttu-id="c3390-107">WCF Web HTTP 编程模型概述</span><span class="sxs-lookup"><span data-stu-id="c3390-107">WCF Web HTTP Programming Model Overview</span></span>](wcf-web-http-programming-model-overview.md)  
 <span data-ttu-id="c3390-108">提供 Windows Communication Foundation (WCF) Web HTTP 编程模型的概述。</span><span class="sxs-lookup"><span data-stu-id="c3390-108">Provides an overview of the Windows Communication Foundation (WCF) Web HTTP Programming Model.</span></span>  
  
 [<span data-ttu-id="c3390-109">WCF Web HTTP 编程对象模型</span><span class="sxs-lookup"><span data-stu-id="c3390-109">WCF Web HTTP Programming Object Model</span></span>](wcf-web-http-programming-object-model.md)  
 <span data-ttu-id="c3390-110">讨论 Windows Communication Foundation (WCF) Web HTTP 编程模型及其工作原理。</span><span class="sxs-lookup"><span data-stu-id="c3390-110">Discusses the Windows Communication Foundation (WCF) Web HTTP Programming Model and how it works.</span></span>  
  
 [<span data-ttu-id="c3390-111">如何：创建基本 WCF Web HTTP 服务</span><span class="sxs-lookup"><span data-stu-id="c3390-111">How to: Create a Basic WCF Web HTTP Service</span></span>](how-to-create-a-basic-wcf-web-http-service.md)  
 <span data-ttu-id="c3390-112">说明如何编写公开非 SOAP 终结点的基本服务。</span><span class="sxs-lookup"><span data-stu-id="c3390-112">Describes how to write a basic service that exposes a non-SOAP endpoint.</span></span>  
  
 [<span data-ttu-id="c3390-113">如何：向 SOAP 和 Web 客户端公开协定</span><span class="sxs-lookup"><span data-stu-id="c3390-113">How to: Expose a Contract to SOAP and Web Clients</span></span>](how-to-expose-a-contract-to-soap-and-web-clients.md)  
 <span data-ttu-id="c3390-114">说明如何编写向 SOAP 和非 SOAP 客户端公开同一协定的基本服务。</span><span class="sxs-lookup"><span data-stu-id="c3390-114">Describes how to write a basic service that exposes the same contract to both SOAP and non-SOAP clients.</span></span>  
  
 [<span data-ttu-id="c3390-115">UriTemplate 和 UriTemplateTable</span><span class="sxs-lookup"><span data-stu-id="c3390-115">UriTemplate and UriTemplateTable</span></span>](uritemplate-and-uritemplatetable.md)  
 <span data-ttu-id="c3390-116">说明如何使用 <xref:System.UriTemplate> 和 <xref:System.UriTemplateTable> 控制 URI。</span><span class="sxs-lookup"><span data-stu-id="c3390-116">Describes how to control URIs using <xref:System.UriTemplate> and <xref:System.UriTemplateTable>.</span></span>  
  
 [<span data-ttu-id="c3390-117">对 WCF Web HTTP 服务的缓存支持</span><span class="sxs-lookup"><span data-stu-id="c3390-117">Caching Support for WCF Web HTTP Services</span></span>](caching-support-for-wcf-web-http-services.md)  
 <span data-ttu-id="c3390-118">说明如何指定 WCF Web HTTP 服务的缓存行为。</span><span class="sxs-lookup"><span data-stu-id="c3390-118">Describes how to specify caching behavior for a WCF Web HTTP service.</span></span>  
  
 [<span data-ttu-id="c3390-119">WCF Web HTTP 格式设置</span><span class="sxs-lookup"><span data-stu-id="c3390-119">WCF Web HTTP Formatting</span></span>](wcf-web-http-formatting.md)  
 <span data-ttu-id="c3390-120">说明如何指定 WCF Web HTTP 服务响应的格式。</span><span class="sxs-lookup"><span data-stu-id="c3390-120">Describes how to specify the format of the response from a WCF Web HTTP service.</span></span>  
  
 [<span data-ttu-id="c3390-121">WCF Web HTTP 错误处理</span><span class="sxs-lookup"><span data-stu-id="c3390-121">WCF Web HTTP Error Handling</span></span>](wcf-web-http-error-handling.md)  
 <span data-ttu-id="c3390-122">说明如何将错误返回 WCF Web 客户端，包括 HTTP 状态代码和用户定义的其他错误数据。</span><span class="sxs-lookup"><span data-stu-id="c3390-122">Describes how to return errors to WCF Web clients including HTTP status codes and additional user-defined error data.</span></span>  
  
 [<span data-ttu-id="c3390-123">从 WCF 服务调用 REST 样式服务</span><span class="sxs-lookup"><span data-stu-id="c3390-123">Calling a REST-style service from a WCF service</span></span>](calling-a-rest-style-service-from-a-wcf-service.md)  
 <span data-ttu-id="c3390-124">说明如何从 WCF 服务内部来调用 REST 样式服务。</span><span class="sxs-lookup"><span data-stu-id="c3390-124">Describes how to call a REST-style service from inside a WCF service.</span></span>
