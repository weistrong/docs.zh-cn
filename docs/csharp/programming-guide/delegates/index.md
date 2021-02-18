---
title: 委托 - C# 编程指南
description: C# 中的委托是一种类型，它引用具有参数列表和返回类型的方法。 委托用于将方法作为参数传递给其他方法。
ms.date: 02/02/2021
helpviewer_keywords:
- C# language, delegates
- delegates [C#]
ms.assetid: 97de039b-c76b-4b9c-a27d-8c1e1c8d93da
ms.openlocfilehash: 0da404146f09028754087c5e24bd05b9289a4220
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100456921"
---
# <a name="delegates-c-programming-guide"></a>委托（C# 编程指南）

[委托](../../language-reference/builtin-types/reference-types.md)是一种引用类型，表示对具有特定参数列表和返回类型的方法的引用。 在实例化委托时，你可以将其实例与任何具有兼容签名和返回类型的方法相关联。 你可以通过委托实例调用方法。

委托用于将方法作为参数传递给其他方法。 事件处理程序就是通过委托调用的方法。 你可以创建一个自定义方法，当发生特定事件时，某个类（如 Windows 控件）就可以调用你的方法。 下面的示例演示了一个委托声明：

[!code-csharp[csProgGuideDelegates#20](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDelegates/CS/Delegates.cs#20)]

可将任何可访问类或结构中与委托类型匹配的任何方法分配给委托。 该方法可以是静态方法，也可以是实例方法。 此灵活性意味着你可以通过编程方式来更改方法调用，还可以向现有类中插入新代码。

> [!NOTE]
> 在方法重载的上下文中，方法的签名不包括返回值。 但在委托的上下文中，签名包括返回值。 换句话说，方法和委托必须具有相同的返回类型。

将方法作为参数进行引用的能力使委托成为定义回调方法的理想选择。 可编写一个比较应用程序中两个对象的方法。 该方法可用在排序算法的委托中。 由于比较代码与库分离，因此排序方法可能更常见。

对于类似的方案，已将[函数指针](~/_csharplang/proposals/csharp-9.0/function-pointers.md)添加到 C# 9，其中你需要对调用约定有更多的控制。 使用添加到委托类型的虚方法调用与委托关联的代码。 使用函数指针，可以指定不同的约定。

## <a name="delegates-overview"></a>委托概述

委托具有以下属性：

- 委托类似于 C++ 函数指针，但委托完全面向对象，不像 C++ 指针会记住函数，委托会同时封装对象实例和方法。
- 委托允许将方法作为参数进行传递。
- 委托可用于定义回调方法。
- 委托可以链接在一起；例如，可以对一个事件调用多个方法。
- 方法不必与委托类型完全匹配。 有关详细信息，请参阅[使用委托中的变体](../concepts/covariance-contravariance/using-variance-in-delegates.md)。
- 使用 Lambda 表达式可以更简练地编写内联代码块。 Lambda 表达式（在某些上下文中）可编译为委托类型。 若要详细了解 lambda 表达式，请参阅 [lambda 表达式](../../language-reference/operators/lambda-expressions.md)。

## <a name="in-this-section"></a>本节内容

- [使用委托](./using-delegates.md)
- [何时使用委托，而不是接口（C# 编程指南）](/previous-versions/visualstudio/visual-studio-2010/ms173173(v=vs.100))
- [带有命名方法的委托与带有匿名方法的委托](./delegates-with-named-vs-anonymous-methods.md)
- [使用委托中的变体](../concepts/covariance-contravariance/using-variance-in-delegates.md)
- [如何合并委托（多播委托）](./how-to-combine-delegates-multicast-delegates.md)
- [如何声明、实例化和使用委托](./how-to-declare-instantiate-and-use-a-delegate.md)

## <a name="c-language-specification"></a>C# 语言规范

有关详细信息，请参阅 [C# 语言规范](/dotnet/csharp/language-reference/language-specification/introduction)中的[委托](~/_csharplang/spec/delegates.md)。 该语言规范是 C# 语法和用法的权威资料。

## <a name="featured-book-chapters"></a>重要章节

- [C# 3.0 手册（第三版）：面向 C# 3.0 程序员的超过 250 个解决方案](/previous-versions/visualstudio/visual-studio-2008/ff518995(v=orm.10))中的[委托、事件和 Lambda 表达式](/previous-versions/visualstudio/visual-studio-2008/ff518994(v=orm.10))
- [学习 C# 3.0：掌握 C# 3.0 基础知识](/previous-versions/visualstudio/visual-studio-2008/ff652493(v=orm.10))中的[委托和事件](/previous-versions/visualstudio/visual-studio-2008/ff652490(v=orm.10))

## <a name="see-also"></a>请参阅

- <xref:System.Delegate>
- [C# 编程指南](../index.md)
- [事件](../events/index.md)
