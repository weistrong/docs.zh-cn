---
description: '详细了解：收集 (实体 SQL) '
title: COLLECTION (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 03228bfa-be3a-4ccc-82f8-eee429f85cf1
ms.openlocfilehash: 1269680b2a9009277e79337cfe4df154885b7c1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697044"
---
# <a name="collection-entity-sql"></a><span data-ttu-id="74689-103">COLLECTION (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="74689-103">COLLECTION (Entity SQL)</span></span>

<span data-ttu-id="74689-104">COLLECTION 关键字仅在内联函数的定义中使用。</span><span class="sxs-lookup"><span data-stu-id="74689-104">The COLLECTION keyword is only used in the definition of an inline function.</span></span> <span data-ttu-id="74689-105">集合函数是对值的集合进行操作并生成标量输出的函数。</span><span class="sxs-lookup"><span data-stu-id="74689-105">Collection functions are functions that operate on a collection of values and produce a scalar output.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74689-106">语法</span><span class="sxs-lookup"><span data-stu-id="74689-106">Syntax</span></span>  
  
```csharp  
COLLECTION(type_definition)
```  
  
## <a name="arguments"></a><span data-ttu-id="74689-107">参数</span><span class="sxs-lookup"><span data-stu-id="74689-107">Arguments</span></span>  

 `type_definition`  
 <span data-ttu-id="74689-108">一个表达式，返回受支持类型、行或引用的集合。</span><span class="sxs-lookup"><span data-stu-id="74689-108">An expression that returns a collection of supported types, rows, or references.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="74689-109">备注</span><span class="sxs-lookup"><span data-stu-id="74689-109">Remarks</span></span>  

 <span data-ttu-id="74689-110">有关 COLLECTION 关键字的详细信息，请参阅 [Type Definitions](type-definitions-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="74689-110">For more information about the COLLECTION keyword, see [Type Definitions](type-definitions-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="74689-111">示例</span><span class="sxs-lookup"><span data-stu-id="74689-111">Example</span></span>  

 <span data-ttu-id="74689-112">下面的示例演示如何使用 COLLECTION 关键字将十进制值集合声明为内联查询函数的参数。</span><span class="sxs-lookup"><span data-stu-id="74689-112">The following sample shows how to use the COLLECTION keyword to declare a collection of decimals as an argument for an inline query function.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#Collection_GroupPartition](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#collection_grouppartition)]  
  
## <a name="see-also"></a><span data-ttu-id="74689-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="74689-113">See also</span></span>

- [<span data-ttu-id="74689-114">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="74689-114">Entity SQL Reference</span></span>](entity-sql-reference.md)
