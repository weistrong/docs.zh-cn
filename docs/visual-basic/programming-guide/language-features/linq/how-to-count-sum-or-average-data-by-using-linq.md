---
description: '了解有关详细信息，请参阅如何：使用 LINQ (Visual Basic 对数据进行计数、求和或求平均值) '
title: 如何：使用 LINQ 对数据进行计数、求和与求平均值计算
ms.date: 07/20/2015
helpviewer_keywords:
- average operator [LINQ in Visual Basic]
- aggregate operator [LINQ in Visual Basic]
- aggregate queries
- queries [LINQ in Visual Basic], sum results
- Aggregate clause [Visual Basic]
- sum operator [LINQ in Visual Basic]
- queries [LINQ in Visual Basic], aggregate queries
- queries [LINQ in Visual Basic], counting results
- querying databases [LINQ]
- queries [LINQ in Visual Basic], how-to topics
- query samples [Visual Basic]
- count operator [LINQ in Visual Basic]
ms.assetid: 51ca1f59-7770-4884-8b76-113002e54fc0
ms.openlocfilehash: 1759a2f990c2e61a862d032f2a09f29f65a05103
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100422780"
---
# <a name="how-to-count-sum-or-average-data-by-using-linq-visual-basic"></a><span data-ttu-id="e5543-103">如何：使用 LINQ 对数据进行计数、求和与求平均值计算 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e5543-103">How to: Count, Sum, or Average Data by Using LINQ (Visual Basic)</span></span>

<span data-ttu-id="e5543-104">Language-Integrated 查询 (LINQ) 可以轻松地访问数据库信息和执行查询。</span><span class="sxs-lookup"><span data-stu-id="e5543-104">Language-Integrated Query (LINQ) makes it easy to access database information and execute queries.</span></span>  
  
 <span data-ttu-id="e5543-105">下面的示例演示如何创建一个新应用程序，用于对 SQL Server 数据库执行查询。</span><span class="sxs-lookup"><span data-stu-id="e5543-105">The following example shows how to create a new application that performs queries against a SQL Server database.</span></span> <span data-ttu-id="e5543-106">该示例通过使用和子句对结果进行计数、求和和求平均值 `Aggregate` `Group By` 。</span><span class="sxs-lookup"><span data-stu-id="e5543-106">The sample counts, sums, and averages the results by using the `Aggregate` and `Group By` clauses.</span></span> <span data-ttu-id="e5543-107">有关详细信息，请参阅 [Aggregate 子句](../../../language-reference/queries/aggregate-clause.md) 和 [Group By 子句](../../../language-reference/queries/group-by-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="e5543-107">For more information, see [Aggregate Clause](../../../language-reference/queries/aggregate-clause.md) and [Group By Clause](../../../language-reference/queries/group-by-clause.md).</span></span>  
  
 <span data-ttu-id="e5543-108">本主题中的示例使用 Northwind 示例数据库。</span><span class="sxs-lookup"><span data-stu-id="e5543-108">The examples in this topic use the Northwind sample database.</span></span> <span data-ttu-id="e5543-109">如果你的开发计算机上没有此数据库，可以从 Microsoft 下载中心进行下载。</span><span class="sxs-lookup"><span data-stu-id="e5543-109">If you do not have this database on your development computer, you can download it from the Microsoft Download Center.</span></span> <span data-ttu-id="e5543-110">有关说明，请参阅 [下载示例数据库](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="e5543-110">For instructions, see [Downloading Sample Databases](../../../../framework/data/adonet/sql/linq/downloading-sample-databases.md).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-connection-to-a-database"></a><span data-ttu-id="e5543-111">创建与数据库的连接</span><span class="sxs-lookup"><span data-stu-id="e5543-111">To create a connection to a database</span></span>  
  
1. <span data-ttu-id="e5543-112">在 Visual Studio 中，  / 单击 / "**视图**" 菜单上的 "服务器资源管理器"**数据库资源管理器** 打开服务器资源管理器数据库资源管理器。</span><span class="sxs-lookup"><span data-stu-id="e5543-112">In Visual Studio, open **Server Explorer**/**Database Explorer** by clicking **Server Explorer**/**Database Explorer** on the **View** menu.</span></span>  
  
2. <span data-ttu-id="e5543-113">右键单击 **服务器资源管理器** 数据库资源管理器中的 "**数据连接**" /  ，然后单击 "**添加连接**"。</span><span class="sxs-lookup"><span data-stu-id="e5543-113">Right-click **Data Connections** in **Server Explorer**/**Database Explorer** and then click **Add Connection**.</span></span>  
  
3. <span data-ttu-id="e5543-114">指定与 Northwind 示例数据库的有效连接。</span><span class="sxs-lookup"><span data-stu-id="e5543-114">Specify a valid connection to the Northwind sample database.</span></span>  
  
### <a name="to-add-a-project-that-contains-a-linq-to-sql-file"></a><span data-ttu-id="e5543-115">添加包含 LINQ to SQL 文件的项目</span><span class="sxs-lookup"><span data-stu-id="e5543-115">To add a project that contains a LINQ to SQL file</span></span>  
  
1. <span data-ttu-id="e5543-116">在 Visual Studio 中的“文件”菜单上，指向“新建”，然后单击“项目”。</span><span class="sxs-lookup"><span data-stu-id="e5543-116">In Visual Studio, on the **File** menu, point to **New** and then click **Project**.</span></span> <span data-ttu-id="e5543-117">选择 Visual Basic **Windows 窗体应用程序** 作为项目类型。</span><span class="sxs-lookup"><span data-stu-id="e5543-117">Select Visual Basic **Windows Forms Application** as the project type.</span></span>  
  
2. <span data-ttu-id="e5543-118">在 **“项目”** 菜单上，单击 **“添加新项”**。</span><span class="sxs-lookup"><span data-stu-id="e5543-118">On the **Project** menu, click **Add New Item**.</span></span> <span data-ttu-id="e5543-119">选择 " **LINQ to SQL 类** " 项模板。</span><span class="sxs-lookup"><span data-stu-id="e5543-119">Select the **LINQ to SQL Classes** item template.</span></span>  
  
3. <span data-ttu-id="e5543-120">命名文件 `northwind.dbml`。</span><span class="sxs-lookup"><span data-stu-id="e5543-120">Name the file `northwind.dbml`.</span></span> <span data-ttu-id="e5543-121">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="e5543-121">Click **Add**.</span></span> <span data-ttu-id="e5543-122">将为 northwind 文件打开对象关系设计器 (O/R 设计器) 。</span><span class="sxs-lookup"><span data-stu-id="e5543-122">The Object Relational Designer (O/R Designer) is opened for the northwind.dbml file.</span></span>  
  
### <a name="to-add-tables-to-query-to-the-or-designer"></a><span data-ttu-id="e5543-123">添加要查询到 O/R 设计器的表</span><span class="sxs-lookup"><span data-stu-id="e5543-123">To add tables to query to the O/R Designer</span></span>  
  
1. <span data-ttu-id="e5543-124">在 **服务器资源管理器** / **数据库资源管理器** 中，展开与 Northwind 数据库的连接。</span><span class="sxs-lookup"><span data-stu-id="e5543-124">In **Server Explorer**/**Database Explorer**, expand the connection to the Northwind database.</span></span> <span data-ttu-id="e5543-125">展开 **“表”** 文件夹。</span><span class="sxs-lookup"><span data-stu-id="e5543-125">Expand the **Tables** folder.</span></span>  
  
     <span data-ttu-id="e5543-126">如果关闭了 O/R 设计器，则可以通过双击先前添加的 northwind 文件来重新打开它。</span><span class="sxs-lookup"><span data-stu-id="e5543-126">If you have closed the O/R Designer, you can reopen it by double-clicking the northwind.dbml file that you added earlier.</span></span>  
  
2. <span data-ttu-id="e5543-127">单击 "Customers" 表，并将其拖到设计器的左窗格中。</span><span class="sxs-lookup"><span data-stu-id="e5543-127">Click the Customers table and drag it to the left pane of the designer.</span></span> <span data-ttu-id="e5543-128">单击 "Orders" 表，并将其拖到设计器的左窗格中。</span><span class="sxs-lookup"><span data-stu-id="e5543-128">Click the Orders table and drag it to the left pane of the designer.</span></span>  
  
     <span data-ttu-id="e5543-129">设计器将 `Customer` `Order` 为您的项目创建新的和对象。</span><span class="sxs-lookup"><span data-stu-id="e5543-129">The designer creates new `Customer` and `Order` objects for your project.</span></span> <span data-ttu-id="e5543-130">请注意，设计器将自动检测表之间的关系，并创建相关对象的子属性。</span><span class="sxs-lookup"><span data-stu-id="e5543-130">Notice that the designer automatically detects relationships between the tables and creates child properties for related objects.</span></span> <span data-ttu-id="e5543-131">例如，IntelliSense 将显示 `Customer` 对象具有 `Orders` 与该客户相关的所有订单的属性。</span><span class="sxs-lookup"><span data-stu-id="e5543-131">For example, IntelliSense will show that the `Customer` object has an `Orders` property for all orders related to that customer.</span></span>  
  
3. <span data-ttu-id="e5543-132">保存更改并关闭设计器。</span><span class="sxs-lookup"><span data-stu-id="e5543-132">Save your changes and close the designer.</span></span>  
  
4. <span data-ttu-id="e5543-133">保存你的项目。</span><span class="sxs-lookup"><span data-stu-id="e5543-133">Save your project.</span></span>  
  
### <a name="to-add-code-to-query-the-database-and-display-the-results"></a><span data-ttu-id="e5543-134">添加代码以查询数据库并显示结果</span><span class="sxs-lookup"><span data-stu-id="e5543-134">To add code to query the database and display the results</span></span>  
  
1. <span data-ttu-id="e5543-135">从 " **工具箱**" 中，将 <xref:System.Windows.Forms.DataGridView> 控件拖动到项目的默认 Windows 窗体 "Form1"。</span><span class="sxs-lookup"><span data-stu-id="e5543-135">From the **Toolbox**, drag a <xref:System.Windows.Forms.DataGridView> control onto the default Windows Form for your project, Form1.</span></span>  
  
2. <span data-ttu-id="e5543-136">双击 "Form1"，将代码添加到 `Load` 窗体的事件中。</span><span class="sxs-lookup"><span data-stu-id="e5543-136">Double-click Form1 to add code to the `Load` event of the form.</span></span>  
  
3. <span data-ttu-id="e5543-137">在将表添加到 O/R 设计器后，设计器将 <xref:System.Data.Linq.DataContext> 为您的项目添加一个对象。</span><span class="sxs-lookup"><span data-stu-id="e5543-137">When you added tables to the O/R Designer, the designer added a <xref:System.Data.Linq.DataContext> object for your project.</span></span> <span data-ttu-id="e5543-138">此对象包含访问这些表所需的代码，以及访问每个表的单个对象和集合的代码。</span><span class="sxs-lookup"><span data-stu-id="e5543-138">This object contains the code that you must have to access those tables, and to access individual objects and collections for each table.</span></span> <span data-ttu-id="e5543-139"><xref:System.Data.Linq.DataContext>项目的对象根据 .dbml 文件的名称进行命名。</span><span class="sxs-lookup"><span data-stu-id="e5543-139">The <xref:System.Data.Linq.DataContext> object for your project is named based on the name of your .dbml file.</span></span> <span data-ttu-id="e5543-140">对于此项目，该 <xref:System.Data.Linq.DataContext> 对象的名称为 `northwindDataContext` 。</span><span class="sxs-lookup"><span data-stu-id="e5543-140">For this project, the <xref:System.Data.Linq.DataContext> object is named `northwindDataContext`.</span></span>  
  
     <span data-ttu-id="e5543-141">您可以在代码中创建的一个实例 <xref:System.Data.Linq.DataContext> ，并查询由 O/R 设计器指定的表。</span><span class="sxs-lookup"><span data-stu-id="e5543-141">You can create an instance of the <xref:System.Data.Linq.DataContext> in your code and query the tables specified by the O/R Designer.</span></span>  
  
     <span data-ttu-id="e5543-142">将以下代码添加到 `Load` 事件，以查询作为的属性公开的表， <xref:System.Data.Linq.DataContext> 并计算结果的计数、总和和平均值。</span><span class="sxs-lookup"><span data-stu-id="e5543-142">Add the following code to the `Load` event to query the tables that are exposed as properties of your <xref:System.Data.Linq.DataContext> and count, sum, and average the results.</span></span> <span data-ttu-id="e5543-143">该示例使用 `Aggregate` 子句来查询单个结果，并使用 `Group By` 子句来显示分组结果的平均值。</span><span class="sxs-lookup"><span data-stu-id="e5543-143">The sample uses the `Aggregate` clause to query for a single result, and the `Group By` clause to show an average for grouped results.</span></span>  
  
     [!code-vb[VbLINQToSQLHowTos#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos/VB/Form6.vb#13)]  
  
4. <span data-ttu-id="e5543-144">按 F5 运行项目并查看结果。</span><span class="sxs-lookup"><span data-stu-id="e5543-144">Press F5 to run your project and view the results.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5543-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e5543-145">See also</span></span>

- [<span data-ttu-id="e5543-146">LINQ</span><span class="sxs-lookup"><span data-stu-id="e5543-146">LINQ</span></span>](index.md)
- [<span data-ttu-id="e5543-147">查询</span><span class="sxs-lookup"><span data-stu-id="e5543-147">Queries</span></span>](../../../language-reference/queries/index.md)
- [<span data-ttu-id="e5543-148">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="e5543-148">LINQ to SQL</span></span>](../../../../framework/data/adonet/sql/linq/index.md)
- [<span data-ttu-id="e5543-149">DataContext 方法（O/R 设计器）</span><span class="sxs-lookup"><span data-stu-id="e5543-149">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)
- [<span data-ttu-id="e5543-150">Aggregate Clause</span><span class="sxs-lookup"><span data-stu-id="e5543-150">Aggregate Clause</span></span>](../../../language-reference/queries/aggregate-clause.md)
- [<span data-ttu-id="e5543-151">Group By 子句</span><span class="sxs-lookup"><span data-stu-id="e5543-151">Group By Clause</span></span>](../../../language-reference/queries/group-by-clause.md)
