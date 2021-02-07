---
description: 了解详细信息：使用命令修改数据
title: 使用命令修改数据
ms.date: 03/30/2017
ms.assetid: f4160389-b9ff-4b74-b655-437c76dcd586
ms.openlocfilehash: 3addcb93850aa8e26fe441b5c859502779433bfb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766551"
---
# <a name="using-commands-to-modify-data"></a><span data-ttu-id="c2d4d-103">使用命令修改数据</span><span class="sxs-lookup"><span data-stu-id="c2d4d-103">Using Commands to Modify Data</span></span>

<span data-ttu-id="c2d4d-104">使用 .NET Framework 数据提供程序，您可以执行存储过程或数据定义语言语句（如 CREATE TABLE 和 ALTER COLUMN）来对数据库或编录执行架构处理。</span><span class="sxs-lookup"><span data-stu-id="c2d4d-104">Using a .NET Framework data provider, you can execute stored procedures or data definition language statements (for example, CREATE TABLE and ALTER COLUMN) to perform schema manipulation on a database or catalog.</span></span> <span data-ttu-id="c2d4d-105">这些命令不会像查询那样返回行，因此 **Command** 对象提供 **ExecuteNonQuery** 来处理它们。</span><span class="sxs-lookup"><span data-stu-id="c2d4d-105">These commands do not return rows as a query would, so the **Command** object provides an **ExecuteNonQuery** to process them.</span></span>  
  
 <span data-ttu-id="c2d4d-106">除了使用 ExecuteNonQuery 来修改架构之外，还可以使用此方法处理那些修改数据但不返回行的 SQL 语句，如 INSERT、UPDATE 和 DELETE。</span><span class="sxs-lookup"><span data-stu-id="c2d4d-106">In addition to using **ExecuteNonQuery** to modify schema, you can also use this method to process SQL statements that modify data but that do not return rows, such as INSERT, UPDATE, and DELETE.</span></span>  
  
 <span data-ttu-id="c2d4d-107">虽然行不是由 ExecuteNonQuery 方法返回的，但可以通过 Command 对象的 Parameters 集合来传递和返回输入和输出参数以及返回值。</span><span class="sxs-lookup"><span data-stu-id="c2d4d-107">Although rows are not returned by the **ExecuteNonQuery** method, input and output parameters and return values can be passed and returned via the **Parameters** collection of the **Command** object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c2d4d-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="c2d4d-108">In This Section</span></span>  

 [<span data-ttu-id="c2d4d-109">更新数据源中的数据</span><span class="sxs-lookup"><span data-stu-id="c2d4d-109">Updating Data in a Data Source</span></span>](updating-data-in-a-data-source.md)  
 <span data-ttu-id="c2d4d-110">描述如何执行对数据库中的数据进行修改的命令或存储过程。</span><span class="sxs-lookup"><span data-stu-id="c2d4d-110">Describes how to execute commands or stored procedures that modify data in a database.</span></span>  
  
 [<span data-ttu-id="c2d4d-111">执行目录操作</span><span class="sxs-lookup"><span data-stu-id="c2d4d-111">Performing Catalog Operations</span></span>](performing-catalog-operations.md)  
 <span data-ttu-id="c2d4d-112">描述如何执行对数据库架构进行修改的命令。</span><span class="sxs-lookup"><span data-stu-id="c2d4d-112">Describes how to execute commands that modify database schema.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2d4d-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2d4d-113">See also</span></span>

- [<span data-ttu-id="c2d4d-114">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="c2d4d-114">Retrieving and Modifying Data in ADO.NET</span></span>](retrieving-and-modifying-data.md)
- [<span data-ttu-id="c2d4d-115">命令和参数</span><span class="sxs-lookup"><span data-stu-id="c2d4d-115">Commands and Parameters</span></span>](commands-and-parameters.md)
- [<span data-ttu-id="c2d4d-116">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="c2d4d-116">ADO.NET Overview</span></span>](ado-net-overview.md)
