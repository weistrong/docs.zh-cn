---
description: 了解详细信息： Namespace 语句
title: Namespace 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Namespace
helpviewer_keywords:
- namespaces [Visual Basic], root
- Namespace statement [Visual Basic]
- namespaces [Visual Basic], nested
- declaring namespaces [Visual Basic], syntax
- namespaces [Visual Basic], declaring
- root namespaces
- declarations [Visual Basic], namespaces
ms.assetid: a31fbd95-9ace-4c3d-bbb1-51222a2272b2
ms.openlocfilehash: 2c315947a26f72a90e03bc1f4bf1b5f647866b33
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768852"
---
# <a name="namespace-statement"></a><span data-ttu-id="68e8e-103">Namespace 语句</span><span class="sxs-lookup"><span data-stu-id="68e8e-103">Namespace Statement</span></span>

<span data-ttu-id="68e8e-104">声明命名空间的名称，并导致在该命名空间中编译跟在声明后的源代码。</span><span class="sxs-lookup"><span data-stu-id="68e8e-104">Declares the name of a namespace and causes the source code that follows the declaration to be compiled within that namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68e8e-105">语法</span><span class="sxs-lookup"><span data-stu-id="68e8e-105">Syntax</span></span>  
  
```vb  
Namespace [Global.] { name | name.name }  
    [ componenttypes ]  
End Namespace  
```  
  
## <a name="parts"></a><span data-ttu-id="68e8e-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="68e8e-106">Parts</span></span>  

 <span data-ttu-id="68e8e-107">全球</span><span class="sxs-lookup"><span data-stu-id="68e8e-107">Global</span></span>  
 <span data-ttu-id="68e8e-108">可选。</span><span class="sxs-lookup"><span data-stu-id="68e8e-108">Optional.</span></span> <span data-ttu-id="68e8e-109">允许你在项目的根命名空间外定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-109">Allows you to define a namespace out of the root namespace of your project.</span></span> <span data-ttu-id="68e8e-110">请参阅 [Visual Basic 中的命名空间](../../programming-guide/program-structure/namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="68e8e-110">See [Namespaces in Visual Basic](../../programming-guide/program-structure/namespaces.md).</span></span>  
  
 `name`  
 <span data-ttu-id="68e8e-111">必需。</span><span class="sxs-lookup"><span data-stu-id="68e8e-111">Required.</span></span> <span data-ttu-id="68e8e-112">标识命名空间的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="68e8e-112">A unique name that identifies the namespace.</span></span> <span data-ttu-id="68e8e-113">必须是有效的 Visual Basic 标识符。</span><span class="sxs-lookup"><span data-stu-id="68e8e-113">Must be a valid Visual Basic identifier.</span></span> <span data-ttu-id="68e8e-114">有关详细信息，请参阅已 [声明的元素名称](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="68e8e-114">For more information, see [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
 `componenttypes`  
 <span data-ttu-id="68e8e-115">可选。</span><span class="sxs-lookup"><span data-stu-id="68e8e-115">Optional.</span></span> <span data-ttu-id="68e8e-116">构成命名空间的元素。</span><span class="sxs-lookup"><span data-stu-id="68e8e-116">Elements that make up the namespace.</span></span> <span data-ttu-id="68e8e-117">其中包括但不限于枚举、结构、接口、类、模块、委托和其他命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-117">These include, but are not limited to, enumerations, structures, interfaces, classes, modules, delegates, and other namespaces.</span></span>  
  
 `End Namespace`  
 <span data-ttu-id="68e8e-118">终止 `Namespace` 块。</span><span class="sxs-lookup"><span data-stu-id="68e8e-118">Terminates a `Namespace` block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="68e8e-119">备注</span><span class="sxs-lookup"><span data-stu-id="68e8e-119">Remarks</span></span>  

 <span data-ttu-id="68e8e-120">命名空间用作组织系统。</span><span class="sxs-lookup"><span data-stu-id="68e8e-120">Namespaces are used as an organizational system.</span></span> <span data-ttu-id="68e8e-121">它们提供了一种方法来分类和显示向其他程序和应用程序公开的编程元素。</span><span class="sxs-lookup"><span data-stu-id="68e8e-121">They provide a way to classify and present programming elements that are exposed to other programs and applications.</span></span> <span data-ttu-id="68e8e-122">请注意，在类或结构为的意义上，命名空间不是 *类型* ，不能将编程元素声明为具有命名空间的数据类型。</span><span class="sxs-lookup"><span data-stu-id="68e8e-122">Note that a namespace is not a *type* in the sense that a class or structure is—you cannot declare a programming element to have the data type of a namespace.</span></span>  
  
 <span data-ttu-id="68e8e-123">语句后声明的所有编程元素都 `Namespace` 属于该命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-123">All programming elements declared after a `Namespace` statement belong to that namespace.</span></span> <span data-ttu-id="68e8e-124">Visual Basic 继续将元素编译到最后一个声明的命名空间中，直到它遇到 `End Namespace` 语句或另一个 `Namespace` 语句。</span><span class="sxs-lookup"><span data-stu-id="68e8e-124">Visual Basic continues to compile elements into the last declared namespace until it encounters either an `End Namespace` statement or another `Namespace` statement.</span></span>  
  
 <span data-ttu-id="68e8e-125">如果命名空间已定义，即使是项目外部的命名空间，也可以向其中添加编程元素。</span><span class="sxs-lookup"><span data-stu-id="68e8e-125">If a namespace is already defined, even outside your project, you can add programming elements to it.</span></span> <span data-ttu-id="68e8e-126">为此，请使用 `Namespace` 语句来指示 Visual Basic 将元素编译到该命名空间中。</span><span class="sxs-lookup"><span data-stu-id="68e8e-126">To do this, you use a `Namespace` statement to direct Visual Basic to compile elements into that namespace.</span></span>  
  
 <span data-ttu-id="68e8e-127">只能 `Namespace` 在文件或命名空间级别使用语句。</span><span class="sxs-lookup"><span data-stu-id="68e8e-127">You can use a `Namespace` statement only at the file or namespace level.</span></span> <span data-ttu-id="68e8e-128">这意味着命名空间的 *声明上下文* 必须是源文件或其他命名空间，不能是类、结构、模块、接口或过程。</span><span class="sxs-lookup"><span data-stu-id="68e8e-128">This means the *declaration context* for a namespace must be a source file or another namespace, and cannot be a class, structure, module, interface, or procedure.</span></span> <span data-ttu-id="68e8e-129">有关详细信息，请参阅[声明上下文和默认访问级别](declaration-contexts-and-default-access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="68e8e-129">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>  
  
 <span data-ttu-id="68e8e-130">可以在另一个命名空间中声明一个命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-130">You can declare one namespace within another.</span></span> <span data-ttu-id="68e8e-131">您可以声明的嵌套级别没有严格限制，但是请记住，如果其他代码访问在最内层命名空间中声明的元素，则必须使用包含嵌套层次结构中所有命名空间名称的限定字符串。</span><span class="sxs-lookup"><span data-stu-id="68e8e-131">There is no strict limit to the levels of nesting you can declare, but remember that when other code accesses the elements declared in the innermost namespace, it must use a qualification string that contains all the namespace names in the nesting hierarchy.</span></span>  
  
## <a name="access-level"></a><span data-ttu-id="68e8e-132">访问级别</span><span class="sxs-lookup"><span data-stu-id="68e8e-132">Access Level</span></span>  

 <span data-ttu-id="68e8e-133">命名空间将被视为具有 `Public` 访问级别。</span><span class="sxs-lookup"><span data-stu-id="68e8e-133">Namespaces are treated as if they have a `Public` access level.</span></span> <span data-ttu-id="68e8e-134">可以从同一项目中的任何位置、引用该项目的其他项目以及从项目生成的任何程序集访问该命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-134">A namespace can be accessed from code anywhere in the same project, from other projects that reference the project, and from any assembly built from the project.</span></span>  
  
 <span data-ttu-id="68e8e-135">在命名空间级别声明的编程元素（在命名空间中，而不是在任何其他元素内）可以具有 `Public` 或 `Friend` 访问。</span><span class="sxs-lookup"><span data-stu-id="68e8e-135">Programming elements declared at namespace level, meaning in a namespace but not inside any other element, can have `Public` or `Friend` access.</span></span> <span data-ttu-id="68e8e-136">如果未指定，则默认情况下，此类元素的访问级别使用 `Friend` 。</span><span class="sxs-lookup"><span data-stu-id="68e8e-136">If unspecified, the access level of such an element uses `Friend` by default.</span></span> <span data-ttu-id="68e8e-137">可在命名空间级别声明的元素包括类、结构、模块、接口、枚举和委托。</span><span class="sxs-lookup"><span data-stu-id="68e8e-137">Elements you can declare at namespace level include classes, structures, modules, interfaces, enumerations, and delegates.</span></span> <span data-ttu-id="68e8e-138">有关详细信息，请参阅[声明上下文和默认访问级别](declaration-contexts-and-default-access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="68e8e-138">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>  
  
## <a name="root-namespace"></a><span data-ttu-id="68e8e-139">根命名空间</span><span class="sxs-lookup"><span data-stu-id="68e8e-139">Root Namespace</span></span>  

 <span data-ttu-id="68e8e-140">项目中的所有命名空间名称都基于 *根命名空间*。</span><span class="sxs-lookup"><span data-stu-id="68e8e-140">All namespace names in your project are based on a *root namespace*.</span></span> <span data-ttu-id="68e8e-141">Visual Studio 针对项目中的所有代码，将项目名称指定为默认根命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-141">Visual Studio assigns your project name as the default root namespace for all code in your project.</span></span> <span data-ttu-id="68e8e-142">例如，如果项目命名为 `Payroll`，则其编程元素属于命名空间 `Payroll`。</span><span class="sxs-lookup"><span data-stu-id="68e8e-142">For example, if your project is named `Payroll`, its programming elements belong to namespace `Payroll`.</span></span> <span data-ttu-id="68e8e-143">如果声明 `Namespace funding` ，则该命名空间的完整名称为 `Payroll.funding` 。</span><span class="sxs-lookup"><span data-stu-id="68e8e-143">If you declare `Namespace funding`, the full name of that namespace is `Payroll.funding`.</span></span>  
  
 <span data-ttu-id="68e8e-144">如果要在语句中指定现有命名空间（ `Namespace` 如泛型列表类示例中所示），可以将根命名空间设置为 null 值。</span><span class="sxs-lookup"><span data-stu-id="68e8e-144">If you want to specify an existing namespace in a `Namespace` statement, such as in the generic list class example, you can set your root namespace to a null value.</span></span> <span data-ttu-id="68e8e-145">为此，请单击 "**项目**" 菜单中的 "**项目属性**"，然后清除 "**根命名空间**" 条目，以便此框为空。</span><span class="sxs-lookup"><span data-stu-id="68e8e-145">To do this, click **Project Properties** from the **Project** menu and then clear the **Root namespace** entry so that the box is empty.</span></span> <span data-ttu-id="68e8e-146">如果未在泛型列表类示例中执行此操作，则 Visual Basic 编译器会将 `System.Collections.Generic` 项目中的新命名空间作为的 `Payroll` 完整名称 `Payroll.System.Collections.Generic` 。</span><span class="sxs-lookup"><span data-stu-id="68e8e-146">If you did not do this in the generic list class example, the Visual Basic compiler would take `System.Collections.Generic` as a new namespace within project `Payroll`, with the full name of `Payroll.System.Collections.Generic`.</span></span>  
  
 <span data-ttu-id="68e8e-147">或者，可以使用 `Global` 关键字来引用在项目外部定义的命名空间的元素。</span><span class="sxs-lookup"><span data-stu-id="68e8e-147">Alternatively, you can use the `Global` keyword to refer to elements of namespaces defined outside your project.</span></span> <span data-ttu-id="68e8e-148">这样做可以使项目名称保留为根命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-148">Doing so lets you retain your project name as the root namespace.</span></span> <span data-ttu-id="68e8e-149">这可以减少无意中将您的编程元素与现有命名空间的合并。</span><span class="sxs-lookup"><span data-stu-id="68e8e-149">This reduces the chance of unintentionally merging your programming elements together with those of existing namespaces.</span></span> <span data-ttu-id="68e8e-150">有关详细信息，请参阅 [Visual Basic 中命名空间](../../programming-guide/program-structure/namespaces.md)的 "完全限定名称中的全局关键字" 部分。</span><span class="sxs-lookup"><span data-stu-id="68e8e-150">For more information, see the "Global Keyword in Fully Qualified Names" section in [Namespaces in Visual Basic](../../programming-guide/program-structure/namespaces.md).</span></span>  
  
 <span data-ttu-id="68e8e-151">`Global`关键字还可以在命名空间语句中使用。</span><span class="sxs-lookup"><span data-stu-id="68e8e-151">The `Global` keyword can also be used in a Namespace statement.</span></span> <span data-ttu-id="68e8e-152">这将允许你定义项目根命名空间之外的命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-152">This lets you define a namespace out of the root namespace of your project.</span></span> <span data-ttu-id="68e8e-153">有关详细信息，请参阅 [Visual Basic 的命名空间](../../programming-guide/program-structure/namespaces.md)中的 "命名空间语句中的全局关键字" 部分。</span><span class="sxs-lookup"><span data-stu-id="68e8e-153">For more information, see the "Global Keyword in Namespace Statements" section in [Namespaces in Visual Basic](../../programming-guide/program-structure/namespaces.md).</span></span>  
  
 <span data-ttu-id="68e8e-154">**有关.**</span><span class="sxs-lookup"><span data-stu-id="68e8e-154">**Troubleshooting.**</span></span> <span data-ttu-id="68e8e-155">根命名空间可能会导致命名空间名称出现意外的串联。</span><span class="sxs-lookup"><span data-stu-id="68e8e-155">The root namespace can lead to unexpected concatenations of namespace names.</span></span> <span data-ttu-id="68e8e-156">如果你引用在项目外部定义的命名空间，则 Visual Basic 编译器可以将它们作为根命名空间中的嵌套命名空间 construe。</span><span class="sxs-lookup"><span data-stu-id="68e8e-156">If you make reference to namespaces defined outside your project, the Visual Basic compiler can construe them as nested namespaces in the root namespace.</span></span> <span data-ttu-id="68e8e-157">在这种情况下，编译器不能识别已在外部命名空间中定义的任何类型。</span><span class="sxs-lookup"><span data-stu-id="68e8e-157">In such a case, the compiler does not recognize any types that have been already defined in the external namespaces.</span></span> <span data-ttu-id="68e8e-158">若要避免这种情况，请将根命名空间设置为空值（如 "根命名空间" 中所述）或使用 `Global` 关键字访问外部命名空间的元素。</span><span class="sxs-lookup"><span data-stu-id="68e8e-158">To avoid this, either set your root namespace to a null value as described in "Root Namespace," or use the `Global` keyword to access elements of external namespaces.</span></span>  
  
## <a name="attributes-and-modifiers"></a><span data-ttu-id="68e8e-159">特性和修饰符</span><span class="sxs-lookup"><span data-stu-id="68e8e-159">Attributes and Modifiers</span></span>  

 <span data-ttu-id="68e8e-160">不能将属性应用到命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-160">You cannot apply attributes to a namespace.</span></span> <span data-ttu-id="68e8e-161">特性向程序集的元数据提供信息，这对于源分类器（如命名空间）没有意义。</span><span class="sxs-lookup"><span data-stu-id="68e8e-161">An attribute contributes information to the assembly's metadata, which is not meaningful for source classifiers such as namespaces.</span></span>  
  
 <span data-ttu-id="68e8e-162">不能将任何访问或过程修饰符或任何其他修饰符应用到命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-162">You cannot apply any access or procedure modifiers, or any other modifiers, to a namespace.</span></span> <span data-ttu-id="68e8e-163">由于这不是类型，因此这些修饰符没有意义。</span><span class="sxs-lookup"><span data-stu-id="68e8e-163">Because it is not a type, these modifiers are not meaningful.</span></span>  
  
## <a name="example"></a><span data-ttu-id="68e8e-164">示例</span><span class="sxs-lookup"><span data-stu-id="68e8e-164">Example</span></span>  

 <span data-ttu-id="68e8e-165">下面的示例声明了两个命名空间，一个嵌套在另一个。</span><span class="sxs-lookup"><span data-stu-id="68e8e-165">The following example declares two namespaces, one nested in the other.</span></span>  
  
 [!code-vb[VbVbalrStatements#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#43)]  
  
## <a name="example"></a><span data-ttu-id="68e8e-166">示例</span><span class="sxs-lookup"><span data-stu-id="68e8e-166">Example</span></span>  

 <span data-ttu-id="68e8e-167">下面的示例在一行上声明多个嵌套命名空间，并且它等效于前面的示例。</span><span class="sxs-lookup"><span data-stu-id="68e8e-167">The following example declares multiple nested namespaces on a single line, and it is equivalent to the previous example.</span></span>  
  
 [!code-vb[VbVbalrStatements#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#41)]  
  
## <a name="example"></a><span data-ttu-id="68e8e-168">示例</span><span class="sxs-lookup"><span data-stu-id="68e8e-168">Example</span></span>  

 <span data-ttu-id="68e8e-169">以下示例访问在前面的示例中定义的类。</span><span class="sxs-lookup"><span data-stu-id="68e8e-169">The following example accesses the class defined in the previous examples.</span></span>  
  
 [!code-vb[VbVbalrStatements#42](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#42)]  
  
## <a name="example"></a><span data-ttu-id="68e8e-170">示例</span><span class="sxs-lookup"><span data-stu-id="68e8e-170">Example</span></span>  

 <span data-ttu-id="68e8e-171">下面的示例定义了一个新的泛型列表类的主干，并将其添加到了 <xref:System.Collections.Generic?displayProperty=nameWithType> 命名空间。</span><span class="sxs-lookup"><span data-stu-id="68e8e-171">The following example defines the skeleton of a new generic list class and adds it to the <xref:System.Collections.Generic?displayProperty=nameWithType> namespace.</span></span>  
  
```vb  
Namespace System.Collections.Generic  
    Class specialSortedList(Of T)  
        Inherits List(Of T)  
        ' Insert code to define the special generic list class.  
    End Class  
End Namespace  
```  
  
## <a name="see-also"></a><span data-ttu-id="68e8e-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="68e8e-172">See also</span></span>

- [<span data-ttu-id="68e8e-173">Imports 语句（.NET 命名空间和类型）</span><span class="sxs-lookup"><span data-stu-id="68e8e-173">Imports Statement (.NET Namespace and Type)</span></span>](imports-statement-net-namespace-and-type.md)
- [<span data-ttu-id="68e8e-174">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="68e8e-174">Declared Element Names</span></span>](../../programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="68e8e-175">Visual Basic 中的命名空间</span><span class="sxs-lookup"><span data-stu-id="68e8e-175">Namespaces in Visual Basic</span></span>](../../programming-guide/program-structure/namespaces.md)
