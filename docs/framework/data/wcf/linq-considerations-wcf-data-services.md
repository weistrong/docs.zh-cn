---
description: '了解详细信息： (WCF Data Services LINQ 注意事项) '
title: LINQ 注意事项（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, LINQ
- querying the data service [WCF Data Services]
- WCF Data Services, querying
ms.assetid: cc4ec9e9-348f-42a6-a78e-1cd40e370656
ms.openlocfilehash: 4205fc5c67c5939377e2a964d5a82d8855b03fce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764959"
---
# <a name="linq-considerations-wcf-data-services"></a><span data-ttu-id="2b081-103">LINQ 注意事项（WCF 数据服务）</span><span class="sxs-lookup"><span data-stu-id="2b081-103">LINQ Considerations (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="2b081-104">本主题提供有关在使用 WCF Data Services 客户端时如何编写和执行 LINQ 查询的信息，以及使用 LINQ 查询实现 Open Data Protocol (OData) 的数据服务的限制。</span><span class="sxs-lookup"><span data-stu-id="2b081-104">This topic provides information about the way in which LINQ queries are composed and executed when you are using the WCF Data Services client and limitations of using LINQ to query a data service that implements the Open Data Protocol (OData).</span></span> <span data-ttu-id="2b081-105">有关对基于 OData 的数据服务编写和执行查询的详细信息，请参阅 [查询数据服务](querying-the-data-service-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2b081-105">For more information about composing and executing queries against an OData-based data service, see [Querying the Data Service](querying-the-data-service-wcf-data-services.md).</span></span>  
  
## <a name="composing-linq-queries"></a><span data-ttu-id="2b081-106">编写 LINQ 查询</span><span class="sxs-lookup"><span data-stu-id="2b081-106">Composing LINQ Queries</span></span>  

 <span data-ttu-id="2b081-107">LINQ 允许针对实现 <xref:System.Collections.Generic.IEnumerable%601> 的对象集合编写查询。</span><span class="sxs-lookup"><span data-stu-id="2b081-107">LINQ enables you to compose queries against a collection of objects that implements <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="2b081-108">Visual Studio 中的 " **添加服务引用** " 对话框和 "DataSvcUtil.exe" 工具都用于生成 OData 服务的表示形式，作为从继承的实体容器类以及 <xref:System.Data.Services.Client.DataServiceContext> 表示源中返回的实体的对象。</span><span class="sxs-lookup"><span data-stu-id="2b081-108">Both the **Add Service Reference** dialog box in Visual Studio and the DataSvcUtil.exe tool are used to generate a representation of an OData service as an entity container class that inherits from <xref:System.Data.Services.Client.DataServiceContext>, as well as objects that represent the entities returned in feeds.</span></span> <span data-ttu-id="2b081-109">这些工具还可为由服务作为源公开的集合的实体容器类生成属性。</span><span class="sxs-lookup"><span data-stu-id="2b081-109">These tools also generate properties on the entity container class for the collections that are exposed as feeds by the service.</span></span> <span data-ttu-id="2b081-110">封装了数据服务的类的每个属性都会返回一个 <xref:System.Data.Services.Client.DataServiceQuery%601>。</span><span class="sxs-lookup"><span data-stu-id="2b081-110">Each of these properties of the class that encapsulates the data service return a <xref:System.Data.Services.Client.DataServiceQuery%601>.</span></span> <span data-ttu-id="2b081-111">因为 <xref:System.Data.Services.Client.DataServiceQuery%601> 类实现 LINQ 定义的 <xref:System.Linq.IQueryable%601> 接口，所以可以针对数据服务公开的源编写 LINQ 查询，客户端库会将其转换为一个查询请求 URI，在执行时将此 URI 发送给数据服务。</span><span class="sxs-lookup"><span data-stu-id="2b081-111">Because the <xref:System.Data.Services.Client.DataServiceQuery%601> class implements the <xref:System.Linq.IQueryable%601> interface defined by LINQ, you can compose a LINQ query against feeds exposed by the data service, which are translated by the client library into a query request URI that is sent to the data service on execution.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="2b081-112">LINQ 语法中可表达的查询集比 OData 数据服务使用的 URI 语法中启用的查询更广泛。</span><span class="sxs-lookup"><span data-stu-id="2b081-112">The set of queries expressible in the LINQ syntax is broader than those enabled in the URI syntax that is used by OData data services.</span></span> <span data-ttu-id="2b081-113">如果无法将查询映射到目标数据服务中的 URI，则会引发 <xref:System.NotSupportedException>。</span><span class="sxs-lookup"><span data-stu-id="2b081-113">A <xref:System.NotSupportedException> is raised when the query cannot be mapped to a URI in the target data service.</span></span> <span data-ttu-id="2b081-114">有关详细信息，请参阅本主题中的 [不受支持的 LINQ 方法](linq-considerations-wcf-data-services.md#unsupportedMethods) 。</span><span class="sxs-lookup"><span data-stu-id="2b081-114">For more information, see the [Unsupported LINQ Methods](linq-considerations-wcf-data-services.md#unsupportedMethods) in this topic.</span></span>  
  
 <span data-ttu-id="2b081-115">下面的示例是一个 LINQ 查询，它返回运费成本超过 30 美元的 `Orders` 并按装运日期对结果进行排序，最近的装运日期排在最前面：</span><span class="sxs-lookup"><span data-stu-id="2b081-115">The following example is a LINQ query that returns `Orders` that have a freight cost of more than $30 and sorts the results by the shipping date, starting with the latest ship date:</span></span>  
  
[!code-csharp[Astoria Northwind Client#AddQueryOptionsLinqSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#addqueryoptionslinqspecific)]
[!code-vb[Astoria Northwind Client#AddQueryOptionsLinqSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#addqueryoptionslinqspecific)]
  
 <span data-ttu-id="2b081-116">此 LINQ 查询转换为对基于 Northwind 的 [快速入门](quickstart-wcf-data-services.md) 数据服务执行的以下查询 URI：</span><span class="sxs-lookup"><span data-stu-id="2b081-116">This LINQ query is translated into the following query URI that is executed against the Northwind-based [quickstart](quickstart-wcf-data-services.md) data service:</span></span>  
  
```http
http://localhost:12345/Northwind.svc/Orders?Orderby=ShippedDate&?filter=Freight gt 30  
```  
  
 <span data-ttu-id="2b081-117">有关 LINQ 的更多常规信息，请参阅 [语言集成查询 (linq) c #](../../../csharp/programming-guide/concepts/linq/index.md) 或 [语言集成查询 (LINQ) -Visual Basic](../../../visual-basic/programming-guide/concepts/linq/index.md)。</span><span class="sxs-lookup"><span data-stu-id="2b081-117">For more general information about LINQ, see [Language-Integrated Query (LINQ) - C#](../../../csharp/programming-guide/concepts/linq/index.md) or [Language-Integrated Query (LINQ) - Visual Basic](../../../visual-basic/programming-guide/concepts/linq/index.md).</span></span>  
  
 <span data-ttu-id="2b081-118">LINQ 允许使用语言特定声明查询语法（如上例所示）和一组称为标准查询运算符的查询方法编写查询。</span><span class="sxs-lookup"><span data-stu-id="2b081-118">LINQ enables you to compose queries by using both the language-specific declarative query syntax, shown in the previous example, as well as a set of query methods known as standard query operators.</span></span> <span data-ttu-id="2b081-119">通过仅使用基于方法的语法可以编写与上例等效的查询，如下面的示例所示：</span><span class="sxs-lookup"><span data-stu-id="2b081-119">An equivalent query to the previous example can be composed by using only the method-based syntax, as shown the following example:</span></span>  
  
[!code-csharp[Astoria Northwind Client#AddQueryOptionsLinqExpressionSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#addqueryoptionslinqexpressionspecific)]
[!code-vb[Astoria Northwind Client#AddQueryOptionsLinqExpressionSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#addqueryoptionslinqexpressionspecific)]
  
 <span data-ttu-id="2b081-120">WCF Data Services 客户端可以将这两种组合查询转换为查询 URI，并且可以通过将查询方法追加到查询表达式来扩展 LINQ 查询。</span><span class="sxs-lookup"><span data-stu-id="2b081-120">The WCF Data Services client is able to translate both kinds of composed queries into a query URI, and you can extend a LINQ query by appending query methods to a query expression.</span></span> <span data-ttu-id="2b081-121">通过向查询表达式或 <xref:System.Data.Services.Client.DataServiceQuery%601> 追加方法语法来编写 LINQ 查询时，运算将按照方法的调用顺序添加到查询 URI 中。</span><span class="sxs-lookup"><span data-stu-id="2b081-121">When you compose LINQ queries by appending method syntax to a query expression or a <xref:System.Data.Services.Client.DataServiceQuery%601>, the operations are added to the query URI in the order in which methods are called.</span></span> <span data-ttu-id="2b081-122">这等效于调用 <xref:System.Data.Services.Client.DataServiceQuery%601.AddQueryOption%2A> 方法将每个查询选项添加到查询 URI 中。</span><span class="sxs-lookup"><span data-stu-id="2b081-122">This is equivalent to calling the <xref:System.Data.Services.Client.DataServiceQuery%601.AddQueryOption%2A> method to add each query option to the query URI.</span></span>  
  
## <a name="executing-linq-queries"></a><span data-ttu-id="2b081-123">执行 LINQ 查询</span><span class="sxs-lookup"><span data-stu-id="2b081-123">Executing LINQ Queries</span></span>  

 <span data-ttu-id="2b081-124">某些 LINQ 查询方法（如 <xref:System.Linq.Enumerable.First%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%29> 或 <xref:System.Linq.Enumerable.Single%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%29>）在追加到查询中时会导致执行查询。</span><span class="sxs-lookup"><span data-stu-id="2b081-124">Certain LINQ query methods, such as <xref:System.Linq.Enumerable.First%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%29> or <xref:System.Linq.Enumerable.Single%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%29>, when appended to the query, cause the query to be executed.</span></span> <span data-ttu-id="2b081-125">在隐式枚举结果时也会执行查询，例如在 `foreach` 循环过程中或将查询分配给一个 `List` 集合时。</span><span class="sxs-lookup"><span data-stu-id="2b081-125">A query is also executed when results are enumerated implicitly, such as during a `foreach` loop or when the query is assigned to a `List` collection.</span></span> <span data-ttu-id="2b081-126">有关详细信息，请参阅 [查询数据服务](querying-the-data-service-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2b081-126">For more information, see [Querying the Data Service](querying-the-data-service-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="2b081-127">客户端分两个部分来执行 LINQ 查询。</span><span class="sxs-lookup"><span data-stu-id="2b081-127">The client executes a LINQ query in two parts.</span></span> <span data-ttu-id="2b081-128">只要有可能，将首先在客户端上计算查询中的 LINQ 表达式，然后生成基于 URI 的查询并将其发送至数据服务，以针对服务中的数据进行计算。</span><span class="sxs-lookup"><span data-stu-id="2b081-128">Whenever possible, LINQ expressions in a query are first evaluated on the client, and then a URI-based query is generated and sent to the data service for evaluation against data in the service.</span></span> <span data-ttu-id="2b081-129">有关详细信息，请参阅[查询数据服务](querying-the-data-service-wcf-data-services.md)中的[客户端与服务器执行](querying-the-data-service-wcf-data-services.md#executingQueries)的部分。</span><span class="sxs-lookup"><span data-stu-id="2b081-129">For more information, see the section [Client versus Server Execution](querying-the-data-service-wcf-data-services.md#executingQueries) in [Querying the Data Service](querying-the-data-service-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="2b081-130">如果 LINQ 查询无法在符合 OData 的查询 URI 中进行转换，则在尝试执行时将引发异常。</span><span class="sxs-lookup"><span data-stu-id="2b081-130">When a LINQ query cannot be translated in an OData-compliant query URI, an exception is raised when execution is attempted.</span></span> <span data-ttu-id="2b081-131">有关详细信息，请参阅 [查询数据服务](querying-the-data-service-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2b081-131">For more information, see [Querying the Data Service](querying-the-data-service-wcf-data-services.md).</span></span>  
  
## <a name="linq-query-examples"></a><span data-ttu-id="2b081-132">LINQ 查询示例</span><span class="sxs-lookup"><span data-stu-id="2b081-132">LINQ Query Examples</span></span>  

 <span data-ttu-id="2b081-133">以下部分中的示例演示了可以对 OData 服务执行的 LINQ 查询的类型。</span><span class="sxs-lookup"><span data-stu-id="2b081-133">The examples in the following sections demonstrate the kinds of LINQ queries that can be executed against an OData service.</span></span>  
  
<a name="filtering"></a>

### <a name="filtering"></a><span data-ttu-id="2b081-134">筛选</span><span class="sxs-lookup"><span data-stu-id="2b081-134">Filtering</span></span>  

 <span data-ttu-id="2b081-135">本小节中的 LINQ 查询示例将筛选由服务返回的源中的数据。</span><span class="sxs-lookup"><span data-stu-id="2b081-135">The LINQ query examples in this section filter data in the feed returned by the service.</span></span>  
  
 <span data-ttu-id="2b081-136">下面这些示例是等效的查询，它们将筛选返回的 `Orders` 实体并仅返回运费成本高于 30 美元的订单：</span><span class="sxs-lookup"><span data-stu-id="2b081-136">The following examples are equivalent queries that filter the returned `Orders` entities so that only orders with a freight cost greater than $30 are returned:</span></span>  
  
- <span data-ttu-id="2b081-137">使用 LINQ 查询语法：</span><span class="sxs-lookup"><span data-stu-id="2b081-137">Using LINQ query syntax:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqWhereClauseSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqwhereclausespecific)]
[!code-vb[Astoria Northwind Client#LinqWhereClauseSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqwhereclausespecific)]
  
- <span data-ttu-id="2b081-138">使用 LINQ 查询方法：</span><span class="sxs-lookup"><span data-stu-id="2b081-138">Using LINQ query methods:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqWhereMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqwheremethodspecific)]
[!code-vb[Astoria Northwind Client#LinqWhereMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqwheremethodspecific)]
  
- <span data-ttu-id="2b081-139">URI 查询字符串 `$filter` 选项：</span><span class="sxs-lookup"><span data-stu-id="2b081-139">The URI query string `$filter` option:</span></span>  
  
[!code-csharp[Astoria Northwind Client#ExplicitQueryWhereMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#explicitquerywheremethodspecific)]
[!code-vb[Astoria Northwind Client#ExplicitQueryWhereMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#explicitquerywheremethodspecific)]
  
 <span data-ttu-id="2b081-140">前面的所有示例都将转换为查询 URI：`http://localhost:12345/northwind.svc/Orders()?$filter=Freight gt 30M`。</span><span class="sxs-lookup"><span data-stu-id="2b081-140">All of the previous examples are translated to the query URI: `http://localhost:12345/northwind.svc/Orders()?$filter=Freight gt 30M`.</span></span>  
  
<a name="sorting"></a>

### <a name="sorting"></a><span data-ttu-id="2b081-141">排序</span><span class="sxs-lookup"><span data-stu-id="2b081-141">Sorting</span></span>  

 <span data-ttu-id="2b081-142">下面的示例显示了按公司名称和邮政编码降序排序返回的数据的等效查询：</span><span class="sxs-lookup"><span data-stu-id="2b081-142">The following examples show equivalent queries that sort returned data both by the company name and by postal code, descending:</span></span>  
  
- <span data-ttu-id="2b081-143">使用 LINQ 查询语法：</span><span class="sxs-lookup"><span data-stu-id="2b081-143">Using LINQ query syntax:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqOrderByClauseSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqorderbyclausespecific)]
[!code-vb[Astoria Northwind Client#LinqOrderByClauseSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqorderbyclausespecific)]
  
- <span data-ttu-id="2b081-144">使用 LINQ 查询方法：</span><span class="sxs-lookup"><span data-stu-id="2b081-144">Using LINQ query methods:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqOrderByMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqorderbymethodspecific)]
[!code-vb[Astoria Northwind Client#LinqOrderByMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqorderbymethodspecific)]
  
- <span data-ttu-id="2b081-145">URI 查询字符串 `$orderby` 选项：</span><span class="sxs-lookup"><span data-stu-id="2b081-145">URI query string `$orderby` option):</span></span>  
  
[!code-csharp[Astoria Northwind Client#ExplicitQueryOrderByMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#explicitqueryorderbymethodspecific)]
[!code-vb[Astoria Northwind Client#ExplicitQueryOrderByMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#explicitqueryorderbymethodspecific)]
  
 <span data-ttu-id="2b081-146">前面的所有示例都将转换为查询 URI：`http://localhost:12345/northwind.svc/Customers()?$orderby=CompanyName,PostalCode desc`。</span><span class="sxs-lookup"><span data-stu-id="2b081-146">All of the previous examples are translated to the query URI: `http://localhost:12345/northwind.svc/Customers()?$orderby=CompanyName,PostalCode desc`.</span></span>  
  
<a name="projection"></a>

### <a name="projection"></a><span data-ttu-id="2b081-147">投影</span><span class="sxs-lookup"><span data-stu-id="2b081-147">Projection</span></span>  

 <span data-ttu-id="2b081-148">下面的示例显示了将返回的数据投影到较窄的 `CustomerAddress` 类型的等效查询：</span><span class="sxs-lookup"><span data-stu-id="2b081-148">The following examples show equivalent queries that project returned data into the narrower `CustomerAddress` type:</span></span>  
  
- <span data-ttu-id="2b081-149">使用 LINQ 查询语法：</span><span class="sxs-lookup"><span data-stu-id="2b081-149">Using LINQ query syntax:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqSelectClauseSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqselectclausespecific)]
[!code-vb[Astoria Northwind Client#LinqSelectClauseSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqselectclausespecific)]
  
- <span data-ttu-id="2b081-150">使用 LINQ 查询方法：</span><span class="sxs-lookup"><span data-stu-id="2b081-150">Using LINQ query methods:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqSelectMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqselectmethodspecific)]
[!code-vb[Astoria Northwind Client#LinqSelectMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqselectmethodspecific)]

> [!NOTE]
> <span data-ttu-id="2b081-151">不能使用 `$select` 方法将 <xref:System.Data.Services.Client.DataServiceQuery%601.AddQueryOption%2A> 查询选项添加到查询 URI 中。</span><span class="sxs-lookup"><span data-stu-id="2b081-151">The `$select` query option cannot be added to a query URI by using the <xref:System.Data.Services.Client.DataServiceQuery%601.AddQueryOption%2A> method.</span></span> <span data-ttu-id="2b081-152">我们建议使用 LINQ <xref:System.Linq.Enumerable.Select%2A> 方法，让客户端在请求 URI 中生成 `$select` 查询选项。</span><span class="sxs-lookup"><span data-stu-id="2b081-152">We recommend that you use the LINQ <xref:System.Linq.Enumerable.Select%2A> method to have the client generate the `$select` query option in the request URI.</span></span>  
  
 <span data-ttu-id="2b081-153">前面的两个示例都将转换为查询 URI：`"http://localhost:12345/northwind.svc/Customers()?$filter=Country eq 'GerGerm'&$select=CustomerID,Address,City,Region,PostalCode,Country"`。</span><span class="sxs-lookup"><span data-stu-id="2b081-153">Both of the previous examples are translated to the query URI: `"http://localhost:12345/northwind.svc/Customers()?$filter=Country eq 'GerGerm'&$select=CustomerID,Address,City,Region,PostalCode,Country"`.</span></span>  
  
<a name="paging"></a>

### <a name="client-paging"></a><span data-ttu-id="2b081-154">客户端分页</span><span class="sxs-lookup"><span data-stu-id="2b081-154">Client Paging</span></span>  

 <span data-ttu-id="2b081-155">下面所示的等效查询示例将请求返回一页包含 25 个订单的排序订单实体，并跳过前 50 个订单：</span><span class="sxs-lookup"><span data-stu-id="2b081-155">The following examples show equivalent queries that request a page of sorted order entities that includes 25 orders, skipping the first 50 orders:</span></span>  
  
- <span data-ttu-id="2b081-156">为 LINQ 查询应用查询方法：</span><span class="sxs-lookup"><span data-stu-id="2b081-156">Applying query methods to a LINQ query:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqSkipTakeMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqskiptakemethodspecific)]
[!code-vb[Astoria Northwind Client#LinqSkipTakeMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqskiptakemethodspecific)]
  
- <span data-ttu-id="2b081-157">URI 查询字符串 `$skip` 和 `$top` 选项：</span><span class="sxs-lookup"><span data-stu-id="2b081-157">URI query string `$skip` and `$top` options):</span></span>  
  
[!code-csharp[Astoria Northwind Client#ExplicitQuerySkipTakeMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#explicitqueryskiptakemethodspecific)]
[!code-vb[Astoria Northwind Client#ExplicitQuerySkipTakeMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#explicitqueryskiptakemethodspecific)]
  
 <span data-ttu-id="2b081-158">前面的两个示例都将转换为查询 URI：`http://localhost:12345/northwind.svc/Orders()?$orderby=OrderDate desc&$skip=50&$top=25`。</span><span class="sxs-lookup"><span data-stu-id="2b081-158">Both of the previous examples are translated to the query URI: `http://localhost:12345/northwind.svc/Orders()?$orderby=OrderDate desc&$skip=50&$top=25`.</span></span>  
  
<a name="expand"></a>

### <a name="expand"></a><span data-ttu-id="2b081-159">展开</span><span class="sxs-lookup"><span data-stu-id="2b081-159">Expand</span></span>  

 <span data-ttu-id="2b081-160">查询 OData 数据服务时，您可以请求将与查询针对的实体相关的实体包含在返回的源中。</span><span class="sxs-lookup"><span data-stu-id="2b081-160">When you query an OData data service, you can request that entities related to the entity targeted by the query be included the returned feed.</span></span> <span data-ttu-id="2b081-161">针对 LINQ 查询的目标实体集调用 <xref:System.Data.Services.Client.DataServiceQuery%601.Expand%2A> 的 <xref:System.Data.Services.Client.DataServiceQuery%601> 方法，相关实体集名称作为 `path` 参数提供。</span><span class="sxs-lookup"><span data-stu-id="2b081-161">The <xref:System.Data.Services.Client.DataServiceQuery%601.Expand%2A> method is called on the <xref:System.Data.Services.Client.DataServiceQuery%601> for the entity set targeted by the LINQ query, with the related entity set name supplied as the `path` parameter.</span></span> <span data-ttu-id="2b081-162">有关详细信息，请参阅 [加载延迟的内容](loading-deferred-content-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2b081-162">For more information, see [Loading Deferred Content](loading-deferred-content-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="2b081-163">下面的示例显示了在查询中使用 <xref:System.Data.Services.Client.DataServiceQuery%601.Expand%2A> 方法的等效方式：</span><span class="sxs-lookup"><span data-stu-id="2b081-163">The following examples show equivalent ways to use the <xref:System.Data.Services.Client.DataServiceQuery%601.Expand%2A> method in a query:</span></span>  
  
- <span data-ttu-id="2b081-164">在 LINQ 查询语法中：</span><span class="sxs-lookup"><span data-stu-id="2b081-164">In LINQ query syntax:</span></span>  
  
[!code-csharp[Astoria Northwind Client#LinqQueryExpandSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqqueryexpandspecific)]
[!code-vb[Astoria Northwind Client#LinqQueryExpandSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqqueryexpandspecific)]  
  
- <span data-ttu-id="2b081-165">使用 LINQ 查询方法：</span><span class="sxs-lookup"><span data-stu-id="2b081-165">With LINQ query methods:</span></span>  

[!code-csharp[Astoria Northwind Client#LinqQueryExpandMethodSpecific](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#linqqueryexpandmethodspecific)]
[!code-vb[Astoria Northwind Client#LinqQueryExpandMethodSpecific](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#linqqueryexpandmethodspecific)]

 <span data-ttu-id="2b081-166">前面的两个示例都将转换为查询 URI：`http://localhost:12345/northwind.svc/Orders()?$filter=CustomerID eq 'ALFKI'&$expand=Order_Details`。</span><span class="sxs-lookup"><span data-stu-id="2b081-166">Both of the previous examples are translated to the query URI: `http://localhost:12345/northwind.svc/Orders()?$filter=CustomerID eq 'ALFKI'&$expand=Order_Details`.</span></span>  
  
<a name="unsupportedMethods"></a>

## <a name="unsupported-linq-methods"></a><span data-ttu-id="2b081-167">不支持的 LINQ 方法</span><span class="sxs-lookup"><span data-stu-id="2b081-167">Unsupported LINQ Methods</span></span>  

 <span data-ttu-id="2b081-168">下表包含不支持的 LINQ 方法的类，并且不能包含在针对 OData 服务执行的查询中：</span><span class="sxs-lookup"><span data-stu-id="2b081-168">The following table contains the classes of LINQ methods are not supported and cannot be included in a query executed against an OData service:</span></span>  
  
|<span data-ttu-id="2b081-169">操作类型</span><span class="sxs-lookup"><span data-stu-id="2b081-169">Operation Type</span></span>|<span data-ttu-id="2b081-170">不支持的方法</span><span class="sxs-lookup"><span data-stu-id="2b081-170">Unsupported Method</span></span>|  
|--------------------|------------------------|  
|<span data-ttu-id="2b081-171">集合运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-171">Set operators</span></span>|<span data-ttu-id="2b081-172">所有集合运算符都不能用于 <xref:System.Data.Services.Client.DataServiceQuery%601>，其中包括：</span><span class="sxs-lookup"><span data-stu-id="2b081-172">All set operators are unsupported against a <xref:System.Data.Services.Client.DataServiceQuery%601>, which included the following:</span></span><br /><br /> -   <xref:System.Linq.Enumerable.All%2A><br />-   <xref:System.Linq.Enumerable.Any%2A><br />-   <xref:System.Linq.Enumerable.Concat%2A><br />-   <xref:System.Linq.Enumerable.DefaultIfEmpty%2A><br />-   <xref:System.Linq.Enumerable.Distinct%2A><br />-   <xref:System.Linq.Enumerable.Except%2A><br />-   <xref:System.Linq.Enumerable.Intersect%2A><br />-   <xref:System.Linq.Enumerable.Union%2A><br />-   <xref:System.Linq.Enumerable.Zip%2A>|  
|<span data-ttu-id="2b081-173">排序运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-173">Ordering operators</span></span>|<span data-ttu-id="2b081-174">要求 <xref:System.Collections.Generic.IComparer%601> 的以下排序运算符不能用于 <xref:System.Data.Services.Client.DataServiceQuery%601>：</span><span class="sxs-lookup"><span data-stu-id="2b081-174">The following ordering operators that require <xref:System.Collections.Generic.IComparer%601> are unsupported against a <xref:System.Data.Services.Client.DataServiceQuery%601>:</span></span><br /><br /> -   <xref:System.Linq.Enumerable.OrderBy%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%2CSystem.Collections.Generic.IComparer%7B%60%601%7D%29><br />-   <xref:System.Linq.Enumerable.OrderByDescending%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%2CSystem.Collections.Generic.IComparer%7B%60%601%7D%29><br />-   <xref:System.Linq.Enumerable.ThenBy%60%602%28System.Linq.IOrderedEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%2CSystem.Collections.Generic.IComparer%7B%60%601%7D%29><br />-   <xref:System.Linq.Enumerable.ThenByDescending%60%602%28System.Linq.IOrderedEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%2CSystem.Collections.Generic.IComparer%7B%60%601%7D%29>|  
|<span data-ttu-id="2b081-175">投影和筛选运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-175">Projection and filtering operators</span></span>|<span data-ttu-id="2b081-176">以下接受位置自变量的投影和筛选运算符不能用于 <xref:System.Data.Services.Client.DataServiceQuery%601>：</span><span class="sxs-lookup"><span data-stu-id="2b081-176">The following projection and filtering operators that accept a positional argument are unsupported against a <xref:System.Data.Services.Client.DataServiceQuery%601>:</span></span><br /><br /> -   <xref:System.Linq.Enumerable.Join%60%604%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%2CSystem.Func%7B%60%600%2C%60%602%7D%2CSystem.Func%7B%60%601%2C%60%602%7D%2CSystem.Func%7B%60%600%2C%60%601%2C%60%603%7D%2CSystem.Collections.Generic.IEqualityComparer%7B%60%602%7D%29><br />-   <xref:System.Linq.Enumerable.Select%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2CSystem.Int32%2C%60%601%7D%29><br />-   <xref:System.Linq.Enumerable.SelectMany%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%7D%29><br />-   <xref:System.Linq.Enumerable.SelectMany%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2CSystem.Int32%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%7D%29><br />-   <xref:System.Linq.Enumerable.SelectMany%60%603%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%7D%2CSystem.Func%7B%60%600%2C%60%601%2C%60%602%7D%29><br />-   <xref:System.Linq.Enumerable.SelectMany%60%603%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2CSystem.Int32%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%7D%2CSystem.Func%7B%60%600%2C%60%601%2C%60%602%7D%29><br />-   <xref:System.Linq.Enumerable.Where%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2CSystem.Int32%2CSystem.Boolean%7D%29>|  
|<span data-ttu-id="2b081-177">分组运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-177">Grouping operators</span></span>|<span data-ttu-id="2b081-178">所有分组运算符都不能用于 <xref:System.Data.Services.Client.DataServiceQuery%601>，其中包括：</span><span class="sxs-lookup"><span data-stu-id="2b081-178">All grouping operators are unsupported against a <xref:System.Data.Services.Client.DataServiceQuery%601>, including the following:</span></span><br /><br /> -   <xref:System.Linq.Enumerable.GroupBy%2A><br />-   <xref:System.Linq.Enumerable.GroupJoin%2A><br /><br /> <span data-ttu-id="2b081-179">分组运算符必须在客户端上执行。</span><span class="sxs-lookup"><span data-stu-id="2b081-179">Grouping operations must be performed on the client.</span></span>|  
|<span data-ttu-id="2b081-180">聚合运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-180">Aggregate operators</span></span>|<span data-ttu-id="2b081-181">所有聚合运算符都不能用于 <xref:System.Data.Services.Client.DataServiceQuery%601>，其中包括：</span><span class="sxs-lookup"><span data-stu-id="2b081-181">All aggregate operations are unsupported against a <xref:System.Data.Services.Client.DataServiceQuery%601>, including the following:</span></span><br /><br /> -   <xref:System.Linq.Enumerable.Aggregate%2A><br />-   <xref:System.Linq.Enumerable.Average%2A><br />-   <xref:System.Linq.Enumerable.Count%2A><br />-   <xref:System.Linq.Enumerable.LongCount%2A><br />-   <xref:System.Linq.Enumerable.Max%2A><br />-   <xref:System.Linq.Enumerable.Min%2A><br />-   <xref:System.Linq.Enumerable.Sum%2A><br /><br /> <span data-ttu-id="2b081-182">聚合运算符必须在客户端上执行或由服务操作封装。</span><span class="sxs-lookup"><span data-stu-id="2b081-182">Aggregate operations must either be performed on the client or be encapsulated by a service operation.</span></span>|  
|<span data-ttu-id="2b081-183">分页运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-183">Paging operators</span></span>|<span data-ttu-id="2b081-184">以下分页运算符不能用于 <xref:System.Data.Services.Client.DataServiceQuery%601>：</span><span class="sxs-lookup"><span data-stu-id="2b081-184">The following paging operators are not supported against a <xref:System.Data.Services.Client.DataServiceQuery%601>:</span></span><br /><br /> -   <xref:System.Linq.Enumerable.ElementAt%2A><br />-   <xref:System.Linq.Enumerable.Last%2A><br />-   <xref:System.Linq.Enumerable.LastOrDefault%2A><br />-   <xref:System.Linq.Enumerable.SkipWhile%2A><br />-   <xref:System.Linq.Enumerable.TakeWhile%2A><br/><br/><span data-ttu-id="2b081-185">**注意：**  对空序列执行的分页运算符将返回 null。</span><span class="sxs-lookup"><span data-stu-id="2b081-185">**Note:**  Paging operators that are executed on an empty sequence return null.</span></span>|  
|<span data-ttu-id="2b081-186">其他运算符</span><span class="sxs-lookup"><span data-stu-id="2b081-186">Other operators</span></span>|<span data-ttu-id="2b081-187">还不支持以下运算符 <xref:System.Data.Services.Client.DataServiceQuery%601> ：</span><span class="sxs-lookup"><span data-stu-id="2b081-187">The following operators are also not supported against a <xref:System.Data.Services.Client.DataServiceQuery%601>:</span></span><br /><br /> - <xref:System.Linq.Enumerable.Empty%2A><br />- <xref:System.Linq.Enumerable.Range%2A><br />- <xref:System.Linq.Enumerable.Repeat%2A><br />- <xref:System.Linq.Enumerable.ToDictionary%2A><br />- <xref:System.Linq.Enumerable.ToLookup%2A>|  
  
<a name="supportedExpressions"></a>

## <a name="supported-expression-functions"></a><span data-ttu-id="2b081-188">支持的表达式函数</span><span class="sxs-lookup"><span data-stu-id="2b081-188">Supported Expression Functions</span></span>  

 <span data-ttu-id="2b081-189">支持以下公共语言运行时 (CLR) 方法和属性，因为这些方法和属性可以在查询表达式中进行转换，以便将其包含在请求 URI 中以包含在 OData 服务中：</span><span class="sxs-lookup"><span data-stu-id="2b081-189">The following common-language runtime (CLR) methods and properties are supported because they can be translated in a query expression for inclusion in the request URI to an OData service:</span></span>  
  
|<span data-ttu-id="2b081-190"><xref:System.String> 成员</span><span class="sxs-lookup"><span data-stu-id="2b081-190"><xref:System.String> Member</span></span>|<span data-ttu-id="2b081-191">支持的 OData 函数</span><span class="sxs-lookup"><span data-stu-id="2b081-191">Supported OData Function</span></span>|  
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|  
|<xref:System.String.Concat%28System.String%2CSystem.String%29>|`string concat(string p0, string p1)`|  
|<xref:System.String.Contains%28System.String%29>|`bool substringof(string p0, string p1)`|  
|<xref:System.String.EndsWith%28System.String%29>|`bool endswith(string p0, string p1)`|  
|<xref:System.String.IndexOf%28System.String%2CSystem.Int32%29>|`int indexof(string p0, string p1)`|  
|<xref:System.String.Length>|`int length(string p0)`|  
|<xref:System.String.Replace%28System.String%2CSystem.String%29>|`string replace(string p0, string find, string replace)`|  
|<xref:System.String.Substring%28System.Int32%29>|`string substring(string p0, int pos)`|  
|<xref:System.String.Substring%28System.Int32%2CSystem.Int32%29>|`string substring(string p0, int pos, int length)`|  
|<xref:System.String.ToLower>|`string tolower(string p0)`|  
|<xref:System.String.ToUpper>|`string toupper(string p0)`|  
|<xref:System.String.Trim>|`string trim(string p0)`|  
  
|<span data-ttu-id="2b081-192"><xref:System.DateTime> 成员<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="2b081-192"><xref:System.DateTime> Member<sup>1</sup></span></span>|<span data-ttu-id="2b081-193">支持的 OData 函数</span><span class="sxs-lookup"><span data-stu-id="2b081-193">Supported OData Function</span></span>|  
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|  
|<xref:System.DateTime.Day>|`int day(DateTime p0)`|  
|<xref:System.DateTime.Hour>|`int hour(DateTime p0)`|  
|<xref:System.DateTime.Minute>|`int minute(DateTime p0)`|  
|<xref:System.DateTime.Month>|`int month(DateTime p0)`|  
|<xref:System.DateTime.Second>|`int second(DateTime p0)`|  
|<xref:System.DateTime.Year>|`int year(DateTime p0)`|  
  
 <span data-ttu-id="2b081-194"><sup>1</sup>和 Visual Basic 中的等效的日期和时间属性 <xref:Microsoft.VisualBasic.DateAndTime?displayProperty=nameWithType> <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A> 也受支持。</span><span class="sxs-lookup"><span data-stu-id="2b081-194"><sup>1</sup>The equivalent date and time properties of <xref:Microsoft.VisualBasic.DateAndTime?displayProperty=nameWithType> and the <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A> method in Visual Basic are also supported.</span></span>  
  
|<span data-ttu-id="2b081-195"><xref:System.Math> 成员</span><span class="sxs-lookup"><span data-stu-id="2b081-195"><xref:System.Math> Member</span></span>|<span data-ttu-id="2b081-196">支持的 OData 函数</span><span class="sxs-lookup"><span data-stu-id="2b081-196">Supported OData Function</span></span>|  
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|  
|<xref:System.Math.Ceiling%28System.Decimal%29>|`decimal ceiling(decimal p0)`|  
|<xref:System.Math.Ceiling%28System.Double%29>|`double ceiling(double p0)`|  
|<xref:System.Math.Floor%28System.Decimal%29>|`decimal floor(decimal p0)`|  
|<xref:System.Math.Floor%28System.Double%29>|`double floor(double p0)`|  
|<xref:System.Math.Round%28System.Decimal%29>|`decimal round(decimal p0)`|  
|<xref:System.Math.Round%28System.Double%29>|`double round(double p0)`|  
  
|<span data-ttu-id="2b081-197"><xref:System.Linq.Expressions.Expression> 成员</span><span class="sxs-lookup"><span data-stu-id="2b081-197"><xref:System.Linq.Expressions.Expression> Member</span></span>|<span data-ttu-id="2b081-198">支持的 OData 函数</span><span class="sxs-lookup"><span data-stu-id="2b081-198">Supported OData Function</span></span>|  
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|  
|<xref:System.Linq.Expressions.Expression.TypeIs%28System.Linq.Expressions.Expression%2CSystem.Type%29>|`bool isof(type p0)`|  
  
 <span data-ttu-id="2b081-199">客户端或许还可以在客户端上计算其他 CLR 函数。</span><span class="sxs-lookup"><span data-stu-id="2b081-199">The client may also be able to evaluate additional CLR functions on the client.</span></span> <span data-ttu-id="2b081-200">对于无法在客户端上计算以及无法转换为有效请求 URI 以便在服务器上计算的任何表达式，将引发 <xref:System.NotSupportedException>。</span><span class="sxs-lookup"><span data-stu-id="2b081-200">A <xref:System.NotSupportedException> is raised for any expression that cannot be evaluated on the client and cannot be translated into a valid request URI for evaluation on the server.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b081-201">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b081-201">See also</span></span>

- [<span data-ttu-id="2b081-202">查询数据服务</span><span class="sxs-lookup"><span data-stu-id="2b081-202">Querying the Data Service</span></span>](querying-the-data-service-wcf-data-services.md)
- [<span data-ttu-id="2b081-203">查询投影</span><span class="sxs-lookup"><span data-stu-id="2b081-203">Query Projections</span></span>](query-projections-wcf-data-services.md)
- [<span data-ttu-id="2b081-204">对象具体化</span><span class="sxs-lookup"><span data-stu-id="2b081-204">Object Materialization</span></span>](object-materialization-wcf-data-services.md)
- [<span data-ttu-id="2b081-205">OData：URI 约定</span><span class="sxs-lookup"><span data-stu-id="2b081-205">OData: URI Conventions</span></span>](https://www.odata.org/documentation/odata-version-2-0/uri-conventions/)
