---
description: '了解详细信息：演练：操作数据 (c # ) '
title: 演练：操作数据 (C#)
ms.date: 03/30/2017
ms.assetid: 24adfbe0-0ad6-449f-997d-8808e0770d2e
ms.openlocfilehash: 6176709a2e02d8c06ec54b70cc6e0e4c302509c3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729583"
---
# <a name="walkthrough-manipulating-data-c"></a><span data-ttu-id="34b1f-103">演练：操作数据 (C#)</span><span class="sxs-lookup"><span data-stu-id="34b1f-103">Walkthrough: Manipulating Data (C#)</span></span>

<span data-ttu-id="34b1f-104">本演练提供了用于在数据库中添加、修改和删除数据的基本端对端 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 方案。</span><span class="sxs-lookup"><span data-stu-id="34b1f-104">This walkthrough provides a fundamental end-to-end [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] scenario for adding, modifying, and deleting data in a database.</span></span> <span data-ttu-id="34b1f-105">您将使用 Northwind 示例数据库的一个副本来添加一位客户，更改该客户的姓名，然后删除一个订单。</span><span class="sxs-lookup"><span data-stu-id="34b1f-105">You will use a copy of the sample Northwind database to add a customer, change the name of a customer, and delete an order.</span></span>  
  
 [!INCLUDE[note_settings_general](../../../../../../includes/note-settings-general-md.md)]  
  
 <span data-ttu-id="34b1f-106">本演练是使用 Visual C# 开发设置编写的。</span><span class="sxs-lookup"><span data-stu-id="34b1f-106">This walkthrough was written by using Visual C# Development Settings.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="34b1f-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="34b1f-107">Prerequisites</span></span>  

 <span data-ttu-id="34b1f-108">本演练需要如下内容：</span><span class="sxs-lookup"><span data-stu-id="34b1f-108">This walkthrough requires the following:</span></span>  
  
- <span data-ttu-id="34b1f-109">本演练使用专用文件夹（“c:\linqtest6”）来保存文件。</span><span class="sxs-lookup"><span data-stu-id="34b1f-109">This walkthrough uses a dedicated folder ("c:\linqtest6") to hold files.</span></span> <span data-ttu-id="34b1f-110">请在开始本演练前创建此文件夹。</span><span class="sxs-lookup"><span data-stu-id="34b1f-110">Create this folder before you begin the walkthrough.</span></span>  
  
- <span data-ttu-id="34b1f-111">Northwind 示例数据库。</span><span class="sxs-lookup"><span data-stu-id="34b1f-111">The Northwind sample database.</span></span>  
  
     <span data-ttu-id="34b1f-112">如果您的开发计算机上没有此数据库，您可以从 Microsoft 下载网站下载它。</span><span class="sxs-lookup"><span data-stu-id="34b1f-112">If you do not have this database on your development computer, you can download it from the Microsoft download site.</span></span> <span data-ttu-id="34b1f-113">有关说明，请参阅 [下载示例数据库](downloading-sample-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="34b1f-113">For instructions, see [Downloading Sample Databases](downloading-sample-databases.md).</span></span> <span data-ttu-id="34b1f-114">下载此数据库后，请将 northwnd.mdf 文件复制到 c:\linqtest6 文件夹。</span><span class="sxs-lookup"><span data-stu-id="34b1f-114">After you have downloaded the database, copy the northwnd.mdf file to the c:\linqtest6 folder.</span></span>  
  
- <span data-ttu-id="34b1f-115">从 Northwind 数据库生成的 C# 代码文件。</span><span class="sxs-lookup"><span data-stu-id="34b1f-115">A C# code file generated from the Northwind database.</span></span>  
  
     <span data-ttu-id="34b1f-116">您可以使用对象关系设计器或 SQLMetal 工具生成此文件。</span><span class="sxs-lookup"><span data-stu-id="34b1f-116">You can generate this file by using either the Object Relational Designer or the SQLMetal tool.</span></span> <span data-ttu-id="34b1f-117">本演练是通过使用 SQLMetal 工具以及如下命令行编写的：</span><span class="sxs-lookup"><span data-stu-id="34b1f-117">This walkthrough was written by using the SQLMetal tool with the following command line:</span></span>  
  
     <span data-ttu-id="34b1f-118">**sqlmetal/code： "c:\linqtest6\northwind.cs"/language： csharp "C:\linqtest6\northwnd.mdf"/pluralize**</span><span class="sxs-lookup"><span data-stu-id="34b1f-118">**sqlmetal /code:"c:\linqtest6\northwind.cs" /language:csharp "C:\linqtest6\northwnd.mdf" /pluralize**</span></span>  
  
     <span data-ttu-id="34b1f-119">有关详细信息，请参阅 [SqlMetal.exe（代码生成工具）](../../../../tools/sqlmetal-exe-code-generation-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="34b1f-119">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
## <a name="overview"></a><span data-ttu-id="34b1f-120">概述</span><span class="sxs-lookup"><span data-stu-id="34b1f-120">Overview</span></span>  

 <span data-ttu-id="34b1f-121">本演练由六项主要任务组成：</span><span class="sxs-lookup"><span data-stu-id="34b1f-121">This walkthrough consists of six main tasks:</span></span>  
  
- <span data-ttu-id="34b1f-122">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]在 Visual Studio 中创建解决方案。</span><span class="sxs-lookup"><span data-stu-id="34b1f-122">Creating the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] solution in Visual Studio.</span></span>  
  
- <span data-ttu-id="34b1f-123">向项目添加数据库代码文件。</span><span class="sxs-lookup"><span data-stu-id="34b1f-123">Adding the database code file to the project.</span></span>  
  
- <span data-ttu-id="34b1f-124">创建新的客户对象。</span><span class="sxs-lookup"><span data-stu-id="34b1f-124">Creating a new customer object.</span></span>  
  
- <span data-ttu-id="34b1f-125">修改客户的联系人姓名。</span><span class="sxs-lookup"><span data-stu-id="34b1f-125">Modifying the contact name of a customer.</span></span>  
  
- <span data-ttu-id="34b1f-126">删除订单。</span><span class="sxs-lookup"><span data-stu-id="34b1f-126">Deleting an order.</span></span>  
  
- <span data-ttu-id="34b1f-127">将这些更改提交至 Northwind 数据库。</span><span class="sxs-lookup"><span data-stu-id="34b1f-127">Submitting these changes to the Northwind database.</span></span>  
  
## <a name="creating-a-linq-to-sql-solution"></a><span data-ttu-id="34b1f-128">创建 LINQ to SQL 解决方案</span><span class="sxs-lookup"><span data-stu-id="34b1f-128">Creating a LINQ to SQL Solution</span></span>  

 <span data-ttu-id="34b1f-129">在第一个任务中，您将创建一个 Visual Studio 解决方案，其中包含生成和运行项目所必需的引用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="34b1f-129">In this first task, you create a Visual Studio solution that contains the necessary references to build and run a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] project.</span></span>  
  
#### <a name="to-create-a-linq-to-sql-solution"></a><span data-ttu-id="34b1f-130">创建 LINQ to SQL 解决方案</span><span class="sxs-lookup"><span data-stu-id="34b1f-130">To create a LINQ to SQL solution</span></span>  
  
1. <span data-ttu-id="34b1f-131">在 Visual Studio 的 " **文件** " 菜单上，指向 " **新建**"，然后单击 " **项目**"。</span><span class="sxs-lookup"><span data-stu-id="34b1f-131">On the Visual Studio **File** menu, point to **New**, and then click **Project**.</span></span>  
  
2. <span data-ttu-id="34b1f-132">在 "**新建项目**" 对话框的 "**项目类型**" 窗格中，单击 " **Visual c #**"。</span><span class="sxs-lookup"><span data-stu-id="34b1f-132">In the **Project types** pane in the **New Project** dialog box, click **Visual C#**.</span></span>  
  
3. <span data-ttu-id="34b1f-133">在“模板”窗格中，单击“控制台应用程序”。</span><span class="sxs-lookup"><span data-stu-id="34b1f-133">In the **Templates** pane, click **Console Application**.</span></span>  
  
4. <span data-ttu-id="34b1f-134">在 " **名称** " 框中，键入 **LinqDataManipulationApp**。</span><span class="sxs-lookup"><span data-stu-id="34b1f-134">In the **Name** box, type **LinqDataManipulationApp**.</span></span>  
  
5. <span data-ttu-id="34b1f-135">在 " **位置** " 框中，验证要存储项目文件的位置。</span><span class="sxs-lookup"><span data-stu-id="34b1f-135">In the **Location** box, verify where you want to store your project files.</span></span>  
  
6. <span data-ttu-id="34b1f-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="34b1f-136">Click **OK**.</span></span>  
  
## <a name="adding-linq-references-and-directives"></a><span data-ttu-id="34b1f-137">添加 LINQ 引用和指令</span><span class="sxs-lookup"><span data-stu-id="34b1f-137">Adding LINQ References and Directives</span></span>  

 <span data-ttu-id="34b1f-138">本演练用到默认情况下您的项目中可能未安装的程序集。</span><span class="sxs-lookup"><span data-stu-id="34b1f-138">This walkthrough uses assemblies that might not be installed by default in your project.</span></span> <span data-ttu-id="34b1f-139">如果在您的项目中未将 System.Data.Linq 作为引用列出，请按照以下步骤中的说明添加它。</span><span class="sxs-lookup"><span data-stu-id="34b1f-139">If System.Data.Linq is not listed as a reference in your project, add it, as explained in the following steps:</span></span>  
  
#### <a name="to-add-systemdatalinq"></a><span data-ttu-id="34b1f-140">添加 System.Data.Linq</span><span class="sxs-lookup"><span data-stu-id="34b1f-140">To add System.Data.Linq</span></span>  
  
1. <span data-ttu-id="34b1f-141">在 **解决方案资源管理器** 中，右键单击 " **引用**"，然后单击 " **添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="34b1f-141">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>  
  
2. <span data-ttu-id="34b1f-142">在 " **添加引用** " 对话框中，单击 " **.net**"，单击 "system.web" 程序集，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="34b1f-142">In the **Add Reference** dialog box, click **.NET**, click the System.Data.Linq assembly, and then click **OK**.</span></span>  
  
     <span data-ttu-id="34b1f-143">此程序集即被添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="34b1f-143">The assembly is added to the project.</span></span>  
  
3. <span data-ttu-id="34b1f-144">在 Program.cs 的顶部添加以下指令：</span><span class="sxs-lookup"><span data-stu-id="34b1f-144">Add the following directives at the top of Program.cs:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#1)]  
  
## <a name="adding-the-northwind-code-file-to-the-project"></a><span data-ttu-id="34b1f-145">将 Northwind 代码文件添加到项目</span><span class="sxs-lookup"><span data-stu-id="34b1f-145">Adding the Northwind Code File to the Project</span></span>  

 <span data-ttu-id="34b1f-146">以下这些步骤假定你已使用 SQLMetal 工具从 Northwind 示例数据库生成代码文件。</span><span class="sxs-lookup"><span data-stu-id="34b1f-146">These steps assume that you have used the SQLMetal tool to generate a code file from the Northwind sample database.</span></span> <span data-ttu-id="34b1f-147">有关更多信息，请参见本演练前面部分的“先决条件”一节。</span><span class="sxs-lookup"><span data-stu-id="34b1f-147">For more information, see the Prerequisites section earlier in this walkthrough.</span></span>  
  
#### <a name="to-add-the-northwind-code-file-to-the-project"></a><span data-ttu-id="34b1f-148">将 northwind 代码文件添加到项目</span><span class="sxs-lookup"><span data-stu-id="34b1f-148">To add the northwind code file to the project</span></span>  
  
1. <span data-ttu-id="34b1f-149">在“项目”菜单上，单击“添加现有项”。</span><span class="sxs-lookup"><span data-stu-id="34b1f-149">On the **Project** menu, click **Add Existing Item**.</span></span>  
  
2. <span data-ttu-id="34b1f-150">在 " **添加现有项** " 对话框中，导航到 "c:\linqtest6\northwind.cs"，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="34b1f-150">In the **Add Existing Item** dialog box, navigate to c:\linqtest6\northwind.cs, and then click **Add**.</span></span>  
  
     <span data-ttu-id="34b1f-151">northwind.cs 文件即被添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="34b1f-151">The northwind.cs file is added to the project.</span></span>  
  
## <a name="setting-up-the-database-connection"></a><span data-ttu-id="34b1f-152">设置数据库连接</span><span class="sxs-lookup"><span data-stu-id="34b1f-152">Setting Up the Database Connection</span></span>  

 <span data-ttu-id="34b1f-153">首先，测试与数据库的连接。</span><span class="sxs-lookup"><span data-stu-id="34b1f-153">First, test your connection to the database.</span></span> <span data-ttu-id="34b1f-154">特别要注意，数据库 Northwnd 不含 i 字符。</span><span class="sxs-lookup"><span data-stu-id="34b1f-154">Note especially that the database, Northwnd, has no i character.</span></span> <span data-ttu-id="34b1f-155">如果在后面的步骤中产生错误，请检查 northwind.cs 文件以确定 Northwind 分部类的拼法。</span><span class="sxs-lookup"><span data-stu-id="34b1f-155">If you generate errors in the next steps, review the northwind.cs file to determine how the Northwind partial class is spelled.</span></span>  
  
#### <a name="to-set-up-and-test-the-database-connection"></a><span data-ttu-id="34b1f-156">设置并测试数据库连接</span><span class="sxs-lookup"><span data-stu-id="34b1f-156">To set up and test the database connection</span></span>  
  
1. <span data-ttu-id="34b1f-157">将下面的代码键入或粘贴到 Program 类的 `Main` 方法中：</span><span class="sxs-lookup"><span data-stu-id="34b1f-157">Type or paste the following code into the `Main` method in the Program class:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#2)]  
  
2. <span data-ttu-id="34b1f-158">按 F5 在此点测试应用程序。</span><span class="sxs-lookup"><span data-stu-id="34b1f-158">Press F5 to test the application at this point.</span></span>  
  
     <span data-ttu-id="34b1f-159">此时将打开一个 **控制台** 窗口。</span><span class="sxs-lookup"><span data-stu-id="34b1f-159">A **Console** window opens.</span></span>  
  
     <span data-ttu-id="34b1f-160">可以通过在 **控制台** 窗口中按 enter，或在 Visual Studio 的 "**调试**" 菜单上单击 "**停止调试**" 来关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="34b1f-160">You can close the application by pressing Enter in the **Console** window, or by clicking **Stop Debugging** on the Visual Studio **Debug** menu.</span></span>  
  
## <a name="creating-a-new-entity"></a><span data-ttu-id="34b1f-161">创建新实体</span><span class="sxs-lookup"><span data-stu-id="34b1f-161">Creating a New Entity</span></span>  

 <span data-ttu-id="34b1f-162">创建新实体很简单。</span><span class="sxs-lookup"><span data-stu-id="34b1f-162">Creating a new entity is straightforward.</span></span> <span data-ttu-id="34b1f-163">可以使用 `Customer` 关键字创建对象（如 `new`）。</span><span class="sxs-lookup"><span data-stu-id="34b1f-163">You can create objects (such as `Customer`) by using the `new` keyword.</span></span>  
  
 <span data-ttu-id="34b1f-164">在本节及后续各节中，您将只对本地缓存进行更改。</span><span class="sxs-lookup"><span data-stu-id="34b1f-164">In this and the following sections, you are making changes only to the local cache.</span></span> <span data-ttu-id="34b1f-165">如果您不调用 <xref:System.Data.Linq.DataContext.SubmitChanges%2A>，则不会向数据库发送任何更改，一直到本演练结束都是如此。</span><span class="sxs-lookup"><span data-stu-id="34b1f-165">No changes are sent to the database until you call <xref:System.Data.Linq.DataContext.SubmitChanges%2A> toward the end of this walkthrough.</span></span>  
  
#### <a name="to-add-a-new-customer-entity-object"></a><span data-ttu-id="34b1f-166">添加新的 Customer 实体对象</span><span class="sxs-lookup"><span data-stu-id="34b1f-166">To add a new Customer entity object</span></span>  
  
1. <span data-ttu-id="34b1f-167">通过在 `Customer` 方法中的 `Console.ReadLine();` 前添加如下代码，创建一个新的 `Main`：</span><span class="sxs-lookup"><span data-stu-id="34b1f-167">Create a new `Customer` by adding the following code before `Console.ReadLine();` in the `Main` method:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#3)]  
  
2. <span data-ttu-id="34b1f-168">按 F5 调试解决方案。</span><span class="sxs-lookup"><span data-stu-id="34b1f-168">Press F5 to debug the solution.</span></span>  
  
3. <span data-ttu-id="34b1f-169">在 **控制台** 窗口中按 enter 以停止调试并继续演练。</span><span class="sxs-lookup"><span data-stu-id="34b1f-169">Press Enter in the **Console** window to stop debugging and continue the walkthrough.</span></span>  
  
## <a name="updating-an-entity"></a><span data-ttu-id="34b1f-170">更新实体</span><span class="sxs-lookup"><span data-stu-id="34b1f-170">Updating an Entity</span></span>  

 <span data-ttu-id="34b1f-171">在以下步骤中，您将检索一个 `Customer` 对象并修改其属性之一。</span><span class="sxs-lookup"><span data-stu-id="34b1f-171">In the following steps, you will retrieve a `Customer` object and modify one of its properties.</span></span>  
  
#### <a name="to-change-the-name-of-a-customer"></a><span data-ttu-id="34b1f-172">更改客户的姓名</span><span class="sxs-lookup"><span data-stu-id="34b1f-172">To change the name of a Customer</span></span>  
  
- <span data-ttu-id="34b1f-173">将下面的代码添加到 `Console.ReadLine();` 上方：</span><span class="sxs-lookup"><span data-stu-id="34b1f-173">Add the following code above `Console.ReadLine();`:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#4)]  
  
## <a name="deleting-an-entity"></a><span data-ttu-id="34b1f-174">删除实体</span><span class="sxs-lookup"><span data-stu-id="34b1f-174">Deleting an Entity</span></span>  

 <span data-ttu-id="34b1f-175">使用同一客户对象，您可以删除第一个订单。</span><span class="sxs-lookup"><span data-stu-id="34b1f-175">Using the same customer object, you can delete the first order.</span></span>  
  
 <span data-ttu-id="34b1f-176">下面的代码演示如何切断行与行之间的关系，以及如何从数据库中删除行。</span><span class="sxs-lookup"><span data-stu-id="34b1f-176">The following code demonstrates how to sever relationships between rows, and how to delete a row from the database.</span></span> <span data-ttu-id="34b1f-177">请将下面的代码添加到 `Console.ReadLine` 前面，以了解如何可以删除对象：</span><span class="sxs-lookup"><span data-stu-id="34b1f-177">Add the following code before `Console.ReadLine` to see how objects can be deleted:</span></span>  
  
#### <a name="to-delete-a-row"></a><span data-ttu-id="34b1f-178">删除行</span><span class="sxs-lookup"><span data-stu-id="34b1f-178">To delete a row</span></span>  
  
- <span data-ttu-id="34b1f-179">将下面的代码添加到 `Console.ReadLine();` 上方紧靠它的位置：</span><span class="sxs-lookup"><span data-stu-id="34b1f-179">Add the following code just above `Console.ReadLine();`:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#5)]  
  
## <a name="submitting-changes-to-the-database"></a><span data-ttu-id="34b1f-180">将更改提交到数据库</span><span class="sxs-lookup"><span data-stu-id="34b1f-180">Submitting Changes to the Database</span></span>  

 <span data-ttu-id="34b1f-181">创建、更新和删除对象所需执行的最后一步是将更改实际提交到数据库。</span><span class="sxs-lookup"><span data-stu-id="34b1f-181">The final step required for creating, updating, and deleting objects, is to actually submit the changes to the database.</span></span> <span data-ttu-id="34b1f-182">如不执行这一步，您所做的更改将仅限本地，不会出现在查询结果中。</span><span class="sxs-lookup"><span data-stu-id="34b1f-182">Without this step, your changes are only local and will not appear in query results.</span></span>  
  
#### <a name="to-submit-changes-to-the-database"></a><span data-ttu-id="34b1f-183">将更改提交到数据库</span><span class="sxs-lookup"><span data-stu-id="34b1f-183">To submit changes to the database</span></span>  
  
1. <span data-ttu-id="34b1f-184">将下面的代码插入到 `Console.ReadLine` 上方紧靠它的位置：</span><span class="sxs-lookup"><span data-stu-id="34b1f-184">Insert the following code just above `Console.ReadLine`:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#6](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#6)]  
  
2. <span data-ttu-id="34b1f-185">将下面的代码插入到 `SubmitChanges` 后面，以显示提交更改前后的效果：</span><span class="sxs-lookup"><span data-stu-id="34b1f-185">Insert the following code (after `SubmitChanges`) to show the before and after effects of submitting the changes:</span></span>  
  
     [!code-csharp[DLinqWalk3CS#7](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqWalk3CS/cs/Program.cs#7)]  
  
3. <span data-ttu-id="34b1f-186">按 F5 调试解决方案。</span><span class="sxs-lookup"><span data-stu-id="34b1f-186">Press F5 to debug the solution.</span></span>  
  
4. <span data-ttu-id="34b1f-187">在 **控制台** 窗口中按 enter，以关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="34b1f-187">Press Enter in the **Console** window to close the application.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="34b1f-188">通过提交更改添加了新的客户后，您无法再次按原样执行此解决方案。</span><span class="sxs-lookup"><span data-stu-id="34b1f-188">After you have added the new customer by submitting the changes, you cannot execute this solution again as is.</span></span> <span data-ttu-id="34b1f-189">若要再次执行此解决方案，请更改要添加的客户姓名和客户 ID。</span><span class="sxs-lookup"><span data-stu-id="34b1f-189">To execute the solution again, change the name of the customer and customer ID to be added.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34b1f-190">请参阅</span><span class="sxs-lookup"><span data-stu-id="34b1f-190">See also</span></span>

- [<span data-ttu-id="34b1f-191">通过演练学习</span><span class="sxs-lookup"><span data-stu-id="34b1f-191">Learning by Walkthroughs</span></span>](learning-by-walkthroughs.md)
