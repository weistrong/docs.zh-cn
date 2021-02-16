---
description: 了解更多相关信息，请参阅如何：在 Visual Basic 中声明对象变量并为其分配对象
title: 如何：声明对象变量并为其分配对象
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], declaring
- declaring object variables [Visual Basic]
ms.assetid: 2fa77dde-1fb2-439a-80d4-3e9787649fad
ms.openlocfilehash: f79cda4507a3dbf2a6946dee7d909b6d1b10802d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481943"
---
# <a name="how-to-declare-an-object-variable-and-assign-an-object-to-it-in-visual-basic"></a><span data-ttu-id="d6b04-103">如何：在 Visual Basic 中声明对象变量并为它分配对象</span><span class="sxs-lookup"><span data-stu-id="d6b04-103">How to: Declare an Object Variable and Assign an Object to It in Visual Basic</span></span>

<span data-ttu-id="d6b04-104">通过[](../../../language-reference/data-types/object-data-type.md) `As Object` 在[Dim 语句](../../../language-reference/statements/dim-statement.md)中指定来声明对象数据类型的变量。</span><span class="sxs-lookup"><span data-stu-id="d6b04-104">You declare a variable of the [Object Data Type](../../../language-reference/data-types/object-data-type.md) by specifying `As Object` in a [Dim Statement](../../../language-reference/statements/dim-statement.md).</span></span> <span data-ttu-id="d6b04-105">通过 `=` 在赋值语句或初始化子句中将对象放置在等号 () 之后，可以将对象分配给此类变量。</span><span class="sxs-lookup"><span data-stu-id="d6b04-105">You assign an object to such a variable by placing the object after the equal sign (`=`) in an assignment statement or initialization clause.</span></span>

## <a name="example"></a><span data-ttu-id="d6b04-106">示例</span><span class="sxs-lookup"><span data-stu-id="d6b04-106">Example</span></span>

<span data-ttu-id="d6b04-107">下面的示例声明一个 `Object` 变量，并将当前的实例分配给它。</span><span class="sxs-lookup"><span data-stu-id="d6b04-107">The following example declares an `Object` variable and assigns the current instance to it.</span></span>

```vb
Dim thisObject As Object
thisObject = "This is an Object"
```

<span data-ttu-id="d6b04-108">可以通过将变量初始化为其声明的一部分，来合并声明和赋值。</span><span class="sxs-lookup"><span data-stu-id="d6b04-108">You can combine the declaration and assignment by initializing the variable as part of its declaration.</span></span> <span data-ttu-id="d6b04-109">下面的示例与前面的示例等效。</span><span class="sxs-lookup"><span data-stu-id="d6b04-109">The following example is equivalent to the preceding example.</span></span>

```vb
Dim thisObject As Object= "This is an Object"
```

## <a name="compile-the-code"></a><span data-ttu-id="d6b04-110">编译代码</span><span class="sxs-lookup"><span data-stu-id="d6b04-110">Compile the code</span></span>

<span data-ttu-id="d6b04-111">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="d6b04-111">This example requires:</span></span>

- <span data-ttu-id="d6b04-112">对 <xref:System> 命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="d6b04-112">A reference to the <xref:System> namespace.</span></span>

- <span data-ttu-id="d6b04-113">要在其中放置语句的类、结构或模块 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="d6b04-113">A class, structure, or module in which to put the `Dim` statement.</span></span>

- <span data-ttu-id="d6b04-114">要在其中放置赋值语句的过程。</span><span class="sxs-lookup"><span data-stu-id="d6b04-114">A procedure in which to put the assignment statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6b04-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6b04-115">See also</span></span>

- [<span data-ttu-id="d6b04-116">变量声明</span><span class="sxs-lookup"><span data-stu-id="d6b04-116">Variable Declaration</span></span>](variable-declaration.md)
- [<span data-ttu-id="d6b04-117">对象变量</span><span class="sxs-lookup"><span data-stu-id="d6b04-117">Object Variables</span></span>](object-variables.md)
- [<span data-ttu-id="d6b04-118">对象变量声明</span><span class="sxs-lookup"><span data-stu-id="d6b04-118">Object Variable Declaration</span></span>](object-variable-declaration.md)
- [<span data-ttu-id="d6b04-119">Object Data Type</span><span class="sxs-lookup"><span data-stu-id="d6b04-119">Object Data Type</span></span>](../../../language-reference/data-types/object-data-type.md)
- [<span data-ttu-id="d6b04-120">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="d6b04-120">Dim Statement</span></span>](../../../language-reference/statements/dim-statement.md)
- [<span data-ttu-id="d6b04-121">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="d6b04-121">Local Type Inference</span></span>](local-type-inference.md)
- [<span data-ttu-id="d6b04-122">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="d6b04-122">Option Strict Statement</span></span>](../../../language-reference/statements/option-strict-statement.md)
