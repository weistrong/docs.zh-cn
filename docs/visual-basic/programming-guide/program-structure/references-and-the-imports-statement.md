---
description: '详细了解：引用和 Imports 语句 (Visual Basic) '
title: 引用和 Imports 语句
ms.date: 07/20/2015
helpviewer_keywords:
- assemblies [Visual Basic], namespaces
- references [Visual Basic], assembly
- namespaces [Visual Basic], assemblies
- referencing assemblies
- Imports statement [Visual Basic], referencing assemblies
- assemblies [Visual Basic], references
ms.assetid: 38149bd4-0a6f-4b31-b5f8-94a8c33f1600
ms.openlocfilehash: 3ca685d33f69224a6eea324d7357be4b5203eb45
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100468234"
---
# <a name="references-and-the-imports-statement-visual-basic"></a><span data-ttu-id="58e13-103">引用和 Imports 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="58e13-103">References and the Imports Statement (Visual Basic)</span></span>

<span data-ttu-id="58e13-104">通过选择 "**项目**" 菜单上的 "**添加引用**" 命令，可以使外部对象对项目可用。</span><span class="sxs-lookup"><span data-stu-id="58e13-104">You can make external objects available to your project by choosing the **Add Reference** command on the **Project** menu.</span></span> <span data-ttu-id="58e13-105">Visual Basic 中的引用可指向程序集，这些程序集类似于类型库，但包含更多信息。</span><span class="sxs-lookup"><span data-stu-id="58e13-105">References in Visual Basic can point to assemblies, which are like type libraries but contain more information.</span></span>  
  
## <a name="the-imports-statement"></a><span data-ttu-id="58e13-106">Imports 语句</span><span class="sxs-lookup"><span data-stu-id="58e13-106">The Imports Statement</span></span>  

 <span data-ttu-id="58e13-107">程序集包括一个或多个命名空间。</span><span class="sxs-lookup"><span data-stu-id="58e13-107">Assemblies include one or more namespaces.</span></span> <span data-ttu-id="58e13-108">添加对程序集的引用时，还可以向模块添加一个 `Imports` 语句，该模块控制该程序集的命名空间在模块中的可见性。</span><span class="sxs-lookup"><span data-stu-id="58e13-108">When you add a reference to an assembly, you can also add an `Imports` statement to a module that controls the visibility of that assembly's namespaces within the module.</span></span> <span data-ttu-id="58e13-109">`Imports`语句提供了一个范围上下文，该上下文允许只使用提供唯一引用所需的命名空间部分。</span><span class="sxs-lookup"><span data-stu-id="58e13-109">The `Imports` statement provides a scoping context that lets you use only the portion of the namespace necessary to supply a unique reference.</span></span>  
  
 <span data-ttu-id="58e13-110">`Imports`语句具有以下语法：</span><span class="sxs-lookup"><span data-stu-id="58e13-110">The `Imports` statement has the following syntax:</span></span>  
  
 `Imports [Aliasname =] Namespace`  
  
 <span data-ttu-id="58e13-111">`Aliasname` 引用可以在代码中用来引用导入的命名空间的短名称。</span><span class="sxs-lookup"><span data-stu-id="58e13-111">`Aliasname` refers to a short name you can use within code to refer to an imported namespace.</span></span> <span data-ttu-id="58e13-112">`Namespace` 是通过项目引用、项目中的定义或通过上一条语句提供的命名空间 `Imports` 。</span><span class="sxs-lookup"><span data-stu-id="58e13-112">`Namespace` is a namespace available through either a project reference, through a definition within the project, or through a previous `Imports` statement.</span></span>  
  
 <span data-ttu-id="58e13-113">模块可以包含任意多个 `Imports` 语句。</span><span class="sxs-lookup"><span data-stu-id="58e13-113">A module may contain any number of `Imports` statements.</span></span> <span data-ttu-id="58e13-114">它们必须出现在任何 `Option` 语句之后（如果存在），但在任何其他代码之前。</span><span class="sxs-lookup"><span data-stu-id="58e13-114">They must appear after any `Option` statements, if present, but before any other code.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="58e13-115">不要将项目引用与 `Imports` 语句或 `Declare` 语句混淆。</span><span class="sxs-lookup"><span data-stu-id="58e13-115">Do not confuse project references with the `Imports` statement or the `Declare` statement.</span></span> <span data-ttu-id="58e13-116">项目引用使外部对象（如程序集中的对象）可用于 Visual Basic 项目。</span><span class="sxs-lookup"><span data-stu-id="58e13-116">Project references make external objects, such as objects in assemblies, available to Visual Basic projects.</span></span> <span data-ttu-id="58e13-117">`Imports`语句用于简化对项目引用的访问，但不提供对这些对象的访问权限。</span><span class="sxs-lookup"><span data-stu-id="58e13-117">The `Imports` statement is used to simplify access to project references, but does not provide access to these objects.</span></span> <span data-ttu-id="58e13-118">`Declare`语句用于声明对动态链接库中的外部过程的引用 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="58e13-118">The `Declare` statement is used to declare a reference to an external procedure in a dynamic-link library (DLL).</span></span>  
  
## <a name="using-aliases-with-the-imports-statement"></a><span data-ttu-id="58e13-119">在 Imports 语句中使用别名</span><span class="sxs-lookup"><span data-stu-id="58e13-119">Using Aliases with the Imports Statement</span></span>  

 <span data-ttu-id="58e13-120">使用 `Imports` 语句，无需显式键入引用的完全限定名，就能更轻松地访问类的方法。</span><span class="sxs-lookup"><span data-stu-id="58e13-120">The `Imports` statement makes it easier to access methods of classes by eliminating the need to explicitly type the fully qualified names of references.</span></span> <span data-ttu-id="58e13-121">使用别名可以为一个命名空间的一部分分配更友好的名称。</span><span class="sxs-lookup"><span data-stu-id="58e13-121">Aliases let you assign a friendlier name to just one part of a namespace.</span></span> <span data-ttu-id="58e13-122">例如，在多行上显示一段文本的回车/换行符序列是 <xref:Microsoft.VisualBasic.ControlChars> 命名空间中的模块的一部分 <xref:Microsoft.VisualBasic?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="58e13-122">For example, the carriage return/line feed sequence that causes a single piece of text to be displayed on multiple lines is part of the <xref:Microsoft.VisualBasic.ControlChars> module in the <xref:Microsoft.VisualBasic?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="58e13-123">若要在不带别名的程序中使用此常量，需要键入以下代码：</span><span class="sxs-lookup"><span data-stu-id="58e13-123">To use this constant in a program without an alias, you would need to type the following code:</span></span>  
  
 [!code-vb[VbVbalrApplication#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrApplication/VB/Class1.vb#3)]  
  
 <span data-ttu-id="58e13-124">`Imports` 语句必须始终是紧跟在模块中的任何语句之后的第一行 `Option` 。</span><span class="sxs-lookup"><span data-stu-id="58e13-124">`Imports` statements must always be the first lines immediately following any `Option` statements in a module.</span></span> <span data-ttu-id="58e13-125">下面的代码段演示了如何导入和分配模块的别名 <xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType> ：</span><span class="sxs-lookup"><span data-stu-id="58e13-125">The following code fragment shows how to import and assign an alias to the <xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType> module:</span></span>  
  
 [!code-vb[VbVbalrApplication#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrApplication/VB/Class1.vb#4)]  
  
 <span data-ttu-id="58e13-126">以后引用此命名空间可能会大大缩短：</span><span class="sxs-lookup"><span data-stu-id="58e13-126">Future references to this namespace can be considerably shorter:</span></span>  
  
 [!code-vb[VbVbalrApplication#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrApplication/VB/Class1.vb#5)]  
  
 <span data-ttu-id="58e13-127">如果 `Imports` 语句不包含别名，则在导入的命名空间中定义的元素无需限定即可在模块中使用。</span><span class="sxs-lookup"><span data-stu-id="58e13-127">If an `Imports` statement does not include an alias name, elements defined within the imported namespace can be used in the module without qualification.</span></span> <span data-ttu-id="58e13-128">如果指定了别名，则必须将其用作该命名空间中包含的名称的限定符。</span><span class="sxs-lookup"><span data-stu-id="58e13-128">If the alias name is specified, it must be used as a qualifier for names contained within that namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58e13-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="58e13-129">See also</span></span>

- <xref:Microsoft.VisualBasic.ControlChars>
- <xref:Microsoft.VisualBasic>
- [<span data-ttu-id="58e13-130">Visual Basic 中的命名空间</span><span class="sxs-lookup"><span data-stu-id="58e13-130">Namespaces in Visual Basic</span></span>](namespaces.md)
- [<span data-ttu-id="58e13-131">.NET 中的程序集</span><span class="sxs-lookup"><span data-stu-id="58e13-131">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
- [<span data-ttu-id="58e13-132">Imports 语句（.NET 命名空间和类型）</span><span class="sxs-lookup"><span data-stu-id="58e13-132">Imports Statement (.NET Namespace and Type)</span></span>](../../language-reference/statements/imports-statement-net-namespace-and-type.md)
