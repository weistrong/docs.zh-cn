---
description: 了解详细信息： Oracle 分布式事务
title: Oracle 分布式事务
ms.date: 03/30/2017
ms.assetid: c340ca81-ef79-402f-b204-c5156b890fe5
ms.openlocfilehash: d0c41920f18e0f56ebdf57e3cb82cf829a59c450
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786168"
---
# <a name="oracle-distributed-transactions"></a><span data-ttu-id="53671-103">Oracle 分布式事务</span><span class="sxs-lookup"><span data-stu-id="53671-103">Oracle Distributed Transactions</span></span>

<span data-ttu-id="53671-104"><xref:System.Data.OracleClient.OracleConnection> 对象自动在现有分布式事务中登记（如果确定某个事务是活动的）。</span><span class="sxs-lookup"><span data-stu-id="53671-104">The <xref:System.Data.OracleClient.OracleConnection> object automatically enlists in an existing distributed transaction if it determines that a transaction is active.</span></span> <span data-ttu-id="53671-105">如果连接从连接池中打开或检索，将自动登记事务。</span><span class="sxs-lookup"><span data-stu-id="53671-105">Automatic transaction enlistment occurs when the connection is opened or retrieved from the connection pool.</span></span> <span data-ttu-id="53671-106">可以禁用现有事务中的自动登记，方法是将</span><span class="sxs-lookup"><span data-stu-id="53671-106">You can disable auto-enlistment in existing transactions by specifying</span></span>  
  
```csharp  
Enlist=false  
```  
  
 <span data-ttu-id="53671-107">指定为 <xref:System.Data.OracleClient.OracleConnection> 的连接字符串参数。</span><span class="sxs-lookup"><span data-stu-id="53671-107">as a connection string parameter for an <xref:System.Data.OracleClient.OracleConnection>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53671-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="53671-108">See also</span></span>

- [<span data-ttu-id="53671-109">Oracle 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="53671-109">Oracle and ADO.NET</span></span>](oracle-and-adonet.md)
- [<span data-ttu-id="53671-110">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="53671-110">ADO.NET Overview</span></span>](ado-net-overview.md)
