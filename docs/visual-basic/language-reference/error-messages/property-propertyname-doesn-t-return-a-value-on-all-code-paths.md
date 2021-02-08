---
description: 了解有关以下内容的详细信息： BC42107：属性 " <propertyname> " 不会在所有代码路径上都返回值
title: 属性“<propertyname>”并非在所有代码路径上都返回值
ms.date: 07/20/2015
f1_keywords:
- bc42107
- vbc42107
helpviewer_keywords:
- BC42107
ms.assetid: 06800966-9c3b-4844-9f13-83ac95607d32
ms.openlocfilehash: 9aa0d6fea1feeaf7503f5f8831fbd3de910a4822
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774884"
---
# <a name="bc42107-property-propertyname-doesnt-return-a-value-on-all-code-paths"></a><span data-ttu-id="69bc3-103">BC42107：属性 " \<propertyname> " 不会在所有代码路径上都返回值</span><span class="sxs-lookup"><span data-stu-id="69bc3-103">BC42107: Property '\<propertyname>' doesn't return a value on all code paths</span></span>

<span data-ttu-id="69bc3-104">属性 " \<propertyname> " 不会在所有代码路径上都返回值。</span><span class="sxs-lookup"><span data-stu-id="69bc3-104">Property '\<propertyname>' doesn't return a value on all code paths.</span></span> <span data-ttu-id="69bc3-105">使用该结果时，可能会在运行时发生 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="69bc3-105">A null reference exception could occur at run time when the result is used.</span></span>

<span data-ttu-id="69bc3-106">属性 `Get` 过程至少有一个可能的路径，其代码中不返回值。</span><span class="sxs-lookup"><span data-stu-id="69bc3-106">A property `Get` procedure has at least one possible path through its code that does not return a value.</span></span>

 <span data-ttu-id="69bc3-107">可以通过 `Get` 以下任一方式从属性过程返回值：</span><span class="sxs-lookup"><span data-stu-id="69bc3-107">You can return a value from a property `Get` procedure in any of the following ways:</span></span>

- <span data-ttu-id="69bc3-108">将值分配给属性名称，然后执行 `Exit Property` 语句。</span><span class="sxs-lookup"><span data-stu-id="69bc3-108">Assign the value to the property name and then perform an `Exit Property` statement.</span></span>

- <span data-ttu-id="69bc3-109">将值分配给属性名称，然后执行 `End Get` 语句。</span><span class="sxs-lookup"><span data-stu-id="69bc3-109">Assign the value to the property name and then perform the `End Get` statement.</span></span>

- <span data-ttu-id="69bc3-110">在 [Return 语句](../statements/return-statement.md)中包含值。</span><span class="sxs-lookup"><span data-stu-id="69bc3-110">Include the value in a [Return Statement](../statements/return-statement.md).</span></span>

<span data-ttu-id="69bc3-111">如果控件传递给 `Exit Property` 或 `End Get` ，并且没有为属性名称分配任何值，则该 `Get` 过程将返回属性数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="69bc3-111">If control passes to `Exit Property` or `End Get` and you have not assigned any value to the property name, the `Get` procedure returns the default value of the property's data type.</span></span> <span data-ttu-id="69bc3-112">有关详细信息，请参阅 [Function 语句](../statements/function-statement.md)中的 "行为"。</span><span class="sxs-lookup"><span data-stu-id="69bc3-112">For more information, see "Behavior" in [Function Statement](../statements/function-statement.md).</span></span>

<span data-ttu-id="69bc3-113">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="69bc3-113">By default, this message is a warning.</span></span> <span data-ttu-id="69bc3-114">有关隐藏警告或将警告视为错误的详细信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="69bc3-114">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

<span data-ttu-id="69bc3-115">**错误 ID：** BC42107</span><span class="sxs-lookup"><span data-stu-id="69bc3-115">**Error ID:** BC42107</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="69bc3-116">更正此错误</span><span class="sxs-lookup"><span data-stu-id="69bc3-116">To correct this error</span></span>

- <span data-ttu-id="69bc3-117">检查控制流逻辑，并确保在导致返回的每个语句之前赋值。</span><span class="sxs-lookup"><span data-stu-id="69bc3-117">Check your control flow logic and make sure you assign a value before every statement that causes a return.</span></span>

  <span data-ttu-id="69bc3-118">如果始终使用语句，则更容易保证每次从过程返回一个值 `Return` 。</span><span class="sxs-lookup"><span data-stu-id="69bc3-118">It's easier to guarantee that every return from the procedure returns a value if you always use the `Return` statement.</span></span> <span data-ttu-id="69bc3-119">如果执行此操作，则之前的最后一个语句 `End Get` 应为 `Return` 语句。</span><span class="sxs-lookup"><span data-stu-id="69bc3-119">If you do this, the last statement before `End Get` should be a `Return` statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="69bc3-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="69bc3-120">See also</span></span>

- [<span data-ttu-id="69bc3-121">Property 过程</span><span class="sxs-lookup"><span data-stu-id="69bc3-121">Property Procedures</span></span>](../../programming-guide/language-features/procedures/property-procedures.md)
- [<span data-ttu-id="69bc3-122">Property Statement</span><span class="sxs-lookup"><span data-stu-id="69bc3-122">Property Statement</span></span>](../statements/property-statement.md)
- [<span data-ttu-id="69bc3-123">Get 语句</span><span class="sxs-lookup"><span data-stu-id="69bc3-123">Get Statement</span></span>](../statements/get-statement.md)
