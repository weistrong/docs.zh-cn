---
description: 详细了解：运算符重载
title: 运算符重载
ms.date: 10/22/2008
helpviewer_keywords:
- operators [.NET Framework], overloads
- names [.NET Framework], overloaded operators
- member design guidelines, operators
- overloaded operators
ms.assetid: 37585bf2-4c27-4dee-849a-af70e3338cc1
ms.openlocfilehash: e6552f35081afa542e4dc14239206a63c7c1bd59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713320"
---
# <a name="operator-overloads"></a>运算符重载

运算符重载可以使框架类型看起来像是内置语言基元一样。

 尽管运算符重载在某些情况下是允许使用的，而且很有用，但还是应该谨慎使用它们。 在许多情况下，运算符重载被滥用，例如当框架设计者开始使用运算符来执行本应是简单方法的运算时。 以下准则应该可帮助你决定何时以及如何使用运算符重载。

 ❌ 请避免定义运算符重载，除非在感觉像是基元（内置）类型的类型中。

 ✔️ 请考虑在一个感觉像是基元类型的类型中定义运算符重载。

 例如，<xref:System.String?displayProperty=nameWithType> 定义了 `operator==` 和 `operator!=`。

 ✔️ 请务必在表示数字的结构（如 <xref:System.Decimal?displayProperty=nameWithType>）中定义运算符重载。

 ❌ 在定义运算符重载时请勿太刻意。

 运算符重载在运算结果显而易见的情况下非常有用。 例如，能够从另一个 `DateTime` 中减去一个 <xref:System.DateTime> 并得到一个 <xref:System.TimeSpan>，这是有意义的。 但是，以下操作是不恰当的：使用逻辑 union 运算符来联合两个数据库查询或使用 shift 运算符写入到流中。

 ❌ 除非至少有一个操作数属于定义重载的类型，否则请勿提供运算符重载。

 ✔️ 请确保以对称方式重载运算符。

 例如，如果你重载了 `operator==`，则还应重载 `operator!=`。 同样，如果你重载了 `operator<`，则还应重载 `operator>`，诸如此类。

 ✔️ 请考虑为方法提供与每个重载的运算符相对应的友好名称。

 许多语言不支持运算符重载。 出于此原因，建议重载运算符的类型包含一个辅助方法，该方法具有适当的特定于域的名称且提供等效功能。

 下表包含一个运算符列表及相应的友好方法名称。

|C# 运算符符号|元数据名称|友好名称|
|-------------------------|-------------------|-------------------|
|`N/A`|`op_Implicit`|`To<TypeName>/From<TypeName>`|
|`N/A`|`op_Explicit`|`To<TypeName>/From<TypeName>`|
|`+ (binary)`|`op_Addition`|`Add`|
|`- (binary)`|`op_Subtraction`|`Subtract`|
|`* (binary)`|`op_Multiply`|`Multiply`|
|`/`|`op_Division`|`Divide`|
|`%`|`op_Modulus`|`Mod or Remainder`|
|`^`|`op_ExclusiveOr`|`Xor`|
|`& (binary)`|`op_BitwiseAnd`|`BitwiseAnd`|
|<code>&#124;</code>|`op_BitwiseOr`|`BitwiseOr`|
|`&&`|`op_LogicalAnd`|`And`|
|<code>&#124;&#124;</code>|`op_LogicalOr`|`Or`|
|`=`|`op_Assign`|`Assign`|
|`<<`|`op_LeftShift`|`LeftShift`|
|`>>`|`op_RightShift`|`RightShift`|
|`N/A`|`op_SignedRightShift`|`SignedRightShift`|
|`N/A`|`op_UnsignedRightShift`|`UnsignedRightShift`|
|`==`|`op_Equality`|`Equals`|
|`!=`|`op_Inequality`|`Equals`|
|`>`|`op_GreaterThan`|`CompareTo`|
|`<`|`op_LessThan`|`CompareTo`|
|`>=`|`op_GreaterThanOrEqual`|`CompareTo`|
|`<=`|`op_LessThanOrEqual`|`CompareTo`|
|`*=`|`op_MultiplicationAssignment`|`Multiply`|
|`-=`|`op_SubtractionAssignment`|`Subtract`|
|`^=`|`op_ExclusiveOrAssignment`|`Xor`|
|`<<=`|`op_LeftShiftAssignment`|`LeftShift`|
|`%=`|`op_ModulusAssignment`|`Mod`|
|`+=`|`op_AdditionAssignment`|`Add`|
|`&=`|`op_BitwiseAndAssignment`|`BitwiseAnd`|
|<code>&#124;=</code>|`op_BitwiseOrAssignment`|`BitwiseOr`|
|`,`|`op_Comma`|`Comma`|
|`/=`|`op_DivisionAssignment`|`Divide`|
|`--`|`op_Decrement`|`Decrement`|
|`++`|`op_Increment`|`Increment`|
|`- (unary)`|`op_UnaryNegation`|`Negate`|
|`+ (unary)`|`op_UnaryPlus`|`Plus`|
|`~`|`op_OnesComplement`|`OnesComplement`|

### <a name="overloading-operator-"></a>重载运算符 ==

 重载 `operator ==` 非常复杂。 该运算符的语义需要与其他一些成员（如 <xref:System.Object.Equals%2A?displayProperty=nameWithType>）兼容。

### <a name="conversion-operators"></a>转换运算符

 转换运算符是允许从一种类型转换为另一种类型的一元运算符。 该运算符必须对操作数或返回类型定义为静态成员。 有两种类型的转换运算符：隐式和显式。

 ❌ 如果最终用户没有明确期望进行此类转换，请勿提供转换运算符。

 ❌ 请勿在类型的域外定义转换运算符。

 例如，<xref:System.Int32>、<xref:System.Double> 和 <xref:System.Decimal> 均为数值类型，而 <xref:System.DateTime> 则不是。 因此，应该没有转换运算符能够将 `Double(long)` 转换为 `DateTime`。 在这种情况下，首选使用构造函数。

 ❌ 如果转换可能有损，请勿提供隐式转换运算符。

 例如，不应存在从 `Double` 到 `Int32` 的隐式转换，因为 `Double` 的范围比 `Int32` 大。 即使转换可能会有损，也可以提供显式转换运算符。

 ❌ 请勿从隐式强制转换引发异常。

 最终用户很难了解发生的情况，因为他们可能没有意识到正在进行转换。

 ✔️ 如果对强制转换运算符的调用导致有损转换，而该运算符的协定不允许有损转换，请务必引发 <xref:System.InvalidCastException?displayProperty=nameWithType>。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
