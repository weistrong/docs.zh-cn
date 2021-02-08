---
description: 了解有关详细信息，请参阅如何：使用 Scalar-Valued User-Defined 函数
title: 如何：使用标量值用户定义的函数
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 714e252f-c053-4bbb-b1f3-924111cd4d97
ms.openlocfilehash: e606dd3f840b8f082928217c6118b48d8d4a2e5c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785805"
---
# <a name="how-to-use-scalar-valued-user-defined-functions"></a>如何：使用标量值用户定义的函数

您可以通过使用 <xref:System.Data.Linq.Mapping.FunctionAttribute> 属性将类中定义的客户端方法映射到用户定义的函数。 请注意，方法体会构造一个捕获方法调用意向的表达式，并将该表达式传递给 <xref:System.Data.Linq.DataContext> 进行转换和执行。  
  
> [!NOTE]
> 只有在查询外部调用此函数时，才会直接执行。 有关详细信息，请参阅 [如何：以内联方式调用 User-Defined 函数](how-to-call-user-defined-functions-inline.md)。  
  
## <a name="example"></a>示例  

 下面的 SQL 代码展示了一个用户定义的标量值函数 `ReverseCustName()`。  
  
```sql  
CREATE FUNCTION ReverseCustName(@string varchar(100))  
RETURNS varchar(100)  
AS  
BEGIN  
    DECLARE @custName varchar(100)  
    -- Implementation left as exercise for users.  
    RETURN @custName  
END  
```  
  
 您可以为此代码映射一个客户端方法，例如，可以映射下面这个方法：  
  
 [!code-csharp[DLinqUDFS#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqUDFS/cs/northwind-tfunc.cs#3)]
 [!code-vb[DLinqUDFS#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqUDFS/vb/northwind-tfunc.vb#3)]  
  
## <a name="see-also"></a>请参阅

- [用户定义函数](user-defined-functions.md)
