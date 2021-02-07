---
description: '了解详细信息： Nothing 关键字 (Visual Basic) '
title: Nothing 关键字
ms.date: 07/20/2015
f1_keywords:
- Nothing
- vb.Nothing
helpviewer_keywords:
- Nothing keyword [Visual Basic]
- Nothing keyword [Visual Basic], syntax
ms.assetid: 06176e2d-bbf7-4a37-afaa-a86ad21ee99f
ms.openlocfilehash: c77f39c0a431dd05aabd24a235fb2dc88ea29e69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674722"
---
# <a name="nothing-keyword-visual-basic"></a><span data-ttu-id="f9f5c-103">无关键字 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="f9f5c-103">Nothing keyword (Visual Basic)</span></span>

<span data-ttu-id="f9f5c-104">表示任意数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-104">Represents the default value of any data type.</span></span> <span data-ttu-id="f9f5c-105">对于引用类型，默认值为 `null` 引用。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-105">For reference types, the default value is the `null` reference.</span></span> <span data-ttu-id="f9f5c-106">对于值类型，默认值取决于值类型是否可以为 null。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-106">For value types, the default value depends on whether the value type is nullable.</span></span>

> [!NOTE]
> <span data-ttu-id="f9f5c-107">对于不可为 null 的值类型， `Nothing` Visual Basic 中的与 c # 中的不同 `null` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-107">For non-nullable value types, `Nothing` in Visual Basic differs from `null` in C#.</span></span> <span data-ttu-id="f9f5c-108">在 Visual Basic 中，如果将不可以为 null 的值类型的变量设置为 `Nothing` ，则该变量将设置为其声明的类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-108">In Visual Basic, if you set a variable of a non-nullable value type to `Nothing`, the variable is set to the default value for its declared type.</span></span> <span data-ttu-id="f9f5c-109">在 c # 中，如果将不可以为 null 的值类型的变量分配给 `null` ，则会发生编译时错误。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-109">In C#, if you assign a variable of a non-nullable value type to `null`, a compile-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9f5c-110">备注</span><span class="sxs-lookup"><span data-stu-id="f9f5c-110">Remarks</span></span>

<span data-ttu-id="f9f5c-111">`Nothing` 表示数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-111">`Nothing` represents the default value of a data type.</span></span> <span data-ttu-id="f9f5c-112">默认值取决于变量是值类型还是引用类型。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-112">The default value depends on whether the variable is of a value type or of a reference type.</span></span>

<span data-ttu-id="f9f5c-113">*值类型* 的变量直接包含其值。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-113">A variable of a *value type* directly contains its value.</span></span> <span data-ttu-id="f9f5c-114">值类型包括所有数值数据类型、 `Boolean` 、 `Char` 、 `Date` 、所有结构和所有枚举。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-114">Value types include all numeric data types, `Boolean`, `Char`, `Date`, all structures, and all enumerations.</span></span> <span data-ttu-id="f9f5c-115">*引用类型* 的变量存储对内存中对象的实例的引用。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-115">A variable of a *reference type* stores a reference to an instance of the object in memory.</span></span> <span data-ttu-id="f9f5c-116">引用类型包括类、数组、委托和字符串。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-116">Reference types include classes, arrays, delegates, and strings.</span></span> <span data-ttu-id="f9f5c-117">有关详细信息，请参阅 [值类型和引用类型](../programming-guide/language-features/data-types/value-types-and-reference-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-117">For more information, see [Value Types and Reference Types](../programming-guide/language-features/data-types/value-types-and-reference-types.md).</span></span>

<span data-ttu-id="f9f5c-118">如果变量是值类型，则的行为 `Nothing` 取决于变量是否为可为 null 的数据类型。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-118">If a variable is of a value type, the behavior of `Nothing` depends on whether the variable is of a nullable data type.</span></span> <span data-ttu-id="f9f5c-119">若要表示可以为 null 的值类型，请向 `?` 类型名称添加修饰符。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-119">To represent a nullable value type, add a `?` modifier to the type name.</span></span> <span data-ttu-id="f9f5c-120">分配 `Nothing` 给可以为 null 的变量会将值设置为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-120">Assigning `Nothing` to a nullable variable sets the value to `null`.</span></span> <span data-ttu-id="f9f5c-121">有关详细信息和示例，请参阅 [可以为 null 的值类型](../programming-guide/language-features/data-types/nullable-value-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-121">For more information and examples, see [Nullable Value Types](../programming-guide/language-features/data-types/nullable-value-types.md).</span></span>

<span data-ttu-id="f9f5c-122">如果变量是不可为 null 的值类型，则分配 `Nothing` 给它会将它设置为其声明类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-122">If a variable is of a value type that is not nullable, assigning `Nothing` to it sets it to the default value for its declared type.</span></span> <span data-ttu-id="f9f5c-123">如果该类型包含变量成员，则它们都设置为其默认值。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-123">If that type contains variable members, they are all set to their default values.</span></span> <span data-ttu-id="f9f5c-124">下面的示例对标量类型进行了说明。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-124">The following example illustrates this for scalar types.</span></span>

[!code-vb[VbVbalrKeywords#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class2.vb#7)]

<span data-ttu-id="f9f5c-125">如果变量为引用类型，则 `Nothing` 为变量赋值会将其设置为 `null` 变量类型的引用。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-125">If a variable is of a reference type, assigning `Nothing` to the variable sets it to a `null` reference of the variable's type.</span></span> <span data-ttu-id="f9f5c-126">设置为引用的变量 `null` 不与任何对象关联。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-126">A variable that is set to a `null` reference is not associated with any object.</span></span> <span data-ttu-id="f9f5c-127">下面的示例演示这一操作：</span><span class="sxs-lookup"><span data-stu-id="f9f5c-127">The following example demonstrates this:</span></span>

[!code-vb[VbVbalrKeywords#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/class3.vb#8)]

<span data-ttu-id="f9f5c-128">当检查引用 (或可以为 null 的值类型) 变量是否为时 `null` ，请不要使用 `= Nothing` 或 `<> Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-128">When checking whether a reference (or nullable value type) variable is `null`, do not use `= Nothing` or `<> Nothing`.</span></span> <span data-ttu-id="f9f5c-129">始终使用 `Is Nothing` 或 `IsNot Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-129">Always use `Is Nothing` or `IsNot Nothing`.</span></span>

<span data-ttu-id="f9f5c-130">对于 Visual Basic 中的字符串，空字符串等于 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-130">For strings in Visual Basic, the empty string equals `Nothing`.</span></span> <span data-ttu-id="f9f5c-131">因此， `"" = Nothing` 为 true。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-131">Therefore, `"" = Nothing` is true.</span></span>

<span data-ttu-id="f9f5c-132">下面的示例演示使用 `Is` 和运算符的比较 `IsNot` ：</span><span class="sxs-lookup"><span data-stu-id="f9f5c-132">The following example shows comparisons that use the `Is` and `IsNot` operators:</span></span>

[!code-vb[VbVbalrKeywords#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class4.vb#9)]

<span data-ttu-id="f9f5c-133">如果在不使用子句的情况下声明变量 `As` 并将其设置为 `Nothing` ，则该变量的类型为 `Object` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-133">If you declare a variable without using an `As` clause and set it to `Nothing`, the variable has a type of `Object`.</span></span> <span data-ttu-id="f9f5c-134">这是一个示例 `Dim something = Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-134">An example of this is `Dim something = Nothing`.</span></span> <span data-ttu-id="f9f5c-135">当 `Option Strict` 处于打开 `Option Infer` 状态且处于关闭状态时，会发生编译时错误。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-135">A compile-time error occurs in this case when `Option Strict` is on and `Option Infer` is off.</span></span>

<span data-ttu-id="f9f5c-136">将分配 `Nothing` 给对象变量时，它将不再引用任何对象实例。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-136">When you assign `Nothing` to an object variable, it no longer refers to any object instance.</span></span> <span data-ttu-id="f9f5c-137">如果变量以前引用了某个实例，则将其设置为不 `Nothing` 会终止实例本身。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-137">If the variable had previously referred to an instance, setting it to `Nothing` does not terminate the instance itself.</span></span> <span data-ttu-id="f9f5c-138">实例终止，仅在垃圾回收器 (GC) 检测到没有剩余活动引用后，才会释放与之关联的内存和系统资源。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-138">The instance is terminated, and the memory and system resources associated with it are released, only after the garbage collector (GC) detects that there are no active references remaining.</span></span>

<span data-ttu-id="f9f5c-139">`Nothing` 与对象不同 <xref:System.DBNull> ，后者表示未初始化的变量或不存在的数据库列。</span><span class="sxs-lookup"><span data-stu-id="f9f5c-139">`Nothing` differs from the <xref:System.DBNull> object, which represents an uninitialized variant or a nonexistent database column.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9f5c-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9f5c-140">See also</span></span>

- [<span data-ttu-id="f9f5c-141">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="f9f5c-141">Dim Statement</span></span>](./statements/dim-statement.md)
- [<span data-ttu-id="f9f5c-142">对象生存期：如何创建和销毁对象</span><span class="sxs-lookup"><span data-stu-id="f9f5c-142">Object Lifetime: How Objects Are Created and Destroyed</span></span>](../programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
- [<span data-ttu-id="f9f5c-143">Visual Basic 中的生存期</span><span class="sxs-lookup"><span data-stu-id="f9f5c-143">Lifetime in Visual Basic</span></span>](../programming-guide/language-features/declared-elements/lifetime.md)
- [<span data-ttu-id="f9f5c-144">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="f9f5c-144">Is Operator</span></span>](./operators/is-operator.md)
- [<span data-ttu-id="f9f5c-145">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="f9f5c-145">IsNot Operator</span></span>](./operators/isnot-operator.md)
- [<span data-ttu-id="f9f5c-146">可以为 null 的值类型</span><span class="sxs-lookup"><span data-stu-id="f9f5c-146">Nullable Value Types</span></span>](../programming-guide/language-features/data-types/nullable-value-types.md)
