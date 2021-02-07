---
description: '了解有关详细信息，请参阅如何：定义服务操作 (WCF Data Services) '
title: 如何：定义服务操作（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Service Operations [WCF Data Services]
- WCF Data Services, service operations
ms.assetid: dfcd3cb1-2f07-4d0b-b16a-6b056c4f45fa
ms.openlocfilehash: 9fcad3a31ea5b439c248ba103cbf4ddd75b8109a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765615"
---
# <a name="how-to-define-a-service-operation-wcf-data-services"></a><span data-ttu-id="ed752-103">如何：定义服务操作（WCF 数据服务）</span><span class="sxs-lookup"><span data-stu-id="ed752-103">How to: Define a Service Operation (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="ed752-104">WCF Data Services 公开在服务器上作为服务操作定义的方法。</span><span class="sxs-lookup"><span data-stu-id="ed752-104">WCF Data Services expose methods that are defined on the server as service operations.</span></span> <span data-ttu-id="ed752-105">服务操作允许数据服务通过 URI 提供对服务器上定义的方法的访问。</span><span class="sxs-lookup"><span data-stu-id="ed752-105">Service operations allow a data service to provide access through a URI to a method that is defined on the server.</span></span> <span data-ttu-id="ed752-106">若要定义服务操作，请将 [ `WebGet]` 或 `[WebInvoke]` 特性应用于方法。</span><span class="sxs-lookup"><span data-stu-id="ed752-106">To define a service operation, apply the [`WebGet]` or `[WebInvoke]` attribute to the method.</span></span> <span data-ttu-id="ed752-107">若要支持查询运算符，服务操作必须返回 <xref:System.Linq.IQueryable%601> 实例。</span><span class="sxs-lookup"><span data-stu-id="ed752-107">To support query operators, the service operation must return an <xref:System.Linq.IQueryable%601> instance.</span></span> <span data-ttu-id="ed752-108">服务操作可以通过 <xref:System.Data.Services.DataService%601.CurrentDataSource%2A> 的 <xref:System.Data.Services.DataService%601> 属性访问基础数据源。</span><span class="sxs-lookup"><span data-stu-id="ed752-108">Service operations may access the underlying data source through the <xref:System.Data.Services.DataService%601.CurrentDataSource%2A> property on the <xref:System.Data.Services.DataService%601>.</span></span> <span data-ttu-id="ed752-109">有关详细信息，请参阅 [服务操作](service-operations-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="ed752-109">For more information, see [Service Operations](service-operations-wcf-data-services.md).</span></span>

<span data-ttu-id="ed752-110">本主题中的示例定义一个名为 `GetOrdersByCity` 的服务操作，该操作返回 <xref:System.Linq.IQueryable%601> 和相关 `Orders` 对象的经筛选后的 `Order_Details` 实例。</span><span class="sxs-lookup"><span data-stu-id="ed752-110">The example in this topic defines a service operation named `GetOrdersByCity` that returns a filtered <xref:System.Linq.IQueryable%601> instance of `Orders` and related `Order_Details` objects.</span></span> <span data-ttu-id="ed752-111">该示例访问作为 Northwind 示例数据服务数据源的 <xref:System.Data.Objects.ObjectContext> 实例。</span><span class="sxs-lookup"><span data-stu-id="ed752-111">The example accesses the <xref:System.Data.Objects.ObjectContext> instance that is the data source for the Northwind sample data service.</span></span> <span data-ttu-id="ed752-112">此服务是在完成 [WCF Data Services 快速入门](quickstart-wcf-data-services.md)时创建的。</span><span class="sxs-lookup"><span data-stu-id="ed752-112">This service is created when you complete the [WCF Data Services quickstart](quickstart-wcf-data-services.md).</span></span>

### <a name="to-define-a-service-operation-in-the-northwind-data-service"></a><span data-ttu-id="ed752-113">在 Northwind 数据服务中定义服务操作</span><span class="sxs-lookup"><span data-stu-id="ed752-113">To define a service operation in the Northwind data service</span></span>

1. <span data-ttu-id="ed752-114">在 Northwind 数据服务项目中，打开 Northwind.svc 文件。</span><span class="sxs-lookup"><span data-stu-id="ed752-114">In the Northwind data service project, open the Northwind.svc file.</span></span>

2. <span data-ttu-id="ed752-115">在 `Northwind` 类中，定义一个名为 `GetOrdersByCity` 的服务操作方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ed752-115">In the `Northwind` class, define a service operation method named `GetOrdersByCity` as follows:</span></span>

     [!code-csharp[Astoria Northwind Service#ServiceOperationDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#serviceoperationdef)]
     [!code-vb[Astoria Northwind Service#ServiceOperationDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#serviceoperationdef)]

3. <span data-ttu-id="ed752-116">在 `InitializeService` 类的 `Northwind` 方法中，添加以下代码以支持对服务操作的访问：</span><span class="sxs-lookup"><span data-stu-id="ed752-116">In the `InitializeService` method of the `Northwind` class, add the following code to enable access to the service operation:</span></span>

     [!code-csharp[Astoria Northwind Service#ServiceOperationConfig](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#serviceoperationconfig)]
     [!code-vb[Astoria Northwind Service#ServiceOperationConfig](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#serviceoperationconfig)]

### <a name="to-query-the-getordersbycity-service-operation"></a><span data-ttu-id="ed752-117">查询 GetOrdersByCity 服务操作</span><span class="sxs-lookup"><span data-stu-id="ed752-117">To query the GetOrdersByCity service operation</span></span>

- <span data-ttu-id="ed752-118">在 Web 浏览器中，输入以下 URI 之一以调用在以下示例中定义的服务操作：</span><span class="sxs-lookup"><span data-stu-id="ed752-118">In a Web browser, enter one of the following URIs to invoke the service operation that is defined in the following example:</span></span>

  - `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'`

  - `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$top=2`

  - `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$expand=Order_Details&$orderby=RequiredDate desc`

## <a name="example"></a><span data-ttu-id="ed752-119">示例</span><span class="sxs-lookup"><span data-stu-id="ed752-119">Example</span></span>

<span data-ttu-id="ed752-120">以下示例对 Northwind 数据服务实现一个名为 `GetOrderByCity` 的服务操作。</span><span class="sxs-lookup"><span data-stu-id="ed752-120">The following example implements a service operation named `GetOrderByCity` on the Northwind data service.</span></span> <span data-ttu-id="ed752-121">此操作根据提供的城市名称使用 ADO.NET 实体框架返回一组 `Orders` 和相关 `Order_Details` 对象，以作为 <xref:System.Linq.IQueryable%601> 实例。</span><span class="sxs-lookup"><span data-stu-id="ed752-121">This operation uses the ADO.NET Entity Framework to return a set of `Orders` and related `Order_Details` objects as an <xref:System.Linq.IQueryable%601> instance based on the provided city name.</span></span>

> [!NOTE]
> <span data-ttu-id="ed752-122">由于此方法返回了一个 <xref:System.Linq.IQueryable%601> 实例，因此该服务操作终结点支持查询运算符。</span><span class="sxs-lookup"><span data-stu-id="ed752-122">Query operators are supported on this service operation endpoint because the method returns an <xref:System.Linq.IQueryable%601> instance.</span></span>

[!code-csharp[Astoria Northwind Service#ServiceOperation](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#serviceoperation)]
[!code-vb[Astoria Northwind Service#ServiceOperation](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#serviceoperation)]

## <a name="see-also"></a><span data-ttu-id="ed752-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed752-123">See also</span></span>

- [<span data-ttu-id="ed752-124">定义 WCF 数据服务</span><span class="sxs-lookup"><span data-stu-id="ed752-124">Defining WCF Data Services</span></span>](defining-wcf-data-services.md)
