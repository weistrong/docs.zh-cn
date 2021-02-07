---
description: 了解详细信息：以独占方式使用存储过程自定义操作
title: 通过仅使用存储过程自定义操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 441e8ef3-998c-4d12-8825-ce66a178f90f
ms.openlocfilehash: 4ddcc6b4face1abccb502e12617105a734bb5f0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729544"
---
# <a name="customizing-operations-by-using-stored-procedures-exclusively"></a><span data-ttu-id="5570e-103">通过仅使用存储过程自定义操作</span><span class="sxs-lookup"><span data-stu-id="5570e-103">Customizing Operations by Using Stored Procedures Exclusively</span></span>

<span data-ttu-id="5570e-104">通过仅使用存储过程来访问数据是常见的情况。</span><span class="sxs-lookup"><span data-stu-id="5570e-104">Access to data by using only stored procedures is a common scenario.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5570e-105">示例</span><span class="sxs-lookup"><span data-stu-id="5570e-105">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="5570e-106">说明</span><span class="sxs-lookup"><span data-stu-id="5570e-106">Description</span></span>  

 <span data-ttu-id="5570e-107">您可以通过 [使用存储过程来修改自定义操作](customizing-operations-by-using-stored-procedures.md) 中提供的示例，方法是使用存储过程来替换第一个查询 (这将导致动态 SQL 执行与包装存储过程的方法调用) 。</span><span class="sxs-lookup"><span data-stu-id="5570e-107">You can modify the example provided in [Customizing Operations By Using Stored Procedures](customizing-operations-by-using-stored-procedures.md) by replacing even the first query (which causes dynamic SQL execution) with a method call that wraps a stored procedure.</span></span>  
  
 <span data-ttu-id="5570e-108">假定 `CustomersByCity` 就是此方法，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="5570e-108">Assume `CustomersByCity` is the method, as in the following example.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5570e-109">代码</span><span class="sxs-lookup"><span data-stu-id="5570e-109">Code</span></span>  

 [!code-csharp[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/northwind.cs#4)]
 [!code-vb[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/northwind.vb#4)]  
  
 <span data-ttu-id="5570e-110">下面的代码不用任何动态 SQL 即可执行。</span><span class="sxs-lookup"><span data-stu-id="5570e-110">The following code executes without any dynamic SQL.</span></span>  
  
 [!code-csharp[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/Program.cs#5)]
 [!code-vb[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/Module1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="5570e-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="5570e-111">See also</span></span>

- [<span data-ttu-id="5570e-112">开发人员在重写默认行为中的责任</span><span class="sxs-lookup"><span data-stu-id="5570e-112">Responsibilities of the Developer In Overriding Default Behavior</span></span>](responsibilities-of-the-developer-in-overriding-default-behavior.md)
