---
description: '了解详细信息：结构和类 (Visual Basic) '
title: 结构和类
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], vs. structures
- structures [Visual Basic]
- classes [Visual Basic]
- structures [Visual Basic], compared to classes
- structures [Visual Basic], structure variables
- structure variables [Visual Basic]
ms.assetid: a221e74a-ffcf-4bdc-a0f6-a088a9bf26cc
ms.openlocfilehash: 129948bd9a16309ffea5b1e4c690d8883c450b74
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100430620"
---
# <a name="structures-and-classes-visual-basic"></a><span data-ttu-id="93fb8-103">结构和类 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="93fb8-103">Structures and Classes (Visual Basic)</span></span>

<span data-ttu-id="93fb8-104">Visual Basic 统一了结构和类的语法，因此，这两个实体支持大多数相同的功能。</span><span class="sxs-lookup"><span data-stu-id="93fb8-104">Visual Basic unifies the syntax for structures and classes, with the result that both entities support most of the same features.</span></span> <span data-ttu-id="93fb8-105">但结构和类之间也存在重要差异。</span><span class="sxs-lookup"><span data-stu-id="93fb8-105">However, there are also important differences between structures and classes.</span></span>  
  
 <span data-ttu-id="93fb8-106">类的优点是引用类型，传递引用比将结构变量传递到其所有数据更有效。</span><span class="sxs-lookup"><span data-stu-id="93fb8-106">Classes have the advantage of being reference types — passing a reference is more efficient than passing a structure variable with all its data.</span></span> <span data-ttu-id="93fb8-107">另一方面，结构不需要在全局堆上分配内存。</span><span class="sxs-lookup"><span data-stu-id="93fb8-107">On the other hand, structures do not require allocation of memory on the global heap.</span></span>  
  
 <span data-ttu-id="93fb8-108">由于不能从结构继承，因此结构应仅用于不需要扩展的对象。</span><span class="sxs-lookup"><span data-stu-id="93fb8-108">Because you cannot inherit from a structure, structures should be used only for objects that do not need to be extended.</span></span> <span data-ttu-id="93fb8-109">如果要创建的对象的实例大小较小，请使用结构，并考虑类与结构的性能特征。</span><span class="sxs-lookup"><span data-stu-id="93fb8-109">Use structures when the object you wish to create has a small instance size, and take into account the performance characteristics of classes versus structures.</span></span>  
  
## <a name="similarities"></a><span data-ttu-id="93fb8-110">相似性</span><span class="sxs-lookup"><span data-stu-id="93fb8-110">Similarities</span></span>  

 <span data-ttu-id="93fb8-111">结构和类在以下方面类似：</span><span class="sxs-lookup"><span data-stu-id="93fb8-111">Structures and classes are similar in the following respects:</span></span>  
  
- <span data-ttu-id="93fb8-112">两者都是 *容器* 类型，这意味着它们包含其他类型作为成员。</span><span class="sxs-lookup"><span data-stu-id="93fb8-112">Both are *container* types, meaning that they contain other types as members.</span></span>  
  
- <span data-ttu-id="93fb8-113">两者都具有成员，其中可以包含构造函数、方法、属性、字段、常量、枚举、事件和事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="93fb8-113">Both have members, which can include constructors, methods, properties, fields, constants, enumerations, events, and event handlers.</span></span> <span data-ttu-id="93fb8-114">但是，不要将这些成员与结构的已声明 *元素* 混淆。</span><span class="sxs-lookup"><span data-stu-id="93fb8-114">However, do not confuse these members with the declared *elements* of a structure.</span></span>  
  
- <span data-ttu-id="93fb8-115">两者的成员可以具有不同的访问级别。</span><span class="sxs-lookup"><span data-stu-id="93fb8-115">Members of both can have individualized access levels.</span></span> <span data-ttu-id="93fb8-116">例如，一个成员可以声明， `Public` 另一个成员 `Private` 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-116">For example, one member can be declared `Public` and another `Private`.</span></span>  
  
- <span data-ttu-id="93fb8-117">两者均可实现接口。</span><span class="sxs-lookup"><span data-stu-id="93fb8-117">Both can implement interfaces.</span></span>  
  
- <span data-ttu-id="93fb8-118">两者都可以具有共享构造函数（带有或不带参数）。</span><span class="sxs-lookup"><span data-stu-id="93fb8-118">Both can have shared constructors, with or without parameters.</span></span>  
  
- <span data-ttu-id="93fb8-119">两者都可以公开 *默认属性*，前提是该属性至少采用一个参数。</span><span class="sxs-lookup"><span data-stu-id="93fb8-119">Both can expose a *default property*, provided that property takes at least one parameter.</span></span>  
  
- <span data-ttu-id="93fb8-120">两者都可以声明和引发事件，并且两者都可以声明委托。</span><span class="sxs-lookup"><span data-stu-id="93fb8-120">Both can declare and raise events, and both can declare delegates.</span></span>  
  
## <a name="differences"></a><span data-ttu-id="93fb8-121">差异</span><span class="sxs-lookup"><span data-stu-id="93fb8-121">Differences</span></span>  

 <span data-ttu-id="93fb8-122">结构和类在以下方面有所不同：</span><span class="sxs-lookup"><span data-stu-id="93fb8-122">Structures and classes differ in the following particulars:</span></span>  
  
- <span data-ttu-id="93fb8-123">结构是 *值类型*;类是 *引用类型*。</span><span class="sxs-lookup"><span data-stu-id="93fb8-123">Structures are *value types*; classes are *reference types*.</span></span> <span data-ttu-id="93fb8-124">结构类型的变量包含结构的数据，而不是包含对作为类类型的数据的引用。</span><span class="sxs-lookup"><span data-stu-id="93fb8-124">A variable of a structure type contains the structure's data, rather than containing a reference to the data as a class type does.</span></span>  
  
- <span data-ttu-id="93fb8-125">结构使用堆栈分配;类使用堆分配。</span><span class="sxs-lookup"><span data-stu-id="93fb8-125">Structures use stack allocation; classes use heap allocation.</span></span>  
  
- <span data-ttu-id="93fb8-126">默认情况下，所有结构元素都是默认的; 默认情况下 `Public` ，类变量和常量是 `Private` 其他类成员 `Public` 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-126">All structure elements are `Public` by default; class variables and constants are `Private` by default, while other class members are `Public` by default.</span></span> <span data-ttu-id="93fb8-127">类成员的这种行为提供与 Visual Basic 6.0 系统的默认值的兼容性。</span><span class="sxs-lookup"><span data-stu-id="93fb8-127">This behavior for class members provides compatibility with the Visual Basic 6.0 system of defaults.</span></span>  
  
- <span data-ttu-id="93fb8-128">结构中必须至少有一个非共享变量或非共享的非自定义事件元素;类可以完全为空。</span><span class="sxs-lookup"><span data-stu-id="93fb8-128">A structure must have at least one nonshared variable or nonshared, noncustom event element; a class can be completely empty.</span></span>  
  
- <span data-ttu-id="93fb8-129">不能将结构元素声明为 `Protected` ; 类成员可以。</span><span class="sxs-lookup"><span data-stu-id="93fb8-129">Structure elements cannot be declared as `Protected`; class members can.</span></span>  
  
- <span data-ttu-id="93fb8-130">仅当结构过程是[共享](../../../language-reference/modifiers/shared.md) `Sub` 过程，并且仅通过[AddHandler 语句](../../../language-reference/statements/addhandler-statement.md)的方式处理时，结构过程才能处理事件; 任何类过程都可以使用[Handles](../../../language-reference/statements/handles-clause.md)关键字或语句处理事件 `AddHandler` 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-130">A structure procedure can handle events only if it is a [Shared](../../../language-reference/modifiers/shared.md)`Sub` procedure, and only by means of the [AddHandler Statement](../../../language-reference/statements/addhandler-statement.md); any class procedure can handle events, using either the [Handles](../../../language-reference/statements/handles-clause.md) keyword or the `AddHandler` statement.</span></span> <span data-ttu-id="93fb8-131">有关详细信息，请参阅[事件](../events/index.md)。</span><span class="sxs-lookup"><span data-stu-id="93fb8-131">For more information, see [Events](../events/index.md).</span></span>  
  
- <span data-ttu-id="93fb8-132">结构变量声明不能为数组指定初始值设定项或初始大小;类变量声明可以。</span><span class="sxs-lookup"><span data-stu-id="93fb8-132">Structure variable declarations cannot specify initializers or initial sizes for arrays; class variable declarations can.</span></span>  
  
- <span data-ttu-id="93fb8-133">结构隐式继承自 <xref:System.ValueType?displayProperty=nameWithType> 类，且不能从任何其他类型继承; 类可以继承自以外的任何类 <xref:System.ValueType?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-133">Structures implicitly inherit from the <xref:System.ValueType?displayProperty=nameWithType> class and cannot inherit from any other type; classes can inherit from any class or classes other than <xref:System.ValueType?displayProperty=nameWithType>.</span></span>  
  
- <span data-ttu-id="93fb8-134">结构不可继承;类为。</span><span class="sxs-lookup"><span data-stu-id="93fb8-134">Structures are not inheritable; classes are.</span></span>  
  
- <span data-ttu-id="93fb8-135">结构永远都不会终止，因此，公共语言运行时 (CLR) 从不对 <xref:System.Object.Finalize%2A> 任何结构调用方法; 类由垃圾回收器 (GC) 终止，后者 <xref:System.Object.Finalize%2A> 在检测到没有剩余的活动引用时调用类。</span><span class="sxs-lookup"><span data-stu-id="93fb8-135">Structures are never terminated, so the common language runtime (CLR) never calls the <xref:System.Object.Finalize%2A> method on any structure; classes are terminated by the garbage collector (GC), which calls <xref:System.Object.Finalize%2A> on a class when it detects there are no active references remaining.</span></span>  
  
- <span data-ttu-id="93fb8-136">结构不需要构造函数;类。</span><span class="sxs-lookup"><span data-stu-id="93fb8-136">A structure does not require a constructor; a class does.</span></span>  
  
- <span data-ttu-id="93fb8-137">仅当结构使用参数时，才可具有非共享构造函数;类可以具有或不带参数。</span><span class="sxs-lookup"><span data-stu-id="93fb8-137">Structures can have nonshared constructors only if they take parameters; classes can have them with or without parameters.</span></span>  
  
 <span data-ttu-id="93fb8-138">每个结构都具有一个不带参数的隐式公共构造函数。</span><span class="sxs-lookup"><span data-stu-id="93fb8-138">Every structure has an implicit public constructor without parameters.</span></span> <span data-ttu-id="93fb8-139">此构造函数将结构的所有数据元素初始化为其默认值。</span><span class="sxs-lookup"><span data-stu-id="93fb8-139">This constructor initializes all the structure's data elements to their default values.</span></span> <span data-ttu-id="93fb8-140">不能重新定义此行为。</span><span class="sxs-lookup"><span data-stu-id="93fb8-140">You cannot redefine this behavior.</span></span>  
  
## <a name="instances-and-variables"></a><span data-ttu-id="93fb8-141">实例和变量</span><span class="sxs-lookup"><span data-stu-id="93fb8-141">Instances and Variables</span></span>  

 <span data-ttu-id="93fb8-142">由于结构是值类型，因此每个结构变量将永久绑定到单个结构实例。</span><span class="sxs-lookup"><span data-stu-id="93fb8-142">Because structures are value types, each structure variable is permanently bound to an individual structure instance.</span></span> <span data-ttu-id="93fb8-143">但类是引用类型，而对象变量可在不同时间引用各种类实例。</span><span class="sxs-lookup"><span data-stu-id="93fb8-143">But classes are reference types, and an object variable can refer to various class instances at different times.</span></span> <span data-ttu-id="93fb8-144">这种区分会按以下方式影响结构和类的使用：</span><span class="sxs-lookup"><span data-stu-id="93fb8-144">This distinction affects your usage of structures and classes in the following ways:</span></span>  
  
- <span data-ttu-id="93fb8-145">**初始化。**</span><span class="sxs-lookup"><span data-stu-id="93fb8-145">**Initialization.**</span></span> <span data-ttu-id="93fb8-146">结构变量使用结构的无参数构造函数隐式包括元素的初始化。</span><span class="sxs-lookup"><span data-stu-id="93fb8-146">A structure variable implicitly includes an initialization of the elements using the structure's parameterless constructor.</span></span> <span data-ttu-id="93fb8-147">因此， `Dim s As struct1` 等效于 `Dim s As struct1 = New struct1()` 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-147">Therefore, `Dim s As struct1` is equivalent to `Dim s As struct1 = New struct1()`.</span></span>  
  
- <span data-ttu-id="93fb8-148">**分配变量。**</span><span class="sxs-lookup"><span data-stu-id="93fb8-148">**Assigning Variables.**</span></span> <span data-ttu-id="93fb8-149">将一个结构变量分配给另一个结构变量或将结构实例传递给过程参数时，所有变量元素的当前值都将复制到新结构。</span><span class="sxs-lookup"><span data-stu-id="93fb8-149">When you assign one structure variable to another, or pass a structure instance to a procedure argument, the current values of all the variable elements are copied to the new structure.</span></span> <span data-ttu-id="93fb8-150">当您将一个对象变量分配给另一个对象变量，或将一个对象变量传递给某个过程时，只会复制引用指针。</span><span class="sxs-lookup"><span data-stu-id="93fb8-150">When you assign one object variable to another, or pass an object variable to a procedure, only the reference pointer is copied.</span></span>  
  
- <span data-ttu-id="93fb8-151">**不分配任何内容。**</span><span class="sxs-lookup"><span data-stu-id="93fb8-151">**Assigning Nothing.**</span></span> <span data-ttu-id="93fb8-152">您可以将值 [Nothing](../../../language-reference/nothing.md) 赋给结构变量，但该实例继续与变量关联。</span><span class="sxs-lookup"><span data-stu-id="93fb8-152">You can assign the value [Nothing](../../../language-reference/nothing.md) to a structure variable, but the instance continues to be associated with the variable.</span></span> <span data-ttu-id="93fb8-153">尽管变量元素由赋值重新初始化，仍可以调用其方法并访问其数据元素。</span><span class="sxs-lookup"><span data-stu-id="93fb8-153">You can still call its methods and access its data elements, although variable elements are reinitialized by the assignment.</span></span>  
  
     <span data-ttu-id="93fb8-154">与此相反，如果您将一个对象变量设置为 `Nothing` ，则将其与任何类实例取消关联，并且您无法通过该变量访问任何成员，除非您向其分配了其他实例。</span><span class="sxs-lookup"><span data-stu-id="93fb8-154">In contrast, if you set an object variable to `Nothing`, you dissociate it from any class instance, and you cannot access any members through the variable until you assign another instance to it.</span></span>  
  
- <span data-ttu-id="93fb8-155">**多个实例。**</span><span class="sxs-lookup"><span data-stu-id="93fb8-155">**Multiple Instances.**</span></span> <span data-ttu-id="93fb8-156">对象变量可在不同时间分配给它的不同类实例，而多个对象变量可同时引用相同的类实例。</span><span class="sxs-lookup"><span data-stu-id="93fb8-156">An object variable can have different class instances assigned to it at different times, and several object variables can refer to the same class instance at the same time.</span></span> <span data-ttu-id="93fb8-157">对类成员的值所做的更改会在通过指向同一实例的另一个变量进行访问时影响这些成员。</span><span class="sxs-lookup"><span data-stu-id="93fb8-157">Changes you make to the values of class members affect those members when accessed through another variable pointing to the same instance.</span></span>  
  
     <span data-ttu-id="93fb8-158">但是，结构元素在其自己的实例中是隔离的。</span><span class="sxs-lookup"><span data-stu-id="93fb8-158">Structure elements, however, are isolated within their own instance.</span></span> <span data-ttu-id="93fb8-159">对其值所做的更改不会反映在其他任何结构变量中，即使在同一声明的其他实例中也是如此 `Structure` 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-159">Changes to their values are not reflected in any other structure variables, even in other instances of the same `Structure` declaration.</span></span>  
  
- <span data-ttu-id="93fb8-160">**等于.**</span><span class="sxs-lookup"><span data-stu-id="93fb8-160">**Equality.**</span></span> <span data-ttu-id="93fb8-161">必须使用逐个元素测试来执行两个结构的相等性测试。</span><span class="sxs-lookup"><span data-stu-id="93fb8-161">Equality testing of two structures must be performed with an element-by-element test.</span></span> <span data-ttu-id="93fb8-162">可以使用方法比较两个对象变量 <xref:System.Object.Equals%2A> 。</span><span class="sxs-lookup"><span data-stu-id="93fb8-162">Two object variables can be compared using the <xref:System.Object.Equals%2A> method.</span></span> <span data-ttu-id="93fb8-163"><xref:System.Object.Equals%2A> 指示两个变量是否指向同一个实例。</span><span class="sxs-lookup"><span data-stu-id="93fb8-163"><xref:System.Object.Equals%2A> indicates whether the two variables point to the same instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93fb8-164">请参阅</span><span class="sxs-lookup"><span data-stu-id="93fb8-164">See also</span></span>

- [<span data-ttu-id="93fb8-165">数据类型</span><span class="sxs-lookup"><span data-stu-id="93fb8-165">Data Types</span></span>](index.md)
- [<span data-ttu-id="93fb8-166">复合数据类型</span><span class="sxs-lookup"><span data-stu-id="93fb8-166">Composite Data Types</span></span>](composite-data-types.md)
- [<span data-ttu-id="93fb8-167">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="93fb8-167">Value Types and Reference Types</span></span>](value-types-and-reference-types.md)
- [<span data-ttu-id="93fb8-168">结构</span><span class="sxs-lookup"><span data-stu-id="93fb8-168">Structures</span></span>](structures.md)
- [<span data-ttu-id="93fb8-169">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="93fb8-169">Troubleshooting Data Types</span></span>](troubleshooting-data-types.md)
- [<span data-ttu-id="93fb8-170">结构和其他编程元素</span><span class="sxs-lookup"><span data-stu-id="93fb8-170">Structures and Other Programming Elements</span></span>](structures-and-other-programming-elements.md)
- [<span data-ttu-id="93fb8-171">对象和类</span><span class="sxs-lookup"><span data-stu-id="93fb8-171">Objects and Classes</span></span>](../objects-and-classes/index.md)
