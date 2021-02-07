---
description: 了解详细信息：如何：使用为顺序结果形状映射的存储过程
title: 如何：使用针对顺序结果形状映射的存储过程
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a73530de-5a4e-4d9c-8d66-abb19c225b11
ms.openlocfilehash: 3b5791875a7beb5a0c702e787e775cd528ab2517
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738762"
---
# <a name="how-to-use-stored-procedures-mapped-for-sequential-result-shapes"></a><span data-ttu-id="e0689-103">如何：使用针对顺序结果形状映射的存储过程</span><span class="sxs-lookup"><span data-stu-id="e0689-103">How to: Use Stored Procedures Mapped for Sequential Result Shapes</span></span>

<span data-ttu-id="e0689-104">这种存储过程可以生成多个结果形状，但您知道结果的返回顺序。</span><span class="sxs-lookup"><span data-stu-id="e0689-104">This kind of stored procedure can generate more than one result shape, but you know in what order the results are returned.</span></span> <span data-ttu-id="e0689-105">请将此方案与您不知道返回顺序的方案作一个对比。</span><span class="sxs-lookup"><span data-stu-id="e0689-105">Contrast this scenario with the scenario where you do not know the sequence of the returns.</span></span> <span data-ttu-id="e0689-106">有关详细信息，请参阅 [如何：使用为多个结果形状映射的存储过程](how-to-use-stored-procedures-mapped-for-multiple-result-shapes.md)。</span><span class="sxs-lookup"><span data-stu-id="e0689-106">For more information, see [How to: Use Stored Procedures Mapped for Multiple Result Shapes](how-to-use-stored-procedures-mapped-for-multiple-result-shapes.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e0689-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0689-107">Example</span></span>  

 <span data-ttu-id="e0689-108">下面是一个按顺序返回多个结果形状的存储过程的 T-SQL。</span><span class="sxs-lookup"><span data-stu-id="e0689-108">Here is the T-SQL of a stored procedure that returns multiple result shapes sequentially:</span></span>  
  
```sql
CREATE PROCEDURE MultipleResultTypesSequentially  
AS  
select * from products  
select * from customers  
```  
  
 [!code-csharp[DLinqSprox#6](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/northwind-sprox.cs#6)]
 [!code-vb[DLinqSprox#6](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/northwind-sprox.vb#6)]  
  
## <a name="example"></a><span data-ttu-id="e0689-109">示例</span><span class="sxs-lookup"><span data-stu-id="e0689-109">Example</span></span>  

 <span data-ttu-id="e0689-110">你将使用类似于以下内容的代码来执行此存储过程。</span><span class="sxs-lookup"><span data-stu-id="e0689-110">You would use code similar to the following to execute this stored procedure.</span></span>  
  
 [!code-csharp[DLinqSprox#7](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/Program.cs#7)]
 [!code-vb[DLinqSprox#7](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/Module1.vb#7)]  
  
## <a name="see-also"></a><span data-ttu-id="e0689-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="e0689-111">See also</span></span>

- [<span data-ttu-id="e0689-112">存储过程</span><span class="sxs-lookup"><span data-stu-id="e0689-112">Stored Procedures</span></span>](stored-procedures.md)
