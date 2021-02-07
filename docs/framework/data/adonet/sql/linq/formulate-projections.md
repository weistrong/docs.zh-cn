---
description: 了解详细信息：阐明预测
title: 构建投影
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 745742df-0eda-479b-83f8-29bd8a80db96
ms.openlocfilehash: 591bc175426f08aa4273376e4c5efe370d2be756
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672070"
---
# <a name="formulate-projections"></a><span data-ttu-id="57498-103">构建投影</span><span class="sxs-lookup"><span data-stu-id="57498-103">Formulate Projections</span></span>

<span data-ttu-id="57498-104">下面的示例演示了 `select` c # 中的语句和 Visual Basic 中的语句如何 `Select` 与其他功能组合起来以形成查询投影。</span><span class="sxs-lookup"><span data-stu-id="57498-104">The following examples show how the `select` statement in C# and `Select` statement in Visual Basic can be combined with other features to form query projections.</span></span>  
  
## <a name="example"></a><span data-ttu-id="57498-105">示例</span><span class="sxs-lookup"><span data-stu-id="57498-105">Example</span></span>  

 <span data-ttu-id="57498-106">下面的示例使用 `Select` `select` c # ) 中 Visual Basic (子句中的子句来返回的联系人名称序列 `Customers` 。</span><span class="sxs-lookup"><span data-stu-id="57498-106">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) to return a sequence of contact names for `Customers`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#57](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#57)]
 [!code-vb[DLinqQueryExamples#57](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#57)]  
  
## <a name="example"></a><span data-ttu-id="57498-107">示例</span><span class="sxs-lookup"><span data-stu-id="57498-107">Example</span></span>  

 <span data-ttu-id="57498-108">下面的示例使用 `Select` c # 中 Visual Basic (子句中的子句 `select` ) 和 *匿名类型* 返回的联系人姓名和电话号码序列 `Customers` 。</span><span class="sxs-lookup"><span data-stu-id="57498-108">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a sequence of contact names and telephone numbers for `Customers`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#58](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#58)]
 [!code-vb[DLinqQueryExamples#58](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#58)]  
  
## <a name="example"></a><span data-ttu-id="57498-109">示例</span><span class="sxs-lookup"><span data-stu-id="57498-109">Example</span></span>  

 <span data-ttu-id="57498-110">下面的示例使用 `Select` c # 中 Visual Basic (子句中的子句 `select` ) 和 *匿名类型* 返回员工的姓名和电话号码序列。</span><span class="sxs-lookup"><span data-stu-id="57498-110">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a sequence of names and telephone numbers for employees.</span></span> <span data-ttu-id="57498-111">在产生的序列中，`FirstName` 和 `LastName` 字段组合成单个字段 (`Name`)，`HomePhone` 字段重命名为 `Phone`。</span><span class="sxs-lookup"><span data-stu-id="57498-111">The `FirstName` and `LastName` fields are combined into a single field (`Name`), and the `HomePhone` field is renamed to `Phone` in the resulting sequence.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#59](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#59)]
 [!code-vb[DLinqQueryExamples#59](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#59)]  
  
## <a name="example"></a><span data-ttu-id="57498-112">示例</span><span class="sxs-lookup"><span data-stu-id="57498-112">Example</span></span>  

 <span data-ttu-id="57498-113">下面的示例使用 `Select` c # 中 Visual Basic (子句中的子句 `select` ) 和 *匿名类型* 返回一个序列，其中的所有 `ProductID` 和一个名为的计算值 `HalfPrice` 。</span><span class="sxs-lookup"><span data-stu-id="57498-113">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a sequence of all `ProductID`s and a calculated value named `HalfPrice`.</span></span> <span data-ttu-id="57498-114">此值设置为 `UnitPrice` 的 1/2。</span><span class="sxs-lookup"><span data-stu-id="57498-114">This value is set to the `UnitPrice` divided by 2.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#60](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#60)]
 [!code-vb[DLinqQueryExamples#60](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#60)]  
  
## <a name="example"></a><span data-ttu-id="57498-115">示例</span><span class="sxs-lookup"><span data-stu-id="57498-115">Example</span></span>  

 <span data-ttu-id="57498-116">下面的示例使用了 `Select` c # 中 Visual Basic (子句中的子句 `select` ) 和一个 *条件语句* 来返回产品名称和产品可用性的序列。</span><span class="sxs-lookup"><span data-stu-id="57498-116">The following example uses the `Select` clause in Visual Basic (`select` clause in C#) and a *conditional statement* to return a sequence of product name and product availability.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#61](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#61)]
 [!code-vb[DLinqQueryExamples#61](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#61)]  
  
## <a name="example"></a><span data-ttu-id="57498-117">示例</span><span class="sxs-lookup"><span data-stu-id="57498-117">Example</span></span>  

 <span data-ttu-id="57498-118">下面的示例使用 `Select` c # 中的 Visual Basic 子句 (`select` 子句 ) 和 (名称) 的 *已知类型* 返回员工姓名的序列。</span><span class="sxs-lookup"><span data-stu-id="57498-118">The following example uses a Visual Basic `Select` clause (`select` clause in C#) and a *known type* (Name) to return a sequence of the names of employees.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#62](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#62)]
 [!code-vb[DLinqQueryExamples#62](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#62)]  
  
## <a name="example"></a><span data-ttu-id="57498-119">示例</span><span class="sxs-lookup"><span data-stu-id="57498-119">Example</span></span>  

 <span data-ttu-id="57498-120">下面的示例在 `Select` `Where` Visual Basic (`select` 和 c # ) 中使用和， `where` 以返回伦敦的客户的联系人姓名的 *筛选序列* 。</span><span class="sxs-lookup"><span data-stu-id="57498-120">The following example uses `Select` and `Where` in Visual Basic (`select` and `where` in C#) to return a *filtered sequence* of contact names for customers in London.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#63](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#63)]
 [!code-vb[DLinqQueryExamples#63](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#63)]  
  
## <a name="example"></a><span data-ttu-id="57498-121">示例</span><span class="sxs-lookup"><span data-stu-id="57498-121">Example</span></span>  

 <span data-ttu-id="57498-122">下面的示例使用 `Select` c # 中 Visual Basic (子句中的子句 `select` ) 和 *匿名类型* 返回有关客户的数据的 *形状子集* 。</span><span class="sxs-lookup"><span data-stu-id="57498-122">The following example uses a `Select` clause in Visual Basic (`select` clause in C#) and *anonymous types* to return a *shaped subset* of the data about customers.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#64](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#64)]
 [!code-vb[DLinqQueryExamples#64](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#64)]  
  
## <a name="example"></a><span data-ttu-id="57498-123">示例</span><span class="sxs-lookup"><span data-stu-id="57498-123">Example</span></span>  

 <span data-ttu-id="57498-124">下面的示例使用嵌套查询返回以下结果：</span><span class="sxs-lookup"><span data-stu-id="57498-124">The following example uses nested queries to return the following results:</span></span>  
  
- <span data-ttu-id="57498-125">由所有订单及其对应的 `OrderID` 组成的序列。</span><span class="sxs-lookup"><span data-stu-id="57498-125">A sequence of all orders and their corresponding `OrderID`s.</span></span>  
  
- <span data-ttu-id="57498-126">由订单中具有折扣的项组成的子序列。</span><span class="sxs-lookup"><span data-stu-id="57498-126">A subsequence of the items in the order for which there is a discount.</span></span>  
  
- <span data-ttu-id="57498-127">不含运费时节省的资金数额。</span><span class="sxs-lookup"><span data-stu-id="57498-127">The amount of money saved if the cost of shipping is not included.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#65](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#65)]
 [!code-vb[DLinqQueryExamples#65](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#65)]  
  
## <a name="see-also"></a><span data-ttu-id="57498-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="57498-128">See also</span></span>

- [<span data-ttu-id="57498-129">查询示例</span><span class="sxs-lookup"><span data-stu-id="57498-129">Query Examples</span></span>](query-examples.md)
