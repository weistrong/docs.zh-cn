---
description: '了解有关详细信息，请参阅如何：使用 LINQ (调用存储过程 Visual Basic) '
title: 如何：使用 LINQ 调用存储过程
ms.date: 07/20/2015
helpviewer_keywords:
- queries [LINQ in Visual Basic], stored procedure calls
- stored procedures sample [Visual Basic]
- stored procedures [LINQ to SQL]
- queries [LINQ in Visual Basic], how-to topics
ms.assetid: 6436d384-d1e0-40aa-8afd-451007477260
ms.openlocfilehash: f6fca7ac008e5f0d5f68fdf9c192eaadae9412ef
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100466323"
---
# <a name="how-to-call-a-stored-procedure-by-using-linq-visual-basic"></a><span data-ttu-id="e6fd8-103">如何：使用 LINQ 调用存储过程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e6fd8-103">How to: Call a Stored Procedure by Using LINQ (Visual Basic)</span></span>

<span data-ttu-id="e6fd8-104">Language-Integrated 查询 (LINQ) 使访问数据库信息（包括数据库对象，如存储过程）变得简单。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-104">Language-Integrated Query (LINQ) makes it easy to access database information, including database objects such as stored procedures.</span></span>  
  
 <span data-ttu-id="e6fd8-105">下面的示例演示如何创建一个应用程序，用于调用 SQL Server 数据库中的存储过程。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-105">The following example shows how to create an application that calls a stored procedure in a SQL Server database.</span></span> <span data-ttu-id="e6fd8-106">该示例演示如何调用数据库中的两个不同的存储过程。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-106">The sample shows how to call two different stored procedures in the database.</span></span> <span data-ttu-id="e6fd8-107">每个过程都返回查询的结果。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-107">Each procedure returns the results of a query.</span></span> <span data-ttu-id="e6fd8-108">一个过程采用输入参数，而另一个过程不接受参数。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-108">One procedure takes input parameters, and the other procedure does not take parameters.</span></span>  
  
 <span data-ttu-id="e6fd8-109">本主题中的示例使用 Northwind 示例数据库。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-109">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="e6fd8-110">如果你的开发计算机上没有此数据库，可以从 Microsoft 下载中心进行下载。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-110">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="e6fd8-111">有关说明，请参阅 [下载示例数据库](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-111">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="e6fd8-112">创建与数据库的连接</span><span class="sxs-lookup"><span data-stu-id="e6fd8-112">To create a connection to a database</span></span>  
  
1. <span data-ttu-id="e6fd8-113">在 Visual Studio 中，  / 单击 / "**视图**" 菜单上的 "服务器资源管理器"**数据库资源管理器** 打开服务器资源管理器数据库资源管理器。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-113">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2. <span data-ttu-id="e6fd8-114">右键单击 **服务器资源管理器** 数据库资源管理器中的 "**数据连接**" /  ，然后单击 "**添加连接**"。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-114">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3. <span data-ttu-id="e6fd8-115">指定与 Northwind 示例数据库的有效连接。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-115">Specify a valid connection to the Northwind sample database.</span></span>  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="e6fd8-116">添加包含 LINQ to SQL 文件的项目</span><span class="sxs-lookup"><span data-stu-id="e6fd8-116">To add a project that contains a LINQ to SQL file</span></span>  
  
1. <span data-ttu-id="e6fd8-117">在 Visual Studio 中的“文件”菜单上，指向“新建”，然后单击“项目”。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-117">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="e6fd8-118">选择 Visual Basic **Windows 窗体应用程序** 作为项目类型。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-118">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2. <span data-ttu-id="e6fd8-119">在 **“项目”** 菜单上，单击 **“添加新项”**。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-119">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="e6fd8-120">选择 " **LINQ to SQL 类** " 项模板。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-120">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3. <span data-ttu-id="e6fd8-121">命名文件 `northwind.dbml`。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-121">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="e6fd8-122">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-122">Click **Add**.</span></span> <span data-ttu-id="e6fd8-123">将为 northwind 文件打开对象关系设计器 (O/R 设计器) 。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-123">The Object Relational Designer (O/R Designer) is opened for the northwind.dbml file.</span></span>  
  
### <a name="to-add-stored-procedures-to-the-or-designer"></a><span data-ttu-id="e6fd8-124">将存储过程添加到 O/R 设计器</span><span class="sxs-lookup"><span data-stu-id="e6fd8-124">To add stored procedures to the O/R Designer</span></span>  
  
1. <span data-ttu-id="e6fd8-125">在 **服务器资源管理器** / **数据库资源管理器** 中，展开与 Northwind 数据库的连接。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-125">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="e6fd8-126">展开 **“存储过程”** 文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-126">Expand the **Stored Procedures** folder.</span></span>  
  
     <span data-ttu-id="e6fd8-127">如果关闭了 O/R 设计器，则可以通过双击先前添加的 northwind 文件来重新打开它。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-127">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2. <span data-ttu-id="e6fd8-128">单击 " **按年份的销售额** " 存储过程，并将其拖到设计器的右窗格中。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-128">Click the **Sales by Year** stored procedure and drag it to the right pane of the designer.</span></span> <span data-ttu-id="e6fd8-129">单击 **十个最昂贵的产品** 存储过程，将其拖到设计器的右窗格中。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-129">Click the **Ten Most Expensive Products** stored procedure drag it to the right pane of the designer.</span></span>  
  
3. <span data-ttu-id="e6fd8-130">保存更改并关闭设计器。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-130">Save your changes and close the designer.</span></span>  
  
4. <span data-ttu-id="e6fd8-131">保存你的项目。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-131">Save your project.</span></span>  
  
### <a name="to-add-code-to-display-the-results-of-the-stored-procedures"></a><span data-ttu-id="e6fd8-132">添加代码以显示存储过程的结果</span><span class="sxs-lookup"><span data-stu-id="e6fd8-132">To add code to display the results of the stored procedures</span></span>  
  
1. <span data-ttu-id="e6fd8-133">从 " **工具箱**" 中，将 <xref:System.Windows.Forms.DataGridView> 控件拖动到项目的默认 Windows 窗体 "Form1"。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-133">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2. <span data-ttu-id="e6fd8-134">双击 "Form1"，将代码添加到其 `Load` 事件。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-134">Double-click Form1 to add code to its `Load` event.</span></span>  
  
3. <span data-ttu-id="e6fd8-135">将存储过程添加到 O/R 设计器后，设计器将 <xref:System.Data.Linq.DataContext> 为您的项目添加一个对象。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-135">When you added stored procedures to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object for your project.</span></span> <span data-ttu-id="e6fd8-136">此对象包含访问这些过程所需的代码。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-136">This object contains the code that you must have to access those procedures.</span></span> <span data-ttu-id="e6fd8-137"><xref:System.Data.Linq.DataContext>项目的对象根据 .dbml 文件的名称进行命名。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-137">The <xref:System.Data.Linq.DataContext> object for the project is named based on the name of the .dbml file.</span></span> <span data-ttu-id="e6fd8-138">对于此项目，该 <xref:System.Data.Linq.DataContext> 对象的名称为 `northwindDataContext` 。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-138">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="e6fd8-139">您可以在代码中创建的一个实例 <xref:System.Data.Linq.DataContext> ，并调用由 O/R 设计器指定的存储过程方法。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-139">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and call the stored procedure methods specified by the O/R Designer.</span></span> <span data-ttu-id="e6fd8-140">若要绑定到 <xref:System.Windows.Forms.DataGridView> 对象，可能需要通过对存储过程的结果调用方法来强制立即执行查询 <xref:System.Linq.Enumerable.ToList%2A> 。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-140">To bind to the <xref:System.Windows.Forms.DataGridView> object, you may have to force the query to execute immediately by calling the <xref:System.Linq.Enumerable.ToList%2A> method on the results of the stored procedure.</span></span>  
  
     <span data-ttu-id="e6fd8-141">向事件中添加以下代码 `Load` ，以调用作为数据上下文的方法公开的任何存储过程。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-141">Add the following code to the `Load` event to call either of the stored procedures exposed as methods for your data context.</span></span>  
  
     [!code-vb[VbLINQtoSQLHowTos#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form3.vb#1)]  
    [!code-vb[VbLINQtoSQLHowTos#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form3.vb#2)]  
  
4. <span data-ttu-id="e6fd8-142">按 F5 运行项目并查看结果。</span><span class="sxs-lookup"><span data-stu-id="e6fd8-142">Press F5 to run your project and view the results.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6fd8-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6fd8-143">See also</span></span>

- [<span data-ttu-id="e6fd8-144">LINQ</span><span class="sxs-lookup"><span data-stu-id="e6fd8-144">LINQ</span></span>](index.md)
- [<span data-ttu-id="e6fd8-145">查询</span><span class="sxs-lookup"><span data-stu-id="e6fd8-145">Queries</span></span>](../../../language-reference/queries/index.md)
- [<span data-ttu-id="e6fd8-146">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="e6fd8-146">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)
- [<span data-ttu-id="e6fd8-147">DataContext 方法（O/R 设计器）</span><span class="sxs-lookup"><span data-stu-id="e6fd8-147">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
- [<span data-ttu-id="e6fd8-148">如何：分配存储流程来执行更新、插入和删除操作（O/R 设计器）</span><span class="sxs-lookup"><span data-stu-id="e6fd8-148">How to: Assign stored procedures to perform updates, inserts, and deletes (O/R Designer)</span></span>](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)
