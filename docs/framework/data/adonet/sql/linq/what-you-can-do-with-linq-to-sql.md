---
description: 了解详细信息：可以对 LINQ to SQL 执行的操作
title: 使用 LINQ to SQL 可执行的操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 061d98b2-baa7-4336-8ad2-c14de8134d91
ms.openlocfilehash: adf1d8dfab69db27d15634a12dbdfbfa287dbb4c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791746"
---
# <a name="what-you-can-do-with-linq-to-sql"></a><span data-ttu-id="9a700-103">使用 LINQ to SQL 可执行的操作</span><span class="sxs-lookup"><span data-stu-id="9a700-103">What You Can Do With LINQ to SQL</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="9a700-104">支持您作为 SQL 开发人员所期望的所有关键功能。</span><span class="sxs-lookup"><span data-stu-id="9a700-104">supports all the key capabilities you would expect as a SQL developer.</span></span> <span data-ttu-id="9a700-105">您可以查询表中的信息、在表中插入信息以及更新和删除表中的信息。</span><span class="sxs-lookup"><span data-stu-id="9a700-105">You can query for information, and insert, update, and delete information from tables.</span></span>  
  
## <a name="selecting"></a><span data-ttu-id="9a700-106">选择</span><span class="sxs-lookup"><span data-stu-id="9a700-106">Selecting</span></span>  

 <span data-ttu-id="9a700-107">选择 (*投影*) 只需编写您自己的编程语言的 LINQ 查询，然后执行该查询以检索结果。</span><span class="sxs-lookup"><span data-stu-id="9a700-107">Selecting (*projection*) is achieved by just writing a LINQ query in your own programming language, and then executing that query to retrieve the results.</span></span> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="9a700-108">自行将所有必要操作转换为您所熟悉的必要 SQL 操作。</span><span class="sxs-lookup"><span data-stu-id="9a700-108">itself translates all the necessary operations into the necessary SQL operations that you are familiar with.</span></span> <span data-ttu-id="9a700-109">有关详细信息，请参阅 [LINQ to SQL](index.md)。</span><span class="sxs-lookup"><span data-stu-id="9a700-109">For more information, see [LINQ to SQL](index.md).</span></span>  
  
 <span data-ttu-id="9a700-110">在下面的示例中，检索来自伦敦的客户的公司名称并将其显示在控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="9a700-110">In the following example, the company names of customers from London are retrieved and displayed in the console window.</span></span>  
  
 [!code-csharp[DLinqGettingStarted#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqGettingStarted/cs/Program.cs#1)]
 [!code-vb[DLinqGettingStarted#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqGettingStarted/vb/Module1.vb#1)]  
  
## <a name="inserting"></a><span data-ttu-id="9a700-111">插入</span><span class="sxs-lookup"><span data-stu-id="9a700-111">Inserting</span></span>  

 <span data-ttu-id="9a700-112">若要执行 SQL `Insert`，只需向您已创建的对象模型添加对象，然后对 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 调用 <xref:System.Data.Linq.DataContext>即可。</span><span class="sxs-lookup"><span data-stu-id="9a700-112">To execute a SQL `Insert`, just add objects to the object model you have created, and call <xref:System.Data.Linq.DataContext.SubmitChanges%2A> on the <xref:System.Data.Linq.DataContext>.</span></span>  
  
 <span data-ttu-id="9a700-113">在下面的示例中，通过使用 `Customers` 向 <xref:System.Data.Linq.Table%601.InsertOnSubmit%2A>表添加了一位新客户以及有关该客户的信息。</span><span class="sxs-lookup"><span data-stu-id="9a700-113">In the following example, a new customer and information about the customer is added to the `Customers` table by using <xref:System.Data.Linq.Table%601.InsertOnSubmit%2A>.</span></span>  
  
 [!code-csharp[DLinqGettingStarted#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqGettingStarted/cs/Program.cs#2)]
 [!code-vb[DLinqGettingStarted#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqGettingStarted/vb/Module1.vb#2)]  
  
## <a name="updating"></a><span data-ttu-id="9a700-114">更新</span><span class="sxs-lookup"><span data-stu-id="9a700-114">Updating</span></span>  

 <span data-ttu-id="9a700-115">若要 `Update` 某一数据库项，首先要检索该项，然后直接在对象模型中编辑它。</span><span class="sxs-lookup"><span data-stu-id="9a700-115">To `Update` a database entry, first retrieve the item and edit it directly in the object model.</span></span> <span data-ttu-id="9a700-116">在修改了该对象之后，请对 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 调用 <xref:System.Data.Linq.DataContext> 以更新数据库。</span><span class="sxs-lookup"><span data-stu-id="9a700-116">After you have modified the object, call <xref:System.Data.Linq.DataContext.SubmitChanges%2A> on the <xref:System.Data.Linq.DataContext> to update the database.</span></span>  
  
 <span data-ttu-id="9a700-117">在下面的示例中，检索来自伦敦的所有客户。</span><span class="sxs-lookup"><span data-stu-id="9a700-117">In the following example, all customers who are from London are retrieved.</span></span> <span data-ttu-id="9a700-118">然后将其所在城市的名称从“London”更改为“London - Metro”。</span><span class="sxs-lookup"><span data-stu-id="9a700-118">Then the name of the city is changed from "London" to "London - Metro".</span></span> <span data-ttu-id="9a700-119">最后，调用 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 以将所做的更改发送至数据库。</span><span class="sxs-lookup"><span data-stu-id="9a700-119">Finally, <xref:System.Data.Linq.DataContext.SubmitChanges%2A> is called to send the changes to the database.</span></span>  
  
 [!code-csharp[DLinqGettingStarted#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqGettingStarted/cs/Program.cs#3)]
 [!code-vb[DLinqGettingStarted#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqGettingStarted/vb/Module1.vb#3)]  
  
## <a name="deleting"></a><span data-ttu-id="9a700-120">正在删除</span><span class="sxs-lookup"><span data-stu-id="9a700-120">Deleting</span></span>  

 <span data-ttu-id="9a700-121">若要 `Delete` 某一项，请从其所属集合中移除该项，然后对 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 调用 <xref:System.Data.Linq.DataContext> 以提交所做的更改。</span><span class="sxs-lookup"><span data-stu-id="9a700-121">To `Delete` an item, remove the item from the collection to which it belongs, and then call <xref:System.Data.Linq.DataContext.SubmitChanges%2A> on the <xref:System.Data.Linq.DataContext> to commit the change.</span></span>  
  
> [!NOTE]
> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="9a700-122">无法识别级联删除操作。</span><span class="sxs-lookup"><span data-stu-id="9a700-122">does not recognize cascade-delete operations.</span></span> <span data-ttu-id="9a700-123">如果要删除表中具有约束的行，请参阅 [如何：从数据库中删除行](how-to-delete-rows-from-the-database.md)。</span><span class="sxs-lookup"><span data-stu-id="9a700-123">If you want to delete a row in a table that has constraints against it, see [How to: Delete Rows From the Database](how-to-delete-rows-from-the-database.md).</span></span>  
  
 <span data-ttu-id="9a700-124">在下面的示例中，从数据库中检索 `CustomerID` 为 `98128` 的客户。</span><span class="sxs-lookup"><span data-stu-id="9a700-124">In the following example, the customer who has `CustomerID` of `98128` is retrieved from the database.</span></span> <span data-ttu-id="9a700-125">然后，在确认检索到客户行之后，调用 <xref:System.Data.Linq.Table%601.DeleteOnSubmit%2A> 以将该对象从集合中移除。</span><span class="sxs-lookup"><span data-stu-id="9a700-125">Then, after confirming that the customer row was retrieved, <xref:System.Data.Linq.Table%601.DeleteOnSubmit%2A> is called to remove that object from the collection.</span></span> <span data-ttu-id="9a700-126">最后，调用 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 以将删除内容转发至数据库。</span><span class="sxs-lookup"><span data-stu-id="9a700-126">Finally, <xref:System.Data.Linq.DataContext.SubmitChanges%2A> is called to forward the deletion to the database.</span></span>  
  
 [!code-csharp[DLinqGettingStarted#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqGettingStarted/cs/Program.cs#4)]
 [!code-vb[DLinqGettingStarted#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqGettingStarted/vb/Module1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="9a700-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a700-127">See also</span></span>

- [<span data-ttu-id="9a700-128">编程指南</span><span class="sxs-lookup"><span data-stu-id="9a700-128">Programming Guide</span></span>](programming-guide.md)
- [<span data-ttu-id="9a700-129">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="9a700-129">The LINQ to SQL Object Model</span></span>](the-linq-to-sql-object-model.md)
- [<span data-ttu-id="9a700-130">入门</span><span class="sxs-lookup"><span data-stu-id="9a700-130">Getting Started</span></span>](getting-started.md)
