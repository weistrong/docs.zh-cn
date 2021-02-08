---
description: '了解详细信息：演练：简单对象模型和查询 (Visual Basic) '
title: 演练：简单对象模型和查询 (Visual Basic)
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: c878e457-f715-46e4-a136-ff14d6c86018
ms.openlocfilehash: def2fecf0d6d97841ebd47a1d675f85341053d39
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791798"
---
# <a name="walkthrough-simple-object-model-and-query-visual-basic"></a><span data-ttu-id="bb4d8-103">演练：简单对象模型和查询 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bb4d8-103">Walkthrough: Simple Object Model and Query (Visual Basic)</span></span>

<span data-ttu-id="bb4d8-104">本演练提供了复杂性最小的基本端对端 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 方案。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-104">This walkthrough provides a fundamental end-to-end [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] scenario with minimal complexities.</span></span> <span data-ttu-id="bb4d8-105">您将创建一个可为示例 Northwind 数据库中的 Customers 表建模的实体类。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-105">You will create an entity class that models the Customers table in the sample Northwind database.</span></span> <span data-ttu-id="bb4d8-106">然后您将创建一个简单查询，用于列出位于伦敦的客户。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-106">You will then create a simple query to list customers who are located in London.</span></span>

<span data-ttu-id="bb4d8-107">本演练在设计上是面向代码的，以帮助说明 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 概念。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-107">This walkthrough is code-oriented by design to help show [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] concepts.</span></span> <span data-ttu-id="bb4d8-108">通常，可以使用对象关系设计器来创建对象模型。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-108">Normally speaking, you would use the Object Relational Designer to create your object model.</span></span>

[!INCLUDE[note_settings_general](../../../../../../includes/note-settings-general-md.md)]

<span data-ttu-id="bb4d8-109">本演练是使用 Visual Basic 开发设置编写的。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-109">This walkthrough was written by using Visual Basic Development Settings.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb4d8-110">先决条件</span><span class="sxs-lookup"><span data-stu-id="bb4d8-110">Prerequisites</span></span>

- <span data-ttu-id="bb4d8-111">本演练使用专用文件夹（“c:\linqtest”）来保存文件。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-111">This walkthrough uses a dedicated folder ("c:\linqtest") to hold files.</span></span> <span data-ttu-id="bb4d8-112">请在开始本演练前创建此文件夹。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-112">Create this folder before you begin the walkthrough.</span></span>

- <span data-ttu-id="bb4d8-113">本演练需要 Northwind 示例数据库。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-113">This walkthrough requires the Northwind sample database.</span></span> <span data-ttu-id="bb4d8-114">如果您的开发计算机上没有此数据库，您可以从 Microsoft 下载网站下载它。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-114">If you do not have this database on your development computer, you can download it from the Microsoft download site.</span></span> <span data-ttu-id="bb4d8-115">有关说明，请参阅 [下载示例数据库](downloading-sample-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-115">For instructions, see [Downloading Sample Databases](downloading-sample-databases.md).</span></span> <span data-ttu-id="bb4d8-116">下载此数据库后，请将文件复制到 c:\linqtest 文件夹。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-116">After you have downloaded the database, copy the file to the c:\linqtest folder.</span></span>

## <a name="overview"></a><span data-ttu-id="bb4d8-117">概述</span><span class="sxs-lookup"><span data-stu-id="bb4d8-117">Overview</span></span>

<span data-ttu-id="bb4d8-118">本演练由六项主要任务组成：</span><span class="sxs-lookup"><span data-stu-id="bb4d8-118">This walkthrough consists of six main tasks:</span></span>

- <span data-ttu-id="bb4d8-119">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]在 Visual Studio 中创建解决方案。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-119">Creating a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] solution in Visual Studio.</span></span>

- <span data-ttu-id="bb4d8-120">将类映射到数据库表。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-120">Mapping a class to a database table.</span></span>

- <span data-ttu-id="bb4d8-121">指定类中的属性表示数据库列。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-121">Designating properties on the class to represent database columns.</span></span>

- <span data-ttu-id="bb4d8-122">指定到 Northwind 数据库的连接。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-122">Specifying the connection to the Northwind database.</span></span>

- <span data-ttu-id="bb4d8-123">创建针对该数据库运行的简单查询。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-123">Creating a simple query to run against the database.</span></span>

- <span data-ttu-id="bb4d8-124">执行查询并观察结果。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-124">Executing the query and observing the results.</span></span>

## <a name="creating-a-linq-to-sql-solution"></a><span data-ttu-id="bb4d8-125">创建 LINQ to SQL 解决方案</span><span class="sxs-lookup"><span data-stu-id="bb4d8-125">Creating a LINQ to SQL Solution</span></span>

<span data-ttu-id="bb4d8-126">在第一个任务中，您将创建一个 Visual Studio 解决方案，其中包含生成和运行项目所必需的引用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-126">In this first task, you create a Visual Studio solution that contains the necessary references to build and run a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] project.</span></span>

### <a name="to-create-a-linq-to-sql-solution"></a><span data-ttu-id="bb4d8-127">创建 LINQ to SQL 解决方案</span><span class="sxs-lookup"><span data-stu-id="bb4d8-127">To create a LINQ to SQL solution</span></span>

1. <span data-ttu-id="bb4d8-128">在“文件”菜单上，单击“新建项目”。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-128">On the **File** menu, click **New Project**.</span></span>

2. <span data-ttu-id="bb4d8-129">在 "**新建项目**" 对话框的 "**项目类型**" 窗格中，单击 " **Visual Basic**"。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-129">In the **Project types** pane of the **New Project** dialog box, click **Visual Basic**.</span></span>

3. <span data-ttu-id="bb4d8-130">在“模板”窗格中，单击“控制台应用程序”。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-130">In the **Templates** pane, click **Console Application**.</span></span>

4. <span data-ttu-id="bb4d8-131">在 " **名称** " 框中，键入 **LinqConsoleApp**。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-131">In the **Name** box, type **LinqConsoleApp**.</span></span>

5. <span data-ttu-id="bb4d8-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-132">Click **OK**.</span></span>

## <a name="adding-linq-references-and-directives"></a><span data-ttu-id="bb4d8-133">添加 LINQ 引用和指令</span><span class="sxs-lookup"><span data-stu-id="bb4d8-133">Adding LINQ References and Directives</span></span>

<span data-ttu-id="bb4d8-134">本演练用到默认情况下您的项目中可能未安装的程序集。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-134">This walkthrough uses assemblies that might not be installed by default in your project.</span></span> <span data-ttu-id="bb4d8-135">如果 `System.Data.Linq` 未在你的项目中列为引用 (请单击 "显示 **解决方案资源管理器** 中的 **所有文件**"，然后展开 "**引用**" 节点) "添加"，如以下步骤中所述。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-135">If `System.Data.Linq` is not listed as a reference in your project (click **Show All Files** in **Solution Explorer** and expand the **References** node), add it, as explained in the following steps.</span></span>

### <a name="to-add-systemdatalinq"></a><span data-ttu-id="bb4d8-136">添加 System.Data.Linq</span><span class="sxs-lookup"><span data-stu-id="bb4d8-136">To add System.Data.Linq</span></span>

1. <span data-ttu-id="bb4d8-137">在 **解决方案资源管理器** 中，右键单击 " **引用**"，然后单击 " **添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-137">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>

2. <span data-ttu-id="bb4d8-138">在 " **添加引用** " 对话框中，单击 " **.net**"，单击 "system.web" 程序集，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-138">In the **Add Reference** dialog box, click **.NET**, click the System.Data.Linq assembly, and then click **OK**.</span></span>

     <span data-ttu-id="bb4d8-139">此程序集即被添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-139">The assembly is added to the project.</span></span>

3. <span data-ttu-id="bb4d8-140">同样，在 " **添加引用** " 对话框中，单击 " **.net**"，滚动到 "system.web"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-140">Also in the **Add Reference** dialog box, click **.NET**, scroll to and click System.Windows.Forms, and then click **OK**.</span></span>

     <span data-ttu-id="bb4d8-141">此程序集（支持本演练中的消息框）即被添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-141">This assembly, which supports the message box in the walkthrough, is added to the project.</span></span>

4. <span data-ttu-id="bb4d8-142">在 `Module1` 上方添加以下指令：</span><span class="sxs-lookup"><span data-stu-id="bb4d8-142">Add the following directives above `Module1`:</span></span>

     [!code-vb[DLinqWalk1VB#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqWalk1VB/vb/Module1.vb#1)]

## <a name="mapping-a-class-to-a-database-table"></a><span data-ttu-id="bb4d8-143">将类映射到数据库表</span><span class="sxs-lookup"><span data-stu-id="bb4d8-143">Mapping a Class to a Database Table</span></span>

<span data-ttu-id="bb4d8-144">在此步骤中，您将创建一个类，并将其映射到数据库表。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-144">In this step, you create a class and map it to a database table.</span></span> <span data-ttu-id="bb4d8-145">这类类称为 *实体类*。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-145">Such a class is termed an *entity class*.</span></span> <span data-ttu-id="bb4d8-146">请注意，只需添加 <xref:System.Data.Linq.Mapping.TableAttribute> 属性即可完成映射。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-146">Note that the mapping is accomplished by just adding the <xref:System.Data.Linq.Mapping.TableAttribute> attribute.</span></span> <span data-ttu-id="bb4d8-147"><xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> 属性指定数据库中的表的名称。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-147">The <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> property specifies the name of the table in the database.</span></span>

### <a name="to-create-an-entity-class-and-map-it-to-a-database-table"></a><span data-ttu-id="bb4d8-148">创建一个实体类并将其映射到数据库表</span><span class="sxs-lookup"><span data-stu-id="bb4d8-148">To create an entity class and map it to a database table</span></span>

- <span data-ttu-id="bb4d8-149">将下面的代码键入或粘贴到 `Sub Main` 上方紧靠它的 Module1.vb 中。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-149">Type or paste the following code into Module1.vb immediately above `Sub Main`:</span></span>

     [!code-vb[DLinqWalk1VB#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqWalk1VB/vb/Module1.vb#2)]

## <a name="designating-properties-on-the-class-to-represent-database-columns"></a><span data-ttu-id="bb4d8-150">指定类中的属性表示数据库列</span><span class="sxs-lookup"><span data-stu-id="bb4d8-150">Designating Properties on the Class to Represent Database Columns</span></span>

<span data-ttu-id="bb4d8-151">在此步骤中，你要完成几项任务。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-151">In this step, you accomplish several tasks.</span></span>

- <span data-ttu-id="bb4d8-152">您要使用 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute) 指定实体类中的 `CustomerID` 和 `City` 属性 (Property) 表示数据库表中的列。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-152">You use the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to designate `CustomerID` and `City` properties on the entity class as representing columns in the database table.</span></span>

- <span data-ttu-id="bb4d8-153">您要指定 `CustomerID` 属性表示数据库中的主键列。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-153">You designate the `CustomerID` property as representing a primary key column in the database.</span></span>

- <span data-ttu-id="bb4d8-154">您要指定 `_CustomerID` 和 `_City` 字段用作私有存储字段。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-154">You designate `_CustomerID` and `_City` fields for private storage.</span></span> <span data-ttu-id="bb4d8-155">然后，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 就可以直接存储和检索值，而不用使用可能包含业务逻辑的公共访问器。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-155">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] can then store and retrieve values directly, instead of using public accessors that might include business logic.</span></span>

### <a name="to-represent-characteristics-of-two-database-columns"></a><span data-ttu-id="bb4d8-156">表示两个数据库列的特性</span><span class="sxs-lookup"><span data-stu-id="bb4d8-156">To represent characteristics of two database columns</span></span>

- <span data-ttu-id="bb4d8-157">将下面的代码键入或粘贴到 `End Class` 前面紧靠它的 Module1.vb 中。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-157">Type or paste the following code into Module1.vb just before `End Class`:</span></span>

     [!code-vb[DLinqWalk1VB#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqWalk1VB/vb/Module1.vb#3)]

## <a name="specifying-the-connection-to-the-northwind-database"></a><span data-ttu-id="bb4d8-158">指定到 Northwind 数据库的连接</span><span class="sxs-lookup"><span data-stu-id="bb4d8-158">Specifying the Connection to the Northwind Database</span></span>

<span data-ttu-id="bb4d8-159">在此步骤中，要使用 <xref:System.Data.Linq.DataContext> 对象在你基于代码的数据结构和数据库本身之间建立连接。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-159">In this step you use a <xref:System.Data.Linq.DataContext> object to establish a connection between your code-based data structures and the database itself.</span></span> <span data-ttu-id="bb4d8-160"><xref:System.Data.Linq.DataContext> 是您从数据库中检索对象和提交更改的主要通道。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-160">The <xref:System.Data.Linq.DataContext> is the main channel through which you retrieve objects from the database and submit changes.</span></span>

<span data-ttu-id="bb4d8-161">您还需声明 `Table(Of Customer)`，用作您针对数据库中 Customers 表的查询的逻辑、类型化表。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-161">You also declare a `Table(Of Customer)` to act as the logical, typed table for your queries against the Customers table in the database.</span></span> <span data-ttu-id="bb4d8-162">您将在后续步骤中创建和执行这些查询。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-162">You will create and execute these queries in later steps.</span></span>

### <a name="to-specify-the-database-connection"></a><span data-ttu-id="bb4d8-163">指定数据库连接</span><span class="sxs-lookup"><span data-stu-id="bb4d8-163">To specify the database connection</span></span>

- <span data-ttu-id="bb4d8-164">将下面的代码键入或粘贴到 `Sub Main` 方法中。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-164">Type or paste the following code into the `Sub Main` method.</span></span>

     <span data-ttu-id="bb4d8-165">请注意，假定 `northwnd.mdf` 文件位于 linqtest 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-165">Note that the `northwnd.mdf` file is assumed to be in the linqtest folder.</span></span> <span data-ttu-id="bb4d8-166">有关更多信息，请参见本演练前面部分的“先决条件”一节。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-166">For more information, see the Prerequisites section earlier in this walkthrough.</span></span>

     [!code-vb[DLinqWalk1VB#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqWalk1VB/vb/Module1.vb#4)]

## <a name="creating-a-simple-query"></a><span data-ttu-id="bb4d8-167">创建简单查询</span><span class="sxs-lookup"><span data-stu-id="bb4d8-167">Creating a Simple Query</span></span>

<span data-ttu-id="bb4d8-168">在此步骤中，您将创建一个查询，查找数据库中的 Customers 表内的哪些客户位于伦敦。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-168">In this step, you create a query to find which customers in the database Customers table are located in London.</span></span> <span data-ttu-id="bb4d8-169">此步骤中的查询代码只描述查询。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-169">The query code in this step just describes the query.</span></span> <span data-ttu-id="bb4d8-170">它不执行查询。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-170">It does not execute it.</span></span> <span data-ttu-id="bb4d8-171">此方法称为 " *延迟执行*"。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-171">This approach is known as *deferred execution*.</span></span> <span data-ttu-id="bb4d8-172">有关详细信息，请参阅 [LINQ 查询简介 (C#)](../../../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-172">For more information, see [Introduction to LINQ Queries (C#)](../../../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).</span></span>

<span data-ttu-id="bb4d8-173">您还将生成一个日志输出，显示 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 生成的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-173">You will also produce a log output to show the SQL commands that [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] generates.</span></span> <span data-ttu-id="bb4d8-174">此日志记录功能（使用 <xref:System.Data.Linq.DataContext.Log%2A>）对调试有帮助，并有助于确定发送给数据库的命令是否准确地表示您的查询。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-174">This logging feature (which uses <xref:System.Data.Linq.DataContext.Log%2A>) is helpful in debugging, and in determining that the commands being sent to the database accurately represent your query.</span></span>

### <a name="to-create-a-simple-query"></a><span data-ttu-id="bb4d8-175">创建简单查询</span><span class="sxs-lookup"><span data-stu-id="bb4d8-175">To create a simple query</span></span>

- <span data-ttu-id="bb4d8-176">将下面的代码键入或粘贴到 `Sub Main` 声明之后的 `Table(Of Customer)` 方法中：</span><span class="sxs-lookup"><span data-stu-id="bb4d8-176">Type or paste the following code into the `Sub Main` method after the `Table(Of Customer)` declaration:</span></span>

     [!code-vb[DLinqWalk1AVB#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqWalk1AVB/vb/Module1.vb#5)]

## <a name="executing-the-query"></a><span data-ttu-id="bb4d8-177">执行查询</span><span class="sxs-lookup"><span data-stu-id="bb4d8-177">Executing the Query</span></span>

<span data-ttu-id="bb4d8-178">在此步骤中，您将实际执行查询。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-178">In this step, you actually execute the query.</span></span> <span data-ttu-id="bb4d8-179">您在前面步骤中创建的查询表达式只有在需要结果时才会进行计算。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-179">The query expressions you created in the previous steps are not evaluated until the results are needed.</span></span> <span data-ttu-id="bb4d8-180">当您开始 `For Each` 迭代时，将对数据库执行 SQL 命令，并将对象具体化。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-180">When you begin the `For Each` iteration, a SQL command is executed against the database and objects are materialized.</span></span>

### <a name="to-execute-the-query"></a><span data-ttu-id="bb4d8-181">执行查询</span><span class="sxs-lookup"><span data-stu-id="bb4d8-181">To execute the query</span></span>

1. <span data-ttu-id="bb4d8-182">将下面的代码键入或粘贴到 `Sub Main` 方法的结尾（在查询说明之后）：</span><span class="sxs-lookup"><span data-stu-id="bb4d8-182">Type or paste the following code at the end of the `Sub Main` method (after the query description):</span></span>

     [!code-vb[DLinqWalk1AVB#6](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqWalk1AVB/vb/Module1.vb#6)]

2. <span data-ttu-id="bb4d8-183">按 F5 调试该应用程序。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-183">Press F5 to debug the application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb4d8-184">如果你的应用程序产生运行时错误，请参阅 [通过演练学习](learning-by-walkthroughs.md)的疑难解答部分。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-184">If your application generates a run-time error, see the Troubleshooting section of [Learning by Walkthroughs](learning-by-walkthroughs.md).</span></span>

     <span data-ttu-id="bb4d8-185">消息框会显示一个包含六个客户的列表。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-185">The message box displays a list of six customers.</span></span> <span data-ttu-id="bb4d8-186">控制台窗口会显示生成的 SQL 代码。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-186">The Console window displays the generated SQL code.</span></span>

3. <span data-ttu-id="bb4d8-187">单击“确定”，关闭该消息框。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-187">Click **OK** to dismiss the message box.</span></span>

     <span data-ttu-id="bb4d8-188">应用程序即会关闭。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-188">The application closes.</span></span>

4. <span data-ttu-id="bb4d8-189">在“文件”菜单上，单击“全部保存”。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-189">On the **File** menu, click **Save All**.</span></span>

     <span data-ttu-id="bb4d8-190">如果您要继续下一演练，您将需要此应用程序。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-190">You will need this application if you continue with the next walkthrough.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb4d8-191">后续步骤</span><span class="sxs-lookup"><span data-stu-id="bb4d8-191">Next Steps</span></span>

<span data-ttu-id="bb4d8-192">[演练：跨关系查询 (Visual Basic) ](walkthrough-querying-across-relationships-visual-basic.md)主题将继续本演练结束的位置。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-192">The [Walkthrough: Querying Across Relationships (Visual Basic)](walkthrough-querying-across-relationships-visual-basic.md) topic continues where this walkthrough ends.</span></span> <span data-ttu-id="bb4d8-193">"跨关系进行查询" 演练演示如何 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 跨表进行查询，这类似于关系数据库中的 *联接* 。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-193">The Querying Across Relationships walkthrough demonstrates how [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] can query across tables, similar to *joins* in a relational database.</span></span>

<span data-ttu-id="bb4d8-194">如果您希望进行“跨关系进行查询”演练，请务必保存您刚完成的演练的解决方案，这是一项必备条件。</span><span class="sxs-lookup"><span data-stu-id="bb4d8-194">If you want to do the Querying Across Relationships walkthrough, make sure to save the solution for the walkthrough you have just completed, which is a prerequisite.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb4d8-195">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb4d8-195">See also</span></span>

- [<span data-ttu-id="bb4d8-196">通过演练学习</span><span class="sxs-lookup"><span data-stu-id="bb4d8-196">Learning by Walkthroughs</span></span>](learning-by-walkthroughs.md)
