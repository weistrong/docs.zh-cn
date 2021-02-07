---
description: 了解详细信息：查询表达式语法示例：导航关系
title: 查询表达式语法示例：导航关系
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0d4a7f41-c758-4059-8f83-d2e9c2745593
ms.openlocfilehash: 0548cba8d1d3d834da6a8416cb444898981b4123
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696147"
---
# <a name="query-expression-syntax-examples-navigating-relationships"></a><span data-ttu-id="3f5c5-103">查询表达式语法示例：导航关系</span><span class="sxs-lookup"><span data-stu-id="3f5c5-103">Query Expression Syntax Examples: Navigating Relationships</span></span>

<span data-ttu-id="3f5c5-104">实体框架中的导航属性是快捷方式属性，用于定位位于关联末尾的实体。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-104">Navigation properties in the Entity Framework are shortcut properties used to locate the entities at the ends of an association.</span></span> <span data-ttu-id="3f5c5-105">导航属性允许用户通过关联集从一个实体导航到另一个实体或从一个实体导航到多个相关的实体。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-105">Navigation properties allow a user to navigate from one entity to another, or from one entity to related entities through an association set.</span></span> <span data-ttu-id="3f5c5-106">本主题提供了有关如何通过 LINQ to Entities 查询中的导航属性来导航关系的查询表达式语法的示例。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-106">This topic provides examples in query expression syntax of how to navigate relationships through navigation properties in LINQ to Entities queries.</span></span>  
  
 <span data-ttu-id="3f5c5-107">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-107">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="3f5c5-108">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="3f5c5-108">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="example"></a><span data-ttu-id="3f5c5-109">示例</span><span class="sxs-lookup"><span data-stu-id="3f5c5-109">Example</span></span>  

 <span data-ttu-id="3f5c5-110">以下示例使用 <xref:System.Linq.Queryable.Select%2A> 方法以获取所有联系人 ID 和姓氏为“Zhou”的每个联系人的应付款总计。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-110">The following example uses the <xref:System.Linq.Queryable.Select%2A> method to get all the contact IDs and the sum of the total due for each contact whose last name is "Zhou".</span></span> <span data-ttu-id="3f5c5-111">`Contact.SalesOrderHeader` 导航属性用于获取每个联系人的 `SalesOrderHeader` 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-111">The `Contact.SalesOrderHeader` navigation property is used to get the collection of `SalesOrderHeader` objects for each contact.</span></span> <span data-ttu-id="3f5c5-112">`Sum` 方法使用 `Contact.SalesOrderHeader` 导航属性以汇总每个联系人的所有订单的应付款总计。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-112">The `Sum` method uses the `Contact.SalesOrderHeader` navigation property to sum the total due of all the orders for each contact.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectEachContactsOrders2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selecteachcontactsorders2)]
 [!code-vb[DP L2E Examples#SelectEachContactsOrders2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selecteachcontactsorders2)]  
  
## <a name="example"></a><span data-ttu-id="3f5c5-113">示例</span><span class="sxs-lookup"><span data-stu-id="3f5c5-113">Example</span></span>  

 <span data-ttu-id="3f5c5-114">以下示例获取其姓氏为“Zhou”的联系人的所有订单。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-114">The following example gets all the orders of the contacts whose last name is "Zhou".</span></span> <span data-ttu-id="3f5c5-115">`Contact.SalesOrderHeader` 导航属性用于获取每个联系人的 `SalesOrderHeader` 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-115">The `Contact.SalesOrderHeader` navigation property is used to get the collection of `SalesOrderHeader` objects for each contact.</span></span> <span data-ttu-id="3f5c5-116">联系人的姓名和订单以匿名类型返回。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-116">The contact's name and orders are returned in an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectEachContactsOrders3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selecteachcontactsorders3)]
 [!code-vb[DP L2E Examples#SelectEachContactsOrders3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selecteachcontactsorders3)]  
  
## <a name="example"></a><span data-ttu-id="3f5c5-117">示例</span><span class="sxs-lookup"><span data-stu-id="3f5c5-117">Example</span></span>  

 <span data-ttu-id="3f5c5-118">以下示例使用 `SalesOrderHeader.Address` 和 `SalesOrderHeader.Contact` 导航属性以获取与每个订单关联的 `Address` 对象和 `Contact` 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-118">The following example uses the `SalesOrderHeader.Address` and `SalesOrderHeader.Contact` navigation properties get the collection of `Address` and `Contact` objects associated with each order.</span></span> <span data-ttu-id="3f5c5-119">Seattle 城市发生的每个订单的联系人姓氏、街道地址、销售订单号和应付款总计将以匿名类型返回。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-119">The last name of the contact, the street address, the sales order number, and the total due for each order to the city of Seattle are returned in an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GetOrderInfoThruRelationships](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#getorderinfothrurelationships)]
 [!code-vb[DP L2E Examples#GetOrderInfoThruRelationships](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#getorderinfothrurelationships)]  
  
### <a name="example"></a><span data-ttu-id="3f5c5-120">示例</span><span class="sxs-lookup"><span data-stu-id="3f5c5-120">Example</span></span>  

 <span data-ttu-id="3f5c5-121">以下示例使用 `Where` 方法以查找在 2003 年 12 月 1 日之后生成的订单，然后使用 `order.SalesOrderDetail` 导航属性以获取每个订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3f5c5-121">The following example uses the `Where` method to find orders that were made after December 1, 2003, and then uses the `order.SalesOrderDetail` navigation property to get the details for each order.</span></span>  
  
 [!code-csharp[DP L2E Examples#WhereNavProperty](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#wherenavproperty)]
 [!code-vb[DP L2E Examples#WhereNavProperty](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#wherenavproperty)]  
  
## <a name="see-also"></a><span data-ttu-id="3f5c5-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f5c5-122">See also</span></span>

- [<span data-ttu-id="3f5c5-123">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="3f5c5-123">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
