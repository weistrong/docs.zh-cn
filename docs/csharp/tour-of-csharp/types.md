---
title: 定义类型及其成员 - C# 教程
description: 程序的构建基块是类型。 了解如何使用 C# 创建类、结构、接口等。
ms.date: 08/06/2020
ms.openlocfilehash: b1ce24611fec6fdf01d5ecb8d6ae974e147c78c5
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99216598"
---
# <a name="types-and-members"></a><span data-ttu-id="7dde7-104">类型和成员</span><span class="sxs-lookup"><span data-stu-id="7dde7-104">Types and members</span></span>

<span data-ttu-id="7dde7-105">作为面向对象的语言，C# 支持封装、继承和多态性这些概念。</span><span class="sxs-lookup"><span data-stu-id="7dde7-105">As an object-oriented language, C# supports the concepts of encapsulation, inheritance, and polymorphism.</span></span> <span data-ttu-id="7dde7-106">类可能会直接继承一个父类，并且可以实现任意数量的接口。</span><span class="sxs-lookup"><span data-stu-id="7dde7-106">A class may inherit directly from one parent class, and it may implement any number of interfaces.</span></span> <span data-ttu-id="7dde7-107">若要用方法重写父类中的虚方法，必须使用 `override` 关键字，以免发生意外重定义。</span><span class="sxs-lookup"><span data-stu-id="7dde7-107">Methods that override virtual methods in a parent class require the `override` keyword as a way to avoid accidental redefinition.</span></span> <span data-ttu-id="7dde7-108">在 C# 中，结构就像是轻量级类，是可以实现接口但不支持继承的堆栈分配类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-108">In C#, a struct is like a lightweight class; it's a stack-allocated type that can implement interfaces but doesn't support inheritance.</span></span> <span data-ttu-id="7dde7-109">C# 还可提供记录，这些记录是主要用于存储数据值的类类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-109">C# also provides records, which are class types whose purpose is primarily storing data values.</span></span>

## <a name="classes-and-objects"></a><span data-ttu-id="7dde7-110">类和对象</span><span class="sxs-lookup"><span data-stu-id="7dde7-110">Classes and objects</span></span>

<span data-ttu-id="7dde7-111">*类* 是最基本的 C# 类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-111">*Classes* are the most fundamental of C#’s types.</span></span> <span data-ttu-id="7dde7-112">类是一种数据结构，可在一个单元中就将状态（字段）和操作（方法和其他函数成员）结合起来。</span><span class="sxs-lookup"><span data-stu-id="7dde7-112">A class is a data structure that combines state (fields) and actions (methods and other function members) in a single unit.</span></span> <span data-ttu-id="7dde7-113">类为类实例（亦称为“对象”）提供了定义 。</span><span class="sxs-lookup"><span data-stu-id="7dde7-113">A class provides a definition for *instances* of the class, also known as *objects*.</span></span> <span data-ttu-id="7dde7-114">类支持 *继承* 和 *多形性*，即 *派生类* 可以扩展和专门针对 *基类* 的机制。</span><span class="sxs-lookup"><span data-stu-id="7dde7-114">Classes support *inheritance* and *polymorphism*, mechanisms whereby *derived classes* can extend and specialize *base classes*.</span></span>

<span data-ttu-id="7dde7-115">新类使用类声明进行创建。</span><span class="sxs-lookup"><span data-stu-id="7dde7-115">New classes are created using class declarations.</span></span> <span data-ttu-id="7dde7-116">类声明以标头开头。</span><span class="sxs-lookup"><span data-stu-id="7dde7-116">A class declaration starts with a header.</span></span> <span data-ttu-id="7dde7-117">标头指定以下内容：</span><span class="sxs-lookup"><span data-stu-id="7dde7-117">The header specifies:</span></span>

- <span data-ttu-id="7dde7-118">类的特性和修饰符</span><span class="sxs-lookup"><span data-stu-id="7dde7-118">The attributes and modifiers of the class</span></span>
- <span data-ttu-id="7dde7-119">类的名称</span><span class="sxs-lookup"><span data-stu-id="7dde7-119">The name of the class</span></span>
- <span data-ttu-id="7dde7-120">基类（从[基类](#base-classes)继承时）</span><span class="sxs-lookup"><span data-stu-id="7dde7-120">The base class (when inheriting from a [base class](#base-classes))</span></span>
- <span data-ttu-id="7dde7-121">接口由该类实现。</span><span class="sxs-lookup"><span data-stu-id="7dde7-121">The interfaces implemented by the class.</span></span>

<span data-ttu-id="7dde7-122">标头后面是类主体，由在分隔符 `{` 和 `}` 内编写的成员声明列表组成。</span><span class="sxs-lookup"><span data-stu-id="7dde7-122">The header is followed by the class body, which consists of a list of member declarations written between the delimiters `{` and `}`.</span></span>

<span data-ttu-id="7dde7-123">以下代码展示的是简单类 `Point` 的声明：</span><span class="sxs-lookup"><span data-stu-id="7dde7-123">The following code shows a declaration of a simple class named `Point`:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="PointClass":::

<span data-ttu-id="7dde7-124">类实例是使用 `new` 运算符进行创建，此运算符为新实例分配内存，调用构造函数来初始化实例，并返回对实例的引用。</span><span class="sxs-lookup"><span data-stu-id="7dde7-124">Instances of classes are created using the `new` operator, which allocates memory for a new instance, invokes a constructor to initialize the instance, and returns a reference to the instance.</span></span> <span data-ttu-id="7dde7-125">以下语句创建两个 `Point` 对象，并将对这些对象的引用存储在两个变量中：</span><span class="sxs-lookup"><span data-stu-id="7dde7-125">The following statements create two `Point` objects and store references to those objects in two variables:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="CreatePoints":::

<span data-ttu-id="7dde7-126">当无法再访问对象时，对象占用的内存会被自动回收。</span><span class="sxs-lookup"><span data-stu-id="7dde7-126">The memory occupied by an object is automatically reclaimed when the object is no longer reachable.</span></span> <span data-ttu-id="7dde7-127">没有必要也无法在 C# 中显式解除分配对象。</span><span class="sxs-lookup"><span data-stu-id="7dde7-127">It's not necessary or possible to explicitly deallocate objects in C#.</span></span>

### <a name="type-parameters"></a><span data-ttu-id="7dde7-128">类型参数</span><span class="sxs-lookup"><span data-stu-id="7dde7-128">Type parameters</span></span>

<span data-ttu-id="7dde7-129">泛型类定义[类型参数](../programming-guide/generics/index.md)\*。</span><span class="sxs-lookup"><span data-stu-id="7dde7-129">Generic classes define [\***type parameters** _](../programming-guide/generics/index.md).</span></span> <span data-ttu-id="7dde7-130">类型参数是用尖括号括起来的类型参数名称列表。</span><span class="sxs-lookup"><span data-stu-id="7dde7-130">Type parameters are a list of type parameter names enclosed in angle brackets.</span></span> <span data-ttu-id="7dde7-131">类型参数跟在类名后面。</span><span class="sxs-lookup"><span data-stu-id="7dde7-131">Type parameters follow the class name.</span></span> <span data-ttu-id="7dde7-132">然后，可以在类声明的主体中使用类型参数来定义类成员。</span><span class="sxs-lookup"><span data-stu-id="7dde7-132">The type parameters can then be used in the body of the class declarations to define the members of the class.</span></span> <span data-ttu-id="7dde7-133">在以下示例中，`Pair` 的类型参数是 `TFirst` 和 `TSecond`：</span><span class="sxs-lookup"><span data-stu-id="7dde7-133">In the following example, the type parameters of `Pair` are `TFirst` and `TSecond`:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="DefinePairClass":::

<span data-ttu-id="7dde7-134">声明为需要使用类型参数的类类型被称为“泛型类类型”。</span><span class="sxs-lookup"><span data-stu-id="7dde7-134">A class type that is declared to take type parameters is called a _generic class type\*.</span></span> <span data-ttu-id="7dde7-135">结构、接口和委托类型也可以是泛型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-135">Struct, interface, and delegate types can also be generic.</span></span>
<span data-ttu-id="7dde7-136">使用泛型类时，必须为每个类型参数提供类型自变量：</span><span class="sxs-lookup"><span data-stu-id="7dde7-136">When the generic class is used, type arguments must be provided for each of the type parameters:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="CreatePairObject":::

<span data-ttu-id="7dde7-137">包含类型自变量的泛型类型（如上面的 `Pair<int,string>`）被称为 *构造泛型类型*。</span><span class="sxs-lookup"><span data-stu-id="7dde7-137">A generic type with type arguments provided, like `Pair<int,string>` above, is called a *constructed type*.</span></span>

### <a name="base-classes"></a><span data-ttu-id="7dde7-138">基类</span><span class="sxs-lookup"><span data-stu-id="7dde7-138">Base classes</span></span>

<span data-ttu-id="7dde7-139">类声明可以指定基类。</span><span class="sxs-lookup"><span data-stu-id="7dde7-139">A class declaration may specify a base class.</span></span> <span data-ttu-id="7dde7-140">在类名和类型参数后面加上冒号和基类的名称。</span><span class="sxs-lookup"><span data-stu-id="7dde7-140">Follow the class name and type parameters with a colon and the name of the base class.</span></span> <span data-ttu-id="7dde7-141">省略基类规范与从 `object` 类型派生相同。</span><span class="sxs-lookup"><span data-stu-id="7dde7-141">Omitting a base class specification is the same as deriving from type `object`.</span></span> <span data-ttu-id="7dde7-142">在以下示例中，`Point3D` 的基类是 `Point`</span><span class="sxs-lookup"><span data-stu-id="7dde7-142">In the following example, the base class of `Point3D` is `Point`.</span></span> <span data-ttu-id="7dde7-143">在第一个示例中，`Point` 的基类是 `object`：</span><span class="sxs-lookup"><span data-stu-id="7dde7-143">From the first example, the base class of `Point` is `object`:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="Create3DPoint":::

<span data-ttu-id="7dde7-144">类继承其基类的成员。</span><span class="sxs-lookup"><span data-stu-id="7dde7-144">A class inherits the members of its base class.</span></span> <span data-ttu-id="7dde7-145">继承意味着一个类隐式包含其基类的几乎所有成员。</span><span class="sxs-lookup"><span data-stu-id="7dde7-145">Inheritance means that a class implicitly contains almost all members of its base class.</span></span> <span data-ttu-id="7dde7-146">类不继承实例、静态构造函数以及终结器。</span><span class="sxs-lookup"><span data-stu-id="7dde7-146">A class doesn't inherit the instance and static constructors, and the finalizer.</span></span> <span data-ttu-id="7dde7-147">派生类可以在其继承的成员中添加新成员，但无法删除继承成员的定义。</span><span class="sxs-lookup"><span data-stu-id="7dde7-147">A derived class can add new members to those members it inherits, but it can't remove the definition of an inherited member.</span></span> <span data-ttu-id="7dde7-148">在上面的示例中，`Point3D` 从 `Point` 继承了 `X` 和 `Y` 成员，每个 `Point3D` 实例均包含三种属性（`X`、`Y` 和 `Z`）。</span><span class="sxs-lookup"><span data-stu-id="7dde7-148">In the previous example, `Point3D` inherits the `X` and `Y` members from `Point`, and every `Point3D` instance contains three properties, `X`, `Y`, and `Z`.</span></span>

<span data-ttu-id="7dde7-149">可以将类类型隐式转换成其任意基类类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-149">An implicit conversion exists from a class type to any of its base class types.</span></span> <span data-ttu-id="7dde7-150">类类型的变量可以引用相应类的实例或任意派生类的实例。</span><span class="sxs-lookup"><span data-stu-id="7dde7-150">A variable of a class type can reference an instance of that class or an instance of any derived class.</span></span> <span data-ttu-id="7dde7-151">例如，类声明如上，`Point` 类型的变量可以引用 `Point` 或 `Point3D`：</span><span class="sxs-lookup"><span data-stu-id="7dde7-151">For example, given the previous class declarations, a variable of type `Point` can reference either a `Point` or a `Point3D`:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="ImplicitCastToBase":::

## <a name="structs"></a><span data-ttu-id="7dde7-152">结构</span><span class="sxs-lookup"><span data-stu-id="7dde7-152">Structs</span></span>

<span data-ttu-id="7dde7-153">类定义可支持继承和多形性的类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-153">Classes define types that support inheritance and polymorphism.</span></span> <span data-ttu-id="7dde7-154">它们使你能够基于派生类的层次结构创建复杂的行为。</span><span class="sxs-lookup"><span data-stu-id="7dde7-154">They enable you to create sophisticated behaviors based on hierarchies of derived classes.</span></span> <span data-ttu-id="7dde7-155">相比之下，[结构](../language-reference/builtin-types/struct.md)类型是较为简单的类型，其主要目的是存储数据值\*。</span><span class="sxs-lookup"><span data-stu-id="7dde7-155">By contrast, [\***struct** _](../language-reference/builtin-types/struct.md) types are simpler types whose primary purpose is to store data values.</span></span> <span data-ttu-id="7dde7-156">结构不能声明基类型；它们从 <xref:System.ValueType?displayProperty=nameWithType> 隐式派生。</span><span class="sxs-lookup"><span data-stu-id="7dde7-156">Structs can't declare a base type; they implicitly derive from <xref:System.ValueType?displayProperty=nameWithType>.</span></span> <span data-ttu-id="7dde7-157">不能从 `struct` 类型派生其他 `struct` 类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-157">You can't derive other `struct` types from a `struct` type.</span></span> <span data-ttu-id="7dde7-158">这些类型已隐式密封。</span><span class="sxs-lookup"><span data-stu-id="7dde7-158">They're implicitly sealed.</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="PointStruct":::

## <a name="interfaces"></a><span data-ttu-id="7dde7-159">接口</span><span class="sxs-lookup"><span data-stu-id="7dde7-159">Interfaces</span></span>

<span data-ttu-id="7dde7-160">[接口](../programming-guide/interfaces/index.md)定义了可由类和结构实现的协定。</span><span class="sxs-lookup"><span data-stu-id="7dde7-160">An [_*_interface_*_](../programming-guide/interfaces/index.md) defines a contract that can be implemented by classes and structs.</span></span> <span data-ttu-id="7dde7-161">接口可以包含方法、属性、事件和索引器。</span><span class="sxs-lookup"><span data-stu-id="7dde7-161">An interface can contain methods, properties, events, and indexers.</span></span> <span data-ttu-id="7dde7-162">接口通常不提供所定义成员的实现，仅指定必须由实现接口的类或结构提供的成员。</span><span class="sxs-lookup"><span data-stu-id="7dde7-162">An interface typically doesn't provide implementations of the members it defines—it merely specifies the members that must be supplied by classes or structs that implement the interface.</span></span>

<span data-ttu-id="7dde7-163">接口可以采用“多重继承”。</span><span class="sxs-lookup"><span data-stu-id="7dde7-163">Interfaces may employ _*_multiple inheritance_*_.</span></span> <span data-ttu-id="7dde7-164">在以下示例中，接口 `IComboBox` 同时继承自 `ITextBox` 和 `IListBox`。</span><span class="sxs-lookup"><span data-stu-id="7dde7-164">In the following example, the interface `IComboBox` inherits from both `ITextBox` and `IListBox`.</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="FirstInterfaces":::

<span data-ttu-id="7dde7-165">类和结构可以实现多个接口。</span><span class="sxs-lookup"><span data-stu-id="7dde7-165">Classes and structs can implement multiple interfaces.</span></span> <span data-ttu-id="7dde7-166">在以下示例中，类 `EditBox` 同时实现 `IControl` 和 `IDataBound`。</span><span class="sxs-lookup"><span data-stu-id="7dde7-166">In the following example, the class `EditBox` implements both `IControl` and `IDataBound`.</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="ImplementInterfaces":::

<span data-ttu-id="7dde7-167">当类或结构实现特定接口时，此类或结构的实例可以隐式转换成相应的接口类型。</span><span class="sxs-lookup"><span data-stu-id="7dde7-167">When a class or struct implements a particular interface, instances of that class or struct can be implicitly converted to that interface type.</span></span> <span data-ttu-id="7dde7-168">例如</span><span class="sxs-lookup"><span data-stu-id="7dde7-168">For example</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="UseInterfaces":::

## <a name="enums"></a><span data-ttu-id="7dde7-169">枚举</span><span class="sxs-lookup"><span data-stu-id="7dde7-169">Enums</span></span>

<span data-ttu-id="7dde7-170">[枚举](../language-reference/builtin-types/enum.md)类型定义了一组常数值。</span><span class="sxs-lookup"><span data-stu-id="7dde7-170">An [_*_Enum_*_](../language-reference/builtin-types/enum.md) type defines a set of constant values.</span></span> <span data-ttu-id="7dde7-171">以下 `enum` 声明了定义不同根蔬菜的常数：</span><span class="sxs-lookup"><span data-stu-id="7dde7-171">The following `enum` declares constants that define different root vegetables:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="EnumDeclaration":::

<span data-ttu-id="7dde7-172">还可以定义一个 `enum` 作为标志组合使用。</span><span class="sxs-lookup"><span data-stu-id="7dde7-172">You can also define an `enum` to be used in combination as flags.</span></span> <span data-ttu-id="7dde7-173">以下声明为四季声明了一组标志。</span><span class="sxs-lookup"><span data-stu-id="7dde7-173">The following declaration declares a set of flags for the four seasons.</span></span> <span data-ttu-id="7dde7-174">可以随意搭配季节组合，包括 `All` 值（包含所有季节）：</span><span class="sxs-lookup"><span data-stu-id="7dde7-174">Any combination of the seasons may be applied, including an `All` value that includes all seasons:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="FlagsEnumDeclaration":::

<span data-ttu-id="7dde7-175">以下示例显示了前面两个枚举的声明：</span><span class="sxs-lookup"><span data-stu-id="7dde7-175">The following example shows declarations of both the preceding enums:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="UsingEnums":::

## <a name="nullable-types"></a><span data-ttu-id="7dde7-176">可为 null 的类型</span><span class="sxs-lookup"><span data-stu-id="7dde7-176">Nullable types</span></span>

<span data-ttu-id="7dde7-177">任何类型的变量都可以声明为“不可为 null”或“可为 null” 。</span><span class="sxs-lookup"><span data-stu-id="7dde7-177">Variables of any type may be declared as _*_non-nullable_*_ or _*_nullable_*_.</span></span> <span data-ttu-id="7dde7-178">可为 null 的变量包含一个额外的 `null` 值，表示没有值。</span><span class="sxs-lookup"><span data-stu-id="7dde7-178">A nullable variable can hold an additional `null` value, indicating no value.</span></span> <span data-ttu-id="7dde7-179">可为 null 的值类型（结构或枚举）由 <xref:System.Nullable%601?displayProperty=nameWithType> 表示。</span><span class="sxs-lookup"><span data-stu-id="7dde7-179">Nullable Value types (structs or enums) are represented by <xref:System.Nullable%601?displayProperty=nameWithType>.</span></span> <span data-ttu-id="7dde7-180">不可为 null 和可为 null 的引用类型都由基础引用类型表示。</span><span class="sxs-lookup"><span data-stu-id="7dde7-180">Non-nullable and Nullable Reference types are both represented by the underlying reference type.</span></span> <span data-ttu-id="7dde7-181">这种区别由编译器和某些库读取的元数据体现。</span><span class="sxs-lookup"><span data-stu-id="7dde7-181">The distinction is represented by metadata read by the compiler and some libraries.</span></span> <span data-ttu-id="7dde7-182">当可为 null 的引用在没有先对照 `null` 检查其值的情况下取消引用时，编译器会发出警告。</span><span class="sxs-lookup"><span data-stu-id="7dde7-182">The compiler provides warnings when nullable references are dereferenced without first checking their value against `null`.</span></span> <span data-ttu-id="7dde7-183">当对不可为 null 的引用分配了可能为 `null` 的值时，编译器也会发出警告。</span><span class="sxs-lookup"><span data-stu-id="7dde7-183">The compiler also provides warnings when non-nullable references are assigned a value that may be `null`.</span></span> <span data-ttu-id="7dde7-184">以下示例声明了“可为 null 的 int”，并将其初始化为 `null`。</span><span class="sxs-lookup"><span data-stu-id="7dde7-184">The following example declares a _*_nullable int_*_, initializing it to `null`.</span></span> <span data-ttu-id="7dde7-185">然后将值设置为 `5`。</span><span class="sxs-lookup"><span data-stu-id="7dde7-185">Then, it sets the value to `5`.</span></span> <span data-ttu-id="7dde7-186">该例通过“可为 null 的字符串”演示了同一概念。</span><span class="sxs-lookup"><span data-stu-id="7dde7-186">It demonstrates the same concept with a _*_nullable string_*_.</span></span> <span data-ttu-id="7dde7-187">有关详细信息，请参阅[可为 null 的值类型](../language-reference/builtin-types/nullable-value-types.md)和[可为 null 的引用类型](../nullable-references.md)。</span><span class="sxs-lookup"><span data-stu-id="7dde7-187">For more information, see [nullable value types](../language-reference/builtin-types/nullable-value-types.md) and [nullable reference types](../nullable-references.md).</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="DeclareNullable":::

## <a name="tuples"></a><span data-ttu-id="7dde7-188">元组</span><span class="sxs-lookup"><span data-stu-id="7dde7-188">Tuples</span></span>

<span data-ttu-id="7dde7-189">C# 支持[元组](../language-reference/builtin-types/value-tuples.md)，后者提供了简洁的语法来将多个数据元素分组成一个轻型数据结构\*。</span><span class="sxs-lookup"><span data-stu-id="7dde7-189">C# supports [_ *_tuples_*\*](../language-reference/builtin-types/value-tuples.md), which provides concise syntax to group multiple data elements in a lightweight data structure.</span></span> <span data-ttu-id="7dde7-190">通过声明 `(` 和 `)` 之间的成员的类型和名称来实例化元组，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="7dde7-190">You instantiate a tuple by declaring the types and names of the members between `(` and `)`, as shown in the following example:</span></span>

:::code language="csharp" source="./snippets/shared/Types.cs" ID="DeclareTuples":::

<span data-ttu-id="7dde7-191">元组为具有多个成员的数据结构提供了一种替代方法，且无需使用下一篇文章中介绍的构建基块。</span><span class="sxs-lookup"><span data-stu-id="7dde7-191">Tuples provide an alternative for data structure with multiple members, without using the building blocks described in the next article.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="7dde7-192">[上一页](index.md)
>[下一页](program-building-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="7dde7-192">[Previous](index.md)
[Next](program-building-blocks.md)</span></span>
