---
description: 详细了解： ASP.NET 应用程序中的 SqlDependency
title: ASP.NET 应用程序中的 SqlDependency
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ff226ce3-f6b5-47a1-8d22-dc78b67e07f5
ms.openlocfilehash: 686586af834884f97ff8e62fdc792b3cdc23f507
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767019"
---
# <a name="sqldependency-in-an-aspnet-application"></a><span data-ttu-id="ed283-103">ASP.NET 应用程序中的 SqlDependency</span><span class="sxs-lookup"><span data-stu-id="ed283-103">SqlDependency in an ASP.NET Application</span></span>

<span data-ttu-id="ed283-104">本节中的示例演示了如何通过利用 ASP.NET <xref:System.Web.Caching.SqlCacheDependency> 对象间接使用 <xref:System.Data.SqlClient.SqlDependency>。</span><span class="sxs-lookup"><span data-stu-id="ed283-104">The example in this section shows how to use <xref:System.Data.SqlClient.SqlDependency> indirectly by leveraging the ASP.NET <xref:System.Web.Caching.SqlCacheDependency> object.</span></span> <span data-ttu-id="ed283-105"><xref:System.Web.Caching.SqlCacheDependency> 对象使用 <xref:System.Data.SqlClient.SqlDependency> 侦听通知并正确更新缓存。</span><span class="sxs-lookup"><span data-stu-id="ed283-105">The <xref:System.Web.Caching.SqlCacheDependency> object uses a <xref:System.Data.SqlClient.SqlDependency> to listen for notifications and correctly update the cache.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed283-106">示例代码假定您已通过执行 [启用查询通知](enabling-query-notifications.md)中的脚本启用了查询通知。</span><span class="sxs-lookup"><span data-stu-id="ed283-106">The sample code assumes that you have enabled query notifications by executing the scripts in [Enabling Query Notifications](enabling-query-notifications.md).</span></span>  
  
## <a name="about-the-sample-application"></a><span data-ttu-id="ed283-107">关于示例应用程序</span><span class="sxs-lookup"><span data-stu-id="ed283-107">About the Sample Application</span></span>  

 <span data-ttu-id="ed283-108">示例应用程序使用单个 ASP.NET 网页在 <xref:System.Web.UI.WebControls.GridView> 控件中显示 AdventureWorks SQL Server 数据库中的产品信息。</span><span class="sxs-lookup"><span data-stu-id="ed283-108">The sample application uses a single ASP.NET Web page to display product information from the **AdventureWorks** SQL Server database in a <xref:System.Web.UI.WebControls.GridView> control.</span></span> <span data-ttu-id="ed283-109">页面加载完成后，代码会将当前时间写入 <xref:System.Web.UI.WebControls.Label> 控件。</span><span class="sxs-lookup"><span data-stu-id="ed283-109">When the page loads, the code writes the current time to a <xref:System.Web.UI.WebControls.Label> control.</span></span> <span data-ttu-id="ed283-110">然后，它定义一个 <xref:System.Web.Caching.SqlCacheDependency> 对象并设置 <xref:System.Web.Caching.Cache> 对象的属性，以存储最多三分钟的缓存数据。</span><span class="sxs-lookup"><span data-stu-id="ed283-110">It then defines a <xref:System.Web.Caching.SqlCacheDependency> object and sets properties on the <xref:System.Web.Caching.Cache> object to store the cache data for up to three minutes.</span></span> <span data-ttu-id="ed283-111">然后代码将连接到数据库并检索数据。</span><span class="sxs-lookup"><span data-stu-id="ed283-111">The code then connects to the database and retrieves the data.</span></span> <span data-ttu-id="ed283-112">当页面加载完成且应用程序运行时，ASP.NET 将从缓存中检索数据，如注意到页面上的时间未更改，则可以确认此情况。</span><span class="sxs-lookup"><span data-stu-id="ed283-112">When the page is loaded and the application is running ASP.NET will retrieve data from the cache, which you can verify by noting that the time on the page does not change.</span></span> <span data-ttu-id="ed283-113">如果受到监视的数据发生更改，ASP.NET 将使缓存失效，并在 `GridView` 控件中重新填充新数据，同时更新 `Label` 控件中显示的时间。</span><span class="sxs-lookup"><span data-stu-id="ed283-113">If the data being monitored changes, ASP.NET invalidates the cache and repopulate the `GridView` control with fresh data, updating the time displayed in the `Label` control.</span></span>  
  
## <a name="creating-the-sample-application"></a><span data-ttu-id="ed283-114">创建示例应用程序</span><span class="sxs-lookup"><span data-stu-id="ed283-114">Creating the Sample Application</span></span>  

 <span data-ttu-id="ed283-115">执行以下步骤以创建和运行示例应用程序：</span><span class="sxs-lookup"><span data-stu-id="ed283-115">Follow these steps to create and run the sample application:</span></span>  
  
1. <span data-ttu-id="ed283-116">创建新的 ASP.NET 网站。</span><span class="sxs-lookup"><span data-stu-id="ed283-116">Create a new ASP.NET Web site.</span></span>  
  
2. <span data-ttu-id="ed283-117">向 Default.aspx 页面添加 <xref:System.Web.UI.WebControls.Label> 和 <xref:System.Web.UI.WebControls.GridView> 控件。</span><span class="sxs-lookup"><span data-stu-id="ed283-117">Add a <xref:System.Web.UI.WebControls.Label> and a <xref:System.Web.UI.WebControls.GridView> control to the Default.aspx page.</span></span>  
  
3. <span data-ttu-id="ed283-118">打开页面的类模块并添加以下指令：</span><span class="sxs-lookup"><span data-stu-id="ed283-118">Open the page's class module and add the following directives:</span></span>  
  
    ```vb  
    Option Strict On  
    Option Explicit On  
  
    Imports System.Data.SqlClient  
    ```  
  
    ```csharp  
    using System.Data.SqlClient;  
    using System.Web.Caching;  
    ```  
  
4. <span data-ttu-id="ed283-119">在页面的 `Page_Load` 事件中添加以下代码：</span><span class="sxs-lookup"><span data-stu-id="ed283-119">Add the following code in the page's `Page_Load` event:</span></span>  
  
     [!code-csharp[DataWorks SqlDependency.AspNet#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/CS/Default.aspx.cs#1)]
     [!code-vb[DataWorks SqlDependency.AspNet#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/VB/Default.aspx.vb#1)]  
  
5. <span data-ttu-id="ed283-120">添加两个帮助程序方法：`GetConnectionString` 和 `GetSQL`。</span><span class="sxs-lookup"><span data-stu-id="ed283-120">Add two helper methods, `GetConnectionString` and `GetSQL`.</span></span> <span data-ttu-id="ed283-121">已定义的连接字符串使用集成安全性。</span><span class="sxs-lookup"><span data-stu-id="ed283-121">The connection string defined uses integrated security.</span></span> <span data-ttu-id="ed283-122">你将需要验证所使用的帐户是否具有必要的数据库权限，并且示例数据库 AdventureWorks 是否启用了通知。</span><span class="sxs-lookup"><span data-stu-id="ed283-122">You will need to verify that the account you are using has the necessary database permissions and that the sample database, **AdventureWorks**, has notifications enabled.</span></span>
  
     [!code-csharp[DataWorks SqlDependency.AspNet#2](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/CS/Default.aspx.cs#2)]
     [!code-vb[DataWorks SqlDependency.AspNet#2](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/VB/Default.aspx.vb#2)]  
  
### <a name="testing-the-application"></a><span data-ttu-id="ed283-123">测试应用程序</span><span class="sxs-lookup"><span data-stu-id="ed283-123">Testing the Application</span></span>  

 <span data-ttu-id="ed283-124">应用程序会缓存 Web 窗体上显示的数据，在没有任何活动的情况下，每三分钟刷新一次数据。</span><span class="sxs-lookup"><span data-stu-id="ed283-124">The application caches the data displayed on the Web form and refreshes it every three minutes if there is no activity.</span></span> <span data-ttu-id="ed283-125">如果数据库发生了更改，则立即刷新缓存。</span><span class="sxs-lookup"><span data-stu-id="ed283-125">If a change occurs to the database, the cache is refreshed immediately.</span></span> <span data-ttu-id="ed283-126">从 Visual Studio 中运行应用程序，这样会将页面加载到浏览器中。</span><span class="sxs-lookup"><span data-stu-id="ed283-126">Run the application from Visual Studio, which loads the page into the browser.</span></span> <span data-ttu-id="ed283-127">显示的缓存刷新时间指示上次刷新缓存的时间。</span><span class="sxs-lookup"><span data-stu-id="ed283-127">The cache refresh time displayed indicates when the cache was last refreshed.</span></span> <span data-ttu-id="ed283-128">等待三分钟，然后刷新页面，从而导致发生回发事件。</span><span class="sxs-lookup"><span data-stu-id="ed283-128">Wait three minutes, and then refresh the page, causing a postback event to occur.</span></span> <span data-ttu-id="ed283-129">请注意，页面上显示的时间已更改。</span><span class="sxs-lookup"><span data-stu-id="ed283-129">Note that the time displayed on the page has changed.</span></span> <span data-ttu-id="ed283-130">如果在不到三分钟的时间内刷新页面，则页面上显示的时间将保持不变。</span><span class="sxs-lookup"><span data-stu-id="ed283-130">If you refresh the page in less than three minutes, the time displayed on the page will remain the same.</span></span>  
  
 <span data-ttu-id="ed283-131">现在，使用 Transact-SQL UPDATE 命令更新数据库中的数据并刷新页面。</span><span class="sxs-lookup"><span data-stu-id="ed283-131">Now update the data in the database, using a Transact-SQL UPDATE command and refresh the page.</span></span> <span data-ttu-id="ed283-132">此时显示的时间表示已使用数据库中的新数据刷新缓存。</span><span class="sxs-lookup"><span data-stu-id="ed283-132">The time displayed now indicates that the cache was refreshed with the new data from the database.</span></span> <span data-ttu-id="ed283-133">请注意，尽管缓存已更新，但在回发事件发生之前，页面上显示的时间不会更改。</span><span class="sxs-lookup"><span data-stu-id="ed283-133">Note that although the cache is updated, the time displayed on the page does not change until a postback event occurs.</span></span>  

## <a name="distributed-cache-synchronization-using-sql-dependency"></a><span data-ttu-id="ed283-134">使用 SQL 依赖关系的分布式缓存同步</span><span class="sxs-lookup"><span data-stu-id="ed283-134">Distributed cache synchronization using SQL Dependency</span></span>

<span data-ttu-id="ed283-135">某些第三方分布式缓存（如 [NCache](https://www.alachisoft.com/ncache) ）提供了对使用 [sql 依赖关系](https://www.alachisoft.com/resources/docs/ncache/prog-guide/sql-dependency.html)同步 SQL 数据库和缓存的支持。</span><span class="sxs-lookup"><span data-stu-id="ed283-135">Some of the third-party distributed caches such as [NCache](https://www.alachisoft.com/ncache) provide support to synchronize the SQL database and cache using [SQL Dependency](https://www.alachisoft.com/resources/docs/ncache/prog-guide/sql-dependency.html).</span></span> <span data-ttu-id="ed283-136">有关源代码实现的详细信息和示例，请参阅 [分布式缓存 SQL 依赖项示例](https://github.com/Alachisoft/NCache-Samples/tree/master/dotnet/Dependencies/SQLDependency)。</span><span class="sxs-lookup"><span data-stu-id="ed283-136">For more information and an example source code implementation, see [Distributed cache SQL Dependency sample](https://github.com/Alachisoft/NCache-Samples/tree/master/dotnet/Dependencies/SQLDependency).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed283-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed283-137">See also</span></span>

- [<span data-ttu-id="ed283-138">SQL Server 中的查询通知</span><span class="sxs-lookup"><span data-stu-id="ed283-138">Query Notifications in SQL Server</span></span>](query-notifications-in-sql-server.md)
- [<span data-ttu-id="ed283-139">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="ed283-139">ADO.NET Overview</span></span>](../ado-net-overview.md)
