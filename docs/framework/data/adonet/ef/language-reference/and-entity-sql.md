---
description: '了解详细信息： &amp; &amp; (和)  (实体 SQL) '
title: '&amp;&amp; (和)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: e7d24213-471d-4807-b85e-570375df89b5
ms.openlocfilehash: 14fc6bc3f58ac78cb9806a7f421db87bbad048ae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697174"
---
# <a name="ampamp-and-entity-sql"></a>&amp;&amp; (和)  (实体 SQL) 

如果两个表达式均为 `true` ，则返回 `true`；否则，返回 `false` 或 `NULL`。  
  
## <a name="syntax"></a>语法  
  
```csharp  
boolean_expression AND boolean_expression
```

or  

```csharp
boolean_expression && boolean_expression  
```  
  
## <a name="arguments"></a>自变量  

 `boolean_expression`  
 返回 Boolean 的任何有效表达式。  
  
## <a name="remarks"></a>备注  

 双“与”符号 (&&) 与 AND 运算符具有相同的功能。  
  
 下表显示可能的输入值和返回类型。  
  
||`TRUE`|`FALSE`|`NULL`|  
|-|------------|-------------|------------|  
|`TRUE`|true|false|Null|  
|`FALSE`|false|false|false|  
|`NULL`|Null|false|Null|  
  
## <a name="example"></a>示例  

 以下 Entity SQL 查询演示如何使用 AND 运算符。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1. 执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。  
  
2. 将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-csharp[DP EntityServices Concepts 2#AND](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#and)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
