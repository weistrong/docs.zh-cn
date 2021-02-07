---
description: 了解详细信息： BC32008： " <typename> " 是委托类型
title: “<typename>”是委托类型
ms.date: 07/20/2015
f1_keywords:
- bc32008
- vbc32008
helpviewer_keywords:
- BC32008
ms.assetid: dc6abba0-a9ad-450f-8899-87265bc84abc
ms.openlocfilehash: 72aac48038c433b7938c54e7f1138a5b91bf7689
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99675021"
---
# <a name="bc32008-typename-is-a-delegate-type"></a><span data-ttu-id="6ab81-103">BC32008： " \<typename> " 是委托类型</span><span class="sxs-lookup"><span data-stu-id="6ab81-103">BC32008: '\<typename>' is a delegate type</span></span>

<span data-ttu-id="6ab81-104">" \<typename> " 是委托类型。</span><span class="sxs-lookup"><span data-stu-id="6ab81-104">'\<typename>' is a delegate type.</span></span> <span data-ttu-id="6ab81-105">委托构造仅允许将单个 AddressOf 表达式作为参数列表。</span><span class="sxs-lookup"><span data-stu-id="6ab81-105">Delegate construction permits only a single AddressOf expression as an argument list.</span></span> <span data-ttu-id="6ab81-106">通常可以使用 AddressOf 表达式，而不是委托构造。</span><span class="sxs-lookup"><span data-stu-id="6ab81-106">Often an AddressOf expression can be used instead of a delegate construction.</span></span>

 <span data-ttu-id="6ab81-107">`New`创建委托类的实例的子句为委托构造函数提供了无效的参数列表。</span><span class="sxs-lookup"><span data-stu-id="6ab81-107">A `New` clause creating an instance of a delegate class supplies an invalid argument list to the delegate constructor.</span></span>

 <span data-ttu-id="6ab81-108">`AddressOf`创建新的委托实例时，只能提供单个表达式。</span><span class="sxs-lookup"><span data-stu-id="6ab81-108">You can supply only a single `AddressOf` expression when creating a new delegate instance.</span></span>

 <span data-ttu-id="6ab81-109">如果传递多个参数，或者传递的单个自变量不是有效的表达式，则可能会导致此错误的原因 `AddressOf` 。</span><span class="sxs-lookup"><span data-stu-id="6ab81-109">This error can result if you do not pass any arguments to the delegate constructor, if you pass more than one argument, or if you pass a single argument that is not a valid `AddressOf` expression.</span></span>

 <span data-ttu-id="6ab81-110">**错误 ID：** BC32008</span><span class="sxs-lookup"><span data-stu-id="6ab81-110">**Error ID:** BC32008</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="6ab81-111">更正此错误</span><span class="sxs-lookup"><span data-stu-id="6ab81-111">To correct this error</span></span>

- <span data-ttu-id="6ab81-112">使用子句中的 `AddressOf` 委托类的参数列表中的单个表达式 `New` 。</span><span class="sxs-lookup"><span data-stu-id="6ab81-112">Use a single `AddressOf` expression in the argument list for the delegate class in the `New` clause.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ab81-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="6ab81-113">See also</span></span>

- [<span data-ttu-id="6ab81-114">新建操作员</span><span class="sxs-lookup"><span data-stu-id="6ab81-114">New Operator</span></span>](../operators/new-operator.md)
- [<span data-ttu-id="6ab81-115">AddressOf 运算符</span><span class="sxs-lookup"><span data-stu-id="6ab81-115">AddressOf Operator</span></span>](../operators/addressof-operator.md)
- [<span data-ttu-id="6ab81-116">委托</span><span class="sxs-lookup"><span data-stu-id="6ab81-116">Delegates</span></span>](../../programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="6ab81-117">如何：调用委托方法</span><span class="sxs-lookup"><span data-stu-id="6ab81-117">How to: Invoke a Delegate Method</span></span>](../../programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
