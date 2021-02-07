---
description: '了解详细信息：拦截 (WCF Data Services) '
title: 拦截器（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing
- query interceptors [WCF Data Services]
ms.assetid: e33ae8dc-8069-41d0-99a0-75ff28db7050
ms.openlocfilehash: f73ee498d0419df9e083248802ea52ed050a914b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765069"
---
# <a name="interceptors-wcf-data-services"></a><span data-ttu-id="30977-103">拦截器（WCF 数据服务）</span><span class="sxs-lookup"><span data-stu-id="30977-103">Interceptors (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="30977-104">WCF Data Services 使应用程序能够截获请求消息，以便可以向操作添加自定义逻辑。</span><span class="sxs-lookup"><span data-stu-id="30977-104">WCF Data Services enables an application to intercept request messages so that you can add custom logic to an operation.</span></span> <span data-ttu-id="30977-105">使用此自定义逻辑可以验证传入消息中的数据，</span><span class="sxs-lookup"><span data-stu-id="30977-105">You can use this custom logic to validate data in incoming messages.</span></span> <span data-ttu-id="30977-106">还可以使用它进一步限制查询请求的范围，以便基于每个请求插入自定义授权策略。</span><span class="sxs-lookup"><span data-stu-id="30977-106">You can also use it to further restrict the scope of a query request, such as to insert a custom authorization policy on a per request basis.</span></span>  
  
 <span data-ttu-id="30977-107">侦听由数据服务中具有特殊特性的方法执行。</span><span class="sxs-lookup"><span data-stu-id="30977-107">Interception is performed by specially attributed methods in the data service.</span></span> <span data-ttu-id="30977-108">WCF Data Services 在消息处理中的相应点调用这些方法。</span><span class="sxs-lookup"><span data-stu-id="30977-108">These methods are called by WCF Data Services at the appropriate point in message processing.</span></span> <span data-ttu-id="30977-109">侦听器基于每个实体集进行定义，侦听器方法无法像服务操作那样接受请求中的参数。</span><span class="sxs-lookup"><span data-stu-id="30977-109">Interceptors are defined on a per-entity set basis, and interceptor methods cannot accept parameters from the request like service operations can.</span></span> <span data-ttu-id="30977-110">在处理 HTTP GET 请求时调用的查询侦听器方法必须返回一个 lambda 表达式，该表达式确定查询结果是否应当返回侦听器实体集的实例。</span><span class="sxs-lookup"><span data-stu-id="30977-110">Query interceptor methods, which are called when processing an HTTP GET request, must return a lambda expression that determines whether an instance of the interceptor's entity set should be returned by the query results.</span></span> <span data-ttu-id="30977-111">数据服务使用此表达式来进一步优化请求的操作。</span><span class="sxs-lookup"><span data-stu-id="30977-111">This expression is used by the data service to further refine the requested operation.</span></span> <span data-ttu-id="30977-112">下面是查询侦听器的定义示例。</span><span class="sxs-lookup"><span data-stu-id="30977-112">The following is an example definition of a query interceptor.</span></span>  
  
 [!code-csharp[Astoria Northwind Service#QueryInterceptorDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#queryinterceptordef)]
 [!code-vb[Astoria Northwind Service#QueryInterceptorDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#queryinterceptordef)]  
  
 <span data-ttu-id="30977-113">有关详细信息，请参阅 [如何：截获数据服务消息](how-to-intercept-data-service-messages-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="30977-113">For more information, see [How to: Intercept Data Service Messages](how-to-intercept-data-service-messages-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="30977-114">在处理非查询操作时调用的变更侦听器必须返回 `void`（在 Visual Basic 中为 `Nothing`）。</span><span class="sxs-lookup"><span data-stu-id="30977-114">Change interceptors, which are called when processing non-query operations, must return `void` (`Nothing` in Visual Basic).</span></span> <span data-ttu-id="30977-115">变更侦听器方法必须接受以下两个参数：</span><span class="sxs-lookup"><span data-stu-id="30977-115">Change interceptor methods must accept the following two parameters:</span></span>  
  
1. <span data-ttu-id="30977-116">一个与实体集的实体类型相兼容的类型的参数。</span><span class="sxs-lookup"><span data-stu-id="30977-116">A parameter of a type that is compatible with the entity type of the entity set.</span></span> <span data-ttu-id="30977-117">数据服务调用变更侦听器时，此参数的值将反映请求发送的实体信息。</span><span class="sxs-lookup"><span data-stu-id="30977-117">When the data service invokes the change interceptor, the value of this parameter will reflect the entity information that is sent by the request.</span></span>  
  
2. <span data-ttu-id="30977-118">一个 <xref:System.Data.Services.UpdateOperations> 类型的参数。</span><span class="sxs-lookup"><span data-stu-id="30977-118">A parameter of type <xref:System.Data.Services.UpdateOperations>.</span></span> <span data-ttu-id="30977-119">数据服务调用变更侦听器时，此参数的值将反映请求试图执行的操作。</span><span class="sxs-lookup"><span data-stu-id="30977-119">When the data service invokes the change interceptor, the value of this parameter will reflect the operation that the request is trying to perform.</span></span>  
  
 <span data-ttu-id="30977-120">下面是变更侦听器的定义示例。</span><span class="sxs-lookup"><span data-stu-id="30977-120">The following is an example definition of a change interceptor.</span></span>  
  
 [!code-csharp[Astoria Northwind Service#ChangeInterceptorDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#changeinterceptordef)]
 [!code-vb[Astoria Northwind Service#ChangeInterceptorDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#changeinterceptordef)]  
  
 <span data-ttu-id="30977-121">有关详细信息，请参阅 [如何：截获数据服务消息](how-to-intercept-data-service-messages-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="30977-121">For more information, see [How to: Intercept Data Service Messages](how-to-intercept-data-service-messages-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="30977-122">支持使用以下特性进行侦听。</span><span class="sxs-lookup"><span data-stu-id="30977-122">The following attributes are supported for interception.</span></span>  
  
 <span data-ttu-id="30977-123">**[QueryInterceptor (** *EntitySetName* **) ]**</span><span class="sxs-lookup"><span data-stu-id="30977-123">**[QueryInterceptor(** *EntitySetName* **)]**</span></span>  
 <span data-ttu-id="30977-124">当收到了针对目标实体集资源的 HTTP GET 请求时，将调用应用了 <xref:System.Data.Services.QueryInterceptorAttribute> 特性的方法。</span><span class="sxs-lookup"><span data-stu-id="30977-124">Methods with the <xref:System.Data.Services.QueryInterceptorAttribute> attribute applied are called when an HTTP GET request is received for the targeted entity set resource.</span></span> <span data-ttu-id="30977-125">这些方法必须始终返回一个 `Expression<Func<T,bool>>` 形式的 lambda 表达式。</span><span class="sxs-lookup"><span data-stu-id="30977-125">These methods must always return a lambda expression in the form of `Expression<Func<T,bool>>`.</span></span>  
  
 <span data-ttu-id="30977-126">**[ChangeInterceptor (** *EntitySetName* **) ]**</span><span class="sxs-lookup"><span data-stu-id="30977-126">**[ChangeInterceptor(** *EntitySetName* **)]**</span></span>  
 <span data-ttu-id="30977-127">当收到了针对目标实体集资源的 HTTP GET 请求以外的 HTTP 请求时，将调用应用了 <xref:System.Data.Services.ChangeInterceptorAttribute> 特性的方法。</span><span class="sxs-lookup"><span data-stu-id="30977-127">Methods with the <xref:System.Data.Services.ChangeInterceptorAttribute> attribute applied are called when an HTTP request other than HTTP GET request is received for the targeted entity set resource.</span></span> <span data-ttu-id="30977-128">这些方法必须始终返回 `void`（在 Visual Basic 中为 `Nothing`）。</span><span class="sxs-lookup"><span data-stu-id="30977-128">These methods must always return `void` (`Nothing` in Visual Basic).</span></span>  
  
 <span data-ttu-id="30977-129">有关详细信息，请参阅 [如何：截获数据服务消息](how-to-intercept-data-service-messages-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="30977-129">For more information, see [How to: Intercept Data Service Messages](how-to-intercept-data-service-messages-wcf-data-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30977-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="30977-130">See also</span></span>

- [<span data-ttu-id="30977-131">服务操作</span><span class="sxs-lookup"><span data-stu-id="30977-131">Service Operations</span></span>](service-operations-wcf-data-services.md)
