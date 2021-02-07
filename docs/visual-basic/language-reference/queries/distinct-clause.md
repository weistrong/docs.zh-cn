---
description: '了解详细信息： Distinct 子句 (Visual Basic) '
title: Distinct 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryDistinct
helpviewer_keywords:
- Distinct clause [Visual Basic]
- Distinct statement [Visual Basic]
- queries [Visual Basic], Distinct
ms.assetid: 86f42614-0d8f-4ffc-b888-ce8a37a8d36a
ms.openlocfilehash: df1cdc58f7af406533e67a396a958a26b0c79635
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700645"
---
# <a name="distinct-clause-visual-basic"></a><span data-ttu-id="38cce-103">Distinct 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="38cce-103">Distinct Clause (Visual Basic)</span></span>

<span data-ttu-id="38cce-104">限制当前范围变量的值，以消除后面的查询子句中的重复值。</span><span class="sxs-lookup"><span data-stu-id="38cce-104">Restricts the values of the current range variable to eliminate duplicate values in subsequent query clauses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38cce-105">语法</span><span class="sxs-lookup"><span data-stu-id="38cce-105">Syntax</span></span>  
  
```vb  
Distinct  
```  
  
## <a name="remarks"></a><span data-ttu-id="38cce-106">备注</span><span class="sxs-lookup"><span data-stu-id="38cce-106">Remarks</span></span>  

 <span data-ttu-id="38cce-107">您可以使用 `Distinct` 子句返回唯一项的列表。</span><span class="sxs-lookup"><span data-stu-id="38cce-107">You can use the `Distinct` clause to return a list of unique items.</span></span> <span data-ttu-id="38cce-108">`Distinct`子句使查询忽略重复的查询结果。</span><span class="sxs-lookup"><span data-stu-id="38cce-108">The `Distinct` clause causes the query to ignore duplicate query results.</span></span> <span data-ttu-id="38cce-109">`Distinct`子句适用于子句指定的所有返回字段的重复值 `Select` 。</span><span class="sxs-lookup"><span data-stu-id="38cce-109">The `Distinct` clause applies to duplicate values for all return fields specified by the `Select` clause.</span></span> <span data-ttu-id="38cce-110">如果未 `Select` 指定子句，则将 `Distinct` 子句应用于子句中标识的查询的范围变量 `From` 。</span><span class="sxs-lookup"><span data-stu-id="38cce-110">If no `Select` clause is specified, the `Distinct` clause is applied to the range variable for the query identified in the `From` clause.</span></span> <span data-ttu-id="38cce-111">如果范围变量不是不可变类型，则当该类型的所有成员均与现有查询结果匹配时，该查询将忽略查询结果。</span><span class="sxs-lookup"><span data-stu-id="38cce-111">If the range variable is not an immutable type, the query will only ignore a query result if all members of the type match an existing query result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="38cce-112">示例</span><span class="sxs-lookup"><span data-stu-id="38cce-112">Example</span></span>  

 <span data-ttu-id="38cce-113">下面的查询表达式将联接列表和客户订单列表。</span><span class="sxs-lookup"><span data-stu-id="38cce-113">The following query expression joins a list of customers and a list of customer orders.</span></span> <span data-ttu-id="38cce-114">`Distinct`包含子句是为了返回唯一客户名称和订单日期的列表。</span><span class="sxs-lookup"><span data-stu-id="38cce-114">The `Distinct` clause is included to return a list of unique customer names and order dates.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#20)]  
  
## <a name="see-also"></a><span data-ttu-id="38cce-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="38cce-115">See also</span></span>

- [<span data-ttu-id="38cce-116">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="38cce-116">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="38cce-117">查询</span><span class="sxs-lookup"><span data-stu-id="38cce-117">Queries</span></span>](index.md)
- [<span data-ttu-id="38cce-118">From 子句</span><span class="sxs-lookup"><span data-stu-id="38cce-118">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="38cce-119">Select 子句</span><span class="sxs-lookup"><span data-stu-id="38cce-119">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="38cce-120">Where 子句</span><span class="sxs-lookup"><span data-stu-id="38cce-120">Where Clause</span></span>](where-clause.md)
