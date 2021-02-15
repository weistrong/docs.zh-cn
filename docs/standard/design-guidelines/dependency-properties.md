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
# <a name="dependency-properties"></a><span data-ttu-id="d3bf7-103">依赖项属性</span><span class="sxs-lookup"><span data-stu-id="d3bf7-103">Dependency Properties</span></span>

<span data-ttu-id="d3bf7-104">依赖属性 (DP) 是常规属性 - 例如，它将它的值存储在属性存储中，而不是将其存储在类型变量（字段）中。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-104">A dependency property (DP) is a regular property that stores its value in a property store instead of storing it in a type variable (field), for example.</span></span>

 <span data-ttu-id="d3bf7-105">附加依赖属性是一种作为静态 Get 和 Set 方法建模的依赖属性，这些方法表示描述对象及其容器之间关系（例如 `Button` 对象在 `Panel` 容器上的位置）的“属性”。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-105">An attached dependency property is a kind of dependency property modeled as static Get and Set methods representing "properties" describing relationships between objects and their containers (e.g., the position of a `Button` object on a `Panel` container).</span></span>

 <span data-ttu-id="d3bf7-106">✔️ 如果你需要依赖属性以支持 WPF 功能（如样式设置、触发器、数据绑定、动画、动态资源和继承），请务必提供这些属性。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-106">✔️ DO provide the dependency properties, if you need the properties to support WPF features such as styling, triggers, data binding, animations, dynamic resources, and inheritance.</span></span>

## <a name="dependency-property-design"></a><span data-ttu-id="d3bf7-107">依赖属性设计</span><span class="sxs-lookup"><span data-stu-id="d3bf7-107">Dependency Property Design</span></span>

 <span data-ttu-id="d3bf7-108">✔️ 在实现依赖属性时，请务必要从 <xref:System.Windows.DependencyObject> 或它的一个子类型继承。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-108">✔️ DO inherit from <xref:System.Windows.DependencyObject>, or one of its subtypes, when implementing dependency properties.</span></span> <span data-ttu-id="d3bf7-109">该类型提供了一种非常有效的属性存储实现，并自动支持 WPF 数据绑定。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-109">The type provides a very efficient implementation of a property store and automatically supports WPF data binding.</span></span>

 <span data-ttu-id="d3bf7-110">✔️ 请务必为每个依赖属性提供一个常规 CLR 属性和存储 <xref:System.Windows.DependencyProperty?displayProperty=nameWithType> 实例的公共静态只读字段。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-110">✔️ DO provide a regular CLR property and public static read-only field storing an instance of <xref:System.Windows.DependencyProperty?displayProperty=nameWithType> for each dependency property.</span></span>

 <span data-ttu-id="d3bf7-111">✔️ 请务必通过调用实例方法 <xref:System.Windows.DependencyObject.GetValue%2A?displayProperty=nameWithType> 和 <xref:System.Windows.DependencyObject.SetValue%2A?displayProperty=nameWithType> 来实现依赖属性。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-111">✔️ DO implement dependency properties by calling instance methods <xref:System.Windows.DependencyObject.GetValue%2A?displayProperty=nameWithType> and <xref:System.Windows.DependencyObject.SetValue%2A?displayProperty=nameWithType>.</span></span>

 <span data-ttu-id="d3bf7-112">✔️ 请务必通过在属性名称后加上“Property”后缀来命名依赖属性静态字段。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-112">✔️ DO name the dependency property static field by suffixing the name of the property with "Property."</span></span>

 <span data-ttu-id="d3bf7-113">❌ 请勿在代码中显式设置依赖属性的默认值；请改为在元数据中设置它们。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-113">❌ DO NOT set default values of dependency properties explicitly in code; set them in metadata instead.</span></span>

 <span data-ttu-id="d3bf7-114">如果你显式设置了一个属性默认值，则可能会阻止通过某些隐式方式（如样式设置）来设置该属性。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-114">If you set a property default explicitly, you might prevent that property from being set by some implicit means, such as a styling.</span></span>

 <span data-ttu-id="d3bf7-115">❌ 请勿将标准代码以外的代码置于属性访问器中来访问静态字段。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-115">❌ DO NOT put code in the property accessors other than the standard code to access the static field.</span></span>

 <span data-ttu-id="d3bf7-116">如果属性是通过隐式方式（如样式设置）设置的，则该类代码不会执行，因为样式设置直接使用静态字段。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-116">That code won’t execute if the property is set by implicit means, such as a styling, because styling uses the static field directly.</span></span>

 <span data-ttu-id="d3bf7-117">❌ 请勿使用依赖属性来存储安全数据。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-117">❌ DO NOT use dependency properties to store secure data.</span></span> <span data-ttu-id="d3bf7-118">即使是专用依赖属性，也可以公开地进行访问。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-118">Even private dependency properties can be accessed publicly.</span></span>

## <a name="attached-dependency-property-design"></a><span data-ttu-id="d3bf7-119">附加依赖属性设计</span><span class="sxs-lookup"><span data-stu-id="d3bf7-119">Attached Dependency Property Design</span></span>

 <span data-ttu-id="d3bf7-120">上一部分中所述的依赖属性表示声明类型的固有属性；例如，`Text` 属性是声明它的 `TextButton` 的属性。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-120">Dependency properties described in the preceding section represent intrinsic properties of the declaring type; for example, the `Text` property is a property of `TextButton`, which declares it.</span></span> <span data-ttu-id="d3bf7-121">附加依赖属性是一种特殊的依赖属性。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-121">A special kind of dependency property is the attached dependency property.</span></span>

 <span data-ttu-id="d3bf7-122">一个附加属性的典型示例是 <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> 属性。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-122">A classic example of an attached property is the <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="d3bf7-123">该属性表示 Button 的（而不是 Grid 的）列位置，但它只有在 Button 包含在 Grid 中时才相关，因此它通过 Grid 附加到 Button。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-123">The property represents Button’s (not Grid’s) column position, but it is only relevant if the Button is contained in a Grid, and so it's "attached" to Buttons by Grids.</span></span>

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

 <span data-ttu-id="d3bf7-124">附加属性的定义与常规依赖属性的定义大致相同，不同之处在于访问器由静态 Get 和 Set 方法表示：</span><span class="sxs-lookup"><span data-stu-id="d3bf7-124">The definition of an attached property looks mostly like that of a regular dependency property, except that the accessors are represented by static Get and Set methods:</span></span>

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

## <a name="dependency-property-validation"></a><span data-ttu-id="d3bf7-125">依赖属性验证</span><span class="sxs-lookup"><span data-stu-id="d3bf7-125">Dependency Property Validation</span></span>

 <span data-ttu-id="d3bf7-126">属性通常所实现的内容就是所谓的验证。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-126">Properties often implement what is called validation.</span></span> <span data-ttu-id="d3bf7-127">尝试更改属性的值时，将执行验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-127">Validation logic executes when an attempt is made to change the value of a property.</span></span>

 <span data-ttu-id="d3bf7-128">遗憾的是，依赖属性访问器不能包含任意的验证代码。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-128">Unfortunately dependency property accessors cannot contain arbitrary validation code.</span></span> <span data-ttu-id="d3bf7-129">而需要在属性注册期间指定依赖属性验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-129">Instead, dependency property validation logic needs to be specified during property registration.</span></span>

 <span data-ttu-id="d3bf7-130">❌ 请勿在属性的访问器中放置依赖属性验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-130">❌ DO NOT put dependency property validation logic in the property’s accessors.</span></span> <span data-ttu-id="d3bf7-131">而是将一个验证回调传递到 `DependencyProperty.Register` 方法。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-131">Instead, pass a validation callback to `DependencyProperty.Register` method.</span></span>

## <a name="dependency-property-change-notifications"></a><span data-ttu-id="d3bf7-132">依赖属性更改通知</span><span class="sxs-lookup"><span data-stu-id="d3bf7-132">Dependency Property Change Notifications</span></span>

 <span data-ttu-id="d3bf7-133">❌ 请勿在依赖属性访问器中实现更改通知逻辑。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-133">❌ DO NOT implement change notification logic in dependency property accessors.</span></span> <span data-ttu-id="d3bf7-134">依赖属性具有内置的更改通知功能，必须通过向 <xref:System.Windows.PropertyMetadata> 提供更改通知回调来使用该功能。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-134">Dependency properties have a built-in change notifications feature that must be used by supplying a change notification callback to the <xref:System.Windows.PropertyMetadata>.</span></span>

## <a name="dependency-property-value-coercion"></a><span data-ttu-id="d3bf7-135">依赖属性值强制转换</span><span class="sxs-lookup"><span data-stu-id="d3bf7-135">Dependency Property Value Coercion</span></span>

 <span data-ttu-id="d3bf7-136">在实际修改属性存储之前，若提供给属性 setter 的值被该 setter 修改，就会发生属性强制转换。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-136">Property coercion takes place when the value given to a property setter is modified by the setter before the property store is actually modified.</span></span>

 <span data-ttu-id="d3bf7-137">❌ 请勿在依赖属性访问器中实现强制转换逻辑。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-137">❌ DO NOT implement coercion logic in dependency property accessors.</span></span>

 <span data-ttu-id="d3bf7-138">依赖属性具有内置的强制转换功能，可通过向 `PropertyMetadata` 提供强制转换回调来使用该功能。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-138">Dependency properties have a built-in coercion feature, and it can be used by supplying a coercion callback to the `PropertyMetadata`.</span></span>

 <span data-ttu-id="d3bf7-139">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="d3bf7-139">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="d3bf7-140">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="d3bf7-140">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="d3bf7-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3bf7-141">See also</span></span>

- [<span data-ttu-id="d3bf7-142">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="d3bf7-142">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="d3bf7-143">常用设计模型</span><span class="sxs-lookup"><span data-stu-id="d3bf7-143">Common Design Patterns</span></span>](common-design-patterns.md)
