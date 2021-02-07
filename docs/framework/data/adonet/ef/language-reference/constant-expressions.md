---
description: 了解详细信息：常量表达式
title: 常量表达式
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9d98a7be-b110-4edb-8eba-bed10f250b6d
ms.openlocfilehash: 3c040918df4af6a0302d2435e3564e395044108e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724825"
---
# <a name="constant-expressions"></a><span data-ttu-id="91492-103">常量表达式</span><span class="sxs-lookup"><span data-stu-id="91492-103">Constant Expressions</span></span>

<span data-ttu-id="91492-104">常量表达式由常量值组成。</span><span class="sxs-lookup"><span data-stu-id="91492-104">A constant expression consists of a constant value.</span></span> <span data-ttu-id="91492-105">常量值被直接转换为常量命令目录树表达式，而无需在客户端进行任何变换。</span><span class="sxs-lookup"><span data-stu-id="91492-105">Constant values are directly converted to constant command tree expressions, without any translation on the client.</span></span> <span data-ttu-id="91492-106">这包括产生常量值的表达式。</span><span class="sxs-lookup"><span data-stu-id="91492-106">This includes expressions that result in a constant value.</span></span> <span data-ttu-id="91492-107">因此，所有涉及常量的表达式都应具有数据源行为。</span><span class="sxs-lookup"><span data-stu-id="91492-107">Therefore, data source behavior should be expected for all expressions involving constants.</span></span> <span data-ttu-id="91492-108">这可能产生与 CLR 行为不同的行为。</span><span class="sxs-lookup"><span data-stu-id="91492-108">This can result in behavior that differs from CLR behavior.</span></span>  
  
 <span data-ttu-id="91492-109">下面的示例说明了一个在服务器上求值的常量表达式。</span><span class="sxs-lookup"><span data-stu-id="91492-109">The following example shows a constant expression that is evaluated on the server.</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#ConstantExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#constantexpression)]
 [!code-vb[DP L2E Conceptual Examples#ConstantExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#constantexpression)]  
  
 <span data-ttu-id="91492-110">LINQ to Entities 不支持将用户类用作常量。</span><span class="sxs-lookup"><span data-stu-id="91492-110">LINQ to Entities does not support using a user class as a constant.</span></span> <span data-ttu-id="91492-111">但是，用户类上的属性引用被视为常量，将转换为命令目录树常量表达式并在数据源上执行。</span><span class="sxs-lookup"><span data-stu-id="91492-111">However, a property reference on a user class is considered a constant, and will be converted to a command tree constant expression and executed on the data source.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91492-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="91492-112">See also</span></span>

- [<span data-ttu-id="91492-113">LINQ to Entities 查询中的表达式</span><span class="sxs-lookup"><span data-stu-id="91492-113">Expressions in LINQ to Entities Queries</span></span>](expressions-in-linq-to-entities-queries.md)
