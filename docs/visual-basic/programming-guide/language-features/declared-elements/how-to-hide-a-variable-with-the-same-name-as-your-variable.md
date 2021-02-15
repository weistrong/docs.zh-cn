---
description: '了解详细信息：如何：隐藏与您的变量同名的变量 (Visual Basic) '
title: 如何：隐藏与变量同名的变量
ms.date: 07/20/2015
helpviewer_keywords:
- qualification [Visual Basic], of element names
- declarations [Visual Basic], elements
- element names [Visual Basic], qualification
- references [Visual Basic], declared elements
- declaration statements [Visual Basic], declared elements
- declaring elements [Visual Basic]
- referencing declared elements [Visual Basic]
- declared elements [Visual Basic], referencing
- declared elements [Visual Basic], about declared elements
ms.assetid: e39c0752-f19f-4d2e-a453-00df1b5fc7ee
ms.openlocfilehash: c6699abdc163c6ae1a78f6035cd08439d1b029f0
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100429852"
---
# <a name="how-to-hide-a-variable-with-the-same-name-as-your-variable-visual-basic"></a><span data-ttu-id="246ea-103">如何：隐藏与您的变量同名的变量 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="246ea-103">How to: Hide a Variable with the Same Name as Your Variable (Visual Basic)</span></span>

<span data-ttu-id="246ea-104">您可以通过隐藏变量来 *隐藏该变量* ，也就是说，使用同一名称的变量重新定义该变量即可。</span><span class="sxs-lookup"><span data-stu-id="246ea-104">You can hide a variable by *shadowing* it, that is, by redefining it with a variable of the same name.</span></span> <span data-ttu-id="246ea-105">您可以通过两种方式隐藏要隐藏的变量：</span><span class="sxs-lookup"><span data-stu-id="246ea-105">You can shadow the variable you want to hide in two ways:</span></span>

- <span data-ttu-id="246ea-106">**通过范围隐藏。**</span><span class="sxs-lookup"><span data-stu-id="246ea-106">**Shadowing Through Scope.**</span></span> <span data-ttu-id="246ea-107">可以通过范围将其隐藏，方法是在包含要隐藏的变量的区域的子区域内重新声明。</span><span class="sxs-lookup"><span data-stu-id="246ea-107">You can shadow it through scope by redeclaring it inside a subregion of the region containing the variable you want to hide.</span></span>

- <span data-ttu-id="246ea-108">**通过继承隐藏。**</span><span class="sxs-lookup"><span data-stu-id="246ea-108">**Shadowing Through Inheritance.**</span></span> <span data-ttu-id="246ea-109">如果要隐藏的变量是在类级别定义的，可以通过继承将其隐藏，方法是使用派生类中的 [Shadows](../../../language-reference/modifiers/shadows.md) 关键字对其进行重新声明。</span><span class="sxs-lookup"><span data-stu-id="246ea-109">If the variable you want to hide is defined at class level, you can shadow it through inheritance by redeclaring it with the [Shadows](../../../language-reference/modifiers/shadows.md) keyword in a derived class.</span></span>

## <a name="two-ways-to-hide-a-variable"></a><span data-ttu-id="246ea-110">用于隐藏变量的两种方法</span><span class="sxs-lookup"><span data-stu-id="246ea-110">Two Ways to Hide a Variable</span></span>

#### <a name="to-hide-a-variable-by-shadowing-it-through-scope"></a><span data-ttu-id="246ea-111">通过使用范围隐藏变量来隐藏变量</span><span class="sxs-lookup"><span data-stu-id="246ea-111">To hide a variable by shadowing it through scope</span></span>

1. <span data-ttu-id="246ea-112">确定定义要隐藏的变量的区域，并确定要将其与变量一起重新定义的子区域。</span><span class="sxs-lookup"><span data-stu-id="246ea-112">Determine the region defining the variable you want to hide, and determine a subregion in which to redefine it with your variable.</span></span>

    |<span data-ttu-id="246ea-113">变量的区域</span><span class="sxs-lookup"><span data-stu-id="246ea-113">Variable's region</span></span>|<span data-ttu-id="246ea-114">允许用于重新定义的子区域</span><span class="sxs-lookup"><span data-stu-id="246ea-114">Allowable subregion for redefining it</span></span>|
    |-----------------------|-------------------------------------------|
    |<span data-ttu-id="246ea-115">模块</span><span class="sxs-lookup"><span data-stu-id="246ea-115">Module</span></span>|<span data-ttu-id="246ea-116">模块内的类</span><span class="sxs-lookup"><span data-stu-id="246ea-116">A class within the module</span></span>|
    |<span data-ttu-id="246ea-117">类</span><span class="sxs-lookup"><span data-stu-id="246ea-117">Class</span></span>|<span data-ttu-id="246ea-118">类中的子类</span><span class="sxs-lookup"><span data-stu-id="246ea-118">A subclass within the class</span></span><br /><br /> <span data-ttu-id="246ea-119">类中的过程</span><span class="sxs-lookup"><span data-stu-id="246ea-119">A procedure within the class</span></span>|

    <span data-ttu-id="246ea-120">不能在该过程中的块内重新定义过程变量，例如在 `If` ... `End If` 构造或 `For` 循环中。</span><span class="sxs-lookup"><span data-stu-id="246ea-120">You cannot redefine a procedure variable in a block within that procedure, for example in an `If`...`End If` construction or a `For` loop.</span></span>

2. <span data-ttu-id="246ea-121">如果子区域尚不存在，则创建它。</span><span class="sxs-lookup"><span data-stu-id="246ea-121">Create the subregion if it does not already exist.</span></span>

3. <span data-ttu-id="246ea-122">在子区域内，编写声明隐藏变量的 [Dim 语句](../../../language-reference/statements/dim-statement.md) 。</span><span class="sxs-lookup"><span data-stu-id="246ea-122">Within the subregion, write a [Dim Statement](../../../language-reference/statements/dim-statement.md) declaring the shadowing variable.</span></span>

    <span data-ttu-id="246ea-123">当子区域内的代码引用变量名时，编译器解析对隐藏变量的引用。</span><span class="sxs-lookup"><span data-stu-id="246ea-123">When code inside the subregion refers to the variable name, the compiler resolves the reference to the shadowing variable.</span></span>

    <span data-ttu-id="246ea-124">下面的示例说明了通过范围进行的隐藏，以及跳过隐藏的引用。</span><span class="sxs-lookup"><span data-stu-id="246ea-124">The following example illustrates shadowing through scope, as well as a reference that bypasses the shadowing.</span></span>

    ```vb
    Module shadowByScope
        ' The following statement declares num as a module-level variable.
        Public num As Integer
        Sub show()
            ' The following statement declares num as a local variable.
            Dim num As Integer
            ' The following statement sets the value of the local variable.
            num = 2
            ' The following statement displays the module-level variable.
            MsgBox(CStr(shadowByScope.num))
        End Sub
        Sub useModuleLevelNum()
            ' The following statement sets the value of the module-level variable.
            num = 1
            show()
        End Sub
    End Module
    ```

    <span data-ttu-id="246ea-125">前面的示例在 `num` 过程级别中声明变量，同时在过程 `show`)  (。</span><span class="sxs-lookup"><span data-stu-id="246ea-125">The preceding example declares the variable `num` both at module level and at procedure level (in the procedure `show`).</span></span> <span data-ttu-id="246ea-126">局部变量将 `num` 隐藏中的模块级变量 `num` `show` ，因此本地变量设置为2。</span><span class="sxs-lookup"><span data-stu-id="246ea-126">The local variable `num` shadows the module-level variable `num` within `show`, so the local variable is set to 2.</span></span> <span data-ttu-id="246ea-127">但是， `num` 在此过程中没有要隐藏的局部变量 `useModuleLevelNum` 。</span><span class="sxs-lookup"><span data-stu-id="246ea-127">However, there is no local variable to shadow `num` in the `useModuleLevelNum` procedure.</span></span> <span data-ttu-id="246ea-128">因此， `useModuleLevelNum` 将模块级变量的值设置为1。</span><span class="sxs-lookup"><span data-stu-id="246ea-128">Therefore, `useModuleLevelNum` sets the value of the module-level variable to 1.</span></span>

    <span data-ttu-id="246ea-129">`MsgBox`通过使用模块名称限定，中的调用会 `show` 绕过隐藏机制 `num` 。</span><span class="sxs-lookup"><span data-stu-id="246ea-129">The `MsgBox` call inside `show` bypasses the shadowing mechanism by qualifying `num` with the module name.</span></span> <span data-ttu-id="246ea-130">因此，它会显示模块级变量，而不是局部变量。</span><span class="sxs-lookup"><span data-stu-id="246ea-130">Therefore, it displays the module-level variable instead of the local variable.</span></span>

#### <a name="to-hide-a-variable-by-shadowing-it-through-inheritance"></a><span data-ttu-id="246ea-131">通过继承隐藏变量来隐藏变量</span><span class="sxs-lookup"><span data-stu-id="246ea-131">To hide a variable by shadowing it through inheritance</span></span>

1. <span data-ttu-id="246ea-132">请确保要隐藏的变量在类中声明，在类级别 (在任何过程) 之外。</span><span class="sxs-lookup"><span data-stu-id="246ea-132">Be sure the variable you want to hide is declared in a class, and at class level (outside any procedure).</span></span> <span data-ttu-id="246ea-133">否则，不能通过继承将其隐藏起来。</span><span class="sxs-lookup"><span data-stu-id="246ea-133">Otherwise you cannot shadow it through inheritance.</span></span>

2. <span data-ttu-id="246ea-134">定义派生自变量的类的类（如果尚不存在）。</span><span class="sxs-lookup"><span data-stu-id="246ea-134">Define a class derived from the variable's class if one does not already exist.</span></span>

3. <span data-ttu-id="246ea-135">在派生类中，编写 `Dim` 声明变量的语句。</span><span class="sxs-lookup"><span data-stu-id="246ea-135">Inside the derived class, write a `Dim` statement declaring your variable.</span></span> <span data-ttu-id="246ea-136">在声明中包含 [Shadows](../../../language-reference/modifiers/shadows.md) 关键字。</span><span class="sxs-lookup"><span data-stu-id="246ea-136">Include the [Shadows](../../../language-reference/modifiers/shadows.md) keyword in the declaration.</span></span>

    <span data-ttu-id="246ea-137">当派生类中的代码引用变量名时，编译器会将对变量的引用解析为。</span><span class="sxs-lookup"><span data-stu-id="246ea-137">When code in the derived class refers to the variable name, the compiler resolves the reference to your variable.</span></span>

    <span data-ttu-id="246ea-138">下面的示例演示通过继承进行的隐藏。</span><span class="sxs-lookup"><span data-stu-id="246ea-138">The following example illustrates shadowing through inheritance.</span></span> <span data-ttu-id="246ea-139">它创建两个引用，一个用于访问隐藏变量，另一个用于绕过隐藏。</span><span class="sxs-lookup"><span data-stu-id="246ea-139">It makes two references, one that accesses the shadowing variable and one that bypasses the shadowing.</span></span>

    ```vb
    Public Class shadowBaseClass
        Public shadowString As String = "This is the base class string."
    End Class
    Public Class shadowDerivedClass
        Inherits shadowBaseClass
        Public Shadows shadowString As String = "This is the derived class string."
        Public Sub showStrings()
            Dim s As String = "Unqualified shadowString: " & shadowString &
                 vbCrLf & "MyBase.shadowString: " & MyBase.shadowString
            MsgBox(s)
        End Sub
    End Class
    ```

    <span data-ttu-id="246ea-140">前面的示例声明 `shadowString` 基类中的变量，并将其隐藏在派生类中。</span><span class="sxs-lookup"><span data-stu-id="246ea-140">The preceding example declares the variable `shadowString` in the base class and shadows it in the derived class.</span></span> <span data-ttu-id="246ea-141">`showStrings`派生类中的过程在名称不合格时显示字符串的隐藏版本 `shadowString` 。</span><span class="sxs-lookup"><span data-stu-id="246ea-141">The procedure `showStrings` in the derived class displays the shadowing version of the string when the name `shadowString` is not qualified.</span></span> <span data-ttu-id="246ea-142">当用关键字限定时，它会显示隐藏的版本 `shadowString` `MyBase` 。</span><span class="sxs-lookup"><span data-stu-id="246ea-142">It then displays the shadowed version when `shadowString` is qualified with the `MyBase` keyword.</span></span>

## <a name="robust-programming"></a><span data-ttu-id="246ea-143">可靠编程</span><span class="sxs-lookup"><span data-stu-id="246ea-143">Robust Programming</span></span>

<span data-ttu-id="246ea-144">隐藏引入了一个具有相同名称的变量的多个版本。</span><span class="sxs-lookup"><span data-stu-id="246ea-144">Shadowing introduces more than one version of a variable with the same name.</span></span> <span data-ttu-id="246ea-145">当代码语句引用变量名时，编译器解析引用的版本取决于一些因素，如代码语句的位置和符合条件的字符串的状态。</span><span class="sxs-lookup"><span data-stu-id="246ea-145">When a code statement refers to the variable name, the version to which the compiler resolves the reference depends on factors such as the location of the code statement and the presence of a qualifying string.</span></span> <span data-ttu-id="246ea-146">这可能会增加引用隐藏变量的意外版本的风险。</span><span class="sxs-lookup"><span data-stu-id="246ea-146">This can increase the risk of referring to an unintended version of a shadowed variable.</span></span> <span data-ttu-id="246ea-147">您可以通过完全限定对隐藏变量的所有引用来降低风险。</span><span class="sxs-lookup"><span data-stu-id="246ea-147">You can lower that risk by fully qualifying all references to a shadowed variable.</span></span>

## <a name="see-also"></a><span data-ttu-id="246ea-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="246ea-148">See also</span></span>

- [<span data-ttu-id="246ea-149">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="246ea-149">References to Declared Elements</span></span>](references-to-declared-elements.md)
- [<span data-ttu-id="246ea-150">Visual Basic 中的隐藏</span><span class="sxs-lookup"><span data-stu-id="246ea-150">Shadowing in Visual Basic</span></span>](shadowing.md)
- [<span data-ttu-id="246ea-151">隐藏和重写之间的差异</span><span class="sxs-lookup"><span data-stu-id="246ea-151">Differences Between Shadowing and Overriding</span></span>](differences-between-shadowing-and-overriding.md)
- [<span data-ttu-id="246ea-152">如何：隐藏继承的变量</span><span class="sxs-lookup"><span data-stu-id="246ea-152">How to: Hide an Inherited Variable</span></span>](how-to-hide-an-inherited-variable.md)
- [<span data-ttu-id="246ea-153">如何：访问被派生类隐藏的变量</span><span class="sxs-lookup"><span data-stu-id="246ea-153">How to: Access a Variable Hidden by a Derived Class</span></span>](how-to-access-a-variable-hidden-by-a-derived-class.md)
- [<span data-ttu-id="246ea-154">替代</span><span class="sxs-lookup"><span data-stu-id="246ea-154">Overrides</span></span>](../../../language-reference/modifiers/overrides.md)
- [<span data-ttu-id="246ea-155">Me、My、MyBase 和 MyClass</span><span class="sxs-lookup"><span data-stu-id="246ea-155">Me, My, MyBase, and MyClass</span></span>](../../program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="246ea-156">继承基础知识</span><span class="sxs-lookup"><span data-stu-id="246ea-156">Inheritance Basics</span></span>](../objects-and-classes/inheritance-basics.md)
