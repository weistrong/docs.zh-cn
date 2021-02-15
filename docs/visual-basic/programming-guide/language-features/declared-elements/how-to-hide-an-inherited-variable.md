---
description: '了解有关详细信息，请参阅如何：隐藏继承的变量 (Visual Basic) '
title: 如何：隐藏继承的变量
ms.date: 07/20/2015
helpviewer_keywords:
- qualification [Visual Basic], of element names
- element names [Visual Basic], qualification
- references [Visual Basic], declared elements
- declaration statements [Visual Basic], declared elements
- referencing declared elements [Visual Basic]
- declared elements [Visual Basic], referencing
- declared elements [Visual Basic], about declared elements
- variables [Visual Basic], hiding inherited
ms.assetid: 765728d9-7351-4a30-999d-b5f34f024412
ms.openlocfilehash: be2de980e27b318151c795ae36bd92a01d47d55e
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100429892"
---
# <a name="how-to-hide-an-inherited-variable-visual-basic"></a><span data-ttu-id="c41cb-103">如何：隐藏继承的变量 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c41cb-103">How to: Hide an Inherited Variable (Visual Basic)</span></span>

<span data-ttu-id="c41cb-104">派生类继承其基类的所有定义。</span><span class="sxs-lookup"><span data-stu-id="c41cb-104">A derived class inherits all the definitions of its base class.</span></span> <span data-ttu-id="c41cb-105">如果要使用与基类元素相同的名称来定义变量，则可以在派生类中定义变量时 *隐藏或隐藏* 该基类元素。</span><span class="sxs-lookup"><span data-stu-id="c41cb-105">If you want to define a variable using the same name as an element of the base class, you can hide, or *shadow*, that base class element when you define your variable in the derived class.</span></span> <span data-ttu-id="c41cb-106">如果执行此操作，派生类中的代码将访问你的变量，除非它显式跳过隐藏机制。</span><span class="sxs-lookup"><span data-stu-id="c41cb-106">If you do this, code in the derived class accesses your variable unless it explicitly bypasses the shadowing mechanism.</span></span>

<span data-ttu-id="c41cb-107">您可能想要隐藏继承的变量的另一个原因是为了防止基类修订。</span><span class="sxs-lookup"><span data-stu-id="c41cb-107">Another reason you might want to hide an inherited variable is to protect against base class revision.</span></span> <span data-ttu-id="c41cb-108">基类可能会改变要继承的元素。</span><span class="sxs-lookup"><span data-stu-id="c41cb-108">The base class might undergo a change that alters the element you are inheriting.</span></span> <span data-ttu-id="c41cb-109">如果发生这种情况，则 `Shadows` 修饰符强制将派生类中的引用解析为你的变量，而不是基类元素。</span><span class="sxs-lookup"><span data-stu-id="c41cb-109">If this happens, the `Shadows` modifier forces references from the derived class to be resolved to your variable, instead of to the base class element.</span></span>

## <a name="to-hide-an-inherited-variable"></a><span data-ttu-id="c41cb-110">隐藏继承的变量</span><span class="sxs-lookup"><span data-stu-id="c41cb-110">To hide an inherited variable</span></span>

1. <span data-ttu-id="c41cb-111">请确保要隐藏的变量在类级声明 (在任何过程) 的外部。</span><span class="sxs-lookup"><span data-stu-id="c41cb-111">Be sure the variable you want to hide is declared at class level (outside any procedure).</span></span> <span data-ttu-id="c41cb-112">否则，你无需隐藏它。</span><span class="sxs-lookup"><span data-stu-id="c41cb-112">Otherwise, you do not need to hide it.</span></span>
  
2. <span data-ttu-id="c41cb-113">在派生类中，编写声明变量的 [Dim 语句](../../../language-reference/statements/dim-statement.md) 。</span><span class="sxs-lookup"><span data-stu-id="c41cb-113">Inside your derived class, write a [Dim Statement](../../../language-reference/statements/dim-statement.md) declaring your variable.</span></span> <span data-ttu-id="c41cb-114">使用与继承变量相同的名称。</span><span class="sxs-lookup"><span data-stu-id="c41cb-114">Use the same name as that of the inherited variable.</span></span>

3. <span data-ttu-id="c41cb-115">在声明中包含 [Shadows](../../../language-reference/modifiers/shadows.md) 关键字。</span><span class="sxs-lookup"><span data-stu-id="c41cb-115">Include the [Shadows](../../../language-reference/modifiers/shadows.md) keyword in the declaration.</span></span>

     <span data-ttu-id="c41cb-116">当派生类中的代码引用变量名时，编译器会将对变量的引用解析为。</span><span class="sxs-lookup"><span data-stu-id="c41cb-116">When code in the derived class refers to the variable name, the compiler resolves the reference to your variable.</span></span>

     <span data-ttu-id="c41cb-117">下面的示例说明了继承变量的隐藏：</span><span class="sxs-lookup"><span data-stu-id="c41cb-117">The following example illustrates shadowing of an inherited variable:</span></span>
  
    ```vb  
    Public Class ShadowBaseClass  
        Public shadowString As String = "This is the base class string."  
    End Class  
    Public Class ShadowDerivedClass  
        Inherits ShadowBaseClass  
        Public Shadows shadowString As String = "This is the derived class string."  
        Public Sub ShowStrings()  
            Dim s As String = $"Unqualified shadowString: {shadowString}{vbCrLf}MyBase.shadowString: {MyBase.shadowString}"
            MsgBox(s)  
        End Sub  
    End Class  
    ```  
  
     <span data-ttu-id="c41cb-118">前面的示例声明 `shadowString` 基类中的变量，并将其隐藏在派生类中。</span><span class="sxs-lookup"><span data-stu-id="c41cb-118">The preceding example declares the variable `shadowString` in the base class and shadows it in the derived class.</span></span> <span data-ttu-id="c41cb-119">`ShowStrings`派生类中的过程在名称不合格时显示字符串的隐藏版本 `shadowString` 。</span><span class="sxs-lookup"><span data-stu-id="c41cb-119">The procedure `ShowStrings` in the derived class displays the shadowing version of the string when the name `shadowString` is not qualified.</span></span> <span data-ttu-id="c41cb-120">当用关键字限定时，它会显示隐藏的版本 `shadowString` `MyBase` 。</span><span class="sxs-lookup"><span data-stu-id="c41cb-120">It then displays the shadowed version when `shadowString` is qualified with the `MyBase` keyword.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="c41cb-121">可靠编程</span><span class="sxs-lookup"><span data-stu-id="c41cb-121">Robust programming</span></span>

<span data-ttu-id="c41cb-122">隐藏引入了一个具有相同名称的变量的多个版本。</span><span class="sxs-lookup"><span data-stu-id="c41cb-122">Shadowing introduces more than one version of a variable with the same name.</span></span> <span data-ttu-id="c41cb-123">当代码语句引用变量名时，编译器解析引用的版本取决于一些因素，如代码语句的位置和符合条件的字符串的状态。</span><span class="sxs-lookup"><span data-stu-id="c41cb-123">When a code statement refers to the variable name, the version to which the compiler resolves the reference depends on factors such as the location of the code statement and the presence of a qualifying string.</span></span> <span data-ttu-id="c41cb-124">这可能会增加引用隐藏变量的意外版本的风险。</span><span class="sxs-lookup"><span data-stu-id="c41cb-124">This can increase the risk of referring to an unintended version of a shadowed variable.</span></span> <span data-ttu-id="c41cb-125">您可以通过完全限定对隐藏变量的所有引用来降低风险。</span><span class="sxs-lookup"><span data-stu-id="c41cb-125">You can lower that risk by fully qualifying all references to a shadowed variable.</span></span>

## <a name="see-also"></a><span data-ttu-id="c41cb-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="c41cb-126">See also</span></span>

- [<span data-ttu-id="c41cb-127">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="c41cb-127">References to Declared Elements</span></span>](references-to-declared-elements.md)
- [<span data-ttu-id="c41cb-128">Visual Basic 中的隐藏</span><span class="sxs-lookup"><span data-stu-id="c41cb-128">Shadowing in Visual Basic</span></span>](shadowing.md)
- [<span data-ttu-id="c41cb-129">隐藏和重写之间的差异</span><span class="sxs-lookup"><span data-stu-id="c41cb-129">Differences Between Shadowing and Overriding</span></span>](differences-between-shadowing-and-overriding.md)
- [<span data-ttu-id="c41cb-130">如何：隐藏与变量同名的变量</span><span class="sxs-lookup"><span data-stu-id="c41cb-130">How to: Hide a Variable with the Same Name as Your Variable</span></span>](how-to-hide-a-variable-with-the-same-name-as-your-variable.md)
- [<span data-ttu-id="c41cb-131">如何：访问被派生类隐藏的变量</span><span class="sxs-lookup"><span data-stu-id="c41cb-131">How to: Access a Variable Hidden by a Derived Class</span></span>](how-to-access-a-variable-hidden-by-a-derived-class.md)
- [<span data-ttu-id="c41cb-132">替代</span><span class="sxs-lookup"><span data-stu-id="c41cb-132">Overrides</span></span>](../../../language-reference/modifiers/overrides.md)
- [<span data-ttu-id="c41cb-133">Me、My、MyBase 和 MyClass</span><span class="sxs-lookup"><span data-stu-id="c41cb-133">Me, My, MyBase, and MyClass</span></span>](../../program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="c41cb-134">继承基础知识</span><span class="sxs-lookup"><span data-stu-id="c41cb-134">Inheritance Basics</span></span>](../objects-and-classes/inheritance-basics.md)
