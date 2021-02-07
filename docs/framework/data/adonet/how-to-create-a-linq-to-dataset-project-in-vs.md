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
# <a name="how-to-create-a-linq-to-dataset-project-in-visual-studio"></a><span data-ttu-id="11c25-103">如何：在 Visual Studio 中创建 LINQ to DataSet 项目</span><span class="sxs-lookup"><span data-stu-id="11c25-103">How to: Create a LINQ to DataSet project in Visual Studio</span></span>

<span data-ttu-id="11c25-104">不同类型的 LINQ 项目需要特定的程序集引用和导入的命名空间 (Visual Basic) 或 (c # ) 中 [使用](../../../csharp/language-reference/keywords/using-directive.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="11c25-104">The different types of LINQ projects require certain assembly references and imported namespaces (Visual Basic) or [using](../../../csharp/language-reference/keywords/using-directive.md) directives (C#).</span></span> <span data-ttu-id="11c25-105">LINQ 的最低要求是对 *System.Core.dll* 的引用和的 `using` 指令 <xref:System.Linq> 。</span><span class="sxs-lookup"><span data-stu-id="11c25-105">The minimum requirement for LINQ is a reference to *System.Core.dll* and a `using` directive for <xref:System.Linq>.</span></span>

<span data-ttu-id="11c25-106">默认情况下，如果在 Visual Studio 2017 或更高版本中创建新的 c # 控制台应用程序项目，则会提供这些要求。</span><span class="sxs-lookup"><span data-stu-id="11c25-106">These requirements are supplied by default if you create a new C# console app project in Visual Studio 2017 or a later version.</span></span> <span data-ttu-id="11c25-107">如果要从早期版本的 Visual Studio 升级项目，可能必须手动提供这些与 LINQ 相关的引用。</span><span class="sxs-lookup"><span data-stu-id="11c25-107">If you're upgrading a project from an earlier version of Visual Studio, you might have to supply these LINQ-related references manually.</span></span>

<span data-ttu-id="11c25-108">LINQ to DataSet 需要对 *System.Data.dll* 和 *System.Data.DataSetExtensions.dll* 进行两个附加引用。</span><span class="sxs-lookup"><span data-stu-id="11c25-108">LINQ to DataSet requires two additional references to *System.Data.dll* and *System.Data.DataSetExtensions.dll*.</span></span>

> [!NOTE]
> <span data-ttu-id="11c25-109">如果是从命令提示符生成，则必须在 *%ProgramFiles%\Reference Assemblies\Microsoft\Framework\v3.5* 中手动引用与 LINQ 相关的 dll。</span><span class="sxs-lookup"><span data-stu-id="11c25-109">If you're building from a command prompt, you must manually reference the LINQ-related DLLs in *%ProgramFiles%\Reference Assemblies\Microsoft\Framework\v3.5*.</span></span>

## <a name="to-enable-linq-to-dataset-functionality"></a><span data-ttu-id="11c25-110">启用 LINQ to DataSet 功能</span><span class="sxs-lookup"><span data-stu-id="11c25-110">To enable LINQ to DataSet functionality</span></span>

<span data-ttu-id="11c25-111">按照以下步骤在现有项目中启用 LINQ to DataSet 功能。</span><span class="sxs-lookup"><span data-stu-id="11c25-111">Follow these steps to enable LINQ to DataSet functionality in an existing project.</span></span>

1. <span data-ttu-id="11c25-112">添加对 System.data.datasetextensions.dll **、system.web** 和 system.object 的引用。 </span><span class="sxs-lookup"><span data-stu-id="11c25-112">Add references to **System.Core**, **System.Data**, and **System.Data.DataSetExtensions**.</span></span>

   <span data-ttu-id="11c25-113">在 **解决方案资源管理器** 中，右键单击 " **引用** " 节点，然后选择 " **添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="11c25-113">In **Solution Explorer**, right-click on the **References** node and select **Add Reference**.</span></span> <span data-ttu-id="11c25-114">在 "**引用管理器** **" 对话框** 中 **，选择 "** **system.data.datasetextensions.dll**"。</span><span class="sxs-lookup"><span data-stu-id="11c25-114">In the **Reference Manager** dialog box, select **System.Core**, **System.Data**, and **System.Data.DataSetExtensions**.</span></span> <span data-ttu-id="11c25-115">选择“确定”。</span><span class="sxs-lookup"><span data-stu-id="11c25-115">Select **OK**.</span></span>

1. <span data-ttu-id="11c25-116">使用 Visual Basic) 中的 (或 [Imports 语句](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)添加 [using](../../../csharp/language-reference/keywords/using-directive.md)指令以用于 **system.web** 和 **system.object**。</span><span class="sxs-lookup"><span data-stu-id="11c25-116">Add [using](../../../csharp/language-reference/keywords/using-directive.md) directives (or [Imports statements](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) in Visual Basic) for **System.Data** and **System.Linq**.</span></span>

   ```csharp
   using System.Data;
   using System.Linq;
   ```

1. <span data-ttu-id="11c25-117">（可选） `using` `Imports` 为 SqlClient 或添加指令 (或语句) ，具体取决于连接到数据库的方式。</span><span class="sxs-lookup"><span data-stu-id="11c25-117">Optionally, add a `using` directive (or `Imports` statement) for **System.Data.Common** or **System.Data.SqlClient**, depending on how you connect to the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="11c25-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="11c25-118">See also</span></span>

- [<span data-ttu-id="11c25-119">LINQ to DataSet 入门</span><span class="sxs-lookup"><span data-stu-id="11c25-119">Get started with LINQ to DataSet</span></span>](getting-started-linq-to-dataset.md)
