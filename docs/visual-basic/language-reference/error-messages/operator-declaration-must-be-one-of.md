---
description: 了解详细信息： BC33000：运算符声明必须是以下之一： +,-, *、、/、^、 &amp; 、Like、Mod、And、Or、Xor、Not、 <<、 >> .。。
title: 运算符声明必须是以下其中之一： +,-, *,-,-, ^、 &amp; 、Like、Mod、And、Or、Xor、Not、 <<、 >>、=、 <>、<、<=、>、>=、CType、IsTrue、IsFalse
ms.date: 07/20/2015
f1_keywords:
- bc33000
- vbc33000
helpviewer_keywords:
- BC33000
ms.assetid: 15c5d8eb-3a8c-4141-8f41-33151afabf97
ms.openlocfilehash: 0ad82a6414387278622a10624952ebc35e7e9b83
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795555"
---
# <a name="bc33000-operator-declaration-must-be-one-of----amp-like-mod-and-or-xor-not--"></a><span data-ttu-id="ce881-103">BC33000：运算符声明必须是以下之一： +,-, \*、 \, /、^、 &amp; 、Like、Mod、And、Or、Xor、Not、 \<\<, >> .。。</span><span class="sxs-lookup"><span data-stu-id="ce881-103">BC33000: Operator declaration must be one of:  +,-,\*,\,/,^, &amp;, Like, Mod, And, Or, Xor, Not, \<\<, >>...</span></span>

<span data-ttu-id="ce881-104">您只能声明一个适合重载的运算符。</span><span class="sxs-lookup"><span data-stu-id="ce881-104">You can declare only an operator that is eligible for overloading.</span></span> <span data-ttu-id="ce881-105">下表列出了可以声明的运算符。</span><span class="sxs-lookup"><span data-stu-id="ce881-105">The following table lists the operators you can declare.</span></span>

|<span data-ttu-id="ce881-106">类型</span><span class="sxs-lookup"><span data-stu-id="ce881-106">Type</span></span>|<span data-ttu-id="ce881-107">运算符</span><span class="sxs-lookup"><span data-stu-id="ce881-107">Operators</span></span>|
|----------|---------------|
|<span data-ttu-id="ce881-108">一元</span><span class="sxs-lookup"><span data-stu-id="ce881-108">Unary</span></span>|<span data-ttu-id="ce881-109">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span><span class="sxs-lookup"><span data-stu-id="ce881-109">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span></span>|
|<span data-ttu-id="ce881-110">二进制</span><span class="sxs-lookup"><span data-stu-id="ce881-110">Binary</span></span>|<span data-ttu-id="ce881-111">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span><span class="sxs-lookup"><span data-stu-id="ce881-111">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span></span>|
|<span data-ttu-id="ce881-112">转换（一元）</span><span class="sxs-lookup"><span data-stu-id="ce881-112">Conversion (unary)</span></span>|`CType`|

 <span data-ttu-id="ce881-113">请注意， `=` 二元列表中的运算符是比较运算符，而不是赋值运算符。</span><span class="sxs-lookup"><span data-stu-id="ce881-113">Note that the `=` operator in the binary list is the comparison operator, not the assignment operator.</span></span>

 <span data-ttu-id="ce881-114">**错误 ID：** BC33000</span><span class="sxs-lookup"><span data-stu-id="ce881-114">**Error ID:** BC33000</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="ce881-115">更正此错误</span><span class="sxs-lookup"><span data-stu-id="ce881-115">To correct this error</span></span>

- <span data-ttu-id="ce881-116">从一组可重载运算符中选择一个运算符。</span><span class="sxs-lookup"><span data-stu-id="ce881-116">Select an operator from the set of overloadable operators.</span></span>

- <span data-ttu-id="ce881-117">如果你需要重载无法直接重载的运算符这一功能，请创建用于获取适当参数并返回适当值的 `Function` 过程。</span><span class="sxs-lookup"><span data-stu-id="ce881-117">If you need the functionality of overloading an operator that you cannot overload directly, create a `Function` procedure that takes the appropriate parameters and returns the appropriate value.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce881-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="ce881-118">See also</span></span>

- [<span data-ttu-id="ce881-119">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="ce881-119">Operator Statement</span></span>](../statements/operator-statement.md)
- [<span data-ttu-id="ce881-120">运算符过程</span><span class="sxs-lookup"><span data-stu-id="ce881-120">Operator Procedures</span></span>](../../programming-guide/language-features/procedures/operator-procedures.md)
- [<span data-ttu-id="ce881-121">如何：定义运算符</span><span class="sxs-lookup"><span data-stu-id="ce881-121">How to: Define an Operator</span></span>](../../programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="ce881-122">如何：定义转换运算符</span><span class="sxs-lookup"><span data-stu-id="ce881-122">How to: Define a Conversion Operator</span></span>](../../programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="ce881-123">Function 语句</span><span class="sxs-lookup"><span data-stu-id="ce881-123">Function Statement</span></span>](../statements/function-statement.md)
