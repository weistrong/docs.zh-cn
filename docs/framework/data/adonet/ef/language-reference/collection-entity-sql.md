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
# <a name="collection-entity-sql"></a>COLLECTION (Entity SQL)

COLLECTION 关键字仅在内联函数的定义中使用。 集合函数是对值的集合进行操作并生成标量输出的函数。  
  
## <a name="syntax"></a>语法  
  
```csharp  
COLLECTION(type_definition)
```  
  
## <a name="arguments"></a>参数  

 `type_definition`  
 一个表达式，返回受支持类型、行或引用的集合。  
  
## <a name="remarks"></a>备注  

 有关 COLLECTION 关键字的详细信息，请参阅 [Type Definitions](type-definitions-entity-sql.md)。  
  
## <a name="example"></a>示例  

 下面的示例演示如何使用 COLLECTION 关键字将十进制值集合声明为内联查询函数的参数。  
  
 [!code-csharp[DP EntityServices Concepts 2#Collection_GroupPartition](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#collection_grouppartition)]  
  
## <a name="see-also"></a>请参阅

- [实体 SQL 引用](entity-sql-reference.md)
