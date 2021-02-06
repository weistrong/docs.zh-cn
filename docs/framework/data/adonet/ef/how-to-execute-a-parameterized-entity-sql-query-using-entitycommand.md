---
description: 了解有关详细信息，请参阅如何：使用 EntityCommand 执行参数化实体 SQL 查询
title: 如何：使用 EntityCommand 执行参数化实体 SQL 查询
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e93fea43-7e03-4d7d-9fee-2517b8b88cba
ms.openlocfilehash: c3eb9fdfbad986d54104e94aa719a57edfa14b19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650776"
---
# <a name="how-to-execute-a-parameterized-entity-sql-query-using-entitycommand"></a><span data-ttu-id="752de-103">如何：使用 EntityCommand 执行参数化实体 SQL 查询</span><span class="sxs-lookup"><span data-stu-id="752de-103">How to: Execute a Parameterized Entity SQL Query Using EntityCommand</span></span>

<span data-ttu-id="752de-104">本主题说明如何 [!INCLUDE[esql](../../../../../includes/esql-md.md)] 使用对象执行具有参数的查询 <xref:System.Data.EntityClient.EntityCommand> 。</span><span class="sxs-lookup"><span data-stu-id="752de-104">This topic shows how to execute an [!INCLUDE[esql](../../../../../includes/esql-md.md)] query that has parameters by using an <xref:System.Data.EntityClient.EntityCommand> object.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="752de-105">运行本示例中的代码</span><span class="sxs-lookup"><span data-stu-id="752de-105">To run the code in this example</span></span>  
  
1. <span data-ttu-id="752de-106">将 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 添加到项目中，并将项目配置为使用实体框架。</span><span class="sxs-lookup"><span data-stu-id="752de-106">Add the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) to your project and configure your project to use the Entity Framework.</span></span> <span data-ttu-id="752de-107">有关详细信息，请参阅 [如何：使用实体数据模型向导](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="752de-107">For more information, see [How to: Use the Entity Data Model Wizard](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span></span>  
  
2. <span data-ttu-id="752de-108">在应用程序的代码页中，添加以下 `using` 语句（在 Visual Basic 中为 `Imports`）：</span><span class="sxs-lookup"><span data-stu-id="752de-108">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="752de-109">示例</span><span class="sxs-lookup"><span data-stu-id="752de-109">Example</span></span>  

 <span data-ttu-id="752de-110">以下示例显示如何使用两个参数构造一个查询字符串。</span><span class="sxs-lookup"><span data-stu-id="752de-110">The following example shows how to construct a query string with two parameters.</span></span> <span data-ttu-id="752de-111">然后，它创建 <xref:System.Data.EntityClient.EntityCommand>，将两个参数添加到该 <xref:System.Data.EntityClient.EntityParameter> 的 <xref:System.Data.EntityClient.EntityCommand> 集合，并循环访问 `Contact` 项的集合。</span><span class="sxs-lookup"><span data-stu-id="752de-111">It then creates an <xref:System.Data.EntityClient.EntityCommand>, adds two parameters to the <xref:System.Data.EntityClient.EntityParameter> collection of that <xref:System.Data.EntityClient.EntityCommand>, and iterates through the collection of `Contact` items.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#parameterizedquerywithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#parameterizedquerywithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="752de-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="752de-112">See also</span></span>

- <span data-ttu-id="752de-113">[如何：执行参数化查询](/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="752de-113">[How to: Execute a Parameterized Query](/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))</span></span>
- [<span data-ttu-id="752de-114">Entity SQL 语言</span><span class="sxs-lookup"><span data-stu-id="752de-114">Entity SQL Language</span></span>](./language-reference/entity-sql-language.md)
