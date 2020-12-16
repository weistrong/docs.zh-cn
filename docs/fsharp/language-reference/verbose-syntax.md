---
title: 详细语法
description: '了解 F # 编程语言中的详细和轻型语法之间的差异。'
ms.date: 05/16/2016
ms.openlocfilehash: 4e1725b58c8cb67c074ba12fd4ca25ce0c000a1e
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97595172"
---
# <a name="verbose-syntax"></a><span data-ttu-id="77407-103">详细语法</span><span class="sxs-lookup"><span data-stu-id="77407-103">Verbose Syntax</span></span>

<span data-ttu-id="77407-104">F # 语言中有两种形式的语法可用于许多构造： *详细语法* 和 *轻量语法*。</span><span class="sxs-lookup"><span data-stu-id="77407-104">There are two forms of syntax available for many constructs in the F# language: *verbose syntax* and *lightweight syntax*.</span></span> <span data-ttu-id="77407-105">详细语法并不常用，但优点在于缩进不太敏感。</span><span class="sxs-lookup"><span data-stu-id="77407-105">The verbose syntax is not as commonly used, but has the advantage of being less sensitive to indentation.</span></span> <span data-ttu-id="77407-106">轻型语法较短，并使用缩进来表示构造的开始和结束，而不是使用、、等其他关键字 `begin` `end` `in` 。</span><span class="sxs-lookup"><span data-stu-id="77407-106">The lightweight syntax is shorter and uses indentation to signal the beginning and end of constructs, rather than additional keywords like `begin`, `end`, `in`, and so on.</span></span> <span data-ttu-id="77407-107">默认语法为轻型语法。</span><span class="sxs-lookup"><span data-stu-id="77407-107">The default syntax is the lightweight syntax.</span></span> <span data-ttu-id="77407-108">本主题介绍了未启用轻量语法时 F # 构造的语法。</span><span class="sxs-lookup"><span data-stu-id="77407-108">This topic describes the syntax for F# constructs when lightweight syntax is not enabled.</span></span> <span data-ttu-id="77407-109">详细语法始终处于启用状态，因此即使启用了轻型语法，仍可对某些构造使用详细语法。</span><span class="sxs-lookup"><span data-stu-id="77407-109">Verbose syntax is always enabled, so even if you enable lightweight syntax, you can still use verbose syntax for some constructs.</span></span> <span data-ttu-id="77407-110">您可以使用指令禁用轻型语法 `#light "off"` 。</span><span class="sxs-lookup"><span data-stu-id="77407-110">You can disable lightweight syntax by using the `#light "off"` directive.</span></span>

## <a name="table-of-constructs"></a><span data-ttu-id="77407-111">构造表</span><span class="sxs-lookup"><span data-stu-id="77407-111">Table of Constructs</span></span>

<span data-ttu-id="77407-112">下表显示了上下文中的 F # 语言构造的轻型和详细语法，这两种形式之间存在差异。</span><span class="sxs-lookup"><span data-stu-id="77407-112">The following table shows the lightweight and verbose syntax for F# language constructs in contexts where there is a difference between the two forms.</span></span> <span data-ttu-id="77407-113">在此表中，尖括号 (&lt; &gt;) 将用户提供的语法元素括起来。</span><span class="sxs-lookup"><span data-stu-id="77407-113">In this table, angle brackets (&lt;&gt;) enclose user-supplied syntax elements.</span></span> <span data-ttu-id="77407-114">有关这些构造中使用的语法的更多详细信息，请参阅每个语言构造的文档。</span><span class="sxs-lookup"><span data-stu-id="77407-114">Refer to the documentation for each language construct for more detailed information about the syntax used within these constructs.</span></span>

<table>
<tr>
<th><span data-ttu-id="77407-115">语言构造</span><span class="sxs-lookup"><span data-stu-id="77407-115">Language construct</span></span></th>
<th><span data-ttu-id="77407-116">轻型语法</span><span class="sxs-lookup"><span data-stu-id="77407-116">Lightweight syntax</span></span></th>
<th><span data-ttu-id="77407-117">详细语法</span><span class="sxs-lookup"><span data-stu-id="77407-117">Verbose syntax</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="77407-118">复合表达式</span><span class="sxs-lookup"><span data-stu-id="77407-118">compound expressions</span></span>
</td>
<td>

```fsharp
<expression1>
<expression2>
```

</td><td>

```fsharp
<expression1>; <expression2>
```

</td>
</tr>
<tr><td>

<span data-ttu-id="77407-119">嵌套 `let` 绑定</span><span class="sxs-lookup"><span data-stu-id="77407-119">nested `let` bindings</span></span>

</td><td>

```fsharp
let f x =
    let a = 1
    let b = 2
    x + a + b
```

</td><td>

```fsharp
let f x =
    let a = 1 in
    let b = 2 in
    x + a + b
```

</td>
</tr>
<tr><td>
<span data-ttu-id="77407-120">代码块</span><span class="sxs-lookup"><span data-stu-id="77407-120">code block</span></span>
</td><td>

```fsharp
(
    <expression1>
    <expression2>
)
```

</td><td>

```fsharp
begin
    <expression1>;
    <expression2>;
end
```

</td>
</tr>
<tr><td>
`for...do`
</td><td>

```fsharp
for counter = start to finish do
    ...
```

</td><td>

```fsharp
for counter = start to finish do
    ...
done
```

</td>
</tr>
<tr><td>
`while...do`
</td><td>

```fsharp
while <condition> do
    ...
```

</td><td>

```fsharp
while <condition> do
    ...
done
```

</td>
</tr>
<tr><td>
`for...in`
</td><td>

```fsharp
for var in start .. finish do
    ...
```

</td><td>

```fsharp
for var in start .. finish do
    ...
done
```

</td>
</tr>
<tr><td>
`do`
</td><td>

```fsharp
do
    ...
```

</td><td>

```fsharp
do
    ...
in
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-121">记录 (record)</span><span class="sxs-lookup"><span data-stu-id="77407-121">record</span></span>
</td><td>

```fsharp
type <record-name> =
    {
        <field-declarations>
    }
    <value-or-member-definitions>
```

</td><td>

```fsharp
type <record-name> =
    {
        <field-declarations>
    }
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-122">class</span><span class="sxs-lookup"><span data-stu-id="77407-122">class</span></span>
</td><td>

```fsharp
type <class-name>(<params>) =
    ...
```

</td><td>

```fsharp
type <class-name>(<params>) =
    class
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-123">structure</span><span class="sxs-lookup"><span data-stu-id="77407-123">structure</span></span></td><td>

```fsharp
[<StructAttribute>]
type <structure-name> =
    ...
```

</td><td>

```fsharp
type <structure-name> =
    struct
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-124">可区分联合</span><span class="sxs-lookup"><span data-stu-id="77407-124">discriminated union</span></span></td><td>

```fsharp
type <union-name> =
    | ...
    | ...
    ...
    <value-or-member definitions>
```

</td><td>

```fsharp
type <union-name> =
    | ...
    | ...
    ...
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-125">interface</span><span class="sxs-lookup"><span data-stu-id="77407-125">interface</span></span></td><td>

```fsharp
type <interface-name> =
    ...
```

</td><td>

```fsharp
type <interface-name> =
    interface
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-126">对象表达式</span><span class="sxs-lookup"><span data-stu-id="77407-126">object expression</span></span></td><td>

```fsharp
{ new <type-name>
    with
        <value-or-member-definitions>
        <interface-implementations>
}
```

</td><td>

```fsharp
{ new <type-name>
    with
        <value-or-member-definitions>
    end
    <interface-implementations>
}
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-127">接口实现</span><span class="sxs-lookup"><span data-stu-id="77407-127">interface implementation</span></span></td><td>

```fsharp
interface <interface-name>
    with
        <value-or-member-definitions>
```

</td><td>

```fsharp
interface <interface-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-128">类型扩展</span><span class="sxs-lookup"><span data-stu-id="77407-128">type extension</span></span></td><td>

```fsharp
type <type-name>
    with
        <value-or-member-definitions>
```

</td><td>

```fsharp
type <type-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="77407-129">name</span><span class="sxs-lookup"><span data-stu-id="77407-129">module</span></span></td><td>

```fsharp
module <module-name> =
    ...
```

</td><td>

```fsharp
module <module-name> =
    begin
        ...
    end
```

</td>
</tr>
</table>

## <a name="see-also"></a><span data-ttu-id="77407-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77407-130">See also</span></span>

- [<span data-ttu-id="77407-131">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="77407-131">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="77407-132">编译器指令</span><span class="sxs-lookup"><span data-stu-id="77407-132">Compiler Directives</span></span>](compiler-directives.md)
- [<span data-ttu-id="77407-133">代码格式设置准则</span><span class="sxs-lookup"><span data-stu-id="77407-133">Code Formatting Guidelines</span></span>](../style-guide/formatting.md)
