---
description: 了解详细信息： CLR 存储过程
title: CLR 存储过程
ms.date: 03/30/2017
ms.assetid: fd7eea9b-218a-4988-8c9a-8abcc6031c66
ms.openlocfilehash: d136d3dcb12be2f87276a410c9fa0e713b7dfd52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723616"
---
# <a name="clr-stored-procedures"></a><span data-ttu-id="3ae19-103">CLR 存储过程</span><span class="sxs-lookup"><span data-stu-id="3ae19-103">CLR Stored Procedures</span></span>

<span data-ttu-id="3ae19-104">存储过程是不能用于标量表达式的例程。</span><span class="sxs-lookup"><span data-stu-id="3ae19-104">Stored procedures are routines that cannot be used in scalar expressions.</span></span> <span data-ttu-id="3ae19-105">它们可以将表格形式的结果和消息返回到客户端，调用数据定义语言 (DDL) 和数据操作语言 (DML) 语句，以及返回输出参数。</span><span class="sxs-lookup"><span data-stu-id="3ae19-105">They can return tabular results and messages to the client, invoke data definition language (DDL) and data manipulation language (DML) statements, and return output parameters.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3ae19-106">Microsoft Visual Basic 不支持采用与 Microsoft Visual C# 中相同的方式处理输出参数。</span><span class="sxs-lookup"><span data-stu-id="3ae19-106">Microsoft Visual Basic does not support output parameters in the same way that Microsoft Visual C# does.</span></span> <span data-ttu-id="3ae19-107">您必须指定以通过引用传递参数并应用 \<Out()> 属性以表示输出参数，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3ae19-107">You must specify to pass the parameter by reference and apply the \<Out()> attribute to represent an output parameter, as in the following:</span></span>  
  
```vb
Public Shared Sub ExecuteToClient( <Out()> ByRef number As Integer)  
```
  
<span data-ttu-id="3ae19-108">有关更多详细信息，请参阅所使用 SQL Server 版本的 [SQL Server 文档](/sql) 版本。</span><span class="sxs-lookup"><span data-stu-id="3ae19-108">For more detailed information, see the version of [SQL Server documentation](/sql) for the version of SQL Server you're using.</span></span>
  
 <span data-ttu-id="3ae19-109">**SQL Server 文档**</span><span class="sxs-lookup"><span data-stu-id="3ae19-109">**SQL Server documentation**</span></span>

1. <span data-ttu-id="3ae19-110">[CLR 存储过程](/previous-versions/sql/sql-server-2008/ms131094(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="3ae19-110">[CLR Stored Procedures](/previous-versions/sql/sql-server-2008/ms131094(v=sql.100))</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ae19-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="3ae19-111">See also</span></span>

- <span data-ttu-id="3ae19-112">[在托管代码中创建 SQL Server 2005 对象](/previous-versions/visualstudio/visual-studio-2008/6s0s2at1(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="3ae19-112">[Creating SQL Server 2005 Objects In Managed Code](/previous-versions/visualstudio/visual-studio-2008/6s0s2at1(v=vs.90))</span></span>
- [<span data-ttu-id="3ae19-113">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="3ae19-113">ADO.NET Overview</span></span>](../ado-net-overview.md)
