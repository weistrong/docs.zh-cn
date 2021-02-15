---
description: 了解更多：值类型和引用类型
title: Value Types and Reference Types
ms.date: 07/20/2015
helpviewer_keywords:
- reference data types [Visual Basic]
- reference types [Visual Basic]
- value types [Visual Basic]
- value data types [Visual Basic]
- types [Visual Basic]
- data types [Visual Basic], value types
- data types [Visual Basic], reference types
ms.assetid: fc82ce15-5a40-4c5c-a1e1-a556830e7391
ms.openlocfilehash: 22cce68260955545e810f6fefe645b5ad6a37ca5
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100462134"
---
# <a name="value-types-and-reference-types"></a><span data-ttu-id="acd15-103">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="acd15-103">Value Types and Reference Types</span></span>

<span data-ttu-id="acd15-104">Visual Basic 中有两种类型：引用类型和值类型。</span><span class="sxs-lookup"><span data-stu-id="acd15-104">There are two kinds of types in Visual Basic: reference types and value types.</span></span> <span data-ttu-id="acd15-105">引用类型的变量存储对其数据（对象）的引用，而值类型的变量直接包含其数据。</span><span class="sxs-lookup"><span data-stu-id="acd15-105">Variables of reference types store references to their data (objects), while variables of value types directly contain their data.</span></span> <span data-ttu-id="acd15-106">对于引用类型，两种变量可引用同一对象；因此，对一个变量执行的操作会影响另一个变量所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="acd15-106">With reference types, two variables can reference the same object; therefore, operations on one variable can affect the object referenced by the other variable.</span></span> <span data-ttu-id="acd15-107">对于值类型，每个变量都有自己的数据副本，对一个变量执行的操作不可能影响另一个 (但对于参数) 的 [ByRef 修饰符](../../../language-reference/modifiers/byref.md) 除外。</span><span class="sxs-lookup"><span data-stu-id="acd15-107">With value types, each variable has its own copy of the data, and it is not possible for operations on one variable to affect the other (except in the case of the [ByRef modifier on parameters](../../../language-reference/modifiers/byref.md)).</span></span>
  
## <a name="value-types"></a><span data-ttu-id="acd15-108">值类型</span><span class="sxs-lookup"><span data-stu-id="acd15-108">Value Types</span></span>  

 <span data-ttu-id="acd15-109">如果数据类型在其自身的内存分配中包含数据，则该数据类型为 *值类型* 。</span><span class="sxs-lookup"><span data-stu-id="acd15-109">A data type is a *value type* if it holds the data within its own memory allocation.</span></span> <span data-ttu-id="acd15-110">值类型包括：</span><span class="sxs-lookup"><span data-stu-id="acd15-110">Value types include the following:</span></span>  
  
- <span data-ttu-id="acd15-111">所有数值数据类型</span><span class="sxs-lookup"><span data-stu-id="acd15-111">All numeric data types</span></span>  
  
- <span data-ttu-id="acd15-112">`Boolean`、`Char` 和 `Date`</span><span class="sxs-lookup"><span data-stu-id="acd15-112">`Boolean`, `Char`, and `Date`</span></span>  
  
- <span data-ttu-id="acd15-113">所有结构（即使它们的成员是引用类型）</span><span class="sxs-lookup"><span data-stu-id="acd15-113">All structures, even if their members are reference types</span></span>  
  
- <span data-ttu-id="acd15-114">枚举，因为它们的基础类型始终为、、、 `SByte` `Short` `Integer` `Long` 、 `Byte` 、、 `UShort` `UInteger` 或 `ULong`</span><span class="sxs-lookup"><span data-stu-id="acd15-114">Enumerations, since their underlying type is always `SByte`, `Short`, `Integer`, `Long`, `Byte`, `UShort`, `UInteger`, or `ULong`</span></span>  
  
 <span data-ttu-id="acd15-115">每个结构都是值类型，即使它包含引用类型成员。</span><span class="sxs-lookup"><span data-stu-id="acd15-115">Every structure is a value type, even if it contains reference type members.</span></span> <span data-ttu-id="acd15-116">出于此原因，值类型（如 `Char` 和） `Integer` 是由 .NET Framework 结构实现的。</span><span class="sxs-lookup"><span data-stu-id="acd15-116">For this reason, value types such as `Char` and `Integer` are implemented by .NET Framework structures.</span></span>  
  
 <span data-ttu-id="acd15-117">您可以使用保留的关键字（例如）声明值类型 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="acd15-117">You can declare a value type by using the reserved keyword, for example, `Decimal`.</span></span> <span data-ttu-id="acd15-118">还可以使用 `New` 关键字初始化值类型。</span><span class="sxs-lookup"><span data-stu-id="acd15-118">You can also use the `New` keyword to initialize a value type.</span></span> <span data-ttu-id="acd15-119">如果类型具有采用参数的构造函数，则此方法特别有用。</span><span class="sxs-lookup"><span data-stu-id="acd15-119">This is especially useful if the type has a constructor that takes parameters.</span></span> <span data-ttu-id="acd15-120">这是构造函数的一个示例 <xref:System.Decimal.%23ctor%28System.Int32%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%2CSystem.Byte%29> ，它 `Decimal` 从提供的部分生成一个新值。</span><span class="sxs-lookup"><span data-stu-id="acd15-120">An example of this is the <xref:System.Decimal.%23ctor%28System.Int32%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%2CSystem.Byte%29> constructor, which builds a new `Decimal` value from the supplied parts.</span></span>  
  
## <a name="reference-types"></a><span data-ttu-id="acd15-121">引用类型</span><span class="sxs-lookup"><span data-stu-id="acd15-121">Reference Types</span></span>  

 <span data-ttu-id="acd15-122">*引用类型* 存储对其数据的引用。</span><span class="sxs-lookup"><span data-stu-id="acd15-122">A *reference type* stores a reference to its data.</span></span> <span data-ttu-id="acd15-123">引用类型包括：</span><span class="sxs-lookup"><span data-stu-id="acd15-123">Reference types include the following:</span></span>  
  
- `String`  
  
- <span data-ttu-id="acd15-124">所有数组（即使它们的元素为值类型）</span><span class="sxs-lookup"><span data-stu-id="acd15-124">All arrays, even if their elements are value types</span></span>  
  
- <span data-ttu-id="acd15-125">类类型，如 <xref:System.Windows.Forms.Form></span><span class="sxs-lookup"><span data-stu-id="acd15-125">Class types, such as <xref:System.Windows.Forms.Form></span></span>  
  
- <span data-ttu-id="acd15-126">委托</span><span class="sxs-lookup"><span data-stu-id="acd15-126">Delegates</span></span>  
  
 <span data-ttu-id="acd15-127">类是 *引用类型*。</span><span class="sxs-lookup"><span data-stu-id="acd15-127">A class is a *reference type*.</span></span> <span data-ttu-id="acd15-128">请注意，每个数组都是引用类型，即使其成员是值类型也是如此。</span><span class="sxs-lookup"><span data-stu-id="acd15-128">Note that every array is a reference type, even if its members are value types.</span></span>  
  
 <span data-ttu-id="acd15-129">由于每个引用类型都表示一个基础 .NET Framework 类，因此必须在初始化时使用 [New 运算符](../../../language-reference/operators/new-operator.md) 关键字。</span><span class="sxs-lookup"><span data-stu-id="acd15-129">Since every reference type represents an underlying .NET Framework class, you must use the [New Operator](../../../language-reference/operators/new-operator.md) keyword when you initialize it.</span></span> <span data-ttu-id="acd15-130">下面的语句初始化一个数组。</span><span class="sxs-lookup"><span data-stu-id="acd15-130">The following statement initializes an array.</span></span>  
  
```vb  
Dim totals() As Single = New Single(8) {}  
```  
  
## <a name="elements-that-are-not-types"></a><span data-ttu-id="acd15-131">不是类型的元素</span><span class="sxs-lookup"><span data-stu-id="acd15-131">Elements That Are Not Types</span></span>  

 <span data-ttu-id="acd15-132">下面的编程元素不限定为类型，因为您不能将任何这些元素指定为已声明元素的数据类型：</span><span class="sxs-lookup"><span data-stu-id="acd15-132">The following programming elements do not qualify as types, because you cannot specify any of them as a data type for a declared element:</span></span>  
  
- <span data-ttu-id="acd15-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="acd15-133">Namespaces</span></span>  
  
- <span data-ttu-id="acd15-134">模块</span><span class="sxs-lookup"><span data-stu-id="acd15-134">Modules</span></span>  
  
- <span data-ttu-id="acd15-135">事件</span><span class="sxs-lookup"><span data-stu-id="acd15-135">Events</span></span>  
  
- <span data-ttu-id="acd15-136">属性和过程</span><span class="sxs-lookup"><span data-stu-id="acd15-136">Properties and procedures</span></span>  
  
- <span data-ttu-id="acd15-137">变量、常量和字段</span><span class="sxs-lookup"><span data-stu-id="acd15-137">Variables, constants, and fields</span></span>  
  
## <a name="working-with-the-object-data-type"></a><span data-ttu-id="acd15-138">使用 Object 数据类型</span><span class="sxs-lookup"><span data-stu-id="acd15-138">Working with the Object Data Type</span></span>  

 <span data-ttu-id="acd15-139">可以将引用类型或值类型分配给 `Object` 数据类型的变量。</span><span class="sxs-lookup"><span data-stu-id="acd15-139">You can assign either a reference type or a value type to a variable of the `Object` data type.</span></span> <span data-ttu-id="acd15-140">`Object`变量始终保存对数据的引用，而不是数据本身。</span><span class="sxs-lookup"><span data-stu-id="acd15-140">An `Object` variable always holds a reference to the data, never the data itself.</span></span> <span data-ttu-id="acd15-141">但是，如果将值类型分配给 `Object` 变量，则其行为就像它包含自己的数据一样。</span><span class="sxs-lookup"><span data-stu-id="acd15-141">However, if you assign a value type to an `Object` variable, it behaves as if it holds its own data.</span></span> <span data-ttu-id="acd15-142">有关详细信息，请参阅 [Object Data Type](../../../language-reference/data-types/object-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="acd15-142">For more information, see [Object Data Type](../../../language-reference/data-types/object-data-type.md).</span></span>  
  
 <span data-ttu-id="acd15-143">可以 `Object` 通过将变量传递给 <xref:Microsoft.VisualBasic.Information.IsReference%2A> <xref:Microsoft.VisualBasic.Information> 命名空间类中的方法来确定变量是作为引用类型还是值类型 <xref:Microsoft.VisualBasic?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="acd15-143">You can find out whether an `Object` variable is acting as a reference type or a value type by passing it to the <xref:Microsoft.VisualBasic.Information.IsReference%2A> method in the <xref:Microsoft.VisualBasic.Information> class of the <xref:Microsoft.VisualBasic?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="acd15-144"><xref:Microsoft.VisualBasic.Information.IsReference%2A?displayProperty=nameWithType>`True`如果该变量的内容 `Object` 表示一个引用类型，则返回。</span><span class="sxs-lookup"><span data-stu-id="acd15-144"><xref:Microsoft.VisualBasic.Information.IsReference%2A?displayProperty=nameWithType> returns `True` if the content of the `Object` variable represents a reference type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acd15-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="acd15-145">See also</span></span>

- [<span data-ttu-id="acd15-146">可以为 null 的值类型</span><span class="sxs-lookup"><span data-stu-id="acd15-146">Nullable Value Types</span></span>](nullable-value-types.md)
- [<span data-ttu-id="acd15-147">Visual Basic 中的类型转换</span><span class="sxs-lookup"><span data-stu-id="acd15-147">Type Conversions in Visual Basic</span></span>](type-conversions.md)
- [<span data-ttu-id="acd15-148">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="acd15-148">Structure Statement</span></span>](../../../language-reference/statements/structure-statement.md)
- [<span data-ttu-id="acd15-149">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="acd15-149">Efficient Use of Data Types</span></span>](efficient-use-of-data-types.md)
- [<span data-ttu-id="acd15-150">Object Data Type</span><span class="sxs-lookup"><span data-stu-id="acd15-150">Object Data Type</span></span>](../../../language-reference/data-types/object-data-type.md)
- [<span data-ttu-id="acd15-151">数据类型</span><span class="sxs-lookup"><span data-stu-id="acd15-151">Data Types</span></span>](index.md)
