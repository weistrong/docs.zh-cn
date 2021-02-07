---
description: 了解详细信息： SQL Server 二进制文件和 Large-Value 数据
title: SQL Server 二进制和大值数据
ms.date: 03/30/2017
ms.assetid: e00827b3-7511-4b2d-91d7-851ca86cc6b5
ms.openlocfilehash: 8c7da5d504af0bc1beeea7e210a6fff4157fb090
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767435"
---
# <a name="sql-server-binary-and-large-value-data"></a><span data-ttu-id="7f86b-103">SQL Server 二进制和大值数据</span><span class="sxs-lookup"><span data-stu-id="7f86b-103">SQL Server Binary and Large-Value Data</span></span>

<span data-ttu-id="7f86b-104">SQL Server 提供了 `max` 说明符以扩展 `varchar`、`nvarchar` 和 `varbinary` 数据类型的存储容量。</span><span class="sxs-lookup"><span data-stu-id="7f86b-104">SQL Server provides the `max` specifier, which expands the storage capacity of the `varchar`, `nvarchar`, and `varbinary` data types.</span></span> <span data-ttu-id="7f86b-105">`varchar(max)`、`nvarchar(max)` 和 `varbinary(max)` 统称为“大值数据类型”。</span><span class="sxs-lookup"><span data-stu-id="7f86b-105">`varchar(max)`, `nvarchar(max)`, and `varbinary(max)` are collectively called *large-value data types*.</span></span> <span data-ttu-id="7f86b-106">你可以使用大值数据类型来存储长达 2^31-1 个字节的数据。</span><span class="sxs-lookup"><span data-stu-id="7f86b-106">You can use the large-value data types to store up to 2^31-1 bytes of data.</span></span>  
  
 <span data-ttu-id="7f86b-107">SQL Server 2008 引入了 FILESTREAM 属性，该属性不是数据类型，而是可以在列上定义的属性，从而允许大值数据存储在文件系统而不是数据库中。</span><span class="sxs-lookup"><span data-stu-id="7f86b-107">SQL Server 2008 introduces the FILESTREAM attribute, which is not a data type, but rather an attribute that can be defined on a column, allowing large-value data to be stored on the file system instead of in the database.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7f86b-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="7f86b-108">In This Section</span></span>  

 [<span data-ttu-id="7f86b-109">修改 ADO.NET 中的 Large-Value (max) 数据</span><span class="sxs-lookup"><span data-stu-id="7f86b-109">Modifying Large-Value (max) Data in ADO.NET</span></span>](modifying-large-value-max-data.md)  
 <span data-ttu-id="7f86b-110">说明如何使用大值数据类型。</span><span class="sxs-lookup"><span data-stu-id="7f86b-110">Describes how to work with the large-value data types.</span></span>  
  
 [<span data-ttu-id="7f86b-111">FILESTREAM 数据</span><span class="sxs-lookup"><span data-stu-id="7f86b-111">FILESTREAM Data</span></span>](filestream-data.md)  
 <span data-ttu-id="7f86b-112">介绍如何使用 FILESTREAM 属性处理 SQL Server 2008 中存储的大值数据。</span><span class="sxs-lookup"><span data-stu-id="7f86b-112">Describes how to work with large-value data stored in SQL Server 2008 with the FILESTREAM attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f86b-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7f86b-113">See also</span></span>

- [<span data-ttu-id="7f86b-114">SQL Server 数据类型和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="7f86b-114">SQL Server Data Types and ADO.NET</span></span>](sql-server-data-types.md)
- [<span data-ttu-id="7f86b-115">ADO.NET 中的 SQL Server 数据操作</span><span class="sxs-lookup"><span data-stu-id="7f86b-115">SQL Server Data Operations in ADO.NET</span></span>](sql-server-data-operations.md)
- [<span data-ttu-id="7f86b-116">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="7f86b-116">Retrieving and Modifying Data in ADO.NET</span></span>](../retrieving-and-modifying-data.md)
- [<span data-ttu-id="7f86b-117">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="7f86b-117">ADO.NET Overview</span></span>](../ado-net-overview.md)
