---
description: '了解更多相关信息：面向对象的编程 (Visual Basic) '
title: 面向对象的编程
ms.date: 07/20/2015
ms.assetid: 49794de4-64c3-473c-b8ed-fe98835df69c
ms.openlocfilehash: af2fbac16bfefc90876bf22bb8c67de162ee6459
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100486792"
---
# <a name="object-oriented-programming-visual-basic"></a><span data-ttu-id="b8690-103">面向对象的编程 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="b8690-103">Object-oriented programming (Visual Basic)</span></span>

<span data-ttu-id="b8690-104">Visual Basic 完全支持面向对象的编程，包括封装、继承和多态性。</span><span class="sxs-lookup"><span data-stu-id="b8690-104">Visual Basic provides full support for object-oriented programming including encapsulation, inheritance, and polymorphism.</span></span>

 <span data-ttu-id="b8690-105">“封装”意味着将一组相关属性、方法和其他成员视为一个单元或对象。</span><span class="sxs-lookup"><span data-stu-id="b8690-105">*Encapsulation* means that a group of related properties, methods, and other members are treated as a single unit or object.</span></span>

 <span data-ttu-id="b8690-106">“继承”描述基于现有类创建新类的能力。</span><span class="sxs-lookup"><span data-stu-id="b8690-106">*Inheritance* describes the ability to create new classes based on an existing class.</span></span>

 <span data-ttu-id="b8690-107">多态性意味着可以有多个可互换使用的类，即使每个类以不同方式实现相同属性或方法。</span><span class="sxs-lookup"><span data-stu-id="b8690-107">*Polymorphism* means that you can have multiple classes that can be used interchangeably, even though each class implements the same properties or methods in different ways.</span></span>

 <span data-ttu-id="b8690-108">本节介绍下列概念：</span><span class="sxs-lookup"><span data-stu-id="b8690-108">This section describes the following concepts:</span></span>

- [<span data-ttu-id="b8690-109">类和对象</span><span class="sxs-lookup"><span data-stu-id="b8690-109">Classes and objects</span></span>](#classes-and-objects)
  - [<span data-ttu-id="b8690-110">类成员</span><span class="sxs-lookup"><span data-stu-id="b8690-110">Class members</span></span>](#class-members)
    - [<span data-ttu-id="b8690-111">属性和字段</span><span class="sxs-lookup"><span data-stu-id="b8690-111">Properties and fields</span></span>](#properties-and-fields)
    - [<span data-ttu-id="b8690-112">方法</span><span class="sxs-lookup"><span data-stu-id="b8690-112">Methods</span></span>](#methods)
    - [<span data-ttu-id="b8690-113">构造函数</span><span class="sxs-lookup"><span data-stu-id="b8690-113">Constructors</span></span>](#constructors)
    - [<span data-ttu-id="b8690-114">析构函数</span><span class="sxs-lookup"><span data-stu-id="b8690-114">Destructors</span></span>](#destructors)
    - [<span data-ttu-id="b8690-115">事件</span><span class="sxs-lookup"><span data-stu-id="b8690-115">Events</span></span>](#events)
    - [<span data-ttu-id="b8690-116">嵌套类</span><span class="sxs-lookup"><span data-stu-id="b8690-116">Nested classes</span></span>](#nested-classes)
  - [<span data-ttu-id="b8690-117">访问修饰符和访问级别</span><span class="sxs-lookup"><span data-stu-id="b8690-117">Access modifiers and access levels</span></span>](#access-modifiers-and-access-levels)
    - [<span data-ttu-id="b8690-118">实例化类</span><span class="sxs-lookup"><span data-stu-id="b8690-118">Instantiating classes</span></span>](#instantiating-classes)
    - [<span data-ttu-id="b8690-119">共享类和成员</span><span class="sxs-lookup"><span data-stu-id="b8690-119">Shared classes and members</span></span>](#shared-classes-and-members)
    - [<span data-ttu-id="b8690-120">匿名类型</span><span class="sxs-lookup"><span data-stu-id="b8690-120">Anonymous types</span></span>](#anonymous-types)
- [<span data-ttu-id="b8690-121">继承</span><span class="sxs-lookup"><span data-stu-id="b8690-121">Inheritance</span></span>](#inheritance)
  - [<span data-ttu-id="b8690-122">重写成员</span><span class="sxs-lookup"><span data-stu-id="b8690-122">Overriding members</span></span>](#overriding-members)
- [<span data-ttu-id="b8690-123">接口</span><span class="sxs-lookup"><span data-stu-id="b8690-123">Interfaces</span></span>](#interfaces)
- [<span data-ttu-id="b8690-124">泛型</span><span class="sxs-lookup"><span data-stu-id="b8690-124">Generics</span></span>](#generics)
- [<span data-ttu-id="b8690-125">委托</span><span class="sxs-lookup"><span data-stu-id="b8690-125">Delegates</span></span>](#delegates)

## <a name="classes-and-objects"></a><span data-ttu-id="b8690-126">类和对象</span><span class="sxs-lookup"><span data-stu-id="b8690-126">Classes and objects</span></span>

<span data-ttu-id="b8690-127">“类”和“对象”这两个术语有时互换使用，但实际上，类描述对象的“类型”，而对象是类的可用“实例”。</span><span class="sxs-lookup"><span data-stu-id="b8690-127">The terms *class* and *object* are sometimes used interchangeably, but in fact, classes describe the *type* of objects, while objects are usable *instances* of classes.</span></span> <span data-ttu-id="b8690-128">因此，创建对象的操作称为“实例化”。</span><span class="sxs-lookup"><span data-stu-id="b8690-128">So, the act of creating an object is called *instantiation*.</span></span> <span data-ttu-id="b8690-129">如果使用蓝图类比，类是蓝图，对象就是基于该蓝图的建筑。</span><span class="sxs-lookup"><span data-stu-id="b8690-129">Using the blueprint analogy, a class is a blueprint, and an object is a building made from that blueprint.</span></span>

<span data-ttu-id="b8690-130">定义类：</span><span class="sxs-lookup"><span data-stu-id="b8690-130">To define a class:</span></span>

```vb
Class SampleClass
End Class
```

<span data-ttu-id="b8690-131">Visual Basic 还提供了类的轻量类，这些类称为 *结构* ，当需要创建大量对象且不希望对其消耗太多内存时，它们非常有用。</span><span class="sxs-lookup"><span data-stu-id="b8690-131">Visual Basic also provides a light version of classes called *structures* that are useful when you need to create large array of objects and do not want to consume too much memory for that.</span></span>

<span data-ttu-id="b8690-132">定义结构：</span><span class="sxs-lookup"><span data-stu-id="b8690-132">To define a structure:</span></span>

```vb
Structure SampleStructure
End Structure
```

<span data-ttu-id="b8690-133">有关详情，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-133">For more information, see:</span></span>

- [<span data-ttu-id="b8690-134">Class 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-134">Class Statement</span></span>](../../language-reference/statements/class-statement.md)
- [<span data-ttu-id="b8690-135">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-135">Structure Statement</span></span>](../../language-reference/statements/structure-statement.md)

### <a name="class-members"></a><span data-ttu-id="b8690-136">类成员</span><span class="sxs-lookup"><span data-stu-id="b8690-136">Class members</span></span>

<span data-ttu-id="b8690-137">每个类都可以具有不同的“类成员”。类成员包括属性（用于描述类数据）、方法（用于定义类行为）和事件（用于在不同的类和对象之间提供通信）。</span><span class="sxs-lookup"><span data-stu-id="b8690-137">Each class can have different *class members* that include properties that describe class data, methods that define class behavior, and events that provide communication between different classes and objects.</span></span>

#### <a name="properties-and-fields"></a><span data-ttu-id="b8690-138">属性和字段</span><span class="sxs-lookup"><span data-stu-id="b8690-138">Properties and fields</span></span>

<span data-ttu-id="b8690-139">字段和属性表示对象包含的信息。</span><span class="sxs-lookup"><span data-stu-id="b8690-139">Fields and properties represent information that an object contains.</span></span> <span data-ttu-id="b8690-140">字段类似于变量，因为可以直接读取或设置它们。</span><span class="sxs-lookup"><span data-stu-id="b8690-140">Fields are like variables because they can be read or set directly.</span></span>

<span data-ttu-id="b8690-141">定义字段：</span><span class="sxs-lookup"><span data-stu-id="b8690-141">To define a field:</span></span>

```vb
Class SampleClass
    Public SampleField As String
End Class
```

<span data-ttu-id="b8690-142">属性具有 get 和 set 过程，它们对如何设置或返回值提供更多的控制。</span><span class="sxs-lookup"><span data-stu-id="b8690-142">Properties have get and set procedures, which provide more control on how values are set or returned.</span></span>

<span data-ttu-id="b8690-143">Visual Basic 允许你创建私有字段来存储属性值，或者使用称为自动实现的属性，这些属性在幕后自动创建此字段，并为属性过程提供基本逻辑。</span><span class="sxs-lookup"><span data-stu-id="b8690-143">Visual Basic allows you either to create a private field for storing the property value or use so-called auto-implemented properties that create this field automatically behind the scenes and provide the basic logic for the property procedures.</span></span>

<span data-ttu-id="b8690-144">定义自动实现的属性：</span><span class="sxs-lookup"><span data-stu-id="b8690-144">To define an auto-implemented property:</span></span>

```vb
Class SampleClass
    Public Property SampleProperty as String
End Class
```

<span data-ttu-id="b8690-145">如果你需要执行一些其他操作来读取和写入属性值，请定义一个用于存储属性值的字段，并提供用于存储和检索该字段的基本逻辑：</span><span class="sxs-lookup"><span data-stu-id="b8690-145">If you need to perform some additional operations for reading and writing the property value, define a field for storing the property value and provide the basic logic for storing and retrieving it:</span></span>

```vb
Class SampleClass
    Private m_Sample As String
    Public Property Sample() As String
        Get
            ' Return the value stored in the field.
            Return m_Sample
        End Get
        Set(ByVal Value As String)
            ' Store the value in the field.
            m_Sample = Value
        End Set
    End Property
End Class
```

<span data-ttu-id="b8690-146">大多数属性的方法或过程都是既可以设置也可以获取属性值。</span><span class="sxs-lookup"><span data-stu-id="b8690-146">Most properties have methods or procedures to both set and get the property value.</span></span> <span data-ttu-id="b8690-147">但你可以创建只读或只写属性来限制对它们的修改或读取。</span><span class="sxs-lookup"><span data-stu-id="b8690-147">However, you can create read-only or write-only properties to restrict them from being modified or read.</span></span> <span data-ttu-id="b8690-148">在 Visual Basic 中，可以使用 `ReadOnly` 和 `WriteOnly` 关键字。</span><span class="sxs-lookup"><span data-stu-id="b8690-148">In Visual Basic you can use `ReadOnly` and `WriteOnly` keywords.</span></span> <span data-ttu-id="b8690-149">但是，自动实现的属性不能为只读或只写。</span><span class="sxs-lookup"><span data-stu-id="b8690-149">However, auto-implemented properties cannot be read-only or write-only.</span></span>

<span data-ttu-id="b8690-150">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-150">For more information, see:</span></span>

- [<span data-ttu-id="b8690-151">Property Statement</span><span class="sxs-lookup"><span data-stu-id="b8690-151">Property Statement</span></span>](../../language-reference/statements/property-statement.md)
- [<span data-ttu-id="b8690-152">Get 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-152">Get Statement</span></span>](../../language-reference/statements/get-statement.md)
- [<span data-ttu-id="b8690-153">Set 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-153">Set Statement</span></span>](../../language-reference/statements/set-statement.md)
- [<span data-ttu-id="b8690-154">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b8690-154">ReadOnly</span></span>](../../language-reference/modifiers/readonly.md)
- [<span data-ttu-id="b8690-155">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="b8690-155">WriteOnly</span></span>](../../language-reference/modifiers/writeonly.md)

#### <a name="methods"></a><span data-ttu-id="b8690-156">方法</span><span class="sxs-lookup"><span data-stu-id="b8690-156">Methods</span></span>

 <span data-ttu-id="b8690-157">“方法”是对象可以执行的操作。</span><span class="sxs-lookup"><span data-stu-id="b8690-157">A *method* is an action that an object can perform.</span></span>

> [!NOTE]
> <span data-ttu-id="b8690-158">在 Visual Basic 中，方法的创建途径有两种：如果方法不返回值，可使用 `Sub` 语句；如果方法返回值，可使用 `Function` 语句。</span><span class="sxs-lookup"><span data-stu-id="b8690-158">In Visual Basic, there are two ways to create a method: the `Sub` statement is used if the method does not return a value; the `Function` statement is used if a method returns a value.</span></span>

<span data-ttu-id="b8690-159">定义类的方法：</span><span class="sxs-lookup"><span data-stu-id="b8690-159">To define a method of a class:</span></span>

```vb
Class SampleClass
    Public Function SampleFunc(ByVal SampleParam As String)
        ' Add code here
    End Function
End Class
```

<span data-ttu-id="b8690-160">对于同一方法，一个类可以有多个实现，也叫“重载”，这些实现的区别在于参数个数或参数类型的不同。</span><span class="sxs-lookup"><span data-stu-id="b8690-160">A class can have several implementations, or *overloads*, of the same method that differ in the number of parameters or parameter types.</span></span>

<span data-ttu-id="b8690-161">重载方法：</span><span class="sxs-lookup"><span data-stu-id="b8690-161">To overload a method:</span></span>

```vb
Overloads Sub Display(ByVal theChar As Char)
    ' Add code that displays Char data.
End Sub
Overloads Sub Display(ByVal theInteger As Integer)
    ' Add code that displays Integer data.
End Sub
```

<span data-ttu-id="b8690-162">大多数情况下，方法是在类定义中声明的。</span><span class="sxs-lookup"><span data-stu-id="b8690-162">In most cases you declare a method within a class definition.</span></span> <span data-ttu-id="b8690-163">不过，Visual Basic 还支持 *扩展方法* ，这些方法允许你将方法添加到类的实际定义之外的现有类中。</span><span class="sxs-lookup"><span data-stu-id="b8690-163">However, Visual Basic also supports *extension methods* that allow you to add methods to an existing class outside the actual definition of the class.</span></span>

<span data-ttu-id="b8690-164">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-164">For more information, see:</span></span>

- [<span data-ttu-id="b8690-165">Function 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-165">Function Statement</span></span>](../../language-reference/statements/function-statement.md)
- [<span data-ttu-id="b8690-166">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-166">Sub Statement</span></span>](../../language-reference/statements/sub-statement.md)
- [<span data-ttu-id="b8690-167">重载</span><span class="sxs-lookup"><span data-stu-id="b8690-167">Overloads</span></span>](../../language-reference/modifiers/overloads.md)
- [<span data-ttu-id="b8690-168">扩展方法</span><span class="sxs-lookup"><span data-stu-id="b8690-168">Extension Methods</span></span>](../language-features/procedures/extension-methods.md)

#### <a name="constructors"></a><span data-ttu-id="b8690-169">构造函数</span><span class="sxs-lookup"><span data-stu-id="b8690-169">Constructors</span></span>

<span data-ttu-id="b8690-170">构造函数一种类方法，它们在创建给定类型的对象时自动执行。</span><span class="sxs-lookup"><span data-stu-id="b8690-170">Constructors are class methods that are executed automatically when an object of a given type is created.</span></span> <span data-ttu-id="b8690-171">构造函数通常用于初始化新对象的数据成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-171">Constructors usually initialize the data members of the new object.</span></span> <span data-ttu-id="b8690-172">构造函数只能在创建类时运行一次。</span><span class="sxs-lookup"><span data-stu-id="b8690-172">A constructor can run only once when a class is created.</span></span> <span data-ttu-id="b8690-173">此外，构造函数中的代码始终在类中所有其他代码之前运行。</span><span class="sxs-lookup"><span data-stu-id="b8690-173">Furthermore, the code in the constructor always runs before any other code in a class.</span></span> <span data-ttu-id="b8690-174">但是，你可以按照为任何其他方法创建重载的方式，创建多个构造函数重载。</span><span class="sxs-lookup"><span data-stu-id="b8690-174">However, you can create multiple constructor overloads in the same way as for any other method.</span></span>

<span data-ttu-id="b8690-175">定义类的构造函数：</span><span class="sxs-lookup"><span data-stu-id="b8690-175">To define a constructor for a class:</span></span>

```vb
Class SampleClass
    Sub New(ByVal s As String)
        // Add code here.
    End Sub
End Class
```

<span data-ttu-id="b8690-176">有关详细信息，请参阅： [对象生存期：如何创建和销毁对象](../language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-176">For more information, see: [Object Lifetime: How Objects Are Created and Destroyed](../language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md).</span></span>

#### <a name="destructors"></a><span data-ttu-id="b8690-177">析构函数</span><span class="sxs-lookup"><span data-stu-id="b8690-177">Destructors</span></span>

<span data-ttu-id="b8690-178">析构函数用于析构类的实例。</span><span class="sxs-lookup"><span data-stu-id="b8690-178">Destructors are used to destruct instances of classes.</span></span> <span data-ttu-id="b8690-179">在 .NET Framework 中，垃圾回收器自动管理应用程序中托管对象的内存分配和释放。</span><span class="sxs-lookup"><span data-stu-id="b8690-179">In the .NET Framework, the garbage collector automatically manages the allocation and release of memory for the managed objects in your application.</span></span> <span data-ttu-id="b8690-180">但是，你可能仍会需要析构函数来清理应用程序创建的所有非托管资源。</span><span class="sxs-lookup"><span data-stu-id="b8690-180">However, you may still need destructors to clean up any unmanaged resources that your application creates.</span></span> <span data-ttu-id="b8690-181">一个类只能有一个析构函数。</span><span class="sxs-lookup"><span data-stu-id="b8690-181">There can be only one destructor for a class.</span></span>

<span data-ttu-id="b8690-182">有关析构函数和 .NET Framework 垃圾回收的详细信息，请参阅[垃圾回收](../../../standard/garbage-collection/index.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-182">For more information about destructors and garbage collection in the .NET Framework, see [Garbage Collection](../../../standard/garbage-collection/index.md).</span></span>

#### <a name="events"></a><span data-ttu-id="b8690-183">事件</span><span class="sxs-lookup"><span data-stu-id="b8690-183">Events</span></span>

<span data-ttu-id="b8690-184">类或对象可以通过事件向其他类或对象通知发生的相关事情。</span><span class="sxs-lookup"><span data-stu-id="b8690-184">Events enable a class or object to notify other classes or objects when something of interest occurs.</span></span> <span data-ttu-id="b8690-185">发送（或引发）事件的类称为“发行者”，接收（或处理）事件的类称为“订户”。</span><span class="sxs-lookup"><span data-stu-id="b8690-185">The class that sends (or raises) the event is called the *publisher* and the classes that receive (or handle) the event are called *subscribers*.</span></span> <span data-ttu-id="b8690-186">有关事件以及如何引发和处理事件的详细信息，请参阅[事件](../../../standard/events/index.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-186">For more information about events, how they are raised and handled, see [Events](../../../standard/events/index.md).</span></span>

- <span data-ttu-id="b8690-187">若要声明事件，请使用 [Event 语句](../../language-reference/statements/event-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-187">To declare events, use the [Event Statement](../../language-reference/statements/event-statement.md).</span></span>

- <span data-ttu-id="b8690-188">若要引发事件，请使用 [RaiseEvent 语句](../../language-reference/statements/raiseevent-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-188">To raise events, use the [RaiseEvent Statement](../../language-reference/statements/raiseevent-statement.md).</span></span>

- <span data-ttu-id="b8690-189">若要使用声明性方式指定事件处理程序，请使用 [WithEvents](../../language-reference/modifiers/withevents.md) 语句和 [Handles](../../language-reference/statements/handles-clause.md) 子句。</span><span class="sxs-lookup"><span data-stu-id="b8690-189">To specify event handlers using a declarative way, use the [WithEvents](../../language-reference/modifiers/withevents.md) statement and the [Handles](../../language-reference/statements/handles-clause.md) clause.</span></span>

- <span data-ttu-id="b8690-190">若要能够动态地添加、删除和更改与事件关联的事件处理程序，请将 [AddHandler 语句](../../language-reference/statements/addhandler-statement.md) 和 [RemoveHandler 语句](../../language-reference/statements/removehandler-statement.md) 与 [AddressOf 运算符](../../language-reference/operators/addressof-operator.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="b8690-190">To be able to dynamically add, remove, and change the event handler associated with an event, use the [AddHandler Statement](../../language-reference/statements/addhandler-statement.md) and [RemoveHandler Statement](../../language-reference/statements/removehandler-statement.md) together with the [AddressOf Operator](../../language-reference/operators/addressof-operator.md).</span></span>

#### <a name="nested-classes"></a><span data-ttu-id="b8690-191">嵌套类</span><span class="sxs-lookup"><span data-stu-id="b8690-191">Nested classes</span></span>

<span data-ttu-id="b8690-192">在另一个类中定义的类称为“嵌套”。</span><span class="sxs-lookup"><span data-stu-id="b8690-192">A class defined within another class is called *nested*.</span></span> <span data-ttu-id="b8690-193">默认情况下，嵌套类是私有类。</span><span class="sxs-lookup"><span data-stu-id="b8690-193">By default, the nested class is private.</span></span>

```vb
Class Container
    Class Nested
    ' Add code here.
    End Class
End Class
```

<span data-ttu-id="b8690-194">若要创建嵌套类的实例，请使用容器类的名称，后接一个点，再接嵌套类的名称：</span><span class="sxs-lookup"><span data-stu-id="b8690-194">To create an instance of the nested class, use the name of the container class followed by the dot and then followed by the name of the nested class:</span></span>

```vb
Dim nestedInstance As Container.Nested = New Container.Nested()
```

### <a name="access-modifiers-and-access-levels"></a><span data-ttu-id="b8690-195">访问修饰符和访问级别</span><span class="sxs-lookup"><span data-stu-id="b8690-195">Access modifiers and access levels</span></span>

<span data-ttu-id="b8690-196">所有类和类方法都可以使用“访问修饰符”指定自己为其他类提供的访问级别。</span><span class="sxs-lookup"><span data-stu-id="b8690-196">All classes and class members can specify what access level they provide to other classes by using *access modifiers*.</span></span>

<span data-ttu-id="b8690-197">可用的访问修饰符有以下这些：</span><span class="sxs-lookup"><span data-stu-id="b8690-197">The following access modifiers are available:</span></span>

|<span data-ttu-id="b8690-198">Visual Basic 修饰符</span><span class="sxs-lookup"><span data-stu-id="b8690-198">Visual Basic Modifier</span></span>|<span data-ttu-id="b8690-199">定义</span><span class="sxs-lookup"><span data-stu-id="b8690-199">Definition</span></span>|
|---------------------------|----------------|
|[<span data-ttu-id="b8690-200">公共</span><span class="sxs-lookup"><span data-stu-id="b8690-200">Public</span></span>](../../language-reference/modifiers/public.md)|<span data-ttu-id="b8690-201">同一程序集中的任何其他代码或引用该程序集的其他程序集都可以访问该类型或成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-201">The type or member can be accessed by any other code in the same assembly or another assembly that references it.</span></span>|
|[<span data-ttu-id="b8690-202">专用</span><span class="sxs-lookup"><span data-stu-id="b8690-202">Private</span></span>](../../language-reference/modifiers/private.md)|<span data-ttu-id="b8690-203">只有同一类中的代码可以访问该类型或成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-203">The type or member can only be accessed by code in the same class.</span></span>|
|[<span data-ttu-id="b8690-204">避免</span><span class="sxs-lookup"><span data-stu-id="b8690-204">Protected</span></span>](../../language-reference/modifiers/protected.md)|<span data-ttu-id="b8690-205">只有同一类或派生类中的代码可以访问该类型或成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-205">The type or member can only be accessed by code in the same class or in a derived class.</span></span>|
|[<span data-ttu-id="b8690-206">Friend</span><span class="sxs-lookup"><span data-stu-id="b8690-206">Friend</span></span>](../../language-reference/modifiers/friend.md)|<span data-ttu-id="b8690-207">同一程序集中的任何代码都可以访问该类型或成员，但其他程序集中的代码不可以。</span><span class="sxs-lookup"><span data-stu-id="b8690-207">The type or member can be accessed by any code in the same assembly, but not from another assembly.</span></span>|
|`Protected Friend`|<span data-ttu-id="b8690-208">同一程序集中的任何代码或其他程序集中的任何派生类都可以访问该类型或成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-208">The type or member can be accessed by any code in the same assembly, or by any derived class in another assembly.</span></span>|

<span data-ttu-id="b8690-209">有关详细信息，请参阅 [Visual Basic 中的访问级别](../language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-209">For more information, see [Access levels in Visual Basic](../language-features/declared-elements/access-levels.md).</span></span>

### <a name="instantiating-classes"></a><span data-ttu-id="b8690-210">实例化类</span><span class="sxs-lookup"><span data-stu-id="b8690-210">Instantiating classes</span></span>

<span data-ttu-id="b8690-211">若要创建对象，你需要实例化类，即创建类实例。</span><span class="sxs-lookup"><span data-stu-id="b8690-211">To create an object, you need to instantiate a class, or create a class instance.</span></span>

```vb
Dim sampleObject as New SampleClass()
```

<span data-ttu-id="b8690-212">实例化类之后，可以为该实例的属性和字段赋值，还可以调用类方法。</span><span class="sxs-lookup"><span data-stu-id="b8690-212">After instantiating a class, you can assign values to the instance's properties and fields and invoke class methods.</span></span>

```vb
' Set a property value.
sampleObject.SampleProperty = "Sample String"
' Call a method.
sampleObject.SampleMethod()
```

<span data-ttu-id="b8690-213">若要在类的实例化过程中为属性赋值，请使用对象初始值设定项：</span><span class="sxs-lookup"><span data-stu-id="b8690-213">To assign values to properties during the class instantiation process, use object initializers:</span></span>

```vb
Dim sampleObject = New SampleClass With
    {.FirstProperty = "A", .SecondProperty = "B"}
```

<span data-ttu-id="b8690-214">有关详情，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-214">For more information, see:</span></span>

- [<span data-ttu-id="b8690-215">新建操作员</span><span class="sxs-lookup"><span data-stu-id="b8690-215">New Operator</span></span>](../../language-reference/operators/new-operator.md)
- [<span data-ttu-id="b8690-216">对象初始值设定项：命名和匿名类型</span><span class="sxs-lookup"><span data-stu-id="b8690-216">Object Initializers: Named and Anonymous Types</span></span>](../language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)

### <a name="shared-classes-and-members"></a><span data-ttu-id="b8690-217">共享类和成员</span><span class="sxs-lookup"><span data-stu-id="b8690-217">Shared classes and members</span></span>

 <span data-ttu-id="b8690-218">类的共享成员是一个由类的所有实例共享的属性、过程或字段。</span><span class="sxs-lookup"><span data-stu-id="b8690-218">A shared member of the class is a property, procedure, or field that is shared by all instances of a class.</span></span>

 <span data-ttu-id="b8690-219">定义共享成员：</span><span class="sxs-lookup"><span data-stu-id="b8690-219">To define a shared member:</span></span>

```vb
Class SampleClass
    Public Shared SampleString As String = "Sample String"
End Class
```

 <span data-ttu-id="b8690-220">若要访问共享成员，请使用类的名称，但不要创建此类的对象：</span><span class="sxs-lookup"><span data-stu-id="b8690-220">To access the shared member, use the name of the class without creating an object of this class:</span></span>

```vb
MsgBox(SampleClass.SampleString)
```

 <span data-ttu-id="b8690-221">Visual Basic 中的共享模块仅具有共享成员，因此不能进行实例化。</span><span class="sxs-lookup"><span data-stu-id="b8690-221">Shared modules in Visual Basic have shared members only and cannot be instantiated.</span></span> <span data-ttu-id="b8690-222">共享成员还无法访问非共享属性、字段或方法</span><span class="sxs-lookup"><span data-stu-id="b8690-222">Shared members also cannot access non-shared properties, fields or methods</span></span>

 <span data-ttu-id="b8690-223">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-223">For more information, see:</span></span>

- [<span data-ttu-id="b8690-224">共享</span><span class="sxs-lookup"><span data-stu-id="b8690-224">Shared</span></span>](../../language-reference/modifiers/shared.md)
- [<span data-ttu-id="b8690-225">Module 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-225">Module Statement</span></span>](../../language-reference/statements/module-statement.md)

### <a name="anonymous-types"></a><span data-ttu-id="b8690-226">匿名类型</span><span class="sxs-lookup"><span data-stu-id="b8690-226">Anonymous types</span></span>

<span data-ttu-id="b8690-227">匿名类型使你无需为数据类型编写类定义即可创建对象。</span><span class="sxs-lookup"><span data-stu-id="b8690-227">Anonymous types enable you to create objects without writing a class definition for the data type.</span></span> <span data-ttu-id="b8690-228">此时，编译器将为你生成类。</span><span class="sxs-lookup"><span data-stu-id="b8690-228">Instead, the compiler generates a class for you.</span></span> <span data-ttu-id="b8690-229">该类没有可使用的名称，且包含在声明对象时指定的属性。</span><span class="sxs-lookup"><span data-stu-id="b8690-229">The class has no usable name and contains the properties you specify in declaring the object.</span></span>

<span data-ttu-id="b8690-230">创建匿名类型的实例：</span><span class="sxs-lookup"><span data-stu-id="b8690-230">To create an instance of an anonymous type:</span></span>

```vb
' sampleObject is an instance of a simple anonymous type.
Dim sampleObject =
    New With {Key .FirstProperty = "A", .SecondProperty = "B"}
```

<span data-ttu-id="b8690-231">有关详情，请参阅：[匿名类型](../language-features/objects-and-classes/anonymous-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-231">For more information, see: [Anonymous Types](../language-features/objects-and-classes/anonymous-types.md).</span></span>

## <a name="inheritance"></a><span data-ttu-id="b8690-232">继承</span><span class="sxs-lookup"><span data-stu-id="b8690-232">Inheritance</span></span>

<span data-ttu-id="b8690-233">通过继承，可以创建一个新类，它重用、扩展和修改另一个类中定义的行为。</span><span class="sxs-lookup"><span data-stu-id="b8690-233">Inheritance enables you to create a new class that reuses, extends, and modifies the behavior that is defined in another class.</span></span> <span data-ttu-id="b8690-234">其成员被继承的类称为“基类”，继承这些成员的类称为“派生类”。</span><span class="sxs-lookup"><span data-stu-id="b8690-234">The class whose members are inherited is called the *base class*, and the class that inherits those members is called the *derived class*.</span></span> <span data-ttu-id="b8690-235">但是，Visual Basic 中的所有类都隐式继承自 <xref:System.Object> 类，该类支持 .net 类层次结构，并为所有类提供低级别服务。</span><span class="sxs-lookup"><span data-stu-id="b8690-235">However, all classes in Visual Basic implicitly inherit from the <xref:System.Object> class that supports .NET class hierarchy and provides low-level services to all classes.</span></span>

> [!NOTE]
> <span data-ttu-id="b8690-236">Visual Basic 不支持多重继承。</span><span class="sxs-lookup"><span data-stu-id="b8690-236">Visual Basic doesn't support multiple inheritance.</span></span> <span data-ttu-id="b8690-237">即，只能为一个派生类指定一个基类。</span><span class="sxs-lookup"><span data-stu-id="b8690-237">That is, you can specify only one base class for a derived class.</span></span>

<span data-ttu-id="b8690-238">从基类继承：</span><span class="sxs-lookup"><span data-stu-id="b8690-238">To inherit from a base class:</span></span>

```vb
Class DerivedClass
    Inherits BaseClass
End Class
```

<span data-ttu-id="b8690-239">默认情况下，可以继承所有类。</span><span class="sxs-lookup"><span data-stu-id="b8690-239">By default all classes can be inherited.</span></span> <span data-ttu-id="b8690-240">但你可以指定不得将某个类用作基类，也可以创建只能用作基类的类。</span><span class="sxs-lookup"><span data-stu-id="b8690-240">However, you can specify whether a class must not be used as a base class, or create a class that can be used as a base class only.</span></span>

<span data-ttu-id="b8690-241">指定不得将某个类用作基类：</span><span class="sxs-lookup"><span data-stu-id="b8690-241">To specify that a class cannot be used as a base class:</span></span>

```vb
NotInheritable Class SampleClass
End Class
```

<span data-ttu-id="b8690-242">指定只能用作基类且无法实例化的类：</span><span class="sxs-lookup"><span data-stu-id="b8690-242">To specify that a class can be used as a base class only and cannot be instantiated:</span></span>

```vb
MustInherit Class BaseClass
End Class
```

<span data-ttu-id="b8690-243">有关详情，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-243">For more information, see:</span></span>

- [<span data-ttu-id="b8690-244">Inherits Statement</span><span class="sxs-lookup"><span data-stu-id="b8690-244">Inherits Statement</span></span>](../../language-reference/statements/inherits-statement.md)
- [<span data-ttu-id="b8690-245">NotInheritable</span><span class="sxs-lookup"><span data-stu-id="b8690-245">NotInheritable</span></span>](../../language-reference/modifiers/notinheritable.md)
- [<span data-ttu-id="b8690-246">MustInherit</span><span class="sxs-lookup"><span data-stu-id="b8690-246">MustInherit</span></span>](../../language-reference/modifiers/mustinherit.md)

### <a name="overriding-members"></a><span data-ttu-id="b8690-247">重写成员</span><span class="sxs-lookup"><span data-stu-id="b8690-247">Overriding members</span></span>

<span data-ttu-id="b8690-248">默认情况下，派生类继承其基类的所有成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-248">By default, a derived class inherits all members from its base class.</span></span> <span data-ttu-id="b8690-249">若希望更改继承成员的行为，则需要重写该成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-249">If you want to change the behavior of the inherited member, you need to override it.</span></span> <span data-ttu-id="b8690-250">即，可以在派生类中定义方法、属性或事件的新实现。</span><span class="sxs-lookup"><span data-stu-id="b8690-250">That is, you can define a new implementation of the method, property or event in the derived class.</span></span>

<span data-ttu-id="b8690-251">下列修饰符用于控制如何重写属性和方法：</span><span class="sxs-lookup"><span data-stu-id="b8690-251">The following modifiers are used to control how properties and methods are overridden:</span></span>

|<span data-ttu-id="b8690-252">Visual Basic 修饰符</span><span class="sxs-lookup"><span data-stu-id="b8690-252">Visual Basic Modifier</span></span>|<span data-ttu-id="b8690-253">定义</span><span class="sxs-lookup"><span data-stu-id="b8690-253">Definition</span></span>|
|---------------------------|----------------|
|[<span data-ttu-id="b8690-254">Overrides</span><span class="sxs-lookup"><span data-stu-id="b8690-254">Overridable</span></span>](../../language-reference/modifiers/overridable.md)|<span data-ttu-id="b8690-255">允许在派生类中重写类成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-255">Allows a class member to be overridden in a derived class.</span></span>|
|[<span data-ttu-id="b8690-256">替代</span><span class="sxs-lookup"><span data-stu-id="b8690-256">Overrides</span></span>](../../language-reference/modifiers/overrides.md)|<span data-ttu-id="b8690-257">重写基类中定义的虚拟（可重写）成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-257">Overrides a virtual (overridable) member defined in the base class.</span></span>|
|[<span data-ttu-id="b8690-258">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="b8690-258">NotOverridable</span></span>](../../language-reference/modifiers/notoverridable.md)|<span data-ttu-id="b8690-259">禁止在继承类中重写成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-259">Prevents a member from being overridden in an inheriting class.</span></span>|
|[<span data-ttu-id="b8690-260">New</span><span class="sxs-lookup"><span data-stu-id="b8690-260">MustOverride</span></span>](../../language-reference/modifiers/mustoverride.md)|<span data-ttu-id="b8690-261">要求在派生类中重写类成员。</span><span class="sxs-lookup"><span data-stu-id="b8690-261">Requires that a class member to be overridden in the derived class.</span></span>|
|[<span data-ttu-id="b8690-262">Shadows</span><span class="sxs-lookup"><span data-stu-id="b8690-262">Shadows</span></span>](../../language-reference/modifiers/shadows.md)|<span data-ttu-id="b8690-263">隐藏继承自基类的成员</span><span class="sxs-lookup"><span data-stu-id="b8690-263">Hides a member inherited from a base class</span></span>|

## <a name="interfaces"></a><span data-ttu-id="b8690-264">接口</span><span class="sxs-lookup"><span data-stu-id="b8690-264">Interfaces</span></span>

<span data-ttu-id="b8690-265">和类一样，接口也定义了一系列属性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="b8690-265">Interfaces, like classes, define a set of properties, methods, and events.</span></span> <span data-ttu-id="b8690-266">但与类不同的是，接口并不提供实现。</span><span class="sxs-lookup"><span data-stu-id="b8690-266">But unlike classes, interfaces do not provide implementation.</span></span> <span data-ttu-id="b8690-267">它们由类来实现，并从类中被定义为单独的实体。</span><span class="sxs-lookup"><span data-stu-id="b8690-267">They are implemented by classes, and defined as separate entities from classes.</span></span> <span data-ttu-id="b8690-268">接口表示一种约定，实现接口的类必须严格按其定义来实现接口的每个方面。</span><span class="sxs-lookup"><span data-stu-id="b8690-268">An interface represents a contract, in that a class that implements an interface must implement every aspect of that interface exactly as it is defined.</span></span>

<span data-ttu-id="b8690-269">定义接口：</span><span class="sxs-lookup"><span data-stu-id="b8690-269">To define an interface:</span></span>

```vb
Public Interface ISampleInterface
    Sub DoSomething()
End Interface
```

<span data-ttu-id="b8690-270">在类中实现接口：</span><span class="sxs-lookup"><span data-stu-id="b8690-270">To implement an interface in a class:</span></span>

```vb
Class SampleClass
    Implements ISampleInterface
    Sub DoSomething
        ' Method implementation.
    End Sub
End Class
```

<span data-ttu-id="b8690-271">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-271">For more information, see:</span></span>

- [<span data-ttu-id="b8690-272">接口</span><span class="sxs-lookup"><span data-stu-id="b8690-272">Interfaces</span></span>](../language-features/interfaces/index.md)
- [<span data-ttu-id="b8690-273">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-273">Interface Statement</span></span>](../../language-reference/statements/interface-statement.md)
- [<span data-ttu-id="b8690-274">Implements 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-274">Implements Statement</span></span>](../../language-reference/statements/implements-statement.md)

## <a name="generics"></a><span data-ttu-id="b8690-275">泛型</span><span class="sxs-lookup"><span data-stu-id="b8690-275">Generics</span></span>

<span data-ttu-id="b8690-276">.NET 中的类、结构、接口和方法可以包含定义它们可以存储或使用的对象类型的 *类型参数* 。</span><span class="sxs-lookup"><span data-stu-id="b8690-276">Classes, structures, interfaces and methods in .NET can include *type parameters* that define types of objects that they can store or use.</span></span> <span data-ttu-id="b8690-277">最常见的泛型示例是集合，从中可以指定要存储在集合中的对象的类型。</span><span class="sxs-lookup"><span data-stu-id="b8690-277">The most common example of generics is a collection, where you can specify the type of objects to be stored in a collection.</span></span>

<span data-ttu-id="b8690-278">定义泛型类：</span><span class="sxs-lookup"><span data-stu-id="b8690-278">To define a generic class:</span></span>

```vb
Class SampleGeneric(Of T)
    Public Field As T
End Class
```

<span data-ttu-id="b8690-279">创建泛型类的实例：</span><span class="sxs-lookup"><span data-stu-id="b8690-279">To create an instance of a generic class:</span></span>

```vb
Dim sampleObject As New SampleGeneric(Of String)
sampleObject.Field = "Sample string"
```

<span data-ttu-id="b8690-280">有关详细信息，请参见:</span><span class="sxs-lookup"><span data-stu-id="b8690-280">For more information, see:</span></span>

- [<span data-ttu-id="b8690-281">泛型</span><span class="sxs-lookup"><span data-stu-id="b8690-281">Generics</span></span>](../../../standard/generics/index.md)
- [<span data-ttu-id="b8690-282">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b8690-282">Generic Types in Visual Basic</span></span>](../language-features/data-types/generic-types.md)

## <a name="delegates"></a><span data-ttu-id="b8690-283">委托</span><span class="sxs-lookup"><span data-stu-id="b8690-283">Delegates</span></span>

 <span data-ttu-id="b8690-284">“委托”是一种类型，它定义方法签名，可以提供对具有兼容签名的任何方法的引用。</span><span class="sxs-lookup"><span data-stu-id="b8690-284">A *delegate* is a type that defines a method signature, and can provide a reference to any method with a compatible signature.</span></span> <span data-ttu-id="b8690-285">你可以通过委托调用方法。</span><span class="sxs-lookup"><span data-stu-id="b8690-285">You can invoke (or call) the method through the delegate.</span></span> <span data-ttu-id="b8690-286">委托用于将方法作为参数传递给其他方法。</span><span class="sxs-lookup"><span data-stu-id="b8690-286">Delegates are used to pass methods as arguments to other methods.</span></span>

> [!NOTE]
> <span data-ttu-id="b8690-287">事件处理程序就是通过委托调用的方法。</span><span class="sxs-lookup"><span data-stu-id="b8690-287">Event handlers are nothing more than methods that are invoked through delegates.</span></span> <span data-ttu-id="b8690-288">有关在事件处理中使用委托的详细信息，请参阅[事件](../../../standard/events/index.md)。</span><span class="sxs-lookup"><span data-stu-id="b8690-288">For more information about using delegates in event handling, see [Events](../../../standard/events/index.md).</span></span>

<span data-ttu-id="b8690-289">创建委托：</span><span class="sxs-lookup"><span data-stu-id="b8690-289">To create a delegate:</span></span>

```vb
Delegate Sub SampleDelegate(ByVal str As String)
```

<span data-ttu-id="b8690-290">创建对与委托指定的签名相匹配的方法的引用：</span><span class="sxs-lookup"><span data-stu-id="b8690-290">To create a reference to a method that matches the signature specified by the delegate:</span></span>

```vb
Class SampleClass
    ' Method that matches the SampleDelegate signature.
    Sub SampleSub(ByVal str As String)
        ' Add code here.
    End Sub
    ' Method that instantiates the delegate.
    Sub SampleDelegateSub()
        Dim sd As SampleDelegate = AddressOf SampleSub
        sd("Sample string")
    End Sub
End Class
```

<span data-ttu-id="b8690-291">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b8690-291">For more information, see:</span></span>

- [<span data-ttu-id="b8690-292">委托</span><span class="sxs-lookup"><span data-stu-id="b8690-292">Delegates</span></span>](../language-features/delegates/index.md)
- [<span data-ttu-id="b8690-293">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="b8690-293">Delegate Statement</span></span>](../../language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="b8690-294">AddressOf 运算符</span><span class="sxs-lookup"><span data-stu-id="b8690-294">AddressOf Operator</span></span>](../../language-reference/operators/addressof-operator.md)

## <a name="see-also"></a><span data-ttu-id="b8690-295">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8690-295">See also</span></span>

- [<span data-ttu-id="b8690-296">Visual Basic 编程指南</span><span class="sxs-lookup"><span data-stu-id="b8690-296">Visual Basic Programming Guide</span></span>](../index.md)
