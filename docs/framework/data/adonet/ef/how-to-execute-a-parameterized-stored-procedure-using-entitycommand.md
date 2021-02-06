---
description: 了解详细信息：如何：使用 EntityCommand 执行参数化存储过程
title: 如何：使用 EntityCommand 执行参数化存储过程
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4f5639bf-bb7f-4982-bb1d-c7caa4348888
ms.openlocfilehash: a45c9a276cc33037a4d353e05d1174c9748aab82
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650685"
---
# <a name="how-to-execute-a-parameterized-stored-procedure-using-entitycommand"></a><span data-ttu-id="66c54-103">如何：使用 EntityCommand 执行参数化存储过程</span><span class="sxs-lookup"><span data-stu-id="66c54-103">How to: Execute a Parameterized Stored Procedure Using EntityCommand</span></span>

<span data-ttu-id="66c54-104">本主题说明如何使用 <xref:System.Data.EntityClient.EntityCommand> 类执行参数化存储过程。</span><span class="sxs-lookup"><span data-stu-id="66c54-104">This topic shows how to execute a parameterized stored procedure by using the <xref:System.Data.EntityClient.EntityCommand> class.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="66c54-105">运行本示例中的代码</span><span class="sxs-lookup"><span data-stu-id="66c54-105">To run the code in this example</span></span>  
  
1. <span data-ttu-id="66c54-106">将 [School 模型](/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)) 添加到项目中，并将项目配置为使用实体框架。</span><span class="sxs-lookup"><span data-stu-id="66c54-106">Add the [School Model](/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)) to your project and configure your project to use the Entity Framework.</span></span> <span data-ttu-id="66c54-107">有关详细信息，请参阅 [如何：使用实体数据模型向导](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="66c54-107">For more information, see [How to: Use the Entity Data Model Wizard](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span></span>  
  
2. <span data-ttu-id="66c54-108">在应用程序的代码页中，添加以下 `using` 语句（在 Visual Basic 中为 `Imports`）：</span><span class="sxs-lookup"><span data-stu-id="66c54-108">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3. <span data-ttu-id="66c54-109">导入 `GetStudentGrades` 存储过程并将 `CourseGrade` 实体指定为返回类型。</span><span class="sxs-lookup"><span data-stu-id="66c54-109">Import the `GetStudentGrades` stored procedure and specify `CourseGrade` entities as a return type.</span></span> <span data-ttu-id="66c54-110">有关如何导入存储过程的信息，请参阅 [如何：导入存储过程](/previous-versions/dotnet/netframework-4.0/bb896231(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="66c54-110">For information on how to import a stored procedure, see [How to: Import a Stored Procedure](/previous-versions/dotnet/netframework-4.0/bb896231(v=vs.100)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="66c54-111">示例</span><span class="sxs-lookup"><span data-stu-id="66c54-111">Example</span></span>  

 <span data-ttu-id="66c54-112">下面的代码执行 `GetStudentGrades` 存储过程，其中，`StudentId` 为必需的参数。</span><span class="sxs-lookup"><span data-stu-id="66c54-112">The following code executes the `GetStudentGrades` stored procedure where `StudentId` is a required parameter.</span></span> <span data-ttu-id="66c54-113">然后由 <xref:System.Data.EntityClient.EntityDataReader> 读取结果。</span><span class="sxs-lookup"><span data-stu-id="66c54-113">The results are then read by an <xref:System.Data.EntityClient.EntityDataReader>.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#StoredProcWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#storedprocwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#StoredProcWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#storedprocwithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="66c54-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="66c54-114">See also</span></span>

- [<span data-ttu-id="66c54-115">用于实体框架的 EntityClient 提供程序</span><span class="sxs-lookup"><span data-stu-id="66c54-115">EntityClient Provider for the Entity Framework</span></span>](entityclient-provider-for-the-entity-framework.md)
