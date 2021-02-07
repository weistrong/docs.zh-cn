---
description: 了解有关详细信息，请参阅如何：在 Visual Studio 中创建 LINQ to DataSet 项目
title: 在 Visual Studio 中创建 LINQ to DataSet 项目
ms.date: 08/15/2018
ms.assetid: 49ba6cb0-cdd2-4571-aeaa-25bf0f40e9b3
ms.openlocfilehash: 4ab626ddaa27780759df95462faac366be8beeff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723824"
---
# <a name="how-to-create-a-linq-to-dataset-project-in-visual-studio"></a>如何：在 Visual Studio 中创建 LINQ to DataSet 项目

不同类型的 LINQ 项目需要特定的程序集引用和导入的命名空间 (Visual Basic) 或 (c # ) 中 [使用](../../../csharp/language-reference/keywords/using-directive.md) 指令。 LINQ 的最低要求是对 *System.Core.dll* 的引用和的 `using` 指令 <xref:System.Linq> 。

默认情况下，如果在 Visual Studio 2017 或更高版本中创建新的 c # 控制台应用程序项目，则会提供这些要求。 如果要从早期版本的 Visual Studio 升级项目，可能必须手动提供这些与 LINQ 相关的引用。

LINQ to DataSet 需要对 *System.Data.dll* 和 *System.Data.DataSetExtensions.dll* 进行两个附加引用。

> [!NOTE]
> 如果是从命令提示符生成，则必须在 *%ProgramFiles%\Reference Assemblies\Microsoft\Framework\v3.5* 中手动引用与 LINQ 相关的 dll。

## <a name="to-enable-linq-to-dataset-functionality"></a>启用 LINQ to DataSet 功能

按照以下步骤在现有项目中启用 LINQ to DataSet 功能。

1. 添加对 System.data.datasetextensions.dll **、system.web** 和 system.object 的引用。 

   在 **解决方案资源管理器** 中，右键单击 " **引用** " 节点，然后选择 " **添加引用**"。 在 "**引用管理器** **" 对话框** 中 **，选择 "** **system.data.datasetextensions.dll**"。 选择“确定”。

1. 使用 Visual Basic) 中的 (或 [Imports 语句](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)添加 [using](../../../csharp/language-reference/keywords/using-directive.md)指令以用于 **system.web** 和 **system.object**。

   ```csharp
   using System.Data;
   using System.Linq;
   ```

1. （可选） `using` `Imports` 为 SqlClient 或添加指令 (或语句) ，具体取决于连接到数据库的方式。

## <a name="see-also"></a>请参阅

- [LINQ to DataSet 入门](getting-started-linq-to-dataset.md)
