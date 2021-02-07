---
description: 了解详细信息： SqlClient 对 LocalDB 的支持
title: SqlClient 对 LocalDB 的支持
ms.date: 03/30/2017
ms.assetid: cf796898-5575-46f2-ae6e-21e5aa8c4123
ms.openlocfilehash: f99c46277638c810c91f7ceffd0e47c896125c63
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767162"
---
# <a name="sqlclient-support-for-localdb"></a><span data-ttu-id="00e4e-103">SqlClient 对 LocalDB 的支持</span><span class="sxs-lookup"><span data-stu-id="00e4e-103">SqlClient Support for LocalDB</span></span>

<span data-ttu-id="00e4e-104">本文讨论如何连接到 LocalDB 数据库。</span><span class="sxs-lookup"><span data-stu-id="00e4e-104">This article discusses how to connect to a LocalDB database.</span></span> <span data-ttu-id="00e4e-105">LocalDB 是 SQL Server 的轻型版本。</span><span class="sxs-lookup"><span data-stu-id="00e4e-105">LocalDB is a lightweight version of SQL Server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00e4e-106">备注</span><span class="sxs-lookup"><span data-stu-id="00e4e-106">Remarks</span></span>
  
 <span data-ttu-id="00e4e-107">若要汇总可通过 LocalDB 执行的操作：</span><span class="sxs-lookup"><span data-stu-id="00e4e-107">To summarize what you can do with LocalDB:</span></span>  
  
- <span data-ttu-id="00e4e-108">使用 sqllocaldb 或 app.config 文件创建和启动 LocalDB 实例。</span><span class="sxs-lookup"><span data-stu-id="00e4e-108">Create and start LocalDB instances with sqllocaldb.exe or your app.config file.</span></span>  
  
- <span data-ttu-id="00e4e-109">使用 sqlcmd.exe 添加和修改 LocalDB 实例中的数据库。</span><span class="sxs-lookup"><span data-stu-id="00e4e-109">Use sqlcmd.exe to add and modify databases in a LocalDB instance.</span></span> <span data-ttu-id="00e4e-110">例如，`sqlcmd -S (localdb)\myinst`。</span><span class="sxs-lookup"><span data-stu-id="00e4e-110">For example, `sqlcmd -S (localdb)\myinst`.</span></span>  
  
- <span data-ttu-id="00e4e-111">使用 `AttachDBFilename` 连接字符串关键字将数据库添加到 LocalDB 实例。</span><span class="sxs-lookup"><span data-stu-id="00e4e-111">Use the `AttachDBFilename` connection string keyword to add a database to your LocalDB instance.</span></span> <span data-ttu-id="00e4e-112">在使用 `AttachDBFilename` 时，如果你没有使用 `Database` 连接字符串关键字指定数据库的名称，则在应用程序关闭时，将从 LocalDB 实例中删除该数据库。</span><span class="sxs-lookup"><span data-stu-id="00e4e-112">When using `AttachDBFilename`, if you do not specify the name of the database with the `Database` connection string keyword, the database will be removed from the LocalDB instance when the application closes.</span></span>  
  
- <span data-ttu-id="00e4e-113">在连接字符串中指定 LocalDB 实例。</span><span class="sxs-lookup"><span data-stu-id="00e4e-113">Specify a LocalDB instance in your connection string.</span></span> <span data-ttu-id="00e4e-114">例如，实例名称为 `myInstance`，连接字符串将包括：</span><span class="sxs-lookup"><span data-stu-id="00e4e-114">For example, your instance name is `myInstance`, the connection string would include:</span></span>  
  
    `server=(localdb)\\myInstance`  
  
 <span data-ttu-id="00e4e-115">连接到 LocalDB 数据库时不允许使用 `User Instance=True`。</span><span class="sxs-lookup"><span data-stu-id="00e4e-115">`User Instance=True` is not allowed when connecting to a LocalDB database.</span></span>  
  
<span data-ttu-id="00e4e-116">有关安装 LocalDB 的详细信息，请参阅 [SQL Server Express localdb](/sql/database-engine/configure-windows/sql-server-express-localdb)。</span><span class="sxs-lookup"><span data-stu-id="00e4e-116">For information about installing LocalDB, see [SQL Server Express LocalDB](/sql/database-engine/configure-windows/sql-server-express-localdb).</span></span>
  
## <a name="programmatically-create-a-named-instance"></a><span data-ttu-id="00e4e-117">以编程方式创建命名实例</span><span class="sxs-lookup"><span data-stu-id="00e4e-117">Programmatically Create a Named Instance</span></span>  

 <span data-ttu-id="00e4e-118">应用程序可以创建命名实例并指定数据库，如下所示：</span><span class="sxs-lookup"><span data-stu-id="00e4e-118">An application can create a named instance and specify a database as follows:</span></span>  
  
- <span data-ttu-id="00e4e-119">在 app.config 文件中指定要创建的 LocalDB 实例，如下所示。</span><span class="sxs-lookup"><span data-stu-id="00e4e-119">Specify the LocalDB instances to create in the app.config file, as follows.</span></span>  <span data-ttu-id="00e4e-120">实例的版本号应与 LocalDB 安装的版本号相同。</span><span class="sxs-lookup"><span data-stu-id="00e4e-120">The version number of the instance should be the same as the version number of your LocalDB installation.</span></span>  
  
    ```xml  
    <?xml version="1.0" encoding="utf-8" ?>  
    <configuration>  
      <configSections>  
        <section  
        name="system.data.localdb"  
        type="System.Data.LocalDBConfigurationSection,System.Data,Version=4.0.0.0,Culture=neutral,PublicKeyToken=b77a5c561934e089"/>  
      </configSections>  
      <system.data.localdb>  
        <localdbinstances>  
          <add name="myInstance" version="11.0" />  
        </localdbinstances>  
      </system.data.localdb>  
    </configuration>  
    ```  
  
- <span data-ttu-id="00e4e-121">使用 `server` 连接字符串关键字指定实例的名称。</span><span class="sxs-lookup"><span data-stu-id="00e4e-121">Specify the name of the instance using the `server` connection string keyword.</span></span>  <span data-ttu-id="00e4e-122">`server` 连接字符串关键字中指定的实例名称必须与 app.config 文件中指定的名称匹配。</span><span class="sxs-lookup"><span data-stu-id="00e4e-122">The instance name specified in the `server` connection string keyword must match the name specified in the app.config file.</span></span>  
  
- <span data-ttu-id="00e4e-123">使用 `AttachDBFilename` 连接字符串关键字来指定 .MDF 文件。</span><span class="sxs-lookup"><span data-stu-id="00e4e-123">Use the `AttachDBFilename` connection string keyword to specify the .MDF file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00e4e-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="00e4e-124">See also</span></span>

- [<span data-ttu-id="00e4e-125">SQL Server 功能和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="00e4e-125">SQL Server Features and ADO.NET</span></span>](sql-server-features-and-adonet.md)
- [<span data-ttu-id="00e4e-126">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="00e4e-126">ADO.NET Overview</span></span>](../ado-net-overview.md)
