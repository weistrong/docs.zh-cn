---
description: 了解更多相关信息：如何：通过导航运算符导航关系
title: 如何：使用导航运算符导航关系
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 79996d2d-9b03-4a9d-82cc-7c5e7c2ad93d
ms.openlocfilehash: ff419a959c2ec895a238d37caeedcf1f06812050
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697525"
---
# <a name="how-to-navigate-relationships-with-the-navigate-operator"></a><span data-ttu-id="ca92c-103">如何：使用导航运算符导航关系</span><span class="sxs-lookup"><span data-stu-id="ca92c-103">How to: Navigate Relationships with the Navigate Operator</span></span>

<span data-ttu-id="ca92c-104">本主题演示如何使用 <xref:System.Data.EntityClient.EntityCommand> 对象针对概念模型执行命令，以及如何使用 <xref:System.Data.Metadata.Edm.RefType> 检索 <xref:System.Data.EntityClient.EntityDataReader> 结果。</span><span class="sxs-lookup"><span data-stu-id="ca92c-104">This topic shows how to execute a command against a conceptual model by using an <xref:System.Data.EntityClient.EntityCommand> object, and how to retrieve the <xref:System.Data.Metadata.Edm.RefType> results by using an <xref:System.Data.EntityClient.EntityDataReader>.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="ca92c-105">运行本示例中的代码</span><span class="sxs-lookup"><span data-stu-id="ca92c-105">To run the code in this example</span></span>  
  
1. <span data-ttu-id="ca92c-106">将 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 添加到项目中，并将项目配置为使用实体框架。</span><span class="sxs-lookup"><span data-stu-id="ca92c-106">Add the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) to your project and configure your project to use the Entity Framework.</span></span> <span data-ttu-id="ca92c-107">有关详细信息，请参阅 [如何：使用实体数据模型向导](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="ca92c-107">For more information, see [How to: Use the Entity Data Model Wizard](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span></span>  
  
2. <span data-ttu-id="ca92c-108">在应用程序的代码页中，添加以下 `using` 语句（在 Visual Basic 中为 `Imports`）：</span><span class="sxs-lookup"><span data-stu-id="ca92c-108">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="ca92c-109">示例</span><span class="sxs-lookup"><span data-stu-id="ca92c-109">Example</span></span>  

 <span data-ttu-id="ca92c-110">下面的示例演示如何 [!INCLUDE[esql](../../../../../includes/esql-md.md)] 使用 [定位](./language-reference/navigate-entity-sql.md) 运算符在中导航关系。</span><span class="sxs-lookup"><span data-stu-id="ca92c-110">The following example shows how to navigate relationships in [!INCLUDE[esql](../../../../../includes/esql-md.md)] by using the [NAVIGATE](./language-reference/navigate-entity-sql.md) operator.</span></span> <span data-ttu-id="ca92c-111">`Navigate`运算符采用以下参数：实体的实例、关系类型、关系的结束和关系的开始。</span><span class="sxs-lookup"><span data-stu-id="ca92c-111">The `Navigate` operator takes the following parameters: an instance of an entity, the relationship type, the end of the relationship, and the beginning of the relationship.</span></span> <span data-ttu-id="ca92c-112">或者，您可以仅向运算符传递实体的实例和关系类型 `Navigate` 。</span><span class="sxs-lookup"><span data-stu-id="ca92c-112">Optionally, you can pass only an instance of an entity and the relationship type to the `Navigate` operator.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#NavigateWithNavOperatorWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#navigatewithnavoperatorwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#NavigateWithNavOperatorWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#navigatewithnavoperatorwithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="ca92c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca92c-113">See also</span></span>

- [<span data-ttu-id="ca92c-114">用于实体框架的 EntityClient 提供程序</span><span class="sxs-lookup"><span data-stu-id="ca92c-114">EntityClient Provider for the Entity Framework</span></span>](entityclient-provider-for-the-entity-framework.md)
- [<span data-ttu-id="ca92c-115">Entity SQL 语言</span><span class="sxs-lookup"><span data-stu-id="ca92c-115">Entity SQL Language</span></span>](./language-reference/entity-sql-language.md)
