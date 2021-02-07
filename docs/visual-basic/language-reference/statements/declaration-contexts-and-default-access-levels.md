---
description: '了解详细信息： (Visual Basic 的声明上下文和默认访问级别) '
title: 声明上下文和默认访问级别
ms.date: 07/20/2015
helpviewer_keywords:
- module level, defined
- declaration contexts, Visual Basic
- procedure level, defined
- namespace level, defined
- access levels, Visual Basic
- access levels, default levels
ms.assetid: bf63b96e-e825-4745-88c8-5dae222728db
ms.openlocfilehash: c550db39862fbe9f69e5651b6e9fc7fdfcc88513
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700333"
---
# <a name="declaration-contexts-and-default-access-levels-visual-basic"></a><span data-ttu-id="01439-103">声明上下文和默认访问级别 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="01439-103">Declaration Contexts and Default Access Levels (Visual Basic)</span></span>

<span data-ttu-id="01439-104">本主题介绍了哪些 Visual Basic 类型可以在哪些其他类型中进行声明，如果未指定，它们的访问级别将默认为。</span><span class="sxs-lookup"><span data-stu-id="01439-104">This topic describes which Visual Basic types can be declared within which other types, and what their access levels default to if not specified.</span></span>  
  
## <a name="declaration-context-levels"></a><span data-ttu-id="01439-105">声明上下文级别</span><span class="sxs-lookup"><span data-stu-id="01439-105">Declaration Context Levels</span></span>  

 <span data-ttu-id="01439-106">编程元素的 *声明上下文* 是声明它的代码区域。</span><span class="sxs-lookup"><span data-stu-id="01439-106">The *declaration context* of a programming element is the region of code in which it is declared.</span></span> <span data-ttu-id="01439-107">这通常是另一个编程元素，该元素称为 " *包含元素*"。</span><span class="sxs-lookup"><span data-stu-id="01439-107">This is often another programming element, which is then called the *containing element*.</span></span>  
  
 <span data-ttu-id="01439-108">声明上下文的级别如下：</span><span class="sxs-lookup"><span data-stu-id="01439-108">The levels for declaration contexts are the following:</span></span>  
  
- <span data-ttu-id="01439-109">*命名空间级别* -在源文件或命名空间中，但不在类、结构、模块或接口中</span><span class="sxs-lookup"><span data-stu-id="01439-109">*Namespace level* — within a source file or namespace but not within a class, structure, module, or interface</span></span>  
  
- <span data-ttu-id="01439-110">*模块级别* -在类、结构、模块或接口中，但不在过程或块中</span><span class="sxs-lookup"><span data-stu-id="01439-110">*Module level* — within a class, structure, module, or interface but not within a procedure or block</span></span>  
  
- <span data-ttu-id="01439-111">*过程级别* -在过程或块中 (如 `If` 或 `For`) </span><span class="sxs-lookup"><span data-stu-id="01439-111">*Procedure level* — within a procedure or block (such as `If` or `For`)</span></span>  
  
 <span data-ttu-id="01439-112">下表显示了各种已声明的编程元素的默认访问级别，具体取决于它们的声明上下文。</span><span class="sxs-lookup"><span data-stu-id="01439-112">The following table shows the default access levels for various declared programming elements, depending on their declaration contexts.</span></span>  
  
|<span data-ttu-id="01439-113">已声明的元素</span><span class="sxs-lookup"><span data-stu-id="01439-113">Declared element</span></span>|<span data-ttu-id="01439-114">命名空间级别</span><span class="sxs-lookup"><span data-stu-id="01439-114">Namespace level</span></span>|<span data-ttu-id="01439-115">模块级别</span><span class="sxs-lookup"><span data-stu-id="01439-115">Module level</span></span>|<span data-ttu-id="01439-116">过程级别</span><span class="sxs-lookup"><span data-stu-id="01439-116">Procedure level</span></span>|  
|----------------------|---------------------|------------------|---------------------|  
|<span data-ttu-id="01439-117">变量 ([Dim 语句](dim-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-117">Variable ([Dim Statement](dim-statement.md))</span></span>|<span data-ttu-id="01439-118">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-118">Not allowed</span></span>|<span data-ttu-id="01439-119">`Private` (`Public` 在中 `Structure` ，不允许在) 中使用 `Interface`</span><span class="sxs-lookup"><span data-stu-id="01439-119">`Private` (`Public` in `Structure`, not allowed in `Interface`)</span></span>|`Public`|  
|<span data-ttu-id="01439-120">常量 ([Const 语句](const-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-120">Constant ([Const Statement](const-statement.md))</span></span>|<span data-ttu-id="01439-121">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-121">Not allowed</span></span>|<span data-ttu-id="01439-122">`Private` (`Public` 在中 `Structure` ，不允许在) 中使用 `Interface`</span><span class="sxs-lookup"><span data-stu-id="01439-122">`Private` (`Public` in `Structure`, not allowed in `Interface`)</span></span>|`Public`|  
|<span data-ttu-id="01439-123">枚举 ([枚举语句](enum-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-123">Enumeration ([Enum Statement](enum-statement.md))</span></span>|`Friend`|`Public`|<span data-ttu-id="01439-124">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-124">Not allowed</span></span>|  
|<span data-ttu-id="01439-125">类 [语句](class-statement.md) (类) </span><span class="sxs-lookup"><span data-stu-id="01439-125">Class ([Class Statement](class-statement.md))</span></span>|`Friend`|`Public`|<span data-ttu-id="01439-126">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-126">Not allowed</span></span>|  
|<span data-ttu-id="01439-127">结构 ([结构语句](structure-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-127">Structure ([Structure Statement](structure-statement.md))</span></span>|`Friend`|`Public`|<span data-ttu-id="01439-128">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-128">Not allowed</span></span>|  
|<span data-ttu-id="01439-129">Module ([Module 语句](module-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-129">Module ([Module Statement](module-statement.md))</span></span>|`Friend`|<span data-ttu-id="01439-130">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-130">Not allowed</span></span>|<span data-ttu-id="01439-131">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-131">Not allowed</span></span>|  
|<span data-ttu-id="01439-132">Interface ([Interface 语句](interface-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-132">Interface ([Interface Statement](interface-statement.md))</span></span>|`Friend`|`Public`|<span data-ttu-id="01439-133">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-133">Not allowed</span></span>|  
|<span data-ttu-id="01439-134">Procedure ([函数语句](function-statement.md)， [Sub 语句](sub-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-134">Procedure ([Function Statement](function-statement.md), [Sub Statement](sub-statement.md))</span></span>|<span data-ttu-id="01439-135">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-135">Not allowed</span></span>|`Public`|<span data-ttu-id="01439-136">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-136">Not allowed</span></span>|  
|<span data-ttu-id="01439-137">外部引用 ([声明语句](declare-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-137">External reference ([Declare Statement](declare-statement.md))</span></span>|<span data-ttu-id="01439-138">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-138">Not allowed</span></span>|<span data-ttu-id="01439-139">`Public`不允许在) 中 (`Interface`</span><span class="sxs-lookup"><span data-stu-id="01439-139">`Public` (not allowed in `Interface`)</span></span>|<span data-ttu-id="01439-140">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-140">Not allowed</span></span>|  
|<span data-ttu-id="01439-141">运算符 ([运算符语句](operator-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-141">Operator ([Operator Statement](operator-statement.md))</span></span>|<span data-ttu-id="01439-142">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-142">Not allowed</span></span>|<span data-ttu-id="01439-143">`Public``Interface`或) 不允许 (`Module`</span><span class="sxs-lookup"><span data-stu-id="01439-143">`Public` (not allowed in `Interface` or `Module`)</span></span>|<span data-ttu-id="01439-144">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-144">Not allowed</span></span>|  
|<span data-ttu-id="01439-145">Property ([属性语句](property-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-145">Property ([Property Statement](property-statement.md))</span></span>|<span data-ttu-id="01439-146">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-146">Not allowed</span></span>|`Public`|<span data-ttu-id="01439-147">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-147">Not allowed</span></span>|  
|<span data-ttu-id="01439-148">[默认属性 (默认](../modifiers/default.md)属性) </span><span class="sxs-lookup"><span data-stu-id="01439-148">Default property ([Default](../modifiers/default.md))</span></span>|<span data-ttu-id="01439-149">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-149">Not allowed</span></span>|<span data-ttu-id="01439-150">`Public`不允许在) 中 (`Module`</span><span class="sxs-lookup"><span data-stu-id="01439-150">`Public` (not allowed in `Module`)</span></span>|<span data-ttu-id="01439-151">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-151">Not allowed</span></span>|  
|<span data-ttu-id="01439-152">Event ([事件语句](event-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-152">Event ([Event Statement](event-statement.md))</span></span>|<span data-ttu-id="01439-153">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-153">Not allowed</span></span>|`Public`|<span data-ttu-id="01439-154">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-154">Not allowed</span></span>|  
|<span data-ttu-id="01439-155">委托 ([委托语句](delegate-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="01439-155">Delegate ([Delegate Statement](delegate-statement.md))</span></span>|`Friend`|`Public`|<span data-ttu-id="01439-156">不允许</span><span class="sxs-lookup"><span data-stu-id="01439-156">Not allowed</span></span>|  
  
 <span data-ttu-id="01439-157">有关详细信息，请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="01439-157">For more information, see [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01439-158">请参阅</span><span class="sxs-lookup"><span data-stu-id="01439-158">See also</span></span>

- [<span data-ttu-id="01439-159">Friend</span><span class="sxs-lookup"><span data-stu-id="01439-159">Friend</span></span>](../modifiers/friend.md)
- [<span data-ttu-id="01439-160">专用</span><span class="sxs-lookup"><span data-stu-id="01439-160">Private</span></span>](../modifiers/private.md)
- [<span data-ttu-id="01439-161">公共</span><span class="sxs-lookup"><span data-stu-id="01439-161">Public</span></span>](../modifiers/public.md)
