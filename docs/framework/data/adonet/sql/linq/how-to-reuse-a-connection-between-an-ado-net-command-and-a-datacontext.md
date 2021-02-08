---
description: 了解详细信息：如何：在 ADO.NET 命令与 DataContext 之间重复使用连接
title: 如何：重复使用 ADO.NET 命令和 DataContext 之间的连接
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7e26c7eb-c18a-43b5-a8f0-28fd8b04b0f0
ms.openlocfilehash: d5bf45dfd705ed6e9b9d4ed9659e01bfcb539df2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785947"
---
# <a name="how-to-reuse-a-connection-between-an-adonet-command-and-a-datacontext"></a><span data-ttu-id="179fc-103">如何：重复使用 ADO.NET 命令和 DataContext 之间的连接</span><span class="sxs-lookup"><span data-stu-id="179fc-103">How to: Reuse a Connection Between an ADO.NET Command and a DataContext</span></span>

<span data-ttu-id="179fc-104">由于 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 是 ADO.NET 系列技术的一部分，并且基于 ADO.NET 提供的服务，因此你可以重复使用 ADO.NET 命令和之间的连接 <xref:System.Data.Linq.DataContext> 。</span><span class="sxs-lookup"><span data-stu-id="179fc-104">Because [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] is a part of the ADO.NET family of technologies and is based on services provided by ADO.NET, you can reuse a connection between an ADO.NET command and a <xref:System.Data.Linq.DataContext>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="179fc-105">示例</span><span class="sxs-lookup"><span data-stu-id="179fc-105">Example</span></span>  

 <span data-ttu-id="179fc-106">下面的示例演示如何在 ADO.NET 命令和之间重复使用相同的连接 <xref:System.Data.Linq.DataContext> 。</span><span class="sxs-lookup"><span data-stu-id="179fc-106">The following example shows how to reuse the same connection between an ADO.NET command and the <xref:System.Data.Linq.DataContext>.</span></span>  
  
 [!code-csharp[DLinqCommunicatingWithDatabase#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCommunicatingWithDatabase/cs/Program.cs#4)]
 [!code-vb[DLinqCommunicatingWithDatabase#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCommunicatingWithDatabase/vb/Module1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="179fc-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="179fc-107">See also</span></span>

- [<span data-ttu-id="179fc-108">背景信息</span><span class="sxs-lookup"><span data-stu-id="179fc-108">Background Information</span></span>](background-information.md)
- [<span data-ttu-id="179fc-109">ADO.NET 和 LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="179fc-109">ADO.NET and LINQ to SQL</span></span>](ado-net-and-linq-to-sql.md)
- [<span data-ttu-id="179fc-110">与数据库通信</span><span class="sxs-lookup"><span data-stu-id="179fc-110">Communicating with the Database</span></span>](communicating-with-the-database.md)
