---
description: '了解详细信息：类语句 (Visual Basic) '
title: Class 语句
ms.date: 05/12/2018
f1_keywords:
- vb.Class
helpviewer_keywords:
- class modules
- Class statement [Visual Basic]
- classes [Visual Basic], fields
- fields [Visual Basic], of classes
- class types [Visual Basic], class statements
- classes [Visual Basic], creating
- classes [Visual Basic], data members
- data members [Visual Basic], of classes
ms.assetid: f2664f38-eb5a-4d4b-a374-1d041521fb6c
ms.openlocfilehash: de4541addc9f4755d973586c7d1b4410e4bf12ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673890"
---
# <a name="class-statement-visual-basic"></a><span data-ttu-id="2c949-103">Class 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2c949-103">Class Statement (Visual Basic)</span></span>

<span data-ttu-id="2c949-104">声明类的名称，并引入类所包含的变量、属性、事件和过程的定义。</span><span class="sxs-lookup"><span data-stu-id="2c949-104">Declares the name of a class and introduces the definition of the variables, properties, events, and procedures that the class comprises.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c949-105">语法</span><span class="sxs-lookup"><span data-stu-id="2c949-105">Syntax</span></span>  
  
```vb  
[ <attributelist> ] [ accessmodifier ] [ Shadows ] [ MustInherit | NotInheritable ] [ Partial ] _  
Class name [ ( Of typelist ) ]  
    [ Inherits classname ]  
    [ Implements interfacenames ]  
    [ statements ]  
End Class  
```  
  
## <a name="parts"></a><span data-ttu-id="2c949-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="2c949-106">Parts</span></span>  
  
|<span data-ttu-id="2c949-107">术语</span><span class="sxs-lookup"><span data-stu-id="2c949-107">Term</span></span>|<span data-ttu-id="2c949-108">定义</span><span class="sxs-lookup"><span data-stu-id="2c949-108">Definition</span></span>|  
|---|---|  
|`attributelist`|<span data-ttu-id="2c949-109">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-109">Optional.</span></span> <span data-ttu-id="2c949-110">请参阅 [特性列表](attribute-list.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-110">See [Attribute List](attribute-list.md).</span></span>|  
|`accessmodifier`|<span data-ttu-id="2c949-111">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-111">Optional.</span></span> <span data-ttu-id="2c949-112">可以是以下其中一个值：</span><span class="sxs-lookup"><span data-stu-id="2c949-112">Can be one of the following:</span></span><br /><br /> <span data-ttu-id="2c949-113">-   [公布](../modifiers/public.md)</span><span class="sxs-lookup"><span data-stu-id="2c949-113">-   [Public](../modifiers/public.md)</span></span><br /><span data-ttu-id="2c949-114">-   [避免](../modifiers/protected.md)</span><span class="sxs-lookup"><span data-stu-id="2c949-114">-   [Protected](../modifiers/protected.md)</span></span><br /><span data-ttu-id="2c949-115">-   [友好](../modifiers/friend.md)</span><span class="sxs-lookup"><span data-stu-id="2c949-115">-   [Friend](../modifiers/friend.md)</span></span><br /><span data-ttu-id="2c949-116">-   [专有](../modifiers/private.md)</span><span class="sxs-lookup"><span data-stu-id="2c949-116">-   [Private](../modifiers/private.md)</span></span><br /><span data-ttu-id="2c949-117">-   [受保护的朋友](../modifiers/protected-friend.md)</span><span class="sxs-lookup"><span data-stu-id="2c949-117">-   [Protected Friend](../modifiers/protected-friend.md)</span></span><br /><span data-ttu-id="2c949-118">- [私有受保护](../modifiers/private-protected.md)</span><span class="sxs-lookup"><span data-stu-id="2c949-118">- [Private Protected](../modifiers/private-protected.md)</span></span><br/><br/> <span data-ttu-id="2c949-119">请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-119">See [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>|  
|`Shadows`|<span data-ttu-id="2c949-120">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-120">Optional.</span></span> <span data-ttu-id="2c949-121">请参阅 [阴影](../modifiers/shadows.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-121">See [Shadows](../modifiers/shadows.md).</span></span>|  
|`MustInherit`|<span data-ttu-id="2c949-122">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-122">Optional.</span></span> <span data-ttu-id="2c949-123">请参阅 [MustInherit](../modifiers/mustinherit.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-123">See [MustInherit](../modifiers/mustinherit.md).</span></span>|  
|`NotInheritable`|<span data-ttu-id="2c949-124">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-124">Optional.</span></span> <span data-ttu-id="2c949-125">请参阅 [NotInheritable](../modifiers/notinheritable.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-125">See [NotInheritable](../modifiers/notinheritable.md).</span></span>|  
|`Partial`|<span data-ttu-id="2c949-126">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-126">Optional.</span></span> <span data-ttu-id="2c949-127">指示类的分部定义。</span><span class="sxs-lookup"><span data-stu-id="2c949-127">Indicates a partial definition of the class.</span></span> <span data-ttu-id="2c949-128">请参阅 [部分](../modifiers/partial.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-128">See [Partial](../modifiers/partial.md).</span></span>|  
|`name`|<span data-ttu-id="2c949-129">必需。</span><span class="sxs-lookup"><span data-stu-id="2c949-129">Required.</span></span> <span data-ttu-id="2c949-130">此类的名称。</span><span class="sxs-lookup"><span data-stu-id="2c949-130">Name of this class.</span></span> <span data-ttu-id="2c949-131">请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-131">See [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>|  
|`Of`|<span data-ttu-id="2c949-132">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-132">Optional.</span></span> <span data-ttu-id="2c949-133">指定这是一个泛型类。</span><span class="sxs-lookup"><span data-stu-id="2c949-133">Specifies that this is a generic class.</span></span>|  
|`typelist`|<span data-ttu-id="2c949-134">如果使用 of 关键字，则 [为](of-clause.md) 必需。</span><span class="sxs-lookup"><span data-stu-id="2c949-134">Required if you use the [Of](of-clause.md) keyword.</span></span> <span data-ttu-id="2c949-135">此类的类型参数列表。</span><span class="sxs-lookup"><span data-stu-id="2c949-135">List of type parameters for this class.</span></span> <span data-ttu-id="2c949-136">请参阅 [类型列表](type-list.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-136">See [Type List](type-list.md).</span></span>|  
|`Inherits`|<span data-ttu-id="2c949-137">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-137">Optional.</span></span> <span data-ttu-id="2c949-138">指示此类继承另一个类的成员。</span><span class="sxs-lookup"><span data-stu-id="2c949-138">Indicates that this class inherits the members of another class.</span></span> <span data-ttu-id="2c949-139">请参阅 [Inherits 语句](inherits-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-139">See [Inherits Statement](inherits-statement.md).</span></span>|  
|`classname`|<span data-ttu-id="2c949-140">如果使用语句，则为必需 `Inherits` 。</span><span class="sxs-lookup"><span data-stu-id="2c949-140">Required if you use the `Inherits` statement.</span></span> <span data-ttu-id="2c949-141">此类派生自的类的名称。</span><span class="sxs-lookup"><span data-stu-id="2c949-141">The name of the class from which this class derives.</span></span>|  
|`Implements`|<span data-ttu-id="2c949-142">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-142">Optional.</span></span> <span data-ttu-id="2c949-143">指示此类实现一个或多个接口的成员。</span><span class="sxs-lookup"><span data-stu-id="2c949-143">Indicates that this class implements the members of one or more interfaces.</span></span> <span data-ttu-id="2c949-144">请参阅 [Implements 语句](implements-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-144">See [Implements Statement](implements-statement.md).</span></span>|  
|`interfacenames`|<span data-ttu-id="2c949-145">如果使用语句，则为必需 `Implements` 。</span><span class="sxs-lookup"><span data-stu-id="2c949-145">Required if you use the `Implements` statement.</span></span> <span data-ttu-id="2c949-146">此类实现的接口的名称。</span><span class="sxs-lookup"><span data-stu-id="2c949-146">The names of the interfaces this class implements.</span></span>|  
|`statements`|<span data-ttu-id="2c949-147">可选。</span><span class="sxs-lookup"><span data-stu-id="2c949-147">Optional.</span></span> <span data-ttu-id="2c949-148">定义此类的成员的语句。</span><span class="sxs-lookup"><span data-stu-id="2c949-148">Statements which define the members of this class.</span></span>|  
|`End Class`|<span data-ttu-id="2c949-149">必需。</span><span class="sxs-lookup"><span data-stu-id="2c949-149">Required.</span></span> <span data-ttu-id="2c949-150">终止 `Class` 定义。</span><span class="sxs-lookup"><span data-stu-id="2c949-150">Terminates the `Class` definition.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2c949-151">备注</span><span class="sxs-lookup"><span data-stu-id="2c949-151">Remarks</span></span>  

 <span data-ttu-id="2c949-152">`Class`语句定义新的数据类型。</span><span class="sxs-lookup"><span data-stu-id="2c949-152">A `Class` statement defines a new data type.</span></span> <span data-ttu-id="2c949-153">*类* 是面向对象编程的基本构建基块 (OOP) 。</span><span class="sxs-lookup"><span data-stu-id="2c949-153">A *class* is a fundamental building block of object-oriented programming (OOP).</span></span> <span data-ttu-id="2c949-154">有关详细信息，请参阅 [对象和类](../../programming-guide/language-features/objects-and-classes/index.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-154">For more information, see [Objects and Classes](../../programming-guide/language-features/objects-and-classes/index.md).</span></span>  
  
 <span data-ttu-id="2c949-155">只能 `Class` 在命名空间或模块级别使用。</span><span class="sxs-lookup"><span data-stu-id="2c949-155">You can use `Class` only at namespace or module level.</span></span> <span data-ttu-id="2c949-156">这意味着类的 *声明上下文* 必须是源文件、命名空间、类、结构、模块或接口，不能是过程或块。</span><span class="sxs-lookup"><span data-stu-id="2c949-156">This means the *declaration context* for a class must be a source file, namespace, class, structure, module, or interface, and cannot be a procedure or block.</span></span> <span data-ttu-id="2c949-157">有关详细信息，请参阅[声明上下文和默认访问级别](declaration-contexts-and-default-access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-157">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>  
  
 <span data-ttu-id="2c949-158">类的每个实例都具有独立于所有其他实例的生存期。</span><span class="sxs-lookup"><span data-stu-id="2c949-158">Each instance of a class has a lifetime independent of all other instances.</span></span> <span data-ttu-id="2c949-159">此生存期在由 [新运算符](../operators/new-operator.md) 子句或函数（如）创建时开始 <xref:Microsoft.VisualBasic.Interaction.CreateObject%2A> 。</span><span class="sxs-lookup"><span data-stu-id="2c949-159">This lifetime begins when it is created by a [New Operator](../operators/new-operator.md) clause or by a function such as <xref:Microsoft.VisualBasic.Interaction.CreateObject%2A>.</span></span> <span data-ttu-id="2c949-160">当指向实例的所有变量均设置为 [Nothing](../nothing.md) 或其他类的实例时，它将结束。</span><span class="sxs-lookup"><span data-stu-id="2c949-160">It ends when all variables pointing to the instance have been set to [Nothing](../nothing.md) or to instances of other classes.</span></span>  
  
 <span data-ttu-id="2c949-161">类默认为 [Friend](../modifiers/friend.md) 访问。</span><span class="sxs-lookup"><span data-stu-id="2c949-161">Classes default to [Friend](../modifiers/friend.md) access.</span></span> <span data-ttu-id="2c949-162">您可以使用访问修饰符调整其访问级别。</span><span class="sxs-lookup"><span data-stu-id="2c949-162">You can adjust their access levels with the access modifiers.</span></span> <span data-ttu-id="2c949-163">有关详细信息，请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-163">For more information, see [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
## <a name="rules"></a><span data-ttu-id="2c949-164">规则</span><span class="sxs-lookup"><span data-stu-id="2c949-164">Rules</span></span>  
  
- <span data-ttu-id="2c949-165">**层.**</span><span class="sxs-lookup"><span data-stu-id="2c949-165">**Nesting.**</span></span> <span data-ttu-id="2c949-166">可以在另一个类中定义一个类。</span><span class="sxs-lookup"><span data-stu-id="2c949-166">You can define one class within another.</span></span> <span data-ttu-id="2c949-167">外部类称为 *包含类*，内部类称为 " *嵌套类*"。</span><span class="sxs-lookup"><span data-stu-id="2c949-167">The outer class is called the *containing class*, and the inner class is called a *nested class*.</span></span>  
  
- <span data-ttu-id="2c949-168">**继承.**</span><span class="sxs-lookup"><span data-stu-id="2c949-168">**Inheritance.**</span></span> <span data-ttu-id="2c949-169">如果类使用 [Inherits 语句](inherits-statement.md)，则只能指定一个基类或接口。</span><span class="sxs-lookup"><span data-stu-id="2c949-169">If the class uses the [Inherits Statement](inherits-statement.md), you can specify only one base class or interface.</span></span> <span data-ttu-id="2c949-170">类不能从多个元素继承。</span><span class="sxs-lookup"><span data-stu-id="2c949-170">A class cannot inherit from more than one element.</span></span>  
  
     <span data-ttu-id="2c949-171">类不能继承自具有限制性更强的访问级别的另一个类。</span><span class="sxs-lookup"><span data-stu-id="2c949-171">A class cannot inherit from another class with a more restrictive access level.</span></span> <span data-ttu-id="2c949-172">例如， `Public` 类不能从 `Friend` 类继承。</span><span class="sxs-lookup"><span data-stu-id="2c949-172">For example, a `Public` class cannot inherit from a `Friend` class.</span></span>  
  
     <span data-ttu-id="2c949-173">类不能从嵌套在它中的类继承。</span><span class="sxs-lookup"><span data-stu-id="2c949-173">A class cannot inherit from a class nested within it.</span></span>  
  
- <span data-ttu-id="2c949-174">**部署.**</span><span class="sxs-lookup"><span data-stu-id="2c949-174">**Implementation.**</span></span> <span data-ttu-id="2c949-175">如果类使用 [Implements 语句](implements-statement.md)，则必须实现在中指定的每个接口所定义的每个成员 `interfacenames` 。</span><span class="sxs-lookup"><span data-stu-id="2c949-175">If the class uses the [Implements Statement](implements-statement.md), you must implement every member defined by every interface you specify in `interfacenames`.</span></span> <span data-ttu-id="2c949-176">这种情况的一个例外是基类成员的重新实现。</span><span class="sxs-lookup"><span data-stu-id="2c949-176">An exception to this is reimplementation of a base class member.</span></span> <span data-ttu-id="2c949-177">有关详细信息，请参阅 [实现](implements-clause.md)中的 "重新实现"。</span><span class="sxs-lookup"><span data-stu-id="2c949-177">For more information, see "Reimplementation" in [Implements](implements-clause.md).</span></span>  
  
- <span data-ttu-id="2c949-178">**默认属性。**</span><span class="sxs-lookup"><span data-stu-id="2c949-178">**Default Property.**</span></span> <span data-ttu-id="2c949-179">一个类最多只能指定一个属性作为其 *默认属性*。</span><span class="sxs-lookup"><span data-stu-id="2c949-179">A class can specify at most one property as its *default property*.</span></span> <span data-ttu-id="2c949-180">有关详细信息，请参阅 [默认值](../modifiers/default.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-180">For more information, see [Default](../modifiers/default.md).</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="2c949-181">行为</span><span class="sxs-lookup"><span data-stu-id="2c949-181">Behavior</span></span>  
  
- <span data-ttu-id="2c949-182">**访问级别。**</span><span class="sxs-lookup"><span data-stu-id="2c949-182">**Access Level.**</span></span> <span data-ttu-id="2c949-183">在类中，可以使用其自己的访问级别声明每个成员。</span><span class="sxs-lookup"><span data-stu-id="2c949-183">Within a class, you can declare each member with its own access level.</span></span> <span data-ttu-id="2c949-184">类成员默认为 [公共](../modifiers/public.md) 访问，变量和常量除外，默认为 [私有](../modifiers/private.md) 访问。</span><span class="sxs-lookup"><span data-stu-id="2c949-184">Class members default to [Public](../modifiers/public.md) access, except variables and constants, which default to [Private](../modifiers/private.md) access.</span></span> <span data-ttu-id="2c949-185">当某个类的访问权限超过其成员之一时，类访问级别将优先。</span><span class="sxs-lookup"><span data-stu-id="2c949-185">When a class has more restricted access than one of its members, the class access level takes precedence.</span></span>  
  
- <span data-ttu-id="2c949-186">**划分范围。**</span><span class="sxs-lookup"><span data-stu-id="2c949-186">**Scope.**</span></span> <span data-ttu-id="2c949-187">类在其包含的命名空间、类、结构或模块的范围内。</span><span class="sxs-lookup"><span data-stu-id="2c949-187">A class is in scope throughout its containing namespace, class, structure, or module.</span></span>  
  
     <span data-ttu-id="2c949-188">每个类成员的作用域都是整个类。</span><span class="sxs-lookup"><span data-stu-id="2c949-188">The scope of every class member is the entire class.</span></span>  
  
     <span data-ttu-id="2c949-189">**生存期.**</span><span class="sxs-lookup"><span data-stu-id="2c949-189">**Lifetime.**</span></span> <span data-ttu-id="2c949-190">Visual Basic 不支持静态类。</span><span class="sxs-lookup"><span data-stu-id="2c949-190">Visual Basic does not support static classes.</span></span> <span data-ttu-id="2c949-191">与静态类等效的功能由模块提供。</span><span class="sxs-lookup"><span data-stu-id="2c949-191">The functional equivalent of a static class is provided by a module.</span></span> <span data-ttu-id="2c949-192">有关详细信息，请参阅 [Module 语句](module-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-192">For more information, see [Module Statement](module-statement.md).</span></span>  
  
     <span data-ttu-id="2c949-193">类成员的生存期取决于其声明的方式和位置。</span><span class="sxs-lookup"><span data-stu-id="2c949-193">Class members have lifetimes depending on how and where they are declared.</span></span> <span data-ttu-id="2c949-194">有关详细信息，请参阅 [Visual Basic 中的生存期](../../programming-guide/language-features/declared-elements/lifetime.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-194">For more information, see [Lifetime in Visual Basic](../../programming-guide/language-features/declared-elements/lifetime.md).</span></span>  
  
- <span data-ttu-id="2c949-195">**限定.**</span><span class="sxs-lookup"><span data-stu-id="2c949-195">**Qualification.**</span></span> <span data-ttu-id="2c949-196">类之外的代码必须使用该类的名称来限定成员的名称。</span><span class="sxs-lookup"><span data-stu-id="2c949-196">Code outside a class must qualify a member's name with the name of that class.</span></span>  
  
     <span data-ttu-id="2c949-197">如果嵌套类中的代码对编程元素进行了非限定引用，则 Visual Basic 首先在嵌套类中搜索元素，然后在其包含类中搜索元素，并将其放入外部的包含元素。</span><span class="sxs-lookup"><span data-stu-id="2c949-197">If code inside a nested class makes an unqualified reference to a programming element, Visual Basic searches for the element first in the nested class, then in its containing class, and so on out to the outermost containing element.</span></span>  
  
## <a name="classes-and-modules"></a><span data-ttu-id="2c949-198">类和模块</span><span class="sxs-lookup"><span data-stu-id="2c949-198">Classes and Modules</span></span>  

 <span data-ttu-id="2c949-199">这些元素具有许多相似之处，但也存在一些重要的差异。</span><span class="sxs-lookup"><span data-stu-id="2c949-199">These elements have many similarities, but there are some important differences as well.</span></span>  
  
- <span data-ttu-id="2c949-200">**术语。**</span><span class="sxs-lookup"><span data-stu-id="2c949-200">**Terminology.**</span></span> <span data-ttu-id="2c949-201">Visual Basic 的早期版本可识别两种类型的模块： *类模块* ( cls 文件) 和 *标准模块* ( bas 文件) 。</span><span class="sxs-lookup"><span data-stu-id="2c949-201">Previous versions of Visual Basic recognize two types of modules: *class modules* (.cls files) and *standard modules* (.bas files).</span></span> <span data-ttu-id="2c949-202">当前版本分别调用这些 *类* 和 *模块*。</span><span class="sxs-lookup"><span data-stu-id="2c949-202">The current version calls these *classes* and *modules*, respectively.</span></span>  
  
- <span data-ttu-id="2c949-203">**共享成员。**</span><span class="sxs-lookup"><span data-stu-id="2c949-203">**Shared Members.**</span></span> <span data-ttu-id="2c949-204">您可以控制某个类的成员是共享成员还是实例成员。</span><span class="sxs-lookup"><span data-stu-id="2c949-204">You can control whether a member of a class is a shared or instance member.</span></span>  
  
- <span data-ttu-id="2c949-205">**对象方向。**</span><span class="sxs-lookup"><span data-stu-id="2c949-205">**Object Orientation.**</span></span> <span data-ttu-id="2c949-206">类是面向对象的，但模块不是。</span><span class="sxs-lookup"><span data-stu-id="2c949-206">Classes are object-oriented, but modules are not.</span></span> <span data-ttu-id="2c949-207">你可以创建一个或多个类的实例。</span><span class="sxs-lookup"><span data-stu-id="2c949-207">You can create one or more instances of a class.</span></span> <span data-ttu-id="2c949-208">有关详细信息，请参阅 [对象和类](../../programming-guide/language-features/objects-and-classes/index.md)。</span><span class="sxs-lookup"><span data-stu-id="2c949-208">For more information, see [Objects and Classes](../../programming-guide/language-features/objects-and-classes/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c949-209">示例</span><span class="sxs-lookup"><span data-stu-id="2c949-209">Example</span></span>  

 <span data-ttu-id="2c949-210">下面的示例使用 `Class` 语句定义一个类和多个成员。</span><span class="sxs-lookup"><span data-stu-id="2c949-210">The following example uses a `Class` statement to define a class and several members.</span></span>  
  
 [!code-vb[VbVbalrStatements#62](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#62)]  
  
## <a name="see-also"></a><span data-ttu-id="2c949-211">请参阅</span><span class="sxs-lookup"><span data-stu-id="2c949-211">See also</span></span>

- [<span data-ttu-id="2c949-212">对象和类</span><span class="sxs-lookup"><span data-stu-id="2c949-212">Objects and Classes</span></span>](../../programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="2c949-213">结构和类</span><span class="sxs-lookup"><span data-stu-id="2c949-213">Structures and Classes</span></span>](../../programming-guide/language-features/data-types/structures-and-classes.md)
- [<span data-ttu-id="2c949-214">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="2c949-214">Interface Statement</span></span>](interface-statement.md)
- [<span data-ttu-id="2c949-215">Module 语句</span><span class="sxs-lookup"><span data-stu-id="2c949-215">Module Statement</span></span>](module-statement.md)
- [<span data-ttu-id="2c949-216">Property Statement</span><span class="sxs-lookup"><span data-stu-id="2c949-216">Property Statement</span></span>](property-statement.md)
- [<span data-ttu-id="2c949-217">对象生存期：如何创建和销毁对象</span><span class="sxs-lookup"><span data-stu-id="2c949-217">Object Lifetime: How Objects Are Created and Destroyed</span></span>](../../programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
- [<span data-ttu-id="2c949-218">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2c949-218">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="2c949-219">如何：使用泛型类</span><span class="sxs-lookup"><span data-stu-id="2c949-219">How to: Use a Generic Class</span></span>](../../programming-guide/language-features/data-types/how-to-use-a-generic-class.md)
