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
# <a name="quickstart-wcf-data-services"></a>快速入门（WCF 数据服务）

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

本快速入门帮助你熟悉 WCF Data Services 和 Open Data Protocol (OData) 通过一系列支持 [入门](getting-started-with-wcf-data-services.md)中的主题的任务。

## <a name="what-youll-learn"></a>学习内容

本快速入门中的第一项任务介绍如何创建数据服务以公开 Northwind 示例数据库中的 OData 数据源。 在后面的主题中，你将使用 Web 浏览器访问 OData 源，并使用客户端库创建使用 OData 源的 Windows Presentation Foundation (WPF) 客户端应用程序。

## <a name="prerequisites"></a>先决条件

若要完成本快速入门教程，请安装以下组件：

- Visual Studio

- SQL Server 的实例。 这包括默认安装的 Visual Studio 2015 或更高版本2017中的 **数据存储和处理** 工作负荷的一部分 SQL Server Express。

- Northwind 示例数据库。 若要安装数据库，请从 [Northwind 和 pubs 示例数据库](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)运行 transact-sql 脚本，以 Microsoft SQL Server。

## <a name="wcf-data-services-quickstart-tasks"></a>WCF 数据服务快速入门任务

 [创建数据服务](creating-the-data-service.md)

 定义 ASP.NET 应用程序，定义数据模型，创建数据服务，并启用对资源的访问。

 [从 Web 浏览器访问服务](accessing-the-service-from-a-web-browser-wcf-data-services-quickstart.md)

 通过 Visual Studio 启动服务，并通过 Web 浏览器向公开的源提交 HTTP GET 请求以访问该服务。

 [创建 .NET Framework 客户端应用程序](creating-the-dotnet-client-application-wcf-data-services-quickstart.md)

 创建一个使用 OData 源的 WPF 应用程序，将数据绑定到 Windows 控件，在绑定控件中更改数据，然后将更改发送回数据服务。

> [!NOTE]
> 可以从 [GitHub](https://github.com/microsoftarchive/msdn-code-gallery-community-s-z/tree/master/WCF%20Data%20Services%20Quickstart%20(OData%20Service%20and%20WPF%20Client))下载完整版本的快速入门中的项目文件。

## <a name="next-steps"></a>后续步骤

> [!div class="nextstepaction"]
> [启动快速入门](creating-the-data-service.md)

## <a name="see-also"></a>请参阅

- [ADO.NET 实体框架](../adonet/ef/index.md)
