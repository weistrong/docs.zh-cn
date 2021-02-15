---
description: '了解详细信息：引用 (Visual Basic 的已声明元素) '
title: References to Declared Elements
ms.date: 07/20/2015
helpviewer_keywords:
- declared elements [Visual Basic]
- references [Visual Basic], declared elements
- qualified names [Visual Basic]
ms.assetid: d6301709-f4cc-4b7a-b8ba-80898f14ab46
ms.openlocfilehash: 75cc05381f01af00ac75995739647810fb7ff1d7
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100471430"
---
# <a name="references-to-declared-elements-visual-basic"></a><span data-ttu-id="4a209-103">对已声明元素的引用 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4a209-103">References to Declared Elements (Visual Basic)</span></span>

<span data-ttu-id="4a209-104">当代码引用已声明的元素时，Visual Basic 编译器会将引用中的名称与该名称的相应声明进行匹配。</span><span class="sxs-lookup"><span data-stu-id="4a209-104">When your code refers to a declared element, the Visual Basic compiler matches the name in your reference to the appropriate declaration of that name.</span></span> <span data-ttu-id="4a209-105">如果用相同的名称声明了多个元素，则可以通过 *限定* 其名称来控制要引用的元素。</span><span class="sxs-lookup"><span data-stu-id="4a209-105">If more than one element is declared with the same name, you can control which of those elements is to be referenced by *qualifying* its name.</span></span>  
  
 <span data-ttu-id="4a209-106">编译器尝试将名称引用与最 *窄的范围* 进行匹配。</span><span class="sxs-lookup"><span data-stu-id="4a209-106">The compiler attempts to match a name reference to a name declaration with the *narrowest scope*.</span></span> <span data-ttu-id="4a209-107">这意味着，它从发出引用的代码开始，并通过连续的包含元素级别进行处理。</span><span class="sxs-lookup"><span data-stu-id="4a209-107">This means it starts with the code making the reference and works outward through successive levels of containing elements.</span></span>  
  
 <span data-ttu-id="4a209-108">下面的示例显示对两个名称相同的变量的引用。</span><span class="sxs-lookup"><span data-stu-id="4a209-108">The following example shows references to two variables with the same name.</span></span> <span data-ttu-id="4a209-109">该示例在 `totalCount` 模块的不同范围内声明了两个变量，每个变量都命名为 `container` 。</span><span class="sxs-lookup"><span data-stu-id="4a209-109">The example declares two variables, each named `totalCount`, at different levels of scope in module `container`.</span></span> <span data-ttu-id="4a209-110">如果过程 `showCount` 显示时 `totalCount` 未进行限定，则 Visual Basic 编译器会将引用解析为范围最窄的声明，即内的本地声明 `showCount` 。</span><span class="sxs-lookup"><span data-stu-id="4a209-110">When the procedure `showCount` displays `totalCount` without qualification, the Visual Basic compiler resolves the reference to the declaration with the narrowest scope, namely the local declaration inside `showCount`.</span></span> <span data-ttu-id="4a209-111">当它符合 `totalCount` 包含模块时 `container` ，编译器会将引用解析为范围更广的声明。</span><span class="sxs-lookup"><span data-stu-id="4a209-111">When it qualifies `totalCount` with the containing module `container`, the compiler resolves the reference to the declaration with the broader scope.</span></span>  
  
```vb  
' Assume these two modules are both in the same assembly.  
Module container  
    Public totalCount As Integer = 1  
    Public Sub showCount()  
        Dim totalCount As Integer = 6000  
        ' The following statement displays the local totalCount (6000).  
        MsgBox("Unqualified totalCount is " & CStr(totalCount))  
        ' The following statement displays the module's totalCount (1).  
        MsgBox("container.totalCount is " & CStr(container.totalCount))  
    End Sub  
End Module  
Module callingModule  
    Public Sub displayCount()  
        container.showCount()  
        ' The following statement displays the containing module's totalCount (1).  
        MsgBox("container.totalCount is " & CStr(container.totalCount))  
    End Sub  
End Module  
```  
  
## <a name="qualifying-an-element-name"></a><span data-ttu-id="4a209-112">限定元素名称</span><span class="sxs-lookup"><span data-stu-id="4a209-112">Qualifying an Element Name</span></span>  

 <span data-ttu-id="4a209-113">如果要重写此搜索过程并指定在更大范围内声明的名称，则必须使用范围更广的包含元素 *限定* 该名称。</span><span class="sxs-lookup"><span data-stu-id="4a209-113">If you want to override this search process and specify a name declared in a broader scope, you must *qualify* the name with the containing element of the broader scope.</span></span> <span data-ttu-id="4a209-114">在某些情况下，你可能还必须限定包含元素。</span><span class="sxs-lookup"><span data-stu-id="4a209-114">In some cases, you might also have to qualify the containing element.</span></span>  
  
 <span data-ttu-id="4a209-115">限定名称表示在源语句中使用标识目标元素定义位置的信息。</span><span class="sxs-lookup"><span data-stu-id="4a209-115">Qualifying a name means preceding it in your source statement with information that identifies where the target element is defined.</span></span> <span data-ttu-id="4a209-116">此信息称为 *限定字符串*。</span><span class="sxs-lookup"><span data-stu-id="4a209-116">This information is called a *qualification string*.</span></span> <span data-ttu-id="4a209-117">它可以包含一个或多个命名空间以及模块、类或结构。</span><span class="sxs-lookup"><span data-stu-id="4a209-117">It can include one or more namespaces and a module, class, or structure.</span></span>  
  
 <span data-ttu-id="4a209-118">限定字符串应明确指定包含目标元素的模块、类或结构。</span><span class="sxs-lookup"><span data-stu-id="4a209-118">The qualification string should unambiguously specify the module, class, or structure containing the target element.</span></span> <span data-ttu-id="4a209-119">容器可能又位于另一个包含元素中，通常是一个命名空间。</span><span class="sxs-lookup"><span data-stu-id="4a209-119">The container might in turn be located in another containing element, usually a namespace.</span></span> <span data-ttu-id="4a209-120">你可能需要在限定字符串中包含多个包含元素。</span><span class="sxs-lookup"><span data-stu-id="4a209-120">You might need to include several containing elements in the qualification string.</span></span>  
  
#### <a name="to-access-a-declared-element-by-qualifying-its-name"></a><span data-ttu-id="4a209-121">通过限定其名称访问声明的元素</span><span class="sxs-lookup"><span data-stu-id="4a209-121">To access a declared element by qualifying its name</span></span>  
  
1. <span data-ttu-id="4a209-122">确定定义元素的位置。</span><span class="sxs-lookup"><span data-stu-id="4a209-122">Determine the location in which the element has been defined.</span></span> <span data-ttu-id="4a209-123">这可能包括命名空间，甚至命名空间的层次结构。</span><span class="sxs-lookup"><span data-stu-id="4a209-123">This might include a namespace, or even a hierarchy of namespaces.</span></span> <span data-ttu-id="4a209-124">在最低级别的命名空间中，元素必须包含在模块、类或结构中。</span><span class="sxs-lookup"><span data-stu-id="4a209-124">Within the lowest-level namespace, the element must be contained in a module, class, or structure.</span></span>  
  
    ```vb  
    ' Assume the following hierarchy exists outside your code.  
    Namespace outerSpace  
        Namespace innerSpace  
            Module holdsTotals  
                Public Structure totals  
                    Public thisTotal As Integer  
                    Public Shared grandTotal As Long  
                End Structure  
            End Module  
        End Namespace  
    End Namespace  
    ```  
  
2. <span data-ttu-id="4a209-125">根据目标元素的位置确定限定路径。</span><span class="sxs-lookup"><span data-stu-id="4a209-125">Determine a qualification path based on the target element's location.</span></span> <span data-ttu-id="4a209-126">从最高层命名空间开始，转到最低级别命名空间，并以包含目标元素的模块、类或结构结尾。</span><span class="sxs-lookup"><span data-stu-id="4a209-126">Start with the highest-level namespace, proceed to the lowest-level namespace, and end with the module, class, or structure containing the target element.</span></span> <span data-ttu-id="4a209-127">路径中的每个元素都必须包含其后的元素。</span><span class="sxs-lookup"><span data-stu-id="4a209-127">Each element in the path must contain the element that follows it.</span></span>  
  
     <span data-ttu-id="4a209-128">`outerSpace` → `innerSpace` → `holdsTotals` → `totals`</span><span class="sxs-lookup"><span data-stu-id="4a209-128">`outerSpace` → `innerSpace` → `holdsTotals` → `totals`</span></span>  
  
3. <span data-ttu-id="4a209-129">准备目标元素的限定字符串。</span><span class="sxs-lookup"><span data-stu-id="4a209-129">Prepare the qualification string for the target element.</span></span> <span data-ttu-id="4a209-130">将一个句点 (在 `.` 路径中的每个元素之后) 。</span><span class="sxs-lookup"><span data-stu-id="4a209-130">Place a period (`.`) after every element in the path.</span></span> <span data-ttu-id="4a209-131">应用程序必须有权访问限定字符串中的每个元素。</span><span class="sxs-lookup"><span data-stu-id="4a209-131">Your application must have access to every element in your qualification string.</span></span>  
  
    ```vb  
    outerSpace.innerSpace.holdsTotals.totals.  
    ```  
  
4. <span data-ttu-id="4a209-132">以正常方式编写引用目标元素的表达式或赋值语句。</span><span class="sxs-lookup"><span data-stu-id="4a209-132">Write the expression or assignment statement referring to the target element in the normal way.</span></span>  
  
    ```vb  
    grandTotal = 9000  
    ```  
  
5. <span data-ttu-id="4a209-133">在目标元素名称之前加上限定字符串。</span><span class="sxs-lookup"><span data-stu-id="4a209-133">Precede the target element name with the qualification string.</span></span> <span data-ttu-id="4a209-134">该名称应紧跟 `.` 在包含元素的模块、类或结构 () 时间段之后。</span><span class="sxs-lookup"><span data-stu-id="4a209-134">The name should immediately follow the period (`.`) that follows the module, class, or structure that contains the element.</span></span>  
  
    ```vb  
    ' Assume the following module is part of your code.  
    Module accessGrandTotal  
        Public Sub setGrandTotal()  
            outerSpace.innerSpace.holdsTotals.totals.grandTotal = 9000  
        End Sub  
    End Module  
    ```  
  
6. <span data-ttu-id="4a209-135">编译器使用限定字符串来查找可与目标元素引用匹配的明确、明确的声明。</span><span class="sxs-lookup"><span data-stu-id="4a209-135">The compiler uses the qualification string to find a clear, unambiguous declaration to which it can match the target element reference.</span></span>  
  
 <span data-ttu-id="4a209-136">如果你的应用程序有权访问多个具有相同名称的编程元素，则可能还必须限定名称引用。</span><span class="sxs-lookup"><span data-stu-id="4a209-136">You might also have to qualify a name reference if your application has access to more than one programming element that has the same name.</span></span> <span data-ttu-id="4a209-137">例如， <xref:System.Windows.Forms> 和 <xref:System.Web.UI.WebControls> 命名空间都包含一个 `Label` 类 (<xref:System.Windows.Forms.Label?displayProperty=nameWithType> 和 <xref:System.Web.UI.WebControls.Label?displayProperty=nameWithType>) 。</span><span class="sxs-lookup"><span data-stu-id="4a209-137">For example, the <xref:System.Windows.Forms> and <xref:System.Web.UI.WebControls> namespaces both contain a `Label` class (<xref:System.Windows.Forms.Label?displayProperty=nameWithType> and <xref:System.Web.UI.WebControls.Label?displayProperty=nameWithType>).</span></span> <span data-ttu-id="4a209-138">如果你的应用程序同时使用这两个，或者它定义自己的 `Label` 类，则必须区分不同的 `Label` 对象。</span><span class="sxs-lookup"><span data-stu-id="4a209-138">If your application uses both, or if it defines its own `Label` class, you must distinguish the different `Label` objects.</span></span> <span data-ttu-id="4a209-139">在变量声明中包含命名空间或导入别名。</span><span class="sxs-lookup"><span data-stu-id="4a209-139">Include the namespace or import alias in the variable declaration.</span></span> <span data-ttu-id="4a209-140">下面的示例使用了导入别名。</span><span class="sxs-lookup"><span data-stu-id="4a209-140">The following example uses the import alias.</span></span>  
  
```vb  
' The following statement must precede all your declarations.  
Imports win = System.Windows.Forms, web = System.Web.UI.WebControls  
' The following statement references the Windows.Forms.Label class.  
Dim winLabel As New win.Label()  
```  
  
## <a name="members-of-other-containing-elements"></a><span data-ttu-id="4a209-141">其他包含元素的成员</span><span class="sxs-lookup"><span data-stu-id="4a209-141">Members of Other Containing Elements</span></span>  

 <span data-ttu-id="4a209-142">如果使用其他类或结构的非共享成员，则必须先使用指向类或结构的实例的变量或表达式来限定成员名称。</span><span class="sxs-lookup"><span data-stu-id="4a209-142">When you use a nonshared member of another class or structure, you must first qualify the member name with a variable or expression that points to an instance of the class or structure.</span></span> <span data-ttu-id="4a209-143">在下面的示例中， `demoClass` 是名为的类的实例 `class1` 。</span><span class="sxs-lookup"><span data-stu-id="4a209-143">In the following example, `demoClass` is an instance of a class named `class1`.</span></span>  
  
```vb  
Dim demoClass As class1 = New class1()  
demoClass.someSub[(argumentlist)]  
```  
  
 <span data-ttu-id="4a209-144">不能使用类名本身来限定未 [共享](../../../language-reference/modifiers/shared.md)的成员。</span><span class="sxs-lookup"><span data-stu-id="4a209-144">You cannot use the class name itself to qualify a member that is not [Shared](../../../language-reference/modifiers/shared.md).</span></span> <span data-ttu-id="4a209-145">在此示例中，您必须首先在对象 (变量中创建实例 `demoClass`) 然后通过变量名称引用它。</span><span class="sxs-lookup"><span data-stu-id="4a209-145">You must first create an instance in an object variable (in this case `demoClass`) and then reference it by the variable name.</span></span>  
  
 <span data-ttu-id="4a209-146">如果某个类或结构具有 `Shared` 成员，则可以使用类或结构名称或指向实例的变量或表达式来限定该成员。</span><span class="sxs-lookup"><span data-stu-id="4a209-146">If a class or structure has a `Shared` member, you can qualify that member either with the class or structure name or with a variable or expression that points to an instance.</span></span>  
  
 <span data-ttu-id="4a209-147">模块没有任何单独的实例，并且默认情况下其所有成员均为 `Shared` 。</span><span class="sxs-lookup"><span data-stu-id="4a209-147">A module does not have any separate instances, and all its members are `Shared` by default.</span></span> <span data-ttu-id="4a209-148">因此，您可以使用模块名称限定模块成员。</span><span class="sxs-lookup"><span data-stu-id="4a209-148">Therefore, you qualify a module member with the module name.</span></span>  
  
 <span data-ttu-id="4a209-149">下面的示例演示对模块成员过程的限定引用。</span><span class="sxs-lookup"><span data-stu-id="4a209-149">The following example shows qualified references to module member procedures.</span></span> <span data-ttu-id="4a209-150">该示例 `Sub` `perform` 在项目的不同模块中声明了两个名为的过程。</span><span class="sxs-lookup"><span data-stu-id="4a209-150">The example declares two `Sub` procedures, both named `perform`, in different modules in a project.</span></span> <span data-ttu-id="4a209-151">可以在其自身的模块中无需限定地指定每个项，但在其他任何地方引用时必须进行限定。</span><span class="sxs-lookup"><span data-stu-id="4a209-151">Each one can be specified without qualification within its own module but must be qualified if referenced from anywhere else.</span></span> <span data-ttu-id="4a209-152">因为中的最后一个引用 `module3` 不符合条件 `perform` ，所以编译器无法解析该引用。</span><span class="sxs-lookup"><span data-stu-id="4a209-152">Because the final reference in `module3` does not qualify `perform`, the compiler cannot resolve that reference.</span></span>  
  
```vb  
' Assume these three modules are all in the same assembly.  
Module module1  
    Public Sub perform()  
        MsgBox("module1.perform() now returning")  
    End Sub  
End Module  
Module module2  
    Public Sub perform()  
        MsgBox("module2.perform() now returning")  
    End Sub  
    Public Sub doSomething()  
        ' The following statement calls perform in module2, the active module.  
        perform()  
        ' The following statement calls perform in module1.  
        module1.perform()  
    End Sub  
End Module  
Module module3  
    Public Sub callPerform()  
        ' The following statement calls perform in module1.  
        module1.perform()  
        ' The following statement makes an unresolvable name reference  
        ' and therefore generates a COMPILER ERROR.  
        perform() ' INVALID statement  
    End Sub  
End Module  
```  
  
## <a name="references-to-projects"></a><span data-ttu-id="4a209-153">对项目的引用</span><span class="sxs-lookup"><span data-stu-id="4a209-153">References to Projects</span></span>  

 <span data-ttu-id="4a209-154">若要使用另一个项目中定义的 [公共](../../../language-reference/modifiers/public.md) 元素，必须首先设置对该项目的程序集或类型库的 *引用* 。</span><span class="sxs-lookup"><span data-stu-id="4a209-154">To use [Public](../../../language-reference/modifiers/public.md) elements defined in another project, you must first set a *reference* to that project's assembly or type library.</span></span> <span data-ttu-id="4a209-155">若要设置引用，请在 "**项目**" 菜单上单击 "**添加引用**"，或使用 [引用 (Visual Basic)](../../../reference/command-line-compiler/reference.md)命令行编译器选项。</span><span class="sxs-lookup"><span data-stu-id="4a209-155">To set a reference, click **Add Reference** on the **Project** menu, or use the [-reference (Visual Basic)](../../../reference/command-line-compiler/reference.md) command-line compiler option.</span></span>  
  
 <span data-ttu-id="4a209-156">例如，可以使用 .NET Framework 的 XML 对象模型。</span><span class="sxs-lookup"><span data-stu-id="4a209-156">For example, you can use the XML object model of the .NET Framework.</span></span> <span data-ttu-id="4a209-157">如果设置了对 <xref:System.Xml> 命名空间的引用，则可以声明并使用它的任何类，如 <xref:System.Xml.XmlDocument> 。</span><span class="sxs-lookup"><span data-stu-id="4a209-157">If you set a reference to the <xref:System.Xml> namespace, you can declare and use any of its classes, such as <xref:System.Xml.XmlDocument>.</span></span> <span data-ttu-id="4a209-158">下面的示例使用 <xref:System.Xml.XmlDocument>。</span><span class="sxs-lookup"><span data-stu-id="4a209-158">The following example uses <xref:System.Xml.XmlDocument>.</span></span>  
  
```vb  
' Assume this project has a reference to System.Xml  
' The following statement creates xDoc as an XML document object.  
Dim xDoc As System.Xml.XmlDocument  
```  
  
## <a name="importing-containing-elements"></a><span data-ttu-id="4a209-159">导入包含元素</span><span class="sxs-lookup"><span data-stu-id="4a209-159">Importing Containing Elements</span></span>  

 <span data-ttu-id="4a209-160">您可以使用 import [语句 ( .Net 命名空间，并键入)](../../../language-reference/statements/imports-statement-net-namespace-and-type.md) 以 *导入* 包含您要使用的模块或类的命名空间。</span><span class="sxs-lookup"><span data-stu-id="4a209-160">You can use the [Imports Statement (.NET Namespace and Type)](../../../language-reference/statements/imports-statement-net-namespace-and-type.md) to *import* the namespaces that contain the modules or classes that you want to use.</span></span> <span data-ttu-id="4a209-161">这使您可以引用在导入的命名空间中定义的元素，而无需完全限定其名称。</span><span class="sxs-lookup"><span data-stu-id="4a209-161">This enables you to refer to the elements defined in an imported namespace without fully qualifying their names.</span></span> <span data-ttu-id="4a209-162">下面的示例重写上一示例以导入 <xref:System.Xml> 命名空间。</span><span class="sxs-lookup"><span data-stu-id="4a209-162">The following example rewrites the previous example to import the <xref:System.Xml> namespace.</span></span>  
  
```vb  
' Assume this project has a reference to System.Xml  
' The following statement must precede all your declarations.  
Imports System.Xml  
' The following statement creates xDoc as an XML document object.  
Dim xDoc As XmlDocument  
```  
  
 <span data-ttu-id="4a209-163">此外， `Imports` 语句可以为每个导入的命名空间定义 *导入别名* 。</span><span class="sxs-lookup"><span data-stu-id="4a209-163">In addition, the `Imports` statement can define an *import alias* for each imported namespace.</span></span> <span data-ttu-id="4a209-164">这会使源代码更短且更易于阅读。</span><span class="sxs-lookup"><span data-stu-id="4a209-164">This can make the source code shorter and easier to read.</span></span> <span data-ttu-id="4a209-165">下面的示例重写上一个示例，以 `xD` 用作 <xref:System.Xml> 命名空间的别名。</span><span class="sxs-lookup"><span data-stu-id="4a209-165">The following example rewrites the previous example to use `xD` as an alias for the <xref:System.Xml> namespace.</span></span>  
  
```vb  
' Assume this project has a reference to System.Xml  
' The following statement must precede all your declarations.  
Imports xD = System.Xml  
' The following statement creates xDoc as an XML document object.  
Dim xDoc As xD.XmlDocument  
```  
  
 <span data-ttu-id="4a209-166">`Imports`语句不会使其他项目中的元素可用于你的应用程序。</span><span class="sxs-lookup"><span data-stu-id="4a209-166">The `Imports` statement does not make elements from other projects available to your application.</span></span> <span data-ttu-id="4a209-167">也就是说，它不会取代设置引用。</span><span class="sxs-lookup"><span data-stu-id="4a209-167">That is, it does not take the place of setting a reference.</span></span> <span data-ttu-id="4a209-168">导入命名空间只是不再要求限定命名空间中定义的名称。</span><span class="sxs-lookup"><span data-stu-id="4a209-168">Importing a namespace just removes the requirement to qualify the names defined in that namespace.</span></span>  
  
 <span data-ttu-id="4a209-169">你还可以使用 `Imports` 语句来导入模块、类、结构和枚举。</span><span class="sxs-lookup"><span data-stu-id="4a209-169">You can also use the `Imports` statement to import modules, classes, structures, and enumerations.</span></span> <span data-ttu-id="4a209-170">然后，可以使用此类导入元素的成员而无需进行限定。</span><span class="sxs-lookup"><span data-stu-id="4a209-170">You can then use the members of such imported elements without qualification.</span></span> <span data-ttu-id="4a209-171">但是，必须始终使用计算结果为类或结构的实例的变量或表达式来限定类和结构的非共享成员。</span><span class="sxs-lookup"><span data-stu-id="4a209-171">However, you must always qualify nonshared members of classes and structures with a variable or expression that evaluates to an instance of the class or structure.</span></span>  
  
## <a name="naming-guidelines"></a><span data-ttu-id="4a209-172">命名准则</span><span class="sxs-lookup"><span data-stu-id="4a209-172">Naming Guidelines</span></span>  

 <span data-ttu-id="4a209-173">在定义两个或多个具有相同名称的编程元素时，当编译器尝试解析对该名称的引用时，可能会导致 *名称不明确* 。</span><span class="sxs-lookup"><span data-stu-id="4a209-173">When you define two or more programming elements that have the same name, a *name ambiguity* can result when the compiler attempts to resolve a reference to that name.</span></span> <span data-ttu-id="4a209-174">如果范围内有多个定义，或者如果没有定义在范围内，则引用为不能纠正。</span><span class="sxs-lookup"><span data-stu-id="4a209-174">If more than one definition is in scope, or if no definition is in scope, the reference is irresolvable.</span></span> <span data-ttu-id="4a209-175">有关示例，请参阅此帮助页上的 "限定引用示例"。</span><span class="sxs-lookup"><span data-stu-id="4a209-175">For an example, see "Qualified Reference Example" on this Help page.</span></span>  
  
 <span data-ttu-id="4a209-176">可以通过提供所有元素的唯一名称来避免名称不明确。</span><span class="sxs-lookup"><span data-stu-id="4a209-176">You can avoid name ambiguity by giving all your elements unique names.</span></span> <span data-ttu-id="4a209-177">然后，可以引用任何元素，而无需使用命名空间、模块或类限定其名称。</span><span class="sxs-lookup"><span data-stu-id="4a209-177">Then you can make reference to any element without having to qualify its name with a namespace, module, or class.</span></span> <span data-ttu-id="4a209-178">您还可以减少意外引用错误元素的几率。</span><span class="sxs-lookup"><span data-stu-id="4a209-178">You also reduce the chances of accidentally referring to the wrong element.</span></span>  
  
## <a name="shadowing"></a><span data-ttu-id="4a209-179">阴影操作</span><span class="sxs-lookup"><span data-stu-id="4a209-179">Shadowing</span></span>  

 <span data-ttu-id="4a209-180">当两个编程元素共享同一名称时，其中一个元素可以 *隐藏或隐藏* 另一个。</span><span class="sxs-lookup"><span data-stu-id="4a209-180">When two programming elements share the same name, one of them can hide, or *shadow*, the other one.</span></span> <span data-ttu-id="4a209-181">隐藏的元素不可用于引用;相反，当代码使用隐藏的元素名称时，Visual Basic 编译器会将其解析为隐藏元素。</span><span class="sxs-lookup"><span data-stu-id="4a209-181">A shadowed element is not available for reference; instead, when your code uses the shadowed element name, the Visual Basic compiler resolves it to the shadowing element.</span></span> <span data-ttu-id="4a209-182">有关示例的更详细说明，请参阅 [Visual Basic 中的隐藏](shadowing.md)。</span><span class="sxs-lookup"><span data-stu-id="4a209-182">For a more detailed explanation with examples, see [Shadowing in Visual Basic](shadowing.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a209-183">请参阅</span><span class="sxs-lookup"><span data-stu-id="4a209-183">See also</span></span>

- [<span data-ttu-id="4a209-184">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="4a209-184">Declared Element Names</span></span>](declared-element-names.md)
- [<span data-ttu-id="4a209-185">已声明元素的特性</span><span class="sxs-lookup"><span data-stu-id="4a209-185">Declared Element Characteristics</span></span>](declared-element-characteristics.md)
- [<span data-ttu-id="4a209-186">管理项目和解决方案属性</span><span class="sxs-lookup"><span data-stu-id="4a209-186">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
- [<span data-ttu-id="4a209-187">变量</span><span class="sxs-lookup"><span data-stu-id="4a209-187">Variables</span></span>](../variables/index.md)
- [<span data-ttu-id="4a209-188">Imports 语句（.NET 命名空间和类型）</span><span class="sxs-lookup"><span data-stu-id="4a209-188">Imports Statement (.NET Namespace and Type)</span></span>](../../../language-reference/statements/imports-statement-net-namespace-and-type.md)
- [<span data-ttu-id="4a209-189">新建操作员</span><span class="sxs-lookup"><span data-stu-id="4a209-189">New Operator</span></span>](../../../language-reference/operators/new-operator.md)
- [<span data-ttu-id="4a209-190">公共</span><span class="sxs-lookup"><span data-stu-id="4a209-190">Public</span></span>](../../../language-reference/modifiers/public.md)
