---
description: '了解详细信息： > (大于)  (实体 SQL) '
title: '> （大于）(Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 4cea865c-677c-4b06-99a1-010f2ae2394a
ms.openlocfilehash: e14470d477336fd719bb419657af3fdadcd54d98
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786285"
---
# <a name="-greater-than-entity-sql"></a>> (大于)  (实体 SQL) 

比较两个表达式以确定左侧表达式的值是否大于右侧表达式的值。  
  
## <a name="syntax"></a>语法  
  
```sql  
expression > expression  
```  
  
## <a name="arguments"></a>参数  

 `expression`  
 任何有效的表达式。 两个表达式都必须包含可隐式转换的数据类型。  
  
## <a name="result-types"></a>结果类型  

 如果左侧表达式的值大于右侧表达式的值，则为`true` ；否则为 `false`。  
  
## <a name="example"></a>示例  

 下面的 Entity SQL 查询使用 > 比较运算符比较两个表达式，以确定左侧表达式的值是否大于右侧表达式的值。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1. 执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。  
  
2. 将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-sql[DP EntityServices Concepts#GREATER](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#greater)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
