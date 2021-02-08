---
description: '了解详细信息：设置 (实体 SQL) '
title: SET (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 28b4deac-c7e4-4f09-b428-4d352ef2dc94
ms.openlocfilehash: 80be5b76e654c39776d97413c4ece5a8f3df8d2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768020"
---
# <a name="set-entity-sql"></a>SET (Entity SQL)

SET 表达式用于通过生成一个新集合（其中移除了所有重复元素）将对象集合转换为一个集。  
  
## <a name="syntax"></a>语法  
  
```sql  
SET ( expression )  
```  
  
## <a name="arguments"></a>参数  

 `expression`  
 任何返回集合的有效查询表达式。  
  
## <a name="remarks"></a>备注  

 SET 表达式 `SET(c)` 在逻辑上等效于以下 select 语句：  
  
```sql  
SELECT VALUE DISTINCT c FROM c  
```  
  
 `SET` 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。 所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。 有关集运算符 [的优先级信息，请参阅](except-entity-sql.md) [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 。  
  
## <a name="example"></a>示例  

 以下 Entity SQL 查询使用 SET 表达式将一个对象集合转换为一个集。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1. 按照 [如何：执行返回 PrimitiveType 结果的查询](../how-to-execute-a-query-that-returns-primitivetype-results.md)中的过程进行操作。  
  
2. 将以下查询作为参数传递给 `ExecutePrimitiveTypeQuery` 方法：  
  
 [!code-sql[DP EntityServices Concepts#SET](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#set)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
