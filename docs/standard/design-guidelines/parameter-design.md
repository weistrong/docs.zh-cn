---
description: 详细了解：参数设计
title: 参数设计
ms.date: 10/22/2008
helpviewer_keywords:
- member design guidelines [.NET Framework], parameters
- members [.NET Framework], parameters
- names [.NET Framework], parameters
- parameters, design guidelines
- reserved parameters
ms.assetid: 3f33bf46-4a7b-43b3-bb78-1ffebe0dcfa6
ms.openlocfilehash: 9663ef8146054985374fdb3e2974fcd996fd1402
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731820"
---
# <a name="parameter-design"></a><span data-ttu-id="293e8-103">参数设计</span><span class="sxs-lookup"><span data-stu-id="293e8-103">Parameter Design</span></span>

<span data-ttu-id="293e8-104">本部分就参数设计提供广泛的指导，其中有内容介绍自变量检查指南。</span><span class="sxs-lookup"><span data-stu-id="293e8-104">This section provides broad guidelines on parameter design, including sections with guidelines for checking arguments.</span></span> <span data-ttu-id="293e8-105">此外，你还应查看[命名参数](naming-parameters.md)中描述的指南。</span><span class="sxs-lookup"><span data-stu-id="293e8-105">In addition, you should refer to the guidelines described in [Naming Parameters](naming-parameters.md).</span></span>

 <span data-ttu-id="293e8-106">✔️ 请使用提供成员所需功能的最低派生参数类型。</span><span class="sxs-lookup"><span data-stu-id="293e8-106">✔️ DO use the least derived parameter type that provides the functionality required by the member.</span></span>

 <span data-ttu-id="293e8-107">例如，假设你想要设计这样一种方法，它可枚举集合并将每个项目输出到控制台。</span><span class="sxs-lookup"><span data-stu-id="293e8-107">For example, suppose you want to design a method that enumerates a collection and prints each item to the console.</span></span> <span data-ttu-id="293e8-108">此类方法应将 <xref:System.Collections.IEnumerable> 用作参数，而不是使用 <xref:System.Collections.ArrayList> 或 <xref:System.Collections.IList> 等内容。</span><span class="sxs-lookup"><span data-stu-id="293e8-108">Such a method should take <xref:System.Collections.IEnumerable> as the parameter, not <xref:System.Collections.ArrayList> or <xref:System.Collections.IList>, for example.</span></span>

 <span data-ttu-id="293e8-109">❌ 请勿使用保留的参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-109">❌ DO NOT use reserved parameters.</span></span>

 <span data-ttu-id="293e8-110">如果在某一将来版本中需要对某成员输入更多内容，则可添加新的重载。</span><span class="sxs-lookup"><span data-stu-id="293e8-110">If more input to a member is needed in some future version, a new overload can be added.</span></span>

 <span data-ttu-id="293e8-111">❌ 请勿具有将指针、指针数组或多维数组用作参数的公开方法。</span><span class="sxs-lookup"><span data-stu-id="293e8-111">❌ DO NOT have publicly exposed methods that take pointers, arrays of pointers, or multidimensional arrays as parameters.</span></span>

 <span data-ttu-id="293e8-112">指针和多维数组相对而言很难正确使用。</span><span class="sxs-lookup"><span data-stu-id="293e8-112">Pointers and multidimensional arrays are relatively difficult to use properly.</span></span> <span data-ttu-id="293e8-113">几乎在任何情况下，API 都可重新设计来避免将这些类型用作参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-113">In almost all cases, APIs can be redesigned to avoid taking these types as parameters.</span></span>

 <span data-ttu-id="293e8-114">✔️ 请替换跟在所有按值参数和 `ref` 参数后面的所有 `out` 参数（参数数组除外），即使这会导致重载之间的参数排序不一致也是如此（具体请参见[成员重载](member-overloading.md)）。</span><span class="sxs-lookup"><span data-stu-id="293e8-114">✔️ DO place all `out` parameters following all of the by-value and `ref` parameters (excluding parameter arrays), even if it results in an inconsistency in parameter ordering between overloads (see [Member Overloading](member-overloading.md)).</span></span>

 <span data-ttu-id="293e8-115">`out` 参数可被视为额外的返回值，将它们组合在一起可使方法签名更易于理解。</span><span class="sxs-lookup"><span data-stu-id="293e8-115">The `out` parameters can be seen as extra return values, and grouping them together makes the method signature easier to understand.</span></span>

 <span data-ttu-id="293e8-116">✔️ 在替代成员或实现接口成员时，请在参数命名方面保持一致。</span><span class="sxs-lookup"><span data-stu-id="293e8-116">✔️ DO be consistent in naming parameters when overriding members or implementing interface members.</span></span>

 <span data-ttu-id="293e8-117">这可更好地在方法之间传达关系。</span><span class="sxs-lookup"><span data-stu-id="293e8-117">This better communicates the relationship between the methods.</span></span>

### <a name="choosing-between-enum-and-boolean-parameters"></a><span data-ttu-id="293e8-118">在枚举参数和布尔参数之间选择</span><span class="sxs-lookup"><span data-stu-id="293e8-118">Choosing Between Enum and Boolean Parameters</span></span>  

 <span data-ttu-id="293e8-119">✔️ 如果不使用枚举，成员会具有两个或更多布尔参数，那么请使用枚举型。</span><span class="sxs-lookup"><span data-stu-id="293e8-119">✔️ DO use enums if a member would otherwise have two or more Boolean parameters.</span></span>

 <span data-ttu-id="293e8-120">❌ 请勿使用布尔型，除非你完全确信永远不需要两个以上的值。</span><span class="sxs-lookup"><span data-stu-id="293e8-120">❌ DO NOT use Booleans unless you are absolutely sure there will never be a need for more than two values.</span></span>

 <span data-ttu-id="293e8-121">枚举型让你有空间将来添加值，但你应了解向枚举添加值所带来的全部影响，具体可查看[枚举设计](enum.md)。</span><span class="sxs-lookup"><span data-stu-id="293e8-121">Enums give you some room for future addition of values, but you should be aware of all the implications of adding values to enums, which are described in [Enum Design](enum.md).</span></span>

 <span data-ttu-id="293e8-122">✔️ 请考虑为是真正的双状态值且仅用于初始化布尔属性的构造函数参数使用布尔型。</span><span class="sxs-lookup"><span data-stu-id="293e8-122">✔️ CONSIDER using Booleans for constructor parameters that are truly two-state values and are simply used to initialize Boolean properties.</span></span>

### <a name="validating-arguments"></a><span data-ttu-id="293e8-123">验证自变量</span><span class="sxs-lookup"><span data-stu-id="293e8-123">Validating Arguments</span></span>

 <span data-ttu-id="293e8-124">✔️ 请验证传递到公共、受保护或已显式实现的成员的自变量。</span><span class="sxs-lookup"><span data-stu-id="293e8-124">✔️ DO validate arguments passed to public, protected, or explicitly implemented members.</span></span> <span data-ttu-id="293e8-125">引发 <xref:System.ArgumentException?displayProperty=nameWithType>；如果验证失败，则引发其某个子类。</span><span class="sxs-lookup"><span data-stu-id="293e8-125">Throw <xref:System.ArgumentException?displayProperty=nameWithType>, or one of its subclasses, if the validation fails.</span></span>

 <span data-ttu-id="293e8-126">请注意，并非一定要在公共成员或受保护成员自身进行实际验证。</span><span class="sxs-lookup"><span data-stu-id="293e8-126">Note that the actual validation does not necessarily have to happen in the public or protected member itself.</span></span> <span data-ttu-id="293e8-127">在某些专用或内部例程中，也可在更低级别进行验证。</span><span class="sxs-lookup"><span data-stu-id="293e8-127">It could happen at a lower level in some private or internal routine.</span></span> <span data-ttu-id="293e8-128">要点是被公开给最终用户的整个表面区域都对自变量进行检查。</span><span class="sxs-lookup"><span data-stu-id="293e8-128">The main point is that the entire surface area that is exposed to the end users checks the arguments.</span></span>

 <span data-ttu-id="293e8-129">✔️ 如果传递了 NULL 自变量，而成员不支持 NULL 自变量，则引发 <xref:System.ArgumentNullException>。</span><span class="sxs-lookup"><span data-stu-id="293e8-129">✔️ DO throw <xref:System.ArgumentNullException> if a null argument is passed and the member does not support null arguments.</span></span>

 <span data-ttu-id="293e8-130">✔️ 请验证枚举参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-130">✔️ DO validate enum parameters.</span></span>

 <span data-ttu-id="293e8-131">不要假设将在枚举定义的范围内的枚举自变量。</span><span class="sxs-lookup"><span data-stu-id="293e8-131">Do not assume enum arguments will be in the range defined by the enum.</span></span> <span data-ttu-id="293e8-132">CLR 允许将任何整数值强制转换为枚举值，即使值未在枚举中定义也是如此。</span><span class="sxs-lookup"><span data-stu-id="293e8-132">The CLR allows casting any integer value into an enum value even if the value is not defined in the enum.</span></span>

 <span data-ttu-id="293e8-133">❌ 请勿将 <xref:System.Enum.IsDefined%2A?displayProperty=nameWithType> 用于枚举范围检查。</span><span class="sxs-lookup"><span data-stu-id="293e8-133">❌ DO NOT use <xref:System.Enum.IsDefined%2A?displayProperty=nameWithType> for enum range checks.</span></span>

 <span data-ttu-id="293e8-134">✔️ 请注意可变参数在经过验证后可能会更改。</span><span class="sxs-lookup"><span data-stu-id="293e8-134">✔️ DO be aware that mutable arguments might have changed after they were validated.</span></span>

 <span data-ttu-id="293e8-135">如果成员对安全性很敏感，则请进行复制，然后再验证和处理参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-135">If the member is security sensitive, you are encouraged to make a copy and then validate and process the argument.</span></span>

### <a name="parameter-passing"></a><span data-ttu-id="293e8-136">参数传递</span><span class="sxs-lookup"><span data-stu-id="293e8-136">Parameter Passing</span></span>

 <span data-ttu-id="293e8-137">从框架设计者的角度来看，存在三组主要的参数：按值参数、`ref` 参数和 `out` 参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-137">From the perspective of a framework designer, there are three main groups of parameters: by-value parameters, `ref` parameters, and `out` parameters.</span></span>

 <span data-ttu-id="293e8-138">当自变量通过按值参数传递时，成员会收到传入的实际自变量的副本。</span><span class="sxs-lookup"><span data-stu-id="293e8-138">When an argument is passed through a by-value parameter, the member receives a copy of the actual argument passed in.</span></span> <span data-ttu-id="293e8-139">如果自变量是值类型，则会在堆栈上放置自变量的副本。</span><span class="sxs-lookup"><span data-stu-id="293e8-139">If the argument is a value type, a copy of the argument is put on the stack.</span></span> <span data-ttu-id="293e8-140">如果自变量是引用类型，则会在堆栈上放置引用的副本。</span><span class="sxs-lookup"><span data-stu-id="293e8-140">If the argument is a reference type, a copy of the reference is put on the stack.</span></span> <span data-ttu-id="293e8-141">最常用的 CLR 语言（例如 C#、VB.NET 和 C++）默认为按值传递参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-141">Most popular CLR languages, such as C#, VB.NET, and C++, default to passing parameters by value.</span></span>

 <span data-ttu-id="293e8-142">当自变量通过 `ref` 参数传递时，成员会收到对传入的实际自变量的引用。</span><span class="sxs-lookup"><span data-stu-id="293e8-142">When an argument is passed through a `ref` parameter, the member receives a reference to the actual argument passed in.</span></span> <span data-ttu-id="293e8-143">如果自变量是值类型，则会在堆栈上放置对自变量的引用。</span><span class="sxs-lookup"><span data-stu-id="293e8-143">If the argument is a value type, a reference to the argument is put on the stack.</span></span> <span data-ttu-id="293e8-144">如果自变量是引用类型，则会在堆栈上放置对该引用的引用。</span><span class="sxs-lookup"><span data-stu-id="293e8-144">If the argument is a reference type, a reference to the reference is put on the stack.</span></span> <span data-ttu-id="293e8-145">`Ref` 参数可用于允许成员修改调用方传递的自变量。</span><span class="sxs-lookup"><span data-stu-id="293e8-145">`Ref` parameters can be used to allow the member to modify arguments passed by the caller.</span></span>

 <span data-ttu-id="293e8-146">`Out` 参数与 `ref` 参数类似，但有一些细微的区别。</span><span class="sxs-lookup"><span data-stu-id="293e8-146">`Out` parameters are similar to `ref` parameters, with some small differences.</span></span> <span data-ttu-id="293e8-147">参数最初被视为未分配，在分配了某个值之前无法在成员主体中读取。</span><span class="sxs-lookup"><span data-stu-id="293e8-147">The parameter is initially considered unassigned and cannot be read in the member body before it is assigned some value.</span></span> <span data-ttu-id="293e8-148">此外，在成员返回之前，必须向参数分配某个值。</span><span class="sxs-lookup"><span data-stu-id="293e8-148">Also, the parameter has to be assigned some value before the member returns.</span></span>

 <span data-ttu-id="293e8-149">❌ 不要使用 `out` 和 `ref` 参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-149">❌ AVOID using `out` or `ref` parameters.</span></span>

 <span data-ttu-id="293e8-150">若要使用 `out` 或 `ref` 参数，需要具有使用指针的经验，了解值类型和引用类型的区别，还能处理具有多个返回值的方法。</span><span class="sxs-lookup"><span data-stu-id="293e8-150">Using `out` or `ref` parameters requires experience with pointers, understanding how value types and reference types differ, and handling methods with multiple return values.</span></span> <span data-ttu-id="293e8-151">另外，`out` 和 `ref` 参数之间的区别并未得到广泛了解。</span><span class="sxs-lookup"><span data-stu-id="293e8-151">Also, the difference between `out` and `ref` parameters is not widely understood.</span></span> <span data-ttu-id="293e8-152">针对一般受众进行设计的框架架构师不应指望用户能熟练运用 `out` 或 `ref` 参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-152">Framework architects designing for a general audience should not expect users to master working with `out` or `ref` parameters.</span></span>

 <span data-ttu-id="293e8-153">❌ 请勿按引用来传递引用类型。</span><span class="sxs-lookup"><span data-stu-id="293e8-153">❌ DO NOT pass reference types by reference.</span></span>

 <span data-ttu-id="293e8-154">此规则存在一些有限的例外情况，例如可用于交换引用的方法。</span><span class="sxs-lookup"><span data-stu-id="293e8-154">There are some limited exceptions to the rule, such as a method that can be used to swap references.</span></span>

### <a name="members-with-variable-number-of-parameters"></a><span data-ttu-id="293e8-155">参数数目可变的成员</span><span class="sxs-lookup"><span data-stu-id="293e8-155">Members with Variable Number of Parameters</span></span>

 <span data-ttu-id="293e8-156">可提供一个数组参数来表示采用可变数量的参数的成员。</span><span class="sxs-lookup"><span data-stu-id="293e8-156">Members that can take a variable number of arguments are expressed by providing an array parameter.</span></span> <span data-ttu-id="293e8-157">例如，<xref:System.String> 提供以下方法：</span><span class="sxs-lookup"><span data-stu-id="293e8-157">For example, <xref:System.String> provides the following method:</span></span>

```csharp
public class String {
    public static string Format(string format, object[] parameters);
}
```

 <span data-ttu-id="293e8-158">然后，用户可调用 <xref:System.String.Format%2A?displayProperty=nameWithType> 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="293e8-158">A user can then call the <xref:System.String.Format%2A?displayProperty=nameWithType> method, as follows:</span></span>

 `String.Format("File {0} not found in {1}",new object[]{filename,directory});`

 <span data-ttu-id="293e8-159">如果向数组参数添加 C# params 关键字，会将参数更改为所谓的 params 数组参数，并提供用于创建临时数组的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="293e8-159">Adding the C# params keyword to an array parameter changes the parameter to a so-called params array parameter and provides a shortcut to creating a temporary array.</span></span>

```csharp
public class String {
    public static string Format(string format, params object[] parameters);
}
```

 <span data-ttu-id="293e8-160">这样，用户就可通过直接在自变量列表中传递数组元素来调用方法。</span><span class="sxs-lookup"><span data-stu-id="293e8-160">Doing this allows the user to call the method by passing the array elements directly in the argument list.</span></span>

 `String.Format("File {0} not found in {1}",filename,directory);`

 <span data-ttu-id="293e8-161">请注意，params 这一关键字仅可添加到参数列表中的最后一个参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-161">Note that the params keyword can be added only to the last parameter in the parameter list.</span></span>

 <span data-ttu-id="293e8-162">✔️ 如果预计最终用户会传递具有少量元素的数组，那么请考虑向数组参数添加 params 关键字。</span><span class="sxs-lookup"><span data-stu-id="293e8-162">✔️ CONSIDER adding the params keyword to array parameters if you expect the end users to pass arrays with a small number of elements.</span></span> <span data-ttu-id="293e8-163">如果在常见方案中将传递大量元素，那么用户将可能根本不以内联方式传递这些元素，因此不需要使用 params 关键字。</span><span class="sxs-lookup"><span data-stu-id="293e8-163">If it's expected that lots of elements will be passed in common scenarios, users will probably not pass these elements inline anyway, and so the params keyword is not necessary.</span></span>

 <span data-ttu-id="293e8-164">❌ 如果调用方几乎总是已在数组中具有输入，那么请不要使用 params 数组。</span><span class="sxs-lookup"><span data-stu-id="293e8-164">❌ AVOID using params arrays if the caller would almost always have the input already in an array.</span></span>

 <span data-ttu-id="293e8-165">例如，几乎永远不会通过传递单个字节来调用具有字节数组参数的成员。</span><span class="sxs-lookup"><span data-stu-id="293e8-165">For example, members with byte array parameters would almost never be called by passing individual bytes.</span></span> <span data-ttu-id="293e8-166">因此，.NET Framework 中的字节数组参数不会使用 params 关键字。</span><span class="sxs-lookup"><span data-stu-id="293e8-166">For this reason, byte array parameters in the .NET Framework do not use the params keyword.</span></span>

 <span data-ttu-id="293e8-167">❌ 如果通过采用 params 数组参数的成员修改数组，那么请勿使用 params 数组。</span><span class="sxs-lookup"><span data-stu-id="293e8-167">❌ DO NOT use params arrays if the array is modified by the member taking the params array parameter.</span></span>

 <span data-ttu-id="293e8-168">事实上很多编译器会将成员的自变量转换为调用站点处的临时数组，因此该数组可能是一个临时对象，这使得对该数组的所有修改都将丢失。</span><span class="sxs-lookup"><span data-stu-id="293e8-168">Because of the fact that many compilers turn the arguments to the member into a temporary array at the call site, the array might be a temporary object, and therefore any modifications to the array will be lost.</span></span>

 <span data-ttu-id="293e8-169">✔️ 请考虑在简单重载中使用 params 关键字，即使更复杂的重载不可使用它也是如此。</span><span class="sxs-lookup"><span data-stu-id="293e8-169">✔️ CONSIDER using the params keyword in a simple overload, even if a more complex overload could not use it.</span></span>

 <span data-ttu-id="293e8-170">请自我提问，了解用户即使不在所有重载中使用 params 数组，是否也会在一个重载中使用它。</span><span class="sxs-lookup"><span data-stu-id="293e8-170">Ask yourself if users would value having the params array in one overload even if it wasn't in all overloads.</span></span>

 <span data-ttu-id="293e8-171">✔️ 请尝试对参数排序，以便可使用 params 参数。</span><span class="sxs-lookup"><span data-stu-id="293e8-171">✔️ DO try to order parameters to make it possible to use the params keyword.</span></span>

 <span data-ttu-id="293e8-172">✔️ 在对性能极度敏感的 API 中，请考虑对具有少量自变量的调用提供特定重载和代码路径。</span><span class="sxs-lookup"><span data-stu-id="293e8-172">✔️ CONSIDER providing special overloads and code paths for calls with a small number of arguments in extremely performance-sensitive APIs.</span></span>

 <span data-ttu-id="293e8-173">这样，当使用少量自变量调用 API 时，就能避免创建数组对象。</span><span class="sxs-lookup"><span data-stu-id="293e8-173">This makes it possible to avoid creating array objects when the API is called with a small number of arguments.</span></span> <span data-ttu-id="293e8-174">通过采用单数形式的数组参数并添加数字后缀来创建参数的名称。</span><span class="sxs-lookup"><span data-stu-id="293e8-174">Form the names of the parameters by taking a singular form of the array parameter and adding a numeric suffix.</span></span>

 <span data-ttu-id="293e8-175">仅当要将完整代码路径用作特例时（不仅仅是创建数组和调用更常规的方法），才应这样操作。</span><span class="sxs-lookup"><span data-stu-id="293e8-175">You should only do this if you are going to special-case the entire code path, not just create an array and call the more general method.</span></span>

 <span data-ttu-id="293e8-176">✔️ 请注意 NULL 可作为 params 数组自变量传递。</span><span class="sxs-lookup"><span data-stu-id="293e8-176">✔️ DO be aware that null could be passed as a params array argument.</span></span>

 <span data-ttu-id="293e8-177">在处理之前，应验证数组是否不是 NULL。</span><span class="sxs-lookup"><span data-stu-id="293e8-177">You should validate that the array is not null before processing.</span></span>

 <span data-ttu-id="293e8-178">❌ 请勿使用 `varargs` 方法（也就是省略号）。</span><span class="sxs-lookup"><span data-stu-id="293e8-178">❌ DO NOT use the `varargs` methods, otherwise known as the ellipsis.</span></span>

 <span data-ttu-id="293e8-179">对于传递可变参数列表，某些 CLR 语言（例如 C++）支持替代约定（称为 `varargs` 方法）。</span><span class="sxs-lookup"><span data-stu-id="293e8-179">Some CLR languages, such as C++, support an alternative convention for passing variable parameter lists called `varargs` methods.</span></span> <span data-ttu-id="293e8-180">不得在框架中使用此约定，因为它不符合 CLS。</span><span class="sxs-lookup"><span data-stu-id="293e8-180">The convention should not be used in frameworks, because it is not CLS compliant.</span></span>

### <a name="pointer-parameters"></a><span data-ttu-id="293e8-181">指针参数</span><span class="sxs-lookup"><span data-stu-id="293e8-181">Pointer Parameters</span></span>

 <span data-ttu-id="293e8-182">通常，指针不得出现在设计良好的托管式代码框架的公共表面区域中。</span><span class="sxs-lookup"><span data-stu-id="293e8-182">In general, pointers should not appear in the public surface area of a well-designed managed code framework.</span></span> <span data-ttu-id="293e8-183">大多数情况下，应封装指针。</span><span class="sxs-lookup"><span data-stu-id="293e8-183">Most of the time, pointers should be encapsulated.</span></span> <span data-ttu-id="293e8-184">但在某些情况下，由于可操作性原因需要使用指针，因此在这类情况下使用指针是合适的。</span><span class="sxs-lookup"><span data-stu-id="293e8-184">However, in some cases pointers are required for interoperability reasons, and using pointers in such cases is appropriate.</span></span>

 <span data-ttu-id="293e8-185">✔️ 请对采用指针自变量的所有成员提供替代约定，原因是指针不符合 CLS。</span><span class="sxs-lookup"><span data-stu-id="293e8-185">✔️ DO provide an alternative for any member that takes a pointer argument, because pointers are not CLS-compliant.</span></span>

 <span data-ttu-id="293e8-186">❌ 不要对指针自变量执行自变量检查，此类检查成本高昂。</span><span class="sxs-lookup"><span data-stu-id="293e8-186">❌ AVOID doing expensive argument checking of pointer arguments.</span></span>

 <span data-ttu-id="293e8-187">✔️ 请在使用指针设计成员时遵循与指针相关的常见约定。</span><span class="sxs-lookup"><span data-stu-id="293e8-187">✔️ DO follow common pointer-related conventions when designing members with pointers.</span></span>

 <span data-ttu-id="293e8-188">例如，无需传递开始索引，原因是可使用简单的指针算法实现这一效果。</span><span class="sxs-lookup"><span data-stu-id="293e8-188">For example, there is no need to pass the start index, because simple pointer arithmetic can be used to accomplish the same result.</span></span>

 <span data-ttu-id="293e8-189">*Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="293e8-189">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="293e8-190">*在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines:Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*</span><span class="sxs-lookup"><span data-stu-id="293e8-190">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="293e8-191">请参阅</span><span class="sxs-lookup"><span data-stu-id="293e8-191">See also</span></span>

- [<span data-ttu-id="293e8-192">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="293e8-192">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="293e8-193">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="293e8-193">Framework Design Guidelines</span></span>](index.md)
