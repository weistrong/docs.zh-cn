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
# <a name="parameter-design"></a>参数设计

本部分就参数设计提供广泛的指导，其中有内容介绍自变量检查指南。 此外，你还应查看[命名参数](naming-parameters.md)中描述的指南。

 ✔️ 请使用提供成员所需功能的最低派生参数类型。

 例如，假设你想要设计这样一种方法，它可枚举集合并将每个项目输出到控制台。 此类方法应将 <xref:System.Collections.IEnumerable> 用作参数，而不是使用 <xref:System.Collections.ArrayList> 或 <xref:System.Collections.IList> 等内容。

 ❌ 请勿使用保留的参数。

 如果在某一将来版本中需要对某成员输入更多内容，则可添加新的重载。

 ❌ 请勿具有将指针、指针数组或多维数组用作参数的公开方法。

 指针和多维数组相对而言很难正确使用。 几乎在任何情况下，API 都可重新设计来避免将这些类型用作参数。

 ✔️ 请替换跟在所有按值参数和 `ref` 参数后面的所有 `out` 参数（参数数组除外），即使这会导致重载之间的参数排序不一致也是如此（具体请参见[成员重载](member-overloading.md)）。

 `out` 参数可被视为额外的返回值，将它们组合在一起可使方法签名更易于理解。

 ✔️ 在替代成员或实现接口成员时，请在参数命名方面保持一致。

 这可更好地在方法之间传达关系。

### <a name="choosing-between-enum-and-boolean-parameters"></a>在枚举参数和布尔参数之间选择  

 ✔️ 如果不使用枚举，成员会具有两个或更多布尔参数，那么请使用枚举型。

 ❌ 请勿使用布尔型，除非你完全确信永远不需要两个以上的值。

 枚举型让你有空间将来添加值，但你应了解向枚举添加值所带来的全部影响，具体可查看[枚举设计](enum.md)。

 ✔️ 请考虑为是真正的双状态值且仅用于初始化布尔属性的构造函数参数使用布尔型。

### <a name="validating-arguments"></a>验证自变量

 ✔️ 请验证传递到公共、受保护或已显式实现的成员的自变量。 引发 <xref:System.ArgumentException?displayProperty=nameWithType>；如果验证失败，则引发其某个子类。

 请注意，并非一定要在公共成员或受保护成员自身进行实际验证。 在某些专用或内部例程中，也可在更低级别进行验证。 要点是被公开给最终用户的整个表面区域都对自变量进行检查。

 ✔️ 如果传递了 NULL 自变量，而成员不支持 NULL 自变量，则引发 <xref:System.ArgumentNullException>。

 ✔️ 请验证枚举参数。

 不要假设将在枚举定义的范围内的枚举自变量。 CLR 允许将任何整数值强制转换为枚举值，即使值未在枚举中定义也是如此。

 ❌ 请勿将 <xref:System.Enum.IsDefined%2A?displayProperty=nameWithType> 用于枚举范围检查。

 ✔️ 请注意可变参数在经过验证后可能会更改。

 如果成员对安全性很敏感，则请进行复制，然后再验证和处理参数。

### <a name="parameter-passing"></a>参数传递

 从框架设计者的角度来看，存在三组主要的参数：按值参数、`ref` 参数和 `out` 参数。

 当自变量通过按值参数传递时，成员会收到传入的实际自变量的副本。 如果自变量是值类型，则会在堆栈上放置自变量的副本。 如果自变量是引用类型，则会在堆栈上放置引用的副本。 最常用的 CLR 语言（例如 C#、VB.NET 和 C++）默认为按值传递参数。

 当自变量通过 `ref` 参数传递时，成员会收到对传入的实际自变量的引用。 如果自变量是值类型，则会在堆栈上放置对自变量的引用。 如果自变量是引用类型，则会在堆栈上放置对该引用的引用。 `Ref` 参数可用于允许成员修改调用方传递的自变量。

 `Out` 参数与 `ref` 参数类似，但有一些细微的区别。 参数最初被视为未分配，在分配了某个值之前无法在成员主体中读取。 此外，在成员返回之前，必须向参数分配某个值。

 ❌ 不要使用 `out` 和 `ref` 参数。

 若要使用 `out` 或 `ref` 参数，需要具有使用指针的经验，了解值类型和引用类型的区别，还能处理具有多个返回值的方法。 另外，`out` 和 `ref` 参数之间的区别并未得到广泛了解。 针对一般受众进行设计的框架架构师不应指望用户能熟练运用 `out` 或 `ref` 参数。

 ❌ 请勿按引用来传递引用类型。

 此规则存在一些有限的例外情况，例如可用于交换引用的方法。

### <a name="members-with-variable-number-of-parameters"></a>参数数目可变的成员

 可提供一个数组参数来表示采用可变数量的参数的成员。 例如，<xref:System.String> 提供以下方法：

```csharp
public class String {
    public static string Format(string format, object[] parameters);
}
```

 然后，用户可调用 <xref:System.String.Format%2A?displayProperty=nameWithType> 方法，如下所示：

 `String.Format("File {0} not found in {1}",new object[]{filename,directory});`

 如果向数组参数添加 C# params 关键字，会将参数更改为所谓的 params 数组参数，并提供用于创建临时数组的快捷方式。

```csharp
public class String {
    public static string Format(string format, params object[] parameters);
}
```

 这样，用户就可通过直接在自变量列表中传递数组元素来调用方法。

 `String.Format("File {0} not found in {1}",filename,directory);`

 请注意，params 这一关键字仅可添加到参数列表中的最后一个参数。

 ✔️ 如果预计最终用户会传递具有少量元素的数组，那么请考虑向数组参数添加 params 关键字。 如果在常见方案中将传递大量元素，那么用户将可能根本不以内联方式传递这些元素，因此不需要使用 params 关键字。

 ❌ 如果调用方几乎总是已在数组中具有输入，那么请不要使用 params 数组。

 例如，几乎永远不会通过传递单个字节来调用具有字节数组参数的成员。 因此，.NET Framework 中的字节数组参数不会使用 params 关键字。

 ❌ 如果通过采用 params 数组参数的成员修改数组，那么请勿使用 params 数组。

 事实上很多编译器会将成员的自变量转换为调用站点处的临时数组，因此该数组可能是一个临时对象，这使得对该数组的所有修改都将丢失。

 ✔️ 请考虑在简单重载中使用 params 关键字，即使更复杂的重载不可使用它也是如此。

 请自我提问，了解用户即使不在所有重载中使用 params 数组，是否也会在一个重载中使用它。

 ✔️ 请尝试对参数排序，以便可使用 params 参数。

 ✔️ 在对性能极度敏感的 API 中，请考虑对具有少量自变量的调用提供特定重载和代码路径。

 这样，当使用少量自变量调用 API 时，就能避免创建数组对象。 通过采用单数形式的数组参数并添加数字后缀来创建参数的名称。

 仅当要将完整代码路径用作特例时（不仅仅是创建数组和调用更常规的方法），才应这样操作。

 ✔️ 请注意 NULL 可作为 params 数组自变量传递。

 在处理之前，应验证数组是否不是 NULL。

 ❌ 请勿使用 `varargs` 方法（也就是省略号）。

 对于传递可变参数列表，某些 CLR 语言（例如 C++）支持替代约定（称为 `varargs` 方法）。 不得在框架中使用此约定，因为它不符合 CLS。

### <a name="pointer-parameters"></a>指针参数

 通常，指针不得出现在设计良好的托管式代码框架的公共表面区域中。 大多数情况下，应封装指针。 但在某些情况下，由于可操作性原因需要使用指针，因此在这类情况下使用指针是合适的。

 ✔️ 请对采用指针自变量的所有成员提供替代约定，原因是指针不符合 CLS。

 ❌ 不要对指针自变量执行自变量检查，此类检查成本高昂。

 ✔️ 请在使用指针设计成员时遵循与指针相关的常见约定。

 例如，无需传递开始索引，原因是可使用简单的指针算法实现这一效果。

 *Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*

 *在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines:Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
