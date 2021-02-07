---
description: 了解详细信息：使用 SqlNotificationRequest 执行 SqlCommand
title: 使用 SqlNotificationRequest 执行 SqlCommand
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1776f48f-9bea-41f6-83a4-c990c7a2c991
ms.openlocfilehash: d3e82022794aa67d4bd20223cac852097f2be9dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767045"
---
# <a name="sqlcommand-execution-with-a-sqlnotificationrequest"></a><span data-ttu-id="76b7f-103">使用 SqlNotificationRequest 执行 SqlCommand</span><span class="sxs-lookup"><span data-stu-id="76b7f-103">SqlCommand Execution with a SqlNotificationRequest</span></span>

<span data-ttu-id="76b7f-104">可以将 <xref:System.Data.SqlClient.SqlCommand> 配置为在数据从服务器中提取后发生更改时生成通知，如果再次执行查询，结果集将不同。</span><span class="sxs-lookup"><span data-stu-id="76b7f-104">A <xref:System.Data.SqlClient.SqlCommand> can be configured to generate a notification when data changes after it has been fetched from the server and the result set would be different if the query were executed again.</span></span> <span data-ttu-id="76b7f-105">这对于以下情况非常有用：你希望在服务器上使用自定义通知队列，或者不希望维护活动对象的情况。</span><span class="sxs-lookup"><span data-stu-id="76b7f-105">This is useful for scenarios where you want to use custom notification queues on the server or when you do not want to maintain live objects.</span></span>

## <a name="creating-the-notification-request"></a><span data-ttu-id="76b7f-106">创建通知请求</span><span class="sxs-lookup"><span data-stu-id="76b7f-106">Creating the Notification Request</span></span>

<span data-ttu-id="76b7f-107">可以使用 <xref:System.Data.Sql.SqlNotificationRequest> 对象，通过将通知请求绑定到 `SqlCommand` 对象来创建请求。</span><span class="sxs-lookup"><span data-stu-id="76b7f-107">You can use a <xref:System.Data.Sql.SqlNotificationRequest> object to create the notification request by binding it to a `SqlCommand` object.</span></span> <span data-ttu-id="76b7f-108">创建请求后，你将不再需要 `SqlNotificationRequest` 对象。</span><span class="sxs-lookup"><span data-stu-id="76b7f-108">Once the request is created, you no longer need the `SqlNotificationRequest` object.</span></span> <span data-ttu-id="76b7f-109">可以在队列中查询任何通知，并做出相应响应。</span><span class="sxs-lookup"><span data-stu-id="76b7f-109">You can query the queue for any notifications and respond appropriately.</span></span> <span data-ttu-id="76b7f-110">即使应用程序关闭后重新启动，也会出现通知。</span><span class="sxs-lookup"><span data-stu-id="76b7f-110">Notifications can occur even if the application is shut down and subsequently restarted.</span></span>

<span data-ttu-id="76b7f-111">在对关联通知执行命令时，对原始结果集所做的任何更改都会触发向在通知请求中配置的 SQL Server 队列发送消息。</span><span class="sxs-lookup"><span data-stu-id="76b7f-111">When the command with the associated notification is executed, any changes to the original result set trigger sending a message to the SQL Server queue that was configured in the notification request.</span></span>

<span data-ttu-id="76b7f-112">如何轮询 SQL Server 队列和解释该消息是应用程序特定的。</span><span class="sxs-lookup"><span data-stu-id="76b7f-112">How you poll the SQL Server queue and interpret the message is specific to your application.</span></span> <span data-ttu-id="76b7f-113">应用程序负责轮询队列并根据消息的内容做出响应。</span><span class="sxs-lookup"><span data-stu-id="76b7f-113">The application is responsible for polling the queue and reacting based on the contents of the message.</span></span>

> [!NOTE]
> <span data-ttu-id="76b7f-114">在 <xref:System.Data.SqlClient.SqlDependency> 中使用 SQL Server 通知请求时，请创建自己的队列名称，而不是使用默认的服务名称。</span><span class="sxs-lookup"><span data-stu-id="76b7f-114">When using SQL Server notification requests with <xref:System.Data.SqlClient.SqlDependency>, create your own queue name instead of using the default service name.</span></span>

<span data-ttu-id="76b7f-115"><xref:System.Data.Sql.SqlNotificationRequest> 没有新的客户端安全元素。</span><span class="sxs-lookup"><span data-stu-id="76b7f-115">There are no new client-side security elements for <xref:System.Data.Sql.SqlNotificationRequest>.</span></span> <span data-ttu-id="76b7f-116">这主要是一种服务器功能，并且服务器已创建用户必须拥有的用于请求通知的特殊权限。</span><span class="sxs-lookup"><span data-stu-id="76b7f-116">This is primarily a server feature, and the server has created special privileges that users must have to request a notification.</span></span>

### <a name="example"></a><span data-ttu-id="76b7f-117">示例</span><span class="sxs-lookup"><span data-stu-id="76b7f-117">Example</span></span>

<span data-ttu-id="76b7f-118">下面的代码段演示如何创建 <xref:System.Data.Sql.SqlNotificationRequest> 并将其与 <xref:System.Data.SqlClient.SqlCommand> 相关联。</span><span class="sxs-lookup"><span data-stu-id="76b7f-118">The following code fragment demonstrates how to create a <xref:System.Data.Sql.SqlNotificationRequest> and associate it with a <xref:System.Data.SqlClient.SqlCommand>.</span></span>

```vb
' Assume connection is an open SqlConnection.
' Create a new SqlCommand object.
Dim command As New SqlCommand( _
  "SELECT ShipperID, CompanyName, Phone FROM dbo.Shippers", connection)

' Create a SqlNotificationRequest object.
Dim notifcationRequest As New SqlNotificationRequest()
notificationRequest.id = "NotificationID"
notificationRequest.Service = "mySSBQueue"

' Associate the notification request with the command.
command.Notification = notificationRequest
' Execute the command.
command.ExecuteReader()
' Process the DataReader.
' You can use Transact-SQL syntax to periodically poll the
' SQL Server queue to see if you have a new message.
```

```csharp
// Assume connection is an open SqlConnection.
// Create a new SqlCommand object.
SqlCommand command=new SqlCommand(
 "SELECT ShipperID, CompanyName, Phone FROM dbo.Shippers", connection);

// Create a SqlNotificationRequest object.
SqlNotificationRequest notificationRequest=new SqlNotificationRequest();
notificationRequest.id="NotificationID";
notificationRequest.Service="mySSBQueue";

// Associate the notification request with the command.
command.Notification=notificationRequest;
// Execute the command.
command.ExecuteReader();
// Process the DataReader.
// You can use Transact-SQL syntax to periodically poll the
// SQL Server queue to see if you have a new message.
```

## <a name="see-also"></a><span data-ttu-id="76b7f-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="76b7f-119">See also</span></span>

- [<span data-ttu-id="76b7f-120">SQL Server 中的查询通知</span><span class="sxs-lookup"><span data-stu-id="76b7f-120">Query Notifications in SQL Server</span></span>](query-notifications-in-sql-server.md)
- [<span data-ttu-id="76b7f-121">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="76b7f-121">ADO.NET Overview</span></span>](../ado-net-overview.md)
