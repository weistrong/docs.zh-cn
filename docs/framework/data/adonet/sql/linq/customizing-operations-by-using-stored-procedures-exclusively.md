---
description: 了解详细信息：以独占方式使用存储过程自定义操作
title: 通过仅使用存储过程自定义操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 441e8ef3-998c-4d12-8825-ce66a178f90f
ms.openlocfilehash: 4ddcc6b4face1abccb502e12617105a734bb5f0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729544"
---
# <a name="customizing-operations-by-using-stored-procedures-exclusively"></a>通过仅使用存储过程自定义操作

通过仅使用存储过程来访问数据是常见的情况。  
  
## <a name="example"></a>示例  
  
### <a name="description"></a>说明  

 您可以通过 [使用存储过程来修改自定义操作](customizing-operations-by-using-stored-procedures.md) 中提供的示例，方法是使用存储过程来替换第一个查询 (这将导致动态 SQL 执行与包装存储过程的方法调用) 。  
  
 假定 `CustomersByCity` 就是此方法，如下面的示例所示。  
  
### <a name="code"></a>代码  

 [!code-csharp[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/northwind.cs#4)]
 [!code-vb[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/northwind.vb#4)]  
  
 下面的代码不用任何动态 SQL 即可执行。  
  
 [!code-csharp[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/Program.cs#5)]
 [!code-vb[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/Module1.vb#5)]  
  
## <a name="see-also"></a>请参阅

- [开发人员在重写默认行为中的责任](responsibilities-of-the-developer-in-overriding-default-behavior.md)
