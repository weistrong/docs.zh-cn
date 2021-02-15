---
description: 详细了解：依赖项属性
title: 依赖项属性
ms.date: 10/22/2008
ms.assetid: 212cfb1e-cec4-4047-94a6-47209b387f6f
ms.openlocfilehash: 78b141d6e8d1bb6bd5cf050a89aa67705111bae3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642300"
---
# <a name="dependency-properties"></a>依赖项属性

依赖属性 (DP) 是常规属性 - 例如，它将它的值存储在属性存储中，而不是将其存储在类型变量（字段）中。

 附加依赖属性是一种作为静态 Get 和 Set 方法建模的依赖属性，这些方法表示描述对象及其容器之间关系（例如 `Button` 对象在 `Panel` 容器上的位置）的“属性”。

 ✔️ 如果你需要依赖属性以支持 WPF 功能（如样式设置、触发器、数据绑定、动画、动态资源和继承），请务必提供这些属性。

## <a name="dependency-property-design"></a>依赖属性设计

 ✔️ 在实现依赖属性时，请务必要从 <xref:System.Windows.DependencyObject> 或它的一个子类型继承。 该类型提供了一种非常有效的属性存储实现，并自动支持 WPF 数据绑定。

 ✔️ 请务必为每个依赖属性提供一个常规 CLR 属性和存储 <xref:System.Windows.DependencyProperty?displayProperty=nameWithType> 实例的公共静态只读字段。

 ✔️ 请务必通过调用实例方法 <xref:System.Windows.DependencyObject.GetValue%2A?displayProperty=nameWithType> 和 <xref:System.Windows.DependencyObject.SetValue%2A?displayProperty=nameWithType> 来实现依赖属性。

 ✔️ 请务必通过在属性名称后加上“Property”后缀来命名依赖属性静态字段。

 ❌ 请勿在代码中显式设置依赖属性的默认值；请改为在元数据中设置它们。

 如果你显式设置了一个属性默认值，则可能会阻止通过某些隐式方式（如样式设置）来设置该属性。

 ❌ 请勿将标准代码以外的代码置于属性访问器中来访问静态字段。

 如果属性是通过隐式方式（如样式设置）设置的，则该类代码不会执行，因为样式设置直接使用静态字段。

 ❌ 请勿使用依赖属性来存储安全数据。 即使是专用依赖属性，也可以公开地进行访问。

## <a name="attached-dependency-property-design"></a>附加依赖属性设计

 上一部分中所述的依赖属性表示声明类型的固有属性；例如，`Text` 属性是声明它的 `TextButton` 的属性。 附加依赖属性是一种特殊的依赖属性。

 一个附加属性的典型示例是 <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> 属性。 该属性表示 Button 的（而不是 Grid 的）列位置，但它只有在 Button 包含在 Grid 中时才相关，因此它通过 Grid 附加到 Button。

```xaml
<Grid>
    <Grid.ColumnDefinitions>
        <ColumnDefinition />
        <ColumnDefinition />
    </Grid.ColumnDefinitions>

    <Button Grid.Column="0">Click</Button>
    <Button Grid.Column="1">Clack</Button>
</Grid>
```

 附加属性的定义与常规依赖属性的定义大致相同，不同之处在于访问器由静态 Get 和 Set 方法表示：

```csharp
public class Grid {

    public static int GetColumn(DependencyObject obj) {
        return (int)obj.GetValue(ColumnProperty);
    }

    public static void SetColumn(DependencyObject obj, int value) {
        obj.SetValue(ColumnProperty,value);
    }

    public static readonly DependencyProperty ColumnProperty =
        DependencyProperty.RegisterAttached(
            "Column",
            typeof(int),
            typeof(Grid)
    );
}
```

## <a name="dependency-property-validation"></a>依赖属性验证

 属性通常所实现的内容就是所谓的验证。 尝试更改属性的值时，将执行验证逻辑。

 遗憾的是，依赖属性访问器不能包含任意的验证代码。 而需要在属性注册期间指定依赖属性验证逻辑。

 ❌ 请勿在属性的访问器中放置依赖属性验证逻辑。 而是将一个验证回调传递到 `DependencyProperty.Register` 方法。

## <a name="dependency-property-change-notifications"></a>依赖属性更改通知

 ❌ 请勿在依赖属性访问器中实现更改通知逻辑。 依赖属性具有内置的更改通知功能，必须通过向 <xref:System.Windows.PropertyMetadata> 提供更改通知回调来使用该功能。

## <a name="dependency-property-value-coercion"></a>依赖属性值强制转换

 在实际修改属性存储之前，若提供给属性 setter 的值被该 setter 修改，就会发生属性强制转换。

 ❌ 请勿在依赖属性访问器中实现强制转换逻辑。

 依赖属性具有内置的强制转换功能，可通过向 `PropertyMetadata` 提供强制转换回调来使用该功能。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [常用设计模型](common-design-patterns.md)
