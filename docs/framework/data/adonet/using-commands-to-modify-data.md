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
# <a name="using-commands-to-modify-data"></a>使用命令修改数据

使用 .NET Framework 数据提供程序，您可以执行存储过程或数据定义语言语句（如 CREATE TABLE 和 ALTER COLUMN）来对数据库或编录执行架构处理。 这些命令不会像查询那样返回行，因此 **Command** 对象提供 **ExecuteNonQuery** 来处理它们。  
  
 除了使用 ExecuteNonQuery 来修改架构之外，还可以使用此方法处理那些修改数据但不返回行的 SQL 语句，如 INSERT、UPDATE 和 DELETE。  
  
 虽然行不是由 ExecuteNonQuery 方法返回的，但可以通过 Command 对象的 Parameters 集合来传递和返回输入和输出参数以及返回值。  
  
## <a name="in-this-section"></a>本节内容  

 [更新数据源中的数据](updating-data-in-a-data-source.md)  
 描述如何执行对数据库中的数据进行修改的命令或存储过程。  
  
 [执行目录操作](performing-catalog-operations.md)  
 描述如何执行对数据库架构进行修改的命令。  
  
## <a name="see-also"></a>另请参阅

- [在 ADO.NET 中检索和修改数据](retrieving-and-modifying-data.md)
- [命令和参数](commands-and-parameters.md)
- [ADO.NET 概述](ado-net-overview.md)
