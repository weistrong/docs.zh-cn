---
description: 引用类型 - C# 参考
title: 引用类型 - C# 参考
ms.date: 07/20/2015
f1_keywords:
- cs.referencetypes
helpviewer_keywords:
- reference types [C#]
- C# language, reference types
- types [C#], reference types
ms.assetid: 801cf030-6e2d-4a0d-9daf-1431b0c31f47
ms.openlocfilehash: 075ec5ecd8f71f5cb85bab0e2baff56409709191
ms.sourcegitcommit: 88fbb019b84c2d044d11fb4f6004aec07f2b25b1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/05/2021
ms.locfileid: "97899608"
---
# <a name="reference-types-c-reference"></a><span data-ttu-id="525dd-103">引用类型（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="525dd-103">Reference types (C# Reference)</span></span>

<span data-ttu-id="525dd-104">C# 中有两种类型：引用类型和值类型。</span><span class="sxs-lookup"><span data-stu-id="525dd-104">There are two kinds of types in C#: reference types and value types.</span></span> <span data-ttu-id="525dd-105">引用类型的变量存储对其数据（对象）的引用，而值类型的变量直接包含其数据。</span><span class="sxs-lookup"><span data-stu-id="525dd-105">Variables of reference types store references to their data (objects), while variables of value types directly contain their data.</span></span> <span data-ttu-id="525dd-106">对于引用类型，两种变量可引用同一对象；因此，对一个变量执行的操作会影响另一个变量所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="525dd-106">With reference types, two variables can reference the same object; therefore, operations on one variable can affect the object referenced by the other variable.</span></span> <span data-ttu-id="525dd-107">对于值类型，每个变量都具有其自己的数据副本，对一个变量执行的操作不会影响另一个变量（in、ref 和 out 参数变量除外；请参阅 [in](in-parameter-modifier.md)、[ref](ref.md) 和 [out](out-parameter-modifier.md) 参数修饰符）。</span><span class="sxs-lookup"><span data-stu-id="525dd-107">With value types, each variable has its own copy of the data, and it is not possible for operations on one variable to affect the other (except in the case of in, ref and out parameter variables; see [in](in-parameter-modifier.md), [ref](ref.md) and [out](out-parameter-modifier.md) parameter modifier).</span></span>

 <span data-ttu-id="525dd-108">下列关键字用于声明引用类型：</span><span class="sxs-lookup"><span data-stu-id="525dd-108">The following keywords are used to declare reference types:</span></span>

- [<span data-ttu-id="525dd-109">class</span><span class="sxs-lookup"><span data-stu-id="525dd-109">class</span></span>](class.md)

- [<span data-ttu-id="525dd-110">interface</span><span class="sxs-lookup"><span data-stu-id="525dd-110">interface</span></span>](interface.md)

- [<span data-ttu-id="525dd-111">delegate</span><span class="sxs-lookup"><span data-stu-id="525dd-111">delegate</span></span>](../builtin-types/reference-types.md)
- [<span data-ttu-id="525dd-112">record</span><span class="sxs-lookup"><span data-stu-id="525dd-112">record</span></span>](../builtin-types/reference-types.md)

 <span data-ttu-id="525dd-113">C# 也提供了下列内置引用类型：</span><span class="sxs-lookup"><span data-stu-id="525dd-113">C# also provides the following built-in reference types:</span></span>

- [<span data-ttu-id="525dd-114">dynamic</span><span class="sxs-lookup"><span data-stu-id="525dd-114">dynamic</span></span>](../builtin-types/reference-types.md)

- [<span data-ttu-id="525dd-115">object</span><span class="sxs-lookup"><span data-stu-id="525dd-115">object</span></span>](../builtin-types/reference-types.md)

- [<span data-ttu-id="525dd-116">string</span><span class="sxs-lookup"><span data-stu-id="525dd-116">string</span></span>](../builtin-types/reference-types.md)

## <a name="see-also"></a><span data-ttu-id="525dd-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="525dd-117">See also</span></span>

- [<span data-ttu-id="525dd-118">C# 参考</span><span class="sxs-lookup"><span data-stu-id="525dd-118">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="525dd-119">C# 关键字</span><span class="sxs-lookup"><span data-stu-id="525dd-119">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="525dd-120">指针类型</span><span class="sxs-lookup"><span data-stu-id="525dd-120">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="525dd-121">值类型</span><span class="sxs-lookup"><span data-stu-id="525dd-121">Value types</span></span>](../builtin-types/value-types.md)
