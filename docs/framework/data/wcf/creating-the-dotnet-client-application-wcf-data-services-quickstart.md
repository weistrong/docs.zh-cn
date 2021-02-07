---
description: '详细了解：创建 .NET Framework 客户端应用程序 (WCF Data Services 快速入门) '
title: 创建 .NET Framework 客户端应用程序（WCF 数据服务快速入门）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 41ade767-eeab-437d-9121-9797e8fb8045
ms.openlocfilehash: 6a397726b0680d4091f7cefd8928e43c74dc08bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766207"
---
# <a name="creating-the-net-framework-client-application-wcf-data-services-quickstart"></a><span data-ttu-id="5f90d-103">创建 .NET Framework 客户端应用程序（WCF 数据服务快速入门）</span><span class="sxs-lookup"><span data-stu-id="5f90d-103">Creating the .NET Framework Client Application (WCF Data Services Quickstart)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="5f90d-104">这是 WCF Data Services 快速入门的最后一任务。</span><span class="sxs-lookup"><span data-stu-id="5f90d-104">This is the final task of the WCF Data Services quickstart.</span></span> <span data-ttu-id="5f90d-105">在此任务中，您将向解决方案添加一个控制台应用程序，添加对该 Open Data Protocol 的引用 (OData) 源添加到此新的客户端应用程序，并使用生成的客户端数据服务类和客户端库从客户端应用程序访问 OData 数据源。</span><span class="sxs-lookup"><span data-stu-id="5f90d-105">In this task, you will add a console application to the solution, add a reference to the Open Data Protocol (OData) feed into this new client application, and access the OData feed from the client application by using the generated client data service classes and client libraries.</span></span>

> [!NOTE]
> <span data-ttu-id="5f90d-106">访问数据源不需要基于 .NET Framework 的客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f90d-106">A .NET Framework-based client application is not required to access a data feed.</span></span> <span data-ttu-id="5f90d-107">使用 OData 源的任何应用程序组件都可以访问该数据服务。</span><span class="sxs-lookup"><span data-stu-id="5f90d-107">The data service can be accessed by any application component that consumes an OData feed.</span></span> <span data-ttu-id="5f90d-108">有关详细信息，请参阅 [在客户端应用程序中使用数据服务](using-a-data-service-in-a-client-application-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="5f90d-108">For more information, see [Using a Data Service in a Client Application](using-a-data-service-in-a-client-application-wcf-data-services.md).</span></span>

## <a name="to-create-the-client-application-by-using-visual-studio"></a><span data-ttu-id="5f90d-109">使用 Visual Studio 创建客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="5f90d-109">To create the client application by using Visual Studio</span></span>

1. <span data-ttu-id="5f90d-110">在 **解决方案资源管理器** 中，右键单击解决方案，单击 " **添加**"，然后单击 " **新建项目**"。</span><span class="sxs-lookup"><span data-stu-id="5f90d-110">In **Solution Explorer**, right-click the solution, click **Add**, and then click **New Project**.</span></span>

2. <span data-ttu-id="5f90d-111">在左窗格中，选择 " **已安装** > [**Visual c #** 或 **Visual Basic**]" > **Windows 桌面**"，然后选择" **WPF 应用程序** "模板。</span><span class="sxs-lookup"><span data-stu-id="5f90d-111">In the left pane, select **Installed** > [**Visual C#** or **Visual Basic**] > **Windows Desktop**, and then select the **WPF App** template.</span></span>

3. <span data-ttu-id="5f90d-112">输入 `NorthwindClient` 作为项目名称，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="5f90d-112">Enter `NorthwindClient` for the project name, and then click **OK**.</span></span>

4. <span data-ttu-id="5f90d-113">打开文件 MainWindow.xaml 并用下列代码替换 XAML 代码：</span><span class="sxs-lookup"><span data-stu-id="5f90d-113">Open the file MainWindow.xaml and replace the XAML code with the following code:</span></span>

     [!code-xaml[Astoria Quickstart Client#Window1Xaml](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_quickstart_client/vb/window1.xaml#window1xaml)]

## <a name="to-add-a-data-service-reference-to-the-project"></a><span data-ttu-id="5f90d-114">在项目中添加数据服务引用</span><span class="sxs-lookup"><span data-stu-id="5f90d-114">To add a data service reference to the project</span></span>

1. <span data-ttu-id="5f90d-115">在 **解决方案资源管理器** 中，右键单击 NorthwindClient 项目，单击 "**添加**  >  **服务引用**"，然后单击 "**发现**"。</span><span class="sxs-lookup"><span data-stu-id="5f90d-115">In **Solution Explorer**, right-click the NorthwindClient project, click **Add** > **Service Reference**, and then click **Discover**.</span></span>

     <span data-ttu-id="5f90d-116">这将显示在第一个任务中创建的 Northwind 数据服务。</span><span class="sxs-lookup"><span data-stu-id="5f90d-116">This displays the Northwind data service that you created in the first task.</span></span>

2. <span data-ttu-id="5f90d-117">在 " **命名空间** " 文本框中，键入 `Northwind` ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="5f90d-117">In the **Namespace** text box, type `Northwind`, and then click **OK**.</span></span>

     <span data-ttu-id="5f90d-118">这将在项目中添加一个新的代码文件，其中包含用于作为对象访问数据服务资源并与其交互的数据类。</span><span class="sxs-lookup"><span data-stu-id="5f90d-118">This adds a new code file to the project, which contains the data classes that are used to access and interact with data service resources as objects.</span></span> <span data-ttu-id="5f90d-119">这些数据类是在命名空间 `NorthwindClient.Northwind` 中创建的。</span><span class="sxs-lookup"><span data-stu-id="5f90d-119">The data classes are created in the namespace `NorthwindClient.Northwind`.</span></span>

## <a name="to-access-data-service-data-in-the-wpf-application"></a><span data-ttu-id="5f90d-120">在 WPF 应用程序中访问数据服务数据</span><span class="sxs-lookup"><span data-stu-id="5f90d-120">To access data service data in the WPF application</span></span>

1. <span data-ttu-id="5f90d-121">在 " **NorthwindClient**" 下的 "**解决方案资源管理器** 中，右键单击项目，然后单击"**添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="5f90d-121">In **Solution Explorer** under **NorthwindClient**, right-click the project and click **Add Reference**.</span></span>

2. <span data-ttu-id="5f90d-122">在 " **添加引用** " 对话框中，单击 " **.net** " 选项卡，选择 System.Data.Services.Client.dll 程序集，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="5f90d-122">In the **Add Reference** dialog box, click the **.NET** tab, select the System.Data.Services.Client.dll assembly, and then click **OK**.</span></span>

3. <span data-ttu-id="5f90d-123">在 " **NorthwindClient**" 下的 "**解决方案资源管理器** 中，打开 mainwindow.xaml 文件的代码页，并将以下 `using` 语句 (添加 `Imports` Visual Basic) 中。</span><span class="sxs-lookup"><span data-stu-id="5f90d-123">In **Solution Explorer** under **NorthwindClient**, open the code page for the MainWindow.xaml file, and add the following `using` statement (`Imports` in Visual Basic).</span></span>

    [!code-csharp[Astoria Quickstart Client#Using](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_quickstart_client/cs/window1.xaml.cs#using)]
    [!code-vb[Astoria Quickstart Client#Using](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_quickstart_client/vb/window1.xaml.vb#using)]

4. <span data-ttu-id="5f90d-124">将用于查询数据服务并将结果绑定到 <xref:System.Data.Services.Client.DataServiceCollection%601> 的下列代码插入到 `MainWindow` 类：</span><span class="sxs-lookup"><span data-stu-id="5f90d-124">Insert the following code that queries that data service and binds the result to a <xref:System.Data.Services.Client.DataServiceCollection%601> into the `MainWindow` class:</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f90d-125">必须用承载 Northwind 数据服务的实例的服务器和端口替换主机名 `localhost:12345`。</span><span class="sxs-lookup"><span data-stu-id="5f90d-125">You must replace the host name `localhost:12345` with the server and port that is hosting your instance of the Northwind data service.</span></span>

     [!code-csharp[Astoria Quickstart Client#QueryCode](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_quickstart_client/cs/window1.xaml.cs#querycode)]
     [!code-vb[Astoria Quickstart Client#QueryCode](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_quickstart_client/vb/window1.xaml.vb#querycode)]

5. <span data-ttu-id="5f90d-126">将用于保存更改的下列代码插入到 `MainWindow` 类：</span><span class="sxs-lookup"><span data-stu-id="5f90d-126">Insert the following code that saves changes into the `MainWindow` class:</span></span>

     [!code-csharp[Astoria Quickstart Client#SaveChanges](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_quickstart_client/cs/window1.xaml.cs#savechanges)]
     [!code-vb[Astoria Quickstart Client#SaveChanges](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_quickstart_client/vb/window1.xaml.vb#savechanges)]

## <a name="to-build-and-run-the-northwindclient-application"></a><span data-ttu-id="5f90d-127">生成并运行 NorthwindClient 应用程序</span><span class="sxs-lookup"><span data-stu-id="5f90d-127">To build and run the NorthwindClient application</span></span>

1. <span data-ttu-id="5f90d-128">在 **解决方案资源管理器** 中，右键单击 NorthwindClient 项目，然后选择 " **设为启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="5f90d-128">In **Solution Explorer**, right-click the NorthwindClient project and select **Set as startup project**.</span></span>

2. <span data-ttu-id="5f90d-129">按 **F5** 启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f90d-129">Press **F5** to start the application.</span></span>

     <span data-ttu-id="5f90d-130">这将生成解决方案并启动客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f90d-130">This builds the solution and starts the client application.</span></span> <span data-ttu-id="5f90d-131">将从服务请求数据并将其显示在控制台中。</span><span class="sxs-lookup"><span data-stu-id="5f90d-131">Data is requested from the service and displayed in the console.</span></span>

3. <span data-ttu-id="5f90d-132">编辑数据网格的 " **数量** " 列中的值，然后单击 " **保存**"。</span><span class="sxs-lookup"><span data-stu-id="5f90d-132">Edit a value in the **Quantity** column of the data grid, and then click **Save**.</span></span>

     <span data-ttu-id="5f90d-133">将更改保存到数据服务。</span><span class="sxs-lookup"><span data-stu-id="5f90d-133">Changes are saved to the data service.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f90d-134">此版本的 NorthwindClient 应用程序不支持添加和删除实体。</span><span class="sxs-lookup"><span data-stu-id="5f90d-134">This version of the NorthwindClient application does not support adding and deleting of entities.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5f90d-135">后续步骤</span><span class="sxs-lookup"><span data-stu-id="5f90d-135">Next Steps</span></span>

<span data-ttu-id="5f90d-136">你已成功创建了访问示例 Northwind OData 源的客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f90d-136">You have successfully created the client application that accesses the sample Northwind OData feed.</span></span> <span data-ttu-id="5f90d-137">你还完成了 WCF Data Services 快速入门！</span><span class="sxs-lookup"><span data-stu-id="5f90d-137">You've also completed the WCF Data Services quickstart!</span></span>

<span data-ttu-id="5f90d-138">有关从 .NET Framework 应用程序访问 OData 源的详细信息，请参阅 [WCF Data Services 客户端库](wcf-data-services-client-library.md)。</span><span class="sxs-lookup"><span data-stu-id="5f90d-138">For more information about accessing an OData feed from a .NET Framework application, see [WCF Data Services Client Library](wcf-data-services-client-library.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f90d-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f90d-139">See also</span></span>

- [<span data-ttu-id="5f90d-140">入门</span><span class="sxs-lookup"><span data-stu-id="5f90d-140">Getting Started</span></span>](getting-started-with-wcf-data-services.md)
- [<span data-ttu-id="5f90d-141">资源</span><span class="sxs-lookup"><span data-stu-id="5f90d-141">Resources</span></span>](wcf-data-services-resources.md)
