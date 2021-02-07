---
description: 了解详细信息：如何：将 DataView 对象绑定到 Windows 窗体 DataGridView 控件
title: 如何：将 DataView 对象绑定到 Windows 窗体 DataGridView 控件
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2b73d60a-6049-446a-85a7-3e5a68b183e2
ms.openlocfilehash: 59bc1a0f6b7b2b0d6da4fa6d88e06922d95c9f46
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723902"
---
# <a name="how-to-bind-a-dataview-object-to-a-windows-forms-datagridview-control"></a><span data-ttu-id="9a330-103">如何：将 DataView 对象绑定到 Windows 窗体 DataGridView 控件</span><span class="sxs-lookup"><span data-stu-id="9a330-103">How to: Bind a DataView Object to a Windows Forms DataGridView Control</span></span>

<span data-ttu-id="9a330-104"><xref:System.Windows.Forms.DataGridView> 控件提供一种以表格格式显示数据的功能强大且灵活的方法。</span><span class="sxs-lookup"><span data-stu-id="9a330-104">The <xref:System.Windows.Forms.DataGridView> control provides a powerful and flexible way to display data in a tabular format.</span></span> <span data-ttu-id="9a330-105"><xref:System.Windows.Forms.DataGridView> 控件支持标准 Windows 窗体数据绑定模型，因此它可以绑定到 <xref:System.Data.DataView> 和各种其他数据源。</span><span class="sxs-lookup"><span data-stu-id="9a330-105">The <xref:System.Windows.Forms.DataGridView> control supports the standard Windows Forms data binding model, so it will bind to <xref:System.Data.DataView> and a variety of other data sources.</span></span> <span data-ttu-id="9a330-106">但在多数情况下，该控件将会绑定到用于管理数据源交互详细信息的 <xref:System.Windows.Forms.BindingSource> 组件。</span><span class="sxs-lookup"><span data-stu-id="9a330-106">In most situations, however, you will bind to a <xref:System.Windows.Forms.BindingSource> component that will manage the details of interacting with the data source.</span></span>  
  
 <span data-ttu-id="9a330-107">有关控件的详细信息 <xref:System.Windows.Forms.DataGridView> ，请参阅 [DataGridView 控件概述](/dotnet/desktop/winforms/controls/datagridview-control-overview-windows-forms)。</span><span class="sxs-lookup"><span data-stu-id="9a330-107">For more information about the <xref:System.Windows.Forms.DataGridView> control, see [DataGridView Control Overview](/dotnet/desktop/winforms/controls/datagridview-control-overview-windows-forms).</span></span>  
  
### <a name="to-connect-a-datagridview-control-to-a-dataview"></a><span data-ttu-id="9a330-108">将 DataGridView 控件连接到 DataView</span><span class="sxs-lookup"><span data-stu-id="9a330-108">To connect a DataGridView control to a DataView</span></span>  
  
1. <span data-ttu-id="9a330-109">实现方法以处理有关从数据库检索数据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9a330-109">Implement a method to handle the details of retrieving data from a database.</span></span> <span data-ttu-id="9a330-110">下面的代码示例实现 `GetData` 方法，该方法初始化 <xref:System.Data.SqlClient.SqlDataAdapter> 组件并使用该组件来填充 <xref:System.Data.DataSet>。</span><span class="sxs-lookup"><span data-stu-id="9a330-110">The following code example implements a `GetData` method that initializes a <xref:System.Data.SqlClient.SqlDataAdapter> component and uses it to fill a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="9a330-111">请确保将 `connectionString` 变量设置为适合数据库的值。</span><span class="sxs-lookup"><span data-stu-id="9a330-111">Be sure to set the `connectionString` variable to a value that is appropriate for your database.</span></span> <span data-ttu-id="9a330-112">您需要访问安装有 AdventureWorks SQL Server 示例数据库的服务器。</span><span class="sxs-lookup"><span data-stu-id="9a330-112">You will need access to a server with the AdventureWorks SQL Server sample database installed.</span></span>  
  
     [!code-csharp[DP DataViewWinForms Sample#LDVSample1GetData](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP DataViewWinForms Sample/CS/Form1.cs#ldvsample1getdata)]
     [!code-vb[DP DataViewWinForms Sample#LDVSample1GetData](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP DataViewWinForms Sample/VB/Form1.vb#ldvsample1getdata)]  
  
2. <span data-ttu-id="9a330-113">在窗体的 <xref:System.Windows.Forms.Form.Load> 事件处理程序中，将 <xref:System.Windows.Forms.DataGridView> 控件绑定到 <xref:System.Windows.Forms.BindingSource> 组件并调用 `GetData` 方法，以从数据库检索数据。</span><span class="sxs-lookup"><span data-stu-id="9a330-113">In the <xref:System.Windows.Forms.Form.Load> event handler of your form, bind the <xref:System.Windows.Forms.DataGridView> control to the <xref:System.Windows.Forms.BindingSource> component and call the `GetData` method to retrieve the data from the database.</span></span> <span data-ttu-id="9a330-114"><xref:System.Data.DataView>通过联系人的 LINQ to DataSet 查询创建 <xref:System.Data.DataTable> ，然后绑定到 <xref:System.Windows.Forms.BindingSource> 组件。</span><span class="sxs-lookup"><span data-stu-id="9a330-114">The <xref:System.Data.DataView> is created from a LINQ to DataSet query over the Contact <xref:System.Data.DataTable> and is then bound to the <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
     [!code-csharp[DP DataViewWinForms Sample#LDVSample1FormLoad](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP DataViewWinForms Sample/CS/Form1.cs#ldvsample1formload)]
     [!code-vb[DP DataViewWinForms Sample#LDVSample1FormLoad](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP DataViewWinForms Sample/VB/Form1.vb#ldvsample1formload)]  
  
## <a name="see-also"></a><span data-ttu-id="9a330-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a330-115">See also</span></span>

- [<span data-ttu-id="9a330-116">数据绑定和 LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="9a330-116">Data Binding and LINQ to DataSet</span></span>](data-binding-and-linq-to-dataset.md)
