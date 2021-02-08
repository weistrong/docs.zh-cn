---
description: '了解详细信息： >= (大于或等于)  (实体 SQL) '
title: '>=（大于或等于）(Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 70780ac4-0123-4da8-b731-8af856daffe3
ms.openlocfilehash: d05685123e3262a2d2ae01553c7c5334a7e53c40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786272"
---
# <a name="-greater-than-or-equal-to-entity-sql"></a>>= (大于或等于)  (实体 SQL) 

比较两个表达式以确定左侧表达式的值是否大于或等于右侧表达式的值。  
  
## <a name="syntax"></a>语法  
  
```sql  
expression >= expression  
```  
  
## <a name="arguments"></a>参数  

 `expression`  
 任何有效的表达式。 两个表达式都必须包含可隐式转换的数据类型。  
  
## <a name="result-types"></a>结果类型  

 如果左侧表达式的值大于或等于右侧表达式的值，则为`true` ；否则为 `false`。  
  
## <a name="example"></a>示例  

 下面的 Entity SQL 查询使用 >= 比较运算符比较两个表达式，以确定左侧表达式的值是否大于或等于右侧表达式的值。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1. 执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。  
  
2. 将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-sql[DP EntityServices Concepts#GREATER_OR_EQUALS](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#greater_or_equals)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
