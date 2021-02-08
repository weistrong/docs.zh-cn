---
description: '了解详细信息： ( .NET 命名空间和类型的 Imports 语句) '
title: Imports 语句-.NET 命名空间和类型
ms.date: 07/20/2015
f1_keywords:
- vb.Imports
- imports
helpviewer_keywords:
- declared element names [Visual Basic], qualification
- imports [Visual Basic]
- Imports statement [Visual Basic]
- aliases [Visual Basic], Imports statement
- container elements [Visual Basic]
- namespaces [Visual Basic], importing
- Imports statement [Visual Basic], syntax
- import aliases [Visual Basic]
- aliases [Visual Basic], import
- declared elements [Visual Basic], container elements
ms.assetid: 7062f8aa-d890-4232-9eed-92836e13fb6e
ms.openlocfilehash: 28b7608e250fdba9c39f0209154d5a3d8f725eea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768969"
---
# <a name="imports-statement-net-namespace-and-type"></a><span data-ttu-id="d8b7c-103">Imports 语句（.NET 命名空间和类型）</span><span class="sxs-lookup"><span data-stu-id="d8b7c-103">Imports Statement (.NET Namespace and Type)</span></span>

<span data-ttu-id="d8b7c-104">允许引用类型名称，而无需命名空间限定。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">Enables type names to be referenced without namespace qualification.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b7c-105">语法</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">Syntax</span></span>

```vb
Imports [ aliasname = ] namespace
' -or-
Imports [ aliasname = ] namespace.element
```

## <a name="parts"></a><span data-ttu-id="d8b7c-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">Parts</span></span>

|<span data-ttu-id="d8b7c-107">术语</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">Term</span></span>|<span data-ttu-id="d8b7c-108">定义</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">Definition</span></span>|
|---|---|
|`aliasname`|<span data-ttu-id="d8b7c-109">可选。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">Optional.</span></span> <span data-ttu-id="d8b7c-110">*导入别名* 或代码可以引用的名称， `namespace` 而不是完全限定字符串。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">An *import alias* or name by which code can refer to `namespace` instead of the full qualification string.</span></span> <span data-ttu-id="d8b7c-111">请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">See [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>|
|`namespace`|<span data-ttu-id="d8b7c-112">必需。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">Required.</span></span> <span data-ttu-id="d8b7c-113">要导入的命名空间的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">The fully qualified name of the namespace being imported.</span></span> <span data-ttu-id="d8b7c-114">可以是嵌套到任何级别的命名空间的字符串。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-114">Can be a string of namespaces nested to any level.</span></span>|
|`element`|<span data-ttu-id="d8b7c-115">可选。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-115">Optional.</span></span> <span data-ttu-id="d8b7c-116">命名空间中声明的编程元素的名称。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-116">The name of a programming element declared in the namespace.</span></span> <span data-ttu-id="d8b7c-117">可以是任何容器元素。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-117">Can be any container element.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d8b7c-118">备注</span><span class="sxs-lookup"><span data-stu-id="d8b7c-118">Remarks</span></span>

<span data-ttu-id="d8b7c-119">`Imports`语句允许直接引用给定命名空间中包含的类型。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-119">The `Imports` statement enables types that are contained in a given namespace to be referenced directly.</span></span>

<span data-ttu-id="d8b7c-120">您可以提供单个命名空间名称或嵌套命名空间的字符串。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-120">You can supply a single namespace name or a string of nested namespaces.</span></span> <span data-ttu-id="d8b7c-121">每个嵌套命名空间都通过句点 () 与下一个较高的级别命名空间分离 `.` ，如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="d8b7c-121">Each nested namespace is separated from the next higher level namespace by a period (`.`), as the following example illustrates:</span></span>

```vb
Imports System.Collections.Generic
```

<span data-ttu-id="d8b7c-122">每个源文件可以包含任意多个 `Imports` 语句。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-122">Each source file can contain any number of `Imports` statements.</span></span> <span data-ttu-id="d8b7c-123">它们必须遵循任何选项声明，如 `Option Strict` 语句，它们必须位于任何编程元素声明（如或语句）之前 `Module` `Class` 。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-123">These must follow any option declarations, such as the `Option Strict` statement, and they must precede any programming element declarations, such as `Module` or `Class` statements.</span></span>

<span data-ttu-id="d8b7c-124">只能 `Imports` 在文件级别使用。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-124">You can use `Imports` only at file level.</span></span> <span data-ttu-id="d8b7c-125">这意味着，用于导入的声明上下文必须是一个源文件，而不能是命名空间、类、结构、模块、接口、过程或块。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-125">This means the declaration context for importation must be a source file, and cannot be a namespace, class, structure, module, interface, procedure, or block.</span></span>

<span data-ttu-id="d8b7c-126">请注意，该 `Imports` 语句不会使其他项目和程序集中的元素可用于您的项目。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-126">Note that the `Imports` statement does not make elements from other projects and assemblies available to your project.</span></span> <span data-ttu-id="d8b7c-127">导入不会替代设置引用。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-127">Importing does not take the place of setting a reference.</span></span> <span data-ttu-id="d8b7c-128">它只是不再需要限定已可用于你的项目的名称。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-128">It only removes the need to qualify names that are already available to your project.</span></span> <span data-ttu-id="d8b7c-129">有关详细信息，请参阅对已 [声明元素的引用](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md)中的 "导入包含元素"。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-129">For more information, see "Importing Containing Elements" in [References to Declared Elements](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d8b7c-130">您可以 `Imports` 使用 " [引用" 页、"项目设计器" (Visual Basic) ](/visualstudio/ide/reference/references-page-project-designer-visual-basic)定义隐式语句。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-130">You can define implicit `Imports` statements by using the [References Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic).</span></span> <span data-ttu-id="d8b7c-131">有关详细信息，请参阅 [如何：添加或移除导入的命名空间 (Visual Basic) ](/visualstudio/ide/how-to-add-or-remove-imported-namespaces-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-131">For more information, see [How to: Add or Remove Imported Namespaces (Visual Basic)](/visualstudio/ide/how-to-add-or-remove-imported-namespaces-visual-basic).</span></span>

## <a name="import-aliases"></a><span data-ttu-id="d8b7c-132">导入别名</span><span class="sxs-lookup"><span data-stu-id="d8b7c-132">Import Aliases</span></span>

<span data-ttu-id="d8b7c-133">*导入别名* 定义命名空间或类型的别名。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-133">An *import alias* defines the alias for a namespace or type.</span></span> <span data-ttu-id="d8b7c-134">如果需要使用一个或多个命名空间中声明的同名项，则导入别名非常有用。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-134">Import aliases are useful when you need to use items with the same name that are declared in one or more namespaces.</span></span> <span data-ttu-id="d8b7c-135">有关详细信息和示例，请参阅对已 [声明元素的引用](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md)中的 "限定元素名称"。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-135">For more information and an example, see "Qualifying an Element Name" in [References to Declared Elements](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>

<span data-ttu-id="d8b7c-136">不应在模块级别使用与相同的名称声明成员 `aliasname` 。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-136">You should not declare a member at module level with the same name as `aliasname`.</span></span> <span data-ttu-id="d8b7c-137">如果这样做，则 Visual Basic 编译器仅对已声明的成员使用，而不再将 `aliasname` 其识别为导入别名。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-137">If you do, the Visual Basic compiler uses `aliasname` only for the declared member and no longer recognizes it as an import alias.</span></span>

<span data-ttu-id="d8b7c-138">尽管用于声明导入别名的语法与用于导入 XML 命名空间前缀的语法类似，但结果不同。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-138">Although the syntax used for declaring an import alias is like that used for importing an XML namespace prefix, the results are different.</span></span> <span data-ttu-id="d8b7c-139">导入别名可用作代码中的表达式，而 XML 命名空间前缀只能在 XML 文本或 XML 轴属性中用作限定元素或属性名的前缀。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-139">An import alias can be used as an expression in your code, whereas an XML namespace prefix can be used only in XML literals or XML axis properties as the prefix for a qualified element or attribute name.</span></span>

### <a name="element-names"></a><span data-ttu-id="d8b7c-140">元素名称</span><span class="sxs-lookup"><span data-stu-id="d8b7c-140">Element Names</span></span>

<span data-ttu-id="d8b7c-141">如果提供 `element` ，则它必须表示一个 *容器元素*，即一个可以包含其他元素的编程元素。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-141">If you supply `element`, it must represent a *container element*, that is, a programming element that can contain other elements.</span></span> <span data-ttu-id="d8b7c-142">容器元素包括类、结构、模块、接口和枚举。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-142">Container elements include classes, structures, modules, interfaces, and enumerations.</span></span>

<span data-ttu-id="d8b7c-143">语句提供的元素的作用域 `Imports` 取决于您是否指定了 `element` 。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-143">The scope of the elements made available by an `Imports` statement depends on whether you specify `element`.</span></span> <span data-ttu-id="d8b7c-144">如果仅指定 `namespace` ，则该命名空间的所有唯一命名的成员以及该命名空间内的容器元素的成员均可使用而无需进行限定。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-144">If you specify only `namespace`, all uniquely named members of that namespace, and members of container elements within that namespace, are available without qualification.</span></span> <span data-ttu-id="d8b7c-145">如果同时指定 `namespace` 和 `element` ，则仅可使用该元素的成员而无需进行限定。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-145">If you specify both `namespace` and `element`, only the members of that element are available without qualification.</span></span>

## <a name="example"></a><span data-ttu-id="d8b7c-146">示例</span><span class="sxs-lookup"><span data-stu-id="d8b7c-146">Example</span></span>

<span data-ttu-id="d8b7c-147">下面的示例使用类返回 *C： \\* 目录中的所有文件夹 <xref:System.IO.DirectoryInfo> ：</span><span class="sxs-lookup"><span data-stu-id="d8b7c-147">The following example returns all the folders in the *C:\\* directory by using the <xref:System.IO.DirectoryInfo> class:</span></span>

<span data-ttu-id="d8b7c-148">该代码的 `Imports` 顶部没有语句。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-148">The code has no `Imports` statements at the top of the file.</span></span> <span data-ttu-id="d8b7c-149">因此， <xref:System.IO.DirectoryInfo> 、 <xref:System.Text.StringBuilder> 和 <xref:Microsoft.VisualBasic.ControlChars.CrLf> 引用均由命名空间完全限定。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-149">Therefore, the <xref:System.IO.DirectoryInfo>, <xref:System.Text.StringBuilder>, and <xref:Microsoft.VisualBasic.ControlChars.CrLf> references are all fully qualified with the namespaces.</span></span>

[!code-vb[VbVbalrStatements#152](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#152)]

## <a name="example"></a><span data-ttu-id="d8b7c-150">示例</span><span class="sxs-lookup"><span data-stu-id="d8b7c-150">Example</span></span>

<span data-ttu-id="d8b7c-151">下面的示例包含 `Imports` 引用的命名空间的语句。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-151">The following example includes `Imports` statements for the referenced namespaces.</span></span> <span data-ttu-id="d8b7c-152">因此，无需使用命名空间完全限定类型。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-152">Therefore, the types do not have to be fully qualified with the namespaces.</span></span>

[!code-vb[VbVbalrStatements#153](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#153)]

[!code-vb[VbVbalrStatements#154](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#154)]
  
## <a name="example"></a><span data-ttu-id="d8b7c-153">示例</span><span class="sxs-lookup"><span data-stu-id="d8b7c-153">Example</span></span>

<span data-ttu-id="d8b7c-154">下面的示例包含 `Imports` 为被引用命名空间创建别名的语句。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-154">The following example includes `Imports` statements that create aliases for the referenced namespaces.</span></span> <span data-ttu-id="d8b7c-155">类型是用别名限定的。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-155">The types are qualified with the aliases.</span></span>

[!code-vb[VbVbalrStatements#155](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#155)]

[!code-vb[VbVbalrStatements#156](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#156)]

## <a name="example"></a><span data-ttu-id="d8b7c-156">示例</span><span class="sxs-lookup"><span data-stu-id="d8b7c-156">Example</span></span>

<span data-ttu-id="d8b7c-157">下面的示例包含 `Imports` 为引用的类型创建别名的语句。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-157">The following example includes `Imports` statements that create aliases for the referenced types.</span></span> <span data-ttu-id="d8b7c-158">别名用于指定类型。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-158">Aliases are used to specify the types.</span></span>

[!code-vb[VbVbalrStatements#157](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#157)]

[!code-vb[VbVbalrStatements#158](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class12.vb#158)]
  
## <a name="see-also"></a><span data-ttu-id="d8b7c-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8b7c-159">See also</span></span>

- [<span data-ttu-id="d8b7c-160">Namespace 语句</span><span class="sxs-lookup"><span data-stu-id="d8b7c-160">Namespace Statement</span></span>](namespace-statement.md)
- [<span data-ttu-id="d8b7c-161">Visual Basic 中的命名空间</span><span class="sxs-lookup"><span data-stu-id="d8b7c-161">Namespaces in Visual Basic</span></span>](../../programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="d8b7c-162">引用和 Imports 语句</span><span class="sxs-lookup"><span data-stu-id="d8b7c-162">References and the Imports Statement</span></span>](../../programming-guide/program-structure/references-and-the-imports-statement.md)
- [<span data-ttu-id="d8b7c-163">Imports 语句（XML 命名空间）</span><span class="sxs-lookup"><span data-stu-id="d8b7c-163">Imports Statement (XML Namespace)</span></span>](imports-statement-xml-namespace.md)
- [<span data-ttu-id="d8b7c-164">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="d8b7c-164">References to Declared Elements</span></span>](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md)
