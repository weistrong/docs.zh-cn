---
description: 了解详细信息： Property 语句
title: Property Statement
ms.date: 05/12/2018
f1_keywords:
- vb.PropertySet
- vb.Property
- vb.PropertyGet
helpviewer_keywords:
- Property statement [Visual Basic]
- default modifier
- property procedures [Visual Basic], Property statements
- Property keyword [Visual Basic]
ms.assetid: 3155edaf-8ebd-45c6-9cef-11d5d2dc8d38
ms.openlocfilehash: 95f2ac1f993fc8698d2033dfe50d925cd55a7dc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741388"
---
# <a name="property-statement"></a>Property Statement

声明属性的名称，以及用于存储和检索属性值的属性过程。

## <a name="syntax"></a>语法

```vb
[ <attributelist> ] [ Default ] [ accessmodifier ]
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ] [ Iterator ]
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]
    [ <attributelist> ] [ accessmodifier ] Get
        [ statements ]
    End Get
    [ <attributelist> ] [ accessmodifier ] Set ( ByVal value As returntype [, parameterlist ] )
        [ statements ]
    End Set
End Property
- or -
[ <attributelist> ] [ Default ] [ accessmodifier ]
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ]
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]
```

## <a name="parts"></a>组成部分

- `attributelist`

  可选。 应用于此属性或或过程的特性的列表 `Get` `Set` 。 请参阅 [特性列表](attribute-list.md)。

- `Default`

  可选。 指定此属性是在其上定义该属性的类或结构的默认属性。 默认属性必须接受参数，并且可以在不指定属性名称的情况下进行设置和检索。 如果将属性声明为 `Default` ，则不能 `Private` 对属性或其任一属性过程使用。

- `accessmodifier`

  语句上的可选 `Property` ，最多一个 `Get` 和 `Set` 语句。 可以是以下其中一个值：

  - [公共](../modifiers/public.md)

  - [Protected](../modifiers/protected.md)

  - [Friend](../modifiers/friend.md)

  - [专用](../modifiers/private.md)

  - [Protected Friend](../modifiers/protected-friend.md)

  - [Private Protected](../modifiers/private-protected.md)

  请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。

- `propertymodifiers`

  可选。 可以是以下其中一个值：

  - [重载](../modifiers/overloads.md)

  - [替代](../modifiers/overrides.md)

  - [Overrides](../modifiers/overridable.md)

  - [NotOverridable](../modifiers/notoverridable.md)

  - [New](../modifiers/mustoverride.md)

  - `MustOverride Overrides`

  - `NotOverridable Overrides`

- `Shared`

  可选。 请参阅 [共享](../modifiers/shared.md)。

- `Shadows`

  可选。 请参阅 [阴影](../modifiers/shadows.md)。

- `ReadOnly`

  可选。 请参阅 [ReadOnly](../modifiers/readonly.md)。

- `WriteOnly`

  可选。 请参阅 [WriteOnly](../modifiers/writeonly.md)。

- `Iterator`

  可选。 请参阅 [迭代器](../modifiers/iterator.md)。

- `name`

  必需。 属性的名称。 请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。

- `parameterlist`

  可选。 表示此属性的参数的局部变量名称的列表，以及此过程的可能的其他参数 `Set` 。 请参阅 [参数列表](parameter-list.md)。

- `returntype`

  如果 `Option Strict` 为，则为必需 `On` 。 此属性返回的值的数据类型。

- `Implements`

  可选。 指示此属性实现一个或多个属性，每个属性都是由该属性的包含类或结构实现的接口中定义的。 请参阅 [Implements 语句](implements-statement.md)。

- `implementslist`

  如果提供 `Implements`，则是必需的。 要实现的属性列表。

  `implementedproperty [ , implementedproperty ... ]`

  每个 `implementedproperty` 都具有以下语法和部件：

  `interface.definedname`

  |组成部分|说明|
  |---|---|
  |`interface`|必需。 此属性的包含类或结构实现的接口的名称。|
  |`definedname`|必需。 在其中定义属性的名称 `interface` 。|

- `Get`

  可选。 如果已标记属性，则为必需 `ReadOnly` 。 启动 `Get` 用于返回属性值的属性过程。  `Get`语句不与[自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)一起使用。

- `statements`

  可选。 要在或过程中运行的语句块 `Get` `Set` 。

- `End Get`

  终止 `Get` 属性过程。

- `Set`

  可选。 如果已标记属性，则为必需 `WriteOnly` 。 启动 `Set` 用于存储属性值的属性过程。  `Set`语句不与[自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)一起使用。

- `End Set`

  终止 `Set` 属性过程。

- `End Property`

  终止此属性的定义。

## <a name="remarks"></a>备注

`Property`语句引入属性的声明。 属性可以有一个 `Get` 过程 (只读) 、 `Set` 过程 (只写) ，或是同时 (读写) 。 `Get` `Set` 使用自动实现的属性时，可以忽略和过程。 有关详细信息，请参阅[自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)。

只能 `Property` 在类级别使用。 这意味着属性的 *声明上下文* 必须是类、结构、模块或接口，不能是源文件、命名空间、过程或块。 有关详细信息，请参阅[声明上下文和默认访问级别](declaration-contexts-and-default-access-levels.md)。

默认情况下，属性使用公共访问。 您可以在语句中使用访问修饰符调整属性的访问级别 `Property` ，还可以根据需要将其一个属性过程调整到限制性更强的访问级别。

Visual Basic `Set` 在属性分配过程中将参数传递给过程。 如果未提供参数 `Set` ，则集成开发环境 (IDE) 使用名为的隐式参数 `value` 。 此参数保存要赋给属性的值。 通常将此值存储在私有本地变量中，并在 `Get` 调用过程时返回。

## <a name="rules"></a>规则

- **混合访问级别。** 如果要定义读写属性，则可以选择为或过程指定不同的访问级别 `Get` `Set` ，但不能同时指定两者。 如果执行此操作，则过程访问级别必须比属性的访问级别更严格。 例如，如果声明了属性 `Friend` ，则可以声明该 `Set` 过程 `Private` ，而不是 `Public` 。

  如果要定义 `ReadOnly` 或 `WriteOnly` 属性，则单个属性过程 (`Get` 或 `Set` 分别) 表示所有属性。 不能为此类过程声明不同的访问级别，因为这会为属性设置两个访问级别。

- **返回类型。** `Property`语句可以声明其返回的值的数据类型。 您可以指定任何数据类型或枚举、结构、类或接口的名称。

  如果不指定 `returntype` ，则属性将返回 `Object` 。

- **部署.** 如果此属性使用 `Implements` 关键字，则包含类或结构必须 `Implements` 紧跟在其或语句后面的 `Class` 语句 `Structure` 。 `Implements`语句必须包括中指定的每个接口 `implementslist` 。 但是，接口用于定义) 中的 (的名称不必与 `Property` `definedname`) 中 (的此属性的名称相同 `name` 。

## <a name="behavior"></a>行为

- **从属性过程返回。** 当 `Get` 或 `Set` 过程返回到调用代码时，执行将继续执行调用它的语句后面的语句。

  `Exit Property`和 `Return` 语句导致直接从属性过程退出。 任意数量的 `Exit Property` 和 `Return` 语句可以出现在过程中的任何位置，并且可以混合使用 `Exit Property` 和 `Return` 语句。

- **返回值。** 若要从过程返回值 `Get` ，可以将值分配给属性名称，或者将其包含在 `Return` 语句中。 下面的示例将返回值分配给属性名称 `quoteForTheDay` ，然后使用 `Exit Property` 语句返回。

  [!code-vb[VbVbalrStatements#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#27)]

  [!code-vb[VbVbalrStatements#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#28)]

  如果在 `Exit Property` 不向赋值的情况下使用 `name` ，则该 `Get` 过程将返回属性数据类型的默认值。

  `Return`语句同时分配 `Get` 过程返回值并退出该过程。 下面的示例显示了这种情况。

  [!code-vb[VbVbalrStatements#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#27)]

  [!code-vb[VbVbalrStatements#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#29)]

## <a name="example"></a>示例

下面的示例声明类中的一个属性。

[!code-vb[VbVbalrStatements#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#51)]

## <a name="see-also"></a>请参阅

- [自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)
- [对象和类](../../programming-guide/language-features/objects-and-classes/index.md)
- [Get 语句](get-statement.md)
- [Set 语句](set-statement.md)
- [参数列表](parameter-list.md)
- [默认](../modifiers/default.md)
