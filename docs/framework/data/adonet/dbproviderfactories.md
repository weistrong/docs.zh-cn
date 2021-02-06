---
description: 了解详细信息： DbProviderFactories
title: DbProviderFactories
ms.date: 03/30/2017
ms.assetid: 2a8e2640-3a49-42a1-a3a9-b43026907ae1
ms.openlocfilehash: 735c78a846fc8df31a922acf90e587c6d96f4995
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651257"
---
# <a name="dbproviderfactories"></a><span data-ttu-id="f17f0-103">DbProviderFactories</span><span class="sxs-lookup"><span data-stu-id="f17f0-103">DbProviderFactories</span></span>

<span data-ttu-id="f17f0-104"><xref:System.Data.Common> 命名空间提供用于创建与特定数据源一起使用的 <xref:System.Data.Common.DbProviderFactory> 实例的类。</span><span class="sxs-lookup"><span data-stu-id="f17f0-104">The <xref:System.Data.Common> namespace provides classes for creating <xref:System.Data.Common.DbProviderFactory> instances to work with specific data sources.</span></span> <span data-ttu-id="f17f0-105">当创建 <xref:System.Data.Common.DbProviderFactory> 实例并向其传递有关数据提供程序的信息时，`DbProviderFactory` 可以根据为其提供的信息确定要返回的正确的强类型连接对象。</span><span class="sxs-lookup"><span data-stu-id="f17f0-105">When you create a <xref:System.Data.Common.DbProviderFactory> instance and pass it information about the data provider, the `DbProviderFactory` can determine the correct, strongly typed connection object to return based on the information it has been provided.</span></span>  
  
 <span data-ttu-id="f17f0-106">从 .NET Framework 4 开始，machine.config 文件中不再列出诸如 <xref:System.Data.Odbc>、<xref:System.Data.OleDb>、<xref:System.Data.SqlClient> 和 <xref:System.Data.OracleClient> 等数据提供程序，但会继续列出自定义提供程序。</span><span class="sxs-lookup"><span data-stu-id="f17f0-106">Beginning in the .NET Framework version 4, data providers such as <xref:System.Data.Odbc>, <xref:System.Data.OleDb>, <xref:System.Data.SqlClient>, and <xref:System.Data.OracleClient> are no longer listed in machine.config file, but custom providers will continue to be listed there.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f17f0-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="f17f0-107">In This Section</span></span>  

 [<span data-ttu-id="f17f0-108">工厂模型概述</span><span class="sxs-lookup"><span data-stu-id="f17f0-108">Factory Model Overview</span></span>](factory-model-overview.md)  
 <span data-ttu-id="f17f0-109">提供工厂设计样式和编程接口概述。</span><span class="sxs-lookup"><span data-stu-id="f17f0-109">Provides an overview of the factory design pattern and programming interface.</span></span>  
  
 [<span data-ttu-id="f17f0-110">获取 DbProviderFactory</span><span class="sxs-lookup"><span data-stu-id="f17f0-110">Obtaining a DbProviderFactory</span></span>](obtaining-a-dbproviderfactory.md)  
 <span data-ttu-id="f17f0-111">演示如何列出安装的数据提供程序以及如何从 <xref:System.Data.Common.DbConnection> 创建 `DbProviderFactory`。</span><span class="sxs-lookup"><span data-stu-id="f17f0-111">Demonstrates how to list the installed data providers and create a <xref:System.Data.Common.DbConnection> from a `DbProviderFactory`.</span></span>  
  
 [<span data-ttu-id="f17f0-112">DbConnection、DbCommand 和 DbException</span><span class="sxs-lookup"><span data-stu-id="f17f0-112">DbConnection, DbCommand and DbException</span></span>](dbconnection-dbcommand-and-dbexception.md)  
 <span data-ttu-id="f17f0-113">演示如何创建 <xref:System.Data.Common.DbCommand> 和 <xref:System.Data.Common.DbDataReader>，以及如何使用 <xref:System.Data.Common.DbException> 处理数据错误。</span><span class="sxs-lookup"><span data-stu-id="f17f0-113">Demonstrates how to create a <xref:System.Data.Common.DbCommand> and <xref:System.Data.Common.DbDataReader>, and how to handle data errors using <xref:System.Data.Common.DbException>.</span></span>  
  
 [<span data-ttu-id="f17f0-114">使用 DbDataAdapter 修改数据</span><span class="sxs-lookup"><span data-stu-id="f17f0-114">Modifying Data with a DbDataAdapter</span></span>](modifying-data-with-a-dbdataadapter.md)  
 <span data-ttu-id="f17f0-115">演示如何使用 <xref:System.Data.Common.DbCommandBuilder> 和 <xref:System.Data.Common.DbDataAdapter> 检索并修改数据。</span><span class="sxs-lookup"><span data-stu-id="f17f0-115">Demonstrates how to use a <xref:System.Data.Common.DbCommandBuilder> with a <xref:System.Data.Common.DbDataAdapter> to retrieve and modify data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f17f0-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f17f0-116">See also</span></span>

- [<span data-ttu-id="f17f0-117">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="f17f0-117">Retrieving and Modifying Data in ADO.NET</span></span>](retrieving-and-modifying-data.md)
- [<span data-ttu-id="f17f0-118">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="f17f0-118">ADO.NET Overview</span></span>](ado-net-overview.md)
