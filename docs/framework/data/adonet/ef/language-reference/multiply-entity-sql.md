---
description: '详细了解： * (乘法)  (实体 SQL) '
title: '*  (乘)  (实体 SQL) '
ms.date: 03/30/2017
ms.assetid: 508ce246-4e86-47dd-a605-4af4bebb9891
ms.openlocfilehash: 92606e5f9e4646ab651d0e07095e6f419401188f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696615"
---
# <a name="-multiply-entity-sql"></a>*（乘）(Entity SQL)

将两个表达式相乘。  
  
## <a name="syntax"></a>语法  
  
```sql  
expression * expression  
```  
  
## <a name="arguments"></a>参数  

 `expression`  
 任何一种数值数据类型的任何有效表达式。  
  
## <a name="result-types"></a>结果类型  

 对这两个参数进行隐式类型提升而产生的数据类型。 有关隐式类型升级的详细信息，请参阅 [类型系统](type-system-entity-sql.md)。  
  
## <a name="example"></a>示例  

 以下 Entity SQL 查询使用 * 算术运算符将两个数字相乘。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1. 执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。  
  
2. 将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-sql[DP EntityServices Concepts#MULTIPLY](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#multiply)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
