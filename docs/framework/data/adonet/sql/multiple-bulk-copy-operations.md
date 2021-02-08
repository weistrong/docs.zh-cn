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
# <a name="multiple-bulk-copy-operations"></a><span data-ttu-id="43d48-103">多个批量复制操作</span><span class="sxs-lookup"><span data-stu-id="43d48-103">Multiple Bulk Copy Operations</span></span>

<span data-ttu-id="43d48-104">可以使用 <xref:System.Data.SqlClient.SqlBulkCopy> 类的单个实例执行多次大容量复制操作。</span><span class="sxs-lookup"><span data-stu-id="43d48-104">You can perform multiple bulk copy operations using a single instance of a <xref:System.Data.SqlClient.SqlBulkCopy> class.</span></span> <span data-ttu-id="43d48-105">如果复制之间的操作参数已更改（例如，目标表的名称），必须首先更新它们，之后再对任何 WriteToServer 方法进行任何后续调用，如以下示例所示  。</span><span class="sxs-lookup"><span data-stu-id="43d48-105">If the operation parameters change between copies (for example, the name of the destination table), you must update them prior to any subsequent calls to any of the **WriteToServer** methods, as demonstrated in the following example.</span></span> <span data-ttu-id="43d48-106">除非已明确更改，否则将所有属性值保持为与给定实例的较早大容量复制上的属性值相同。</span><span class="sxs-lookup"><span data-stu-id="43d48-106">Unless explicitly changed, all property values remain the same as they were on the previous bulk copy operation for a given instance.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="43d48-107">与每个操作使用单独实例相比，使用 <xref:System.Data.SqlClient.SqlBulkCopy> 的同一实例执行多次大容量复制操作通常效率更高。</span><span class="sxs-lookup"><span data-stu-id="43d48-107">Performing multiple bulk copy operations using the same instance of <xref:System.Data.SqlClient.SqlBulkCopy> is usually more efficient than using a separate instance for each operation.</span></span>  
  
 <span data-ttu-id="43d48-108">在使用同一 <xref:System.Data.SqlClient.SqlBulkCopy> 对象执行多次大容量复制操作时，对于每个操作中的源信息或目标信息相同与否没有限制。</span><span class="sxs-lookup"><span data-stu-id="43d48-108">If you perform several bulk copy operations using the same <xref:System.Data.SqlClient.SqlBulkCopy> object, there are no restrictions on whether source or target information is equal or different in each operation.</span></span> <span data-ttu-id="43d48-109">但是，必须确保每次写入服务器时正确设置列关联信息。</span><span class="sxs-lookup"><span data-stu-id="43d48-109">However, you must ensure that column association information is properly set each time you write to the server.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="43d48-110">除非已按照 [大容量复制示例设置](bulk-copy-example-setup.md)中所述创建了工作表，否则此示例将不会运行。</span><span class="sxs-lookup"><span data-stu-id="43d48-110">This sample will not run unless you have created the work tables as described in [Bulk Copy Example Setup](bulk-copy-example-setup.md).</span></span> <span data-ttu-id="43d48-111">提供此代码是为了演示仅使用 SqlBulkCopy 时的语法。</span><span class="sxs-lookup"><span data-stu-id="43d48-111">This code is provided to demonstrate the syntax for using **SqlBulkCopy** only.</span></span> <span data-ttu-id="43d48-112">如果源表和目标表位于同一 SQL Server 实例中，可以更便捷地使用 Transact-SQL `INSERT … SELECT` 语句复制数据。</span><span class="sxs-lookup"><span data-stu-id="43d48-112">If the source and destination tables are located in the same SQL Server instance, it is easier and faster to use a Transact-SQL `INSERT … SELECT` statement to copy the data.</span></span>  
  
 [!code-csharp[DataWorks SqlBulkCopy.ColumnMappingOrdersDetails#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlBulkCopy.ColumnMappingOrdersDetails/CS/source.cs#1)]
 [!code-vb[DataWorks SqlBulkCopy.ColumnMappingOrdersDetails#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlBulkCopy.ColumnMappingOrdersDetails/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="43d48-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="43d48-113">See also</span></span>

- [<span data-ttu-id="43d48-114">SQL Server 中的大容量复制操作</span><span class="sxs-lookup"><span data-stu-id="43d48-114">Bulk Copy Operations in SQL Server</span></span>](bulk-copy-operations-in-sql-server.md)
- [<span data-ttu-id="43d48-115">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="43d48-115">ADO.NET Overview</span></span>](../ado-net-overview.md)
