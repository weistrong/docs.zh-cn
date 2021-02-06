---
description: 了解详细信息：如何：执行多态查询
title: 如何：执行多态查询
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2f05da1e-845b-4f14-83e4-c6353a850553
ms.openlocfilehash: 02074fb0ad60e5ba8d62094e25f35db40f8a2dbb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650724"
---
# <a name="how-to-execute-a-polymorphic-query"></a><span data-ttu-id="70d5f-103">如何：执行多态查询</span><span class="sxs-lookup"><span data-stu-id="70d5f-103">How to: Execute a Polymorphic Query</span></span>

<span data-ttu-id="70d5f-104">本主题说明如何 [!INCLUDE[esql](../../../../../includes/esql-md.md)] 使用 [OFTYPE](./language-reference/oftype-entity-sql.md) 运算符执行多态查询。</span><span class="sxs-lookup"><span data-stu-id="70d5f-104">This topic shows how to execute a polymorphic [!INCLUDE[esql](../../../../../includes/esql-md.md)] query using the [OFTYPE](./language-reference/oftype-entity-sql.md) operator.</span></span>

### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="70d5f-105">运行本示例中的代码</span><span class="sxs-lookup"><span data-stu-id="70d5f-105">To run the code in this example</span></span>

1. <span data-ttu-id="70d5f-106">将 [School 模型](/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)) 添加到项目中，并将项目配置为使用实体框架。</span><span class="sxs-lookup"><span data-stu-id="70d5f-106">Add the [School Model](/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)) to your project and configure your project to use the Entity Framework.</span></span> <span data-ttu-id="70d5f-107">有关详细信息，请参阅 [如何：使用实体数据模型向导](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="70d5f-107">For more information, see [How to: Use the Entity Data Model Wizard](/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span></span>

2. <span data-ttu-id="70d5f-108">在应用程序的代码页中，添加以下 `using` 语句（在 Visual Basic 中为 `Imports`）：</span><span class="sxs-lookup"><span data-stu-id="70d5f-108">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>

    [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
    [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]

3. <span data-ttu-id="70d5f-109">按照 [演练：映射继承-每个层次结构一个表](/previous-versions/dotnet/netframework-4.0/cc716683(v=vs.100))中的步骤修改概念模型，使其具有每个层次结构一个表继承。</span><span class="sxs-lookup"><span data-stu-id="70d5f-109">Modify the conceptual model to have a table-per-hierarchy inheritance by following the steps in [Walkthrough: Mapping Inheritance - Table-per-Hierarchy](/previous-versions/dotnet/netframework-4.0/cc716683(v=vs.100)).</span></span>

## <a name="example"></a><span data-ttu-id="70d5f-110">示例</span><span class="sxs-lookup"><span data-stu-id="70d5f-110">Example</span></span>

<span data-ttu-id="70d5f-111">下面的示例使用 OFTYPE 运算符从 `OnsiteCourses` 的集合中获取和显示仅包含 `Courses` 的集合。</span><span class="sxs-lookup"><span data-stu-id="70d5f-111">The following example uses an OFTYPE operator to get and display a collection of only `OnsiteCourses` from a collection of `Courses`.</span></span>

[!code-csharp[DP EntityServices Concepts#PolymorphicQuery](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#polymorphicquery)]
[!code-vb[DP EntityServices Concepts#PolymorphicQuery](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#polymorphicquery)]

## <a name="see-also"></a><span data-ttu-id="70d5f-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="70d5f-112">See also</span></span>

- [<span data-ttu-id="70d5f-113">用于实体框架的 EntityClient 提供程序</span><span class="sxs-lookup"><span data-stu-id="70d5f-113">EntityClient Provider for the Entity Framework</span></span>](entityclient-provider-for-the-entity-framework.md)
- [<span data-ttu-id="70d5f-114">Entity SQL 语言</span><span class="sxs-lookup"><span data-stu-id="70d5f-114">Entity SQL Language</span></span>](./language-reference/entity-sql-language.md)
