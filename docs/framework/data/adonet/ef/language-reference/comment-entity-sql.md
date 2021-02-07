---
description: '了解详细信息：-- (注释)  (实体 SQL) '
title: --（注释）(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5d9de735-2099-47f1-b7e7-60856f494924
ms.openlocfilehash: 793649177d9e64bead7b8755f35bdb51f53f4dd8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724968"
---
# <a name="---comment-entity-sql"></a><span data-ttu-id="cda5d-103">--（注释）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="cda5d-103">-- (Comment) (Entity SQL)</span></span>

[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="cda5d-104">查询可以包含注释。</span><span class="sxs-lookup"><span data-stu-id="cda5d-104">queries can contain comments.</span></span> <span data-ttu-id="cda5d-105">注释行以两个短划线 (`--`) 开头。</span><span class="sxs-lookup"><span data-stu-id="cda5d-105">Two dashes (`--`) start a comment line.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cda5d-106">语法</span><span class="sxs-lookup"><span data-stu-id="cda5d-106">Syntax</span></span>  
  
```csharp  
-- text_of_comment  
```  
  
## <a name="arguments"></a><span data-ttu-id="cda5d-107">参数</span><span class="sxs-lookup"><span data-stu-id="cda5d-107">Arguments</span></span>  

 `text_of_comment`  
 <span data-ttu-id="cda5d-108">包含注释文本的字符串。</span><span class="sxs-lookup"><span data-stu-id="cda5d-108">Is the character string that contains the text of the comment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cda5d-109">示例</span><span class="sxs-lookup"><span data-stu-id="cda5d-109">Example</span></span>  

 <span data-ttu-id="cda5d-110">下面的 Entity SQL 查询演示如何使用注释。</span><span class="sxs-lookup"><span data-stu-id="cda5d-110">The following Entity SQL query demonstrates how to use comments.</span></span> <span data-ttu-id="cda5d-111">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="cda5d-111">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="cda5d-112">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="cda5d-112">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="cda5d-113">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="cda5d-113">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="cda5d-114">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="cda5d-114">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#COMMENT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#comment)]  
  
## <a name="see-also"></a><span data-ttu-id="cda5d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="cda5d-115">See also</span></span>

- [<span data-ttu-id="cda5d-116">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="cda5d-116">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="cda5d-117">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="cda5d-117">Entity SQL Reference</span></span>](entity-sql-reference.md)
