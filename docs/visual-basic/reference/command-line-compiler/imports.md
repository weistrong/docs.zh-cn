---
description: 详细了解：-imports (Visual Basic)
title: -imports
ms.date: 03/10/2018
helpviewer_keywords:
- /imports compiler option [Visual Basic]
- imports compiler option [Visual Basic]
- -imports compiler option [Visual Basic]
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
ms.openlocfilehash: 8c6744ff857a15da9362b724a62fcf053e9fd8f0
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100470195"
---
# <a name="-imports-visual-basic"></a><span data-ttu-id="0c79d-103">-imports (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0c79d-103">-imports (Visual Basic)</span></span>

<span data-ttu-id="0c79d-104">从指定程序集导入命名空间。</span><span class="sxs-lookup"><span data-stu-id="0c79d-104">Imports namespaces from a specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c79d-105">语法</span><span class="sxs-lookup"><span data-stu-id="0c79d-105">Syntax</span></span>  
  
```console  
-imports:namespaceList  
```  
  
## <a name="arguments"></a><span data-ttu-id="0c79d-106">自变量</span><span class="sxs-lookup"><span data-stu-id="0c79d-106">Arguments</span></span>  
  
|<span data-ttu-id="0c79d-107">术语</span><span class="sxs-lookup"><span data-stu-id="0c79d-107">Term</span></span>|<span data-ttu-id="0c79d-108">定义</span><span class="sxs-lookup"><span data-stu-id="0c79d-108">Definition</span></span>|  
|---|---|  
|`namespaceList`|<span data-ttu-id="0c79d-109">必需。</span><span class="sxs-lookup"><span data-stu-id="0c79d-109">Required.</span></span> <span data-ttu-id="0c79d-110">要导入的命名空间的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="0c79d-110">Comma-delimited list of namespaces to be imported.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c79d-111">备注</span><span class="sxs-lookup"><span data-stu-id="0c79d-111">Remarks</span></span>  

 <span data-ttu-id="0c79d-112">`-imports` 选项会导入在当前源文件集中定义的任何命名空间或是从任何引用程序集导入任何命名空间。</span><span class="sxs-lookup"><span data-stu-id="0c79d-112">The `-imports` option imports any namespace defined within the current set of source files or from any referenced assembly.</span></span>  
  
 <span data-ttu-id="0c79d-113">使用 `-imports` 指定的命名空间中的成员可用于编译中的所有源代码文件。</span><span class="sxs-lookup"><span data-stu-id="0c79d-113">The members in a namespace specified with `-imports` are available to all source-code files in the compilation.</span></span> <span data-ttu-id="0c79d-114">使用 [Imports 语句（.NET 命名空间和类型）](../../language-reference/statements/imports-statement-net-namespace-and-type.md)可将命名空间用于单个源代码文件中。</span><span class="sxs-lookup"><span data-stu-id="0c79d-114">Use the [Imports Statement (.NET Namespace and Type)](../../language-reference/statements/imports-statement-net-namespace-and-type.md) to use a namespace in a single source-code file.</span></span>  
  
|<span data-ttu-id="0c79d-115">若在 Visual Studio 集成开发环境中设置 -imports</span><span class="sxs-lookup"><span data-stu-id="0c79d-115">To set -imports in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="0c79d-116">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="0c79d-116">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="0c79d-117">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="0c79d-117">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="0c79d-118">2.单击“引用”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="0c79d-118">2.  Click the **References** tab.</span></span><br /><span data-ttu-id="0c79d-119">3.在“添加用户导入”  按钮旁的框中输入命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="0c79d-119">3.  Enter the namespace name in the box beside the **Add User Import** button.</span></span><br /><span data-ttu-id="0c79d-120">4.单击“添加用户导入”  按钮。</span><span class="sxs-lookup"><span data-stu-id="0c79d-120">4.  Click the **Add User Import** button.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0c79d-121">示例</span><span class="sxs-lookup"><span data-stu-id="0c79d-121">Example</span></span>  

 <span data-ttu-id="0c79d-122">以下代码在指定 `-imports:system.globalization` 时进行编译。</span><span class="sxs-lookup"><span data-stu-id="0c79d-122">The following code compiles when `-imports:system.globalization` is specified.</span></span> <span data-ttu-id="0c79d-123">如果没有它，则成功编译需要将 `Imports System.Globalization` 语句包含在源代码文件的开头，或者属性完全限定为 `System.Globalization.CultureInfo.CurrentCulture.Name`。</span><span class="sxs-lookup"><span data-stu-id="0c79d-123">Without it, successful compilation requires either that an `Imports System.Globalization` statement be included at the beginning of the source code file, or that the property be fully qualified as `System.Globalization.CultureInfo.CurrentCulture.Name`.</span></span>

```vb
Module Example
   Public Sub Main()
      Console.WriteLine($"The current culture is {CultureInfo.CurrentCulture.Name}")
   End Sub
End Module
```

## <a name="see-also"></a><span data-ttu-id="0c79d-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c79d-124">See also</span></span>

- [<span data-ttu-id="0c79d-125">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="0c79d-125">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="0c79d-126">引用和 Imports 语句</span><span class="sxs-lookup"><span data-stu-id="0c79d-126">References and the Imports Statement</span></span>](../../programming-guide/program-structure/references-and-the-imports-statement.md)
- [<span data-ttu-id="0c79d-127">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="0c79d-127">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
