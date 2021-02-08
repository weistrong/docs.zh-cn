---
description: 了解详细信息：多个大容量复制操作
title: 多个批量复制操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5ad12f94-7459-4a93-a421-4160d1a90715
ms.openlocfilehash: dfc694cfb4a993889bed607be71821bb1f9fddf1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767656"
---
# <a name="multiple-bulk-copy-operations"></a>多个批量复制操作

可以使用 <xref:System.Data.SqlClient.SqlBulkCopy> 类的单个实例执行多次大容量复制操作。 如果复制之间的操作参数已更改（例如，目标表的名称），必须首先更新它们，之后再对任何 WriteToServer 方法进行任何后续调用，如以下示例所示  。 除非已明确更改，否则将所有属性值保持为与给定实例的较早大容量复制上的属性值相同。  
  
> [!NOTE]
> 与每个操作使用单独实例相比，使用 <xref:System.Data.SqlClient.SqlBulkCopy> 的同一实例执行多次大容量复制操作通常效率更高。  
  
 在使用同一 <xref:System.Data.SqlClient.SqlBulkCopy> 对象执行多次大容量复制操作时，对于每个操作中的源信息或目标信息相同与否没有限制。 但是，必须确保每次写入服务器时正确设置列关联信息。  
  
> [!IMPORTANT]
> 除非已按照 [大容量复制示例设置](bulk-copy-example-setup.md)中所述创建了工作表，否则此示例将不会运行。 提供此代码是为了演示仅使用 SqlBulkCopy 时的语法。 如果源表和目标表位于同一 SQL Server 实例中，可以更便捷地使用 Transact-SQL `INSERT … SELECT` 语句复制数据。  
  
 [!code-csharp[DataWorks SqlBulkCopy.ColumnMappingOrdersDetails#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlBulkCopy.ColumnMappingOrdersDetails/CS/source.cs#1)]
 [!code-vb[DataWorks SqlBulkCopy.ColumnMappingOrdersDetails#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlBulkCopy.ColumnMappingOrdersDetails/VB/source.vb#1)]  
  
## <a name="see-also"></a>请参阅

- [SQL Server 中的大容量复制操作](bulk-copy-operations-in-sql-server.md)
- [ADO.NET 概述](../ado-net-overview.md)
