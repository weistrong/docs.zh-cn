---
description: 了解有关以下内容的详细信息： BC30220：委托类 " <classname> " 没有 Invoke 方法，所以此类型的表达式不能作为方法调用的目标
title: 委托类“<classname>”没有 Invoke 方法，所以此类型的表达式不能作为方法调用的目标
ms.date: 07/20/2015
f1_keywords:
- vbc30220
- bc30220
helpviewer_keywords:
- BC30220
ms.assetid: 6be0d61c-f2f9-4f9b-ab90-8871a0d7206d
ms.openlocfilehash: c0d3f6e352a98e194b2c2ddca04bfa7254ec37a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796621"
---
# <a name="bc30220-delegate-class-classname-has-no-invoke-method-so-an-expression-of-this-type-cannot-be-the-target-of-a-method-call"></a><span data-ttu-id="e9030-103">BC30220：委托类 " \<classname> " 没有 Invoke 方法，所以此类型的表达式不能作为方法调用的目标</span><span class="sxs-lookup"><span data-stu-id="e9030-103">BC30220: Delegate class '\<classname>' has no Invoke method, so an expression of this type cannot be the target of a method call</span></span>

<span data-ttu-id="e9030-104">`Invoke`通过委托调用失败，因为 `Invoke` 未在委托类上实现。</span><span class="sxs-lookup"><span data-stu-id="e9030-104">A call to `Invoke` through a delegate has failed because `Invoke` is not implemented on the delegate class.</span></span>

 <span data-ttu-id="e9030-105">**错误 ID：** BC30220</span><span class="sxs-lookup"><span data-stu-id="e9030-105">**Error ID:** BC30220</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="e9030-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="e9030-106">To correct this error</span></span>

1. <span data-ttu-id="e9030-107">请确保已使用语句创建了委托类的实例 `Dim` ，并且已使用运算符将一个过程分配给了该委托实例 `AddressOf` 。</span><span class="sxs-lookup"><span data-stu-id="e9030-107">Ensure that an instance of the delegate class has been created with a `Dim` statement and that a procedure has been assigned to the delegate instance with the `AddressOf` operator.</span></span>

2. <span data-ttu-id="e9030-108">找到实现委托类的代码，并确保它实现 `Invoke` 过程。</span><span class="sxs-lookup"><span data-stu-id="e9030-108">Locate the code that implements the delegate class and make sure it implements the `Invoke` procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9030-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9030-109">See also</span></span>

- [<span data-ttu-id="e9030-110">委托</span><span class="sxs-lookup"><span data-stu-id="e9030-110">Delegates</span></span>](../../programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="e9030-111">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="e9030-111">Delegate Statement</span></span>](../statements/delegate-statement.md)
- [<span data-ttu-id="e9030-112">AddressOf 运算符</span><span class="sxs-lookup"><span data-stu-id="e9030-112">AddressOf Operator</span></span>](../operators/addressof-operator.md)
- [<span data-ttu-id="e9030-113">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="e9030-113">Dim Statement</span></span>](../statements/dim-statement.md)
