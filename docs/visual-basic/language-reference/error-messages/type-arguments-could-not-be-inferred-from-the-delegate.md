---
description: 了解更多相关信息： BC36564：无法从委托推断类型参数
title: 未能从委托中推理类型参数
ms.date: 07/20/2015
f1_keywords:
- bc36564
- vbc36564
helpviewer_keywords:
- BC36564
ms.assetid: 21312807-e1cd-4ac1-ae1c-c28a9c25164d
ms.openlocfilehash: 1a83ee64df4523cee87d0d677ddafaeadfe5543d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666259"
---
# <a name="bc36564-type-arguments-could-not-be-inferred-from-the-delegate"></a><span data-ttu-id="f465f-103">BC36564：无法从委托推断类型参数</span><span class="sxs-lookup"><span data-stu-id="f465f-103">BC36564: Type arguments could not be inferred from the delegate</span></span>

<span data-ttu-id="f465f-104">赋值语句使用 `AddressOf` 将泛型过程的地址赋给委托，但它不会为泛型过程提供任何类型参数。</span><span class="sxs-lookup"><span data-stu-id="f465f-104">An assignment statement uses `AddressOf` to assign the address of a generic procedure to a delegate, but it does not supply any type arguments to the generic procedure.</span></span>

 <span data-ttu-id="f465f-105">通常，在调用某个泛型类型时，要为该泛型类型定义的每个类型形参提供一个类型实参。</span><span class="sxs-lookup"><span data-stu-id="f465f-105">Normally, when you invoke a generic type, you supply a type argument for each type parameter that the generic type defines.</span></span> <span data-ttu-id="f465f-106">如果未提供任何类型实参，编译器将尝试推断要传递给类型形参的类型。</span><span class="sxs-lookup"><span data-stu-id="f465f-106">If you do not supply any type arguments, the compiler attempts to infer the types to be passed to the type parameters.</span></span> <span data-ttu-id="f465f-107">如果上下文未提供充足的信息供编译器推断类型，则将生成错误。</span><span class="sxs-lookup"><span data-stu-id="f465f-107">If the context does not provide enough information for the compiler to infer the types, an error is generated.</span></span>

 <span data-ttu-id="f465f-108">**错误 ID：** BC36564</span><span class="sxs-lookup"><span data-stu-id="f465f-108">**Error ID:** BC36564</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="f465f-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="f465f-109">To correct this error</span></span>

- <span data-ttu-id="f465f-110">为 `AddressOf` 表达式中的泛型过程指定类型参数。</span><span class="sxs-lookup"><span data-stu-id="f465f-110">Specify the type arguments for the generic procedure in the `AddressOf` expression.</span></span>

## <a name="see-also"></a><span data-ttu-id="f465f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="f465f-111">See also</span></span>

- [<span data-ttu-id="f465f-112">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f465f-112">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="f465f-113">AddressOf 运算符</span><span class="sxs-lookup"><span data-stu-id="f465f-113">AddressOf Operator</span></span>](../operators/addressof-operator.md)
- [<span data-ttu-id="f465f-114">Generic Procedures in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f465f-114">Generic Procedures in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-procedures.md)
- [<span data-ttu-id="f465f-115">Type List</span><span class="sxs-lookup"><span data-stu-id="f465f-115">Type List</span></span>](../statements/type-list.md)
- [<span data-ttu-id="f465f-116">扩展方法</span><span class="sxs-lookup"><span data-stu-id="f465f-116">Extension Methods</span></span>](../../programming-guide/language-features/procedures/extension-methods.md)
