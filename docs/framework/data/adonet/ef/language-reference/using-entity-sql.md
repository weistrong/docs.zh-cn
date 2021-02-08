---
description: '了解详细信息：使用 (实体 SQL) '
title: USING (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 20f58b8f-6070-4456-b7e8-5ff3d6269273
ms.openlocfilehash: 084ab56f25041377dd6a0a35dd743122f482eeba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795048"
---
# <a name="using-entity-sql"></a><span data-ttu-id="b766e-103">USING (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="b766e-103">USING (Entity SQL)</span></span>

<span data-ttu-id="b766e-104">指定查询表达式中使用的命名空间。</span><span class="sxs-lookup"><span data-stu-id="b766e-104">Specifies namespaces used in a query expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b766e-105">语法</span><span class="sxs-lookup"><span data-stu-id="b766e-105">Syntax</span></span>  
  
```sql  
USING [ alias = ] namespace  
```  
  
## <a name="arguments"></a><span data-ttu-id="b766e-106">参数</span><span class="sxs-lookup"><span data-stu-id="b766e-106">Arguments</span></span>  

 `alias`  
 <span data-ttu-id="b766e-107">指定用于限定命名空间的较短别名。</span><span class="sxs-lookup"><span data-stu-id="b766e-107">Specifies a shorter alias to qualify a namespace with.</span></span>  
  
 `namespace`  
 <span data-ttu-id="b766e-108">任何有效的命名空间。</span><span class="sxs-lookup"><span data-stu-id="b766e-108">Any valid namespace.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b766e-109">示例</span><span class="sxs-lookup"><span data-stu-id="b766e-109">Example</span></span>  

 <span data-ttu-id="b766e-110">以下 Entity SQL 查询使用 USING 运算符以指定查询表达式中使用的命名空间。</span><span class="sxs-lookup"><span data-stu-id="b766e-110">The following Entity SQL query uses the USING operator to specify namespaces used in a query expression.</span></span> <span data-ttu-id="b766e-111">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="b766e-111">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="b766e-112">按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。</span><span class="sxs-lookup"><span data-stu-id="b766e-112">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2. <span data-ttu-id="b766e-113">将以下查询作为参数传递给 `ExecutePrimitiveTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="b766e-113">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
```csharp
using SqlServer; RAND()  
```  
  
## <a name="see-also"></a><span data-ttu-id="b766e-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="b766e-114">See also</span></span>

- [<span data-ttu-id="b766e-115">命名空间</span><span class="sxs-lookup"><span data-stu-id="b766e-115">Namespaces</span></span>](namespaces-entity-sql.md)
- [<span data-ttu-id="b766e-116">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="b766e-116">Entity SQL Reference</span></span>](entity-sql-reference.md)
