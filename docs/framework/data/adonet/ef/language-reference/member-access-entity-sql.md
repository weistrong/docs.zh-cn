---
description: 了解详细信息：。 （成员访问）(Entity SQL)
title: . （成员访问）(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4733e3b2-3efa-4b96-b591-ac31350e96ad
ms.openlocfilehash: 94833d3525c7d17cadaef15065b3dcbdb43a6ded
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739373"
---
# <a name="-member-access-entity-sql"></a>. （成员访问）(Entity SQL)

点运算符 (。 ) 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 成员访问运算符。 使用成员访问运算符可生成结构化概念模型类型实例的属性或字段的值。  
  
## <a name="syntax"></a>语法  
  
```sql  
expression.identifier  
```  
  
## <a name="arguments"></a>参数  

 `expression`  
 结构化概念模型类型的实例。  
  
 `identifier`  
 属于对象实例的属性或字段。  
  
## <a name="remarks"></a>备注  

 点 (.) 运算符可以用于从记录中提取字段，类似于提取复杂类型或实体类型的属性。 例如，如果类型 Name 的 n 是类型 Person 的成员，而 p 是类型 Person 的实例，则 p.n 是合法的成员访问表达式，该表达式生成类型为 Name 的值。  
  
 `select p.Name.FirstName from LOB.Person as p`  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
