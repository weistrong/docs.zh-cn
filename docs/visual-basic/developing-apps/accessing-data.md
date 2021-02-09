---
description: 详细了解：在 Visual Basic 应用程序中访问数据
title: 在 Visual Basic 应用程序中访问数据
ms.date: 07/20/2015
helpviewer_keywords:
- data [Visual Basic]
- Visual Basic, data access
ms.assetid: 3086ab38-3be5-4b22-9385-7d0e16b04f6a
ms.openlocfilehash: 751705a1375782fae1f7ed3aa8590c377ac93d9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641585"
---
# <a name="accessing-data-in-visual-basic-applications"></a><span data-ttu-id="c5d71-103">在 Visual Basic 应用程序中访问数据</span><span class="sxs-lookup"><span data-stu-id="c5d71-103">Accessing data in Visual Basic applications</span></span>

<span data-ttu-id="c5d71-104">Visual Basic 包括多种新功能，以帮助开发访问数据的应用程序。</span><span class="sxs-lookup"><span data-stu-id="c5d71-104">Visual Basic includes several new features to assist in developing applications that access data.</span></span> <span data-ttu-id="c5d71-105">通过将项从[“数据源”窗口](/visualstudio/data-tools/add-new-data-sources)拖到窗体上来创建 Windows 应用程序的数据绑定窗体。</span><span class="sxs-lookup"><span data-stu-id="c5d71-105">Data-bound forms for Windows applications are created by dragging items from the [Data Sources Window](/visualstudio/data-tools/add-new-data-sources) onto the form.</span></span> <span data-ttu-id="c5d71-106">通过将项从“数据源窗口”拖动到现有控件上来将控件绑定到数据。 </span><span class="sxs-lookup"><span data-stu-id="c5d71-106">You bind controls to data by dragging items from the **Data Sources Window** onto existing controls.</span></span>

## <a name="related-sections"></a><span data-ttu-id="c5d71-107">相关章节</span><span class="sxs-lookup"><span data-stu-id="c5d71-107">Related sections</span></span>

[<span data-ttu-id="c5d71-108">在 Visual Studio 中访问数据</span><span class="sxs-lookup"><span data-stu-id="c5d71-108">Accessing Data in Visual Studio</span></span>](/visualstudio/data-tools/)  
<span data-ttu-id="c5d71-109">提供相关页面链接，这些页面讨论如何将数据访问功能结合到应用程序中。</span><span class="sxs-lookup"><span data-stu-id="c5d71-109">Provides links to pages that discuss incorporating data access functionality into your applications.</span></span>

[<span data-ttu-id="c5d71-110">适用于 NET 的 Visual Studio Data Tools</span><span class="sxs-lookup"><span data-stu-id="c5d71-110">Visual Studio data tools for .NET</span></span>](/visualstudio/data-tools/visual-studio-data-tools-for-dotnet)  
<span data-ttu-id="c5d71-111">收录了相关页面链接，这些页面介绍了如何使用 Visual Studio 创建数据处理应用程序。</span><span class="sxs-lookup"><span data-stu-id="c5d71-111">Provides links to pages on creating applications that work with data, using Visual Studio.</span></span>

[<span data-ttu-id="c5d71-112">LINQ</span><span class="sxs-lookup"><span data-stu-id="c5d71-112">LINQ</span></span>](../programming-guide/language-features/linq/index.md)  
<span data-ttu-id="c5d71-113">提供介绍如何在 Visual Basic 中使用 LINQ 的主题的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-113">Provides links to topics that describe how to use LINQ with Visual Basic.</span></span>

[<span data-ttu-id="c5d71-114">LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="c5d71-114">LINQ to SQL</span></span>](../../framework/data/adonet/sql/linq/index.md)  
<span data-ttu-id="c5d71-115">提供有关 [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] 的信息。</span><span class="sxs-lookup"><span data-stu-id="c5d71-115">Provides information about [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)].</span></span> <span data-ttu-id="c5d71-116">包括编程示例。</span><span class="sxs-lookup"><span data-stu-id="c5d71-116">Includes programming examples.</span></span>  

[<span data-ttu-id="c5d71-117">Visual Studio 中的 LINQ to SQL 工具</span><span class="sxs-lookup"><span data-stu-id="c5d71-117">LINQ to SQL Tools in Visual Studio</span></span>](/visualstudio/data-tools/linq-to-sql-tools-in-visual-studio2)  
<span data-ttu-id="c5d71-118">提供介绍如何在应用程序中创建 [LINQ to SQL](../../framework/data/adonet/sql/linq/index.md) 对象模型的主题的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-118">Provides links to topics about how to create a [LINQ to SQL](../../framework/data/adonet/sql/linq/index.md) object model in applications.</span></span>

[<span data-ttu-id="c5d71-119">在 N 层应用程序中使用数据集</span><span class="sxs-lookup"><span data-stu-id="c5d71-119">Work with datasets in n-tier applications</span></span>](/visualstudio/data-tools/work-with-datasets-in-n-tier-applications)  
<span data-ttu-id="c5d71-120">提供介绍如何创建多层数据应用程序的主题的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-120">Provides links to topics about how to create multitiered data applications.</span></span>

[<span data-ttu-id="c5d71-121">添加新连接</span><span class="sxs-lookup"><span data-stu-id="c5d71-121">Add new connections</span></span>](/visualstudio/data-tools/add-new-connections)  
<span data-ttu-id="c5d71-122">收录了相关页面链接，这些页面介绍了如何通过 Visual Studio 使用设计时工具和 ADO.NET 连接对象将应用程序连接到数据。</span><span class="sxs-lookup"><span data-stu-id="c5d71-122">Provides links to pages on connecting your application to data with design-time tools and ADO.NET connection objects, using Visual Studio.</span></span>

[<span data-ttu-id="c5d71-123">Visual Studio 中的数据集工具</span><span class="sxs-lookup"><span data-stu-id="c5d71-123">Dataset Tools in Visual Studio</span></span>](/visualstudio/data-tools/dataset-tools-in-visual-studio)  
<span data-ttu-id="c5d71-124">提供介绍如何将数据加载到数据集以及如何执行 SQL 语句和存储过程的页面的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-124">Provides links to pages describing how to load data into datasets and how to execute SQL statements and stored procedures.</span></span>  

[<span data-ttu-id="c5d71-125">在 Visual Studio 中将控件绑定到数据</span><span class="sxs-lookup"><span data-stu-id="c5d71-125">Bind controls to data in Visual Studio</span></span>](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)  
<span data-ttu-id="c5d71-126">提供说明如何通过数据绑定控件在 Windows 窗体上显示数据的页面的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-126">Provides links to pages that explain how to display data on Windows Forms through data-bound controls.</span></span>

[<span data-ttu-id="c5d71-127">编辑数据集中的数据</span><span class="sxs-lookup"><span data-stu-id="c5d71-127">Edit Data in Datasets</span></span>](/visualstudio/data-tools/edit-data-in-datasets)  
<span data-ttu-id="c5d71-128">提供介绍如何操作数据集的数据表中数据的页面的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-128">Provides links to pages describing how to manipulate the data in the data tables of a dataset.</span></span>  

[<span data-ttu-id="c5d71-129">验证数据集中的数据</span><span class="sxs-lookup"><span data-stu-id="c5d71-129">Validate data in datasets</span></span>](/visualstudio/data-tools/validate-data-in-datasets)  
<span data-ttu-id="c5d71-130">提供介绍如何在列和行更改过程中向数据集添加验证的页面的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-130">Provides links to pages describing how to add validation to a dataset during column and row changes.</span></span>

[<span data-ttu-id="c5d71-131">将数据保存回数据库</span><span class="sxs-lookup"><span data-stu-id="c5d71-131">Save data back to the database</span></span>](/visualstudio/data-tools/save-data-back-to-the-database)  
<span data-ttu-id="c5d71-132">提供说明如何将更新后的数据从应用程序发送到数据库的页面的链接。</span><span class="sxs-lookup"><span data-stu-id="c5d71-132">Provides links to pages explaining how to send updated data from an application to the database.</span></span>

[<span data-ttu-id="c5d71-133">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="c5d71-133">ADO.NET</span></span>](../../framework/data/adonet/index.md)  
<span data-ttu-id="c5d71-134">描述 ADO.NET 类，该类向 .NET Framework 程序员公开数据访问服务。</span><span class="sxs-lookup"><span data-stu-id="c5d71-134">Describes the ADO.NET classes, which expose data-access services to the .NET Framework programmer.</span></span>

[<span data-ttu-id="c5d71-135">Office 解决方案中的数据</span><span class="sxs-lookup"><span data-stu-id="c5d71-135">Data in Office Solutions</span></span>](/visualstudio/vsto/data-in-office-solutions)  
<span data-ttu-id="c5d71-136">包含相关页面的链接，这些页面阐释了数据在 Office 解决方案中的工作方式（包括有关面向架构的编程、数据缓存和服务器端数据访问的信息）。</span><span class="sxs-lookup"><span data-stu-id="c5d71-136">Contains links to pages that explain how data works in Office solutions, including information about schema-oriented programming, data caching, and server-side data access.</span></span>
