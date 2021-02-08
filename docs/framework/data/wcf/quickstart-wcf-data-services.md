---
description: '了解详细信息：快速入门 (WCF Data Services) '
title: 快速入门（WCF 数据服务）
ms.date: 08/24/2018
helpviewer_keywords:
- WCF Data Services, quick-start example
- WCF Data Services, Entity Data Model (EDM) service
ms.assetid: 7b18ca1e-d4d6-4c7a-afb9-ce3cebb98a8d
ms.openlocfilehash: 92a1b8882f6a7db2ed33f032ad434efd06400421
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794944"
---
# <a name="quickstart-wcf-data-services"></a><span data-ttu-id="d55f3-103">快速入门（WCF 数据服务）</span><span class="sxs-lookup"><span data-stu-id="d55f3-103">Quickstart (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="d55f3-104">本快速入门帮助你熟悉 WCF Data Services 和 Open Data Protocol (OData) 通过一系列支持 [入门](getting-started-with-wcf-data-services.md)中的主题的任务。</span><span class="sxs-lookup"><span data-stu-id="d55f3-104">This quickstart helps you become familiar with WCF Data Services and the Open Data Protocol (OData) through a series of tasks that support the topics in [Getting Started](getting-started-with-wcf-data-services.md).</span></span>

## <a name="what-youll-learn"></a><span data-ttu-id="d55f3-105">学习内容</span><span class="sxs-lookup"><span data-stu-id="d55f3-105">What you'll learn</span></span>

<span data-ttu-id="d55f3-106">本快速入门中的第一项任务介绍如何创建数据服务以公开 Northwind 示例数据库中的 OData 数据源。</span><span class="sxs-lookup"><span data-stu-id="d55f3-106">The first task in this quickstart shows how to create a data service to expose an OData feed from the Northwind sample database.</span></span> <span data-ttu-id="d55f3-107">在后面的主题中，你将使用 Web 浏览器访问 OData 源，并使用客户端库创建使用 OData 源的 Windows Presentation Foundation (WPF) 客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="d55f3-107">In later topics, you will access the OData feed by using a Web browser, and also create a Windows Presentation Foundation (WPF) client application that consumes the OData feed by using client libraries.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d55f3-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="d55f3-108">Prerequisites</span></span>

<span data-ttu-id="d55f3-109">若要完成本快速入门教程，请安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="d55f3-109">To complete this quickstart, install the following components:</span></span>

- <span data-ttu-id="d55f3-110">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d55f3-110">Visual Studio</span></span>

- <span data-ttu-id="d55f3-111">SQL Server 的实例。</span><span class="sxs-lookup"><span data-stu-id="d55f3-111">An instance of SQL Server.</span></span> <span data-ttu-id="d55f3-112">这包括默认安装的 Visual Studio 2015 或更高版本2017中的 **数据存储和处理** 工作负荷的一部分 SQL Server Express。</span><span class="sxs-lookup"><span data-stu-id="d55f3-112">This includes SQL Server Express, which is included in a default installation of Visual Studio 2015, or as part of the **Data storage and processing** workload in Visual Studio 2017 or later.</span></span>

- <span data-ttu-id="d55f3-113">Northwind 示例数据库。</span><span class="sxs-lookup"><span data-stu-id="d55f3-113">The Northwind sample database.</span></span> <span data-ttu-id="d55f3-114">若要安装数据库，请从 [Northwind 和 pubs 示例数据库](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)运行 transact-sql 脚本，以 Microsoft SQL Server。</span><span class="sxs-lookup"><span data-stu-id="d55f3-114">To install the database, run the Transact-SQL script from [Northwind and pubs sample databases for Microsoft SQL Server](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs).</span></span>

## <a name="wcf-data-services-quickstart-tasks"></a><span data-ttu-id="d55f3-115">WCF 数据服务快速入门任务</span><span class="sxs-lookup"><span data-stu-id="d55f3-115">WCF data services quickstart tasks</span></span>

 [<span data-ttu-id="d55f3-116">创建数据服务</span><span class="sxs-lookup"><span data-stu-id="d55f3-116">Create the Data Service</span></span>](creating-the-data-service.md)

 <span data-ttu-id="d55f3-117">定义 ASP.NET 应用程序，定义数据模型，创建数据服务，并启用对资源的访问。</span><span class="sxs-lookup"><span data-stu-id="d55f3-117">Define the ASP.NET application, define the data model, create the data service, and enable access to resources.</span></span>

 [<span data-ttu-id="d55f3-118">从 Web 浏览器访问服务</span><span class="sxs-lookup"><span data-stu-id="d55f3-118">Access the Service from a Web Browser</span></span>](accessing-the-service-from-a-web-browser-wcf-data-services-quickstart.md)

 <span data-ttu-id="d55f3-119">通过 Visual Studio 启动服务，并通过 Web 浏览器向公开的源提交 HTTP GET 请求以访问该服务。</span><span class="sxs-lookup"><span data-stu-id="d55f3-119">Start the service from Visual Studio and access the service by submitting HTTP GET requests through a Web browser to the exposed feed.</span></span>

 [<span data-ttu-id="d55f3-120">创建 .NET Framework 客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="d55f3-120">Create the .NET Framework Client Application</span></span>](creating-the-dotnet-client-application-wcf-data-services-quickstart.md)

 <span data-ttu-id="d55f3-121">创建一个使用 OData 源的 WPF 应用程序，将数据绑定到 Windows 控件，在绑定控件中更改数据，然后将更改发送回数据服务。</span><span class="sxs-lookup"><span data-stu-id="d55f3-121">Create a WPF app to consume the OData feed, bind data to Windows controls, change data in the bound controls, and then send the changes back to the data service.</span></span>

> [!NOTE]
> <span data-ttu-id="d55f3-122">可以从 [GitHub](https://github.com/microsoftarchive/msdn-code-gallery-community-s-z/tree/master/WCF%20Data%20Services%20Quickstart%20(OData%20Service%20and%20WPF%20Client))下载完整版本的快速入门中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="d55f3-122">Project files from a completed version of the quickstart can be downloaded from [GitHub](https://github.com/microsoftarchive/msdn-code-gallery-community-s-z/tree/master/WCF%20Data%20Services%20Quickstart%20(OData%20Service%20and%20WPF%20Client)).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d55f3-123">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d55f3-123">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d55f3-124">启动快速入门</span><span class="sxs-lookup"><span data-stu-id="d55f3-124">Start the quickstart</span></span>](creating-the-data-service.md)

## <a name="see-also"></a><span data-ttu-id="d55f3-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="d55f3-125">See also</span></span>

- [<span data-ttu-id="d55f3-126">ADO.NET 实体框架</span><span class="sxs-lookup"><span data-stu-id="d55f3-126">ADO.NET Entity Framework</span></span>](../adonet/ef/index.md)
