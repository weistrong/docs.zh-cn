---
description: 了解详细信息：如何查询信息
title: 如何：查询信息
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e538d288-2070-40ca-9da6-4fbc68cd6ad0
ms.openlocfilehash: 41774834fe919b28d71691203941cb8e0a8a0397
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802016"
---
# <a name="how-to-query-for-information"></a><span data-ttu-id="c7618-103">如何：查询信息</span><span class="sxs-lookup"><span data-stu-id="c7618-103">How to: Query for Information</span></span>

<span data-ttu-id="c7618-104">中 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 的查询使用的语法与 LINQ 中的查询相同。</span><span class="sxs-lookup"><span data-stu-id="c7618-104">Queries in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] use the same syntax as queries in LINQ.</span></span> <span data-ttu-id="c7618-105">唯一的区别是查询中引用的对象 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 映射到数据库中的元素。</span><span class="sxs-lookup"><span data-stu-id="c7618-105">The only difference is that the objects referenced in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] queries are mapped to elements in a database.</span></span> <span data-ttu-id="c7618-106">有关详细信息，请参阅 [LINQ 查询简介 (C#)](../../../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="c7618-106">For more information, see [Introduction to LINQ Queries (C#)](../../../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).</span></span>  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="c7618-107">将您编写的查询转换成等效的 SQL 查询，然后将它们发送至服务器进行处理。</span><span class="sxs-lookup"><span data-stu-id="c7618-107">translates the queries you write into equivalent SQL queries and sends them to the server for processing.</span></span>  
  
 <span data-ttu-id="c7618-108">LINQ 查询的某些功能在应用程序中可能需要特别注意 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="c7618-108">Some features of LINQ queries might need special attention in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] applications.</span></span> <span data-ttu-id="c7618-109">有关详细信息，请参阅 [查询概念](query-concepts.md)。</span><span class="sxs-lookup"><span data-stu-id="c7618-109">For more information, see [Query Concepts](query-concepts.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c7618-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7618-110">Example</span></span>  

 <span data-ttu-id="c7618-111">下面的查询请求来自伦敦的客户的列表。</span><span class="sxs-lookup"><span data-stu-id="c7618-111">The following query asks for a list of customers from London.</span></span> <span data-ttu-id="c7618-112">在此示例中，`Customers` 是 Northwind 示例数据库中的表。</span><span class="sxs-lookup"><span data-stu-id="c7618-112">In this example, `Customers` is a table in the Northwind sample database.</span></span>  
  
 [!code-csharp[DLinqQuerying#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#1)]
 [!code-vb[DLinqQuerying#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="c7618-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7618-113">See also</span></span>

- [<span data-ttu-id="c7618-114">创建对象模型</span><span class="sxs-lookup"><span data-stu-id="c7618-114">Creating the Object Model</span></span>](creating-the-object-model.md)
- [<span data-ttu-id="c7618-115">下载示例数据库</span><span class="sxs-lookup"><span data-stu-id="c7618-115">Downloading Sample Databases</span></span>](downloading-sample-databases.md)
- [<span data-ttu-id="c7618-116">查询数据库</span><span class="sxs-lookup"><span data-stu-id="c7618-116">Querying the Database</span></span>](querying-the-database.md)
