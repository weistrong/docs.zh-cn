---
description: 了解详细信息：如何：通过修改 DBML 文件生成自定义代码
title: 如何：通过修改 DBML 文件生成自定义代码
ms.date: 03/30/2017
ms.assetid: 50ad597a-8598-42d3-82dd-fc7d702ebc37
ms.openlocfilehash: 0dd4024b3f6a0ca0583de6bfbdb7463fab14d969
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785999"
---
# <a name="how-to-generate-customized-code-by-modifying-a-dbml-file"></a><span data-ttu-id="e593f-103">如何：通过修改 DBML 文件生成自定义代码</span><span class="sxs-lookup"><span data-stu-id="e593f-103">How to: Generate Customized Code by Modifying a DBML File</span></span>

<span data-ttu-id="e593f-104">您可以 ( .dbml) 元数据文件生成 Visual Basic 或 c # 源代码。</span><span class="sxs-lookup"><span data-stu-id="e593f-104">You can generate Visual Basic or C# source code from a database markup language (.dbml) metadata file.</span></span> <span data-ttu-id="e593f-105">此方法提供了一个在生成应用程序映射代码前自定义默认 .dbml 文件的机会。</span><span class="sxs-lookup"><span data-stu-id="e593f-105">This approach provides an opportunity to customize the default .dbml file before you generate the application mapping code.</span></span> <span data-ttu-id="e593f-106">这是一项高级功能。</span><span class="sxs-lookup"><span data-stu-id="e593f-106">This is an advanced feature.</span></span>  
  
 <span data-ttu-id="e593f-107">此过程中的步骤如下：</span><span class="sxs-lookup"><span data-stu-id="e593f-107">The steps in this process are as follows:</span></span>  
  
1. <span data-ttu-id="e593f-108">生成 .dbml 文件。</span><span class="sxs-lookup"><span data-stu-id="e593f-108">Generate a .dbml file.</span></span>  
  
2. <span data-ttu-id="e593f-109">使用编辑器修改此 .dbml 文件。</span><span class="sxs-lookup"><span data-stu-id="e593f-109">Use an editor to modify the .dbml file.</span></span> <span data-ttu-id="e593f-110">请注意，此 .dbml 文件必须通过 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] .dbml 文件的架构定义 (.xsd) 文件的验证。</span><span class="sxs-lookup"><span data-stu-id="e593f-110">Note that the .dbml file must validate against the schema definition (.xsd) file for [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] .dbml files.</span></span> <span data-ttu-id="e593f-111">有关详细信息，请参阅 [LINQ to SQL 中的代码生成](code-generation-in-linq-to-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="e593f-111">For more information, see [Code Generation in LINQ to SQL](code-generation-in-linq-to-sql.md).</span></span>  
  
3. <span data-ttu-id="e593f-112">生成 Visual Basic 或 c # 源代码。</span><span class="sxs-lookup"><span data-stu-id="e593f-112">Generate the Visual Basic or C# source code.</span></span>  
  
 <span data-ttu-id="e593f-113">下面的示例使用 SQLMetal 命令行工具。</span><span class="sxs-lookup"><span data-stu-id="e593f-113">The following examples use the SQLMetal command-line tool.</span></span> <span data-ttu-id="e593f-114">有关详细信息，请参阅 [SqlMetal.exe（代码生成工具）](../../../../tools/sqlmetal-exe-code-generation-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="e593f-114">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e593f-115">示例</span><span class="sxs-lookup"><span data-stu-id="e593f-115">Example</span></span>  

 <span data-ttu-id="e593f-116">下面的代码从 Northwind 示例数据库生成 .dbml 文件。</span><span class="sxs-lookup"><span data-stu-id="e593f-116">The following code generates a .dbml file from the Northwind sample database.</span></span> <span data-ttu-id="e593f-117">您可以使用数据库的名称或 .mdf 文件的名称作为数据库元数据的源。</span><span class="sxs-lookup"><span data-stu-id="e593f-117">As source for the database metadata, you can use either the name of the database or the name of the .mdf file.</span></span>  
  
```console  
sqlmetal /server:myserver /database:northwind /dbml:mymeta.dbml  
sqlmetal /dbml:mymeta.dbml mydbfile.mdf  
```  
  
## <a name="example"></a><span data-ttu-id="e593f-118">示例</span><span class="sxs-lookup"><span data-stu-id="e593f-118">Example</span></span>  

 <span data-ttu-id="e593f-119">下面的代码从 .dbml 文件生成 Visual Basic 或 c # 源代码文件。</span><span class="sxs-lookup"><span data-stu-id="e593f-119">The following code generates Visual Basic or C# source code file from a .dbml file.</span></span>  
  
```console
sqlmetal /namespace:nwind /code:nwind.vb /language:vb DBMLFile.dbml  
sqlmetal /namespace:nwind /code:nwind.cs /language:csharp DBMLFile.dbml  
```  
  
## <a name="see-also"></a><span data-ttu-id="e593f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e593f-120">See also</span></span>

- [<span data-ttu-id="e593f-121">LINQ to SQL 中的代码生成</span><span class="sxs-lookup"><span data-stu-id="e593f-121">Code Generation in LINQ to SQL</span></span>](code-generation-in-linq-to-sql.md)
- [<span data-ttu-id="e593f-122">SqlMetal.exe（代码生成工具）</span><span class="sxs-lookup"><span data-stu-id="e593f-122">SqlMetal.exe (Code Generation Tool)</span></span>](../../../../tools/sqlmetal-exe-code-generation-tool.md)
- [<span data-ttu-id="e593f-123">创建对象模型</span><span class="sxs-lookup"><span data-stu-id="e593f-123">Creating the Object Model</span></span>](creating-the-object-model.md)
